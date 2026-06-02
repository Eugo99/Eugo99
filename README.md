# Emmanuel Ugochukwu Akalabu

**Cybersecurity Analyst · MSc Cybersecurity — University of Aberdeen (exp. Sept 2026)**

> Focused on IIoT/OT security, SOC operations, digital forensics, and offensive security. I build isolated lab environments to test what the theory says and measure what actually happens.

---

## Current Research

**A Comparative Evaluation of Detection and Mitigation Strategies for Network-Based Attacks in Industrial IoT Environments**

Comparing Suricata 6.0.4 (reactive, signature-based IDS) against Linux iptables (preventive, network-layer ACL) for Modbus/TCP attack scenarios inside a Docker-isolated testbed on a Kali Linux QEMU/KVM VM.

| Component | Detail |
|---|---|
| Attack scenarios | Modbus/TCP replay attacks · Unauthorised command injection |
| Risk basis | IEC 62443-3-2 Critical rating (absent authentication + absent message freshness) |
| Testbed | 3 containers: `modbus-target` (pymodbus) · `ids-monitor` (Suricata) · `attacker` (Scapy/pymodbus/tcpreplay) |
| Dataset | 4SICS ICS Network Traffic Captures (replay traffic + FP baseline) |
| Metrics | Attack success rate · Detection rate · False positive rate · Packet processing overhead |
| Supervisor | Dr Chunyan Mu, University of Aberdeen |

---

## Technical Skills

```
Languages & Scripting    Python 3 · Bash
Security Tooling         Suricata · Wireshark/Tshark · Burp Suite · Nmap · Scapy · Netcat
                         Autopsy · FTK Imager · Aid4Mail · Nessus · OpenVAS
IDS / Network            Suricata 6.0.4 · iptables · tcpreplay · tcpdump
Containerisation         Docker · QEMU/KVM
Frameworks               MITRE ATT&CK · ATT&CK for ICS · NIST CSF · NIST SP 800-82
                         IEC 62443 · OWASP Web Top 10 · OWASP LLM Top 10 · SLSA/in-toto
SIEM                     Microsoft Sentinel (labs) · Splunk (labs) · Elastic (basic)
OS                       Kali Linux · Debian · Ubuntu · Windows
```

---

## Selected Projects

### IIoT Attack Detection & Mitigation Testbed
`Python` `Docker` `Suricata` `iptables` `Scapy` `pymodbus` `tcpreplay`

Three-container Docker environment isolated within a Kali Linux QEMU/KVM VM. Implements and measures two Modbus/TCP attack types against a reactive IDS and a preventive ACL control. Custom Suricata rules target function code misuse, write coil/register anomalies, and replay-like repeated PDU signatures (threshold-based via `detection_filter`). iptables rules restrict inbound TCP/502 to authorised client IP only.

**Status:** Active (MSc project, Jun–Aug 2026)

---

### Digital Forensics: Email & Disk Image Analysis
`Autopsy 4.19.3` `FTK Imager 4.7.1.2` `Aid4Mail 5.0.19` `Python`

**Email forensics — Enron dataset:**
- Converted 1,328-item Eric Saibi PST to structured CSV (Aid4Mail); applied keyword, status, and address filters to surface financial misconduct evidence.
- Indexed Kenneth Lay PST in Autopsy: 14,933 messages, 45 communication accounts, 33,992 email addresses, 129,388 keyword hits. Identified regulatory investigation, price-fixing, and financial instability communications.

**File carving — raw disk image:**
- Manually recovered 11 artefacts from unallocated space in `raw_image2.dd` using hex signature identification and logical EOF validation (no automated carving tools).
- File types: JPEG · PDF (x2) · GIF (x2) · TXT · EXE (x2) · XLSX · DOCX · Windows Prefetch.
- Each file verified by opening in a compatible application post-carving.

---

### Web Security CTF (10 Challenges) — CS552H
`Burp Suite` `Python` `Netcat` `Browser DevTools`

| Challenge | Technique |
|---|---|
| Level 1 | Client-side credential disclosure (hardcoded JS credentials) |
| Level 2 | IDOR / parameter tampering (uid/view DOM manipulation) |
| Level 3 | OS command injection (`2;cat secret.txt`) |
| Level 4 | Forced browsing / predictable path (`/static/img/secret.txt`) |
| Level 5 | Broken auth via unsigned cookie (`pwd=` header replay) |
| Level 6 | UNION-based SQL injection (cross-table credential extraction) |
| Level 7 | PNG LSB steganography (custom Python PIL bit-extraction) |
| Level 8 | JWT alg:none signature bypass (forged `role:admin` token) |
| Level 9 | Stored XSS + cookie exfiltration (script-filter bypass via event handler; netcat listener) |
| Level 10 | Stack buffer overflow — 106-byte authentication bypass |

---

### Application Security CTF (10 Challenges)
`GDB` `Python` `pwntools`

Buffer overflow exploitation, shellcode injection, and brute-force stack address discovery across 10 binary challenges. Includes both scripted and manual approaches to stack canary bypass and return address control.

---

### ICMP Spoofing Lab
`Scapy` `Python` `Wireshark` `Docker`

Scapy script sniffing ICMP echo requests on a Docker bridge interface and responding with crafted packets bearing a spoofed source IP. End-to-end spoof confirmed via Wireshark packet analysis.

---

### Automation Engineer Intern — Industrial OT/ICS Environment
`Allen Bradley PLC` `HMI` `MPPT Inverters` `IIoT` `Control Systems`

Hands-on industrial automation internship at Djreda Ltd (Abeokuta, Nigeria, Feb 2019 – Feb 2020) working within a live OT/ICS environment.

- Reviewed Allen Bradley PLC programs to identify sensor and actuator connection flaws in live control logic — direct exposure to the same OT layer targeted in my MSc research.
- Assisted in design and construction of control systems integrating Allen Bradley PLCs with HMI interfaces for industrial process management.
- Assisted in the construction of IIoT-enabled solar power systems with MPPT inverters, bridging embedded hardware and networked industrial control.

---

### Agentic AI Security Analysis — CS552H Assessment 06
`OWASP LLM Top 10 (2025)` `OWASP Agentic Top 10 (2026)` `NIST AI RMF` `EU AI Act`

Analysed an indirect prompt-injection scenario in a fictional Django patient portal (MedBridge) involving an agentic coding assistant. Mapped attack vectors against OWASP LLM Top 10, OWASP Agentic Applications Top 10 (2026), NIST AI RMF, SLSA/in-toto supply-chain controls, CODEOWNERS enforcement, and EU AI Act deployer obligations (Article 26).

---

## Certifications

| Certification | Issuer | Date |
|---|---|---|
| Ethical Hacker | Cisco Networking Academy | May 2025 |
| Networking Basics | Cisco Networking Academy | Nov 2024 |
| IoT Fundamentals: IoT Security | Cisco Networking Academy | Feb 2023 |
| Partner: Cloud Security (CCSK) | Cisco Networking Academy | Dec 2022 |
| Introduction to Cybersecurity | Cisco Networking Academy | Nov 2022 |

---

## Education

**MSc Cybersecurity** — University of Aberdeen, UK *(exp. Sept 2026)*

**BEng Electrical & Electronic Engineering** — Michael Okpara University of Agriculture, Nigeria *(2018)*

---

## Contact

- Email: emmanuelakalabu@gmail.com
- Location: Aberdeen, UK (open to UK & EU relocation)
- LinkedIn: [emmanuel-akalabu](https://www.linkedin.com/in/emmanuel-akalabu-7ba409159)

---

*Home lab: Debian host running Kali Linux QEMU/KVM VM — all security research and tooling isolated from the host OS by design.*
