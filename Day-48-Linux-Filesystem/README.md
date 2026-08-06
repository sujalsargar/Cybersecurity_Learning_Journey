Day 48 - Linux Filesystem
Objective

Understand how the Linux filesystem is organized, learn the purpose of important system directories, and understand how Linux uses paths to locate files and directories.

Lesson of the Day

Today, I learned about the Linux Filesystem, which is one of the most fundamental concepts for working with Linux.

Unlike Windows, which separates storage into different drives such as C: and D:, Linux organizes everything under a single directory tree.

A simple way to remember today's lesson is:

Everything in Linux begins from a single root directory (/).

Understanding the filesystem makes it much easier to navigate Linux, locate files, and manage the operating system.

Linux Filesystem Structure

Linux uses a tree-like directory structure.

At the very top of the tree is the Root Directory, represented by:

/

Every file and directory on the system exists somewhere beneath this root directory.

Example:

/
├── home
├── etc
├── var
├── usr
├── bin
├── sbin
├── tmp
├── root
├── dev
└── proc

Unlike Windows, Linux does not create separate directory trees for different drives.

Root Directory vs Root User

Today's lesson also clarified an important difference.

Root Directory (/)

The Root Directory is the highest directory in the Linux filesystem.

It is the starting point for every file and folder.

Root User

The Root User is the administrator account in Linux.

The root user has full control over the operating system and can access or modify almost every file and setting.

Although they share the word "root," the Root Directory and the Root User are two different concepts.

Standard Linux Directories

Linux follows a standard directory structure, where each top-level directory has a specific purpose.

/home

Stores the personal files and folders of regular users.

Example:

/home/sujal

Each user typically has their own home directory.

/etc

Contains system configuration files and software configuration settings.

Administrators often modify files in this directory when configuring the system.

/var

Stores data that changes while the system is running.

Examples include:

Log files
Cache files
Mail queues
Application data
/usr

Contains user applications, libraries, documentation, and shared resources.

Many installed programs are located here.

/bin

Stores essential command-line programs used by all users.

Examples include commands such as:

ls
cp
mv
cat
/sbin

Contains important system administration commands.

These commands are generally used by administrators for system management.

/tmp

Stores temporary files created by applications and the operating system.

These files are usually removed automatically after a reboot or after some time.

/root

This is the home directory of the root user.

It is different from the Root Directory (/).

Understanding Paths

Linux uses paths to describe the location of files and directories.

Today's lesson covered two types of paths.

1. Absolute Path

An Absolute Path always starts from the Root Directory (/).

Example:

/home/sujal/Documents/report.txt

No matter where you are currently working, this path always refers to the same file.

2. Relative Path

A Relative Path describes a location relative to the current working directory.

Example:

Documents/report.txt

Its meaning depends on your current location in the filesystem.

Special Directory Symbols

Linux provides two useful symbols for navigating directories.

. (Current Directory)

The single dot (.) represents the current directory.

Example:

.
.. (Parent Directory)

The double dot (..) represents the parent directory.

Example:

..

It allows users to move one level up in the directory tree.

Special System Directories

Today's lesson also introduced two important system directories.

/dev

The /dev directory contains device files.

Linux treats hardware devices such as:

Hard drives
USB devices
Keyboards
Mice

as special files located inside /dev.

/proc

The /proc directory contains information about:

Running processes
System status
Kernel information

It provides a virtual view of the system and is commonly used for system monitoring and troubleshooting.

Why the Filesystem Matters

Understanding the Linux filesystem helps users:

Navigate the operating system.
Locate important files.
Configure software.
Manage user data.
Troubleshoot Linux systems.
Work efficiently from the command line.

This knowledge forms the foundation for many advanced Linux and cybersecurity tasks.

What I Learned
Linux organizes files using a single directory tree.
Everything starts from the Root Directory (/).
The Root Directory and Root User are different concepts.
Standard directories each serve a specific purpose.
Linux supports both Absolute and Relative paths.
. represents the current directory.
.. represents the parent directory.
Device information is stored in /dev, while process information is available through /proc.
Key Takeaways

✅ Linux uses one unified filesystem instead of separate drive letters.

✅ Every file begins somewhere under the Root Directory.

✅ Standard directories have specific roles.

✅ Absolute paths always begin with /.

✅ Relative paths depend on the current directory.

✅ Understanding the filesystem makes Linux navigation much easier.

Reflection

Today's lesson helped me understand how Linux organizes its files and directories.

I learned that Linux uses a single hierarchical filesystem rather than separate drive letters like Windows. Understanding directories such as /home, /etc, /var, and /proc gave me a much clearer picture of where different types of files are stored.

Learning about absolute and relative paths also helped me understand how Linux locates files and why navigation is an essential skill when working from the command line.

My biggest takeaway is:

Once you understand the Linux filesystem, navigating and managing the operating system becomes much more logical and efficient.

Quote of the Day

"In Linux, every file has a place—and every path begins at the root."

Progress Tracker
Day: 48/90
Topic: Linux Filesystem
Concepts Learned: Root Directory, Root User, Standard Directories, Absolute Path, Relative Path, Special Symbols (. and ..), /dev, /proc
Key Insight: Understanding the Linux filesystem is the foundation for navigating, managing, and securing Linux systems.
Status: ✅ Completed
