Day 32 - Reading Network Packets
Objective

Learn how to read TCP packets in Wireshark, understand the lifecycle of a TCP connection, and analyze network traffic from connection establishment to connection termination.

Lesson of the Day

Today, I learned how to read and analyze network packets using Wireshark.

Instead of only capturing packets, I focused on understanding the complete lifecycle of a TCP connection—from the initial handshake, through data transfer, to the final connection teardown.

This practical exercise helped me understand how devices communicate over a network and how Wireshark can be used to observe every stage of that communication.

The TCP Connection Lifecycle

A TCP connection follows three main stages:

Connection Establishment
Data Transfer
Connection Termination

Understanding these stages makes it much easier to analyze packet captures during troubleshooting or security investigations.

Stage 1 - TCP Three-Way Handshake

Before any data is exchanged, TCP establishes a reliable connection using the Three-Way Handshake.

The handshake consists of three packets:

Client                    Server

SYN --------------------->

      <------------------- SYN-ACK

ACK --------------------->
SYN

The client sends a SYN (Synchronize) packet to request a connection.

SYN-ACK

The server replies with a SYN-ACK packet, acknowledging the request and indicating that it is ready to communicate.

ACK

The client responds with an ACK (Acknowledgement) packet.

At this point, the TCP connection is successfully established, and both the client and server are ready to exchange data.

Stage 2 - Data Transfer

Once the connection is established, both systems begin exchanging data.

During this stage:

Data packets are transmitted.
The receiving device acknowledges successful delivery.
TCP ensures that packets arrive in the correct order.
Lost packets can be retransmitted if necessary.

This reliability is one of TCP's biggest advantages.

HTTPS Traffic

While analyzing HTTPS traffic, I learned an important concept:

Although HTTPS encrypts the contents of the communication using TLS, some information is still visible in packet captures.

Examples include:

Packet size
Timing
Source and destination IP addresses
Direction of traffic

The actual application data remains encrypted and cannot be read without the appropriate decryption keys.

Stage 3 - Connection Termination

After communication is complete, the TCP connection is closed.

A normal connection shutdown uses a Four-Way Termination process.

Client                    Server

FIN --------------------->

      <------------------- ACK

      <------------------- FIN

ACK --------------------->

This graceful termination ensures that both sides have finished sending data before closing the connection.

Reset (RST) Packets

Not every connection ends normally.

Sometimes a RST (Reset) packet is sent.

A Reset packet immediately terminates the connection.

This may occur because:

The application closes unexpectedly.
A connection error occurs.
The destination is unavailable.
A firewall rejects the connection.
The connection is no longer valid.

RST packets are not always malicious, but they can indicate network or application issues that require investigation.

Hands-on Practice

Today's lesson was entirely practical.

Using Wireshark, I analyzed captured packets in detail.

I practiced:

Identifying the TCP Three-Way Handshake.
Observing data transfer between client and server.
Understanding acknowledgements (ACK).
Examining HTTPS packet flows.
Identifying normal connection termination using FIN and ACK packets.
Observing Reset (RST) packets.
Applying multiple display filters to inspect different types of traffic.

This exercise improved my ability to interpret real network traffic instead of simply viewing packet captures.

What I Learned
TCP communication follows a predictable lifecycle.
The Three-Way Handshake establishes reliable communication.
Data transfer includes acknowledgements to ensure reliability.
HTTPS encrypts the data but not all packet metadata.
TCP connections normally close using FIN and ACK packets.
RST packets terminate connections immediately and may indicate errors.
Wireshark makes it possible to analyze every stage of a network conversation.
Key Takeaways

✅ TCP begins with the Three-Way Handshake.

✅ Reliable communication depends on acknowledgements.

✅ HTTPS encrypts application data using TLS.

✅ Packet size, timing, and direction remain visible even when traffic is encrypted.

✅ Normal TCP sessions end with a FIN-ACK sequence.

✅ RST packets abruptly terminate a connection.

✅ Wireshark is a powerful tool for understanding network communication in depth.

Reflection

Today's lesson helped me move beyond simply capturing packets to actually understanding what those packets represent.

By analyzing the complete TCP connection lifecycle, I gained a better understanding of how reliable communication is established, maintained, and terminated.

Examining HTTPS traffic also showed me that while encryption protects the contents of communication, network metadata such as packet size and timing can still provide useful information during analysis.

My biggest takeaway is:

Every TCP packet has a purpose, and understanding its role helps reveal the complete story of a network connection.

Quote of the Day

"Reading packets is like reading a conversation—every message has a purpose."

Progress Tracker
Day: 32/90
Topic: Reading Network Packets
Concepts Learned: TCP Three-Way Handshake, Data Transfer, ACK, HTTPS/TLS, FIN, RST, Connection Teardown
Hands-on Activity: Analyzed TCP packet captures in Wireshark using multiple display filters and examined the complete lifecycle of network connections.
Key Insight: Understanding the sequence of TCP packets makes network troubleshooting and security analysis much more effective.
Status: ✅ Completed
