---
layout: default
title: Cryptography Deep Dive
permalink: /learning/cryptography/
---

# Cryptography Deep Dive 🔐

Learn how data is protected using **encryption**, **encoding**, and **hashing**.  
This section goes beyond the basics — perfect for classroom demos or independent study.

---

## 🧠 What Is Cryptography?

Cryptography is the science of **securing communication** so that only intended parties can read the information.  
It’s used in nearly everything — from banking and messaging apps to password storage and digital signatures.

---

## 🧩 Three Core Concepts

| Concept | Description | Real-World Example |
|----------|--------------|-------------------|
| **Encoding** | Converts data into another format for transfer or storage. Not meant for secrecy. | Base64 encoding emails or URLs |
| **Encryption** | Uses **keys** to lock/unlock data. Can be reversed with the correct key. | Encrypting a file with a password |
| **Hashing** | One-way transformation that produces a fixed-length “fingerprint.” | Storing passwords securely (e.g., SHA-256) |

---

## 🔐 Types of Encryption

### **Symmetric Encryption**
- Uses the **same key** to encrypt and decrypt.
- Fast and efficient, used in bulk data encryption.
- Example: **AES (Advanced Encryption Standard)**.

### **Asymmetric Encryption**
- Uses **two keys**: a public key (for encrypting) and a private key (for decrypting).
- Common in secure communications (HTTPS, email).
- Example: **RSA (Rivest–Shamir–Adleman)**.

---

## 🧮 Hashing Algorithms

| Algorithm | Output Length | Common Use |
|------------|----------------|-------------|
| **MD5** | 128 bits | Legacy, not secure anymore |
| **SHA-1** | 160 bits | Legacy, weak to collisions |
| **SHA-256** | 256 bits | Standard for password hashing |
| **bcrypt / scrypt / Argon2** | Variable | Modern, salt-based password hashing |

---

## 🧰 Hands-On Demos

Try these tools in a classroom lab or at home:

- 🔹 **[CyberChef](https://gchq.github.io/CyberChef/)** – Online tool for encoding, hashing, and encryption.  
- 🔹 **[Base64 Decode](https://www.base64decode.org/)** – Decode a message manually.  
- 🔹 **[MD5Hash Generator](https://md5hashgenerator.com/)** – See how hashes change with small text changes.  
- 🔹 **[SHA256 Online](https://emn178.github.io/online-tools/sha256.html)** – Experiment with hash lengths.

---

## 📚 Real-World Connections

- Online banking: encrypts communication with HTTPS (RSA + AES)  
- Password managers: hash and salt your master password  
- Secure messaging apps: use end-to-end encryption  
- Software integrity: code signing uses cryptographic signatures

---

## 🧠 Challenge

Use [CyberChef](https://gchq.github.io/CyberChef/){:target="_blank"} to:
1. Encode a short phrase (Base64).  
2. Hash the same phrase (SHA-256).  
3. Encrypt it using AES with your initials as the key.  
4. Observe how each process differs — what’s reversible and what’s not?

---

**Next:** Return to the [Learning Lab]({{ '/learning/' | relative_url }}) for OSINT, Passwords, and more practice modules.
