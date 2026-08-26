# Kali Setup

## Overview

Kali Linux is the testing machine in my SOC lab.

I use it to generate normal and controlled security testing traffic against the other machines in the lab.

## System Information

* OS: Kali Linux
* Role: Security Testing
* IP: 192.168.50.40
* Network: 192.168.50.0/24

## SOC Lab

My SOC lab uses: 192.168.50.0/24

Wazuh Server: 192.168.50.10
Windows 10: 192.168.50.20
Ubuntu Web: 192.168.50.30
Kali: 192.168.50.40

## Network

Kali uses the SOC network to communicate with the other lab machines.

I also use the NAT network when Kali needs Internet access.

## Connectivity Test

I can test the connection to the Wazuh Server with:

ping -c 4 192.168.50.10

I can test the Windows machine with:

ping -c 4 192.168.50.20

I can test the Ubuntu Web server with:

ping -c 4 192.168.50.30

## Web Server Test

The Ubuntu Web server is running Nginx.

I can send a simple HTTP request from Kali with:

curl http://192.168.50.30

## Purpose

Kali will be used later to generate traffic for detection testing.

For example, I can send HTTP requests to the Ubuntu Web server and then check the Nginx logs and Wazuh alerts.
