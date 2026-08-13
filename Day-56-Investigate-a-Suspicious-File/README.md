Day 56 - Investigate a Suspicious File
Objective

Learn how to investigate a suspicious file systematically, understand what a file or script is trying to do, and make an evidence-based security verdict.

Lesson of the Day

Today, I learned how to investigate a suspicious file like a cybersecurity analyst.

When an analyst finds an unknown or suspicious file, the goal is not to immediately assume that it is malicious.

Instead, the file should be examined carefully and the verdict should be based on evidence.

The four main questions to ask are:

What kind of file is it?
What are its properties?
What's inside it?
Is there anything suspicious inside it?
Investigation Order

A basic investigation workflow I learned today is:

file
  ↓
ls -l
  ↓
cat / less / strings
  ↓
grep
  ↓
Analysis
  ↓
Verdict

Each step helps answer a different question about the file.

1. file – What Kind of File Is It?

The file command identifies the type of a file.

Example:

file suspicious_file

This helps determine whether the file is:

A text file
A script
An executable
An archive
An image
Another type of file

The file extension alone should not always be trusted.

2. ls -l – What Are Its Properties?

The ls -l command provides detailed information about a file.

Example:

ls -l suspicious_file

It can help investigate:

File permissions
File owner
Group
File size
Modification time

These properties can provide useful context during an investigation.

3. Read the File

After identifying the file, the next step is to examine its contents.

Depending on the file, commands such as:

cat suspicious_file

or:

less suspicious_file

can be used.

For some files, strings can help identify readable text contained inside them.

Example:

strings suspicious_file

The goal is to understand what the file contains without making assumptions.

4. Search the Contents

grep can be used to search for specific words or patterns.

Example:

grep "command" suspicious_file

This can help quickly locate interesting lines inside a large text file.

Reading a Script Like an Investigation

A script is essentially a text file containing commands that can be executed by the system.

Instead of simply reading it as normal text, an analyst should ask:

What is each command trying to do?

A safe script might:

Back up files
Print messages
Automate repetitive tasks
Organize files
Perform routine system operations

But a suspicious script may contain commands that perform unexpected or harmful actions.

Questions to Ask While Reading a Script

For every important line, ask:

What is the command trying to do?

Understand the purpose of the command.

Should a legitimate script be doing this?

Compare the command with the expected purpose of the script.

Does the script access sensitive information?

Look for actions involving important files, credentials, or system information.

Does it make unexpected changes?

Look for commands that modify files, permissions, configurations, or system behaviour.

The key is to understand the intent and behaviour of the script.

Reaching a Verdict

After investigating the file, an analyst should provide an honest verdict based on the available evidence.

There are three useful verdict categories:

1. Benign

The file may initially appear suspicious, but investigation shows that it performs a legitimate task.

Example:

A script automatically backs up a specific folder as expected.

Verdict:

Benign — the file performs a legitimate and expected function.

2. Suspicious

The file contains concerning behaviour, but there is not enough evidence to confirm that it is malicious.

Verdict:

Suspicious — the file contains concerning behaviour, but additional evidence is required to confirm malicious activity.

3. Malicious

The file clearly performs harmful actions, and there is specific evidence supporting the conclusion.

Verdict:

Malicious — the file performs harmful actions supported by clear evidence.

Evidence-Based Analysis

One of the most important lessons today was:

Base your verdict on evidence, not guesses.

An analyst should be able to explain:

What was observed
Why it is suspicious
What evidence supports the conclusion
What should happen next

A strong investigation does not simply say:

"This file looks dangerous."

Instead, it explains why the file is dangerous or why it appears legitimate.

Recommendation Based on the Verdict

The recommendation should depend on the investigation result.

Benign
Document the findings.
Continue normal monitoring if necessary.
Suspicious
Do not execute the file unnecessarily.
Preserve the file for further investigation.
Collect additional evidence.
Escalate if required.
Malicious
Isolate or contain the affected system according to the incident response process.
Preserve evidence.
Escalate the incident.
Investigate related systems and activity.
What I Learned
Suspicious files should be investigated systematically.
The file type should be identified first.
File properties such as permissions, ownership, size, and timestamps provide useful context.
File contents should be examined carefully.
cat, less, strings, and grep can help investigate files.
Scripts should be read line by line.
Every command in a script should be understood before deciding whether its behaviour is legitimate.
A verdict should be based on evidence.
Files can be classified as Benign, Suspicious, or Malicious.
Recommendations should be based on the final verdict.
Key Takeaways

✅ Don't immediately assume that a suspicious file is malicious.

✅ Investigate systematically.

✅ Understand what the file is and what it contains.

✅ Read scripts line by line and understand their commands.

✅ Ask what the command is trying to accomplish.

✅ Base the final verdict on evidence rather than assumptions.

Reflection

Today's lesson helped me understand how a cybersecurity analyst approaches a suspicious file.

The most important part is not simply finding something that looks unusual. The analyst needs to investigate the file, understand its properties and contents, determine what it is actually trying to do, and then make a justified decision.

I learned that "suspicious" and "malicious" are not always the same thing. A file can contain unusual behaviour without having enough evidence to prove that it is malicious.

My biggest takeaway is:

Investigate first, understand the evidence, and then make the verdict.

Quote of the Day

"Don't guess. Investigate, collect evidence, and then decide."

Progress Tracker
Day: 56/90
Topic: Investigating a Suspicious File
Commands Learned: file, ls -l, cat, less, strings, grep
Investigation Focus: File type, properties, contents, suspicious behaviour, verdict
Verdicts: Benign, Suspicious, Malicious
Key Insight: Security decisions should be based on evidence, not assumptions.
Status: ✅ Completed
