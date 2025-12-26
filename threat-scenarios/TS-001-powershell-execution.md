## Scenario Overview

This scenario simulates the execution of PowerShell on a Windows 11 endpoint using command-line parameters that reduce visibility and user awareness.

PowerShell is a legitimate administrative tool but is frequently abused by attackers for reconnaissance, execution, and defense evasion.

Attacker Objective

The simulated objective is local system reconnaissance using PowerShell without relying on interactive execution.

---
## Simulated Activity
A PowerShell process is launched with the following characteristics:

Executed via command line

Non-interactive execution

Hidden window

No user profile loaded

Example execution:

powershell.exe -NoProfile -WindowStyle Hidden -Command "Get-LocalUser"

---
## Expected Telemetry

The following telemetry is expected to be generated:

PowerShell Script Block Logging (Event ID 4104)

Process creation events

Command-line arguments captured

Windows Security or Sysmon logs (depending on configuration)

---
## Analyst Notes

This activity alone is not inherently malicious.
Context, frequency, user identity, and follow-on actions are required to assess intent.

However, this technique aligns with common attacker tradecraft and warrants visibility and analysis in a SOC environment.
