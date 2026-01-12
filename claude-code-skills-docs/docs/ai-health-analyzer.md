# AI Health Analyzer Skill

## Overview

The AI Health Analyzer is a specialized Agent Skill for Claude Code that provides expert-level diagnostics and troubleshooting capabilities for production AI systems. It's designed for teams running conversational AI, RAG systems, and multi-agent architectures at scale.

## Key Capabilities

### 1. Log Analysis

- **Pattern Recognition**: Automatically identifies error patterns and frequencies
- **Cascading Failure Detection**: Spots related failures across system components
- **Correlation Analysis**: Links errors with system state changes
- **Root Cause Identification**: Provides evidence-based root cause analysis

### 2. API Failure Analysis

- **Rate Limit Detection**: Identifies 429 errors and quota issues
- **Retry Logic Evaluation**: Analyzes exponential backoff implementation
- **Request Batching**: Suggests optimization for API call patterns
- **Cost Optimization**: Monitors token usage and suggests savings

### 3. RAG Pipeline Health

- **Retrieval Quality**: Analyzes semantic similarity scores
- **Context Window Management**: Optimizes token utilization
- **Chunking Strategy**: Evaluates chunk size and overlap
- **Embedding Freshness**: Detects stale embeddings

### 4. Multi-Agent Coordination

- **Agent Communication**: Monitors message passing and latency
- **Deadlock Detection**: Identifies circular dependencies
- **Resource Contention**: Analyzes concurrent resource access
- **Orchestration Logic**: Reviews agent dependency graphs

## When to Use

### Production Incidents
```
Scenario: AI chatbot returning errors in production
Skill Provides: Systematic incident analysis framework
Output: Root cause with remediation steps
```

### Performance Degradation
```
Scenario: RAG system response time increased 3x
Skill Provides: Performance bottleneck analysis
Output: Specific optimization recommendations
```

### Cost Overruns
```
Scenario: Unexpected spike in LLM API costs
Skill Provides: Token usage analysis and optimization
Output: Cost reduction strategies with projected savings
```

## Installation

See main [Installation Guide](../README.md#installation-guide) for setup instructions.

## Usage Examples

### Example 1: LLM API Rate Limiting

**Input:**
```
"Getting 429 errors from OpenAI API during peak hours"
```

**Analysis Output:**
```
Issue Severity: High

Root Cause Analysis:
- Pattern: Rate limit exceeded (429 errors) during 9 AM - 11 AM EST
- Frequency: 150 errors/hour
- Impact: 15% of user requests failing

Evidence:
- API logs show request bursts of 500+ RPM
- Current tier limit: 350 RPM
- No exponential backoff implemented

Remediation (Priority Order):
1. Implement exponential backoff with jitter
   - Expected: 95% error reduction
   - Effort: 2 hours
   - Code example provided

2. Add request queue with rate limiting
   - Expected: 100% error elimination
   - Effort: 4 hours
   - Architecture diagram provided

3. Upgrade to higher tier
   - Expected: Immediate fix
   - Cost: $200/month additional

Prevention:
- Implement predictive rate limit monitoring
- Add request throttling during peak hours
- Set up alerting at 80% quota usage
```

### Example 2: RAG Retrieval Quality Issues

**Input:**
```
"Users complaining about irrelevant answers from our knowledge base"
```

**Analysis Output:**
```
Issue Severity: Medium

Root Cause Analysis:
- Pattern: Low semantic similarity scores (average 0.52, threshold 0.7)
- Affected Queries: 35% of user questions
- Time Period: Started 5 days ago

Evidence:
- Similarity score distribution shifted left
- Correlation with recent document additions (500 new docs)
- Embeddings created with different model version

Technical Details:
- Old embeddings: text-embedding-ada-002
- New embeddings: text-embedding-3-small
- Vector dimension mismatch causing poor retrieval

Remediation:
1. Re-embed entire corpus with consistent model
   - Expected: Restore 0.68 average similarity
   - Time: 6 hours (batch processing)
   - Cost: $25 for embedding API

2. Adjust chunk size from 1024 to 512 tokens
   - Expected: 15% improvement in relevance
   - Effort: 3 hours

3. Implement hybrid search (keyword + semantic)
   - Expected: 25% improvement in edge cases
   - Effort: 8 hours development

Prevention:
- Lock embedding model version in config
- Add embedding quality monitoring
- Implement A/B testing for retrieval changes
```

### Example 3: Multi-Agent Timeout Errors

**Input:**
```
"My multi-agent system is failing with coordination timeout errors"
```

**Analysis Output:**
```
Issue Severity: High

Multi-Agent Coordination Analysis:

Failure Pattern:
- Error: TimeoutError in agent orchestration
- Frequency: 40% of requests
- Affected Agents: ResearchAgent waiting for AnalysisAgent

Root Cause: Circular dependency deadlock

Dependency Graph:
ResearchAgent → AnalysisAgent → DataAgent → ResearchAgent
                     ↑___________________________|
                          (Circular reference)

Evidence:
- Agent logs show waiting state for 30+ seconds
- No timeout configuration in agent orchestration
- Memory pressure causing context switching delays

Technical Analysis:
- ResearchAgent timeout: 30s
- AnalysisAgent processing: 45s average
- Network latency: 200ms p99
- Total chain latency: 2m 15s

Remediation:
1. Break circular dependency (Critical)
   - Refactor: DataAgent should not call ResearchAgent
   - Create shared state store instead
   - Expected: 100% error elimination

2. Implement proper timeout hierarchy (High)
   - Parent timeout: 3 minutes
   - Child timeout: 45 seconds
   - Add graceful degradation

3. Add circuit breaker pattern (Medium)
   - Fail fast after 3 consecutive timeouts
   - Prevent cascade failures
   - Auto-recovery after cooldown period

Prevention:
- Visualize agent dependency graphs before deployment
- Add integration tests for timeout scenarios
- Monitor agent chain latency in production
- Set up alerting for timeout rate >5%
```

## Configuration

### Customizing Analysis Thresholds

Edit `SKILL.md` to adjust thresholds for your environment:
```markdown
## Custom Thresholds
- Critical Response Time: >5 seconds
- High Memory Usage: >85%
- Rate Limit Warning: >80% quota
- Token Cost Alert: >$100/day
```

### Adding Organization-Specific Patterns

Add your production patterns to recognize:
```markdown
## Known Issues Database
1. MongoDB connection pool exhaustion
   - Pattern: "MongoServerError: connection pool timeout"
   - Fix: Increase pool size to 50

2. Redis cache invalidation storms
   - Pattern: Sudden 10x increase in cache misses
   - Fix: Implement cache warming strategy
```

## Integration with Monitoring Tools

The skill works alongside:
- DataDog / New Relic logs
- Prometheus metrics
- Grafana dashboards
- PagerDuty alerts

Simply paste relevant logs or metrics, and the skill will analyze them.

## Best Practices

1. **Provide Context**: Include timestamps, environment, and recent changes
2. **Share Logs**: Full error logs help identify patterns
3. **Mention Scale**: User count and request volume matter
4. **Include Metrics**: API latencies, error rates, resource usage
5. **Describe Impact**: How many users are affected?

## Limitations

- Cannot access your live systems directly (you must provide logs)
- Recommendations based on best practices, not your specific infrastructure
- Requires human validation before implementing changes

## Support

For issues or questions:
- Open an issue on GitHub
- Tag with `skill:ai-health-analyzer`
- Provide example query and unexpected behavior