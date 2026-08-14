Day 57 - Processes in Linux
Objective

Learn what Linux processes are, how to view running processes, and how cybersecurity analysts can identify potentially suspicious processes running on a system.

Lesson of the Day

Today, I learned about Processes in Linux.

A process is a program that is currently running.

A computer can run many processes at the same time, while the operating system manages those processes and the resources they use.

From a cybersecurity perspective, processes are important because malicious activity has to execute through a running process to actively perform actions on a system.

A useful way to remember this is:

A file shows what could happen, while a process shows what is happening now.

What Information Does a Process Have?

Every running process has important information associated with it.

A process has:

A unique Process ID (PID)
An owner
CPU usage
Memory usage
A parent process that started it

This information helps an analyst understand what is running and who or what started it.

Viewing Processes

The main commands I learned today are:

ps
top
htop

These commands allow us to inspect and monitor running processes.

1. ps

The ps command provides information about running processes.

A particularly useful command is:

ps aux

It provides a snapshot of processes running on the system.

It can show information such as:

Process owner
PID
CPU usage
Memory usage
Command being executed

Example:

ps aux

This is useful when an analyst wants to examine the processes currently running on a system.

2. top

top provides a live, continuously updating view of running processes.

Example:

top

It is useful for monitoring system activity in real time.

Processes using significant amounts of CPU or memory are easy to notice.

This can help an analyst identify:

Resource-heavy processes
Unexpected activity
Potentially suspicious processes
3. htop

htop is a more user-friendly alternative to top.

It provides an interactive view of running processes and makes it easier to monitor system activity.

It can be useful when visually examining processes and resource usage.

ps vs top / htop
Command	Purpose
ps aux	Snapshot of running processes
top	Live monitoring of processes
htop	User-friendly live process monitoring

A simple way to remember:

Use ps to investigate. Use top or htop to monitor.

Identifying a Suspicious Process

Not every unusual process is malicious.

An analyst should investigate processes that show potentially concerning characteristics.

Some things to look for include:

High CPU Usage

A process using an unusually high amount of CPU may deserve investigation.

High Memory Usage

Unexpectedly high memory consumption can also be a useful indicator.

Unknown or Strange Names

A process with an unfamiliar or unusual name should be investigated rather than immediately classified as malicious.

Running as Root

A suspicious process running with root privileges can be particularly concerning because it may have significant access to the system.

Unusual Locations

Processes running from unexpected locations, such as /tmp, may require additional investigation.

The important point is:

An indicator is a reason to investigate, not automatic proof of malicious activity.

Spotting and Stopping

Today's lesson introduced two important concepts:

1. Spotting

Finding and identifying a process that appears suspicious.

A useful starting point is:

ps aux

Then examine the process information, including its:

PID
Owner
CPU usage
Memory usage
Command
Location
2. Stopping

If a process is confirmed to be malicious, it may need to be terminated.

The kill command can be used with the process ID.

Example:

kill <PID>

The PID identifies the specific process that should be terminated.

In a real security investigation, termination should be performed according to the appropriate incident-response procedure because stopping a process can also destroy useful evidence or affect the system.

Investigation Mindset

When investigating a suspicious process, don't immediately ask:

"Is this malware?"

Start with questions such as:

What is the process?
Who owns it?
What is its PID?
What command started it?
What is its parent process?
How much CPU and memory is it using?
Where is it running from?
Is the behaviour expected on this system?

This helps build an evidence-based understanding of the process.

What I Learned
A process is a program that is currently running.
Operating systems manage many processes simultaneously.
Every process has a unique PID.
Processes have owners and parent processes.
Processes consume CPU and memory.
ps aux provides a snapshot of running processes.
top provides live process monitoring.
htop provides a more user-friendly process view.
High resource usage can be an indicator worth investigating.
Unknown names, root privileges, and unusual locations can also require investigation.
A confirmed malicious process can be terminated using its PID.
Key Takeaways

✅ A file represents something that could run, while a process represents something running now.

✅ Process monitoring is an important cybersecurity skill.

✅ ps aux is useful for examining processes.

✅ top and htop are useful for live monitoring.

✅ High CPU or memory usage does not automatically mean malware.

✅ A suspicious process should be investigated using multiple pieces of evidence.

✅ Don't confuse an indicator with proof.

Reflection

Today's lesson helped me understand why processes are important in cybersecurity.

A suspicious file sitting on a system may not currently be doing anything. A running process, however, represents active activity happening on the machine.

Learning to examine processes using ps, top, and htop gives me a basic way to understand what is happening on a Linux system in real time.

The most important lesson for me was that identifying something unusual is only the beginning. I need to investigate the process, understand its owner, parent process, resource usage, command, and location before reaching a conclusion.

My biggest takeaway is:

Don't just look at what is on the system. Look at what is actually running.

Quote of the Day

"A file shows what could happen. A process shows what is happening now."

Progress Tracker
Day: 57/90
Topic: Processes in Linux
Commands Learned: ps aux, top, htop, kill
Concepts: PID, Process Owner, Parent Process, CPU Usage, Memory Usage
Investigation Focus: Identifying and investigating suspicious processes
Key Insight: Running processes provide visibility into what is actively happening on a system.
Status: ✅ Completed
