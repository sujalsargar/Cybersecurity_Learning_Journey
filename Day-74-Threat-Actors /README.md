Day 74 – Threat Actors
🎯 Objective

To understand threat actors, their motivations, capabilities, and how knowing the attacker can help defenders predict attacks and choose the right security response.

📚 Lesson of the Day

Every cyberattack is carried out by a threat actor.

A threat actor can be an individual, group, organization, or other entity that intentionally causes or attempts to cause harm using cyber techniques.

The identity and motivation of a threat actor can influence:

What they target
Which attack techniques they use
How long they stay inside a system
What information they want
How defenders should respond

Not all attackers are the same. Different attackers have different goals, skills, resources, and patience.

🧩 Threat vs Threat Actor

These two terms are related but different.

Threat

A threat is a possible source of harm.

It describes something that could potentially cause damage to a system, organization, or data.

Threat Actor

A threat actor is the actual person or group that may cause harm.

Simple Example
Threat
  ↓
Possible source of harm

Threat Actor
  ↓
Person or group carrying out the harmful activity

Easy way to remember:

Threat = Possible danger
Threat Actor = Who causes the danger

👥 Main Types of Threat Actors

There are several common categories of threat actors.

1. Cybercriminals

Cybercriminals attack systems mainly for financial gain.

They may:

Steal money
Steal credentials
Deploy ransomware
Steal sensitive information
Sell stolen data

Their main motivation is usually profit.

2. Nation-State Actors

Nation-state actors are threat actors supported or directed by governments.

They may target:

Government organizations
Military systems
Critical infrastructure
Companies
Political organizations
Sensitive information

Their goals can include espionage, intelligence gathering, disruption, or strategic advantage.

These attackers may have significant resources, expertise, and patience.

3. Hacktivists

Hacktivists are attackers motivated by political, social, or ideological beliefs.

They may attack organizations to:

Spread a message
Draw public attention
Protest against an organization
Disrupt services
Publish stolen information

Their main motivation is usually an ideological or political cause.

4. Insiders

Insiders are people who already have legitimate access to an organization's systems.

Examples include:

Employees
Contractors
Partners
Former employees with remaining access

An insider can intentionally or accidentally cause harm.

For example, an employee might misuse access and steal confidential information.

5. Script Kiddies

Script kiddies are individuals who use existing tools, scripts, or publicly available attack methods without necessarily having deep technical knowledge.

They may:

Scan systems
Run existing attack tools
Exploit known vulnerabilities
Copy techniques created by others

Their skill level is generally lower than highly capable threat actors.

📊 Capability Spectrum

Threat actors do not all have the same level of capability.

Their capabilities can range from relatively simple to highly sophisticated.

Lower Capability
      ↓
Script Kiddies
      ↓
Less-skilled attackers
      ↓
Skilled Cybercriminal Groups
      ↓
Advanced Groups
      ↓
Nation-State Actors
      ↓
Higher Capability

However, this is a general model, not a strict ranking.

A threat actor's capability can depend on:

Technical knowledge
Available tools
Money and resources
Access to information
Team size
Time and patience
🛡️ Defensive Insight

Understanding the attacker can help defenders make better security decisions.

For example:

Cybercriminal

Likely goal: Money

Possible targets: Financial systems, credentials, valuable data

Defensive focus: Account security, fraud detection, backups, ransomware protection

Nation-State Actor

Likely goal: Intelligence or strategic advantage

Possible targets: Government, critical infrastructure, sensitive organizations

Defensive focus: Strong monitoring, threat intelligence, access control, advanced detection

Hacktivist

Likely goal: Public attention or ideological message

Possible targets: Organizations connected to their cause

Defensive focus: DDoS protection, website security, monitoring, incident response

Insider

Likely goal: Personal benefit, revenge, or accidental damage

Possible targets: Data and systems they can legitimately access

Defensive focus: Least privilege, access monitoring, strong offboarding, data protection

Script Kiddie

Likely goal: Experimentation, attention, or simple disruption

Possible targets: Easily discoverable or vulnerable systems

Defensive focus: Patching, secure configuration, firewalls, monitoring

🌍 Realistic Threat Landscape

The cybersecurity threat landscape is not made up of only highly skilled hackers.

Attackers can range from:

Individuals using basic tools
Organized cybercriminal groups
Ideological groups
Malicious insiders
Highly skilled and well-resourced organizations

This means defenders should not assume that every attack requires an extremely advanced attacker.

Sometimes a basic attack can succeed because of a simple weakness such as:

Weak passwords
Outdated software
Poor access control
Exposed information
Misconfigured systems
Lack of monitoring

Good security protects against both simple and sophisticated threats.

🎯 Why Knowing the Adversary Matters

Understanding threat actors completes the picture of a cyberattack.

Previously, I learned about:

Kill Chain → How an attack progresses

MITRE ATT&CK → What techniques attackers use

Now:

Threat Actors → Who is attacking and why

Knowing the adversary can help defenders understand:

What the attacker may target
What techniques they may prefer
How much effort they may invest
How long they may remain in the environment
What their final objective may be
Which defenses should receive priority
⚙️ Attack = Mechanism + Motive

A useful way to understand an attack is:

                CYBER ATTACK
                     │
          ┌──────────┴──────────┐
          ↓                     ↓
      Mechanism                Motive
          │                     │
   How the attack works      Why they attack
          │                     │
   Techniques and tools       Goal/objective
Mechanism

The technical steps used to carry out the attack.

Examples:

Phishing
Exploitation
Credential theft
Lateral movement
Command and Control
Motive

The goal or reason behind the attack.

Examples:

Financial gain
Espionage
Political beliefs
Revenge
Disruption
Data theft
Simple Example

A cybercriminal may use phishing to steal a user's credentials.

Mechanism → Phishing + Credential Theft
Motive    → Financial Gain

The same technical mechanism can sometimes be used by different threat actors for completely different reasons.

🔄 Connection With Previous Learning

Day 74 connects with several previous concepts:

Day 19 – Social Engineering: Attackers can manipulate people to achieve their goals.
Day 20 – Threat Modeling: Identifying threat actors helps identify risks.
Day 71 – Cyber Kill Chain: Helps understand how an attacker progresses through an attack.
Day 72 – MITRE ATT&CK: Helps understand the techniques used by attackers.
Day 73 – Real Breach Analysis: Helps identify attacker behavior during an actual breach.

Together:

Threat Actor
     ↓
Motive / Goal
     ↓
Chooses Target
     ↓
Uses Techniques
     ↓
Follows Attack Path
     ↓
Attempts to Achieve Objective
🧠 What I Learned
A threat actor is the person or group behind a cyberattack.
Different threat actors have different goals and capabilities.
Cybercriminals generally focus on financial gain.
Nation-state actors may focus on espionage or strategic objectives.
Hacktivists are motivated by political or social causes.
Insiders already have legitimate access to systems.
Script kiddies commonly rely on existing tools and techniques.
Understanding the attacker helps defenders predict possible behavior.
An attack can be understood through both its mechanism and motive.
🔑 Key Takeaways
Easy Memory

Threat = What could cause harm

Threat Actor = Who causes the harm

Mechanism = How the attack happens

Motive = Why the attack happens

Main Threat Actors

C-N-H-I-S

C → Cybercriminals
N → Nation-State Actors
H → Hacktivists
I → Insiders
S → Script Kiddies
💭 Reflection

Today I learned that understanding cybersecurity is not only about knowing how attacks work. It is also important to understand who is behind the attack and what they want.

Different attackers have different motivations, skills, resources, and levels of patience. Knowing these differences can help defenders better understand the threat and choose appropriate defenses.

The biggest lesson for me is:

To understand an attack, understand both the mechanism and the motive.

💬 Quote of the Day

“Know the attacker, understand the motive, defend the target.”

📈 Progress Tracker

Day 74 / 90 Completed ✅

74 days of learning. 16 days remaining.

Current Focus: Cybersecurity Fundamentals → Threat Actors → Adversary Understanding
