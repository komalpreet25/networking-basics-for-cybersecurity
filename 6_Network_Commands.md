# Network Commands

## Description

This document explains common networking commands used for troubleshooting, monitoring, and managing networks. These commands are widely used by network administrators, system administrators, and cybersecurity professionals.

---

# Why Network Commands are Important

Network commands help us:

* Verify network connectivity
* Troubleshoot network problems
* Check IP configurations
* Analyze routing paths
* Resolve DNS issues
* Monitor active network connections

---

# 1. ping

The ping command is used to test connectivity between two devices on a network.

### Syntax

```bash
ping google.com
```

### Example

```bash
ping 8.8.8.8
```

### Uses

* Check internet connectivity
* Verify host availability
* Measure network latency

### Important Terms

#### Reply

```text
Reply from 8.8.8.8
```

The target device is reachable.

#### Request Timed Out

```text
Request timed out.
```

The target did not respond.

#### TTL (Time To Live)

TTL limits how long a packet can travel through routers before being discarded.

---

# 2. traceroute / tracert

Traceroute shows the path packets take from source to destination.

### Linux

```bash
traceroute google.com
```

### Windows

```cmd
tracert google.com
```

### Uses

* Identify network delays
* Locate routing issues
* Analyze packet paths

---

# 3. nslookup

Used to query DNS servers and resolve domain names.

### Example

```bash
nslookup google.com
```

### Output

```text
Name: google.com
Address: 142.x.x.x
```

### Uses

* Verify DNS records
* Troubleshoot DNS issues
* Find IP addresses of domains

---

# 4. dig

dig (Domain Information Groper) is an advanced DNS lookup tool available mainly on Linux.

### Example

```bash
dig google.com
```

### Query Specific Record

```bash
dig google.com MX
```

### Uses

* DNS troubleshooting
* Query DNS records
* Security investigations

---

# 5. ipconfig

Used in Windows to display network configuration.

### Example

```cmd
ipconfig
```

### Detailed Information

```cmd
ipconfig /all
```

### Uses

* View IP address
* View subnet mask
* View default gateway
* View DNS servers

---

# 6. ifconfig

Used in Linux to display network interface information.

### Example

```bash
ifconfig
```

### Uses

* View network interfaces
* Check IP addresses
* Diagnose network issues

---

# 7. ip a

Modern Linux command used instead of ifconfig.

### Example

```bash
ip a
```

### Uses

* Display interfaces
* View IPv4 and IPv6 addresses
* Check network status

---

# 8. netstat

Displays active network connections and listening ports.

### Example

```bash
netstat -an
```

### Show Listening Ports

```bash
netstat -tulnp
```

### Uses

* View active connections
* Check open ports
* Detect suspicious connections

---

# 9. arp

Displays and manages the ARP cache.

### Example

```bash
arp -a
```

### Uses

* View MAC addresses
* Troubleshoot LAN issues
* Understand IP-to-MAC mapping

---

# 10. route

Displays and modifies routing tables.

### Example

```bash
route -n
```

### Uses

* View routing information
* Troubleshoot routing problems
* Analyze network paths

---

# 11. hostname

Displays the system hostname.

### Example

```bash
hostname
```

### Uses

* Identify systems on a network
* Verify host configuration

---

# 12. whois

Provides information about domain registrations.

### Example

```bash
whois google.com
```

### Uses

* Domain investigation
* Security assessments
* Information gathering

---

# 13. curl

Transfers data from servers and APIs.

### Example

```bash
curl https://example.com
```

### View HTTP Headers

```bash
curl -I https://example.com
```

### Uses

* API testing
* Download content
* Security testing

---

# 14. wget

Used to download files from the internet.

### Example

```bash
wget https://example.com/file.zip
```

### Uses

* Download files
* Download websites
* Automation scripts

---

# Common Commands for Cyber Security

```bash
ping 8.8.8.8
traceroute google.com
nslookup google.com
dig google.com
netstat -tulnp
arp -a
route -n
curl -I https://example.com
```

These commands are frequently used during:

* Network Troubleshooting
* Penetration Testing
* Reconnaissance
* Incident Response
* Security Monitoring



