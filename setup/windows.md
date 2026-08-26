# Windows Setup

## Overview

Windows 10 is the main Windows endpoint in my SOC lab.

I use it to test Windows logs, Sysmon events and Wazuh alerts.

## System Information

* OS: Windows 10
* Hostname: Win10Lab
* Role: Endpoint
* IP: 192.168.50.20
* Network: 192.168.50.0/24
* Wazuh Agent: Installed
* Sysmon: Installed

## Network

Windows 10: 192.168.50.20

Subnet: 255.255.255.0

Wazuh Server: 192.168.50.10

My SOC lab uses: 192.168.50.0/24

## Wazuh Agent

The Wazuh Agent is installed on this machine.

Check the Agent service with:

Get-Service WazuhSvc

The service should be running before sending logs to the Wazuh Manager.

## Sysmon

I installed Sysmon to collect more detailed information about Windows activity.

Some useful events include:

* Process creation
* Network connections
* File activity
* Registry activity
* Process relationships

## Sysmon Logs

Sysmon events can be viewed in:

Event Viewer → Applications and Services Logs → Microsoft → Windows → Sysmon → Operational

## Wazuh Configuration

The Wazuh Agent sends data to the Wazuh Manager.

Wazuh Manager: 192.168.50.10

Windows endpoint: 192.168.50.20

## Purpose

I will use this machine to test Windows-related detections and investigate events in Wazuh.
