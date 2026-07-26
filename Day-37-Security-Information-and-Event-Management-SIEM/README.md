Day 37 - Security Information and Event Management (SIEM)
Objective

Understand the purpose of a Security Information and Event Management (SIEM) platform, learn how it collects and correlates security logs, explore common SIEM tools, and understand the differences between SIEM, SOAR, and MDR.

Lesson of the Day

Today, I learned about Security Information and Event Management (SIEM), one of the most important technologies used in modern Security Operations Centers (SOCs).

Organizations generate thousands or even millions of security logs every day. A SIEM platform helps security teams collect, organize, analyze, and correlate these logs to identify potential threats.

A simple way to remember SIEM is:

A SIEM brings security logs together, connects related events, and helps analysts detect threats faster.

What is SIEM?

Security Information and Event Management (SIEM) combines two concepts:

Security Information Management (SIM)

SIM focuses on collecting, storing, and analyzing log data from multiple systems.

It is mainly used for:

Long-term log storage
Reporting
Compliance
Historical analysis
Security Event Management (SEM)

SEM focuses on monitoring security events in real time.

It helps by:

Monitoring live events
Correlating logs
Detecting suspicious activity
Generating security alerts

Together, SIM and SEM form a complete SIEM solution.

What Does a SIEM Collect?

A SIEM gathers logs from many different systems, including:

Servers
Endpoints
Firewalls
Applications
Network devices
Security tools

By collecting information from multiple sources, analysts gain a centralized view of an organization's security events.

What a SIEM Actually Does
1. Collection

The SIEM collects logs from different systems across the organization.

Instead of checking each device individually, analysts can review everything in one place.

2. Normalization

Different devices produce logs in different formats.

A SIEM converts these logs into a standardized format so they can be searched and analyzed consistently.

3. Correlation

Correlation is one of the most powerful features of a SIEM.

Instead of treating each log as an isolated event, the SIEM connects related events across multiple systems to identify suspicious activity.

4. Alerting and Dashboards

When suspicious behavior is detected, the SIEM generates alerts.

Dashboards provide security teams with a real-time view of:

Security events
Active alerts
System health
Investigation status
5. Search and Investigation

SIEM platforms allow analysts to search historical logs during incident investigations.

This supports:

Threat hunting
Incident response
Digital forensics
Compliance investigations
Examples of Correlation Rules

Today's lesson covered several common examples of event correlation.

1. Brute Force Attack

Multiple failed login attempts followed by a successful login may indicate a brute-force attack.

2. Credential Stuffing

Repeated login attempts using stolen username and password combinations across many accounts may indicate credential stuffing.

3. Impossible Travel

If a user logs in from two geographically distant locations within an unrealistically short period, the SIEM may generate an Impossible Travel alert.

Example:

09:00 - Mumbai

09:20 - London

Impossible travel detected
4. Full Attack Chain

A SIEM can correlate multiple related events, such as:

Phishing email received
User account compromised
Privilege escalation
Suspicious file execution
Data exfiltration

By linking these events together, analysts gain a clearer picture of the complete attack.

Common SIEM Tools

Today's lesson introduced several widely used SIEM platforms.

1. Splunk

A popular platform for log management, monitoring, and security analysis used by many organizations.

2. Microsoft Sentinel

Microsoft's cloud-native SIEM and security analytics platform built on Azure.

3. Elastic Security (ELK Stack)

A security solution based on Elasticsearch, Logstash, and Kibana that provides log collection, search, visualization, and security analytics.

4. IBM QRadar

An enterprise SIEM platform used for security monitoring, correlation, and incident investigation.

5. Google Security Operations

Google's cloud-based security operations platform that provides threat detection, investigation, and response capabilities.

SIEM vs SOAR

I also learned about SOAR (Security Orchestration, Automation, and Response).

Although SIEM and SOAR work closely together, they have different purposes.

SIEM	SOAR
Collects and analyzes logs	Automates security actions
Detects suspicious activity	Responds to incidents automatically
Generates alerts	Executes predefined playbooks
Supports investigations	Reduces manual response effort

A simple way to remember the difference:

SIEM tells you something happened.
SOAR helps respond to it automatically.
What is MDR?

I also learned about Managed Detection and Response (MDR).

MDR is a managed security service where an external cybersecurity provider helps organizations:

Monitor security events
Investigate threats
Respond to incidents

This allows organizations without a large internal security team to benefit from continuous security monitoring and expert support.

What I Learned
SIEM combines Security Information Management (SIM) and Security Event Management (SEM).
SIEM collects logs from many security sources.
Correlation helps identify attacks that may not be obvious from individual events.
Dashboards and alerts provide real-time visibility into security incidents.
SIEM supports threat hunting, investigations, and forensic analysis.
SOAR automates incident response actions.
MDR provides managed monitoring and incident response through external security experts.
Key Takeaways

✅ SIEM centralizes security logs.

✅ Correlation connects related security events.

✅ Dashboards help analysts monitor security in real time.

✅ SIEM supports investigations and compliance.

✅ SOAR automates incident response.

✅ MDR provides expert-managed threat detection and response services.

Reflection

Today's lesson helped me understand how Security Operations Centers manage and analyze enormous amounts of security data.

I learned that a SIEM is much more than a log storage system. By collecting data from multiple sources, normalizing it, correlating related events, and generating meaningful alerts, it enables analysts to detect threats that might otherwise go unnoticed.

Learning about SOAR and MDR also showed me how modern organizations combine technology, automation, and expert services to improve their overall security operations.

My biggest takeaway is:

Collecting logs is only the beginning—real security comes from connecting events, identifying meaningful patterns, and responding quickly to threats.

Quote of the Day

"Individual logs tell a story. A SIEM connects those stories into the bigger picture."

Progress Tracker
Day: 37/90
Topic: Security Information and Event Management (SIEM)
Concepts Learned: SIEM, SIM, SEM, Log Collection, Normalization, Correlation, Alerting, SOAR, MDR
Tools Learned: Splunk, Microsoft Sentinel, Elastic Security (ELK), IBM QRadar, Google Security Operations
Key Insight: SIEM platforms help security teams detect threats by collecting, correlating, and analyzing logs from multiple systems.
Status: ✅ Completed
