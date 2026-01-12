# Claude Code Agent Skills Collection

<img width="1103" height="616" alt="image" src="https://github.com/user-attachments/assets/bce03337-11a4-41bc-80fc-92544c407e0f" />

 
![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20macOS%20%7C%20Linux-lightgrey) 
![Claude Code](https://img.shields.io/badge/Claude%20Code-Compatible-brightgreen) 

A curated collection of production-ready Agent Skills for Claude Code that extend AI capabilities with specialized domain expertise. Built for enterprise AI systems, system operations, and production reliability.

## 📚 Table of Contents

- [What Are Agent Skills?](#what-are-agent-skills)
- [Why This Matters](#why-this-matters)
- [Available Skills](#available-skills)
- [Quick Start](#quick-start)
- [Installation Guide](#installation-guide)
- [Usage Examples](#usage-examples)
- [Contributing](#contributing)
- [Author](#author)
- [License](#license)

## 🎯 What Are Agent Skills?

Agent Skills are modular capability extensions for Claude Code that provide:

- **Domain Expertise**: Specialized knowledge in specific technical domains
- **Contextual Activation**: Automatically trigger based on user queries
- **Structured Workflows**: Pre-defined analysis frameworks and methodologies
- **Tool Integration**: Connect with external tools and APIs
- **Reusable Templates**: Standardized approaches to common problems

Think of them as **expert consultants** that Claude Code can call upon when needed. Each skill encapsulates best practices, decision frameworks, and domain knowledge that would typically require years of experience to develop.

### How They Work
```
User Query → Claude Code analyzes intent → Activates relevant skill(s)
                                              ↓
                                    Skill provides:
                                    - Domain expertise
                                    - Analysis frameworks
                                    - Tool definitions
                                    - Output templates
                                              ↓
                          Claude Code generates informed response
```

## 🔥 Why This Matters

### The Problem

Traditional AI assistants face limitations:

1. **Generic Responses**: Lack specialized domain knowledge
2. **Inconsistent Analysis**: No standardized methodologies
3. **Context Loss**: Forget best practices across conversations
4. **Tool Fragmentation**: Difficult to integrate external capabilities
5. **Knowledge Gaps**: Missing production-tested workflows

### The Solution

Agent Skills provide:

✅ **Specialized Expertise**: Deep domain knowledge in production AI, system operations, etc.
✅ **Consistent Quality**: Standardized analysis frameworks and methodologies
✅ **Persistent Knowledge**: Skills remain available across all conversations
✅ **Tool Integration**: Seamless connection to external systems and APIs
✅ **Production-Ready**: Battle-tested workflows from real-world scenarios

### Real-World Impact

**Before Agent Skills:**
```
User: "My AI system is failing in production"
Claude: "That's concerning. Can you provide more details about the error?"
(Generic response, requires multiple back-and-forth)
```

**After Agent Skills:**
```
User: "My AI system is failing in production"
Claude: [AI Health Analyzer skill activates]
        "Let me analyze this systematically:

        Root Cause Analysis:
        1. Check API rate limits and quota usage
        2. Analyze error patterns in logs
        3. Verify model endpoint availability
        4. Review token consumption trends

        Please provide:
        - Recent error logs
        - API response codes
        - Timestamp of first failure

        I'll correlate these to identify the root cause."
(Structured, expert-level response with clear methodology)
```

## 🛠️ Available Skills

### 1. AI Health Analyzer

**Domain**: Production AI Systems Monitoring

**Capabilities**:
- Parse and analyze AI application logs
- Identify LLM API failure patterns
- Analyze RAG retrieval quality
- Detect agent coordination failures
- Monitor token usage and cost optimization
- Root cause analysis for AI system issues

**Best For**:
- AI/ML Engineers managing production systems
- DevOps teams supporting AI applications
- Organizations running conversational AI at scale
- Multi-agent system developers

**Activation Triggers**:
- "analyze logs"
- "debug production"
- "AI system health"
- "check performance"

[📖 Detailed Documentation](./docs/ai-health-analyzer.md)

---

### 2. SystemMind Operations

**Domain**: Cross-Platform System Management

**Capabilities**:
- Real-time system performance monitoring
- Cross-platform diagnostics (Windows/macOS/Linux)
- Resource optimization (CPU, RAM, disk, network)
- Startup program analysis
- Battery life optimization
- Temperature monitoring
- Security audit and health scoring

**Best For**:
- System administrators
- DevOps engineers
- End users troubleshooting performance
- IT support teams

**Activation Triggers**:
- "system health"
- "computer is slow"
- "optimize performance"
- "battery draining"

[📖 Detailed Documentation](./docs/systemmind-ops.md)

---

## ⚡ Quick Start

### Prerequisites

- Claude Code installed and configured
- Terminal/Command Prompt access
- Basic familiarity with file systems

### 30-Second Installation

**Windows (Command Prompt):**
```cmd
cd %USERPROFILE%\.claude\skills
git clone https://github.com/aftabbs/claude-code-skills.git
cd claude-code-skills
copy skills\* ..\ /Y
```

**macOS/Linux:**
```bash
cd ~/.claude/skills
git clone https://github.com/aftabbs/claude-code-skills.git
cd claude-code-skills
cp -r skills/* ../
```

### Verify Installation
```cmd
# Check skills directory
dir %USERPROFILE%\.claude\skills

# Should show:
# - ai-health-analyzer/
# - systemmind-ops/
# - index.json
```

### Test the Skills

Restart Claude Code and try:
```
"Check my system health"
"Analyze this error log: [paste log]"
"My computer is running slow, diagnose it"
```

## 📖 Installation Guide

For detailed installation instructions, see:

- [Windows Installation Guide](./docs/installation-windows.md)
- [macOS Installation Guide](./docs/installation-macos.md)
- [Linux Installation Guide](./docs/installation-linux.md)
- [Troubleshooting Guide](./docs/troubleshooting.md)

## 💡 Usage Examples

### Example 1: Debugging Production AI System
```
User: "My RAG system is returning irrelevant results in production"

Claude (AI Health Analyzer activated):
"Let me analyze your RAG pipeline systematically:

Root Cause Analysis Framework:
1. Retrieval Quality Check
   - Semantic similarity scores
   - Context relevance metrics
   - Query-document matching

2. Embedding Health
   - Vector search latency
   - Embedding freshness
   - Index consistency

3. Context Window Analysis
   - Token utilization
   - Chunk overlap
   - Context pruning strategy

Please provide:
- Sample queries with poor results
- Similarity scores from vector search
- Recent changes to document corpus

I'll identify whether this is a retrieval, embedding, or context issue."
```

### Example 2: System Performance Optimization
```
User: "My laptop is slow and battery drains quickly"

Claude (SystemMind Operations activated):
"I'll perform a comprehensive system analysis:

Performance Diagnosis:
- CPU: 85% usage (abnormal) 🔴
- RAM: 92% (memory pressure) 🔴
- Top Process: Chrome (3.8 GB, 15 tabs)

Battery Analysis:
- Current: 45% (2.1 hours remaining)
- Power Mode: High Performance ⚠️
- Screen: 100% brightness ⚠️

Root Cause: Resource exhaustion from browser tabs + aggressive power settings

Recommendations:
1. Close unused Chrome tabs (+2 GB RAM, +45 min battery)
2. Switch to Balanced power mode (+40 min battery)
3. Reduce brightness to 60% (+30 min battery)

Expected Results:
- 40% performance improvement
- 1.9 hours additional battery life
- System responsiveness restored"
```

### Example 3: Multi-Agent System Debugging
```
User: "My multi-agent coordination is failing with timeout errors"

Claude (AI Health Analyzer activated):
"Multi-Agent Coordination Failure Analysis:

Failure Pattern Analysis:
1. Agent Communication
   - Message queue depth
   - Inter-agent latency
   - Deadlock detection

2. Resource Contention
   - Concurrent API calls
   - Token rate limits
   - Memory allocation

3. Orchestration Logic
   - Agent dependency graph
   - Timeout configuration
   - Retry mechanisms

Common Timeout Causes:
- Agent A waiting for Agent B (circular dependency)
- API rate limit exceeded (429 errors)
- Insufficient timeout buffer (network latency)
- Memory pressure causing slowdown

Debugging Steps:
1. Check agent execution logs for timing
2. Verify API quota and rate limits
3. Review agent dependency chain
4. Monitor resource utilization during execution

Provide your agent orchestration code and error logs for detailed analysis."
```

## 🎓 Learning Resources

- [Creating Custom Skills](./docs/creating-skills.md)
- [Skill Development Best Practices](./docs/best-practices.md)
- [Integration with MCP Servers](./docs/mcp-integration.md)
- [Advanced Skill Patterns](./docs/advanced-patterns.md)

## 🤝 Contributing

We welcome contributions! Here's how you can help:

### Adding New Skills

1. Fork this repository
2. Create a skill following our [Skill Template](./templates/SKILL_TEMPLATE.md)
3. Test thoroughly across platforms
4. Submit a pull request with documentation

### Improving Existing Skills

1. Identify improvement area
2. Make changes following existing patterns
3. Update documentation
4. Submit PR with before/after examples

### Contribution Guidelines

- Follow the established skill structure
- Include comprehensive documentation
- Provide real-world usage examples
- Test on multiple platforms when applicable
- Update the main README with your changes

See [CONTRIBUTING.md](./CONTRIBUTING.md) for detailed guidelines.

## 👤 Author

**Mohammed Ashfaq**
- Applied AI Scientist @ AgentMira USA
- Software Engineer @ Lowe's India
- Microsoft Open Source Contributor

**Expertise**:
- Conversational AI & Multi-Agent Systems
- Production AI System Reliability
- RAG Implementation & Optimization
- Enterprise AI Solutions

**Connect**:
- GitHub: [@YOUR_GITHUB_USERNAME](https://github.com/YOUR_GITHUB_USERNAME)
- LinkedIn: [Your LinkedIn](https://linkedin.com/in/YOUR_PROFILE)
- Email: your.email@example.com

## 🏢 Organizations

Built with expertise from:
- **AgentMira USA**: Advanced AI agent systems
- **Lowe's India**: Enterprise-scale AI solutions
- **Production Experience**: JP Morgan, PwC client projects

## 📄 License

MIT License

Copyright (c) 2025 Mohammed Ashfaq

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

## 🌟 Star History

If you find this project useful, please consider giving it a star! ⭐

## 📊 Project Stats

![GitHub stars](https://img.shields.io/github/stars/aftabbs/claude-code-skills?style=social)
![GitHub forks](https://img.shields.io/github/forks/aftabbs/claude-code-skills?style=social)
![GitHub watchers](https://img.shields.io/github/watchers/aftabbs/claude-code-skills?style=social)

## 🗺️ Roadmap

### Coming Soon

- [ ] Database Performance Analyzer skill
- [ ] Cloud Cost Optimization skill
- [ ] Security Audit & Compliance skill
- [ ] API Integration Testing skill
- [ ] Documentation Generator skill

### Future Enhancements

- Web-based skill configuration UI
- Skill marketplace and sharing platform
- Automated skill testing framework
- Performance benchmarking tools
- Community skill repository

## 💬 Support

- **Issues**: [GitHub Issues](https://github.com/aftabbs/claude-code-skills/issues)
- **Discussions**: [GitHub Discussions](https://github.com/aftabbs/claude-code-skills/discussions)
- **Email**: your.email@example.com

## 🙏 Acknowledgments

- Anthropic team for Claude Code and MCP protocol
- Open source community for inspiration
- AgentMira USA and Lowe's India for real-world use cases
- All contributors and users of this project

---

**Made with ❤️ for the AI development community**
