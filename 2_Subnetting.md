# Subnetting

## Description

This document explains the fundamentals of subnetting, including subnet masks, network IDs, host IDs, and how subnetting helps organize and manage networks efficiently.

---

## What is Subnetting?

Subnetting is the process of dividing a large network into smaller networks called subnets. It improves network performance, security, and management.

For example, instead of having one large network with hundreds of devices, subnetting allows administrators to create multiple smaller networks.

---

## Why is Subnetting Important?

* Reduces network congestion
* Improves network performance
* Enhances security
* Simplifies network management
* Conserves IP addresses

---

## Key Terms

### IP Address

A unique address assigned to a device on a network.

Example:

```text
192.168.1.10
```

### Subnet Mask

A subnet mask separates the network portion from the host portion of an IP address.

Common subnet masks:

```text
255.0.0.0
255.255.0.0
255.255.255.0
```

### Network ID

Identifies the network to which a device belongs.

### Host ID

Identifies a specific device within a network.

---

## Example

IP Address:

```text
192.168.1.100
```

Subnet Mask:

```text
255.255.255.0
```

Network ID:

```text
192.168.1.0
```

Broadcast Address:

```text
192.168.1.255
```

Valid Host Range:

```text
192.168.1.1 - 192.168.1.254
```

---

## CIDR Notation

CIDR (Classless Inter-Domain Routing) is a shorter way of writing subnet masks.

Examples:

```text
/8   = 255.0.0.0
/16  = 255.255.0.0
/24  = 255.255.255.0
```

Example:

```text
192.168.1.0/24
```

---

## Benefits of Subnetting

* Better traffic management
* Efficient use of IP addresses
* Improved security through network segmentation
* Easier troubleshooting
* Reduced broadcast traffic

---

## Summary

* Subnetting divides a network into smaller subnets.
* A subnet mask separates network and host portions.
* CIDR notation provides a compact way to represent subnet masks.
* Subnetting improves performance, security, and scalability.
