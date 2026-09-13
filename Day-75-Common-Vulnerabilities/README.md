Day 75 – Common Vulnerabilities
🎯 Objective

To understand common software vulnerabilities, why they happen, how attackers exploit them, and the basic security practices used to prevent them.

📚 Lesson of the Day

A vulnerability is a weakness in a system, application, or process that an attacker can exploit.

During the Exploitation stage of the Cyber Kill Chain, attackers use vulnerabilities to gain unauthorized access or perform malicious actions.

Some common and well-known vulnerabilities include:

Injection
Cross-Site Scripting (XSS)
Remote Code Execution (RCE)

These vulnerabilities have existed for many years, but they still appear in modern software.

🔓 What Is a Vulnerability?

A vulnerability is a weakness that can be exploited by an attacker.

Simple Example

Imagine a door with a broken lock.

Weak Lock
    ↓
Vulnerability
    ↓
Attacker Exploits It
    ↓
Unauthorized Access

In software, the weakness may be caused by poor input handling, outdated components, insecure coding, or incorrect security controls.

⚠️ The Common Root Cause: Trusting Untrusted Input

One important lesson is that many vulnerabilities happen because an application trusts input that comes from an untrusted user.

User input should normally be treated as data.

But an insecure application may accidentally treat that input as:

A command
Executable code
A database query
Trusted content

This can allow an attacker to manipulate how the application behaves.

Simple Rule

User input should be treated as data, not instructions.

💉 1. Injection

Injection occurs when an application mixes untrusted user input directly with commands or queries.

Instead of treating the input as ordinary data, the application may interpret part of it as instructions.

Injection is one of the most common and dangerous classes of vulnerabilities.

SQL Injection

SQL Injection occurs when an attacker manipulates a database query using specially crafted input.

If an application does not safely handle user input, an attacker may be able to interfere with the database query.

Possible Impact

SQL Injection can potentially allow an attacker to:

Bypass login controls
Read sensitive information
Modify database data
Delete database data
Root Cause
Untrusted User Input
        ↓
Application Trusts Input
        ↓
Input Becomes Part of Query
        ↓
Database Query Is Manipulated
Prevention

The main principle is:

Keep user input separate from database commands and always treat input as data.

Secure development practices such as parameterized queries/prepared statements help prevent SQL injection.

🌐 2. Cross-Site Scripting (XSS)

Cross-Site Scripting (XSS) is a vulnerability where malicious code can be executed in another user's web browser through a vulnerable website or web application.

The attacker tries to make the application treat malicious input as executable web content instead of ordinary data.

Possible Impact

XSS can potentially allow attackers to:

Steal session information
Perform actions as the victim
Redirect users to malicious websites
Manipulate content shown in the victim's browser
Root Cause

The application does not properly handle or encode untrusted input before displaying it in a web page.

Prevention

The basic principle is:

Treat user input as plain text, not executable code.

Important defenses include proper output encoding, input validation, and appropriate browser security controls.

💻 3. Remote Code Execution (RCE)

Remote Code Execution (RCE) is a particularly serious vulnerability because it can allow an attacker to execute their own code on a remote system without authorization.

If successfully exploited, RCE can give an attacker significant control over the affected system.

Possible Impact

An attacker may potentially:

Run unauthorized commands
Access sensitive information
Change system files
Install malicious software
Use the compromised system for further attacks
Why Is RCE Dangerous?

The impact depends on the affected application and the privileges available to the attacker.

Remote Vulnerability
        ↓
Attacker Exploits It
        ↓
Unauthorized Code Execution
        ↓
System Compromise
Prevention

Important defenses include:

Handle input safely
Use secure memory-management practices
Keep software patched
Remove or reduce unnecessary privileges
Monitor for unusual behavior
📊 Comparison of Common Vulnerabilities
Vulnerability	Basic Meaning	Possible Impact	Main Prevention
Injection	Input becomes part of a command/query	Data access or modification	Separate input from commands
XSS	Malicious content runs in a user's browser	Session abuse, redirects, impersonation	Treat input as data and encode output
RCE	Attacker executes code remotely	Potential system compromise	Safe input/memory handling and quick patching
🛡️ Why Do These Vulnerabilities Still Exist?

These vulnerabilities are not new. Many have been known for decades, and their basic prevention methods are also well understood.

So why do they continue to appear?

1. Software Is Large and Complex

Modern applications contain thousands or millions of lines of code.

The larger the system, the harder it is to identify every possible weakness.

2. Many Developers Work on the Same Software

Large applications are often developed by many people.

Different developers may have different levels of security knowledge and coding experience.

3. Software Changes Over Time

Applications are continuously updated with:

New features
New libraries
New APIs
New integrations
New functionality

A previously secure application can introduce a new vulnerability after a change.

4. Old Code Remains in Use

Some applications contain code that was written many years ago.

Older code may not follow modern secure development practices.

5. Security Can Be Missed During Development

Developers may focus mainly on making a feature work.

If security is not considered throughout development, vulnerabilities can be introduced.

🔗 Connection to the Cyber Kill Chain

Day 75 connects directly to the Exploitation stage that I studied earlier.

Reconnaissance
      ↓
Weaponization
      ↓
Delivery
      ↓
🔴 Exploitation ← Vulnerability Used Here
      ↓
Installation
      ↓
Command & Control
      ↓
Actions on Objectives

An attacker may discover a vulnerability during reconnaissance or other preparation stages and then use it during exploitation.

This shows why vulnerability management and patching are important defensive controls.

🛡️ Basic Security Principles

The vulnerabilities studied today show some simple but powerful security principles:

Injection

Separate data from commands.

XSS

Do not allow untrusted input to become executable content.

RCE

Handle input and system resources safely and patch vulnerabilities quickly.

General Principle

Never blindly trust untrusted input.

🧠 What I Learned
A vulnerability is a weakness that an attacker can exploit.
Vulnerabilities are commonly used during the exploitation stage of an attack.
Injection happens when untrusted input is incorrectly treated as part of a command or query.
SQL Injection can affect database confidentiality and integrity.
XSS can cause malicious content to execute in another user's browser.
RCE can allow unauthorized code execution on a remote system.
Many vulnerabilities are caused by incorrectly trusting untrusted input.
Secure input handling is an important defense.
Software should be regularly patched and updated.
Vulnerabilities continue to exist because modern software is large, complex, and continuously changing.
🔑 Key Takeaways
Easy Memory

Vulnerability = Weakness

Injection = Input becomes instructions

XSS = Malicious code in the browser

RCE = Attacker runs code remotely

Golden Rule

Treat untrusted input as data, not instructions.

💭 Reflection

Today I learned that many serious vulnerabilities come from a simple mistake: trusting something that should not be trusted.

The interesting part is that the solutions to many common vulnerabilities are already well known. The challenge is consistently applying secure practices to large and constantly changing software systems.

This helped me understand why secure coding, patching, input handling, and continuous security testing are so important.

💬 Quote of the Day

“Never trust input you do not control.”

📈 Progress Tracker

Day 75 / 90 Completed ✅

75 days of learning. 15 days remaining.

Current Focus: Cybersecurity Fundamentals → Vulnerabilities → Exploitation → Secure Development
