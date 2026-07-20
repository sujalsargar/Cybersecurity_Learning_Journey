Day 31 - Wireshark Basics
Objective

Understand the fundamentals of Wireshark, learn its interface, use display filters to analyze network traffic, and gain hands-on experience inspecting captured packets.

Lesson of the Day

Today, I learned about Wireshark, one of the most widely used network protocol analyzers in cybersecurity and networking.

Wireshark allows users to capture and inspect network traffic in real time.

A simple way to describe it is:

Wireshark is a packet analyzer that captures actual network traffic flowing through your computer's network interface and displays it packet by packet.

Instead of only knowing that devices are communicating, Wireshark lets you see exactly what is happening on the network.

What is Wireshark?

Wireshark is a network packet analyzer.

It captures packets travelling through a network interface and presents detailed information about each packet.

Security professionals, network engineers, and incident responders use Wireshark to:

Troubleshoot network problems
Analyze network traffic
Investigate security incidents
Learn how network protocols work
Verify application communication
Wireshark Interface

One of the main things I learned today was how the Wireshark interface is organized.

It consists of three primary panes.

1. Packet List Pane

This is the top pane.

It displays every captured packet in chronological order.

Each packet includes information such as:

Packet number
Timestamp
Source IP
Destination IP
Protocol
Packet length
Summary (Info)

This pane provides a quick overview of all captured traffic.

2. Packet Details Pane

The middle pane (or bottom-left, depending on the layout) shows the detailed structure of the selected packet.

Here, I could expand different protocol layers to inspect information such as:

Ethernet
Internet Protocol (IP)
TCP or UDP
HTTP, HTTPS, DNS, and other protocols

This helped me understand how network protocols are layered.

3. Packet Bytes Pane

The bottom pane displays the raw packet data in hexadecimal and ASCII format.

This allows analysts to inspect the actual bytes transmitted across the network.

Display Filters

Wireshark provides display filters that make packet analysis much easier.

Instead of viewing every captured packet, filters allow us to focus on specific traffic.

1. Filter by Protocol

Examples:

tcp
udp
dns
http
https

These filters display packets belonging to a particular protocol.

2. Filter by IP Address

Example:

ip.addr == 192.168.1.10

This displays traffic associated with a specific IP address.

3. Filter by Port

Example:

tcp.port == 443

This displays traffic using a specific port.

4. Combined Filters

Multiple conditions can be combined to narrow down results.

For example, filters can combine protocol, IP address, and port information to isolate very specific traffic.

Packet Colors

Another useful feature I explored was packet coloring.

Wireshark automatically assigns colors to different types of traffic to make analysis easier.

For example:

Different protocols are shown in different colors.
Black or red packets often indicate errors, retransmissions, or other network issues that may require investigation.

These colors help analysts quickly identify unusual or problematic traffic.

Hands-on Practice

Today's session was primarily practical.

I used Wireshark to:

Capture live network traffic.
Apply different display filters.
Analyze packets from various protocols.
Explore protocol layers in the Packet Details pane.
Read information displayed in the Packet Bytes pane.
Observe packet colors and understand what they indicate.

This hands-on practice helped me become more comfortable navigating Wireshark and understanding captured network traffic.

What I Learned
Wireshark is a packet analyzer used to inspect network traffic.
The interface consists of the Packet List, Packet Details, and Packet Bytes panes.
Display filters help isolate specific network traffic.
Packets can be filtered by protocol, IP address, and port.
Packet colors provide quick visual indicators of different traffic types and potential network issues.
Practical packet analysis improves understanding of how network communication works.
Key Takeaways

✅ Wireshark captures and analyzes live network traffic.

✅ The three main panes each provide different levels of packet information.

✅ Display filters make packet analysis faster and more efficient.

✅ Packet colors help identify traffic patterns and possible errors.

✅ Hands-on packet analysis is an essential skill for networking and cybersecurity.

Reflection

Today's lesson gave me practical experience using one of the most important tools in networking and cybersecurity.

Instead of only learning networking concepts theoretically, I explored real network packets and understood how information is organized inside each packet.

Using display filters and examining different protocol layers helped me better understand how devices communicate over a network. I also became familiar with Wireshark's interface, making it easier to investigate network traffic in future security and troubleshooting tasks.

My biggest takeaway is:

Wireshark transforms invisible network communication into detailed information that can be analyzed, understood, and investigated.

Quote of the Day

"Every packet tells a story—Wireshark helps you read it."

Progress Tracker
Day: 31/90
Topic: Wireshark Basics
Concepts Learned: Packet Analysis, Display Filters, Protocol Layers, Packet Colors
Hands-on Activity: Captured live network traffic, applied filters, explored protocol layers, and analyzed packets using Wireshark.
Key Insight: Wireshark provides deep visibility into network communication and is an essential tool for network troubleshooting and security analysis.
Status: ✅ Completed
