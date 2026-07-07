Day 18 - How Attacks Actually Work
Objective

Understand how real cyberattacks progress through multiple stages, learn the Cyber Kill Chain framework, explore the MITRE ATT&CK framework, and understand how defenders can interrupt an attack before it reaches its final objective.

Lesson of the Day

Today, I learned an important cybersecurity concept:

Real attacks follow a process.

Cyberattacks usually do not happen in a single step. An attacker moves through multiple stages, starting with gathering information and eventually attempting to achieve a final objective.

The most important lesson was:

If defenders interrupt the attack at any stage, they can prevent the later stages from happening.

For example, if an attack is detected and stopped at Stage 3 - Delivery, then:

Stage 4 - Exploitation
Stage 5 - Installation
Stage 6 - Command and Control
Stage 7 - Actions on Objectives

may never happen.

This is one of the core responsibilities of cybersecurity defenders.

Cyber Kill Chain

The Cyber Kill Chain is a cybersecurity framework developed by Lockheed Martin and publicly introduced in 2011.

It describes how many cyber intrusions progress through seven stages.

The seven stages are:

Reconnaissance
Weaponization
Delivery
Exploitation
Installation
Command and Control
Actions on Objectives
1. Reconnaissance

The attacker gathers information about the target.

This may include information about:

Domains
IP addresses
Employees
Email addresses
Technologies
Applications
Cloud infrastructure
Publicly exposed systems

The attacker's goal is to understand the target and identify possible weaknesses.

Defender's Goal

Defenders can:

Reduce unnecessary public exposure
Monitor reconnaissance activity
Secure exposed services
Review attack surfaces
2. Weaponization

The attacker prepares something that can be used against the target.

This may involve:

Malicious documents
Exploit chains
Malware
Payloads
Phishing content

The attacker combines knowledge of a weakness with a method of exploitation.

Defender's Goal

Defenders can:

Use threat intelligence
Track known malicious tools
Detect suspicious payloads
Maintain updated security controls
3. Delivery

The attacker delivers the malicious content or attack mechanism to the target.

Possible delivery methods include:

Phishing emails
Malicious links
Malicious attachments
Compromised websites
Exposed internet-facing applications
Defender's Goal

Defenders can:

Filter suspicious emails
Block malicious domains
Scan attachments
Train users
Monitor exposed applications

If the attack is stopped here, the later stages may never occur.

4. Exploitation

The attacker exploits a vulnerability or weakness.

Examples may include:

Software vulnerabilities
Web application vulnerabilities
Weak authentication
Misconfigurations
Social engineering

The goal is to gain unauthorized access or execute attacker-controlled actions.

Defender's Goal

Defenders can:

Patch vulnerabilities
Monitor suspicious behavior
Use secure configurations
Detect exploitation attempts
5. Installation

The attacker attempts to establish a presence in the compromised environment.

This may involve:

Installing malware
Creating persistence
Deploying malicious tools
Modifying system settings

The goal is often to maintain access.

Defender's Goal

Defenders can:

Use EDR tools
Monitor file changes
Detect suspicious processes
Monitor persistence mechanisms
6. Command and Control

Command and Control is commonly called C2 or C&C.

At this stage, a compromised system communicates with infrastructure controlled by the attacker.

This communication may allow the attacker to:

Send commands
Control malware
Download additional tools
Coordinate further actions
Defender's Goal

Defenders can:

Monitor unusual outbound traffic
Block malicious domains and IP addresses
Detect suspicious DNS activity
Analyze network behavior
7. Actions on Objectives

This is the stage where the attacker attempts to achieve the final goal.

Possible objectives include:

Stealing data
Disrupting operations
Financial fraud
Espionage
Extortion
Account takeover
Defender's Goal

Defenders can:

Detect unusual data access
Monitor data movement
Apply access controls
Use incident response procedures
Cyber Kill Chain Flow
Reconnaissance
      ↓
Weaponization
      ↓
Delivery
      ↓
Exploitation
      ↓
Installation
      ↓
Command and Control
      ↓
Actions on Objectives

The key defensive idea is:

Break the chain at any stage.

Capital One Case Study and the Cyber Kill Chain

Today, I also learned how the 2019 Capital One breach can be studied using the Cyber Kill Chain as a defensive learning exercise.

A simplified mapping can look like this:

1. Reconnaissance

The attacker identifies:

An internet-facing application environment
Potential weaknesses
Cloud-connected infrastructure
2. Weaponization

The attacker prepares requests designed to exploit the identified server-side weakness.

3. Delivery

The crafted request is sent to the vulnerable application environment.

4. Exploitation

A Server-Side Request Forgery (SSRF) weakness is exploited.

This allows unintended server-side requests to internal resources.

5. Installation

This stage does not always map perfectly to every real-world attack.

Not every attack requires traditional malware installation.

In this case, the attacker could continue using obtained access rather than installing conventional malware on a victim endpoint.

6. Command and Control

This stage also does not perfectly match every cloud-focused intrusion.

The attacker could interact with cloud resources using obtained access rather than relying on a traditional malware-based C2 channel.

7. Actions on Objectives

The attacker accesses and exfiltrates sensitive data.

Important Lesson from the Mapping

The Cyber Kill Chain is useful, but real attacks do not always fit perfectly into every stage.

Some attacks:

Skip stages
Combine stages
Repeat stages
Use cloud identities instead of malware
Do not require traditional Command and Control

This is why cybersecurity professionals also use other frameworks such as MITRE ATT&CK.

MITRE ATT&CK Framework

I also learned about MITRE ATT&CK, an industry-standard cybersecurity knowledge base.

ATT&CK stands for:

Adversarial Tactics, Techniques, and Common Knowledge

It is developed and maintained by the MITRE Corporation.

MITRE ATT&CK is widely used by:

SOC Analysts
Threat Intelligence Teams
Red Teams
Blue Teams
Incident Responders
Detection Engineers
Security Tool Vendors
Two Important Components
1. Tactics - "The Why"

Tactics describe the attacker's objective.

They answer:

Why is the attacker performing this action?

Examples include:

Initial Access
Execution
Persistence
Privilege Escalation
Credential Access
Discovery
Collection
Exfiltration
2. Techniques - "The How"

Techniques describe how the attacker attempts to achieve the objective.

They answer:

How is the attacker doing it?

For example:

Tactic:
Credential Access

Question:
Why?

Answer:
The attacker wants to obtain credentials.

Then:

Technique:
Phishing for Information

Question:
How?

Answer:
The attacker attempts to obtain information through phishing.
Cyber Kill Chain vs MITRE ATT&CK
Cyber Kill Chain

Helps understand:

How an intrusion progresses through stages.

It provides a high-level attack lifecycle.

MITRE ATT&CK

Helps understand:

What behaviors and techniques attackers use during operations.

It provides more detailed information about adversary behavior.

Simple Difference
Cyber Kill Chain
      ↓
Where is the attacker in the attack process?
MITRE ATT&CK
      ↓
Why is the attacker doing this?
How are they doing it?

Both frameworks help defenders understand and detect attacks.

What I Learned
Real cyberattacks usually follow a process.
Attackers move through multiple stages.
The Cyber Kill Chain contains seven stages.
Defenders can stop attacks by interrupting the chain.
Not every real attack fits perfectly into every Kill Chain stage.
MITRE ATT&CK is widely used across the cybersecurity industry.
Tactics represent "The Why."
Techniques represent "The How."
Understanding attacker behavior helps defenders build better detection and response strategies.
Key Takeaways

✅ Real attacks follow a process.

✅ The seven Cyber Kill Chain stages are:

Reconnaissance
Weaponization
Delivery
Exploitation
Installation
Command and Control
Actions on Objectives

✅ If defenders stop the attack early, later stages may never happen.

✅ MITRE ATT&CK helps security teams understand adversary behavior.

✅ Tactics explain why an attacker performs an action.

✅ Techniques explain how an attacker performs that action.

Reflection

Today's lesson changed how I think about cyberattacks.

Earlier, I often thought of an attack as one event. Now I understand that real attacks usually involve a sequence of actions.

The most important lesson for me was that defenders do not always need to wait until the final stage. If they detect and interrupt the attacker during reconnaissance, delivery, exploitation, or any other stage, they may prevent the rest of the attack.

Learning about the Cyber Kill Chain and MITRE ATT&CK also helped me understand how SOC Analysts and security teams study attacker behavior in a structured way.

My biggest takeaway is:

The defender's job is to break the chain before the attacker reaches the objective.

Quote of the Day

"Break the chain at any stage, and the rest of the attack may never happen."

Progress Tracker
Day: 18/90
Topic: How Attacks Actually Work
Frameworks Learned: Cyber Kill Chain, MITRE ATT&CK
Cyber Kill Chain Stages: Reconnaissance, Weaponization, Delivery, Exploitation, Installation, Command and Control, Actions on Objectives
MITRE ATT&CK Concepts: Tactics and Techniques
Case Study: Capital One Data Breach mapped to the Cyber Kill Chain
Key Insight: Defenders can stop an attack by interrupting the attack process before the attacker reaches the final objective.
Status: ✅ Completed
