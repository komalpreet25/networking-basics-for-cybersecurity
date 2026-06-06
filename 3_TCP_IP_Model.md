# TCP/IP Model

## Description

This document explains the TCP/IP Model, its layers, functions, and how data travels across a network. The TCP/IP Model is the foundation of modern internet communication and is widely used in networking and cybersecurity.

---

## What is the TCP/IP Model?

The TCP/IP (Transmission Control Protocol/Internet Protocol) Model is a set of communication protocols used to connect devices over the internet and local networks.

It defines how data is transmitted, received, and processed between devices.

---

## Layers of the TCP/IP Model

The TCP/IP Model consists of four layers:

```text
Application Layer
Transport Layer
Internet Layer
Network Access Layer
```

---

## 1. Application Layer

The Application Layer provides network services directly to users and applications.

### Common Protocols

```text
HTTP
HTTPS
FTP
SMTP
DNS
SSH
```

### Functions

* Web browsing
* Email communication
* File transfers
* Domain name resolution

---

## 2. Transport Layer

The Transport Layer is responsible for end-to-end communication and data delivery.

### Common Protocols

```text
TCP
UDP
```

### TCP (Transmission Control Protocol)

* Connection-oriented
* Reliable communication
* Error checking
* Data retransmission

Example:

```text
Websites, Email, File Transfers
```

### UDP (User Datagram Protocol)

* Connectionless
* Faster than TCP
* No delivery guarantee

Example:

```text
Online Gaming
Video Streaming
VoIP Calls
```

---

## 3. Internet Layer

The Internet Layer handles logical addressing and routing.

### Common Protocols

```text
IP
ICMP
ARP
```

### Functions

* Assigning IP addresses
* Routing packets
* Network communication

Example:

```text
192.168.1.10 → 8.8.8.8
```

---

## 4. Network Access Layer

The Network Access Layer is responsible for physical network communication.

### Technologies

```text
Ethernet
Wi-Fi
Switches
Network Cards
```

### Functions

* Sending and receiving data frames
* Physical transmission of data
* MAC addressing

---

## Data Flow in TCP/IP Model

When you open a website:

```text
Application Layer → Creates HTTP Request
Transport Layer → Adds TCP Information
Internet Layer → Adds IP Address
Network Access Layer → Sends Data
```

At the destination, the process occurs in reverse order.

---

## TCP/IP vs OSI Model

| TCP/IP Model   | OSI Model                          |
| -------------- | ---------------------------------- |
| Application    | Application, Presentation, Session |
| Transport      | Transport                          |
| Internet       | Network                            |
| Network Access | Data Link, Physical                |

### Key Difference

* TCP/IP has 4 layers.
* OSI has 7 layers.
* TCP/IP is used in real-world networking.

---

## Importance in Cybersecurity

Understanding the TCP/IP Model helps security professionals:

* Analyze network traffic
* Detect attacks
* Use tools like Wireshark
* Understand packet flow
* Troubleshoot network issues

---

## Summary

* TCP/IP is the foundation of internet communication.
* It consists of four layers.
* Each layer performs a specific networking function.
* TCP provides reliable communication, while UDP prioritizes speed.
* Understanding the TCP/IP Model is essential for networking and cybersecurity.
