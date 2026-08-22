Day 63 - SSH (Secure Shell)
Objective

Understand SSH, learn how it provides secure remote access to Linux systems, understand password and key-based authentication, and learn why SSH is an essential tool in cybersecurity.

Lesson of the Day

Today, I learned about SSH (Secure Shell).

SSH is a protocol that allows you to connect to and control another computer over a network.

It is one of the most important tools used for remote Linux administration and cybersecurity work.

A simple way to remember today's lesson is:

SSH lets you securely control a remote computer from your own computer.

What is SSH?

SSH stands for Secure Shell.

It allows a user to establish an encrypted connection to another computer over a network.

SSH encrypts communication between the client and server, including:

Commands
Passwords
Data
Other session information

This makes SSH suitable for securely managing remote systems.

Why SSH is Important

SSH is commonly used for:

Remote Linux administration
Server management
Cloud administration
Security investigations
Incident response
Secure file transfers

Instead of physically accessing a server, an administrator can securely connect to it remotely.

SSH Client-Server Model

SSH uses a client-server model.

Your Computer
     ↓
 SSH Client
     ↓
 Encrypted Connection
     ↓
 SSH Server
     ↓
Remote Computer

The:

SSH Client initiates the connection.
SSH Server accepts and manages the remote connection.
Basic SSH Command

The basic SSH command is:

ssh username@server_address

For example:

ssh user@192.168.1.10

The command tells SSH:

Which user should log in.
Which remote computer should be contacted.
What Happens After Authentication?

Once authentication is successful, you receive a shell on the remote system.

An important concept is:

Commands entered after connecting are executed on the remote machine, not your local computer.

For example:

Your Computer
     ↓
SSH Connection
     ↓
Remote Linux Server
     ↓
Commands execute here

This is why SSH is so useful for remote administration.

Ending an SSH Session

When you finish working on the remote machine, you can end the session using:

exit

or:

logout

This closes the remote shell and returns you to your local machine.

SCP - Secure File Transfer

SSH can also be used to securely transfer files.

SCP (Secure Copy Protocol) allows files to be transferred over an SSH connection.

It provides encrypted file transfers between systems.

This makes it useful when administrators need to securely move files between computers.

SSH Authentication

Today's lesson covered two major SSH authentication methods:

Password Authentication
SSH Key Authentication
1. Password Authentication

A user can authenticate using a username and password.

Example:

Username
   +
Password
   ↓
Authentication
   ↓
SSH Access

However, weak passwords can become a major security risk.

If an SSH server is exposed to the internet and uses weak credentials, attackers may attempt to compromise the account.

2. SSH Key Authentication

SSH also supports key-based authentication.

It uses two related keys:

Public Key

The public key can be placed on the remote server.

Private Key

The private key remains on your own computer.

The important security principle is:

The private key should never leave your machine.

How SSH Keys Work

A simplified view is:

Your Computer
   │
   ├── Private Key 🔑
   │
   └── Public Key
          ↓
     Remote Server

The server uses the public key to verify that the connecting user possesses the corresponding private key.

The private key itself is not sent to the server.

Why SSH Keys Are Preferred

Key-based authentication is generally preferred in professional environments because properly managed keys can provide strong authentication without relying on reusable passwords.

They are also designed to be resistant to ordinary password-guessing approaches.

However, private keys must be protected carefully.

If an attacker obtains a usable private key, they may be able to authenticate as the associated user depending on the server's configuration and other security controls.

SSH and Cybersecurity

SSH is extremely important in cybersecurity because security professionals frequently need to access remote systems.

It is useful for:

Remote Management

Administrators can securely manage servers from another location.

Incident Response

Security teams can connect to affected systems to investigate incidents.

Security Investigation

Analysts can inspect processes, logs, network connections, and files on remote Linux systems.

Cloud Security

Many cloud-based Linux servers are managed remotely through SSH.

Security Mindset

Today's lesson also reinforced an important principle:

The more powerful the access point, the more securely it must be protected.

SSH can provide powerful control over a remote system.

Therefore, SSH access should be carefully secured.

Important considerations include:

Strong authentication
Secure SSH keys
Protecting private keys
Strong passwords where passwords are enabled
Limiting unnecessary access
Monitoring authentication activity
Keeping the SSH service updated
What I Learned
SSH stands for Secure Shell.
SSH provides encrypted remote access to another computer.
SSH uses a client-server model.
The basic connection format is ssh username@server_address.
Commands entered after connecting execute on the remote machine.
exit or logout ends the SSH session.
SCP can securely transfer files over SSH.
SSH supports password authentication.
SSH also supports public/private key authentication.
The private SSH key should remain protected on the user's machine.
Weak SSH passwords can create serious security risks.
SSH is fundamental to remote administration, incident response, and security investigation.
Key Takeaways

✅ SSH provides encrypted remote access.

✅ The SSH client connects to an SSH server.

✅ Remote commands execute on the remote system.

✅ SCP can securely transfer files.

✅ SSH keys provide an important alternative to password authentication.

✅ Private keys must be protected.

✅ SSH access should be secured carefully because it can provide powerful system access.

Reflection

Today's lesson helped me understand how cybersecurity professionals securely manage systems that they cannot physically access.

SSH is much more than just a remote login tool. It provides a secure way to administer Linux servers, investigate incidents, transfer files, and manage cloud systems.

The difference between password authentication and SSH key authentication was especially important. I learned that key-based authentication can provide stronger security when keys are properly managed, while weak SSH passwords can expose remote systems to attack.

My biggest takeaway is:

Remote access is powerful, so it must be protected with strong authentication and careful access control.

Quote of the Day

"The more powerful the access, the more carefully it must be protected."

Progress Tracker
Day: 63/90
Topic: SSH - Secure Shell
Concepts Learned: SSH, Client-Server Model, Remote Access, SCP, Password Authentication, SSH Keys
Commands Learned: ssh, exit, logout
Key Security Concept: Protecting powerful remote access
Key Insight: SSH is a fundamental tool for secure remote administration and cybersecurity investigations.
Status: ✅ Completed
