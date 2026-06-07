# Network Protocols

## Description

This document explains common network protocols used in networking and cybersecurity. Protocols define the rules that devices follow to communicate and exchange data across a network.

---

## What is a Network Protocol?

A network protocol is a set of rules and standards that enables devices to communicate with each other over a network.

Without protocols, computers would not understand how to send, receive, or process data.

---

## Common Network Protocols

### 1. HTTP (HyperText Transfer Protocol)

HTTP is used to transfer web pages between web servers and web browsers.

#### Default Port

```text
80
```

#### Example

```text
http://example.com
```

#### Features

* Used for web browsing
* Data is transmitted in plain text
* Not encrypted

---

### 2. HTTPS (HyperText Transfer Protocol Secure)

HTTPS is the secure version of HTTP.

#### Default Port

```text
443
```

#### Example

```text
https://example.com
```

#### Features

* Encrypts communication using SSL/TLS
* Protects sensitive information
* Widely used by modern websites

---

### 3. FTP (File Transfer Protocol)

FTP is used for transferring files between systems.

#### Default Port

```text
21
```

#### Features

* Uploading files
* Downloading files
* Client-server architecture

#### Security Note

Traditional FTP is not encrypted.

---

### 4. SSH (Secure Shell)

SSH provides secure remote access to systems.

#### Default Port

```text
22
```

#### Example

```bash
ssh user@192.168.1.10
```

#### Features

* Secure remote login
* Encrypted communication
* Commonly used by system administrators

---

### 5. DNS (Domain Name System)

DNS translates domain names into IP addresses.

#### Default Port

```text
53
```

#### Example

```text
google.com → 142.250.x.x
```

#### Features

* Converts domain names to IP addresses
* Makes internet browsing easier

---

### 6. DHCP (Dynamic Host Configuration Protocol)

DHCP automatically assigns IP addresses to devices.

#### Default Ports

```text
67
68
```

#### Features

* Automatic IP assignment
* Reduces manual configuration
* Common in home and enterprise networks

---

### 7. SMTP (Simple Mail Transfer Protocol)

SMTP is used for sending emails.

#### Default Ports

```text
25
587
465
```

#### Features

* Sends outgoing emails
* Works with mail servers

---

### 8. POP3 (Post Office Protocol Version 3)

POP3 retrieves emails from a mail server.

#### Default Port

```text
110
```

#### Features

* Downloads emails to local devices
* Often removes emails from server after download

---

### 9. IMAP (Internet Message Access Protocol)

IMAP allows users to access emails while keeping them on the server.

#### Default Port

```text
143
```

#### Secure IMAP

```text
993
```

#### Features

* Synchronizes emails across devices
* Keeps messages on the mail server

---

## Protocol Comparison

| Protocol | Port       | Purpose               |
| -------- | ---------- | --------------------- |
| HTTP     | 80         | Web browsing          |
| HTTPS    | 443        | Secure web browsing   |
| FTP      | 21         | File transfer         |
| SSH      | 22         | Secure remote access  |
| DNS      | 53         | Domain resolution     |
| DHCP     | 67/68      | IP assignment         |
| SMTP     | 25/587/465 | Sending email         |
| POP3     | 110        | Receiving email       |
| IMAP     | 143/993    | Email synchronization |

---

## Importance in Cybersecurity

Understanding network protocols helps security professionals:

* Analyze network traffic
* Identify suspicious activity
* Detect attacks
* Configure firewalls
* Perform network troubleshooting

Tools commonly used:

```text
Wireshark
Nmap
tcpdump
Netstat
```

---

## Summary

* Network protocols define communication rules between devices.
* HTTP and HTTPS are used for web communication.
* FTP transfers files.
* SSH provides secure remote access.
* DNS resolves domain names.
* DHCP assigns IP addresses automatically.
* Email communication relies on SMTP, POP3, and IMAP.
