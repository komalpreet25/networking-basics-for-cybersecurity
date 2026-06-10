# Nmap Basics

## Description

This document introduces Nmap (Network Mapper), one of the most widely used network scanning and reconnaissance tools in cybersecurity. Nmap is used to discover hosts, identify open ports, detect running services, and gather information about target systems.

---

# What is Nmap?

Nmap (Network Mapper) is an open-source network scanning tool used for:

* Host Discovery
* Port Scanning
* Service Detection
* Operating System Detection
* Vulnerability Assessment
* Network Auditing

---

# Why Nmap is Important?

Nmap helps security professionals:

* Identify live hosts
* Discover open ports
* Detect running services
* Understand network structure
* Perform reconnaissance during penetration testing

---

# Installing Nmap

## Linux

```bash
sudo apt install nmap
```

## Verify Installation

```bash
nmap --version
```

---

# Basic Nmap Scan

### Scan a Target

```bash
nmap 192.168.1.10
```

This performs a basic scan of the most common ports.

---

# Understanding Port States

Nmap may report ports in different states.

## Open

```text
open
```

A service is actively accepting connections.

---

## Closed

```text
closed
```

The port is reachable but no service is listening.

---

## Filtered

```text
filtered
```

A firewall or filtering device is blocking access.

---

# Host Discovery

Used to identify active systems on a network.

### Ping Scan

```bash
nmap -sn 192.168.1.0/24
```

Purpose:

* Find live hosts
* Skip port scanning

---

# Port Scanning

## Scan Specific Port

```bash
nmap -p 80 192.168.1.10
```

---

## Scan Multiple Ports

```bash
nmap -p 22,80,443 192.168.1.10
```

---

## Scan Port Range

```bash
nmap -p 1-1000 192.168.1.10
```

---

## Scan All Ports

```bash
nmap -p- 192.168.1.10
```

Scans all 65535 TCP ports.

---

# TCP Connect Scan

```bash
nmap -sT 192.168.1.10
```

Characteristics:

* Completes full TCP handshake
* Easy to detect
* Does not require root privileges

---

# SYN Scan (Stealth Scan)

```bash
sudo nmap -sS 192.168.1.10
```

Characteristics:

* Fast
* Commonly used
* More stealthy than TCP Connect Scan

---

# UDP Scan

```bash
sudo nmap -sU 192.168.1.10
```

Used to discover UDP services.

Examples:

```text
DNS
DHCP
SNMP
TFTP
```

---

# Service Version Detection

Determines software versions running on open ports.

```bash
nmap -sV 192.168.1.10
```

Example Output:

```text
22/tcp open ssh OpenSSH 9.2
80/tcp open http Apache 2.4
```

---

# Operating System Detection

Attempts to identify the target operating system.

```bash
sudo nmap -O 192.168.1.10
```

Possible Results:

```text
Linux
Windows
FreeBSD
macOS
```

---

# Aggressive Scan

```bash
sudo nmap -A 192.168.1.10
```

Includes:

* OS Detection
* Version Detection
* Script Scanning
* Traceroute

---

# Timing Options

## Faster Scan

```bash
nmap -T4 192.168.1.10
```

---

## Very Fast Scan

```bash
nmap -T5 192.168.1.10
```

Use carefully to avoid missing results.

---

# Output Options

## Save Output

```bash
nmap -oN scan.txt 192.168.1.10
```

---

## XML Output

```bash
nmap -oX scan.xml 192.168.1.10
```

---

## All Formats

```bash
nmap -oA scan 192.168.1.10
```

Creates:

```text
scan.nmap
scan.xml
scan.gnmap
```

---

# Nmap Scripting Engine (NSE)

NSE allows automated scanning and information gathering.

---

## Run Default Scripts

```bash
nmap -sC 192.168.1.10
```

---

## HTTP Title Detection

```bash
nmap --script=http-title 192.168.1.10
```

---

## SMB Information

```bash
nmap --script=smb-os-discovery 192.168.1.10
```

---

# Useful Scan Combinations

## Host Discovery + Service Detection

```bash
nmap -sn 192.168.1.0/24
```

---

## Version Detection

```bash
nmap -sV 192.168.1.10
```

---

## Stealth Scan

```bash
sudo nmap -sS 192.168.1.10
```

---

## Aggressive Scan

```bash
sudo nmap -A 192.168.1.10
```

---

# Nmap Workflow

A common penetration testing workflow:

### Step 1

Discover hosts

```bash
nmap -sn 192.168.1.0/24
```

### Step 2

Find open ports

```bash
nmap -p- 192.168.1.10
```

### Step 3

Detect services

```bash
nmap -sV 192.168.1.10
```

### Step 4

Run scripts

```bash
nmap -sC 192.168.1.10
```

### Step 5

Identify OS

```bash
sudo nmap -O 192.168.1.10
```

---

# Nmap in Cyber Security

Nmap is heavily used in:

* Penetration Testing
* Red Teaming
* Network Auditing
* Vulnerability Assessment
* Asset Discovery
* Security Monitoring

