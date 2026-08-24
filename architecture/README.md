\# SOC Lab Architecture



\## Overview



This lab simulates a small Security Operations Center (SOC)

environment for security monitoring, detection engineering,

incident investigation, and threat hunting.



\## Lab Components



\### Kali Linux



Role: Attacker / Security Testing Machine



Used to simulate security events against the lab endpoints

and web server.



\### Windows 10



Role: Windows Endpoint



Components:



\- Sysmon

\- Wazuh Agent

\- Windows Security Event Logs



Used to investigate Windows process activity,

authentication events, PowerShell activity, and persistence.



\### Ubuntu



Role: Linux Endpoint and Web Server



Components:



\- Linux system logs

\- SSH

\- Web Server

\- Wazuh Agent



Used to investigate Linux authentication events,

system activity, and web server access logs.



\### Wazuh Server



Role: SIEM / Security Monitoring Platform



Components:



\- Wazuh Manager

\- Wazuh Indexer

\- Wazuh Dashboard



Responsible for collecting, analyzing, and visualizing

security telemetry from the monitored endpoints.



\## Data Flow



Kali Linux

&#x20;   ↓

Windows 10 / Ubuntu Web Server

&#x20;   ↓

Wazuh Agents

&#x20;   ↓

Wazuh Manager

&#x20;   ↓

Wazuh Indexer

&#x20;   ↓

Wazuh Dashboard

&#x20;   ↓

SOC Analyst



\## Detection Scenarios



\- Windows Brute Force

\- PowerShell Activity

\- Suspicious Process Creation

\- Linux SSH Brute Force

\- Web Server Errors

\- Suspicious Web Requests

\- Web Directory Discovery

