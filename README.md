# Nmap-Network-Scan
Basic network scanning using Nmap on a Kali Linux VM in Oracle VirtualBox lab environment.
# Task 1: Basic Network Scanning with Nmap

## Objective

The objective of this task was to perform a basic network scan using Nmap to identify open ports and services running on a target machine in a controlled lab environment.

## Tools Used

* Nmap (Network Mapper)
* Kali Linux (Target Machine)
* Windows Command Prompt (Scanning Machine)
* VirtualBox (Virtual Lab Environment)


## Setup Description

I configured Kali Linux virtual machine using a Host-Only Adapter network. My Windows machine was the host machine used to perform network scans against the VM.

An Apache web server was installed on the Kali machine to create an active service for detection.


## Commands Used

### 1. Check Kali IP Address

hostname -I

### 2. Check Nmap Version

nmap --version

### 3. Basic Scan

nmap 192.168.56.101

### 4. Service Detection Scan

nmap -sV 192.168.56.101

### 5. Install Apache Web Server on Kali

sudo apt update
sudo apt install apache2 -y

### 6. Start Apache Server

sudo systemctl start apache2

## Scan Results

### Open Ports Detected

* Port 80/tcp → HTTP (Apache Web Server)


## Security Analysis

### Port 80 (HTTP)

This port is used for web traffic. In this lab, it was running Apache HTTP Server.

#### Risks:

* Vulnerable to web-based attacks if not secured
* Possible exploitation through misconfigured web services
* Data transmitted is not encrypted

#### Recommendations:

* Use HTTPS instead of HTTP
* Keep Apache updated
* Restrict unnecessary access using firewall rules



## Conclusion

This task demonstrated how to perform basic network scanning using Nmap and identify active services on a target system. The exercise provided practical insight into network reconnaissance techniques used in cybersecurity operations.


