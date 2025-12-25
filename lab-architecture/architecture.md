## Lab Architecture Overview

This lab simulates a small-scale SOC threat analysis environment focused on Windows endpoint monitoring and analyst-driven investigation.
It is designed to practice alert triage, behavior analysis, and detection reasoning rather than enterprise-scale alert automation.

The environment consists of:

One Windows 11 endpoint acting as a monitored host

One Linux-based SIEM platform for log collection and analysis

This setup reflects a realistic junior SOC analyst context, where limited visibility requires careful interpretation of available telemetry.
----

## Data Sources and Telemetry

The following telemetry sources are available for investigation:

Windows Security Event Logs

Successful and failed logon events

Authentication-related activity

Service configuration changes

PowerShell Operational Logs

PowerShell Script Block Logging (Event ID 4104)

Command execution content and context

Sysmon Telemetry

Process creation events

Command-line arguments

Parent-child process relationships

Wazuh Agent Events

Normalized alerts generated from Windows logs

MITRE ATT&CK–mapped detections
----
## Assumptions and Limitations

The following assumptions and limitations apply to this lab environment:

The environment contains a single Windows endpoint with no lateral movement visibility.

Network traffic inspection and full EDR telemetry are not available.

Alerting rules may be generic, noisy, or incomplete by design.

Detection logic focuses on visibility and analyst interpretation rather than automated response.

The lab prioritizes analyst decision-making, false-positive identification, and reasoning over alert volume.
Security Configuration Assessment (CIS Windows 11 benchmark)

These data sources allow investigation of execution, discovery, and basic persistence behaviors on the endpoint.-
