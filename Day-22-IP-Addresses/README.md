Day 22 - IP Addresses
Objective

Understand the role of IP addresses in networking, learn the structure of IPv4 and IPv6 addresses, explore Network Address Translation (NAT), and understand what information an IP address can and cannot reveal.

Lesson of the Day

Today, I learned that an IP address is one of the most important identifiers in networking.

Every device connected to a network needs an IP address so that data packets know where to be sent. Without IP addresses, devices would not be able to communicate with each other over a network or the internet.

What is an IP Address?

An IP (Internet Protocol) address is a unique identifier assigned to a device on a network.

Its main purpose is to help packets reach the correct destination.

Every network conversation depends on devices having valid IP addresses.

Structure of an IPv4 Address

An IPv4 address contains 32 bits and is written as four numbers separated by dots.

Example:

192.168.1.5

This address has two parts:

Network Part
192.168.1

This identifies the network.

Host Part
5

This identifies the individual device on that network.

A simplified view:

192.168.1 | 5
 Network   Host
IPv4 vs IPv6
IPv4
Uses 32-bit addresses.
Written as four decimal numbers.
Supports approximately 4.3 billion addresses.

Example:

192.168.1.5
IPv6

IPv6 was developed to solve the shortage of IPv4 addresses.

It:

Uses 128-bit addresses.
Supports approximately 340 undecillion addresses.
Is written as 8 groups of four hexadecimal digits separated by colons.

Example:

2001:0db8:85a3:0000:0000:8a2e:0370:7334

As of 2026, IPv6 adoption continues to grow, but both IPv4 and IPv6 are widely used together.

Most modern devices support both IPv4 and IPv6 (dual-stack networking).

Network Address Translation (NAT)

I also learned about NAT (Network Address Translation).

NAT allows communication between:

Private IP addresses
Public IP addresses

It translates:

Private IP → Public IP
Public IP → Private IP

This allows many devices inside a home or office network to share a single public IP address when accessing the internet.

Example:

Laptop
192.168.1.10
      ↓
Router (NAT)
      ↓
Public IP
103.x.x.x
      ↓
Internet
RFC 1918 - Private IPv4 Addresses

Today's lesson also introduced RFC 1918.

RFC stands for:

Request for Comments

RFCs are technical documents that define internet standards.

RFC 1918 defines the private IPv4 address ranges used inside local networks.

The three private ranges are:

10.0.0.0 – 10.255.255.255
172.16.0.0 – 172.31.255.255
192.168.0.0 – 192.168.255.255

These addresses are reused in private networks and are not directly routable on the public internet.

Public vs Private IP Addresses
Public IP Address

A public IP address:

Is unique on the internet.
Is assigned by an Internet Service Provider (ISP).
Allows communication with external networks.
Private IP Address

A private IP address:

Is used inside local networks.
Can be reused by many different networks.
Requires NAT to communicate with the public internet.
What Can a Public IP Reveal?

A public IP address may reveal general information such as:

Country
Region
Approximate city
Internet Service Provider (ISP)
Whether the connection appears to use a VPN, proxy, or Tor network

This information is approximate and may not always be accurate.

What an IP Address Cannot Reveal

An IP address alone does not reveal:

Your name
Your exact home address
Your personal identity
Everything you do online
Every website you visit

Additional information would be required for someone to determine those details.

What I Learned
Every device on a network needs an IP address.
IPv4 addresses use 32 bits.
IPv6 addresses use 128 bits.
IPv6 provides a much larger address space than IPv4.
IPv4 addresses contain a network part and a host part.
NAT translates between private and public IP addresses.
RFC 1918 defines the private IPv4 address ranges.
Public IP addresses are unique on the internet.
Private IP addresses are reused inside local networks.
A public IP can reveal approximate location and ISP, but not personal identity.
Key Takeaways

✅ Every network device needs an IP address.

✅ IPv4 uses 32-bit addresses.

✅ IPv6 uses 128-bit addresses.

✅ NAT enables communication between private and public networks.

✅ RFC 1918 defines the private IPv4 address ranges.

✅ Public IP addresses are unique on the internet.

✅ Private IP addresses are reused within local networks.

✅ An IP address can reveal approximate location and ISP but not your exact identity or browsing activity.

Reflection

Today's lesson helped me understand why IP addresses are one of the most important parts of networking.

I learned that every device needs an IP address so data can reach the correct destination, and that an IP address contains both a network part and a host part.

I also understood why IPv6 was introduced, how NAT allows multiple devices to share one public IP address, and what information a public IP address can realistically reveal.

My biggest takeaway is:

An IP address is the foundation of network communication because it tells data where it needs to go.

Quote of the Day

"Every packet has a destination, and every destination needs an IP address."

Progress Tracker
Day: 22/90
Topic: IP Addresses
Concepts Learned: IPv4, IPv6, Network Part, Host Part, NAT, RFC 1918, Public IP, Private IP
Key Insight: IP addresses identify devices on a network, while NAT enables communication between private and public networks.
Status: ✅ Completed
