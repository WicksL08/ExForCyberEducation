---
layout: default
title: Password Cracking Deep Dive
permalink: /learning/passwords/
---

# Password Cracking & Security Deep Dive 

Understand how passwords are **stored, protected, and tested** in cyber security.  
This page explores password hashing, cracking techniques, and ethical guidelines.

---

## What This Page Covers

| Topic | Description |
|-------|-------------|
| **Hashing vs. Encryption** | Learn why passwords are hashed, not encrypted. |
| **Salts & Peppers** | Understand how randomness prevents duplicate hashes. |
| **Cracking Methods** | Explore safe, simulated ways passwords are tested for strength. |
| **Ethical Hacking** | Learn how professionals test systems responsibly. |

---

##  Why Password Cracking Is Taught

cyber security experts study password cracking not to “hack” real systems, but to:
- Understand how attackers exploit weak passwords.
- Demonstrate the importance of hashing and salting.
- Teach students to **create stronger passwords**.

>  Always use **sample data** or **CTF labs**, never real credentials.

---

##  Hashing Refresher

**Hashing** transforms a password into a fixed length fingerprint.

| Password | Hash (SHA-256) |
|-----------|----------------|
| `hello` | `2cf24dba5fb0a...` |
| `Hello` | `185f8db32271f...` |

Notice how just capitalizing one letter completely changes the hash.  
This demonstrates **avalanche effect** — small input changes create huge output differences.

---

##  Adding a Salt

Salting adds random data before hashing.  
Example:
Password: "hello"
Salt: "X9z3"
Hash: SHA256("helloX9z3") → different from unsalted hash

Salts ensure that two users with the same password don’t share the same hash.

---

##  Common Cracking Methods (Educational Overview)

| Method | Description | Educational Use |
|---------|-------------|----------------|
| **Brute Force** | Try every possible combination. | Demonstrates exponential difficulty. |
| **Dictionary Attack** | Use a list of common passwords. | Show why “password123” fails quickly. |
| **Rainbow Tables** | Precomputed hashes for common passwords. | Explain why salts defeat this method. |
| **Hybrid Attack** | Mix dictionary + pattern variations. | Example: “Password” → “P@ssw0rd!” |

> Use tools like **John the Ripper**, **hashcat**, or simulated web based demos **offline or in sandbox environments**.

---

###  Password Strength Analysis
Use [Kaspersky Password Checker](https://password.kaspersky.com/){:target="_blank"} or  
[NCSC Password Strength Tool](https://www.ncsc.gov.uk/section/advice-guidance/all-topics/passwords){:target="_blank"}  
to see how long it would take to brute-force different passwords.

---

##  Key Vocabulary

| Term | Meaning |
|------|---------|
| **Hash** | One-way mathematical fingerprint of a password. |
| **Salt** | Random value added before hashing for uniqueness. |
| **Pepper** | Hidden constant value stored separately for added protection. |
| **Brute Force** | Trying all possible combinations. |
| **Dictionary Attack** | Testing passwords from a list of common words. |
| **Rainbow Table** | Precomputed lookup of hashes. |
| **Key Stretching** | Re-hashing to make cracking slower (e.g., bcrypt). |


---

## Challenge: Hash & Compare

Use [CyberChef](https://gchq.github.io/CyberChef/){:target="_blank"}  
1. Hash the phrase `CrimsonTide2025`.  
2. Add your initials as a salt and hash again.  
3. Compare the two outputs.  
4. Discuss why no one can reverse the hash even if they see it.

---
<nav style="text-align:center; margin-bottom:1rem;">
  <a class="btn" href="{{ '/learning/' | relative_url }}">All Lessons</a>
  <a class="btn" href="{{ '/learning/osint/' | relative_url }}">OSINT</a>
  <a class="btn" href="{{ '/learning/cryptography/' | relative_url }}">Cryptography</a>
  <a class="btn" href="{{ '/learning/passwords/' | relative_url }}">Passwords</a>
</nav>

