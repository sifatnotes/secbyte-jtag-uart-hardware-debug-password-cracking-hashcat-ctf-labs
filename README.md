# secbyte-jtag-uart-hardware-debug-password-cracking-hashcat-ctf-labs
A practical collection of cybersecurity CTF labs covering hardware debugging interfaces (JTAG pinout exploration, UART serial console recovery, silicon-to-secure boot security fundamentals) and password auditing/cracking techniques (Hashcat essentials, John the Ripper, rule-based mutations, mask attacks, rainbow tables, and dictionary attacks).
# JTAG/UART Hardware Debugging, Password Cracking & Hashcat/John the Ripper CTF Labs

Welcome to the **JTAG/UART Hardware Debugging, Password Cracking & Hashcat/John the Ripper CTF Lab Collection**. This repository serves as an organized, searchable catalog of practical cybersecurity labs hosted on Learn SecByte.

This collection focuses on low-level hardware debug port discovery and offline credential cracking methodologies—spanning **Hardware Debug Interfaces & Physical Console Security (JTAG boundary scan, UART serial console recovery, silicon-to-secure boot trust chains)** and **Password Auditing, Recovery & Hash Cracking (Hashcat GPU acceleration, John the Ripper, rule-based pattern mutation, mask attacks, rainbow tables, and dictionary attacks)**.

---

## Lab Collection Index

### 1. Hardware Debug Interfaces & Physical Console Security
* **JTAG Exploration: The Debug Port Incident**  
  *Lab Link:* [https://learn.secbyte.org/ctf/jtag-exploration-the-debug-port-incident](https://learn.secbyte.org/ctf/jtag-exploration-the-debug-port-incident)  
  *Focus:* Identifying unpopulated JTAG test points (TDI, TDO, TCK, TMS) using JTAGulator/OpenOCD, executing boundary scan tests, dumping internal MCU flash memory, and bypassing readout protection (RDP).

* **UART Interface Analysis: Ghost Console Investigation**  
  *Lab Link:* [https://learn.secbyte.org/ctf/uart-interface-analysis-ghost-console-investigation](https://learn.secbyte.org/ctf/uart-interface-analysis-ghost-console-investigation)  
  *Focus:* Locating serial UART pinouts (TX, RX, GND, VCC) on target PCBs, identifying unknown baud rates, intercepting interactive bootloader shells (U-Boot), and gaining unauthenticated root console access.

<Image src="image_agent_tag_14792659433531761568" alt="ARM 20-pin JTAG debug connector pinout diagram showing signal names and descriptions" caption="Standard Hardware JTAG Debug Connector Pinout Specification" />

---

* **Hardware Security Fundamentals: From Silicon to Secure Boot**  
  *Lab Link:* [https://learn.secbyte.org/ctf/hardware-security-fundamentals-from-silicon-to-secure-boot](https://learn.secbyte.org/ctf/hardware-security-fundamentals-from-silicon-to-secure-boot)  
  *Focus:* Auditing hardware security architectures—from silicon-level One-Time Programmable (OTP) fuses, Cryptographic Coprocessors, and Hardware Root-of-Trust (RoT) to immutable Secure Boot chains.

### 2. Password Auditing, Recovery & Cracking Tooling
* **Hashcat Essentials: From Theory to Realistic Cracking**  
  *Lab Link:* [https://learn.secbyte.org/ctf/hashcat-essentials-from-theory-to-realistic-cracking](https://learn.secbyte.org/ctf/hashcat-essentials-from-theory-to-realistic-cracking)  
  *Focus:* Mastering GPU-accelerated hash cracking with Hashcat, selecting optimized hash modes (`-m`), managing wordlists and rules, and benchmark tuning against modern salted hashes (NTLM, bcrypt, SHA-512 crypt).

<Image src="image_agent_tag_14792659433531762671" alt="Table of Hashcat hash modes detailing hash types, names, and payload structures" caption="Hashcat Hash Mode Configurations & Hash Type Specifications" />

---

* **John the Ripper: Password Recovery Lab**  
  *Lab Link:* [https://learn.secbyte.org/ctf/john-the-ripper-password-recovery-lab](https://learn.secbyte.org/ctf/john-the-ripper-password-recovery-lab)  
  *Focus:* Extracting password hashes from various format targets (`zip2john`, `ssh2john`, `unshadow`), configuring custom `john.conf` rulesets, and recovering protected credentials.

* **Password Recovery Lab**  
  *Lab Link:* [https://learn.secbyte.org/ctf/password-recovery-lab](https://learn.secbyte.org/ctf/password-recovery-lab)  
  *Focus:* Recovering legacy system passwords, dissecting SAM database hashes, handling specialized archive encryptions, and performing offline credential extraction.

* **Password Auditing Lab: From Policy to Proof**  
  *Lab Link:* [https://learn.secbyte.org/ctf/password-auditing-lab-from-policy-to-proof](https://learn.secbyte.org/ctf/password-auditing-lab-from-policy-to-proof)  
  *Focus:* Conducting corporate Active Directory password audits, evaluating password complexity policies against cracked hash percentages, and generating vulnerability audit reports.

### 3. Targeted Cracking Techniques & Credential Attacks
* **Dictionary Attack Lab: Credential Hygiene and Password Guessing**  
  *Lab Link:* [https://learn.secbyte.org/ctf/dictionary-attack-lab-credential-hygiene-and-password-guessi](https://learn.secbyte.org/ctf/dictionary-attack-lab-credential-hygiene-and-password-guessi)  
  *Focus:* Optimizing targeted wordlists (SecLists, RockYou), cleaning dictionary dumps, applying leetspeak transformations, and measuring wordlist efficiency.

* **Rule-Based Attacks: Pattern Hunter**  
  *Lab Link:* [https://learn.secbyte.org/ctf/rule-based-attacks-pattern-hunter](https://learn.secbyte.org/ctf/rule-based-attacks-pattern-hunter)  
  *Focus:* Designing custom Hashcat mutation rules (`.rule` files), combining append/prepend/capitalize operators, and targeting common corporate password composition patterns.

* **Mask Attacks: From Masking to Credential Recovery**  
  *Lab Link:* [https://learn.secbyte.org/ctf/mask-attacks-from-masking-to-credential-recovery](https://learn.secbyte.org/ctf/mask-attacks-from-masking-to-credential-recovery)  
  *Focus:* Constructing high-speed mask attacks (`?u?l?l?l?d?d?d?s`), defining custom character sets (`-1`), and efficiently cracking fixed-length structured passwords.

* **Brute-Force Attacks: From Credential Guessing to Defenses**  
  *Lab Link:* [https://learn.secbyte.org/ctf/brute-force-attacks-from-credential-guessing-to-defenses](https://learn.secbyte.org/ctf/brute-force-attacks-from-credential-guessing-to-defenses)  
  *Focus:* Evaluating mathematical search spaces for exhaustiveness, configuring online vs. offline brute-force attempts, and implementing defensive lockout/tarpitting controls.

* **Rainbow Table Breakroom**  
  *Lab Link:* [https://learn.secbyte.org/ctf/rainbow-table-breakroom](https://learn.secbyte.org/ctf/rainbow-table-breakroom)  
  *Focus:* Analyzing precomputed lookup tables (Ophcrack / RainbowCrack), understanding reduction functions and chain collisions, and evaluating why modern salting invalidates precomputation attacks.

---

## Learning Path

### Path A: Hardware Debugging & Physical Console Specialist
1. **Debug Interface Identification:** Start with [JTAG Exploration: The Debug Port Incident](https://learn.secbyte.org/ctf/jtag-exploration-the-debug-port-incident) and [UART Interface Analysis](https://learn.secbyte.org/ctf/uart-interface-analysis-ghost-console-investigation).
2. **Silicon & Boot Security:** Audit hardware root of trust in [Hardware Security Fundamentals](https://learn.secbyte.org/ctf/hardware-security-fundamentals-from-silicon-to-secure-boot).

### Path B: Password Cracking Tooling & Auditing Specialist
1. **Core Cracking Frameworks:** Master tools in [Hashcat Essentials](https://learn.secbyte.org/ctf/hashcat-essentials-from-theory-to-realistic-cracking) and [John the Ripper](https://learn.secbyte.org/ctf/john-the-ripper-password-recovery-lab).
2. **Enterprise Audits & Recovery:** Conduct audits via [Password Recovery Lab](https://learn.secbyte.org/ctf/password-recovery-lab) and [Password Auditing Lab: From Policy to Proof](https://learn.secbyte.org/ctf/password-auditing-lab-from-policy-to-proof).

### Path C: Advanced Attack Vectors & Password Mutation Specialist
1. **Wordlists & Rules:** Optimize attacks in [Dictionary Attack Lab](https://learn.secbyte.org/ctf/dictionary-attack-lab-credential-hygiene-and-password-guessi) and [Rule-Based Attacks: Pattern Hunter](https://learn.secbyte.org/ctf/rule-based-attacks-pattern-hunter).
2. **Masks, Brute-Force & Rainbow Tables:** Execute targeted searches via [Mask Attacks](https://learn.secbyte.org/ctf/mask-attacks-from-masking-to-credential-recovery), [Brute-Force Attacks](https://learn.secbyte.org/ctf/brute-force-attacks-from-credential-guessing-to-defenses), and [Rainbow Table Breakroom](https://learn.secbyte.org/ctf/rainbow-table-breakroom).

---

## How to Use the Labs

1. Select a practice scenario from the **Lab Collection Index**.
2. Click the corresponding direct link to launch the exercise environment hosted on Learn SecByte.
3. Review scenario directives, logic analyzer pin traces, target hash dumps (`$6$`, `$2b$`, NTLM), or corrupted device firmware images.
4. Pinout JTAG/UART headers, write custom Hashcat mutation rules, construct precise mask parameters, extract hashes via `ssh2john`/`zip2john`, or bypass bootloader shell authentication to capture flags.

---

## Target Audience

* **Hardware Pentesters & Embedded Security Engineers:** Locate physical JTAG/UART debug ports, audit MCU readout protections, and evaluate silicon-to-secure boot trust chains.
* **Penetration Testers & Red Team Operators:** Perform high-speed offline password cracking with Hashcat/John the Ripper, build custom mutation rules, and design targeted mask attacks.
* **SOC Analysts & Enterprise Active Directory Auditors:** Audit domain user password hygiene, quantify weak password exposures, and evaluate corporate password complexity policies.
* **Cybersecurity Students:** Acquire practical skills in hardware debug interface manipulation, password hash cracking, and dictionary optimization.

---

## Disclaimer

All lab links provided in this repository direct to official training environments hosted on Learn SecByte. All materials and exercises are provided strictly for educational purposes, defensive skill building, and authorized security research. Unauthorized hardware tampering, password cracking, or credential dumping against external systems without prior consent is strictly prohibited.
