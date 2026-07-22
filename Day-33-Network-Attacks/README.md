Day 33 - Network Attacks
Objective

Understand common network-based attacks, how they work, why they are possible, and the importance of securing network communication.

Lesson of the Day

Today, I learned about Network Attacks—cyberattacks that target communication between devices rather than the devices themselves.

One of the most important lessons was understanding that many of the protocols that built the early internet were designed during a time when networks were much smaller and users were generally trusted.

As the internet evolved, attackers began exploiting weaknesses in these protocols, making network security an essential part of modern cybersecurity.

What are Network Attacks?

Network attacks are attempts to intercept, manipulate, disrupt, or monitor communication between devices.

Instead of attacking a computer directly, attackers target the data traveling across the network.

Their goals may include:

Stealing sensitive information
Redirecting users to malicious systems
Interrupting network services
Monitoring communications
Gaining unauthorized access
Why Do Network Attacks Happen?

Many internet protocols were originally created in an environment where devices were assumed to trust each other.

Today's internet is very different.

Modern networks require additional security controls because attackers actively attempt to exploit weaknesses in network communication.

Common Network Attacks
1. Man-in-the-Middle (MITM) Attack

A Man-in-the-Middle (MITM) attack occurs when an attacker secretly places themselves between two communicating parties.

Instead of communicating directly, both parties unknowingly send their data through the attacker.

User
   │
Attacker
   │
Website

The attacker may:

Read data
Modify data
Forward the communication without either side noticing

Using HTTPS and properly validating certificates helps reduce the risk of MITM attacks.

2. ARP Spoofing

ARP (Address Resolution Protocol) is used to map IP addresses to MAC addresses on a local network.

In an ARP Spoofing attack, the attacker sends fake ARP messages to convince devices that the attacker's MAC address belongs to another device, such as the router.

As a result, network traffic is redirected through the attacker.

This technique is commonly used to perform Man-in-the-Middle attacks on local networks.

3. DNS Spoofing

DNS translates domain names into IP addresses.

In a DNS Spoofing attack, false DNS information is provided so that users are redirected to a fake or malicious website instead of the legitimate one.

Victims may believe they are visiting the correct website while unknowingly interacting with an attacker's server.

4. Denial-of-Service (DoS) and Distributed Denial-of-Service (DDoS)

The objective of a DoS attack is to make a service unavailable by overwhelming it with excessive traffic or requests.

A DDoS attack works similarly but uses many compromised devices (often called a botnet) to generate traffic simultaneously.

Many Devices
      ↓
Target Server
      ↓
Service Becomes Unavailable

These attacks aim to disrupt availability rather than steal data.

5. Packet Sniffing

Packet sniffing involves capturing and analyzing network packets traveling across a network.

Packet sniffers are legitimate tools used by network administrators and security professionals for troubleshooting and analysis.

However, attackers can also misuse packet sniffing to capture sensitive information, especially on unsecured networks.

Using encrypted protocols such as HTTPS helps protect data from being read during transmission.

Protecting Against Network Attacks

Some common security measures include:

Using HTTPS and TLS encryption
Securing Wi-Fi networks
Keeping systems updated
Using firewalls
Monitoring network traffic
Using secure DNS services
Avoiding untrusted public networks when possible

No single control prevents every network attack, so a layered security approach is essential.

What I Learned
Network attacks target communication between devices.
Older network protocols were designed in a more trusted environment.
MITM attacks intercept communication between two parties.
ARP Spoofing manipulates MAC address mappings.
DNS Spoofing redirects users to malicious websites.
DoS and DDoS attacks target service availability.
Packet sniffing can be used for both legitimate analysis and malicious purposes.
Key Takeaways

✅ Network attacks focus on data in transit.

✅ MITM attacks intercept communication.

✅ ARP Spoofing targets local network communications.

✅ DNS Spoofing manipulates domain name resolution.

✅ DoS and DDoS attacks disrupt service availability.

✅ Packet sniffing can be both a valuable diagnostic tool and a potential attack technique.

Reflection

Today's lesson showed me that securing a network is just as important as securing individual computers.

I learned that attackers can target communication itself by intercepting, redirecting, or disrupting network traffic. Understanding attacks such as MITM, ARP Spoofing, DNS Spoofing, DoS/DDoS, and Packet Sniffing has given me a better appreciation of why encryption, secure network design, and continuous monitoring are so important.

My biggest takeaway is:

Protecting the devices is important, but protecting the communication between them is equally essential.

Quote of the Day

"A secure network is built on trusted communication, not trusted assumptions."

Progress Tracker
Day: 33/90
Topic: Network Attacks
Concepts Learned: Man-in-the-Middle (MITM), ARP Spoofing, DNS Spoofing, DoS, DDoS, Packet Sniffing
Key Insight: Many network attacks exploit weaknesses in communication protocols, making encryption and network security essential.
Status: ✅ Completed
