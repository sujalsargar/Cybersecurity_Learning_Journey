Day 61 - Your First Bash Script
Objective

Learn the basics of Bash scripting, understand how scripts automate command-line tasks, and learn the basic requirements for making a Bash script executable.

Lesson of the Day

Today, I learned about Bash scripting and created my first Bash script.

A script is simply a plain text file containing commands that are executed from top to bottom.

Instead of typing the same commands manually every time, a script can run them automatically in the correct order.

A simple way to remember today's lesson is:

A script turns a sequence of commands into an automated task.

What is a Script?

A script is a text file containing commands that a shell can execute.

For example, instead of manually running several commands:

command1
command2
command3

we can place them inside a script and execute the script.

The commands are generally processed from top to bottom, in the order they appear.

Why Use Scripts?

Scripts are useful for automation.

They can:

Automate repetitive tasks.
Save time.
Reduce manual errors.
Run multiple commands in sequence.
Make tasks easier to repeat.
Help standardize routine activities.

For cybersecurity professionals, scripting is especially useful for automating investigation, system administration, monitoring, and repetitive security tasks.

What Makes a Bash Script Runnable?

Today's lesson introduced three important things required to make a Bash script executable.

1. Shebang

A Bash script commonly begins with a shebang:

#!/bin/bash

It tells the operating system which interpreter should be used to execute the script.

In this case, the script is intended to be interpreted by Bash.

2. Commands

The script contains the commands that should be executed.

For example:

#!/bin/bash


echo "Hello, Cybersecurity!"
pwd
ls

When the script runs, these commands are executed in order.

3. Execute Permission

A script also needs the appropriate execute permission if you want to run it directly.

The chmod command can be used:

chmod +x script.sh

Then the script can be executed using:

./script.sh

This connects directly with the Linux permissions lesson from Day 51.

Basic Script Structure

A simple Bash script can look like:

#!/bin/bash


# This is a comment


echo "Starting script..."


pwd
ls


echo "Script completed."

The general structure is:

Shebang
   ↓
Commands
   ↓
Variables / Logic
   ↓
Output

As scripts become more advanced, they can include variables, conditions, loops, functions, and other programming concepts.

Variables

Today's lesson also introduced the concept of variables.

A variable is used to store information that can be used later in the script.

Example:

name="Sujal"
echo "$name"

Here:

name is the variable.
"Sujal" is its value.
$name accesses the stored value.

Variables make scripts more flexible because the same script can work with different values.

Scripts as Dual-Use Tools

One of the most important cybersecurity lessons today was that scripts are dual-use tools.

This means the same scripting capabilities can be used by both:

Defenders

Security professionals can use scripts to:

Automate system checks.
Analyze logs.
Monitor systems.
Collect information.
Perform repetitive administrative tasks.
Attackers

Attackers can also use scripts to:

Automate malicious activity.
Collect information.
Modify systems.
Execute commands.
Perform repetitive actions.

The technology itself is not automatically good or bad.

What matters is how it is used and for what purpose.

Why Bash Scripting Matters in Cybersecurity

Bash scripting is a valuable skill for cybersecurity because Linux environments are widely used in:

Servers
Cloud environments
Security tools
SOC operations
Incident response
System administration

Being able to automate command-line tasks can make security investigations much faster.

For example, instead of manually checking multiple files or commands, a script can perform the same checks automatically.

What I Learned
A Bash script is a plain text file containing commands.
Commands are generally executed from top to bottom.
Scripts automate repetitive tasks.
Automation saves time and reduces human error.
A Bash script commonly uses a shebang such as #!/bin/bash.
Scripts contain commands that perform the desired task.
Execute permission can be given using chmod +x.
Variables can store information used by the script.
Bash scripting is useful for cybersecurity automation.
Scripts are dual-use tools that can be used by both defenders and attackers.
Key Takeaways

✅ Scripts automate repetitive command-line tasks.

✅ The shebang identifies the interpreter.

✅ Commands inside a script execute in sequence.

✅ Execute permission allows a script to be run directly.

✅ Variables make scripts more flexible.

✅ Bash scripting is an important Linux and cybersecurity skill.

✅ The same scripting knowledge can be used for both defensive and offensive purposes.

Reflection

Today's lesson was an important step in my Linux journey because I moved from simply executing individual commands to automating multiple commands using a script.

I learned that even a simple text file can become a useful automation tool when it contains commands that are executed in sequence.

The concept of dual-use scripting was also important. Bash can help defenders automate security tasks, but the same capabilities can also be abused by attackers.

My biggest takeaway is:

Learning to automate commands is the first step toward becoming more efficient in cybersecurity.

Quote of the Day

"Don't repeat the same task manually when you can automate it."

Progress Tracker
Day: 61/90
Topic: Your First Bash Script
Concepts Learned: Bash Scripts, Shebang, Commands, Execute Permission, Variables, Automation, Dual-Use Tools
Command Covered: chmod +x
Key Insight: Bash scripting can automate repetitive Linux tasks and is an important skill for cybersecurity professionals.
Status: ✅ Completed
