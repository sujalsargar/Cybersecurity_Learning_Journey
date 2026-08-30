Day 70 - Hashing
Objective

Understand hashing, learn how it is different from encryption, and understand how hashes are used to verify data integrity and protect stored passwords.

Lesson of the Day

Today, I learned about Hashing.

Hashing is a one-way mathematical process that converts data into a fixed-length value called a hash.

Unlike encryption, hashing is not designed to be reversed.

A simple way to remember it is:

Encryption can be decrypted with the right key. Hashing is one-way.

What is Hashing?

Hashing takes input data and produces a hash value.

Original Data
     ↓
   Hashing
     ↓
 Hash Value

The important idea is that the original data is not supposed to be recovered from the hash through a normal decryption process.

Hashing vs Encryption

Hashing and encryption are different security techniques.

Feature	Hashing	Encryption
Main purpose	Integrity / verification	Confidentiality
Direction	One-way	Reversible with the appropriate key
Can it be decrypted?	No	Yes, with the appropriate key
Common use	Password storage, integrity checks	Protecting data and communication

A simple way to remember:

Encryption = Keep it secret

Hashing = Check that it hasn't changed

Hashing for Data Integrity

One important use of hashing is verifying integrity.

The basic process is:

Original File
     ↓
Generate Hash
     ↓
Store / Compare Hash

If the file is changed, even slightly, its resulting hash should change.

For example:

File A
 ↓
Hash A

File A is modified
 ↓
Hash B

If the hashes are different, the data has changed.

This helps determine whether data has been modified.

Hashing and Passwords

Another important use of hashing is password storage.

A secure system should not store users' passwords as plain readable text.

Instead, it stores password-derived values using appropriate password-hashing mechanisms.

The basic login process can be understood as:

User enters password
        ↓
Password is processed using the password-hashing system
        ↓
Result is compared with the stored value
        ↓
Match?
   ↙        ↘
 Yes         No
 ↓           ↓
Login      Reject

This means the system does not need to store the user's original password in readable form.

Why This Matters During a Database Breach

Imagine a website's password database is compromised.

If passwords were stored as plain text:

Database Breach
      ↓
Actual Passwords Exposed

This would be extremely dangerous.

With properly implemented password hashing:

Database Breach
      ↓
Password-derived Hash Values Exposed

The attacker does not simply receive a list of readable passwords.

However, hashed passwords are not automatically safe.

Attackers may try to guess passwords and compare the resulting values.

Weak vs Strong Passwords

Password strength is very important.

Weak Password

A simple or commonly used password is easier to guess.

Weak Password
      ↓
Many likely guesses
      ↓
Easier to crack
Strong Password

A long, unique, unpredictable password is much harder to guess.

Strong Password
      ↓
Huge number of possible guesses
      ↓
Harder to crack

This is why the password-security lessons from earlier in my journey remain important.

Hashing helps protect stored passwords, but strong passwords still matter.

Hashing Does Not Make Weak Passwords Strong

This is an important security concept.

Suppose a user chooses a very common password.

Even if the website stores a hash instead of the actual password, an attacker who obtains the password database may attempt many common password guesses and compare their results with the stolen values.

Therefore:

Secure Password Hashing
        +
Strong, Unique Password
        ↓
Better Password Security

Password hashing and strong passwords work together.

A Secure System Should Not Store Plain Passwords

The basic principle I learned today is:

A secure system should not store passwords as plain readable text.

Instead, it should use a properly designed password-storage system that stores appropriate password-derived values.

Modern password storage should also use suitable password-hashing algorithms and protections such as unique salts.

What I Learned
Hashing is a one-way mathematical process.
A hash is generated from input data.
Hashing is different from encryption.
Encryption primarily protects confidentiality.
Hashing can help verify integrity.
A changed file should produce a different hash.
Passwords should not be stored as plain text.
Password-storage systems use password-derived hash values.
During login, the entered password is processed and compared with the stored value.
Weak passwords are easier to guess.
Strong and unique passwords are harder to crack.
Password hashing does not eliminate the need for strong passwords.
Key Takeaways

✅ Hashing = One-way

✅ Encryption = Reversible with the appropriate key

✅ Encryption mainly protects Confidentiality.

✅ Hashing is commonly used for Integrity verification and password storage.

✅ A changed file should produce a different hash.

✅ Passwords should not be stored as plain text.

✅ Strong, unique passwords are still important even when password hashing is used.

Reflection

Today's lesson helped me clearly understand the difference between hashing and encryption.

I previously learned that encryption converts readable information into unreadable ciphertext and that the original data can be recovered using the appropriate key. Hashing is different because it is designed as a one-way process.

I also learned why hashing is important for password security. A properly designed system should not simply keep everyone's actual passwords in its database.

However, I learned that hashing alone does not make weak passwords safe. If passwords are easy to guess, attackers can still attempt guesses against stolen password-derived values.

My biggest takeaway is:

Hashing protects stored password values and helps verify integrity, but strong passwords and proper password-storage practices are still essential.

Quote of the Day

"Encryption keeps data secret; hashing helps prove what the data is and whether it changed."

Progress Tracker
Day: 70/90
Topic: Hashing
Core Concepts: Hash, One-Way Function, Integrity, Password Storage
Comparison: Hashing vs Encryption
Security Focus: Data Integrity and Password Protection
Key Insight: Hashing is one-way and is widely used for integrity verification and secure password storage.
Status: ✅ Completed
