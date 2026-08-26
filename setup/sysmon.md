# Sysmon Setup

## Overview

I installed Sysmon on the Windows 10 machine to get more detailed Windows event information.

The Windows machine is:

* Hostname: Win10Lab
* IP: 192.168.50.20

The Wazuh Manager is:

192.168.50.10

## Installation

Sysmon is installed on the Windows 10 endpoint.

After installation, Sysmon runs as a Windows service and writes events to the Sysmon Operational log.

## Event Log

I can view Sysmon events from:

Event Viewer → Applications and Services Logs → Microsoft → Windows → Sysmon → Operational

## Events

Sysmon can provide information about things such as:

* Process creation
* Process termination
* Network connections
* File activity
* Registry activity
* Parent-child processes

## Wazuh

The Wazuh Agent is also installed on the same Windows machine.

The basic flow is:

Windows activity → Sysmon → Windows Event Log → Wazuh Agent → Wazuh Manager

Wazuh Manager: 192.168.50.10

Windows: 192.168.50.20

## Purpose

I will use Sysmon events together with Wazuh to investigate suspicious Windows activity.
