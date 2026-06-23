# Day 05 - How the Internet Actually Works

## Objective
Understand what happens behind the scenes when we type a website address like `www.google.com` into a browser and learn the role of IP addresses and internet communication.

---

## Lesson of the Day

Today, I learned that the internet is not magic. A lot of things happen within a few milliseconds when we type `www.google.com` and press Enter.

I also learned that every device connected to the internet has a unique identifier called an **IP Address**, and every step involved in loading a website can potentially be attacked by cybercriminals.

---

## What is an IP Address?

An **IP (Internet Protocol) Address** is a unique number assigned to every device connected to the internet.

Examples:
- IPv4: `142.250.193.78`
- IPv6: `2404:6800:4009:80a::200e`

IP addresses allow devices to identify and communicate with each other over the internet.

---

## IPv4 vs IPv6

### IPv4 (Internet Protocol Version 4)
- Uses a 32-bit address.
- Supports approximately **4.3 billion** unique addresses.
- Example: `192.168.1.1`

Initially, it seemed impossible to run out of IPv4 addresses, but due to the rapid growth of the internet and connected devices, the available IPv4 addresses were exhausted around **2011**.

### IPv6 (Internet Protocol Version 6)
- Uses a 128-bit address.
- Supports an enormous number of addresses (approximately **340 undecillion** addresses).
- Example: `2001:db8::1`

Today, many modern systems and networks support IPv6 to overcome IPv4 limitations.

---

# What Happens When We Type `www.google.com` and Press Enter?

There are seven major steps:

## 1. Browser Parses the URL
The browser understands:
- Protocol (HTTPS)
- Domain Name (`google.com`)
- Path and resources required

**Possible attacks:**
- Malicious URLs
- URL spoofing
- Phishing links

---

## 2. DNS Lookup
The browser asks a DNS server to convert `google.com` into an IP address.

Example:
```
google.com → 142.250.xxx.xxx
```

**Possible attacks:**
- DNS Spoofing
- DNS Poisoning
- DNS Hijacking

---

## 3. TCP Handshake
The computer establishes a connection with the server using the **Three-Way Handshake**:

1. SYN
2. SYN-ACK
3. ACK

**Possible attacks:**
- SYN Flood Attacks
- TCP Session Hijacking
- Denial of Service (DoS)

---

## 4. TLS Handshake
A secure encrypted connection is established.

The browser:
- Verifies certificates
- Negotiates encryption keys
- Creates a secure HTTPS session

**Possible attacks:**
- Man-in-the-Middle (MITM)
- Certificate Spoofing
- SSL Stripping

---

## 5. HTTP Request Sent
The browser sends a request to the web server.

Example:
```
GET / HTTP/1.1
Host: google.com
```

**Possible attacks:**
- Request Manipulation
- Injection Attacks
- Header Tampering

---

## 6. Server Processes and Responds
The server processes the request and returns the required resources.

**Possible attacks:**
- SQL Injection
- Remote Code Execution (RCE)
- Server Misconfigurations
- Denial of Service (DoS)

---

## 7. Browser Renders the Page
The browser receives the response and displays the webpage.

**Possible attacks:**
- Cross-Site Scripting (XSS)
- Malicious JavaScript
- Drive-by Downloads

---

## Important Learning

One of the biggest takeaways from today was:

> Every step involved in loading a webpage can be attacked.

Cybersecurity professionals need to understand how the internet works because each stage introduces different security risks and attack opportunities.

---

## Key Takeaways

✅ Every device on the internet has an IP address.

✅ IPv4 addresses were exhausted, leading to the adoption of IPv6.

✅ Loading a webpage involves multiple processes happening in milliseconds.

✅ The seven steps are:
1. Browser Parses URL
2. DNS Lookup
3. TCP Handshake
4. TLS Handshake
5. HTTP Request
6. Server Response
7. Browser Rendering

✅ Every one of these stages can be a potential attack surface.

---

## Reflection

Today's lesson completely changed how I look at the internet. Earlier, I simply typed a website address and expected it to open. Now I understand that multiple protocols and processes work together behind the scenes.

I also realized that cybersecurity is deeply connected to networking because every stage of communication can become an attack vector.

---

## Quote of the Day

> "The internet may look simple from the outside, but behind every click lies an entire chain of protocols, processes, and potential attack surfaces."

---

## Progress Tracker

- Day: 05/90
- Topic: How the Internet Actually Works
- Concepts Learned: IP Address, IPv4, IPv6, DNS, TCP Handshake, TLS, HTTP, Browser Rendering
- Key Insight: Every stage of loading a webpage can be attacked.












- Status: ✅ Completed
