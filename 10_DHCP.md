# Dynamic Host Configuration Protocol (DHCP)

## Description

This document explains DHCP (Dynamic Host Configuration Protocol), a network management protocol used to automatically assign IP addresses and other network configuration information to devices on a network.

---

# What is DHCP?

DHCP stands for **Dynamic Host Configuration Protocol**.

It automatically provides network configuration information to devices such as:

* Computers
* Laptops
* Smartphones
* Printers
* Servers
* IoT Devices

Without DHCP, administrators would need to manually configure IP addresses for every device.

---

# Why DHCP is Important

DHCP simplifies network management by automatically assigning:

```text
IP Address
Subnet Mask
Default Gateway
DNS Server
```

Benefits:

* Saves time
* Reduces configuration errors
* Prevents IP conflicts
* Simplifies network administration

---

# Example Without DHCP

Imagine an office with 500 computers.

Without DHCP:

* Every IP address must be configured manually.
* Mistakes can cause connectivity issues.
* Duplicate IP addresses may occur.

With DHCP:

* Everything is assigned automatically.

---

# How DHCP Works

When a device joins a network, it requests an IP address from the DHCP server.

The process follows four steps known as **DORA**.

---

# DHCP DORA Process

## 1. Discover

The client broadcasts a request.

```text
DHCP Discover
```

Meaning:

```text
Is there any DHCP server available?
```

---

## 2. Offer

The DHCP server responds.

```text
DHCP Offer
```

Meaning:

```text
I can provide this IP address.
```

Example:

```text
192.168.1.100
```

---

## 3. Request

The client requests the offered IP address.

```text
DHCP Request
```

Meaning:

```text
I would like to use this IP address.
```

---

## 4. Acknowledge

The DHCP server confirms.

```text
DHCP ACK
```

Meaning:

```text
The IP address is now assigned to you.
```

---

# DHCP DORA Diagram

```text
Client                    DHCP Server

Discover  ------------->

          <-------------  Offer

Request   ------------->

          <-------------  ACK
```

---

# DHCP Ports

DHCP uses UDP.

| Device      | Port   |
| ----------- | ------ |
| DHCP Server | UDP 67 |
| DHCP Client | UDP 68 |

---

# DHCP Lease

A DHCP lease is the amount of time an IP address is assigned to a device.

Example:

```text
24 Hours
7 Days
30 Days
```

After expiration, the client must renew the lease.

---

# DHCP Lease Renewal

The client attempts to renew its IP address before expiration.

Benefits:

* Maintains connectivity
* Reduces network disruptions

---

# DHCP Components

## DHCP Server

Assigns IP addresses and network settings.

Examples:

* Windows Server
* Linux DHCP Server
* Router

---

## DHCP Client

Requests network configuration.

Examples:

* PC
* Laptop
* Smartphone

---

## DHCP Relay Agent

Forwards DHCP requests between different networks.

Used when:

```text
Client and DHCP Server are on different subnets
```

---

# Information Provided by DHCP

DHCP can provide:

```text
IP Address
Subnet Mask
Default Gateway
DNS Server
Domain Name
Lease Time
```

---

# Checking DHCP Information

## Windows

Display full configuration:

```cmd
ipconfig /all
```

Look for:

```text
DHCP Enabled : Yes
```

---

## Linux

Using ip command:

```bash
ip a
```

---

## Check Lease Information

```bash
cat /var/lib/dhcp/dhclient.leases
```

---

# DHCP Reservation

A DHCP reservation assigns the same IP address to a specific device.

Based on:

```text
MAC Address
```

Example:

```text
Printer → Always receives 192.168.1.50
```

Benefits:

* Consistent addressing
* Easier management

---

# DHCP Scope

A DHCP scope is a range of IP addresses available for assignment.

Example:

```text
192.168.1.100
to
192.168.1.200
```

The server can assign addresses only from this range.

---

# DHCP in Home Networks

Typical process:

```text
Router
      ↓
DHCP Server
      ↓
Assigns IP Addresses
      ↓
Connected Devices
```

Most home routers act as DHCP servers.

---

# DHCP in Enterprise Networks

Enterprise networks often use:

* Dedicated DHCP Servers
* Redundant DHCP Servers
* DHCP Relay Agents

Benefits:

* Scalability
* High Availability
* Centralized Management

---

# DHCP Security Risks

Although useful, DHCP can be abused.

---

## Rogue DHCP Server

An attacker installs an unauthorized DHCP server.

Effects:

* Wrong Gateway
* Wrong DNS Server
* Traffic Redirection

---

## DHCP Starvation Attack

An attacker floods the DHCP server with requests.

Result:

```text
No IP addresses available for legitimate users
```

---

## Man-in-the-Middle Attacks

A malicious DHCP server may provide:

```text
Fake Gateway
Fake DNS Server
```

This allows traffic interception.

---

# DHCP Protection Mechanisms

Common protections:

* DHCP Snooping
* Port Security
* Network Access Control (NAC)
* Switch Security Features

---

# DHCP and DNS Relationship

DHCP provides:

```text
IP Address
DNS Server Address
```

DNS provides:

```text
Domain Name Resolution
```

Together they allow users to access websites easily.

Example:

```text
DHCP → Assigns IP Address
DNS → Resolves google.com
```

---

# Wireshark DHCP Filter

Display only DHCP traffic:

```text
bootp
```

You can observe:

```text
Discover
Offer
Request
ACK
```

