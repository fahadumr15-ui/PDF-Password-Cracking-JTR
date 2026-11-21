# 🔐 Password Cracking & Hash Auditing with John the Ripper (JTR)

This repository documents a hands-on cybersecurity lab completed as part of **NetworkWalks Week 3 (Project Module 1)**. The objective was to understand cryptographic hashing versus encryption and perform password auditing on a protected PDF file using **John the Ripper (JTR)** and its GUI frontend, **Johnny**

---

## 🛠️ Tools & Environment
* **OS:** Windows 10/11
* **Core Tool:** John the Ripper (`1.9.0-jumbo-1` Windows x64)
* **GUI Frontend:** Johnny (`v2.2`)
* **Hash Extraction:** `pdf2john` (via OnlineHashCrack PDF Hash Extractor)

---

## 🚀 Lab Execution Steps

### 1. Environment Setup
Configured John the Ripper Jumbo binaries and linked `john.exe` inside the Johnny GUI settings

### 2. PDF Hash Extraction
Extracted the cryptographic password hash (`$pdf$...`) from the target locked file (`My Locked PDF1.pdf`) and saved it in a clean `.txt` format for processing.

### 3. Dictionary / Auditing Attack
Loaded the extracted hash file into Johnny and initiated a password recovery session. JTR successfully matched the hash against its wordlist.

### 4. Verification & Flag Capture
Used the recovered credential to unlock the protected PDF document and verified the flag[cite: 13, 14].

---

## 💡 Key Takeaways
* **Encryption vs. Hashing:** Encryption is a two-way process reversible with a key, while hashing is a one-way cryptographic function used for validation.
* **Password Entropy:** Weak or common dictionary passwords can be cracked within seconds using automated auditing tools, highlighting the necessity of strong, high-entropy passwords and MFA.

---
*Disclaimer: This lab was performed strictly for educational purposes in an authorized environment.*
