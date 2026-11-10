# Case 003: Windows Event Viewer Troubleshooting

**Category:** Windows System Diagnostics  
**Operating System:** Windows 11 Home  
**Tools Used:** Windows Run, Start Menu, Event Viewer  
**Status:** Completed — Event Viewer accessible; warning reviewed

## Problem Description

While attempting to open Windows Event Viewer using the Run dialog, Windows displayed an error indicating that it could not find `eventvwr.msc`.

## Troubleshooting Steps

1. Pressed Windows + R and attempted to launch `eventvwr.msc`.
2. Received a Windows error stating the file could not be found.
3. Searched for Event Viewer using the Windows Start menu.
4. Successfully opened Event Viewer from the Start menu.
5. Navigated to Windows Logs > System.
6. Identified and examined a DistributedCOM warning.

## Findings

- **Event Source:** DistributedCOM
- **Event ID:** 10016
- **Event Level:** Warning
- **Description:** Application-specific permission settings did not grant Local Activation permission to a COM Server application.

DistributedCOM Event ID 10016 warnings can occur during normal Windows operation. No related application failure was confirmed during this investigation.

## Resolution

Event Viewer was successfully accessed through the Start menu.

The DistributedCOM warning was documented without changing system permissions. The original Run dialog launch issue was not fully diagnosed.

## Verification

Confirmed that Event Viewer opened and displayed Windows System logs.

## Skills Demonstrated

- Windows Event Viewer
- Windows troubleshooting
- System log analysis
- Event ID interpretation
- Technical documentation

## Evidence

- [Event Viewer Launch Error](../03-System-Diagnostics/event-viewer-error.png)
- [DistributedCOM Warning](../03-System-Diagnostics/event-viewer-warning.png)
