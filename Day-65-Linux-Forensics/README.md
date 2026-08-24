Day 65 - Linux Forensics
Objective

Learn how to systematically investigate a potentially compromised Linux system, connect evidence from different sources, build a timeline, and report findings based only on evidence.

Lesson of the Day

Today, I learned about Linux Forensics.

Linux forensics is the process of investigating a Linux system to understand what happened, when it happened, and how it happened.

The goal is not to guess what happened. The goal is to collect evidence, connect related findings, build a timeline, and reach conclusions supported by that evidence.

A simple way to remember today's lesson is:

Collect the evidence → Connect the evidence → Build the timeline → Tell the story.

Investigating a Suspected Compromised Linux System

Today's lesson introduced a systematic investigation process.

The six main areas to check are:

Processes
Network connections
Logs
User accounts
Scheduled tasks
Files
1. Check Processes

First, investigate what is currently running on the system.

Questions to ask:

What processes are running?
Are there any unknown processes?
Which users own them?
Are any processes using unusual amounts of resources?
Are processes running with elevated privileges?
What started the process?

Useful commands learned earlier include:

ps aux

and:

top

The goal is to identify anything that requires further investigation.

2. Check Network Connections

Next, investigate what the system is communicating with.

Questions to ask:

What connections are currently established?
What ports are listening?
Which remote systems are being contacted?
Is any process communicating with an unexpected destination?

Useful tools include:

ss

and:

netstat

This step connects process investigation with network investigation.

For example:

Suspicious Process
       ↓
Network Connection
       ↓
Unexpected Remote System

This provides stronger evidence than looking at either the process or network connection alone.

3. Check Logs

Logs provide historical information about what happened on the system.

They can help answer:

When did the activity happen?
Which user was involved?
Were there failed login attempts?
Were services started or stopped?
What other system events occurred?

Useful tools include:

tail
less
grep

and:

journalctl

Logs are particularly useful for building the timeline.

4. Check User Accounts

User accounts should also be investigated.

Questions to ask:

Which users exist on the system?
Are there unexpected accounts?
Which users have administrative privileges?
Were accounts recently created or modified?
Was suspicious activity associated with a particular account?

Understanding user activity can help determine who may have performed an action.

5. Check Scheduled Tasks

Scheduled tasks can automatically execute commands or scripts.

This makes them useful for legitimate automation, but they can also be abused for persistence.

During an investigation, check:

What scheduled tasks exist?
What commands do they execute?
Who owns them?
Are any tasks unexpected?
Do they execute suspicious scripts?

This connects directly with the cron and persistence lesson from Day 62.

6. Check Files

Finally, investigate relevant files on the system.

Look for:

Recently modified files
Suspicious scripts
Unexpected executables
Unusual files in temporary locations
Files associated with suspicious processes
Configuration changes

Useful commands learned earlier include:

find
ls -l
file

and:

grep

The goal is to identify files that help explain what happened.

Building the Timeline

One of the most important parts of Linux forensics is creating a timeline.

A timeline arranges evidence according to timestamps.

For example:

10:05 - User login
   ↓
10:08 - Suspicious process starts
   ↓
10:09 - Network connection established
   ↓
10:12 - Suspicious file created
   ↓
10:15 - Scheduled task modified

This helps investigators understand the sequence of events.

Connecting the Evidence

Individual pieces of evidence become much more useful when they are connected.

Today's lesson introduced this investigation chain:

Process
   ↓
Network Connection
   ↓
Logs
   ↓
Files
   ↓
User Account
   ↓
Scheduled Task

For example:

A suspicious process may connect to an unusual external system.

↓

Logs show when the process or user activity occurred.

↓

A suspicious file was created around the same time.

↓

A scheduled task shows that the file may be executed automatically.

↓

A particular user account is associated with the activity.

Together, these findings can help build a much stronger explanation of what happened.

Finding the Story

The purpose of forensic investigation is to reconstruct the story of the incident.

The key questions are:

What happened?

Identify the observed activity.

When did it happen?

Use timestamps to establish the timeline.

How did it happen?

Connect processes, network activity, logs, files, users, and scheduled tasks.

The investigator should follow the evidence step by step rather than jumping to conclusions.

Investigation Tips

Today's lesson provided several important investigation principles.

Follow the Evidence

Do not start with an assumption and try to make the evidence fit it.

Instead:

Follow the evidence wherever it leads.

Link Related Findings

A single suspicious event may not mean much by itself.

Multiple related findings can provide stronger evidence.

Focus on What, When, and How

Always try to establish:

What happened?
When did it happen?
How did it happen?
Reporting Findings

A forensic investigation is only useful if the findings are clearly documented.

The report should:

State what the evidence proves.
Explain the relevant timeline.
Connect related findings.
Mention the confidence level.
Clearly state what could not be determined.
Avoid unsupported conclusions.
Evidence vs Assumptions

This was one of the most important lessons today.

An analyst should distinguish between:

Evidence

Something directly supported by available information.

Assumption

Something that may be possible but has not been proven.

For example:

❌ Unsupported conclusion:

"The attacker definitely used this account."

✅ Evidence-based statement:

"The account was associated with the observed activity during the relevant time period."

The second statement is more professional because it does not claim more than the evidence supports.

Confidence Levels

Investigators should also communicate how confident they are in their conclusions.

For example:

High confidence: Strong evidence directly supports the conclusion.
Medium confidence: Several pieces of evidence support the conclusion, but some uncertainty remains.
Low confidence: There are indications, but insufficient evidence to confirm the conclusion.

Being honest about uncertainty is an important part of professional forensic reporting.

What I Learned
Linux forensics involves systematically investigating a potentially compromised system.
Processes show what is running.
Network connections show what the system is communicating with.
Logs provide historical evidence.
User accounts help identify who may be associated with activity.
Scheduled tasks can reveal automation or persistence.
Files can provide additional evidence about what happened.
A timeline arranges evidence according to timestamps.
Connecting different evidence sources helps reconstruct an incident.
Reports should contain only conclusions supported by evidence.
Investigators should communicate confidence levels.
Anything that cannot be determined should be clearly stated.
Assumptions and unsupported conclusions should be avoided.
Key Takeaways

✅ Investigate systematically.

✅ Check processes, network, logs, users, scheduled tasks, and files.

✅ Build a timeline using timestamps.

✅ Connect related evidence.

✅ Focus on what happened, when, and how.

✅ Report only what the evidence supports.

✅ Be honest about uncertainty.

✅ Never replace evidence with assumptions.

Reflection

Today's lesson helped me understand how the individual Linux skills I have learned can be combined into a real forensic investigation.

Previously, I learned how to inspect processes, network connections, logs, files, permissions, users, and scheduled tasks separately. Today, I learned how to connect all of those pieces to reconstruct what may have happened during a security incident.

The biggest lesson for me was that forensics is about building a story from evidence.

An analyst should not immediately decide who the attacker was or exactly what happened. Instead, they should follow the evidence, connect related events, build a timeline, and clearly explain what can and cannot be proven.

My biggest takeaway is:

Don't tell the story you think happened. Tell the story the evidence proves.

Quote of the Day

"Follow the evidence, build the timeline, and report only what you can prove."

Progress Tracker
Day: 65/90
Topic: Linux Forensics
Investigation Areas: Processes, Network, Logs, Users, Scheduled Tasks, Files
Core Skill: Timeline Building and Evidence Correlation
Reporting Focus: Evidence, Confidence Levels, Uncertainty
Key Insight: A strong forensic investigation connects multiple evidence sources to reconstruct what happened.
Status: ✅ Completed
