Day 53 - Reading Files in Linux
Objective

Learn how to read, inspect, and search files in Linux using command-line tools, with a focus on how these skills are used during cybersecurity investigations.

Lesson of the Day

Today, I learned about reading files in Linux.

A large part of Linux investigation involves finding and reading the right information from files.

In Linux, many important things are represented as files, including:

Logs
Configuration files
Process information
System information
Application data
Security-related information

For a cybersecurity analyst, knowing which file to investigate and how to quickly find useful information inside it is an important skill.

A simple way to remember today's lesson is:

Investigations often begin by finding the right file and reading the right information from it.

Common File Reading Tools

Different Linux commands are useful for different investigation requirements.

Today's lesson covered:

Command	Purpose
cat	Read the contents of a file
less	Read a file page by page
head	View the beginning of a file
tail	View the end of a file
tail -f	Continuously monitor new content
grep	Search for specific text or patterns
1. cat

The cat command can display the contents of a file.

Example:

cat file.txt

It is useful when the file is relatively small and you want to quickly view its contents.

2. less

The less command allows you to read a file page by page.

Example:

less logfile.txt

This is especially useful for large files because you do not have to load the entire contents into the terminal at once.

It is commonly useful when investigating large log files.

3. head

The head command displays the beginning of a file.

Example:

head logfile.txt

It is useful when you want to quickly understand how a file begins.

4. tail

The tail command displays the end of a file.

Example:

tail logfile.txt

This can be useful when the newest information is located near the end of a log file.

5. tail -f

One particularly useful command for security monitoring is:

tail -f logfile.txt

The -f option means follow.

It continuously displays new lines added to the file.

This can be useful for monitoring logs in real time.

For example, an analyst could monitor a log while a system is actively generating events.

6. grep

The grep command is one of the most useful tools for searching text in Linux.

Instead of reading an entire file, an analyst can search for a specific word or pattern.

Example:

grep "error" logfile.txt

This searches the file for lines containing the word error.

Useful grep Options

Today's lesson also introduced several useful grep options.

-i – Ignore Case
grep -i "error" logfile.txt

This ignores uppercase and lowercase differences.

For example, it can match:

error
Error
ERROR
-n – Show Line Numbers
grep -n "failed" logfile.txt

This displays the line number where the matching text was found.

This makes it easier to locate the information inside the original file.

-r – Recursive Search
grep -r "password" /directory/

The -r option searches through files in a directory and its subdirectories.

This is useful when you don't know exactly which file contains the information you are looking for.

-c – Count Matches
grep -c "failed" logfile.txt

This counts the number of matching lines.

This can be useful when trying to understand how frequently a particular event occurred.

-v – Show Non-Matching Lines
grep -v "success" logfile.txt

The -v option shows lines that do not match the specified pattern.

This can be useful when filtering out information you are not interested in.

Using File Reading for Cybersecurity Investigation

These commands become especially useful when investigating Linux systems.

An analyst might need to:

Find errors in log files
grep "error" logfile.txt
Search for failed login attempts
grep -i "failed" logfile.txt
Find a specific username
grep "username" logfile.txt
Search for a configuration setting
grep "setting" config.txt
Search multiple files
grep -r "failed" /var/log/

These simple commands can save significant time during an investigation.

Why File Reading Matters in Cybersecurity

During a security investigation, analysts often need to answer questions such as:

What happened?
When did it happen?
Which user was involved?
What system generated the event?
Were there failed login attempts?
Were there errors?
What changed?
Is suspicious activity still occurring?

The answers may already exist inside system and application files.

The challenge is knowing where to look and how to find the relevant information efficiently.

What I Learned
Linux investigations often involve reading files.
Logs, configuration files, and system information can provide valuable evidence.
cat displays file contents.
less allows page-by-page reading.
head shows the beginning of a file.
tail shows the end of a file.
tail -f monitors new content in real time.
grep searches for specific words or patterns.
grep -i ignores case.
grep -n displays line numbers.
grep -r searches recursively.
grep -c counts matching lines.
grep -v displays non-matching lines.
Key Takeaways

✅ Knowing how to read files is an essential Linux skill.

✅ Logs can contain valuable information during security investigations.

✅ grep makes searching large amounts of text much faster.

✅ tail -f can be useful for real-time log monitoring.

✅ Command-line tools allow analysts to quickly filter large amounts of information.

Reflection

Today's lesson showed me that cybersecurity investigation is not always about using complicated security tools.

Sometimes, the most important evidence is already available in a system's files.

Learning commands such as cat, less, head, tail, and especially grep gives an analyst the ability to quickly find useful information inside large amounts of data.

I also learned that reading files efficiently is an important foundation for later topics such as log analysis, incident investigation, SIEM, and digital forensics.

My biggest takeaway is:

A good investigator doesn't read everything—they know where to look and how to find what matters.

Quote of the Day

"Don't search everything manually. Learn how to find what matters."

Progress Tracker
Day: 53/90
Topic: Reading Files in Linux
Concepts Learned: cat, less, head, tail, tail -f, grep
Grep Options: -i, -n, -r, -c, -v
Practical Focus: Reading and searching Linux files and logs
Key Insight: Efficient file reading and searching are fundamental skills for Linux investigation and cybersecurity analysis.
Status: ✅ Completed
