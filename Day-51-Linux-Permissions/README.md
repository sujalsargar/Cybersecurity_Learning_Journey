Day 51 - Linux Permissions
Objective

Understand how Linux permissions protect files and directories, learn the three basic permission types, understand users and groups, and learn how chmod and chown are used to manage access.

Lesson of the Day

Today, I learned about Linux File Permissions, one of the most important concepts for system security.

Linux assigns permissions to files and directories to control who can access them and what they can do.

A simple way to remember today's lesson is:

Permissions decide who can read, write, or execute a file.

These permissions help protect private information, applications, configuration files, and important system resources.

Viewing Permissions with ls -l

The command:

ls -l

shows detailed information about files and directories, including their permissions.

Example:

-rwxr-xr--

The permission string contains 10 characters.

Understanding the 10 Characters

The permission format can be divided into four parts:

- rwx r-x r--
│ │   │   │
│ │   │   └── Other permissions
│ │   └────── Group permissions
│ └────────── User/Owner permissions
└──────────── File type
1st Character – File Type

The first character indicates the type of filesystem object.

For example:

-   Regular file
d   Directory
Next 3 Characters – User

These permissions belong to the owner of the file.

Example:

rwx
Next 3 Characters – Group

These permissions apply to members of the file's assigned group.

Example:

r-x
Last 3 Characters – Other

These permissions apply to everyone else.

Example:

r--
Three Basic Permissions

Linux has three fundamental permissions:

Read (r)

Allows a user to view or read the contents of a file.

For a directory, read permission allows the user to view its contents.

Write (w)

Allows a user to modify or change a file.

Depending on the permissions of a directory, write access can also allow files within it to be created, modified, or deleted.

Execute (x)

For a file, execute permission allows it to be run as a program or script.

For a directory, execute permission allows a user to enter/access it using cd and access items within it, subject to other permissions.

Three Permission Groups

Linux permissions are assigned to three categories of users.

1. User

The owner of the file.

2. Group

A group of users who share a set of permissions.

3. Other

Everyone else who is not the owner and is not part of the relevant group.

Example

Consider:

-rwxr-xr--

This means:

Category	Permissions
User	rwx
Group	r-x
Other	r--

So:

The owner can read, write, and execute.
The group can read and execute.
Others can only read.
Principle of Least Privilege

One of the most important security concepts from today's lesson is the Principle of Least Privilege.

It means:

Give users and programs only the permissions they actually need—and no more.

For example, if a user only needs to read a file, there is no reason to give them write or execute permissions.

Excessive permissions can increase the impact of a security incident.

Changing Permissions with chmod

The chmod command is used to change file and directory permissions.

Example:

chmod +x script.sh

This adds execute permission to the file.

Permissions can also be changed using numeric values.

Numeric Permissions

Linux permissions can be represented using numbers:

Permission	Value
Read (r)	4
Write (w)	2
Execute (x)	1

These values can be combined.

For example:

rwx = 4 + 2 + 1 = 7
r-x = 4 + 0 + 1 = 5
r-- = 4 + 0 + 0 = 4

Therefore:

rwxr-xr--

can be represented numerically as:

754
Changing Ownership with chown

The chown command is used to change the owner of a file or directory.

It can also be used to change the associated group.

Example:

chown user file.txt

Ownership management is important because Linux permissions depend on the relationship between:

Owner
Group
Other users
Why Linux Permissions Matter in Cybersecurity

Incorrect permissions can create security weaknesses.

For example:

Sensitive files may become readable by unauthorized users.
Important scripts may become writable by untrusted users.
Executable files may be modified.
Configuration files may be exposed.
Excessive privileges can increase the impact of an attack.

Therefore, understanding permissions is essential for securing Linux systems.

What I Learned
Linux assigns permissions to files and directories.
ls -l can be used to view permissions.
Permissions include Read (r), Write (w), and Execute (x).
Permissions are assigned to User, Group, and Other.
The first character in a permission string represents the file type.
chmod changes file and directory permissions.
Permissions can be represented using numeric values.
chown changes file ownership and can also change the group.
Least privilege means giving only the permissions that are actually required.
Key Takeaways

✅ Linux permissions are an important security boundary.

✅ r, w, and x control what users can do.

✅ Permissions are divided between User, Group, and Other.

✅ chmod manages permissions.

✅ chown manages ownership.

✅ Numeric permissions make permission management easier.

✅ Least privilege reduces unnecessary access and improves security.

Reflection

Today's lesson helped me understand how Linux controls access to files and directories.

Before learning permissions, a file might simply look like something stored on a computer. Now I understand that every file can have a defined access policy controlling who can read, modify, or execute it.

The concept of least privilege was especially important because it connects directly with cybersecurity. Giving unnecessary permissions can create security risks, while limiting access to only what is required helps reduce those risks.

My biggest takeaway is:

Security is not only about protecting a system from external attackers—it is also about controlling what users and programs are allowed to do inside the system.

Quote of the Day

"Give only the access that is needed, nothing more."

Progress Tracker
Day: 51/90
Topic: Linux Permissions
Concepts Learned: File Permissions, User, Group, Other, Read, Write, Execute, Least Privilege, chmod, Numeric Permissions, chown
Commands Covered: ls -l, chmod, chown
Key Insight: Proper permissions and least privilege are fundamental to securing Linux systems.
Status: ✅ Completed
