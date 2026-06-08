# Common Ports and Services

## Description

This document explains common network ports and the services associated with them. Understanding ports is essential for networking, system administration, penetration testing, and cybersecurity.

---

## What is a Port?

A port is a logical communication endpoint used by applications and services to send and receive data over a network.

An IP address identifies a device, while a port identifies a specific service running on that device.

### Example

```text
192.168.1.10:80
```

* IP Address = 192.168.1.10
* Port = 80
* Service = HTTP

---

## Types of Ports

### Well-Known Ports (0-1023)

Used by common protocols and services.

### Registered Ports (1024-49151)

Used by applications and software.

### Dynamic/Ephemeral Ports (49152-65535)

Temporarily assigned by operating systems.

---

## Common Ports and Services

| Port | Protocol | Service                       |
| ---- | -------- | ----------------------------- |
| 20   | TCP      | FTP Data                      |
| 21   | TCP      | FTP Control                   |
| 22   | TCP      | SSH                           |
| 23   | TCP      | Telnet                        |
| 25   | TCP      | SMTP                          |
| 53   | TCP/UDP  | DNS                           |
| 67   | UDP      | DHCP Server                   |
| 68   | UDP      | DHCP Client                   |
| 69   | UDP      | TFTP                          |
| 80   | TCP      | HTTP                          |
| 110  | TCP      | POP3                          |
| 123  | UDP      | NTP                           |
| 135  | TCP      | RPC                           |
| 137  | UDP      | NetBIOS Name Service          |
| 138  | UDP      | NetBIOS Datagram Service      |
| 139  | TCP      | NetBIOS Session Service       |
| 143  | TCP      | IMAP                          |
| 161  | UDP      | SNMP                          |
| 162  | UDP      | SNMP Trap                     |
| 389  | TCP/UDP  | LDAP                          |
| 443  | TCP      | HTTPS                         |
| 445  | TCP      | SMB                           |
| 465  | TCP      | SMTPS                         |
| 514  | UDP      | Syslog                        |
| 587  | TCP      | SMTP Submission               |
| 636  | TCP      | LDAPS                         |
| 993  | TCP      | IMAPS                         |
| 995  | TCP      | POP3S                         |
| 1433 | TCP      | Microsoft SQL Server          |
| 1521 | TCP      | Oracle Database               |
| 3306 | TCP      | MySQL                         |
| 3389 | TCP      | Remote Desktop Protocol (RDP) |
| 5432 | TCP      | PostgreSQL                    |
| 5900 | TCP      | VNC                           |
| 8080 | TCP      | Alternative HTTP              |

---

## Important Ports for Cyber Security

### Port 21 - FTP

Used for file transfers.

Risk:

* Credentials may be transmitted in plain text.

---

### Port 22 - SSH

Used for secure remote administration.

Risk:

* Brute-force attacks.

---

### Port 23 - Telnet

Used for remote access.

Risk:

* No encryption.
* Considered insecure.

---

### Port 53 - DNS

Used for domain name resolution.

Risk:

* DNS Spoofing
* DNS Tunneling

---

### Port 80 - HTTP

Used for websites.

Risk:

* Data transmitted without encryption.

---

### Port 443 - HTTPS

Secure web communication.

Risk:

* SSL/TLS misconfigurations.

---

### Port 445 - SMB

Used for file and printer sharing.

Risk:

* Common target for ransomware and lateral movement.

---

### Port 3389 - RDP

Used for remote desktop access.

Risk:

* Brute-force attacks.
* Unauthorized remote access.

---

## Checking Open Ports with Nmap

### Scan Common Ports

```bash
nmap 192.168.1.1
```

### Scan All Ports

```bash
nmap -p- 192.168.1.1
```

### Service Version Detection

```bash
nmap -sV 192.168.1.1
```

---

## Why Ports Matter?

Ports help:

* Identify running services
* Troubleshoot network issues
* Detect vulnerabilities
* Perform security assessments
* Configure firewalls

---

## Summary

* Ports identify services running on a system.
* Every network service uses a specific port.
* Understanding ports is essential for networking and cybersecurity.
* Tools like Nmap and Wireshark are used to analyze ports and services.
* Some ports are frequently targeted by attackers and should be monitored carefully.
