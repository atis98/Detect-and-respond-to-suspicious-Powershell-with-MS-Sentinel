# This document shows the steps and details of executing a potentially malicious Powershell command on a Windows 10 device onboarded to MS Defender for Endpoint.
## Device used: my own laptop running Windows 10 Pro.
## Response conducted by: MS Defender for Endpoint and MS Sentinel (my own subscription)
## Attack method: executing a command that launches Powershell with execution policy bypass and performs a web request. In real attacks, this is commonly used to download and execute payloads or communicate with a command-and-control server, often as part of fileless malware activity.
