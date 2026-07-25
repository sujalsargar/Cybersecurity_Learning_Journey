Day 36 - Intrusion Detection and Prevention Systems (IDS & IPS)
Objective

Understand the purpose of Intrusion Detection Systems (IDS) and Intrusion Prevention Systems (IPS), learn how they detect threats, explore common detection methods, and understand the challenges of false positives and alert fatigue.

Lesson of the Day

Today, I learned about Intrusion Detection Systems (IDS) and Intrusion Prevention Systems (IPS).

Both are important network security technologies used to detect malicious activity. However, they differ in how they interact with network traffic.

A simple way to remember the difference is:

An IDS watches and alerts. An IPS watches, alerts, and blocks.

What is an IDS?

An Intrusion Detection System (IDS) monitors network traffic for suspicious or malicious activity.

An IDS receives a copy of the network traffic, meaning it does not sit directly in the communication path.

Because of this, an IDS can:

Detect suspicious activity
Generate alerts
Help security analysts investigate threats

However, it cannot block attacks because it is only monitoring traffic.

What is an IPS?

An Intrusion Prevention System (IPS) sits directly in the network traffic path.

Since all traffic passes through it, an IPS can:

Detect malicious activity
Block malicious traffic in real time
Prevent attacks before they reach the target

This makes an IPS more powerful than an IDS, but it also introduces the risk of blocking legitimate traffic if a false alert occurs.

IDS vs IPS
Feature	IDS	IPS
Position	Monitors a copy of traffic	Sits directly in the traffic path
Detect Attacks	✅ Yes	✅ Yes
Generate Alerts	✅ Yes	✅ Yes
Block Attacks	❌ No	✅ Yes
Risk of Blocking Legitimate Traffic	No	Yes (if false positives occur)
Detection Methods

Modern IDS and IPS solutions commonly use two main detection methods.

1. Signature-Based Detection

Signature-based detection compares network activity against a database of known attack patterns or signatures.

Advantages:

Fast
Accurate for known threats
Low false positive rate for recognized attacks

Limitation:

Cannot detect completely new or unknown attacks without an existing signature.
2. Anomaly-Based Detection

Anomaly-based detection learns what normal network behavior looks like.

When unusual or unexpected activity is observed, it generates an alert.

Advantages:

Can detect previously unknown attacks.
Helps identify unusual behavior.

Limitation:

May generate more false positives because unusual behavior is not always malicious.
The False Positive Problem

One of the biggest challenges with IDS and IPS systems is false positives.

A false positive occurs when normal, legitimate activity is incorrectly identified as an attack.

For example:

A legitimate user may trigger an alert.
An IPS might block valid traffic by mistake.

If an IDS or IPS is configured to be too sensitive, it may generate thousands of alerts every day.

Many of these alerts may be harmless, making it difficult for analysts to identify genuine threats.

Alert Fatigue

Too many alerts can lead to alert fatigue.

Alert fatigue happens when security analysts become overwhelmed by the volume of alerts.

As a result:

Important alerts may be overlooked.
Investigation time increases.
Real attacks may go unnoticed.

Reducing unnecessary alerts is an important part of operating an effective Security Operations Center (SOC).

Finding the Right Balance

A security team must carefully balance detection sensitivity.

Too Sensitive
Too many false alerts
Increased alert fatigue
Legitimate traffic may be interrupted
Not Sensitive Enough
Real attacks may not be detected
Security incidents could go unnoticed

Finding the right balance requires continuous tuning and monitoring.

Best Practices

Some common ways to improve IDS and IPS effectiveness include:

Carefully tune detection rules.
Assign severity levels to alerts.
Investigate critical alerts first.
Use a Security Information and Event Management (SIEM) platform to collect, correlate, and prioritize alerts from multiple security tools.

These practices help analysts focus on the most important security events.

Common IDS/IPS Tools

Today's lesson introduced several popular open-source security tools.

1. Snort

Snort is a widely used open-source IDS and IPS that primarily uses signature-based detection.

2. Suricata

Suricata is an open-source IDS/IPS engine capable of high-performance traffic inspection using both signature-based detection and protocol analysis.

3. Zeek

Zeek (formerly Bro) focuses on network monitoring and security analysis.

Instead of simply matching signatures, it generates detailed logs that help analysts investigate network activity.

Host-Based Intrusion Detection System (HIDS)

I also learned about Host-Based Intrusion Detection Systems (HIDS).

Unlike network IDS, a HIDS runs directly on an individual computer or server.

It monitors the host for suspicious activity such as:

Unauthorized file changes
Unusual processes
Signs of compromise
Suspicious system activity

A HIDS helps detect attacks that may not be visible from network traffic alone.

What I Learned
IDS detects attacks but does not block them.
IPS detects and blocks malicious traffic in real time.
Signature-based detection identifies known attack patterns.
Anomaly-based detection identifies unusual behavior.
False positives are a major challenge for IDS and IPS systems.
Alert fatigue can reduce an analyst's effectiveness.
SIEM platforms help organize and prioritize security alerts.
HIDS protects individual computers and servers by monitoring local activity.
Key Takeaways

✅ IDS monitors and alerts.

✅ IPS monitors, alerts, and blocks attacks.

✅ Signature-based detection identifies known threats.

✅ Anomaly-based detection helps identify unknown threats.

✅ Too many false positives can lead to alert fatigue.

✅ Proper tuning and alert prioritization improve detection quality.

✅ HIDS provides security monitoring at the host level.

Reflection

Today's lesson helped me understand how organizations detect and respond to cyber threats in real time.

I learned that IDS and IPS play different but complementary roles in network security. While IDS provides visibility by detecting suspicious activity, IPS adds protection by actively blocking malicious traffic.

I also realized that detection alone is not enough. Security teams must carefully tune these systems to reduce false positives, prioritize important alerts, and avoid alert fatigue. Understanding these operational challenges gave me a better appreciation of how Security Operations Centers (SOCs) manage large volumes of security events.

My biggest takeaway is:

An effective IDS or IPS is not the one that generates the most alerts—it is the one that helps analysts identify and respond to real threats efficiently.

Quote of the Day

"The goal is not more alerts—it's better alerts."

Progress Tracker
Day: 36/90
Topic: Intrusion Detection and Prevention Systems (IDS & IPS)
Concepts Learned: IDS, IPS, Signature-Based Detection, Anomaly-Based Detection, False Positives, Alert Fatigue, HIDS, SIEM
Tools Learned: Snort, Suricata, Zeek
Key Insight: Effective intrusion detection requires balancing sensitivity, reducing false positives, and prioritizing critical alerts.
Status: ✅ Completed
