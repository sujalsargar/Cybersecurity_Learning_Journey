Day 72 - MITRE ATT&CK
Objective

Understand the MITRE ATT&CK framework, learn the difference between tactics and techniques, and understand how security teams use ATT&CK alongside the Cyber Kill Chain to analyze and defend against real-world attacks.

Lesson of the Day

Today, I learned about MITRE ATT&CK, a framework that documents the real-world techniques attackers use during cyberattacks.

MITRE ATT&CK is maintained by MITRE, a non-profit organization.

Unlike a purely theoretical model, ATT&CK is based on observed real-world attacker behavior.

A simple way to remember it is:

Tactic = What the attacker wants to achieve
Technique = How the attacker achieves it

What is MITRE ATT&CK?

MITRE ATT&CK is a knowledge framework that organizes information about attacker behavior.

It helps security professionals understand:

What attackers try to achieve.
What techniques they use.
How those techniques can be detected.
How security teams can improve their defenses.

ATT&CK provides standard names for attacker tactics and techniques, making it easier for cybersecurity teams to communicate.

Why MITRE ATT&CK Is Important

Cyberattacks can involve many different actions.

Instead of simply saying:

"An attacker compromised the system."

ATT&CK helps break the activity into specific behaviors.

For example:

Get Initial Access
       ↓
Execute Code
       ↓
Gain Higher Privileges
       ↓
Avoid Detection
       ↓
Steal Credentials
       ↓
Move to Other Systems

This gives defenders a much more detailed view of what an attacker is doing.

Tactics and Techniques

The two most important concepts are Tactics and Techniques.

Tactic

A tactic describes what the attacker is trying to achieve.

For example:

Persistence = Stay in the system.

Technique

A technique describes how the attacker attempts to achieve that goal.

Therefore:

Tactic
"What does the attacker want?"
          ↓
Technique
"How does the attacker do it?"

One tactic can have many different techniques.

One tactic → Many techniques

Common ATT&CK Tactics

Today's lesson introduced several important tactics.

1. Initial Access
Goal:

Get into the target system or environment.

Simple meaning:

Get in.

2. Execution
Goal:

Run commands or malicious code.

Simple meaning:

Run it.

3. Persistence
Goal:

Maintain access even after events such as a reboot or user login.

Simple meaning:

Stay in.

This connects with the cron persistence concept I learned on Day 62.

4. Privilege Escalation
Goal:

Gain higher-level permissions.

Simple meaning:

Get more power.

For example, an attacker who starts with limited access may attempt to obtain administrative privileges.

5. Defense Evasion
Goal:

Avoid detection or make malicious activity harder to identify.

Simple meaning:

Avoid being detected.

6. Credential Access
Goal:

Obtain passwords, credentials, or other authentication information.

Simple meaning:

Steal credentials.

7. Discovery
Goal:

Gather information about the environment.

An attacker may try to understand:

What systems exist?
What users exist?
What software is installed?
What resources are available?

Simple meaning:

Find out what is around you.

8. Lateral Movement
Goal:

Move from one compromised system to other systems.

Simple meaning:

Move to other systems.

This can allow an attacker to expand their access within an environment.

9. Collection
Goal:

Gather data that may be useful to the attacker.

Simple meaning:

Collect the target data.

Easy Way to Remember the Tactics

A simple attack-flow idea is:

Get In
  ↓
Run
  ↓
Stay
  ↓
Gain More Access
  ↓
Avoid Detection
  ↓
Steal Credentials
  ↓
Discover Environment
  ↓
Move Around
  ↓
Collect Data

The exact order of attacker behavior can vary, but this flow makes the concepts easier to remember.

How Defenders Use MITRE ATT&CK

MITRE ATT&CK is not only useful for understanding attackers.

Security teams can use it to improve their defenses.

1. Detection Coverage

Security teams can examine different attacker techniques and ask:

"Can we detect this technique?"

For example:

Technique
   ↓
Can our tools detect it?
   ↓
Yes / No

This helps organizations identify gaps in their security monitoring.

2. Common Language

ATT&CK provides standardized names and identifiers for attacker techniques.

This helps:

SOC analysts
Threat hunters
Incident responders
Security engineers
Red teams
Blue teams

communicate using a common language.

3. Threat Intelligence

ATT&CK connects real-world attacker groups and campaigns with the techniques they have been observed using.

This helps defenders understand:

Which techniques are associated with particular threats.
What behaviors they should monitor.
How they might improve their defenses.
4. Attack Emulation

Security teams can use ATT&CK to understand and emulate attacker behavior in authorized testing environments.

This is useful for:

Red teams
Blue teams
Security testing
Detection engineering

The goal is to test whether defensive controls can detect relevant attacker techniques.

MITRE ATT&CK vs Cyber Kill Chain

Today's lesson also compared MITRE ATT&CK with the Cyber Kill Chain from Day 71.

The important point is:

They are complementary, not replacements for each other.

They provide different levels of detail.

Cyber Kill Chain

The Cyber Kill Chain gives the big picture of an attack.

It helps answer:

Where is the attack?
What stage is occurring?
What stage may come next?
Where can the attack be stopped?

It focuses mainly on the overall attack flow and lifecycle.

Recon
 ↓
Weaponization
 ↓
Delivery
 ↓
Exploitation
 ↓
Installation
 ↓
C2
 ↓
Objective
MITRE ATT&CK

ATT&CK provides a much more detailed picture of attacker behavior.

It focuses on:

Specific tactics
Specific techniques
Real-world attacker behavior
Detection opportunities

So:

Kill Chain = Big Picture

ATT&CK = Detailed Picture

Using Both Together

The two frameworks can be used together.

Cyber Kill Chain
       ↓
Understand the overall attack lifecycle
       ↓
MITRE ATT&CK
       ↓
Identify specific attacker techniques
       ↓
Detection & Defense

For example:

The Kill Chain may tell us that an attacker has reached the Installation stage.

ATT&CK can then help us understand the specific technique being used to establish persistence.

This gives defenders both:

The overall context
The technical details
Why Using Both Is Useful

Using both frameworks helps security teams:

Analyze Real Attacks

Understand where an attack is in its lifecycle and what techniques are being used.

Make Better Decisions

Understand which security controls or detection rules may be useful.

Improve Defenses

Identify gaps in detection coverage.

Stop Attacks More Effectively

Find opportunities to interrupt attacker activity.

Simple Comparison
Feature	Cyber Kill Chain	MITRE ATT&CK
Main purpose	Understand attack lifecycle	Understand attacker behavior
View	Big picture	Detailed picture
Focus	Attack stages	Tactics and techniques
Helps answer	Where is the attack?	How is the attacker doing it?
Based on	Attack lifecycle model	Real-world observed behavior
Defensive use	Find stages to disrupt	Improve detection and coverage
Connection With Previous Learning

Today's lesson connects with several topics from my journey.

Day 18 - Cyber Kill Chain

The Kill Chain provides the overall attack lifecycle.

Day 36 - IDS/IPS

IDS and IPS can help detect or prevent certain attacker behaviors.

Day 37 - SIEM

SIEM can collect and correlate events that may indicate ATT&CK techniques.

Day 39 - Network Forensics

Forensic evidence can help identify attacker activity.

Day 62 - Cron

Cron can potentially be abused for persistence, which relates to the Persistence tactic.

Day 71 - Cyber Kill Chain

Today's lesson adds more technical detail to the attack lifecycle I learned yesterday.

What I Learned
MITRE ATT&CK is a framework for understanding real-world attacker behavior.
It is maintained by the non-profit organization MITRE.
ATT&CK focuses on tactics and techniques.
A tactic describes what the attacker wants to achieve.
A technique describes how the attacker achieves it.
One tactic can contain many techniques.
Common tactics include Initial Access, Execution, Persistence, Privilege Escalation, Defense Evasion, Credential Access, Discovery, Lateral Movement, and Collection.
Security teams use ATT&CK to improve detection coverage.
ATT&CK provides a common language for cybersecurity teams.
It can support threat intelligence and authorized attack emulation.
Cyber Kill Chain and ATT&CK are complementary.
Kill Chain provides the big picture.
ATT&CK provides the detailed picture.
Key Takeaways

✅ Tactic = What the attacker wants to achieve

✅ Technique = How the attacker achieves it

✅ ATT&CK is based on real-world attacker behavior.

✅ Security teams can use ATT&CK to identify detection gaps.

✅ ATT&CK provides a common language for security professionals.

✅ Kill Chain = Big Picture

✅ ATT&CK = Detailed Picture

✅ Using both helps defenders understand, detect, and disrupt attacks more effectively.

Reflection

Today's lesson helped me understand how cybersecurity professionals describe and analyze attacker behavior in a structured way.

The difference between tactics and techniques was the most important concept for me. A tactic tells me what the attacker wants to accomplish, while a technique explains how they attempt to accomplish it.

I also understood the difference between the Cyber Kill Chain and MITRE ATT&CK. The Kill Chain helps me see the overall attack lifecycle, while ATT&CK lets me look deeper into the specific behaviors and techniques being used.

Together, they provide a much clearer picture of an attack.

My biggest takeaway is:

The Kill Chain shows me where the attacker is in the journey; ATT&CK helps me understand exactly what they are doing.

Quote of the Day

"Understand the attack at a high level, then investigate the techniques behind it."

Progress Tracker
Day: 72/90
Topic: MITRE ATT&CK
Core Concepts: Tactics, Techniques, Detection Coverage, Threat Intelligence, Attack Emulation
Tactics Learned: Initial Access, Execution, Persistence, Privilege Escalation, Defense Evasion, Credential Access, Discovery, Lateral Movement, Collection
Framework Comparison: MITRE ATT&CK vs Cyber Kill Chain
Key Insight: Kill Chain provides the big picture, while ATT&CK provides detailed insight into attacker techniques.
Status: ✅ Completed
