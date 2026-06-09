# Wireshark Basics

## Description

This document introduces Wireshark, one of the most popular network protocol analyzers used for network troubleshooting, monitoring, and cybersecurity investigations.

---

# What is Wireshark?

Wireshark is a packet analyzer that captures and analyzes network traffic in real time.

It allows users to inspect packets traveling across a network and understand how devices communicate.

---

# Why is Wireshark Important?

Wireshark helps:

* Monitor network traffic
* Troubleshoot network issues
* Analyze protocols
* Detect suspicious activity
* Investigate security incidents
* Learn networking concepts

---

# Key Features

* Real-time packet capture
* Deep packet inspection
* Protocol analysis
* Filtering capabilities
* Traffic statistics
* Export captured packets

---

# Understanding a Packet

A packet is a unit of data transmitted over a network.

A packet usually contains:

```text id="pkt1"
Source IP
Destination IP
Protocol
Source Port
Destination Port
Payload Data
```

Wireshark allows us to inspect all these details.

---

# Installing Wireshark

### Linux

```bash id="ws1"
sudo apt install wireshark
```

### Verify Installation

```bash id="ws2"
wireshark
```

---

# Starting Packet Capture

### Step 1

Open Wireshark.

### Step 2

Select a network interface.

Examples:

```text id="iface1"
eth0
wlan0
Ethernet
Wi-Fi
```

### Step 3

Click the Start Capture button.

Wireshark will begin displaying packets in real time.

---

# Wireshark Interface

The interface is divided into three sections.

## 1. Packet List Pane

Displays all captured packets.

Information shown:

```text id="pane1"
Packet Number
Time
Source
Destination
Protocol
Length
Info
```

---

## 2. Packet Details Pane

Displays detailed protocol information.

Examples:

```text id="pane2"
Ethernet Header
IP Header
TCP Header
HTTP Header
```

---

## 3. Packet Bytes Pane

Displays raw packet data in hexadecimal and ASCII format.

---

# Common Protocols Seen in Wireshark

## ARP

Address Resolution Protocol.

Purpose:

```text id="arp1"
Maps IP Address to MAC Address
```

---

## ICMP

Internet Control Message Protocol.

Used by:

```text id="icmp1"
ping
```

---

## TCP

Transmission Control Protocol.

Characteristics:

* Reliable
* Connection-oriented
* Error checking

Examples:

```text id="tcp1"
HTTP
HTTPS
SSH
FTP
```

---

## UDP

User Datagram Protocol.

Characteristics:

* Faster
* Connectionless
* No delivery guarantee

Examples:

```text id="udp1"
DNS
DHCP
VoIP
```

---

## DNS

Converts domain names into IP addresses.

Example:

```text id="dns1"
google.com → IP Address
```

---

## HTTP

Used for web communication.

Default Port:

```text id="http1"
80
```

---

## HTTPS

Secure web communication.

Default Port:

```text id="https1"
443
```

---

# Display Filters

Filters help focus on specific traffic.

## Show Only ICMP

```text id="f1"
icmp
```

---

## Show Only TCP

```text id="f2"
tcp
```

---

## Show Only UDP

```text id="f3"
udp
```

---

## Show Only DNS

```text id="f4"
dns
```

---

## Show Only HTTP

```text id="f5"
http
```

---

## Show Only HTTPS

```text id="f6"
tcp.port == 443
```

---

## Filter by IP Address

```text id="f7"
ip.addr == 192.168.1.10
```

---

# Capturing Ping Traffic

Open terminal and run:

```bash id="ping1"
ping google.com
```

In Wireshark apply filter:

```text id="ping2"
icmp
```

You will see:

```text id="ping3"
Echo Request
Echo Reply
```

This helps analyze ICMP communication.

---

# Following a TCP Stream

Right-click a TCP packet and select:

```text id="tcpstream"
Follow → TCP Stream
```

This shows the complete conversation between client and server.

---

# Useful Statistics

Navigate to:

```text id="stats1"
Statistics → Protocol Hierarchy
```

Shows protocol usage percentages.

---

```text id="stats2"
Statistics → Conversations
```

Shows communication between hosts.

---

```text id="stats3"
Statistics → Endpoints
```

Shows active devices in the capture.

---

# Exporting Captures

Save packet captures as:

```text id="pcap"
.pcap
.pcapng
```

These files can be analyzed later.

---

# Wireshark in Cyber Security

Wireshark is used for:

* Network Forensics
* Incident Response
* Malware Analysis
* Threat Hunting
* Packet Analysis
* Security Investigations

---

