# networking-basics-for-cybersecurity
# IP Addressing
This document explains the fundamentals of IP addressing, including IPv4, IPv6, public and private IP addresses, loopback addresses, and their role in network communication.

## What is an IP Address?

An IP (Internet Protocol) Address is a unique numerical identifier assigned to every device connected to a network. It helps devices communicate with each other over the internet or a local network.

### Example

* 192.168.1.1
* 8.8.8.8
Without an IP address, devices would not be able to send or receive data.
---

## Types of IP Addresses

### 1. IPv4

IPv4 is the most commonly used version of IP addressing. An IPv4 address (Internet Protocol version 4) is a unique numerical label assigned to every device connected to a computer network that uses the Internet Protocol for communication.

### Structure of an IPv4 Address

An IPv4 address is made up of 32 bits (binary digits), which means it is a string of 32 ones and zeros inside the computer's memory. Because binary is hard for humans to read, it is written in dotted-decimal notation.

### Here is how it is broken down:

Four Octets: The 32 bits are divided into four 8-bit groups called octets.

Decimal Range: Each octet is converted into a decimal number ranging from 0 to 255.

Separators: The four decimal numbers are separated by periods (dots).

### Example: 
```text
192.168.1.1
```
---

### 2. IPv6

IPv6 was introduced to overcome the shortage of IPv4 addresses. IPv6 (Internet Protocol version 6) is the most recent generation of the Internet Protocol. It was designed by the Internet Engineering Task Force (IETF) to replace IPv4, the aging protocol that still carries the majority of today's internet traffic.

### The Main Upgrade:
Infinite Address SpaceWhile IPv4 uses a 32-bit address (creating roughly 4.3 billion addresses), IPv6 uses a 128-bit address architecture.This mathematical jump expands the available address pool to:
                         {Total Addresses} = 2^{128} \approx 340 \text{ undecillion addresses}

### Structure of an IPv6 Address
Because an IPv6 address is so long, it is written in hexadecimal format (using numbers 0–9 and letters A–F) instead of decimal notation, and it uses colons instead of periods.

Eight Groups: The 128 bits are divided into eight 16-bit groups (called blocks or hextets).

Format: XXXX:XXXX:XXXX:XXXX:XXXX:XXXX:XXXX:XXXX

### A Real Example:
```text
2001:0db8:85a3:0000:0000:8a2e:0370:7334
```                    
---

## Public vs Private IP Address

### Public IP

* Assigned by an Internet Service Provider (ISP)
* Accessible over the internet

Example:

```text
103.25.45.100
```
---

### Private IP

* Used within local networks
* Not directly accessible from the internet

Private IP Ranges:

```text
10.0.0.0 - 10.255.255.255
172.16.0.0 - 172.31.255.255
192.168.0.0 - 192.168.255.255
```
---

## Loopback Address

The loopback address is used to test network functionality on the local machine.A loopback address is a special, virtual IP address that a device uses to send network traffic back to itself.
When a computer sends data to a loopback address, that data never actually leaves the device, passes onto the local network, or reaches the physical network interface card (NIC). Instead, the operating system's network stack intercepts the traffic at the software level and routes it right back to the originating device.

Example:

```text
127.0.0.1
```

Common Name:

```text
localhost
```
---

## How to Check Your IP Address

### Linux

```bash
ip a
```

### Windows

```cmd
ipconfig
```

---

## Importance of IP Addressing

* Identifies devices on a network
* Enables communication between devices
* Essential for internet connectivity
* Used in routing and network management

---

## Summary

* IP Address uniquely identifies a device on a network.
* IPv4 uses 32 bits, while IPv6 uses 128 bits.
* IP addresses can be Public or Private.
* 127.0.0.1 is the loopback address used for testing.
* Every device connected to a network requires an IP address.

