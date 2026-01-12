# SystemMind Operations Skill

## Overview

SystemMind Operations is a cross-platform system management skill that provides intelligent diagnostics, optimization, and monitoring capabilities for Windows, macOS, and Linux systems. It bridges the gap between users and complex system tools through natural language interactions.

## Key Capabilities

### 1. Performance Diagnostics

- **CPU Analysis**: Core usage, load distribution, thermal throttling
- **Memory Profiling**: RAM usage, swap/page file, memory leaks
- **Disk I/O**: Read/write speeds, queue depth, latency
- **Network**: Bandwidth usage, connection stability, latency

### 2. Resource Optimization

- **Startup Programs**: Impact analysis and recommendations
- **Process Management**: Identify and manage resource-heavy apps
- **Disk Cleanup**: Find large files and suggest cleanup
- **Power Management**: Battery optimization for laptops

### 3. System Health Monitoring

- **Health Scoring**: 0-100 scale with component breakdown
- **Proactive Alerts**: Warn about resources approaching limits
- **Trend Analysis**: Compare current vs historical performance
- **Security Audits**: Firewall, antivirus, update status

### 4. Cross-Platform Support

- **Windows**: Task Manager, Resource Monitor equivalents
- **macOS**: Activity Monitor, Energy analysis
- **Linux**: top/htop, systemd, lm-sensors integration

## When to Use

### Performance Troubleshooting
```
User Issue: "My computer is slow"
Skill Diagnoses: High memory usage from Chrome (3.5 GB)
Recommendation: Close unused tabs, restart browser
Expected Result: 40% performance improvement
```

### Startup Optimization
```
User Issue: "Laptop takes forever to start"
Skill Analyzes: 45 startup programs consuming 2.8 GB
Recommendation: Disable Dropbox, Spotify, Steam at startup
Expected Result: 30-40 seconds faster boot
```

### Battery Life Extension
```
User Issue: "Battery drains too fast"
Skill Identifies: High performance mode + 100% brightness
Recommendation: Balanced mode + 60% brightness
Expected Result: 1.5 hours additional battery life
```

### Disk Space Management
```
User Issue: "Running out of storage"
Skill Locates: 85 GB VM, 45 GB old backups, 23 GB videos
Recommendation: Delete VM snapshots and old backups
Expected Result: 75 GB recovered
```

## Installation

See main [Installation Guide](../README.md#installation-guide) for setup instructions.

## Usage Examples

### Example 1: Complete System Health Check

**Input:**
```
"Give me a complete health report of my computer"
```

**Output:**
```
System Health Report
===================

Overall Status: 🟢 EXCELLENT (92/100)

Hardware Specifications:
- CPU: Intel Core i7-12700K (12 cores, 20 threads)
- RAM: 32 GB DDR4-3200
- Storage: 1 TB NVMe SSD + 2 TB HDD
- GPU: NVIDIA RTX 3070
- OS: Windows 11 Pro (Build 22621)

Current Performance:
┌──────────────┬─────────┬────────┬──────────┐
│ Component    │ Usage   │ Status │ Score    │
├──────────────┼─────────┼────────┼──────────┤
│ CPU          │ 18%     │ ✅     │ 95/100   │
│ Memory       │ 42%     │ ✅     │ 90/100   │
│ Disk C:      │ 45%     │ ✅     │ 92/100   │
│ Network      │ Normal  │ ✅     │ 88/100   │
│ Battery      │ 85% ⚡  │ ✅     │ 94/100   │
└──────────────┴─────────┴────────┴──────────┘

Performance Analysis:
✅ No bottlenecks detected
✅ All resources within optimal range
✅ System uptime: 2 days (healthy)
✅ No background processes consuming excessive resources

Security Status:
✅ Windows Defender: Active and up-to-date
✅ Firewall: Enabled
✅ System Updates: Current (last check: today)
⚠️  Recommended: Enable automatic Windows updates

Top 5 Processes by Memory:
1. Chrome (1.2 GB) - 8 tabs open
2. Visual Studio Code (890 MB) - 3 workspaces
3. Docker Desktop (650 MB)
4. Spotify (420 MB)
5. Windows Explorer (380 MB)

Recommendations:
1. System is running optimally - no action needed
2. Consider enabling automatic updates for security
3. Monitor Chrome if you typically open 15+ tabs

Your computer is in excellent health! 🎉
```

### Example 2: Diagnosing Slow Performance

**Input:**
```
"My computer has been really slow for the past hour"
```

**Output:**
```
Performance Diagnosis
====================

Issue Severity: 🔴 HIGH

Current System State:
- CPU: 95% usage (abnormal) 🔴
- Memory: 88% (high pressure) 🟡
- Disk: 45 MB/s writes (elevated) 🟡
- Response Time: 3-5 second delays

Root Cause Identified:
Windows Update is downloading and installing updates in background

Evidence:
- Process: "Windows Update" using 4.2 GB RAM
- CPU: Update process using 85% across all cores
- Disk: Writing update files at 42 MB/s
- Started: 1 hour 15 minutes ago (matches your timeline)

Top Resource Consumers:
1. Windows Update Service: 85% CPU, 4.2 GB RAM 🔴
2. Chrome: 8% CPU, 1.8 GB RAM 🟡
3. Antivirus Scan: 5% CPU, 650 MB RAM 🟡

Impact on Your Experience:
- Application launch time: 5x slower
- Browser responsiveness: Sluggish scrolling
- File operations: Delayed saves

Recommendations:

Immediate (Next 5 minutes):
1. ✅ Let Windows Update finish (~15 minutes remaining)
   - Why: Interrupting may corrupt updates
   - Impact: System will speed up automatically when done

2. Close unused Chrome tabs (currently 18 open)
   - Why: Free up 800 MB RAM during update
   - How: Keep only tabs you're actively using

Short-term (After update completes):
3. Restart computer to complete update installation
   - Why: Finalize updates and clear memory
   - Impact: Return to normal 18% CPU usage

Long-term Prevention:
4. Schedule Windows Update for off-hours
   - Go to: Settings > Windows Update > Advanced > Active Hours
   - Set: 9 AM - 6 PM as active hours
   - Result: Updates won't run during work time

5. Upgrade to 32 GB RAM if you routinely run heavy workloads
   - Current: 16 GB is limiting with your usage pattern
   - Cost: ~$80 for 16 GB additional RAM
   - Impact: 2x multitasking capacity

Expected Timeline:
- 15 minutes: Update completes, CPU drops to 20%
- 20 minutes: After restart, full performance restored
- Expected normal state: 18% CPU, 42% RAM, fast response

Would you like me to monitor the update progress?
```

### Example 3: Battery Optimization

**Input:**
```
"My laptop battery is dying way too fast, only getting 3 hours"
```

**Output:**
```
Battery Optimization Analysis
============================

Current Battery Status:
- Battery Health: 85% (design capacity: 60 Wh, current: 51 Wh)
- Current Charge: 78%
- Estimated Time: 3 hours 12 minutes
- Power Draw: 15.8 W (high) 🔴

Expected vs Actual:
- Manufacturer Rating: 8 hours
- Your Current: 3.2 hours
- Gap: 4.8 hours missing (60% reduction) 🔴

Root Causes Identified:

1. Power Mode: High Performance ⚠️
   - Current Power Draw: 6.5 W
   - Impact: Reducing battery life by 45%
   - Fix Impact: +1.8 hours

2. Screen Brightness: 100% ⚠️
   - Current Power Draw: 4.2 W
   - Impact: Reducing battery life by 25%
   - Fix Impact: +1.2 hours

3. Background Processes: Excessive ⚠️
   - Chrome: 15% CPU (12 tabs, 2 with video)
   - OneDrive: Actively syncing 2.4 GB
   - Spotify: Streaming music
   - Combined Impact: 15% battery drain
   - Fix Impact: +0.8 hours

4. WiFi: Constantly active
   - Power Draw: 1.8 W
   - Impact: 10% battery drain

Step-by-Step Optimization Plan:

🎯 Quick Wins (Implement Now - 5 minutes):

1. Switch to "Balanced" Power Mode
   - How: Click battery icon > Power mode > Balanced
   - Why: Reduces CPU frequency when not needed
   - Gain: +1.8 hours battery life
   - Trade-off: Slight performance reduction (won't notice in normal use)

2. Reduce Screen Brightness to 60%
   - How: Press Fn + brightness down key 4 times
   - Why: Screen is single biggest battery consumer
   - Gain: +1.2 hours
   - Trade-off: Still perfectly readable indoors

3. Close Unused Chrome Tabs
   - How: Close 8 background tabs, keep only 4 active
   - Why: Each tab with video/animation drains battery
   - Gain: +0.5 hours
   - Which Tabs: YouTube, Netflix (running in background)

4. Pause OneDrive Sync While on Battery
   - How: Right-click OneDrive > Pause syncing > 2 hours
   - Why: Disk and network activity drain battery
   - Gain: +0.3 hours

⚙️ Settings to Configure (10 minutes):

5. Enable Battery Saver at 50%
   - How: Settings > System > Battery > Turn on automatically at 50%
   - Why: Automatically applies power-saving measures
   - Gain: Prevents unexpected shutdowns

6. Adjust "When Plugged In" vs "On Battery" Settings
   - Settings > System > Power & Battery > Screen and sleep
   - On Battery: Screen off after 5 min (currently 15 min)
   - Gain: +0.4 hours if you step away often

7. Disable Background Apps
   - Settings > Apps > Startup
   - Disable: Spotify, Discord, Steam (launch manually when needed)
   - Gain: +0.3 hours

🔬 Advanced Optimizations (Optional):

8. Review Battery Report
   - Open Command Prompt as Admin
   - Run: powercfg /batteryreport
   - Check: Battery degradation over time
   - Consider: Battery replacement if health <80%

9. Disable WiFi When Not Needed
   - Use Airplane mode for focused work
   - Gain: +0.5 hours

Expected Results After All Optimizations:
┌─────────────────────┬──────────┬───────────┐
│ Change              │ Time     │ Cumulative│
├─────────────────────┼──────────┼───────────┤
│ Current             │ 3.2 hrs  │ 3.2 hrs   │
│ + Balanced mode     │ +1.8 hrs │ 5.0 hrs   │
│ + 60% brightness    │ +1.2 hrs │ 6.2 hrs   │
│ + Close tabs        │ +0.5 hrs │ 6.7 hrs   │
│ + Pause OneDrive    │ +0.3 hrs │ 7.0 hrs   │
│ + Other settings    │ +0.7 hrs │ 7.7 hrs   │
└─────────────────────┴──────────┴───────────┘

Final Battery Life: ~7.7 hours (vs manufacturer 8 hrs)
Improvement: +4.5 hours (140% increase)

📊 Your Battery Health Note:
Your battery is at 85% health, which accounts for ~1 hour reduction
from the original 8-hour rating. This is normal wear after 1-2 years.

Implement the quick wins now, and you should immediately see 
3-4 hours of additional battery life! 🔋✨
```

## Platform-Specific Features

### Windows
- Task Manager integration concepts
- Windows Defender status checks
- Startup program analysis via Task Manager
- Power plan optimization
- Windows Update monitoring

### macOS
- Activity Monitor equivalents
- Energy impact analysis
- Login Items management
- Battery condition monitoring
- Thermal management

### Linux
- top/htop process monitoring
- systemd service analysis
- lm-sensors temperature monitoring
- Power management via TLP
- Package manager integration

## Configuration

### Custom Thresholds

Edit skill to adjust for your needs:
```markdown
## Performance Thresholds
- High CPU: >80%
- High Memory: >85%
- High Disk: >90%
- Low Battery: <20%
- High Temp: >85°C
```

## Best Practices

1. **Regular Health Checks**: Weekly system health reports
2. **Monitor Trends**: Compare performance over time
3. **Proactive Maintenance**: Don't wait for issues
4. **Document Baselines**: Know your normal resource usage
5. **Test Recommendations**: Validate improvements after changes

## Limitations

- Provides analysis and recommendations, not direct system control
- You must implement suggested changes manually
- Cannot access actual system metrics (you provide them)
- Recommendations are general best practices

## Support

For issues or questions:
- Open an issue on GitHub
- Tag with `skill:systemmind-ops`
- Include: OS version, issue description, expected behavior