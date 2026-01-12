# Contributing to Claude Code Agent Skills

Thank you for your interest in contributing! This guide will help you create high-quality agent skills that benefit the entire community.

## Ways to Contribute

1. **Create new skills** - Add domain expertise
2. **Improve existing skills** - Enhance accuracy and coverage
3. **Fix bugs** - Report and fix issues
4. **Improve documentation** - Make it clearer
5. **Share examples** - Real-world usage scenarios

## Creating a New Skill

### Step 1: Choose Your Domain

Good skill domains:
- ✅ Specialized technical knowledge
- ✅ Recurring analysis patterns
- ✅ Complex decision frameworks
- ✅ Tool integrations

Avoid:
- ❌ General knowledge (already in Claude)
- ❌ Single-use queries
- ❌ Highly organization-specific

### Step 2: Design Your Skill

Use our template:
```markdown
# Skill Name

## Description
[Clear, concise purpose]

## Capabilities
[Bulleted list of what it can do]

## Activation
[When and how it triggers]

## Analysis Framework
[Structured approach to problems]

## Output Format
[How results are presented]

## Examples
[3-5 real-world scenarios]
```

### Step 3: Test Thoroughly

Before submitting:
- [ ] Test with 10+ diverse queries
- [ ] Verify activation triggers work
- [ ] Ensure output is consistent
- [ ] Check cross-platform compatibility (if relevant)
- [ ] Validate tool integrations

### Step 4: Document

Include:
- Clear README.md
- Usage examples
- Configuration options
- Limitations

### Step 5: Submit PR

1. Fork the repository
2. Create feature branch: `git checkout -b skill/your-skill-name`
3. Add your skill to `skills/` directory
4. Update main README.md with your skill
5. Create pull request with detailed description

## Skill Quality Standards

### Must Have
- ✅ Clear activation triggers
- ✅ Structured analysis framework
- ✅ At least 3 usage examples
- ✅ Output format specification
- ✅ Limitations documented

### Nice to Have
- 🌟 Templates for common scenarios
- 🌟 Tool integrations
- 🌟 Platform-specific guides
- 🌟 Configuration options

## Code of Conduct

- Be respectful and inclusive
- Provide constructive feedback
- Focus on improving the project
- Help others learn and grow

## Review Process

1. **Automated checks**: Syntax validation, file structure
2. **Maintainer review**: Functionality and quality
3. **Community feedback**: Usage and improvements
4. **Merge**: Once approved

## Skill Ideas Needed

We're looking for skills in:
- Database performance optimization
- API design and testing
- Cloud cost optimization
- Security auditing
- Documentation generation
- Code review automation

## Getting Help

- **Questions**: Open a GitHub Discussion
- **Bugs**: Create an Issue with details
- **Ideas**: Start a Discussion in Ideas category

## Recognition

Contributors are:
- Listed in CONTRIBUTORS.md
- Mentioned in release notes
- Credited in skill documentation

Thank you for making Claude Code more powerful! 🙌
```

---

**File: LICENSE**
```
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
```

---

**File: .gitignore**
```
# OS generated files
.DS_Store
Thumbs.db

# Editor files
.vscode/
.idea/
*.swp
*.swo
*~

# Logs
*.log
logs/

# Test files
test-outputs/
temp/