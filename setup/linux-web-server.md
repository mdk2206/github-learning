# Linux Web Server Setup

## Overview

This machine is used as the web server in my SOC lab.

I use Ubuntu Server with Nginx and the Wazuh Agent.

## System Information

* OS: Ubuntu Server 24.04 LTS
* Role: Web Server
* IP: 192.168.50.30
* Network: 192.168.50.0/24
* Web Server: Nginx
* Wazuh Agent: Installed

## Network

My SOC lab uses: 192.168.50.0/24

Wazuh Server: 192.168.50.10
Windows 10: 192.168.50.20
Ubuntu Web: 192.168.50.30
Kali: 192.168.50.40

## Nginx

I installed Nginx and use it to run a simple web server for the lab.

Check Nginx:

sudo systemctl status nginx

Test the web server:

curl http://localhost

## Nginx Logs

The main logs I use are:

* /var/log/nginx/access.log
* /var/log/nginx/error.log

The access log contains information about HTTP requests.

I can watch new requests with:

sudo tail -f /var/log/nginx/access.log

## Wazuh Agent

The Wazuh Agent is installed on this server.

Check the Agent:

sudo systemctl status wazuh-agent

The Agent sends data to: 192.168.50.10

## Purpose

I will use this server to test web-related activity and check how Nginx logs are collected by Wazuh.

Basic flow:

Kali → Ubuntu Web → Nginx → Wazuh Agent → Wazuh Manager
