Day 17 - The Cloud: Someone Else's Computer
Objective

Understand what cloud computing is, learn about major cloud service providers and basic AWS services, explore how cloud misconfigurations can lead to security incidents, and understand what security analysts check in cloud environments.

Lesson of the Day

Today, I learned about Cloud Computing.

A simple way to understand the cloud is:

"The cloud is someone else's computer."

Instead of storing and processing everything only on our own device, data and applications can run on computers located in remote data centers.

Organizations provide this infrastructure as a service, and customers pay to use computing power, storage, networking, and other resources.

What is Cloud Computing?

Cloud computing allows users and organizations to access computing resources over the internet.

Instead of buying and maintaining all physical servers themselves, organizations can use cloud infrastructure.

Cloud services can provide:

Computing power
Data storage
Databases
Networking
Identity management
Security services
Application hosting

The physical servers are usually located inside large remote data centers.

Three Major Cloud Service Providers
1. Amazon Web Services (AWS)

AWS provides cloud services for:

Computing
Storage
Networking
Databases
Security
Machine Learning
2. Microsoft Azure

Microsoft Azure provides cloud infrastructure and services commonly used by:

Businesses
Enterprises
Developers
Government organizations
3. Google Cloud Platform (GCP)

Google Cloud Platform provides services for:

Computing
Storage
Data Analytics
Artificial Intelligence
Networking
Application Hosting
AWS Services I Learned About

Today, I explored some important AWS services.

1. EC2 - Elastic Compute Cloud

EC2 provides virtual computers in the cloud.

It can be used to:

Run applications
Host websites
Deploy servers
Perform computing tasks

A simple way to think about EC2:

A virtual computer running inside AWS infrastructure.

2. S3 - Simple Storage Service

S3 is an object storage service.

It can store:

Images
Videos
Documents
Backups
Application files
Logs

One major security concern is accidentally making sensitive storage publicly accessible.

3. IAM - Identity and Access Management

IAM controls:

Who can access what?

IAM helps manage:

Users
Roles
Permissions
Policies
Access to AWS resources

Incorrect IAM permissions can create serious security risks.

4. VPC - Virtual Private Cloud

A VPC is an isolated virtual network inside AWS.

It helps organizations control:

Network ranges
Subnets
Routing
Internet access
Security boundaries
Resource communication

A simple way to think about VPC:

A private network built inside the cloud.

Cloud Security: The Configuration Matters

One of the biggest lessons today was that many cloud security incidents do not happen simply because the cloud provider itself is insecure.

Security problems can happen because of:

Misconfigurations
Excessive permissions
Publicly exposed storage
Weak credentials
Missing MFA
Poor network rules
Exposed secrets
Insufficient logging

This introduced me to an important cloud security idea:

Using the cloud securely requires correct configuration and access control.

Case Study - Capital One Data Breach (2019)

I also learned about the Capital One data breach, which was disclosed in 2019.

This case is an important example of how cloud-hosted environments can be exposed through application and configuration weaknesses.

At a high level, the attacker exploited a Server-Side Request Forgery (SSRF) vulnerability involving a web application firewall environment.

This allowed access to temporary cloud credentials, which were then used to access data stored in cloud resources.

Simplified Attack Flow
Attacker
   ↓
Exploits SSRF Weakness
   ↓
Server Makes an Unintended Internal Request
   ↓
Temporary Cloud Credentials Become Accessible
   ↓
Credentials Are Misused
   ↓
Cloud Data Is Accessed
What is SSRF?

SSRF stands for:

Server-Side Request Forgery

In an SSRF attack, an attacker tricks a server into making a request that the server should not normally make.

For example, a vulnerable server may be manipulated into accessing:

Internal services
Private network resources
Cloud metadata services
Other restricted endpoints

This can become especially dangerous in cloud environments if sensitive credentials or internal services are exposed.

Important Lesson from the Capital One Case

The lesson was not simply:

"Cloud is insecure."

The more important lesson was:

Security weaknesses can appear when applications, permissions, and cloud configurations are not properly protected.

Cloud providers secure their infrastructure, while customers are also responsible for securely configuring many parts of their cloud environment.

What a Security Analyst Checks in the Cloud
1. Public Storage

Check whether storage resources are accidentally exposed to the internet.

Examples:

Public S3 buckets
Sensitive files accessible without authentication
Incorrect access policies
2. IAM Permissions

Check:

Who has access?
What can they access?
Are permissions excessive?
Are old users still active?
Are unnecessary administrator privileges assigned?

The principle of Least Privilege should be followed.

Give users only the permissions they actually need.

3. Logging and Monitoring

Check whether important activity is being recorded and monitored.

Examples:

Login attempts
API activity
Permission changes
Resource creation
Suspicious access patterns

Without logs, investigating incidents becomes much harder.

4. Root Account MFA

The cloud root or highest-privileged account is extremely sensitive.

Security analysts check whether:

MFA is enabled
Strong authentication is used
The root account is avoided for daily tasks
Access is tightly controlled
5. Data Encryption

Check whether sensitive data is protected:

At rest
In transit

Encryption helps reduce the risk of unauthorized data exposure.

6. Network Exposure

Check whether cloud resources are unnecessarily exposed to the internet.

Examples:

Open ports
Public IP addresses
Overly permissive firewall rules
Exposed databases
Unrestricted remote access
7. Secrets Management

Check how sensitive secrets are stored.

Examples:

API keys
Database passwords
Access tokens
Private keys
Application credentials

Secrets should not be:

Hardcoded into source code
Uploaded to public repositories
Stored in plain text
Shared unnecessarily
Password Security and MFA

Today's lesson also reinforced the importance of strong authentication.

Good practices include:

Use long passwords or passphrases.
Use a different password for every account.
Use a password manager.
Enable MFA wherever possible.
Protect high-privilege cloud accounts carefully.

For important cloud accounts:

A strong unique password + MFA is essential.

What I Learned
The cloud means using computing resources hosted in remote data centers.
AWS, Microsoft Azure, and Google Cloud Platform are major cloud providers.
EC2 provides virtual computing resources.
S3 provides object storage.
IAM controls identities and permissions.
VPC provides isolated cloud networking.
Cloud misconfigurations can create serious security risks.
SSRF can sometimes be used to access internal resources.
Security analysts review permissions, logging, storage, encryption, network exposure, and secrets.
Strong authentication and MFA are essential for important cloud accounts.
Key Takeaways

✅ The cloud is often described as "someone else's computer," but cloud security still requires customer responsibility.

✅ Cloud services must be configured securely.

✅ Public storage can expose sensitive data.

✅ Excessive IAM permissions create unnecessary risk.

✅ Logging and monitoring are essential for detecting suspicious activity.

✅ Root accounts should be strongly protected with MFA.

✅ Sensitive data should be encrypted.

✅ Network exposure should be minimized.

✅ Secrets should never be hardcoded or publicly exposed.

Reflection

Today's lesson helped me understand that cloud security is not only about trusting a cloud provider.

The customer also has an important responsibility to configure cloud resources correctly.

Learning about AWS services such as EC2, S3, IAM, and VPC gave me a clearer understanding of how cloud environments are structured.

The Capital One case study was especially interesting because it showed how an application vulnerability, temporary credentials, and cloud access controls can become connected during a real security incident.

My biggest takeaway is that:

A powerful cloud platform can still become vulnerable when applications, identities, permissions, and configurations are not properly secured.

Quote of the Day

"The cloud is someone else's computer, but securing your cloud configuration is still your responsibility."

Progress Tracker
Day: 17/90
Topic: Cloud Computing and Cloud Security
Cloud Providers Learned: AWS, Microsoft Azure, Google Cloud Platform
AWS Services Learned: EC2, S3, IAM, VPC
Security Concepts: Cloud Misconfiguration, SSRF, IAM Permissions, Public Storage, Logging, MFA, Encryption, Network Exposure, Secrets Management
Case Study: Capital One Data Breach (2019)
Key Insight: Many cloud security incidents happen because of application weaknesses, excessive permissions, or insecure configurations rather than a simple failure of the cloud platform itself.
Status: ✅ Completed
