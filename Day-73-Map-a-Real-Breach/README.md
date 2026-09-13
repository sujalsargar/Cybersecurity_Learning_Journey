Day 73 – Map a Real Breach
🎯 Objective

To analyze a realistic cyber breach, map the attack to the Cyber Kill Chain, identify the MITRE ATT&CK tactics involved, and understand where defenders could have stopped the attack.

📚 Lesson of the Day

A cyberattack is not a single action. It is a sequence of steps.

By mapping a real breach to the Cyber Kill Chain, security analysts can understand:

How the attacker entered the organization
How the attack progressed
What the attacker did after gaining access
Which security controls could have stopped the attack
Where the organization had opportunities to detect or block the attacker

For this exercise, I analyzed a realistic phishing-based breach involving a finance department.

🔗 Breach Mapped to the Cyber Kill Chain
1. Reconnaissance

The attacker first collected information about the company.

They discovered:

Employee names
Company email format
Finance department employees
Information that could help create a convincing phishing email

Goal: Gather information about the target before attacking.

Possible Defense: Limit unnecessary public information about the company and employees.

2. Weaponization

The attacker prepared the tool used for the attack.

In this case, they created a fake invoice containing a malicious attachment.

The invoice was designed to look like a normal business document so that a finance employee would be more likely to open it.

Goal: Prepare a malicious file or payload for delivery.

Possible Defense: Use email security controls and attachment scanning to identify suspicious files.

3. Delivery

The attacker sent the phishing email containing the malicious invoice attachment to finance employees.

The email was the method used to deliver the attack to the target.

Goal: Get the malicious file or message to the victim.

Possible Defense: Use email security filters, spam protection, attachment scanning, and phishing awareness training.

4. Exploitation

An employee opened the malicious attachment.

The attachment exploited outdated software on the employee's computer.

This allowed the attacker to execute malicious activity on the system.

Goal: Take advantage of a vulnerability to gain execution or access.

Possible Defense: Keep operating systems and software updated and apply security patches regularly.

5. Installation

After exploitation, the attacker installed a backdoor on the compromised computer.

A backdoor can provide an attacker with continued access to a system.

Goal: Establish a way to maintain access.

Possible Defense: Monitor for unexpected software, suspicious files, unauthorized changes, and unusual scheduled tasks.

6. Command and Control (C2)

The infected computer connected to an attacker-controlled server.

This communication gave the attacker a way to interact with the compromised system and continue the attack.

Goal: Maintain communication with the compromised system.

Possible Defense: Monitor unusual outbound connections, suspicious domains, and unexpected network traffic.

7. Actions on Objectives

The attacker began carrying out their final goals.

They:

Explored the network
Stole usernames and passwords
Moved to other computers
Reached the customer database

This stage caused the actual business impact of the breach.

Goal: Achieve the attacker's intended objective, such as stealing information or accessing important systems.

Possible Defense: Monitor unusual data transfers, restrict access to sensitive databases, use least privilege, and monitor lateral movement.

🗺️ Complete Attack Flow
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
Command & Control
      ↓
Actions on Objectives
      ↓
Customer Database Access

The attack shows how a simple phishing email can eventually lead to access to sensitive business data.

🧩 MITRE ATT&CK Tactics Identified

The later stages of the attack can also be mapped to MITRE ATT&CK tactics.

1. Discovery

The attacker explored the network to understand available systems and resources.

What: Find information about the environment.

2. Credential Access

The attacker stole usernames and passwords.

What: Obtain credentials that can be used to access systems and accounts.

3. Lateral Movement

The attacker moved from the initially compromised computer to other systems.

What: Move through the organization's network.

🛡️ Finding Where the Chain Could Break

One of the most important lessons from this exercise is that defenders do not have to stop an attack at only one point.

There are multiple opportunities to break the chain.

Kill Chain Stage	Possible Defense
Reconnaissance	Limit unnecessary public information
Weaponization	Scan attachments and detect malicious content
Delivery	Use email security filters
Exploitation	Keep software updated and patched
Installation	Monitor for backdoors and unexpected scheduled tasks
Command & Control	Monitor unusual outbound connections
Actions on Objectives	Monitor large or unusual data transfers
🔐 Defense in Depth

This breach demonstrates why defense in depth is important.

If one control fails, another control can still stop the attacker.

For example:

Phishing Email
      ↓
Email Filter ❌ Missed It
      ↓
Employee Opens Attachment
      ↓
Software Patch ❌ Missing
      ↓
Backdoor Installed
      ↓
Endpoint Monitoring ✅ Detects It
      ↓
Attack Stopped

Security should therefore use multiple layers instead of depending on one security control.

🔄 Connection With Previous Learning

This exercise connects several concepts I have learned:

Day 71 – Cyber Kill Chain: Used to map the attack from reconnaissance to final objectives.
Day 72 – MITRE ATT&CK: Used to identify specific attacker behaviors such as Discovery, Credential Access, and Lateral Movement.
Phishing: Used as the delivery method.
Software Updates: Could have prevented exploitation of outdated software.
Network Monitoring: Could help detect Command and Control activity.
Least Privilege: Could reduce the attacker's ability to access sensitive systems.
Logs and SIEM: Could help detect and investigate suspicious activity.
🧠 What I Learned
A breach can be analyzed as a sequence of attack stages.
The Cyber Kill Chain helps visualize the overall attack.
MITRE ATT&CK provides more detailed information about attacker behavior.
Every stage provides an opportunity for defense.
Security controls should work together.
A phishing email can become a serious breach when combined with an unpatched vulnerability.
Monitoring after compromise is just as important as preventing the initial attack.
Attackers may move from one compromised system to more valuable systems.
The goal of defense is to break the attack chain as early as possible.
🔑 Key Takeaways

Attackers need to complete the chain. Defenders only need to break it once.

Simple memory:

Kill Chain = Where the attack goes

ATT&CK = What the attacker does

Defense = Where we can stop it

💭 Reflection

Today I practiced analyzing a realistic breach instead of looking at each attack technique separately. Mapping the incident across the Kill Chain helped me understand how an attack can progress from simple reconnaissance and phishing to network compromise and sensitive data access.

The biggest lesson for me is that every stage of an attack is also an opportunity for defense.

💬 Quote of the Day

“Find the attack path. Break it before it reaches the goal.”

📈 Progress Tracker

Day 73 / 90 Completed ✅

73 days of learning. 17 days remaining.

Current Focus: Cybersecurity Fundamentals → Attack Analysis → Detection & Defense
