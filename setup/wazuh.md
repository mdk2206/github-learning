# Wazuh Setup

## Overview

Wazuh is the main SIEM in my SOC lab.

I use it to collect logs from the Windows 10 and Ubuntu Web machines and view alerts from the Wazuh Dashboard.

## System Information

* OS: Ubuntu Server 24.04 LTS
* Role: SIEM Server
* IP: 192.168.50.10
* Network: 192.168.50.0/24
* Wazuh Version: 4.9.2

## Components

The Wazuh server has these main components:

* Wazuh Manager
* Wazuh Indexer
* Wazuh Dashboard
* Filebeat

## Agents

### Windows 10

* IP: 192.168.50.20
* Role: Endpoint
* Wazuh Agent: Installed
* Sysmon: Installed

### Ubuntu Web

* IP: 192.168.50.30
* Role: Web Server
* Wazuh Agent: Installed
* Nginx: Installed

## Network

My SOC lab uses:

192.168.50.0/24

Wazuh Server:

192.168.50.10

Windows 10:

192.168.50.20

Ubuntu Web:

192.168.50.30

Kali:

192.168.50.40

## Check Wazuh Services

I can check the Wazuh Manager with:

sudo systemctl status wazuh-manager

The other services can be checked with:

sudo systemctl status wazuh-indexer

sudo systemctl status wazuh-dashboard

## Basic Data Flow

Windows 10 → Wazuh Agent → Wazuh Manager

Ubuntu Web → Wazuh Agent → Wazuh Manager

The collected data can then be viewed in the Wazuh Dashboard.
