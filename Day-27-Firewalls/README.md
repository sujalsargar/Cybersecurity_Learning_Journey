Day 27 - Firewalls
Objective

Understand what a firewall is, how it controls network traffic, learn the different types of firewalls, and explore how firewall rules are created and processed.

Lesson of the Day

Today, I learned about Firewalls, one of the fundamental security controls used to protect computers and networks.

A simple way to understand a firewall is:

A firewall is the doorkeeper of every network.

Just as a security guard checks who is allowed to enter or leave a building, a firewall checks network traffic and decides whether it should be allowed or blocked.

What is a Firewall?

A firewall is a security system that protects a computer or network from unauthorized access.

It monitors network traffic and applies predefined security rules.

Its primary responsibilities are to:

Inspect incoming traffic
Inspect outgoing traffic
Allow legitimate communication
Block unwanted or unauthorized traffic
How a Firewall Works

Whenever network traffic reaches a firewall, it compares the traffic against its configured rules.

The firewall then decides whether to:

Allow the traffic
Block the traffic

A simple flow looks like:

Incoming Traffic
        ↓
     Firewall
        ↓
 Check Security Rules
        ↓
Allow or Block
Types of Firewalls
1. Packet Filtering Firewall

This is the simplest type of firewall.

It examines individual packets based on information such as:

Source IP address
Destination IP address
Protocol
Port number

It makes decisions without understanding the full connection.

2. Stateful Firewall

A stateful firewall keeps track of active network connections.

Instead of inspecting every packet independently, it understands whether a packet belongs to an existing, legitimate connection.

This provides better security than simple packet filtering.

3. Proxy Firewall

A proxy firewall acts as an intermediary between the client and the destination server.

Instead of allowing direct communication, the firewall receives the request first and then communicates with the destination on behalf of the client.

This can provide additional inspection and isolation.

4. Next-Generation Firewall (NGFW)

A Next-Generation Firewall combines traditional firewall features with advanced security capabilities.

These may include:

Application awareness
Intrusion prevention
Deep packet inspection
Threat intelligence
User identity awareness

NGFWs are commonly used in modern enterprise environments.

Firewall Rule Processing

One of the most important lessons today was:

Firewall rules are processed from top to bottom.

The firewall checks each rule one by one.

As soon as a rule matches the traffic:

That rule is applied.
The firewall stops checking the remaining rules.

This means that rule order is extremely important.

Example Rule Set

Example firewall rules:

Rule 1: Allow HTTPS (Port 443)

Rule 2: Allow HTTP (Port 80)

Rule 3: Allow Office IP to SSH (Port 22)

Rule 4: Deny All

In this example:

Web traffic is allowed.
SSH access is restricted to trusted office IP addresses.
Everything else is denied.

The final "Deny All" rule blocks any traffic that does not match an earlier rule.

Allowlist vs Blocklist
1. Allowlist (Whitelist)

An allowlist permits only trusted traffic.

Everything else is blocked.

Example:

Trusted Traffic
        ↓
Allow

Everything Else
        ↓
Block

This approach is generally more secure because access is granted only to approved traffic.

2. Blocklist (Blacklist)

A blocklist blocks only known unwanted traffic.

Everything else is allowed.

Example:

Known Bad Traffic
        ↓
Block

Everything Else
        ↓
Allow

This approach is easier to manage but may allow unknown threats to pass.

Where Firewalls Are Used

Firewalls can be deployed in different locations depending on what needs protection.

1. Perimeter Firewall

Placed at the boundary between an organization's internal network and the internet.

It protects the entire network from external threats.

2. Internal Segmentation Firewall

Used inside an organization to separate different internal networks.

This helps limit the spread of attacks if one part of the network is compromised.

3. Host-Based Firewall

Installed directly on individual computers or servers.

It protects a single device by controlling its network traffic.

4. Windows Defender Firewall

A built-in host-based firewall included with Microsoft Windows.

It helps control inbound and outbound network connections on Windows devices.

5. Cloud Firewall

Protects cloud-hosted resources such as virtual machines, applications, and cloud services.

Examples include cloud security groups and network security rules.

6. Web Application Firewall (WAF)

A WAF protects web applications by filtering and monitoring HTTP/HTTPS traffic.

It helps defend against many web-based attacks, such as SQL Injection and Cross-Site Scripting (XSS).

What Firewalls Do NOT Do

Another important lesson today was understanding the limitations of firewalls.

A firewall alone cannot solve every security problem.

By default, a firewall does not:

Stop attacks hidden inside allowed traffic.
Stop all outbound attacks.
Inspect encrypted traffic unless specifically configured to do so.
Prevent social engineering attacks.
Prevent insider threats.

Firewalls are one layer of security, not a complete security solution.

What I Learned
A firewall controls incoming and outgoing network traffic.
Firewall rules determine whether traffic is allowed or blocked.
Rule order is important because processing stops after the first matching rule.
There are different types of firewalls designed for different purposes.
Allowlists and blocklists use different approaches to access control.
Firewalls can be deployed at the network perimeter, inside networks, on hosts, in cloud environments, and in front of web applications.
Firewalls have limitations and must be combined with other security controls.
Key Takeaways

✅ A firewall acts as the doorkeeper of a network.

✅ Firewall rules are processed from top to bottom.

✅ The first matching rule is applied.

✅ Rule order is critical.

✅ Common firewall types include:

Packet Filtering Firewall
Stateful Firewall
Proxy Firewall
Next-Generation Firewall

✅ Firewalls help control network access but cannot stop every type of cyberattack.

Reflection

Today's lesson helped me understand that firewalls are one of the first lines of defense in network security.

I learned that firewalls are not simply devices that block traffic—they make decisions based on configured rules. The order of those rules is extremely important because the first matching rule determines the outcome.

I also realized that although firewalls are essential, they are only one part of a layered security strategy. Other controls such as endpoint protection, authentication, user awareness, and monitoring are also necessary to defend against modern cyber threats.

My biggest takeaway is:

A firewall controls who can communicate with a system, but strong cybersecurity requires multiple layers of protection.

Quote of the Day

"A firewall is the gatekeeper of a network—but even the best gatekeeper cannot stop every threat."

Progress Tracker
Day: 27/90
Topic: Firewalls
Concepts Learned: Firewall Basics, Firewall Rules, Packet Filtering, Stateful Firewalls, Proxy Firewalls, Next-Generation Firewalls, Allowlists, Blocklists, Firewall Placement
Key Insight: Firewalls are essential for controlling network traffic, but they are only one layer in a comprehensive security strategy.
Status: ✅ Completed
