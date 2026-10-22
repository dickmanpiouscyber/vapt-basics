# 🛡️ The Ultimate VAPT & OSINT Master Guide

Welcome to the comprehensive guide for mastering VAPT and OSINT. This repository contains everything you need to understand the complete attack lifecycle, the exact 101 tools required (ranked by priority and alphabetized), specialized search engines, a 22-project roadmap, and the real-world expectations of a security engineer.

---

## 🩺 The VAPT Lifecycle (The Doctor Analogy)

To understand VAPT, think of a security engineer as a doctor diagnosing a patient. You cannot just start "cutting" (hacking) without a diagnosis.

| # | Doctor Analogy | VAPT Phase | What You Actually Do | Tools Used |
| :--- | :--- | :--- | :--- | :--- |
| **1** | **Consent Form**<br>*(Patient agrees to treatment & points to pain area)* | **Scoping & RoE**<br>*(Rules of Engagement)* | Sign legal contract (NDA & SOW). Define exactly which IPs/websites you can attack and which you must **not** touch. *(No permission = illegal hacking).* | Pen & Paper, NDA/SOW |
| **2** | **Check-Up & Vitals**<br>*(Checks BP, asks history — no surgery yet)* | **Reconnaissance**<br>*(Information Gathering)* | Scan external network. Find open ports, OS versions, software. Look for leaked emails and subdomains. | Nmap, Shodan, theHarvester, Amass |
| **3** | **Blood Test & X-Ray**<br>*(Finds a suspicious spot but hasn't proven it)* | **Vulnerability Assessment**<br>*(Scanning)* | Run automated scanners to find **potential** weaknesses (missing patches, outdated plugins). Filter false positives. | Nessus, OpenVAS, Burp Scanner, Nikto |
| **4** | **Surgery / Biopsy**<br>*(Cuts in to PROVE disease is real)* | **Penetration Testing**<br>*(Exploitation)* | **Actually exploit** the vulnerabilities. Break into the server. Prove the risk is real, not theoretical. | Metasploit, SQLmap, Hydra, Burp Repeater |
| **5** | **Checking for Metastasis**<br>*(Has cancer spread to other organs?)* | **Post-Exploitation**<br>*(Lateral Movement)* | After getting in, find passwords, move to the next server, escalate from normal user to Domain Admin. | Mimikatz, BloodHound, Cobalt Strike |
| **6** | **Prescription & Treatment**<br>*(Doctor writes a plan)* | **Reporting & Remediation**<br>*(The Final Report)* | Write a report explaining the risk in business terms + exact technical fixes (patches, MFA, segmentation). | Word, CVSS Calculator, Dradis |
| **7** | **Follow-Up Visit**<br>*(Did medicine work?)* | **Retesting**<br>*(Verification)* | After client applies fixes, try to hack them again. Confirm "Fixed" or "Still Vulnerable." Deliver a Retest Report. | Same exploit tools (again) |

### 👨‍💻 Experience Needed (Fresher vs Senior) & What a Fresher Can Do
*   **Phase 1 (Scoping):** No technical experience needed. *Fresher action:* Read the NDA. Understand which IPs are in scope. Do not touch anything outside.
*   **Phase 2 (Recon):** Low experience. Tools do most of the work. *Fresher action:* Run Nmap, Shodan, theHarvester. Copy-paste results into a document.
*   **Phase 3 (Scan):** Low experience. Scanners are automated. *Fresher action:* Run Nessus/OpenVAS. Filter out false positives. Export the report.
*   **Phase 4 (Exploit):** High experience. Requires deep understanding. *Fresher action:* Use Metasploit modules. Follow walkthroughs (TryHackMe/HackTheBox). Get a basic shell.
*   **Phase 5 (Post-Exploit):** Very High experience. Requires AD knowledge. *Fresher action:* Just document what you find. Do not attempt complex lateral movement as a fresher.
*   **Phase 6 (Report):** Low-Medium experience. Writing matters more. *Fresher action:* Write the Executive Summary. Use CVSS calculator. Suggest basic fixes.
*   **Phase 7 (Retest):** Low experience. *Fresher action:* Re-run the same exploit. Screenshot "Fixed" or "Still Vulnerable."

---

## 🛠️ The 101-Tool Arsenal (Alphabetical by Priority)

Here are all 101 tools extracted exactly as categorized by priority, sorted alphabetically for easy reference.

### 🥇 Must Master (27 Tools)
*These are non-negotiable for any VAPT role.*
*   **AWS CLI** - Command-line tool for managing AWS services. [Link](https://aws.amazon.com/cli/)
*   **Bash** - Unix shell and command language for scripting automation. [Link](https://www.gnu.org/software/bash/)
*   **BloodHound** - Uses graph theory to reveal hidden relationships and attack paths in Active Directory. [Link](https://github.com/BloodHoundAD/BloodHound)
*   **Burp Suite** - Leading web application security testing platform. [Link](https://portswigger.net/burp)
*   **CVSS Calculator** - Standardized scoring system for vulnerability severity. [Link](https://www.first.org/cvss/calculator/3.1)
*   **Dradis** - Collaboration and reporting platform for security teams. [Link](https://dradisframework.com/)
*   **Frida** - Dynamic code instrumentation toolkit for mobile apps. [Link](https://frida.re/)
*   **Garak** - LLM vulnerability scanner (AI red teaming). [Link](https://github.com/leondz/garak)
*   **Ghidra** - NSA's software reverse engineering (SRE) suite. [Link](https://ghidra-sre.org/)
*   **Google Dorking** - Using advanced search operators to find exposed data. [Link](https://www.google.com/)
*   **Hashcat** - Advanced password recovery and cracking utility. [Link](https://hashcat.net/hashcat/)
*   **Hydra** - Fast network logon cracker (password brute-forcer). [Link](https://github.com/vanhauser-thc/thc-hydra)
*   **John the Ripper** - Fast password cracker. [Link](https://www.openwall.com/john/)
*   **Metasploit** - The world's most used penetration testing framework. [Link](https://www.metasploit.com/)
*   **Microsoft Word** - Standard tool for writing professional VAPT reports. [Link](https://www.microsoft.com/microsoft-365/word)
*   **Mimikatz** - Extracts plaintext passwords, hashes, and Kerberos tickets from memory. [Link](https://github.com/gentilkiwi/mimikatz)
*   **MobSF** - Mobile Security Framework for automated app testing. [Link](https://github.com/MobSF/Mobile-Security-Framework-MobSF)
*   **Nessus** - Industry-standard vulnerability scanner. [Link](https://www.tenable.com/)
*   **Nmap** - The standard network discovery and port scanner. [Link](https://nmap.org/)
*   **OpenVAS** - Open-source vulnerability scanner. [Link](https://www.openvas.org/)
*   **OWASP ZAP** - Open-source web app security scanner. [Link](https://www.zaproxy.org/)
*   **PowerShell** - Task automation and configuration management framework. [Link](https://microsoft.com/powershell)
*   **Python** - General-purpose programming language for custom exploits and automation. [Link](https://www.python.org/)
*   **ScoutSuite** - Multi-cloud security auditing tool. [Link](https://github.com/nccgroup/ScoutSuite)
*   **Shodan** - Search engine for Internet-connected devices. [Link](https://shodan.io/)
*   **SQLmap** - Automatic SQL injection and database takeover tool. [Link](https://sqlmap.org/)
*   **WHOIS** - Query and response protocol for domain registration data. [Link](https://www.whois.com/)

### 🥈 Should Know (30 Tools)
*Elevates you above standard testers.*
*   **Amass** - In-depth DNS enumeration and network mapping. [Link](https://github.com/owasp-amass/amass)
*   **Apktool** - Reverse engineering tool for Android APK files. [Link](https://apktool.org/)
*   **CrackMapExec** - Swiss army knife for pentesting Windows/AD networks. [Link](https://github.com/byt3bl33d3r/CrackMapExec)
*   **enumerate-iam** - Brute-forces AWS IAM permissions. [Link](https://github.com/andresriancho/enumerate-iam)
*   **ffuf** - Fast web fuzzer written in Go. [Link](https://github.com/ffuf/ffuf)
*   **GDB-PEDA** - Python Exploit Development Assistance for GDB. [Link](https://github.com/longld/peda)
*   **Gobuster** - Directory/file & DNS busting tool. [Link](https://github.com/OJ/gobuster)
*   **Hashcat** - Advanced password recovery. *(Also listed in Must Master)*. [Link](https://hashcat.net/hashcat/)
*   **Impacket** - Collection of Python classes for working with network protocols. [Link](https://github.com/fortra/impacket)
*   **jadx** - Dex to Java decompiler for Android apps. [Link](https://github.com/skylot/jadx)
*   **LLM Guard** - Toolkit for LLM security and safety. [Link](https://github.com/protectai/llm-guard)
*   **Medusa** - Speedy, parallel, modular login brute-forcer. [Link](https://github.com/jmk-foofus/medusa)
*   **Nikto** - Web server scanner for dangerous files and outdated software. [Link](https://github.com/sullo/nikto)
*   **Nuclei** - Fast, template-based vulnerability scanner. [Link](https://github.com/projectdiscovery/nuclei)
*   **Objection** - Runtime mobile exploration toolkit. [Link](https://github.com/sensepost/objection)
*   **Pacu** - AWS exploitation framework. [Link](https://github.com/RhinoSecurityLabs/pacu)
*   **PlexTrac** - Reporting and collaboration platform. [Link](https://plextrac.com/)
*   **Postman** - API platform for building and testing APIs. [Link](https://www.postman.com/)
*   **PowerShell Empire** - Post-exploitation framework. [Link](https://github.com/EmpireProject/Empire)
*   **Prowler** - AWS/Azure/GCP security assessments and auditing. [Link](https://github.com/prowler-cloud/prowler)
*   **PyRIT** - Python Risk Identification Tool for generative AI. [Link](https://github.com/Azure/PyRIT)
*   **Requests** - Elegant HTTP library for Python. [Link](https://requests.readthedocs.io/)
*   **Responder** - LLMNR, NBT-NS and MDNS poisoner. [Link](https://github.com/lgandx/Responder)
*   **Rubeus** - C# toolset for raw Kerberos interaction. [Link](https://github.com/GhostPack/Rubeus)
*   **S3Scanner** - Scan for open S3 buckets and dump contents. [Link](https://github.com/sa7mon/S3Scanner)
*   **Scapy** - Python-based interactive packet manipulation program. [Link](https://scapy.net/)
*   **SharpHound** - C# data collector for BloodHound. [Link](https://github.com/BloodHoundAD/SharpHound)
*   **Subfinder** - Fast subdomain discovery tool. [Link](https://github.com/projectdiscovery/subfinder)
*   **SysReptor** - Fully customisable pentest reporting platform. [Link](https://github.com/Syslifters/sysreptor)
*   **theHarvester** - E-mail, subdomain and people names harvester. [Link](https://github.com/laramies/theHarvester)

### 🥉 Good to Know (44 Tools)
*Niche tools for specific scenarios.*
*   **Acunetix** - Automated web vulnerability scanner. [Link](https://www.acunetix.com/)
*   **Adversarial Robustness Toolbox** - Library for AI/ML security. [Link](https://github.com/Trusted-AI/adversarial-robustness-toolbox)
*   **Aircrack-ng** - Complete suite for WiFi security auditing. [Link](https://www.aircrack-ng.org/)
*   **Ansible** - IT automation engine. [Link](https://www.ansible.com/)
*   **APKLab** - VS Code extension for reverse engineering APKs. [Link](https://github.com/APKLab/APKLab)
*   **AzureHound** - BloodHound data collector for Azure. [Link](https://github.com/BloodHoundAD/AzureHound)
*   **BeEF** - Browser Exploitation Framework. [Link](https://beefproject.com/)
*   **bettercap** - Swiss army knife for network attacks and monitoring. [Link](https://www.bettercap.org/)
*   **Checkra1n** - Jailbreak tool for iOS devices. [Link](https://checkra.in/)
*   **Ciphey** - Automated decryption and decoding tool. [Link](https://github.com/Ciphey/Ciphey)
*   **CloudSploit** - Cloud security scanning and monitoring. [Link](https://github.com/aquasecurity/cloudsploit)
*   **Cobalt Strike** - Commercial penetration testing and adversary simulation tool. [Link](https://www.cobaltstrike.com/)
*   **Covenant** - Collaborative .NET C2 framework. [Link](https://github.com/cobbr/Covenant)
*   **CrackStation** - Massive pre-computed password hash database. [Link](https://crackstation.net/)
*   **dnSpy** - .NET debugger and assembly editor. [Link](https://github.com/dnSpy/dnSpy)
*   **DNSRecon** - DNS enumeration and scanning script. [Link](https://github.com/darkoperator/dnsrecon)
*   **Fiddler** - Web debugging proxy. [Link](https://www.telerik.com/fiddler)
*   **GCPBucketBrute** - Enumerate and brute-force GCP storage buckets. [Link](https://github.com/RhinoSecurityLabs/GCPBucketBrute)
*   **Goby** - Attack surface mapping and vulnerability scanner. [Link](https://gobies.org/)
*   **hashID** - Identify different types of hashes. [Link](https://github.com/psypanda/hashID)
*   **Hopper** - Reverse engineering tool for macOS and Linux. [Link](https://www.hopperapp.com/)
*   **HTTP Toolkit** - Intercept, debug and mock HTTP(S). [Link](https://httptoolkit.com/)
*   **httpx** - Fast and multi-purpose HTTP toolkit. [Link](https://github.com/projectdiscovery/httpx)
*   **Legba** - A multiprotocol credentials bruteforcer. [Link](https://github.com/evilsocket/legba)
*   **Magisk** - Rooting solution for Android. [Link](https://github.com/topjohnwu/Magisk)
*   **Maltego** - OSINT and graphical link analysis tool. [Link](https://www.maltego.com/)
*   **Masscan** - The fastest Internet port scanner. [Link](https://github.com/robertdavidgraham/masscan)
*   **mitmproxy** - Interactive TLS-capable intercepting HTTP proxy. [Link](https://mitmproxy.org/)
*   **Ncrack** - High-speed network authentication cracking tool. [Link](https://nmap.org/ncrack/)
*   **NeMo Guardrails** - Toolkit for LLM guardrails. [Link](https://github.com/NVIDIA/NeMo-Guardrails)
*   **Nexpose** - Vulnerability management scanner by Rapid7. [Link](https://www.rapid7.com/)
*   **Patator** - Multi-purpose brute-forcer. [Link](https://github.com/lanjelot/patator)
*   **PEiD** - PE file identifier and signature scanner. [Link](https://www.aldeid.com/wiki/PEiD)
*   **Penelope** - Shell handler and post-exploitation tool. [Link](https://github.com/brightio/penelope)
*   **Qualys** - Cloud-based security and compliance platform. [Link](https://www.qualys.com/)
*   **Rebuff** - LLM prompt injection detector. [Link](https://github.com/protectai/rebuff)
*   **Recon-ng** - Full-featured Web Reconnaissance framework. [Link](https://github.com/lanmaster53/recon-ng)
*   **Selenium** - Browser automation framework. [Link](https://www.selenium.dev/)
*   **Serpico** - Penetration testing reporting tool. [Link](https://github.com/SerpicoProject/Serpico)
*   **Sherlock** - Hunt down social media accounts by username. [Link](https://github.com/sherlock-project/sherlock)
*   **SpiderFoot** - Automated OSINT collection. [Link](https://github.com/smicallef/spiderfoot)
*   **Terraform** - Infrastructure as Code (IaC) tool. [Link](https://www.terraform.io/)
*   **TextAttack** - Framework for adversarial attacks in NLP. [Link](https://github.com/QData/TextAttack)
*   **x64dbg** - Open-source x64/x32 debugger for Windows. [Link](https://x64dbg.com/)

---

## 🔍 The Ultimate OSINT & Pentesting Search Engine Master List
*Specialized engines that index what Google ignores.*
*(♻️ = Core tools from the original graphic)*

### 🖥️ 1. Attack Surface & Internet Asset Discovery
*   [Shodan](https://shodan.io) ♻️ - Search engine for IoT and exposed devices.
*   [Censys](https://censys.io) ♻️ - Search engine for internet-connected hosts.
*   [ZoomEye](https://zoomeye.org) ♻️ - Cyberspace search engine; good for ICS.
*   [BinaryEdge](https://app.binaryedge.io) ♻️ - Continuous internet scanning.
*   [FOFA](https://fofa.info) ♻️ - Cyberspace mapping; protocol fingerprints.
*   [FullHunt](https://fullhunt.io) ♻️ - Attack surface discovery.
*   [Netlas](https://app.netlas.io) ♻️ - Search engine for internet assets.
*   [Onyphe](https://onyphe.io) ♻️ - Cyber defense search engine.
*   [Criminal IP](https://www.criminalip.io) - Asset inventory and risk assessment.
*   [Hunter.how](https://hunter.how) - Search engine for internet-connected devices.
*   [Odin](https://odin.io) - Search engine for scanned internet assets.

### 💻 2. Code & Source Intelligence
*   [Grep.app](https://grep.app) ♻️ - Regex search across public GitHub.
*   [PublicWWW](https://publicwww.com) ♻️ - Search live website source code.
*   [SearchCode](https://searchcode.com) ♻️ - Searches 75B lines of code.
*   [GitHub Code Search](https://github.com/search) - Native GitHub search.
*   [Sourcegraph](https://sourcegraph.com) - Universal code search.
*   [DorkSearch](https://dorksearch.com) - Fast Google Dorking interface.
*   [GitSeek](https://gitseek.dev) - Extracts code for AI workflows.
*   [Repogrep](https://repogrep.app) - AI chat for GitHub repos.

### 🌐 3. DNS, Domain & Certificate Intelligence
*   [crt.sh](https://crt.sh) ♻️ - Certificate Transparency log search.
*   [URLScan](https://urlscan.io) ♻️ - Scan and analyze websites.
*   [WiGLE](https://wigle.net) ♻️ - Database of wireless networks.
*   [SecurityTrails](https://securitytrails.com) - Historical DNS intelligence.
*   [DNSDumpster](https://dnsdumpster.com) - Visual DNS recon.
*   [VirusTotal](https://virustotal.com) - Malware and domain intelligence.
*   [Wayback Machine](https://archive.org/web/) - Historical websites.
*   [Certspotter](https://sslmate.com/certspotter/) - CT log search.
*   [DNSDB](https://www.farsightsecurity.com/solutions/dnsdb/) - Historical DNS data.
*   [SSLBoard](https://sslboard.com) - Visual subdomain map from CT logs.

### 🕵️ 4. Leaks, Credentials & Breach Data
*   [IntelligenceX](https://intelx.io) ♻️ - OSINT covering Tor, I2P, and leaks.
*   [LeakIX](https://leakix.net) ♻️ - Publicly indexed open services.
*   [DeHashed](https://dehashed.com) - Leaked credentials from breaches.
*   [HudsonRock](https://www.hudsonrock.com) - Compromised credentials via infostealers.
*   [0t.rocks](https://0t.rocks) - Massive records and breach search.

### 🦠 5. Threat Intelligence & Internet Noise
*   [GreyNoise](https://viz.greynoise.io) ♻️ - Identifies background internet noise.
*   [Pulsedive](https://pulsedive.com) ♻️ - Threat intelligence search.
*   [Socradar](https://socradar.io) ♻️ - Threat intel and risk protection.
*   [AlienVault OTX](https://otx.alienvault.com) - Threat intel feed.
*   [PolySwarm](https://polyswarm.network) - Scan files and URLs for threats.

### 🐛 6. Vulnerability & Exploit Databases
*   [Vulners](https://vulners.com) ♻️ - Aggregated vulnerability database.
*   [Exploit-DB](https://www.exploit-db.com) - Archive of public exploits.
*   [Packet Storm](https://packetstormsecurity.com) - Latest vulns and exploits.

### 📧 7. Email, Communication & Social OSINT
*   [Hunter.io](https://hunter.io) ♻️ - Find emails for a domain.
*   [Lyzem](https://lyzem.com) - Telegram search engine.
*   [TGStat](https://tgstat.com) - Telegram channel stats.
*   [FindADiscord](https://findadiscord.com) - Discord search engine.
*   [WhatsMyName](https://whatsmyname.app) - Username enumeration.

### 🔍 8. General Web & Google Dorking
*   [Google.com](https://google.com) ♻️ - Use advanced search operators.
*   [OSINT Framework](https://osintframework.com) - Directory of OSINT tools.
*   [Hackyx](https://hackyx.io) - CTF writeups and bug bounty reports.

### ☁️ 9. Cloud & Storage Exposure
*   [GrayHatWarfare](https://grayhatwarfare.com) - Search public S3/GCS/Azure buckets.

---

## 🗺️ The 22-Project Roadmap (Fresher to Pro)

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
