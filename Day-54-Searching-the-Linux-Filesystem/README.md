Day 54 - Searching the Linux Filesystem
Objective

Learn how to search the Linux filesystem efficiently using find and locate, understand different search criteria, and apply filesystem searching from a cybersecurity investigation perspective.

Lesson of the Day

Today, I learned about searching the Linux filesystem.

In a real investigation, an analyst may not know exactly where a suspicious file is located. Instead of manually checking every directory, Linux provides powerful commands to search the filesystem quickly.

The two main commands I learned today are:

find
locate

A simple way to remember the main difference is:

find searches for files and directories. grep searches inside files for content.

The find Command

The find command searches the filesystem for files and directories based on different conditions.

It is especially useful when an investigator needs to locate files that match specific characteristics.

Searching by Name

You can search for a file using its name.

Example:

find /home -name "report.txt"

This searches the /home directory for a file named report.txt.

Searching Using Wildcards

Wildcards allow broader searches.

For example:

find /home -name "*.log"

This searches for files ending in .log.

The * wildcard represents any number of characters.

This is useful when searching for multiple files with a common pattern.

Searching by Type

The find command can search for specific types of filesystem objects.

For example:

find /home -type f

This searches for regular files.

Directories can also be searched for using the appropriate type.

Searching by Modification Time

An investigator may want to know:

What files were changed recently?

find can search files based on their modification time.

This can be useful during investigations because recently modified files may deserve further attention.

Searching by Size

Files can also be searched based on their size.

This can help identify unusually large or small files.

For example, an analyst might search for files larger than a particular size when investigating unexpected data or storage usage.

Searching by Permissions

The filesystem can also be searched based on file permissions.

This is useful for finding files with potentially dangerous or unusual permissions.

For example, an investigator may want to identify files that are writable or executable by users who should not have those permissions.

Searching by Owner

Files can also be searched based on their owner.

This can be useful when investigating:

Suspicious user activity
Unexpected files
Files belonging to a particular account
Unauthorized changes
Combining Search Criteria

One of the most powerful features of find is the ability to combine multiple conditions.

Instead of simply asking:

"Find this file."

An investigator can ask more specific questions such as:

"Find recently modified files of a certain type, owned by a specific user, with particular permissions."

Combining criteria makes searches more precise and reduces unnecessary results.

The locate Command

Another command introduced today is:

locate

Unlike find, locate generally searches a prebuilt database/index of file names.

This makes it very fast for finding files by name.

Example:

locate report.txt

The command searches its database and returns matching file paths.

How locate Works

The basic process is:

Filesystem
     ↓
File-name database / index
     ↓
locate
     ↓
Matching file paths

Because locate uses an existing database rather than searching the filesystem directly each time, it can be much faster for simple filename searches.

However, the database may not immediately reflect the newest filesystem changes.

find vs locate
Feature	find	locate
Search method	Searches filesystem	Searches indexed database
Speed	Can be slower	Usually very fast
Search by name	✅	✅
Search by conditions	✅	Limited
Search by permissions	✅	❌
Search by modification time	✅	❌
Search by owner	✅	❌
Useful for investigations	Very useful	Useful for quick filename searches
find vs grep

This is an important distinction from today's lesson.

find

Searches the filesystem for files and directories.

Where is the file?
grep

Searches inside files for specific text or patterns.

What does the file contain?

A simple way to remember:

find = location
grep = content

These tools can also be used together during investigations.

Hunting Like an Investigator

Today's lesson connected filesystem searching with a security investigation mindset.

Instead of randomly searching files, ask specific questions.

1. What Changed Recently?

Look for recently modified files.

This can help identify unexpected changes to the system.

2. What's in Places Attackers Like?

Investigate directories and locations where suspicious or unauthorized files might be placed.

The goal is not to assume something is malicious, but to identify files that deserve further investigation.

3. What Has Dangerous Permissions?

Search for files with unusual or overly permissive permissions.

This connects directly with the Linux permissions concepts learned earlier.

4. What Does a Suspicious User Own?

Search for files owned by a particular user when investigating suspicious activity.

This can help establish what resources are associated with an account.

Investigation Mindset

The important lesson today was that commands are more useful when combined with investigative questions.

Instead of simply running commands, think:

Question
   ↓
Choose search criteria
   ↓
Search filesystem
   ↓
Review results
   ↓
Identify suspicious findings
   ↓
Investigate further

This is how technical commands become useful investigation techniques.

What I Learned
find searches the filesystem for files and directories.
Files can be searched by name.
Wildcards can be used for broader searches.
Files can be searched by type.
find can search by modification time.
Files can be searched by size.
Files can be searched by permissions.
Files can be searched by owner.
Multiple search criteria can be combined.
locate searches a prebuilt filename database.
find and locate have different strengths.
find searches for file locations, while grep searches file contents.
Key Takeaways

✅ find is a powerful filesystem investigation tool.

✅ Search criteria can make investigations more precise.

✅ locate provides fast filename searches using an index.

✅ Recently modified files can be useful during investigations.

✅ File permissions and ownership can reveal potential security concerns.

✅ find answers "Where is it?", while grep answers "What is inside it?"

Reflection

Today's lesson showed me how filesystem searching can be approached like an investigation rather than simply using commands.

Instead of manually browsing through thousands of files, I can use specific criteria to narrow down what I am looking for.

I also learned the important difference between find and grep. find helps locate files, while grep helps investigate their contents.

The most valuable part of today's lesson was learning to ask investigative questions such as what changed recently, what has dangerous permissions, and what files belong to a suspicious user.

My biggest takeaway is:

Good investigation starts with good questions, and the right search command helps find the evidence.

Quote of the Day

"Don't search randomly. Search with a question in mind."

Progress Tracker
Day: 54/90
Topic: Searching the Linux Filesystem
Commands Learned: find, locate
Search Criteria: Name, Wildcards, Type, Modification Time, Size, Permissions, Owner
Related Command: grep
Key Insight: Filesystem searches become more powerful when driven by investigative questions and combined criteria.
Status: ✅ Completed
