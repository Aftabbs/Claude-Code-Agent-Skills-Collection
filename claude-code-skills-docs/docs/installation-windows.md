# Installation Guide - Windows

This guide walks you through installing Claude Code Agent Skills on Windows systems.

## Prerequisites

- Windows 10 or Windows 11
- Claude Code installed and configured
- Command Prompt or PowerShell access
- Git (optional, for cloning repository)

## Installation Methods

### Method 1: Git Clone (Recommended)

**Step 1: Open Command Prompt**
```cmd
# Press Win + R, type "cmd", press Enter
```

**Step 2: Navigate to Skills Directory**
```cmd
cd %USERPROFILE%\.claude\skills
```

**Step 3: Clone Repository**
```cmd
git clone https://github.com/YOUR_USERNAME/claude-code-skills.git
cd claude-code-skills
```

**Step 4: Copy Skills**
```cmd
xcopy skills\* ..\ /E /I /Y
```

**Step 5: Verify Installation**
```cmd
cd ..
dir
# You should see: ai-health-analyzer, systemmind-ops, index.json
```

### Method 2: Manual Download

**Step 1: Download ZIP**
1. Go to repository page
2. Click "Code" > "Download ZIP"
3. Extract to `Downloads` folder

**Step 2: Create Skills Directory**
```cmd
mkdir %USERPROFILE%\.claude\skills
```

**Step 3: Copy Files**
```cmd
cd %USERPROFILE%\Downloads\claude-code-skills-main\skills
xcopy * %USERPROFILE%\.claude\skills\ /E /I /Y
```

**Step 4: Verify**
```cmd
dir %USERPROFILE%\.claude\skills
```

### Method 3: Manual Creation (From Scratch)

Follow the step-by-step commands in the main README to create each skill manually.

## Verification

**Check Directory Structure:**
```cmd
cd %USERPROFILE%\.claude\skills
tree /F
```

**Expected Output:**
```
skills
├── ai-health-analyzer
│   ├── SKILL.md
│   ├── README.md
│   ├── prompts
│   │   ├── log_analysis_template.md
│   │   └── metrics_analysis_template.md
│   └── tools
│       └── tools.json
├── systemmind-ops
│   ├── SKILL.md
│   ├── README.md
│   ├── templates
│   │   ├── performance_diagnosis.md
│   │   ├── system_optimization.md
│   │   └── health_check.md
│   └── platforms
│       ├── windows_guide.md
│       ├── macos_guide.md
│       └── linux_guide.md
└── index.json
```

## Testing Installation

**Step 1: Restart Claude Code**
- Close Claude Code completely
- Reopen from terminal or application

**Step 2: Test Skills**
```
Try these commands in Claude Code:

1. "Check my system health"
   (Should activate SystemMind Operations)

2. "Analyze this production error: [paste error]"
   (Should activate AI Health Analyzer)

3. "My computer is slow"
   (Should activate SystemMind Operations)
```

## Troubleshooting

### Issue: Skills directory doesn't exist
**Solution:**
```cmd
mkdir %USERPROFILE%\.claude
mkdir %USERPROFILE%\.claude\skills
```

### Issue: Skills not activating
**Check 1:** Verify index.json exists
```cmd
type %USERPROFILE%\.claude\skills\index.json
```

**Check 2:** Validate JSON syntax
- Use online JSON validator
- Ensure no trailing commas

**Check 3:** Restart Claude Code
```cmd
taskkill /F /IM claude-code.exe
# Then reopen Claude Code
```

### Issue: Permission denied
**Solution:** Run Command Prompt as Administrator
1. Right-click Command Prompt
2. Select "Run as administrator"
3. Retry installation

## Updating Skills

**With Git:**
```cmd
cd %USERPROFILE%\.claude\skills\claude-code-skills
git pull origin main
xcopy skills\* ..\ /E /I /Y
```

**Without Git:**
1. Download latest ZIP
2. Extract and copy files
3. Overwrite existing skills

## Uninstalling

**Remove specific skill:**
```cmd
rmdir /S /Q %USERPROFILE%\.claude\skills\ai-health-analyzer
```

**Remove all skills:**
```cmd
rmdir /S /Q %USERPROFILE%\.claude\skills
```

## Next Steps

- Read the [Usage Examples](../README.md#usage-examples)
- Explore [Skill Documentation](./ai-health-analyzer.md)
- Check out [Best Practices](./best-practices.md)

## Support

If you encounter issues:
1. Check [Troubleshooting Guide](./troubleshooting.md)
2. Open a GitHub issue
3. Include error messages and Windows version