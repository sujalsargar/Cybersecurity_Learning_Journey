Day 28 - Network Address Translation (NAT)
Objective

Understand how Network Address Translation (NAT) works, learn the role of Port Address Translation (PAT), and explore how NAT allows multiple devices to share a single public IP address.

Lesson of the Day

Today, I learned about Network Address Translation (NAT).

NAT is a networking technique that allows devices using private IP addresses to communicate with the internet through a public IP address.

A home or office network may contain many devices, but they can all access the internet using one public IP address.

What is NAT?

Network Address Translation (NAT) translates private IP addresses into public IP addresses and translates incoming responses back to the correct private device.

Without NAT, every device would require its own public IP address.

How NAT Works

Whenever a device starts an outbound connection, the router creates a temporary entry in its NAT table.

The router records:

The private source IP address
The private source port
The destination IP address
The destination port
A new source port chosen by the router

This information allows the router to correctly return incoming responses to the device that originally started the connection.

Example of NAT
Laptop
192.168.1.10
        ↓
Router (NAT)
        ↓
Public IP
203.x.x.x
        ↓
Website

When the website sends data back, the router checks its NAT table and forwards the response to the correct device.

NAT Table

A simplified NAT table might look like this:

Private IP	Private Port	Public Port	Destination
192.168.1.10	50432	62001	Website A
192.168.1.15	50433	62002	Website B

Each active connection has its own entry.

When the connection ends, the entry is eventually removed.

Port Address Translation (PAT)

I also learned about Port Address Translation (PAT).

PAT is a type of NAT that allows multiple devices to share a single public IP address by assigning a unique public source port to every connection.

For example:

Laptop 1
192.168.1.10
        ↓
Public IP:203.x.x.x:62001

Laptop 2
192.168.1.11
        ↓
Public IP:203.x.x.x:62002

Although both devices use the same public IP address, the different port numbers allow the router to distinguish between their connections.

Why PAT Is Important

PAT makes efficient use of public IPv4 addresses.

Instead of assigning one public IP address to every device, many devices can safely share a single public IP.

This is one of the reasons NAT became widely used during the IPv4 address shortage.

NAT Security Benefit

One important security benefit I learned is:

NAT blocks unsolicited incoming connections by default because there is no matching NAT table entry.

If an external system tries to initiate a connection without an existing NAT entry, the router usually drops the traffic.

Example:

Internet
      ↓
Unsolicited Connection
      ↓
Router Checks NAT Table
      ↓
No Matching Entry
      ↓
Connection Blocked

This provides a basic layer of protection against unexpected inbound traffic.

Important Note

Although NAT offers some security benefits, it is not a firewall.

NAT's primary purpose is address translation.

Dedicated firewalls still provide additional security features such as:

Rule-based filtering
Traffic inspection
Access control
Threat detection
What I Learned
NAT translates private IP addresses into public IP addresses.
Routers create NAT table entries for outbound connections.
NAT records source and destination IP addresses and ports.
PAT allows many devices to share one public IP address by using different port numbers.
NAT blocks unsolicited inbound connections when no matching NAT table entry exists.
NAT improves IPv4 address usage but is not a replacement for a firewall.
Key Takeaways

✅ NAT translates between private and public IP addresses.

✅ Routers maintain a NAT table for active connections.

✅ PAT uses different port numbers so multiple devices can share one public IP.

✅ NAT helps conserve public IPv4 addresses.

✅ Unsolicited inbound connections are usually blocked because no NAT table entry exists.

✅ NAT provides a security benefit, but it should not be considered a complete security solution.

Reflection

Today's lesson helped me understand what happens behind the scenes when devices in my home network connect to the internet.

I learned that every outbound connection creates a temporary NAT table entry, allowing responses to return to the correct device.

I also understood how PAT makes it possible for multiple devices to share a single public IP address while keeping each connection separate using different port numbers.

My biggest takeaway is:

NAT makes modern home and office networking possible by translating private addresses into public ones while efficiently managing internet communication.

Quote of the Day

"One public IP can serve many devices because NAT keeps track of every connection."

Progress Tracker
Day: 28/90
Topic: Network Address Translation (NAT)
Concepts Learned: NAT, PAT, NAT Table, Public IP, Private IP, Port Translation
Key Insight: NAT enables multiple devices to share a single public IP address while tracking each connection through translation tables.
Status: ✅ Completed
