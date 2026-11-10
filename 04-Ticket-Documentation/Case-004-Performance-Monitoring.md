# Case 004: Windows Performance Monitoring

**Category:** System Performance  
**Operating System:** Windows 11 Home  
**Tools Used:** Windows Task Manager  
**Status:** Completed — Performance baseline recorded

## Objective

Analyze CPU, memory, disk, and network utilization to identify potential system performance bottlenecks.

## Troubleshooting Steps

1. Opened Task Manager using `Ctrl + Shift + Esc`.
2. Navigated to the Processes tab.
3. Reviewed overall CPU, memory, disk, and network utilization.
4. Identified applications consuming system resources.
5. Recorded performance statistics for documentation.

## Findings

| Resource | Observed Utilization |
|---|---|
| CPU | 7% |
| Memory | 50% |
| Disk | 0% |
| Network | 0% displayed |
| Google Chrome Memory Usage | Approximately 2,367.7 MB |

## Analysis

CPU utilization was low during the observation. Disk activity was minimal, and memory utilization was moderate.

Google Chrome was the largest memory consumer visible in the screenshot, using approximately 2.37 GB across its displayed processes.

The captured snapshot did not indicate an obvious CPU or disk bottleneck. However, a single snapshot cannot rule out intermittent performance issues.

## Resolution

No performance-related changes were necessary based on the available evidence.

## Verification

Reviewed Task Manager's Processes tab and documented system resource utilization as a performance baseline.

## Skills Demonstrated

- Windows Task Manager
- CPU and memory monitoring
- Performance troubleshooting
- Resource utilization analysis
- Technical documentation

## Evidence

[View Task Manager Screenshot](../03-System-Diagnostics/task-manager.png)
