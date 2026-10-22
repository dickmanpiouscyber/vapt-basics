# 🛡️ The Ultimate VAPT (Vulnerability Assessment & Penetration Testing) & OSINT Master Guide

Welcome to the comprehensive guide for mastering VAPT and OSINT. This repository contains everything you need to understand the complete attack lifecycle, the exact tools required (including specialized search engines), a 22-project roadmap to build your portfolio, and the real-world expectations of a security engineer.

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

## 🛠️ The 101-Tool VAPT Arsenal (Categorized by Function)

Here is the massive categorized list of tools you need to master, ranked by priority.

### 🥇 Must Master (Priority: 27 Tools)
*These are non-negotiable for any VAPT role.*
*   **Recon & OSINT:** Nmap, Shodan, WHOIS, Google Dorking
*   **Vulnerability Scanning:** Nessus, OpenVAS
*   **Web App Exploitation:** Burp Suite, SQLmap, OWASP ZAP
*   **Network Exploitation:** Metasploit, Hydra, John the Ripper
*   **Post-Exploitation:** Mimikatz, BloodHound
*   **Mobile & Cloud:** Frida, MobSF, Ghidra, AWS CLI, ScoutSuite
*   **Cracking & Reporting:** Hashcat, Dradis, CVSS Calculator, Microsoft Word
*   **AI/LLM & Scripting:** Garak, Python, Bash, PowerShell

### 🥈 Should Know (Priority: 30 Tools)
*Elevates you above standard testers.*
*   **Recon:** theHarvester, Amass, Subfinder, Nikto, Nuclei, Postman, ffuf, Gobuster
*   **Web Testing:** Responder
*   **Credential Attacks:** Hashcat, CrackMapExec, Impacket, Medusa
*   **Post-Exploitation:** PowerShell Empire, SharpHound, Rubeus
*   **Mobile & Binary:** jadx, Apktool, Objection, GDB-PEDA
*   **Cloud & AI:** Pacu, Prowler, enumerate-iam, S3Scanner, PyRIT, LLM Guard
*   **Automation:** Scapy, Requests (Python)

### 🥉 Good to Know (Priority: 44 Tools)
*Niche tools for specific scenarios.*
*   **OSINT & Network:** Maltego, DNSRecon, SpiderFoot, Sherlock, Recon-ng, httpx, Masscan, Qualys, Nexpose, Acunetix, Goby, BeEF, Fiddler, HTTP Toolkit, mitmproxy, Aircrack-ng, bettercap, Cobalt Strike, Covenant, Penelope
*   **Mobile & Binary:** APKLab, Magisk, Checkra1n, dnSpy, Hopper, Ciphey, hashID, PEiD, x64dbg
*   **Cloud & AI:** CloudSploit, AzureHound, GCPBucketBrute, Ncrack, Patator, CrackStation, Legba, Serpico, Rebuff, NeMo Guardrails, TextAttack, Adversarial Robustness Toolbox
*   **Automation:** Selenium, Ansible, Terraform

---

## 🔍 The Ultimate OSINT & Pentesting Search Engine Master List
*Specialized engines that index what Google ignores: exposed devices, leaked code, open S3 buckets, and historical DNS data.*
*(♻️ = Core tools from the original graphic)*

### 🖥️ 1. Attack Surface & Internet Asset Discovery
*   [Shodan](https://shodan.io) ♻️ - Search engine for IoT and exposed devices.
*   [Censys](https://censys.io) ♻️ - Search engine for internet-connected hosts and TLS certificates.
*   [ZoomEye](https://zoomeye.org) ♻️ - Cyberspace search engine; good for ICS and Asian infrastructure.
*   [BinaryEdge](https://app.binaryedge.io) ♻️ - Continuous internet scanning and attack surface mapping.
*   [FOFA](https://fofa.info) ♻️ - Cyberspace mapping; strong on protocol fingerprints.
*   [FullHunt](https://fullhunt.io) ♻️ - Attack surface discovery and exposure management.
*   [Netlas](https://app.netlas.io) ♻️ - Search engine for internet assets and HTTP responses.
*   [Onyphe](https://onyphe.io) ♻️ - Cyber defense search engine for pivoting IPs and certificates.
*   [Criminal IP](https://www.criminalip.io) - Asset inventory, risk assessment, and threat intelligence.
*   [Hunter.how](https://hunter.how) - Search engine for internet-connected devices.
*   [Odin](https://odin.io) - Powerful search engine for scanned internet assets.

### 💻 2. Code & Source Intelligence
*   [Grep.app](https://grep.app) ♻️ - Regex search across public GitHub repositories.
*   [PublicWWW](https://publicwww.com) ♻️ - Search the source code of live websites.
*   [SearchCode](https://searchcode.com) ♻️ - Searches 75 billion lines of code from open-source projects.
*   [GitHub Code Search](https://github.com/search) - Native search for public GitHub repositories.
*   [Sourcegraph](https://sourcegraph.com) - Enterprise-grade universal code search.
*   [DorkSearch](https://dorksearch.com) - Fast interface for advanced Google Dorking.
*   [GitSeek](https://gitseek.dev) - Extracts specific code from repositories for AI workflows.
*   [Repogrep](https://repogrep.app) - AI chat interface for searching GitHub repositories.

### 🌐 3. DNS, Domain & Certificate Intelligence
*   [crt.sh](https://crt.sh) ♻️ - Clean and fast Certificate Transparency log search for subdomains.
*   [URLScan](https://urlscan.io) ♻️ - Free service to scan and analyze websites.
*   [WiGLE](https://wigle.net) ♻️ - Database of wireless networks worldwide.
*   [SecurityTrails](https://securitytrails.com) - Deep historical DNS and domain intelligence.
*   [DNSDumpster](https://dnsdumpster.com) - Visual DNS reconnaissance and mapping.
*   [VirusTotal](https://virustotal.com) - Malware analysis and domain/IP intelligence.
*   [Wayback Machine](https://archive.org/web/) - View content from deleted or historical websites.
*   [Certspotter](https://sslmate.com/certspotter/) - Free Certificate Transparency log search.
*   [DNSDB](https://www.farsightsecurity.com/solutions/dnsdb/) - Historical DNS data search.
*   [SSLBoard](https://sslboard.com) - crt.sh alternative with a visual subdomain map.

### 🕵️ 4. Leaks, Credentials & Breach Data
*   [IntelligenceX](https://intelx.io) ♻️ - Broad OSINT search covering Tor, I2P, data leaks, and pastes.
*   [LeakIX](https://leakix.net) ♻️ - Focuses on publicly indexed open services and leaked info.
*   [DeHashed](https://dehashed.com) - Indexes leaked credentials from public breaches.
*   [HudsonRock](https://www.hudsonrock.com) - Search for compromised credentials via infostealers.
*   [0t.rocks](https://0t.rocks) - Massive records and breach search engine.

### 🦠 5. Threat Intelligence & Internet Noise
*   [GreyNoise](https://viz.greynoise.io) ♻️ - Tells you which IPs are just background internet noise.
*   [Pulsedive](https://pulsedive.com) ♻️ - Threat intelligence search engine.
*   [Socradar](https://socradar.io) ♻️ - Threat intelligence and digital risk protection.
*   [AlienVault OTX](https://otx.alienvault.com) - Extensive threat intelligence feed and community.
*   [PolySwarm](https://polyswarm.network) - Scan files and URLs for threats.

### 🐛 6. Vulnerability & Exploit Databases
*   [Vulners](https://vulners.com) ♻️ - Aggregated vulnerability database with a strong API.
*   [Exploit-DB](https://www.exploit-db.com) - The canonical archive of public exploits.
*   [Packet Storm Security](https://packetstormsecurity.com) - Archive of latest vulnerabilities and exploits.

### 📧 7. Email, Communication & Social OSINT
*   [Hunter.io](https://hunter.io) ♻️ - Find email addresses associated with a domain.
*   [Lyzem](https://lyzem.com) - Search engine for Telegram.
*   [TGStat](https://tgstat.com) - Telegram channel statistics and search.
*   [FindADiscord](https://findadiscord.com) - Discord search engine.
*   [WhatsMyName](https://whatsmyname.app) - Web-based username enumeration across platforms.

### 🔍 8. General Web & Google Dorking
*   [Google.com](https://google.com) ♻️ - The original; use advanced search operators (Dorks).
*   [OSINT Framework](https://osintframework.com) - A massive directory of OSINT tools.
*   [Hackyx](https://hackyx.io) - Find CTF writeups, articles, and bug bounty reports.

### ☁️ 9. Cloud & Storage Exposure
*   [GrayHatWarfare](https://grayhatwarfare.com) - Searches public S3, GCS, and Azure Blob buckets.

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
