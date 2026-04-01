# This document shows the steps and details of executing a potentially malicious Powershell command on a Windows 10 device onboarded to MS Defender for Endpoint.
## Device used: my own laptop running Windows 10 Pro.
## Response conducted by: MS Defender for Endpoint and MS Sentinel (my own subscription)
## Attack method: executing a command that launches Powershell with execution policy bypass and performs a web request. In real attacks, this is commonly used to download and execute payloads or communicate with a command-and-control server, often as part of fileless malware activity.
## MITRE ATT&CK tactic: TA0002: Execution - technique: T1059.001: Command and scripting interpreter - Powershell.
## Steps:
- Preparation1: I onboarded my laptop to MS Defender for Endpoint using the local script method. After some minutes, it appeared in the Defender portal: <img width="1444" height="774" alt="1_mylaptop_in_defender" src="https://github.com/user-attachments/assets/13aa2d5b-5b73-491c-b425-7edb66bf8e40" />
- Preparation2: I created an analytics rule via MS Sentinel to create an alert and an incident whenever the command executed on the device contains "Invoke-WebRequest). An important prerequisite here is that Defender for Endpoint had to be added to Sentinel as a data connector, otherwise the KQL query would not yield any results. <img width="664" height="676" alt="2_analytic-rule" src="https://github.com/user-attachments/assets/f4af00b1-f027-45c9-84d3-9c8a1573a5c1" />
