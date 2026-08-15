Day 58 - Network from the Terminal
Objective

Learn how to inspect network activity directly from the Linux terminal, understand active connections and listening ports, and connect process investigation with network investigation.

Lesson of the Day

Today, I learned how Linux allows us to see network activity directly from the terminal.

In cybersecurity, it is not enough to know what is running on a system. We also need to understand what those processes are communicating with.

A simple way to remember today's lesson is:

What's running? What is it talking to?

Linux provides several command-line tools that help answer these questions.

What is Running?

Before investigating network activity, we need to understand which processes are currently running.

The ps command can be used to examine running processes.

ps aux

This helps identify:

Running processes
Process IDs (PIDs)
Process owners
CPU and memory usage
Commands being executed

This connects directly with what I learned on Day 57.

What Is It Talking To?

After identifying a process, the next question is:

What network connections is it making?

Linux provides commands such as:

ss
netstat

to investigate network connections.

ss - Socket Statistics

ss stands for Socket Statistics.

It is a modern Linux command used to view network connections and sockets.

Example:

ss

It can help identify:

Active connections
Listening ports
Network endpoints
Connection states

It is an important command for network investigation from the terminal.

netstat

netstat is an older command that provides similar network information.

It can be used to examine:

1. Established Connections

These show active network connections between systems.

2. Listening Ports

These show services that are waiting for incoming network connections.

Although ss is the more modern tool, netstat is still useful to understand because it appears in older systems, documentation, and troubleshooting workflows.

Testing Network Connectivity

Two other useful commands introduced today are:

ping
dig
ping

The ping command checks whether another system is reachable over the network.

Example:

ping google.com

It can help determine whether network communication is possible and measure response time.

It is a simple but useful troubleshooting tool.

dig

The dig command is used to perform DNS lookups.

Example:

dig google.com

It provides DNS information about a domain.

This is useful for understanding how a domain resolves and for troubleshooting DNS-related problems.

Spotting a Process "Phoning Home"

One of the cybersecurity concepts introduced today was phoning home.

Phoning home means that a suspicious or malicious process communicates with an external server, potentially an attacker's Command and Control (C2) server.

The important investigation question becomes:

Which process is communicating, and where is it communicating?

This requires combining process information with network information.

Combining Process and Network Investigation

This is one of the most important lessons from today.

Instead of looking at processes and network connections separately, combine the information.

Process Investigation

Using:

ps aux

helps answer:

What's running?

Network Investigation

Using:

ss

helps answer:

What is it talking to?

Together:

Process Investigation
        ↓
What's running?
        ↓
Network Investigation
        ↓
What is it talking to?
        ↓
Investigate suspicious communication

This provides a much clearer picture of system activity.

Three Views of System Activity

Today's lesson introduced three important perspectives.

1. Process

A process shows:

What is running on the system?

2. Network

Network connections show:

What is the process communicating with?

3. Logs

Logs show:

What happened over time?

These three views complement each other.

Process
   ↓
What is running?


Network
   ↓
What is it communicating with?


Logs
   ↓
What happened over time?

Together, they provide a stronger foundation for investigating suspicious activity.

What I Learned
Linux provides several network investigation tools from the terminal.
ss is the modern tool for viewing network connections and sockets.
netstat is an older tool with similar functionality.
Established connections show active communication.
Listening ports show services waiting for connections.
ping checks network reachability.
dig performs DNS lookups.
"Phoning home" can describe suspicious communication with an external C2 server.
Process investigation and network investigation become more powerful when combined.
Processes, network connections, and logs provide three different views of system activity.
Key Takeaways

✅ First ask what is running.

✅ Then ask what it is communicating with.

✅ Use ps to investigate processes.

✅ Use ss to investigate network connections.

✅ Use ping to test connectivity.

✅ Use dig to investigate DNS information.

✅ Combine process, network, and log information when investigating suspicious activity.

Reflection

Today's lesson helped me connect two areas that I had previously learned separately: process investigation and network investigation.

Knowing that a process is running is useful, but it becomes much more meaningful when I can also determine what that process is communicating with.

The concept of a process "phoning home" was especially important because suspicious outbound communication can provide valuable clues during an investigation.

I also learned that a strong investigation should look at multiple sources of evidence:

Processes show what is running, network connections show what it is communicating with, and logs show what happened over time.

This gives an analyst a much more complete picture of system activity.

Quote of the Day

"Don't just ask what is running. Ask what it is talking to."

Progress Tracker
Day: 58/90
Topic: Network from the Terminal
Commands Learned: ss, netstat, ping, dig, ps
Concepts Learned: Network Connections, Listening Ports, DNS Lookup, Connectivity Testing, C2 Communication
Investigation Focus: Combining process and network investigation
Key Insight: Processes, network connections, and logs provide three complementary views of system activity.
Status: ✅ Completed
