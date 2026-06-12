# Domain Name System (DNS)

## Description

This document explains the Domain Name System (DNS), one of the most important services on the internet. DNS translates human-readable domain names into IP addresses so that devices can communicate with each other.

---

# What is DNS?

DNS (Domain Name System) is often called the "Phonebook of the Internet."

Humans remember names like:

```text
google.com
github.com
youtube.com
```

Computers communicate using IP addresses:

```text
142.250.183.14
140.82.114.4
```

DNS converts domain names into IP addresses.

---

# Why DNS is Important

Without DNS, users would need to remember IP addresses for every website.

Instead of typing:

```text
142.250.183.14
```

Users simply type:

```text
google.com
```

DNS handles the translation automatically.

---

# How DNS Works

When a user visits a website:

### Step 1

User enters:

```text
www.google.com
```

### Step 2

The computer checks its local DNS cache.

### Step 3

If no record is found, a DNS query is sent to a DNS resolver.

### Step 4

The resolver contacts DNS servers.

### Step 5

The correct IP address is returned.

### Step 6

The browser connects to the web server.

---

# DNS Hierarchy

DNS follows a hierarchical structure.

```text
Root DNS Server
      │
Top-Level Domain (TLD)
      │
Authoritative DNS Server
      │
Domain Record
```

Example:

```text
www.google.com
```

* Root Server
* .com TLD Server
* Google Authoritative Server

---

# Types of DNS Servers

## 1. Recursive Resolver

Receives DNS requests from clients and finds the answer.

Examples:

```text
Google DNS
Cloudflare DNS
ISP DNS
```

---

## 2. Root Name Server

The highest level in the DNS hierarchy.

Responsibilities:

* Direct requests to TLD servers.

---

## 3. TLD Server

Manages domains under:

```text
.com
.org
.net
.edu
```

---

## 4. Authoritative Name Server

Contains the actual DNS records of a domain.

Provides final answers to DNS queries.

---

# Common DNS Records

## A Record

Maps a domain name to an IPv4 address.

Example:

```text
google.com → 142.250.183.14
```

---

## AAAA Record

Maps a domain name to an IPv6 address.

Example:

```text
google.com → IPv6 Address
```

---

## CNAME Record

Creates an alias for another domain.

Example:

```text
www.example.com
      ↓
example.com
```

---

## MX Record

Mail Exchange Record.

Used for email routing.

Example:

```text
gmail.com → Mail Server
```

---

## NS Record

Name Server Record.

Specifies authoritative DNS servers.

Example:

```text
ns1.example.com
ns2.example.com
```

---

## TXT Record

Stores text-based information.

Commonly used for:

```text
SPF
DKIM
Domain Verification
```

---

# DNS Port

DNS primarily uses:

```text
53/UDP
```

For large responses and zone transfers:

```text
53/TCP
```

---

# DNS Lookup Tools

## nslookup

Query DNS information.

Example:

```bash
nslookup google.com
```

---

## dig

Advanced DNS lookup tool.

Example:

```bash
dig google.com
```

---

## Reverse Lookup

Find a domain from an IP address.

Example:

```bash
nslookup 8.8.8.8
```

---

# DNS Cache

Operating systems store DNS results temporarily.

Benefits:

* Faster browsing
* Reduced DNS traffic
* Improved performance

---

# Flush DNS Cache

## Windows

```cmd
ipconfig /flushdns
```

---

## Linux (systemd)

```bash
sudo systemd-resolve --flush-caches
```

---

# Public DNS Servers

## Google DNS

```text
8.8.8.8
8.8.4.4
```

---

## Cloudflare DNS

```text
1.1.1.1
1.0.0.1
```

---

## OpenDNS

```text
208.67.222.222
208.67.220.220
```

---

# DNS in Cyber Security

DNS plays an important role in cybersecurity investigations.

Security professionals analyze DNS traffic to:

* Detect malware communication
* Identify phishing domains
* Investigate suspicious activity
* Monitor network behavior

---

# DNS Attacks

## DNS Spoofing

Attackers provide fake DNS responses.

Result:

```text
User → Fake Website
```

Instead of:

```text
User → Legitimate Website
```

---

## DNS Cache Poisoning

Malicious DNS records are inserted into cache.

Users may be redirected to attacker-controlled websites.

---

## DNS Tunneling

Attackers use DNS traffic to transfer data.

Commonly used for:

* Data Exfiltration
* Command and Control (C2)

---

## DDoS Against DNS Servers

Attackers overwhelm DNS infrastructure with traffic.

Result:

```text
Website becomes inaccessible
```

---

# Wireshark DNS Filter

Show only DNS packets:

```text
dns
```

---

# Nmap DNS Enumeration

DNS-related scanning:

```bash
nmap --script dns-brute example.com
```

