# 🛡️ The Ultimate VAPT (Vulnerability Assessment & Penetration Testing) Master Guide

Welcome to the comprehensive guide for mastering VAPT. This repository contains everything you need to understand the complete attack lifecycle, the exact tools required, a 22-project roadmap to build your portfolio, and the real-world expectations of a security engineer.

---

## 🩺 The VAPT Lifecycle (The Doctor Analogy)

To understand VAPT, think of a security engineer as a doctor diagnosing a patient. You cannot just start "cutting" (hacking) without a diagnosis.

| Doctor Analogy | VAPT Phase | What You Actually Do | Tools Used |
| :--- | :--- | :--- | :--- |
| **1. Consent Form**<br>*(Patient agrees to treatment)* | **1. Scoping & RoE**<br>*(Rules of Engagement)* | Sign legal contract (NDA & SOW). Define exactly which IPs/websites you can attack and which you must **not** touch. *No permission = illegal hacking.* | Pen & Paper, NDA/SOW Documents |
| **2. Check-Up & Vitals**<br>*(Doctor checks BP, asks history)* | **2. Reconnaissance**<br>*(Information Gathering)* | Scan external network. Find open ports, OS versions, software. Look for leaked emails and subdomains. | Nmap, Shodan, theHarvester, Amass |
| **3. Blood Test & X-Ray**<br>*(Finds a suspicious spot)* | **3. Vulnerability Assessment**<br>*(Scanning)* | Run automated scanners to find **potential** weaknesses (missing patches, outdated plugins). Filter out false positives. | Nessus, OpenVAS, Burp Scanner, Nikto |
| **4. Surgery / Biopsy**<br>*(Cuts in to PROVE disease is real)* | **4. Penetration Testing**<br>*(Exploitation)* | **Actually exploit** the vulnerabilities. Break into the server. Prove the risk is real, not just theoretical. | Metasploit, SQLmap, Hydra, Burp Repeater |
| **5. Checking for Metastasis**<br>*(Has it spread?)* | **5. Post-Exploitation**<br>*(Lateral Movement)* | After getting in, find passwords, move to the next server, escalate from normal user to Domain Admin. | Mimikatz, BloodHound, Cobalt Strike |
| **6. Prescription & Treatment**<br>*(Doctor writes a plan)* | **6. Reporting & Remediation**<br>*(The Final Report)* | Write a report explaining the risk in business terms + exact technical fixes (patches, MFA, network segmentation). | MS Word, CVSS Calculator, Dradis |
| **7. Follow-Up Visit**<br>*(Did medicine work?)* | **7. Retesting**<br>*(Verification)* | After client applies fixes, try to hack them again. Confirm "Fixed" or "Still Vulnerable." Deliver a Retest Report. | Same exploit tools (again) |

*Note: As a fresher, Steps 1, 2, 3, 6, and 7 require Low to Medium technical experience. Steps 4 and 5 require High to Very High experience.*

---

## 🛠️ The Ultimate Tool Arsenal (Categorized)

Here is the massive categorized list of tools you need to master, ranked by priority.

### 🥇 Must Master (Priority: 27 Tools)
*These are non-negotiable for any VAPT role.*
*   **Recon & OSINT:** [Nmap](https://nmap.org/), [Shodan](https://shodan.io/), WHOIS, Google Dorking
*   **Vulnerability Scanning:** [Nessus](https://www.tenable.com/), [OpenVAS](https://www.openvas.org/)
*   **Web App Exploitation:** [Burp Suite](https://portswigger.net/burp), [SQLmap](https://sqlmap.org/), [OWASP ZAP](https://www.zaproxy.org/)
*   **Network Exploitation:** [Metasploit](https://www.metasploit.com/), [Hydra](https://github.com/vanhauser-thc/thc-hydra), [John the Ripper](https://www.openwall.com/john/)
*   **Post-Exploitation:** [Mimikatz](https://github.com/gentilkiwi/mimikatz), [BloodHound](https://github.com/BloodHoundAD/BloodHound)
*   **Mobile & Cloud:** [Frida](https://frida.re/), [MobSF](https://github.com/MobSF/Mobile-Security-Framework-MobSF), [Ghidra](https://ghidra-sre.org/), AWS CLI, [ScoutSuite](https://github.com/nccgroup/ScoutSuite)
*   **Cracking & Reporting:** [Hashcat](https://hashcat.net/hashcat/), [Dradis](https://dradisframework.com/), CVSS Calculator, MS Word
*   **AI/LLM & Scripting:** [Garak](https://github.com/leondz/garak), Python, Bash, PowerShell

### 🥈 Should Know (Priority: 30 Tools)
*Elevates you above standard testers.*
*   **Recon:** [theHarvester](https://github.com/laramies/theHarvester), [Amass](https://github.com/owasp-amass/amass), [Subfinder](https://github.com/projectdiscovery/subfinder), [Nuclei](https://github.com/projectdiscovery/nuclei), [ffuf](https://github.com/ffuf/ffuf), [Gobuster](https://github.com/OJ/gobuster)
*   **Web Testing:** [Postman](https://www.postman.com/), [Responder](https://github.com/lgandx/Responder)
*   **Credential Attacks:** [CrackMapExec](https://github.com/byt3bl33d3r/CrackMapExec), [Impacket](https://github.com/fortra/impacket), [Medusa](https://github.com/jmk-foofus/medusa)
*   **Post-Exploitation:** [PowerShell Empire](https://github.com/EmpireProject/Empire), [SharpHound](https://github.com/BloodHoundAD/SharpHound), [Rubeus](https://github.com/GhostPack/Rubeus)
*   **Mobile & Binary:** [jadx](https://github.com/skylot/jadx), [Apktool](https://apktool.org/), [Objection](https://github.com/sensepost/objection), [GDB-PEDA](https://github.com/longld/peda)
*   **Cloud & AI:** [Pacu](https://github.com/RhinoSecurityLabs/pacu), [Prowler](https://github.com/prowler-cloud/prowler), [enumerate-iam](https://github.com/andresriancho/enumerate-iam), [S3Scanner](https://github.com/sa7mon/S3Scanner), [PyRIT](https://github.com/Azure/PyRIT), [LLM Guard](https://github.com/protectai/llm-guard)
*   **Automation:** [Scapy](https://scapy.net/), Requests (Python)

### 🥉 Good to Know (Priority: 44 Tools)
*Niche tools for specific scenarios.*
*   **OSINT:** [Maltego](https://www.maltego.com/), [DNSRecon](https://github.com/darkoperator/dnsrecon), [SpiderFoot](https://github.com/smicallef/spiderfoot), [Sherlock](https://github.com/sherlock-project/sherlock), [Recon-ng](https://github.com/lanmaster53/recon-ng), [httpx](https://github.com/projectdiscovery/httpx), [Masscan](https://github.com/robertdavidgraham/masscan), [Qualys](https://www.qualys.com/)
*   **Web/Network:** [Nexpose](https://www.rapid7.com/), [Acunetix](https://www.acunetix.com/), [Goby](https://gobies.org/), [BeEF](https://beefproject.com/), [Fiddler](https://www.telerik.com/fiddler), HTTP Toolkit, [mitmproxy](https://mitmproxy.org/), [Aircrack-ng](https://www.aircrack-ng.org/), [bettercap](https://www.bettercap.org/), Ncrack, [Patator](https://github.com/lanjelot/patator)
*   **C2 & Pentest Suites:** [Cobalt Strike](https://www.cobaltstrike.com/), [Covenant](https://github.com/cobbr/Covenant), [Penelope](https://github.com/brightio/penelope)
*   **Mobile & Binary:** [APKLab](https://github.com/APKLab/APKLab), [Magisk](https://github.com/topjohnwu/Magisk), [Checkra1n](https://checkra.in/), [dnSpy](https://github.com/dnSpy/dnSpy), [Hopper](https://www.hopperapp.com/), [Ciphey](https://github.com/Ciphey/Ciphey), [hashID](https://github.com/psypanda/hashID), [PEiD](https://www.aldeid.com/wiki/PEiD), [x64dbg](https://x64dbg.com/)
*   **Cloud & AI:** [CloudSploit](https://github.com/aquasecurity/cloudsploit), [AzureHound](https://github.com/BloodHoundAD/AzureHound), [GCPBucketBrute](https://github.com/RhinoSecurityLabs/GCPBucketBrute), [CrackStation](https://crackstation.net/), [Legba](https://github.com/evilsocket/legba), [Serpico](https://github.com/SerpicoProject/Serpico), [Rebuff](https://github.com/protectai/rebuff), [NeMo Guardrails](https://github.com/NVIDIA/NeMo-Guardrails), [TextAttack](https://github.com/QData/TextAttack), [Adversarial Robustness Toolbox](https://github.com/Trusted-AI/adversarial-robustness-toolbox)
*   **Automation:** [Selenium](https://www.selenium.dev/), [Ansible](https://www.ansible.com/), [Terraform](https://www.terraform.io/)

---

## 🗺️ The 22-Project Roadmap (Fresher to Pro)

Building projects proves you are self-driven and understand the full lifecycle. Here are 22 projects categorized by difficulty and domain.

### 🟢 Beginner Projects
1.  **Web App VAPT:** Exploit DVWA or Juice Shop. Cover SQLi, XSS, CSRF, file upload, IDOR. Write a full professional report.
2.  **Network VAPT:** Scan Metasploitable 2/3. Exploit EternalBlue, VSFTPD backdoor, Samba. Get a shell. Document everything.
3.  **Vulnerability Assessment & Remediation:** Run OpenVAS/Nessus on a lab network. Document findings, CVSS scores, and create a remediation plan.
4.  **Log Analyzer & SIEM:** Build a Python/Splunk dashboard to parse logs, detect failed logins, and generate alerts.
5.  **File Integrity Monitor:** Create a Python script that hashes files and alerts on unauthorized changes (FIM).

### 🟡 Intermediate Projects
6.  **Recon Automation Script:** Write a Bash/Python script that runs masscan + Nmap + ffuf and outputs a clean report.
7.  **Cloud VAPT (AWS):** Scan a deliberately misconfigured AWS S3 bucket. Test IAM privilege escalation. Report findings.
8.  **Cloud VAPT (Azure):** Use ScoutSuite or Prowler to audit an Azure environment. Identify public storage, weak NSGs.
9.  **Mobile App VAPT:** Use MobSF and Frida on an Android APK. Test for insecure storage, hardcoded secrets, SSL pinning bypass.
10. **API Security Testing:** Target a vulnerable API (OWASP API Top 10). Test BOLA, JWT forgery, mass assignment. Report.
11. **AI-Powered Phishing Detection:** Build a Python classifier (scikit-learn) to detect phishing emails based on headers and body text.
12. **Malware Analysis Lab:** Analyze a harmless malware sample in a VM. Document IOCs, behavior, and network traffic.
13. **Cloud Security Posture Audit:** Use Prowler or ScoutSuite to audit a full AWS account. Generate a compliance report (CIS, NIST).
14. **Wireless Security Testing:** Use Aircrack-ng and bettercap to capture and crack a WPA2 handshake (in a lab).
15. **Automated VAPT Report Generator:** Build a Python tool that takes scanner output and auto-generates a PDF report with CVSS scores.
16. **Honeypot Deployment & Analysis:** Deploy Cowrie SSH honeypot. Capture attacker IPs, commands, and analyze patterns.

### 🔴 Advanced Projects
17. **Active Directory VAPT:** Use TryHackMe AD rooms. Perform Kerberoasting, Pass-the-Hash, BloodHound mapping. Escalate to Domain Admin.
18. **AI/LLM VAPT:** Set up a local LLM (Ollama). Test prompt injection, jailbreak, data leak. Write a red team report.
19. **Log4Shell Exploit:** Set up a vulnerable Log4j app. Exploit JNDI lookup to achieve RCE. Document the chain.
20. **Binary Exploitation:** Exploit a stack overflow in a CTF binary. Build a ROP chain to bypass protections.
21. **AI Red Team Agent:** Build a Python-based agent that uses an LLM API to automate recon and vulnerability discovery.
22. **Container/Kubernetes VAPT:** Set up a vulnerable K8s cluster. Test for misconfigurations, container escape, RBAC abuse.

---

## 🧠 What Matters More Than 22 Projects?

Having 22 projects proves you are passionate and better than 95% of freshers. However, it **doesn't** prove you can handle real client pressure, work in a team, or meet deadlines. To get hired, you must master these 5 soft skills:

1.  **Can you explain the attack chain?** — From recon to retest. Tell it as one story.
2.  **Can you write a professional report?** — This is what clients actually pay for.
3.  **Can you think like an attacker?** — Not just run tools.
4.  **Do you have a certification?** — HR filters are real. CEH/eJPT/OSCP will open doors.
5.  **Can you communicate?** — In an interview, you must explain technical concepts to non-technical people.

---

## 📊 Knowledge Coverage Matrix

If you complete the roadmap above, here is your expected coverage level across major domains:

| Domain | Coverage | Key Focus Areas |
| :--- | :--- | :--- |
| **Web App VAPT** | 90% | SQLi, XSS, CSRF, SSRF, IDOR, File Upload, JWT, API |
| **Reporting** | 90% | Executive Summary, CVSS, Remediation, Retest |
| **Network VAPT** | 85% | Nmap, Metasploit, EternalBlue, SMB, Password Attacks |
| **Active Directory** | 75% | Mimikatz, BloodHound, Kerberoasting, Lateral Movement |
| **Cloud VAPT** | 70% | AWS/Azure Misconfig, IAM, S3, ScoutSuite, Prowler |
| **Automation** | 70% | Python, Bash, Custom Scripts, Report Generators |
| **Mobile VAPT** | 60% | MobSF, Frida, APK Analysis, SSL Pinning Bypass |
| **AI/LLM VAPT** | 50% | Prompt Injection, Jailbreak, Garak, PyRIT |

*Overall: You will have broad coverage across all major VAPT domains. This is more than enough for a fresher role.*
