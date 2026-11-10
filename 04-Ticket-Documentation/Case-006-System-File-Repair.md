# Case 006: Windows System File Integrity Repair

**Category:** Windows System Administration  
**Operating System:** Windows 11 Home  
**Tools Used:** Command Prompt, System File Checker (SFC)  
**Status:** Resolved — Repair successfully verified

## Problem Description

During a Windows system integrity assessment, System File Checker (SFC) detected integrity violations affecting protected Windows system files.

The objective was to identify the issue, repair the affected files, and verify that the system passed a follow-up integrity check.

## Initial Troubleshooting

1. Opened Windows Command Prompt.
2. Executed `sfc /verifyonly`.
3. Received an error indicating that administrator privileges were required.
4. Reopened Command Prompt using **Run as administrator**.
5. Executed `sfc /verifyonly` again.
6. The scan completed and reported integrity violations.

## Findings and Root Cause Analysis

The initial SFC command failed because Command Prompt was not running with administrator privileges.

After elevating Command Prompt, SFC identified integrity violations involving protected Windows system files.

**Key findings:**
- The initial scan required elevated administrator permissions.
- The elevated integrity scan detected violations.
- The underlying cause of the file corruption was not determined.
- A repair operation was required to restore system file integrity.

## Resolution

Executed the following command in an elevated Command Prompt:

```cmd
sfc /scannow
```

Windows reported:

> Windows Resource Protection found corrupt files and successfully repaired them.

This confirmed that SFC detected and repaired corrupted protected system files.

## Verification

After completing the repair, executed:

```cmd
sfc /verifyonly
```

The verification scan completed successfully and reported:

> Windows Resource Protection did not find any integrity violations.

This confirmed that no protected system file integrity violations were detected during the follow-up scan.

## Outcome

Successfully identified and repaired Windows system file integrity violations using System File Checker.

Verified the repair by performing a second integrity scan, which reported no remaining violations.

## Skills Demonstrated

- Windows troubleshooting
- Administrator permissions and elevated commands
- System File Checker (SFC)
- System integrity diagnostics
- Windows system file repair
- Root cause investigation
- Post-repair verification
- Technical documentation

## Evidence

- [Administrator Permission Error](../03-System-Diagnostics/sfc-permission-error.png)
- [Initial Integrity Violations](../03-System-Diagnostics/sfc-integrity-violations.png)
- [Successful SFC Repair](../03-System-Diagnostics/sfc-repair.png)
- [Final Verification](../03-System-Diagnostics/sfc-verification.png)
