# Case 005: Windows Memory Utilization Analysis

**Category:** System Performance  
**Operating System:** Windows 11 Home  
**Tools Used:** Windows Task Manager — Performance > Memory  
**Status:** Completed — No memory shortage identified

## Objective

Analyze installed RAM, memory utilization, and available system memory to determine whether the computer is experiencing memory pressure.

## Troubleshooting Steps

1. Opened Task Manager using `Ctrl + Shift + Esc`.
2. Selected the **Performance** tab.
3. Navigated to the **Memory** section.
4. Examined installed RAM, memory utilization, available memory, and hardware specifications.
5. Recorded the results for documentation.

## Findings

| Memory Metric | Observed Value |
|---|---|
| Installed RAM | 32 GB DDR5 |
| Memory In Use | 15.5 GB |
| Available Memory | 15.6 GB |
| Memory Speed | 5200 MT/s |
| Memory Slots Used | 2 of 4 |
| Committed Memory | 25.0 / 41.1 GB |
| Cached Memory | 15.4 GB |

## Analysis

The system was using approximately half of its installed physical memory during the observation.

With 15.6 GB of available memory, there was no obvious indication of insufficient RAM or significant memory pressure at the time of testing.

The committed memory value of 25.0 / 41.1 GB represents the amount of virtual memory committed compared with the system's commit limit. It does not represent physical RAM usage alone.

The system's memory configuration included 32 GB of DDR5 RAM operating at 5200 MT/s, with two of four memory slots occupied.

Based on the available measurements, no immediate memory-related performance bottleneck was identified. However, a single observation cannot rule out intermittent memory pressure.

## Resolution

No memory-related corrective action was required based on the observed results.

## Verification

Reviewed Task Manager's **Performance → Memory** section and documented the system's memory utilization, availability, and hardware configuration.

## Skills Demonstrated

- Windows Task Manager
- RAM diagnostics
- Memory utilization analysis
- System performance monitoring
- Hardware configuration review
- Technical documentation

## Evidence

[View Memory Analysis Screenshot](../03-System-Diagnostics/memory-analysis.png)
