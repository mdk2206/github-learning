# Windows & Linux SOC Home Lab

## Overview

A personal SOC home lab built to practice security monitoring,
detection engineering, incident investigation, and threat hunting.

The lab simulates a small enterprise environment using Windows,
Linux, a web server, an attacker machine, and a centralized
Wazuh SIEM.

## Lab Architecture

### Kali Linux

Role: Attacker / Security Testing Machine

Used to simulate security activity against the monitored
Windows and Linux environments.

### Windows 10

Role: Windows Endpoint

Components:

- Sysmon
- Wazuh Agent
- Windows Security Event Logs

Used to monitor authentication events, process creation,
PowerShell activity, and other Windows security events.

### Ubuntu Linux

Role: Linux Endpoint and Web Server

Components:

- Nginx
- Wazuh Agent
- Linux system logs
- Web server access logs

Used to monitor Linux activity and web server traffic.

### Ubuntu Server

Role: Wazuh SIEM Server

Components:

- Wazuh Manager
- Wazuh Indexer
- Wazuh Dashboard

Used to collect, analyze, store, and visualize security
events from the monitored endpoints.

## Detection Scenarios

- Windows Brute Force
- PowerShell Activity
- Suspicious Process Creation
- Linux SSH Brute Force
- Web Server Errors
- Suspicious Web Requests
- Web Directory Discovery

## Investigation

Security alerts will be investigated using:

- Windows Event Logs
- Sysmon
- Linux Logs
- Web Server Logs
- Source IP
- Username
- Process Information
- Command Line
- Network Activity

## MITRE ATT&CK

Relevant detections will be mapped to MITRE ATT&CK techniques.

## Project Structure

- `architecture/` — SOC lab architecture documentation
- `detections/` — Detection rules and detection analysis
- `investigations/` — Incident investigation reports
- `screenshots/` — Evidence and screenshots
- `README.md` — Project overview

## Goals

- Build practical SOC Analyst skills
- Learn SIEM monitoring
- Practice detection engineering
- Perform security investigations
- Develop threat hunting skills
- Build a practical cybersecurity portfolio
