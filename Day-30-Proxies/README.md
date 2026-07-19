Day 30 - Proxies
Objective

Understand what a proxy server is, how it works, the different types of proxies, their real-world use cases, and summarize the completion of the first month of my 90-day cybersecurity journey.

Lesson of the Day

Today, I learned about Proxy Servers.

A proxy acts as an intermediary between a client and another server. Instead of communicating directly with a website or service, the request first goes to the proxy, which then forwards it on your behalf.

A simple way to remember it is:

A proxy is a middleman between you and the internet.

Unlike a VPN, which usually encrypts all network traffic, a proxy typically handles specific traffic or services for inspection, filtering, or control.

What is a Proxy?

A proxy server sits between a client and the internet.

When a user makes a request:

The request is sent to the proxy.
The proxy receives and examines the request.
The proxy forwards the request to the destination server.
The response returns through the proxy before reaching the user.
Client
   │
Proxy Server
   │
Website / Server

This allows organizations to monitor, filter, or optimize network traffic.

Types of Proxy Servers
1. Forward Proxy

A Forward Proxy sits between users and the internet.

It forwards requests from internal users to external websites.

Common uses include:

Content filtering
Internet access control
Privacy
Caching
2. Reverse Proxy

A Reverse Proxy sits in front of web servers.

Instead of protecting users, it protects servers by receiving client requests first and then forwarding them to the appropriate backend server.

Common uses include:

Load balancing
Security
SSL/TLS termination
Hiding backend infrastructure
3. Transparent Proxy

A Transparent Proxy intercepts traffic without requiring users to configure their devices.

It is commonly used by:

Schools
Colleges
Companies
Internet Service Providers (ISPs)

Typical purposes include:

Web filtering
Monitoring
Caching
What Proxies Actually Do
1. Content Filtering

Proxies can block access to specific websites or categories of content based on organizational policies.

2. Caching

Frequently accessed web content can be stored temporarily so that future requests are served faster, reducing bandwidth usage.

3. Anonymization

Some proxies can hide a user's IP address from the destination server, providing an additional layer of privacy.

4. Load Balancing

Reverse proxies can distribute incoming requests across multiple servers, improving performance and availability.

5. Security Inspection

Proxies can inspect traffic to identify suspicious or malicious activity before it reaches users or servers.

6. TLS Termination

A reverse proxy can decrypt incoming HTTPS traffic, inspect it, and then securely forward it to backend servers.

This helps simplify certificate management and improve performance.

Proxy vs VPN
Feature	Proxy	VPN
Scope	Usually specific applications or services	Entire device/network traffic
Encryption	Not always	Yes (typically)
Primary Purpose	Filtering, caching, inspection, control	Privacy, secure communication, remote access
Common Use	Organizations and web services	Individuals and remote employees
Hands-on Activity

Along with today's lesson, I completed a One-Month Cybersecurity Summary Report.

The report summarizes everything I learned during the first 30 days of my cybersecurity journey, including networking fundamentals, web technologies, DNS, TCP/UDP, VPNs, firewalls, NAT, passive reconnaissance, and other key concepts.

Preparing this report helped me review my progress and reinforce what I have learned over the past month.

What I Learned
A proxy server acts as an intermediary between clients and servers.
Proxies can inspect, filter, and control network traffic.
There are different proxy types designed for different purposes.
Reverse proxies are widely used to protect web servers.
Proxy servers improve performance through caching and enhance security through traffic inspection.
Reviewing and documenting my learning is an important part of continuous improvement.
Key Takeaways

✅ A proxy acts as a middleman between users and the internet.

✅ Forward proxies protect and control client traffic.

✅ Reverse proxies protect backend servers.

✅ Transparent proxies work without user configuration.

✅ Proxies can perform content filtering, caching, load balancing, security inspection, anonymization, and TLS termination.

✅ Regularly documenting progress helps reinforce learning.

Reflection

Today's lesson helped me understand the important role proxy servers play in modern networks.

I learned that proxies are not just used for hiding IP addresses—they also improve performance, enforce security policies, inspect traffic, and protect web applications.

Completing my one-month summary report was also a great milestone. Looking back at everything I've learned over the past 30 days showed me how much my understanding of networking and cybersecurity has grown through consistent daily practice.

My biggest takeaway is:

Learning every day and documenting that knowledge is one of the best ways to build strong cybersecurity skills.

Quote of the Day

"Small lessons every day become big skills over time."

Progress Tracker
Day: 30/90
Topic: Proxy Servers
Concepts Learned: Forward Proxy, Reverse Proxy, Transparent Proxy, Content Filtering, Caching, Load Balancing, TLS Termination
Hands-on Activity: Created a One-Month Cybersecurity Summary Report
Milestone: ✅ Completed the first 30 days of my 90-day cybersecurity journey.
Status: ✅ Completed
