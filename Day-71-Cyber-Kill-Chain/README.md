Day 71 - Cyber Kill Chain
Objective

Understand how a cyberattack happens in multiple stages, learn the 7 stages of the Cyber Kill Chain, and understand how defenders can detect and stop an attack at different stages.

Lesson of the Day

Today, I learned that a cyberattack is not a single event.

It is usually a sequence of different stages called the Cyber Kill Chain.

A simple way to remember it is:

An attacker must complete the chain, but a defender only needs to break it at one stage.

What is the Cyber Kill Chain?

The Cyber Kill Chain is a model that describes the common stages of a cyberattack.

Instead of thinking:

"The attacker attacked the system."

We can break the attack into different stages:

Research
   ↓
Prepare
   ↓
Deliver
   ↓
Exploit
   ↓
Install
   ↓
Control
   ↓
Achieve Goal

This helps defenders understand where an attack is happening and where it can be stopped.

The 7 Stages of the Cyber Kill Chain
1. Reconnaissance

The attacker researches the target.

They may try to understand:

What systems exist?
What services are exposed?
What technologies are being used?
Who are the potential targets?

Simple meaning:

Reconnaissance = Find out about the target.

Target
  ↓
Information Gathering
2. Weaponization

The attacker prepares the tools or malicious components needed for the attack.

Simple meaning:

Weaponization = Prepare the attack.

Information
    ↓
Attack Tools / Malicious Payload
3. Delivery

The attacker attempts to deliver the attack to the target.

The delivery method can vary depending on the attack.

Simple meaning:

Delivery = Get the attack to the target.

Attacker
   ↓
Attack / Payload
   ↓
Target
4. Exploitation

The attacker attempts to exploit a vulnerability or weakness.

Simple meaning:

Exploitation = Use a weakness to gain access.

Vulnerability
      ↓
   Exploit
      ↓
Possible Access

This is an important stage for defenders because patching vulnerabilities and applying security controls can prevent exploitation.

5. Installation

After gaining access, the attacker may attempt to establish a foothold or maintain access to the compromised system.

Simple meaning:

Installation = Establish a foothold.

The attacker wants their access to remain available rather than disappearing immediately.

6. Command and Control

The compromised system may communicate with infrastructure controlled by the attacker.

This allows the attacker to potentially send instructions and receive information.

Simple meaning:

Command and Control = Maintain communication with the compromised system.

Compromised System
       ↕
Attacker-controlled Infrastructure

This stage can be important for defenders because unusual network communication may provide a detection opportunity.

7. Actions on Objectives

The final stage is where the attacker attempts to achieve their goal.

Depending on the attack, the objective could involve:

Stealing information
Disrupting services
Modifying data
Causing damage
Other unauthorized actions

Simple meaning:

Actions on Objectives = Achieve the attacker's goal.

The Complete Kill Chain

The seven stages can be remembered as:

1. Reconnaissance
        ↓
2. Weaponization
        ↓
3. Delivery
        ↓
4. Exploitation
        ↓
5. Installation
        ↓
6. Command & Control
        ↓
7. Actions on Objectives
Easy Memory Flow

Research → Prepare → Deliver → Exploit → Install → Control → Goal

Breaking the Kill Chain

This was one of the most important lessons today.

A cyberattack is a chain of stages.

If a defender successfully stops one important stage, the attacker may not be able to continue to the next stages.

Recon
  ↓
Weaponization
  ↓
Delivery
  ❌ STOP
  ↓
Exploitation
  ↓
Installation
  ↓
C2
  ↓
Objective

The attacker needs to successfully progress through the chain.

The defender does not need to stop every stage.

Break one important link and the attack can fail.

Attacker vs Defender

A simple way to understand the difference:

Attacker

The attacker needs to successfully progress through the necessary stages.

Stage 1 → Stage 2 → Stage 3 → Stage 4 → ...
Defender

The defender can potentially stop the attack at any stage.

Stage 1 ❌
       OR
Stage 2 ❌
       OR
Stage 3 ❌
       OR
Stage 4 ❌
       ...

This gives defenders multiple opportunities to interrupt an attack.

Earlier is Better

Another important lesson was:

Stopping an attack earlier is usually better.

Why?

Early detection can:

Reduce potential damage.
Prevent access from being established.
Reduce investigation complexity.
Reduce the attacker's opportunity to move further into the environment.

For example:

Reconnaissance
     ↓
Early Detection ✅
     ↓
Attack stopped

is generally better than:

Reconnaissance
     ↓
Delivery
     ↓
Exploitation
     ↓
Installation
     ↓
Command & Control
     ↓
Damage
     ↓
Detection ❌

The later an attack is detected, the more opportunity the attacker may have had to cause harm.

Defense in Depth

The Cyber Kill Chain also connects directly with Defense in Depth.

Defense in depth means using multiple layers of security.

Firewall
   ↓
Email Security
   ↓
Endpoint Security
   ↓
Authentication
   ↓
Network Monitoring
   ↓
SIEM
   ↓
Incident Response

If one security control fails, another may detect or stop the attack.

For example:

Defense 1 ❌
     ↓
Defense 2 ❌
     ↓
Defense 3 ✅
     ↓
Attack stopped

This provides multiple opportunities to break the kill chain.

Kill Chain and Detection

The Cyber Kill Chain helps security teams understand where to look for suspicious activity.

For example:

Reconnaissance

Look for unusual information-gathering activity.

Delivery

Look for suspicious emails, files, or other delivery methods.

Exploitation

Look for unusual exploitation attempts or vulnerability-related activity.

Installation

Look for unexpected processes, files, or persistence mechanisms.

Command and Control

Look for unusual network connections.

Actions on Objectives

Look for suspicious data access, modification, or other unauthorized activity.

Kill Chain and Security Operations

The Cyber Kill Chain supports three important cybersecurity activities:

1. Detection

Security teams monitor activity to identify signs of an attack.

Monitor
  ↓
Detect Suspicious Activity
2. Analysis

Analysts investigate the activity and determine which stage of the attack may be occurring.

Alert
  ↓
Investigation
  ↓
Identify Attack Stage
3. Response

Once an attack is identified, defenders can take action to contain or stop it.

Detection
    ↓
Analysis
    ↓
Response
    ↓
Attack Disrupted
Connection With Previous Learning

Today's lesson connected strongly with several previous topics from my 90-day journey.

Day 18 - Cyber Kill Chain

I previously learned the basic Cyber Kill Chain. Today's lesson reinforced how defenders can use it to understand and interrupt attacks.

Day 36 - IDS/IPS

IDS and IPS can help detect or block suspicious network activity.

Day 37 - SIEM

SIEM can collect and correlate security events to help identify attack activity.

Day 39 - Network Forensics

Forensic investigation can help reconstruct the stages of an attack after an incident.

Day 64 - Defense in Depth

Multiple security layers create multiple opportunities to stop an attack.

What I Learned
A cyberattack is a sequence of stages, not just one event.
The Cyber Kill Chain contains seven stages.
The seven stages are:
Reconnaissance
Weaponization
Delivery
Exploitation
Installation
Command and Control
Actions on Objectives
Attackers need to progress through the necessary stages.
Defenders can potentially stop an attack at different stages.
Earlier detection can reduce damage.
Defense in depth provides multiple opportunities to break the attack chain.
The Cyber Kill Chain helps with detection, analysis, and response.
Key Takeaways

✅ Cyberattack = Sequence of stages

✅ 7 stages = Recon → Weaponize → Deliver → Exploit → Install → C2 → Objective

✅ Attackers need to progress through the chain.

✅ Defenders only need to successfully break an important link.

✅ Earlier detection is generally better.

✅ Defense in depth creates multiple opportunities to stop an attack.

✅ The Cyber Kill Chain helps SOC analysts understand and investigate attacks.

Reflection

Today's lesson changed the way I think about cyberattacks.

Instead of seeing an attack as one single event, I now understand it as a chain of activities. Each stage gives defenders an opportunity to detect or stop the attacker.

The most powerful idea I learned was that the attacker has to successfully progress through the chain, while the defender only needs to break one important link.

I also understood why early detection is so valuable. If an attack can be stopped during reconnaissance or delivery, the attacker may never get the opportunity to exploit the system, establish persistence, communicate with their infrastructure, or achieve their objective.

My biggest takeaway is:

The attacker needs to complete the chain. The defender only needs to break it.

Quote of the Day

"You don't have to stop the entire attack. You just have to break the chain."

Progress Tracker
Day: 71/90
Topic: Cyber Kill Chain
Core Concepts: Reconnaissance, Weaponization, Delivery, Exploitation, Installation, Command & Control, Actions on Objectives
Security Focus: Attack Detection and Prevention
Connected Skills: IDS/IPS, SIEM, Network Forensics, Defense in Depth
Key Insight: Every stage of an attack provides an opportunity for defenders to detect and stop it.
Status: ✅ Completed
