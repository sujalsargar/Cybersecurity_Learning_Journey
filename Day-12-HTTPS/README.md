Day 12 - Understanding HTTPS
Objective

Learn what HTTPS is, how it protects communication between a browser and a website, and understand why the padlock icon does not guarantee that a website is safe.

Lesson of the Day

Today, I learned about HTTPS (Hypertext Transfer Protocol Secure) and why it is one of the most important technologies on the modern internet.

One of the biggest misconceptions is that the padlock icon next to a website's URL means the website is safe. In reality, the padlock only means that the communication between my browser and the website is encrypted.

A malicious or phishing website can also use HTTPS.

HTTP vs HTTPS
HTTP

HTTP sends data in plain text.

This means that if someone is able to intercept the network traffic, they may be able to read information such as:

Usernames
Passwords
Messages
Other sensitive data
HTTPS

HTTPS is the secure version of HTTP.

It encrypts the communication between the browser and the web server so that only those two parties can read the data being exchanged.

Even if someone intercepts the traffic, they should not be able to understand the encrypted information.

Firesheep and Why HTTPS Became Important

In 2010, developer Eric Butler released a Firefox extension called Firesheep.

The tool demonstrated how attackers on the same Wi-Fi network could capture unencrypted session cookies and gain access to users' online accounts on websites that were not fully protected by HTTPS.

This highlighted how insecure plain HTTP communication could be.

As awareness grew:

Around 2014, a large portion of the web began adopting HTTPS.
Today, more than 95% of web traffic is protected using HTTPS.
What Does the Padlock Actually Mean?

The padlock icon tells us three important things:

1. Encryption

The communication between the browser and the server is encrypted.

2. Certificate

The website has a valid digital certificate.

3. Certificate Authority (CA)

The certificate has been issued or verified by a trusted Certificate Authority.

What the Padlock Does NOT Mean

The padlock does not guarantee that:

The website is trustworthy.
The content is legitimate.
The website is free from malware.
The website is not a phishing page.

A phishing website can also have a valid HTTPS certificate.

Can a Man-in-the-Middle Read HTTPS Traffic?

Generally, no.

HTTPS encryption prevents an attacker on the network from reading the communication between the browser and the server.

However, attackers may still compromise users through other methods, such as:

Phishing websites
Malware
Stolen credentials
Compromised devices

This means that encryption protects the communication, but it does not automatically make the website or the device safe.

What I Learned
HTTP sends data in plain text.
HTTPS encrypts communication between the browser and the server.
The padlock icon means the connection is encrypted, not that the website is trustworthy.
Digital certificates help verify the identity of websites.
HTTPS greatly improves privacy and security, but users must still stay alert for phishing and other threats.
Key Takeaways

✅ HTTP sends data without encryption.

✅ HTTPS encrypts communication between the browser and the server.

✅ The padlock indicates an encrypted connection.

✅ HTTPS does not guarantee that a website is safe or legitimate.

✅ Always verify the website's domain before entering sensitive information.

Reflection

Today's lesson helped me understand the real purpose of HTTPS. Before this, I assumed the padlock icon meant a website was completely safe. Now I know that it only confirms that the connection is encrypted.

This lesson reminded me that cybersecurity is not just about using secure technologies but also about staying aware of threats like phishing and fake websites. HTTPS protects data in transit, but users must still verify who they are communicating with.

Quote of the Day

"HTTPS protects the conversation, not the intentions of the website."

Progress Tracker
Day: 12/90
Topic: HTTPS
Concepts Learned: HTTP, HTTPS, Encryption, Digital Certificates, Certificate Authorities, Firesheep
Key Insight: The padlock icon means the connection is encrypted—not that the website is automatically safe.
Status: ✅ Completed
