\# Wazuh Server Setup



\## Overview



Wazuh is used as the central SIEM platform for this SOC lab.



The Wazuh Server collects security telemetry from Windows and Linux

endpoints, analyzes events, generates alerts, and provides a centralized

dashboard for security monitoring.



\## Server Information



OS: Ubuntu Server 24.04 LTS

Wazuh Version: 4.9.2

SOC IP: 192.168.50.10

Hostname: wazuhserver



\## Wazuh Components



The Wazuh Server contains:



\- Wazuh Manager

\- Wazuh Indexer

\- Wazuh Dashboard

\- Filebeat



\## Network



SOC monitoring network:

192.168.50.0/24

