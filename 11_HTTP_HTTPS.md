# HTTP and HTTPS

## Description

This document explains HTTP (HyperText Transfer Protocol) and HTTPS (HyperText Transfer Protocol Secure), the protocols used for communication between web browsers and web servers. Understanding HTTP and HTTPS is essential for networking, web development, and cybersecurity.

---

# What is HTTP?

HTTP stands for **HyperText Transfer Protocol**.

It is the foundation of communication on the World Wide Web.

HTTP allows:

* Browsers to request web pages
* Servers to send web content
* Data exchange between clients and servers

---

# HTTP Communication Model

HTTP follows a Client-Server architecture.

```text
Client (Browser)
       │
       │ Request
       ▼
Web Server
       │
       │ Response
       ▼
Client
```

Example:

```text
Browser → Request → Server
Browser ← Response ← Server
```

---

# Default HTTP Port

HTTP uses:

```text
TCP Port 80
```

---

# What is HTTPS?

HTTPS stands for **HyperText Transfer Protocol Secure**.

It is the secure version of HTTP.

HTTPS encrypts communication using:

```text
SSL/TLS
```

This protects data from attackers.

---

# Default HTTPS Port

HTTPS uses:

```text
TCP Port 443
```

---

# Why HTTPS is Important

Without HTTPS:

```text
User → Internet → Website
```

Attackers may intercept traffic.

With HTTPS:

```text
User → Encrypted Traffic → Website
```

Sensitive information remains protected.

Examples:

* Passwords
* Banking Information
* Credit Card Data
* Personal Information

---

# HTTP vs HTTPS

| Feature         | HTTP                        | HTTPS                              |
| --------------- | --------------------------- | ---------------------------------- |
| Full Form       | HyperText Transfer Protocol | HyperText Transfer Protocol Secure |
| Port            | 80                          | 443                                |
| Encryption      | No                          | Yes                                |
| Security        | Low                         | High                               |
| SSL/TLS         | No                          | Yes                                |
| Data Protection | No                          | Yes                                |

---

# HTTP Request

A browser sends a request to a server.

Example:

```http
GET /index.html HTTP/1.1
Host: example.com
```

Components:

* Method
* Path
* Version
* Headers

---

# HTTP Response

The server replies with a response.

Example:

```http
HTTP/1.1 200 OK
Content-Type: text/html
```

Response contains:

* Status Code
* Headers
* Content

---

# Common HTTP Methods

## GET

Retrieves data from a server.

Example:

```http
GET /products
```

Purpose:

```text
Read Data
```

---

## POST

Sends data to a server.

Example:

```http
POST /login
```

Purpose:

```text
Create Data
```

---

## PUT

Updates existing data.

Example:

```http
PUT /user/1
```

Purpose:

```text
Update Data
```

---

## DELETE

Removes data.

Example:

```http
DELETE /user/1
```

Purpose:

```text
Delete Data
```

---

## PATCH

Partially updates data.

Example:

```http
PATCH /user/1
```

---

## HEAD

Retrieves headers only.

Example:

```http
HEAD /index.html
```

---

## OPTIONS

Shows supported methods.

Example:

```http
OPTIONS /
```

---

# Common HTTP Status Codes

## 200 OK

```text
Request Successful
```

---

## 301 Moved Permanently

```text
Resource Permanently Redirected
```

---

## 302 Found

```text
Temporary Redirect
```

---

## 400 Bad Request

```text
Invalid Request
```

---

## 401 Unauthorized

```text
Authentication Required
```

---

## 403 Forbidden

```text
Access Denied
```

---

## 404 Not Found

```text
Page Not Found
```

---

## 500 Internal Server Error

```text
Server Error
```

---

## 503 Service Unavailable

```text
Server Temporarily Unavailable
```

---

# HTTP Headers

Headers provide additional information.

Examples:

```http
User-Agent
Host
Cookie
Authorization
Referer
Content-Type
```

---

# Cookies

Cookies store information in the browser.

Examples:

```text
Session ID
User Preferences
Authentication Tokens
```

Purpose:

* Maintain sessions
* Track users
* Improve user experience

---

# Sessions

A session allows a server to remember a user between requests.

Example:

```text
Login
↓
Session Created
↓
User Remains Authenticated
```

---

# SSL/TLS

SSL/TLS provides:

* Encryption
* Integrity
* Authentication

Benefits:

```text
Confidentiality
Integrity
Authentication
```

---

# HTTPS Handshake Simplified

Step 1:

```text
Client → Hello
```

Step 2:

```text
Server → Certificate
```

Step 3:

```text
Key Exchange
```

Step 4:

```text
Encrypted Communication Begins
```

---

# Digital Certificates

Certificates prove a website's identity.

Example:

```text
example.com Certificate
```

Issued by:

```text
Certificate Authority (CA)
```

Examples:

* Let's Encrypt
* DigiCert
* GlobalSign

---

# HTTP Security Risks

HTTP traffic is not encrypted.

Risks include:

* Packet Sniffing
* Session Hijacking
* Credential Theft
* Man-in-the-Middle Attacks

---

# HTTPS Security Benefits

HTTPS helps prevent:

* Eavesdropping
* Credential Theft
* Data Manipulation
* Session Interception

---

# Viewing HTTP Traffic

Using curl:

```bash
curl http://example.com
```

---

# Viewing HTTP Headers

```bash
curl -I https://example.com
```

---

# HTTP Analysis in Wireshark

Display HTTP traffic:

```text
http
```

Display HTTPS traffic:

```text
tcp.port == 443
```

---

# HTTP Analysis with Burp Suite

Burp Suite can:

* Intercept Requests
* Modify Requests
* Analyze Responses
* Test Web Security

Commonly used by:

* Penetration Testers
* Bug Bounty Hunters
* Security Researchers

