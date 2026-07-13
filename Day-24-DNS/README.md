Day 24 - Domain Name System (DNS)
Objective

Understand how the Domain Name System (DNS) works, learn how a domain name is resolved into an IP address, explore the DNS hierarchy, and study common DNS attacks.

Lesson of the Day

Today, I learned about the Domain Name System (DNS).

One of the simplest ways to understand DNS is:

DNS is the internet's phonebook.

Humans prefer to remember names like:

google.com

But computers communicate using IP addresses.

DNS translates human-readable domain names into the IP addresses that computers use to communicate.

Why DNS Exists

Imagine trying to remember the IP address of every website you visit.

Instead of remembering numbers, we simply remember domain names.

For example:

google.com
        ↓
DNS
        ↓
142.xxx.xxx.xxx

DNS performs this translation automatically, making the internet much easier to use.

DNS Resolution

If the required DNS record is already stored in a cache, the answer is returned quickly.

If it is not cached, the DNS resolver begins searching through the DNS hierarchy.

This process is called DNS Resolution.

The DNS Hierarchy

When the recursive resolver does not already know the answer, it follows a hierarchy.

The hierarchy can be visualized as a tree.

          Root Server
               │
         Top-Level Domain
          (.com, .org, .net)
               │
   Authoritative Name Server
               │
          Domain Record

Each level helps the resolver move closer to the correct answer.

Step 1 - Root Server

The Root Server is the starting point.

It does not know the IP address of every website.

Instead, it directs the resolver to the appropriate Top-Level Domain (TLD) server.

Example:

google.com
      ↓
Ask the .com TLD
Step 2 - Top-Level Domain (TLD) Server

The TLD server manages domains such as:

.com
.org
.net
.edu
.gov

The TLD server points the resolver toward the correct Authoritative Name Server.

Step 3 - Authoritative Name Server

The Authoritative Name Server stores the official DNS records for a domain.

It returns the correct IP address for the requested domain.

Example:

google.com
        ↓
Returns
142.xxx.xxx.xxx
Step 4 - Cache the Result

Once the resolver receives the answer:

It stores the result in its cache.
Future requests become much faster.
Fewer DNS queries are sent across the internet.

Caching improves both performance and efficiency.

The "14-Server Resolution Chain"

Today's lesson introduced the term "14-Server Resolution Chain."

This is not an official DNS standard, but rather a teaching shorthand used to explain the different systems involved in resolving a domain name.

The important idea is that many systems—including caches, recursive resolvers, root servers, TLD servers, and authoritative servers—may be involved before the final IP address is returned.

Important DNS Concepts
1. Most Traditional DNS Queries Are Unencrypted

Standard DNS queries are generally sent without encryption.

This means that someone on the network may be able to observe which domain names are being requested.

Modern technologies such as DNS over HTTPS (DoH) and DNS over TLS (DoT) help encrypt DNS traffic, but traditional DNS itself does not.

2. DNS Uses Caching

Caching is one of the reasons DNS is fast.

After a successful lookup:

The answer is stored temporarily.
Future requests are faster.
Network traffic is reduced.
3. Traditional DNS Does Not Verify Authenticity

Traditional DNS was not originally designed to verify whether a response is genuine.

Because of this, attackers may attempt to manipulate DNS responses.

Technologies such as DNSSEC were developed to help verify the authenticity of DNS records.

Common DNS Attacks
1. DNS Hijacking

In a DNS Hijacking attack, the attacker changes DNS settings so that users are redirected to malicious or fake websites instead of the legitimate destination.

2. DNS Cache Poisoning

In a DNS Cache Poisoning attack, false DNS information is inserted into a resolver's cache.

As a result, users may receive incorrect IP addresses and unknowingly visit malicious websites.

3. DNS Rebinding

DNS Rebinding is an attack where DNS responses change over time to make a browser communicate with systems it normally should not access.

This technique can sometimes be used to interact with internal network resources through a victim's browser.

Case Study - MyEtherWallet Attack (2018)

Today's lesson also mentioned the MyEtherWallet attack.

This incident demonstrated how attackers can exploit weaknesses related to DNS infrastructure to redirect users to fraudulent websites.

Users believed they were visiting the legitimate website, but some were instead redirected to a malicious page designed to steal cryptocurrency credentials.

The case highlighted how important secure DNS infrastructure is for protecting users.

DNS Resolution Flow
User
   ↓
Recursive Resolver
   ↓
Root Server
   ↓
TLD Server
   ↓
Authoritative Name Server
   ↓
IP Address Returned
   ↓
Cached for Future Requests
What I Learned
DNS translates domain names into IP addresses.
The DNS hierarchy consists of Root Servers, TLD Servers, and Authoritative Name Servers.
Recursive resolvers perform DNS lookups when the answer is not cached.
DNS caching improves speed and reduces network traffic.
Traditional DNS queries are generally unencrypted.
Traditional DNS does not verify whether responses are genuine.
DNS attacks can redirect users to malicious destinations.
Key Takeaways

✅ DNS is the internet's phonebook.

✅ It converts human-readable domain names into IP addresses.

✅ When records are not cached, recursive resolvers query:

Root Server
TLD Server
Authoritative Name Server

✅ DNS caching makes future lookups faster.

✅ Traditional DNS traffic is usually unencrypted.

✅ Common DNS attacks include:

DNS Hijacking
DNS Cache Poisoning
DNS Rebinding
Reflection

Today's lesson helped me understand how much work happens behind the scenes every time I type a website address into my browser.

I learned that DNS is not just a simple lookup service—it is a hierarchical system that efficiently translates domain names into IP addresses while using caching to improve performance.

I also realized that because DNS plays such an important role in internet communication, it becomes an attractive target for attackers. Understanding DNS attacks such as hijacking, cache poisoning, and rebinding helped me appreciate why protecting DNS infrastructure is so important.

My biggest takeaway is:

DNS makes the internet easy for humans to use by translating names into addresses, but protecting that translation process is essential for security.

Quote of the Day

"Humans remember names. Computers remember numbers. DNS connects the two."

Progress Tracker
Day: 24/90
Topic: Domain Name System (DNS)
Concepts Learned: DNS Resolution, Recursive Resolver, Root Server, TLD Server, Authoritative Name Server, DNS Caching, DNS Hierarchy
Attacks Learned: DNS Hijacking, DNS Cache Poisoning, DNS Rebinding
Case Study: MyEtherWallet DNS Attack
Key Insight: DNS translates domain names into IP addresses and uses caching to make future lookups faster, but it can also become a target for cyberattacks.
Status: ✅ Completed
