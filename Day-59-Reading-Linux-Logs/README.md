Day 59 - Reading Linux Logs
Objective

Learn how to read and analyze Linux logs, understand what happened on a system over time, and combine log information with process and network activity during a security investigation.

Lesson of the Day

Today, I learned about Reading Logs in Linux.

Logs are records of events that happen on a Linux system over time. Linux continuously writes important system and security events into log files.

For a cybersecurity analyst, logs are extremely valuable because they help answer:

What happened?
When did it happen?
Who did it?
How did it happen?

A simple way to remember today's lesson is:

Processes show what is happening, network shows who the system is talking to, and logs show how it got there.

The Three Views of a Live Linux System

Today's lesson connected the topics from the previous days into an investigation triad.

1. Process

What is the system doing?

Processes show what programs are currently running.

2. Network

Who is it talking to?

Network connections show what the system or its processes are communicating with.

3. Logs

How did it get there?

Logs provide a historical record of events that happened on the system.

Together:

        Linux Investigation
               │
       ┌───────┼───────┐
       ↓       ↓       ↓
    Process  Network  Logs
       ↓       ↓       ↓
   What's   Who is   What
   running? it talking happened?
             to?

These three views provide a much more complete picture of system activity.

What Are Linux Logs?

Logs are records of events stored by the operating system and applications.

They can contain information about:

User activity
Authentication
System events
Services
Applications
Network activity
Errors
Security events

Logs allow an investigator to look back and understand what happened over time.

Authentication Logs

One of the most important security-related logs is the authentication log.

Authentication logs can record events such as:

Successful logins
Failed login attempts
Logouts
sudo usage
Other authentication-related activity

These logs are particularly useful when investigating unauthorized access or suspicious account activity.

For example, repeated failed login attempts may indicate a possible brute-force attempt.

System Logs

System logs record general activity occurring on the Linux system.

They may include:

Service start events
Service stop events
System activity
Hardware-related messages
System errors

These logs help investigators understand what was happening on the machine around a particular time.

Reading Logs from the Terminal

Linux logs are often stored as text and can be examined using many of the same tools learned earlier.

tail

The tail command displays the latest entries in a log.

tail logfile

This is useful when you want to quickly see recent activity.

tail -f

The -f option continuously follows a log file.

tail -f logfile

New log entries appear as they are written.

This is useful for monitoring live system activity.

less

less allows you to read and navigate through large log files.

less logfile

This is useful when investigating historical events without loading the entire file into the terminal at once.

grep

grep searches logs for specific information.

grep "failed" logfile

It can be used to search for:

Keywords
Usernames
IP addresses
Dates
Error messages
Authentication events

This is important because analysts usually do not need to read an entire log file line by line.

Using Pipelines for Log Analysis

Pipes can combine multiple commands to extract useful information from logs.

For example:

Log
 ↓
grep
 ↓
sort
 ↓
uniq
 ↓
count / analyze

This can help with tasks such as:

Counting events
Finding unique IP addresses
Identifying frequently appearing IP addresses
Finding repeated login failures
Identifying common usernames

This is a good example of how the Linux command line can turn large amounts of raw log data into useful information.

journalctl

Another important tool introduced today is:

journalctl

journalctl is used to read and filter the system journal on systems using systemd.

It can help filter events by:

Time
Service
Boot
Priority

This makes it easier to focus on the specific events relevant to an investigation.

The Goal of Log Analysis

The goal is not to read every single line of every log.

The goal is:

Extract the relevant information that helps answer the investigation questions.

An analyst should start with a question and then search the logs for evidence.

For example:

Question: Were there failed login attempts?

↓

Search authentication-related logs.

↓

Filter for failed authentication events.

↓

Look at usernames, timestamps, and source IPs.

↓

Build a timeline.

This is much more efficient than reading thousands of log entries manually.

Finding the Story in the Logs

Logs can help reconstruct the story of a security incident.

Timestamps

Timestamps help establish when events occurred.

Events

Events show what happened.

Users

User information can help determine who was involved.

IP Addresses

IP addresses can help identify where network activity originated or went.

When these details are combined, an analyst can begin building a timeline of the incident.

The Investigation Triad

Today's lesson brought together several previous topics.

Process

What is running?

Network

What is it communicating with?

Logs

What happened over time?

Together:

Process
   +
Network
   +
Logs
   =
Complete Investigation Picture

This combination forms an important foundation for incident response and digital forensics.

What I Learned
Linux logs record system events over time.
Logs help answer what happened, when it happened, who did it, and how it happened.
Authentication logs are important for investigating login and access activity.
System logs record general system and service activity.
tail shows recent log entries.
tail -f monitors new entries in real time.
less is useful for reading large logs.
grep searches logs for specific information.
Pipes can be used to analyze and count events.
journalctl can read and filter the system journal.
Log analysis is about extracting relevant information rather than reading everything.
Processes, network activity, and logs together provide a more complete investigation picture.
Key Takeaways

✅ Logs provide historical evidence.

✅ Authentication logs are important for security investigations.

✅ Timestamps help build an accurate timeline.

✅ grep helps quickly find relevant events.

✅ journalctl provides powerful system-journal filtering.

✅ Log analysis should focus on relevant evidence.

✅ Process + Network + Logs = a stronger incident investigation.

Reflection

Today's lesson connected many of the Linux concepts I have learned recently.

Earlier, I learned how to investigate processes and network connections. Today, I learned how logs provide the historical context needed to understand what happened before and during an event.

The idea of the investigation triad was the biggest takeaway for me:

Process tells me what is running. Network tells me what it is talking to. Logs tell me what happened over time.

When these three sources are combined, an analyst can build a much clearer picture of a potential security incident.

I also learned that good log analysis is not about reading everything. It is about asking the right question, filtering the relevant data, and extracting the evidence needed to understand the story.

Quote of the Day

"Logs tell the story, timestamps build the timeline."

Progress Tracker
Day: 59/90
Topic: Reading Linux Logs
Commands Learned: tail, tail -f, less, grep, journalctl
Concepts Learned: Authentication Logs, System Logs, Log Analysis, Timelines, Investigation Triad
Investigation Triad: Process + Network + Logs
Key Insight: Combining current activity with historical logs provides a stronger picture of a security incident.
Status: ✅ Completed
