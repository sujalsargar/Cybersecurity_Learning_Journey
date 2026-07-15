Day 26 - Map a Website Footprint
Objective

Perform passive reconnaissance using publicly available information to understand a website's infrastructure without directly interacting with the target systems.

Lesson of the Day

Today was a hands-on practical session focused on Passive Reconnaissance.

Unlike previous lessons that introduced new theory, today's objective was to apply what I had already learned by collecting and analyzing publicly available information about a website.

The goal was to understand a website's digital footprint without sending direct traffic to the target.

Passive vs Active Reconnaissance
Passive Reconnaissance

Passive reconnaissance involves gathering information that is already publicly available.

Examples include:

DNS records
WHOIS information
Certificate Transparency logs
Website technologies
Public domain information

The target system is not directly interacted with during this process.

Active Reconnaissance

Active reconnaissance involves directly communicating with the target system.

Examples include:

Port scanning
Service enumeration
Vulnerability scanning
Banner grabbing

Since active reconnaissance sends traffic to the target, it is generally more detectable than passive reconnaissance.

Practical Activity

Today's task was to perform passive reconnaissance on a target website using publicly available information.

During the investigation, I collected and analyzed information such as:

DNS records
WHOIS information
SSL/TLS certificate details
Certificate Transparency logs
Website technologies
Domain information
Basic infrastructure observations

The entire investigation was performed using publicly available sources.

Information Collected
DNS Records

I reviewed publicly available DNS information to understand how the domain is configured.

This included records such as:

A Records
AAAA Records
MX Records
NS Records
TXT Records

These records help reveal how a domain communicates with different internet services.

WHOIS Information

I examined publicly available domain registration information to understand details such as:

Registrar
Registration dates
Expiration dates
Name servers

This helps provide background information about the domain.

SSL/TLS Certificate

I reviewed the website's SSL/TLS certificate and observed information including:

Certificate validity period
Issuer
Expiration date
Certificate details

This helped me understand how websites use digital certificates to secure HTTPS connections.

Certificate Transparency Logs

I explored Certificate Transparency logs to identify publicly issued certificates related to the target domain.

These logs can provide useful insights into a website's certificate history and related domains.

Website Technologies

I also identified technologies used by the website, such as:

Web server
Frameworks
JavaScript libraries
Content Management Systems (if detectable)

Understanding the technology stack provides useful context during reconnaissance.

Practical Outcome

After collecting the information, I prepared a Network Footprint Report.

The report summarized:

Domain information
DNS records
SSL/TLS certificate details
Website technologies
Infrastructure observations
General security recommendations

The objective was not to exploit the website but to understand its publicly visible footprint.

Skills Practiced

Today's exercise helped me practice:

Information gathering
Passive reconnaissance
DNS analysis
Certificate analysis
Technology identification
Documentation
Report writing
What I Learned
Passive reconnaissance relies only on publicly available information.
Public information can reveal valuable details about a website's infrastructure.
DNS records help understand how a domain is configured.
WHOIS provides useful domain registration information.
SSL/TLS certificates reveal certificate-related details and validity periods.
Certificate Transparency logs can provide additional domain insights.
Website technology fingerprinting helps identify the technologies used to build a website.
Documenting findings is an important part of a security assessment.
Key Takeaways

✅ Passive reconnaissance does not require direct interaction with the target.

✅ Public information can reveal valuable infrastructure details.

✅ DNS, WHOIS, SSL certificates, and Certificate Transparency logs are important reconnaissance sources.

✅ Technology fingerprinting helps understand how a website is built.

✅ Good documentation is just as important as information gathering.

Reflection

Today's lesson showed me how much information is publicly available about a website without performing any intrusive activity.

Instead of looking for vulnerabilities, I focused on understanding the target's infrastructure by analyzing DNS records, domain details, SSL certificates, Certificate Transparency logs, and the technologies used by the website.

Creating a Network Footprint Report helped me organize my findings in a professional format and reinforced the importance of documentation during security assessments.

My biggest takeaway is:

Before testing a system, understand it. Passive reconnaissance provides valuable insights while minimizing interaction with the target.

Quote of the Day

"Good security assessments begin with good reconnaissance."

Project Completed
Project: Website Footprint Analysis
Methodology: Passive Reconnaissance
Information Collected: DNS Records, WHOIS, SSL Certificate, Certificate Transparency Logs, Website Technologies
Deliverable: Network Footprint Report
Status: ✅ Completed
Progress Tracker
Day: 26/90
Topic: Map a Website Footprint
Type: Hands-on Practical
Concepts Practiced: Passive Reconnaissance, DNS Analysis, WHOIS, SSL Certificates, Certificate Transparency, Technology Fingerprinting
Practical Activity: Created a Network Footprint Report
Key Insight: Publicly available information can reveal a detailed picture of a website's infrastructure without directly interacting with the target.
Status: ✅ Completed
