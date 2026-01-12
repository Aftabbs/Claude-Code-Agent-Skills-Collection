# Quick Start Guide

Get up and running with Claude Code Agent Skills in under 5 minutes.

## What You'll Get

After this guide, you'll have:
- ✅ 2 powerful agent skills installed
- ✅ Claude Code enhanced with domain expertise
- ✅ Ready-to-use system diagnostics and AI monitoring

## 5-Minute Setup

### Windows Users
```cmd
# 1. Open Command Prompt
# 2. Copy and paste these commands:

cd %USERPROFILE%\.claude\skills
git clone https://github.com/aftabbs/claude-code-skills.git
cd claude-code-skills
xcopy skills\* ..\ /E /I /Y
cd ..
dir
```

### macOS/Linux Users
```bash
# 1. Open Terminal
# 2. Run these commands:

cd ~/.claude/skills
git clone https://github.com/aftabbs/claude-code-skills.git
cd claude-code-skills
cp -r skills/* ../
cd ..
ls -la
```

## First Test

**Restart Claude Code**, then try:
```
"Check my system health"
```

You should see a detailed system analysis! 🎉

## What Each Skill Does

### AI Health Analyzer
**Use when:**
- Debugging production AI systems
- Analyzing error logs
- Optimizing RAG pipelines
- Troubleshooting multi-agent systems

**Try:**
```
"Analyze this error: OpenAI API returned 429 rate limit"
```

### SystemMind Operations
**Use when:**
- Computer running slow
- Battery draining fast
- Need disk space
- System health check

**Try:**
```
"Why is my laptop so slow?"
"My battery life is terrible"
"Find large files on my disk"
```

## Real Examples

### Example 1: Quick Health Check
```
You: "Give me a system health report"

Claude: [SystemMind Operations activates]
        "System Health Report:
         Overall: 🟢 EXCELLENT (92/100)
         - CPU: 18% usage ✅
         - RAM: 42% usage ✅
         - Disk: 55% free ✅
         Your computer is running optimally!"
```

### Example 2: Diagnose Production Issue
```
You: "My RAG system is returning bad results"

Claude: [AI Health Analyzer activates]
        "Let me analyze your RAG pipeline:
         
         Root Cause Analysis:
         1. Check semantic similarity scores
         2. Verify embedding model consistency
         3. Analyze chunk size and overlap
         4. Review context window utilization
         
         Provide your retrieval logs and I'll identify the issue."
```

## Next Steps

1. **Explore Skills**: Try different queries to see how skills activate
2. **Read Docs**: Check out detailed documentation for each skill
3. **Customize**: Edit SKILL.md files to add your own patterns
4. **Share**: Star the repo and share with your team!

## Common Questions

**Q: Do skills work across all conversations?**
A: Yes! Once installed, skills are available in every Claude Code session.

**Q: Can I create my own skills?**
A: Absolutely! See [Creating Custom Skills](./creating-skills.md)

**Q: Do skills access my system directly?**
A: No, skills provide analysis frameworks. You provide data, skills analyze it.

**Q: How do I update skills?**
A: Run `git pull` in the skills repo directory and copy files again.

## Get Help

- [Full Documentation](../README.md)
- [Troubleshooting](./troubleshooting.md)
- [GitHub Issues](https://github.com/aftabbs/claude-code-skills/issues)

---

**Ready to level up your Claude Code experience? Let's go! 🚀**