# Day 07 - Understanding DNS and Common DNS Attacks

## Objective
Understand how the Domain Name System (DNS) works, learn the DNS resolution process, and explore common attacks that target DNS.

---

## Lesson of the Day

Today, I learned how DNS (Domain Name System) works behind the scenes whenever we visit a website.

When we type `www.google.com`, the browser cannot understand the domain name directly. It needs the website's IP address. DNS is responsible for converting a domain name into an IP address.

If the IP address is already stored in a cache, the lookup is very fast. Otherwise, DNS follows a series of steps to find the correct IP address.

---

## The 8 Steps of DNS Resolution

### Step 1: Browser Cache
The browser first checks whether it has recently visited the website.

- If the IP address is found, it is used immediately.
- No further lookup is needed.

---

### Step 2: Operating System (OS) Cache
If the browser cache doesn't contain the IP address, the operating system checks its own DNS cache.

- Stores recently resolved domain names.
- Speeds up future requests.

---

### Step 3: Router Cache
If the operating system doesn't have the IP address, the request goes to the router.

- Home or office routers may cache DNS responses.
- If found, the router returns the IP address.

---

### Step 4: ISP Recursive Resolver
If the router also doesn't know the IP address, the request is sent to the ISP's recursive DNS resolver.

- Internet Service Providers keep a large cache of recently requested domains.
- If the record exists, it is returned immediately.

---

### Step 5: Root DNS Server
If the recursive resolver doesn't have the answer, it asks a Root DNS Server.

The Root Server does **not** know the IP address of `google.com`.

Instead, it directs the resolver to the appropriate Top-Level Domain (TLD) server.

For example:

```
google.com → .com TLD Server
```

---

### Step 6: TLD (Top-Level Domain) Server
The `.com` server also doesn't know Google's IP address.

Instead, it tells the resolver where Google's Authoritative DNS Server is located.

---

### Step 7: Authoritative DNS Server
This is the server managed by the website owner (Google).

It stores the actual DNS records and returns the correct IP address for `google.com`.

---

### Step 8: Back to You
The recursive resolver receives the IP address and:

- Stores it in its cache.
- Sends it back to your router.
- Router sends it to your operating system.
- Operating system sends it to the browser.
- Browser connects to the website using the IP address.

---

## DNS Lookup Flow

```
Browser Cache
      ↓
OS Cache
      ↓
Router Cache
      ↓
ISP Recursive Resolver
      ↓
Root DNS Server
      ↓
TLD Server (.com)
      ↓
Authoritative DNS Server
      ↓
Back to Resolver → Router → OS → Browser
```

---

## Performance

- A complete DNS lookup usually finishes in **under 100 milliseconds**.
- If the IP address is already available in the Browser Cache, OS Cache, Router Cache, or ISP Resolver Cache, the response is almost instant.

Caching helps reduce lookup time and improves browsing performance.

---

## Common DNS Attacks

### 1. DNS Spoofing
An attacker provides a fake DNS response so that users are redirected to a malicious website instead of the legitimate one.

---

### 2. DNS Tunneling
Attackers misuse DNS requests to secretly transfer data or communicate with compromised systems.

---

### 3. DNS Hijacking
An attacker changes DNS settings so users are redirected to fake or malicious websites without their knowledge.

---

### 4. Typosquatting
Attackers register domain names that closely resemble popular websites.

Example:

```
google.com
gooogle.com
goggle.com
```

Users who accidentally type the wrong address may land on a malicious website.

---

## What I Learned

- DNS translates domain names into IP addresses.
- DNS uses multiple layers of caching to improve speed.
- If no cache contains the IP address, DNS queries travel through the Root Server, TLD Server, and Authoritative Server.
- Most DNS lookups complete in less than 100 milliseconds.
- DNS can be targeted by several types of cyberattacks.

---

## Key Takeaways

✅ DNS converts domain names into IP addresses.

✅ Browser, OS, Router, and ISP caches make DNS lookups faster.

✅ The Authoritative Server stores the actual DNS records.

✅ DNS lookups usually complete in under 100 milliseconds.

✅ Common DNS attacks include:
- DNS Spoofing
- DNS Tunneling
- DNS Hijacking
- Typosquatting

---

## Reflection

Today's lesson helped me understand what happens before a website even begins to load. I learned that DNS is one of the most important services on the internet because it connects domain names with their IP addresses.

I also realized that while DNS makes browsing easier, it can also become a target for attackers. Understanding the DNS resolution process will help me better understand networking and cybersecurity concepts in the future.

---

## Quote of the Day

> "Every website begins with a DNS lookup. Understanding DNS is understanding the internet."

---

## Progress Tracker

- Day: 07/90
- Topic: DNS Resolution and DNS Attacks
- Concepts Learned: DNS, Browser Cache, OS Cache, Router Cache, Recursive Resolver, Root Server, TLD Server, Authoritative Server, DNS Attacks
- Key Insight: DNS caching makes browsing faster, while attackers can target DNS to redirect or manipulate traffic.
- Status: ✅ Completed
