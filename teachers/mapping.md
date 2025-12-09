---
layout: default
title: Standards Mapping – Ex4CSLearning
permalink: /teachers/mapping/
---

# Standards Mapping 

The **Ex4CSLearning 3-Day Pilot** aligns each Capture-the-Flag (CTF) topic to the  
**Alabama K-12 Computer Science Standards (2021)** and the **NICE Cybersecurity Workforce Framework (2020)**.  

These mappings ensure classroom activities meet both **state academic goals** and **national cybersecurity competencies**.
---

## Challenge–Standards Mapping

> **DLCS Codes (Alabama DLCS Recurring Standards)**  
> R1 – Safety, Privacy & Security  
> R2 – Legal & Ethical Behavior  
> R3 – Impact of Computing  
> R4 – Systems / Troubleshooting  
> R5 – Collaborative Research  
> R6 – Digital Tools & Artifacts  

> **NICE Category Codes (Workforce Framework)**  
> SP – Securely Provision  
> PR – Protect & Defend  
> AN – Analyze  
> CO – Collect & Operate  
> IN – Investigate  

---

### Cryptography Challenges

| Challenge | Topic | Points / Level | DLCS Alignment (Alabama) | NICE Category Alignment | Main Learning Focus |
|----------|-------|----------------|---------------------------|-------------------------|----------------------|
| **The Secret Scroll** | Cryptography | 100 – Easy | R3 (Impact of Computing); R4 (Systems – algorithms); R6 (Digital Tools) | SP (Securely Provision); PR (Protect & Defend) | Recognize why encryption is used to protect information; practice decoding a simple cipher using step-by-step reasoning. |
| **The Hidden Codebook** | Cryptography | 200 – Medium | R3; R4; R6 | SP; PR; AN (Analyze) | Compare different substitution ciphers; analyze patterns in ciphertext; connect cryptography to real-world secure communication. |
| **The Headmaster’s Secret** | Cryptography | 300 – Hard | R3; R4; R5 (Collaborative Research); R6 | SP; PR; AN | Work collaboratively to break a multi-step cipher; justify solution process; relate strong/weak encryption to security risk. |
| **Crush Code** | Cryptography | 25 – Easy | R3; R6 | SP; PR | Apply a basic cipher tool to encrypt/decrypt short messages; connect cipher keys to password/secret sharing. |
| **Boba Tea Cipher** | Cryptography | 5 – Very Easy | R3; R6 | SP; PR | Practice using a themed substitution cipher to build confidence with encoding/decoding. |
| **Minecraft – “Hidden Chat Message”** | Cryptography | 10 – Easy | R3; R4; R6 | SP; PR; AN | Decode a hidden message embedded in a “game chat”; connect cryptography to in-game and real-world messaging. |

---

### Open Source Intelligence (OSINT) Challenges

| Challenge | Topic | Points / Level | DLCS Alignment (Alabama) | NICE Category Alignment | Main Learning Focus |
|----------|-------|----------------|---------------------------|-------------------------|----------------------|
| **The World’s Traveler’s Watch** | Open Source Intelligence | 100 – Easy | R1 (Safety, Privacy & Security); R2 (Legal & Ethical Behavior); R5 (Collaborative Research); R6 (Digital Tools) | AN (Analyze); CO (Collect & Operate) | Use search tools and public sources to answer location-based clues; practice safe, ethical online research habits. |
| **Find the Bean!** | Open Source Intelligence | 200 – Medium | R1; R2; R3; R5; R6 | AN; CO | Combine multiple OSINT tools (images, maps, websites) to track down a target object; evaluate credibility of sources. |
| **The Vanished Motto** | Open Source Intelligence | 300 – Hard | R1; R2; R3; R5; R6 | AN; CO; IN (Investigate) | Follow a multi-step OSINT trail (Wayback, WHOIS, news, etc.); document evidence and reasoning like a cyber investigator. |

---

### Password Cracking & Security Challenges

| Challenge | Topic | Points / Level | DLCS Alignment (Alabama) | NICE Category Alignment | Main Learning Focus |
|----------|-------|----------------|---------------------------|-------------------------|----------------------|
| **How Long Until It’s Gone?** | Password Cracking / Strength | 50 – Easy | R1 (Safety, Privacy & Security); R2 (Legal & Ethical Behavior); R3; R6 | PR (Protect & Defend); AN | Explore how password length & complexity affect cracking time; connect to personal password hygiene. |
| **County Salt** | Password Cracking | 100 – Medium | R1; R2; R3; R6 | PR; AN | Understand hashing and “salt”; see why salted hashes are harder to crack; relate to stored passwords in real systems. |
| **Forgotten Coffee Shop Wi-Fi** | Password Cracking | 150 (or course value) – Medium | R1; R2; R3; R4; R6 | PR; AN; OM (Operate & Maintain, optional) | Analyze a realistic Wi-Fi password / captive-portal scenario; reason about weak vs strong passwords and user behavior. |

---

You can drop this whole block into your **mapping page** and:

- Adjust **points/levels** if they’re different in CTFd.  
- If you decide on *official* DLCS code labels later (e.g., “DLCS 9–12 CS.3”), you can just replace the “R1, R2…” text in the DLCS column.  
- If you add new challenges, just copy a row, change the title, and adjust the standards.

If you tell me which file name you’re using for the mapping page (`mapping.md`, `teachers-mapping.md`, etc.), I can rewrite this snippet with your exact headings/intro text so it drops in perfectly.
::contentReference[oaicite:2]{index=2}

---

## 📊 Assessment Connections

| Assessment | Purpose | Link |
|-------------|----------|------|
| **Pre-Test** | Measures baseline understanding before activities. | [🧠 Pre-Test]({{ '/assessments/pre/' | relative_url }}) |
| **Post-Test** | Evaluates knowledge growth and comprehension. | [📊 Post-Test]({{ '/assessments/post/' | relative_url }}) |
| **Feedback & Reflections** | Collects qualitative input from students and teachers. | [💬 Feedback Form]({{ '/about/feedback/' | relative_url }}) |

---

## 🔗 Quick Access for Teachers
<div class="btn-row">
  <a class="btn" href="{{ '/teachers/syllabus/' | relative_url }}">📘 3-Day Syllabus</a>
  <a class="btn" href="{{ '/about/consent/' | relative_url }}">📝 Consent Forms</a>
  <a class="btn" href="{{ '/teachers/' | relative_url }}">🧰 Teacher Toolkit</a>
  <a class="btn" href="{{ '/challenges/' | relative_url }}">🎯 CTF Challenges</a>
  <a class="btn" href="{{ '/learning/' | relative_url }}">💡 Learning Lab</a>
</div>

