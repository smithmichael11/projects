# Projects #

I have created a series of documents and videos to showcase my key technical projects. Dive in and explore the details, highlights, valuable skills developed. I delve into various projects, extracting valuable lessons and insights from each endeavor.

## Key Projects:

###Sapphire Quant Lab 

is a Python-based paper-trading command center designed to simulate a disciplined trading operations workflow. It combines expanded-universe market scanning, real-time candidate ranking, setup review, risk controls, officer-style decision oversight, money tracking, audit logs, reports, and a searchable Knowledge Base into one dashboard. The system is built around safety-first principles: scanner results do not equal trade approval, proposals must pass review gates, paper trade actions remain locked unless conditions are satisfied, and live trading is disabled by default.

Through this project, I strengthened my understanding of Python application structure, dashboard design, market-data workflows, runtime state management, safety gates, audit logging, and test-driven development. I also learned how important information architecture is when building operator-facing tools: a system can have strong logic, but it still needs a simple interface, clear source-of-truth data flow, and concise next-action guidance to be useful. The project helped me connect technical automation with financial technology, risk governance, trading psychology, and practical decision-support design.

### HomeShield CLI

# HomeShield CLI

### Local Home SOC Dashboard, Safe Network Scanner, and Privacy-First Security Reporting Tool

HomeShield CLI is a local-first cybersecurity project built in Python to help authorized users inventory, review, and harden their own home networks. It started as a safe network scanner and evolved into a lightweight home SOC dashboard with device identity management, SOC-style case tracking, evidence handling, remediation workflows, automation, PDF reporting, Gmail report delivery, and scrubbed demo mode for portfolio sharing.

The project was designed around one core principle: **useful defensive security without exploitation, credential attacks, payload capture, or unsafe automation.**

<img width="1904" height="938" alt="HomeShield overview dashboard" src="https://github.com/user-attachments/assets/4ba74997-bc60-48cf-9851-f32ec4a6a49e" />

---

## Why I Built This

Home networks are full of routers, phones, laptops, smart TVs, cameras, printers, guest devices, private/randomized MAC addresses, and stale network artifacts. Basic scans can create noise unless the results are tied to a clear source of truth.

I built HomeShield to answer practical questions:

* What devices are actually on the network?
* Which devices are known, unknown, guest, stale, or non-device artifacts?
* Which services are open and need review?
* What evidence supports each finding?
* What needs action, what has been accepted, and what has already been resolved?
* Can reports be generated without leaking private network data?

---

## Core Features

### Local SOC Dashboard

HomeShield includes a browser-based local dashboard for reviewing devices, findings, SOC cases, remediation actions, traffic summaries, evidence, reports, and automation status.

The dashboard uses two main sources of truth:

* **Devices** — asset identity, IP/MAC history, trust state, owner, zone, notes, and device profile data.
* **SOC / Issues** — case status, accepted risks, false positives, stale artifacts, remediation status, and analyst decisions.

This structure keeps the dashboard, reports, remediation views, and email summaries synchronized.

---

### Safe Scanner and Target Review

HomeShield performs safe, authorized service checks against approved local LAN targets. It is designed to avoid noisy or unsafe behavior.

Key scanner features include:

* Authorized-scope validation
* Safe scan profiles
* Scan target inclusion/exclusion logic
* Stale ARP and non-device artifact filtering
* Evidence-backed service review
* Scan history
* Preservation of accepted, resolved, and stale decisions
* No exploitation, brute force, credential testing, or payload capture

<img width="1897" height="812" alt="HomeShield scan target review" src="https://github.com/user-attachments/assets/33aef661-e6d2-4558-bfd4-64406198549c" />

---

### Device Identity Management

A major lesson from this project was that asset identity is harder than just reading an IP address. Devices move, MAC addresses randomize, stale ARP entries linger, and one physical device can appear multiple ways.

HomeShield tracks:

* Friendly device names
* Current IP and evidence IP
* Current MAC and evidence MAC
* Known IP/MAC history
* Private/randomized MAC behavior
* Device type, owner, room, and zone
* Trust state
* Identity confidence
* Stale and non-device artifacts
* Related issues, evidence, and history

This helped me learn how to separate **current identity** from **historical evidence** and avoid incorrect device attribution.

---

### SOC Case Workflow

HomeShield supports a local SOC-style workflow for:

* Open findings
* Needs-review items
* Accepted / monitored risks
* Resolved cases
* False positives
* Stale / non-device artifacts
* Analyst notes
* Evidence linking
* Remediation decisions

A decision made in the SOC view is reflected across the dashboard, reports, remediation pages, ATT&CK-style mappings, and weekly email summaries.

---

### Evidence and Reporting

HomeShield generates structured reports and evidence outputs, including:

* One-page home brief
* Home network summary
* Technical findings
* Remediation playbook
* SOC correlation report
* Device timeline
* Source-of-truth sync report
* Evidence index
* PDF reports
* Weekly email-ready summaries

Reports are designed to separate true action items from accepted risks, resolved items, false positives, and stale artifacts.

---

### Metadata-Only Traffic Review

Traffic review is privacy-conscious by default. HomeShield summarizes metadata only and does not capture payloads, credentials, camera streams, or message contents.

Traffic summaries can show:

* Top talkers
* New destinations
* Unknown device activity
* Guest activity
* Unusual ports
* Volume or timing anomalies
* Device-to-traffic correlation

<img width="1916" height="930" alt="HomeShield traffic metadata dashboard" src="https://github.com/user-attachments/assets/9f8b1cc4-cc26-4965-992e-b18ef01b58b1" />

---

## Automation and Weekly Reporting

HomeShield includes safe automation modes:

* `daily-light`
* `weekly-safe`
* `monthly-report`
* `qa-only`
* `quick-dashboard`
* `portfolio-demo`

Automation can reconcile devices, review scan targets, run safe LAN checks, refresh dashboard data, generate reports, produce PDFs, and send weekly report emails when explicitly enabled.

Automation does **not** automatically trust devices, close cases, accept risk, modify router settings, capture payloads, or perform offensive testing.

Weekly reporting includes:

* PDF attachments
* Safe default attachment policy
* Gmail SMTP support
* `.env`-only SMTP credentials
* No raw evidence, logs, traffic data, router snapshots, or registries attached by default
* Git privacy checks before source commits

---

## Portfolio / Demo Mode

HomeShield includes a scrubbed demo workflow for GitHub and portfolio use. Demo mode removes or replaces sensitive data such as:

* Real MAC addresses
* Real device names
* Personal notes
* Router snapshots
* Raw traffic data
* Raw telemetry
* Private assessment artifacts

This allows the dashboard and reports to be shown publicly without exposing real home-network details.

---

## Lessons Learned

### 1. Asset identity is a source-of-truth problem

A device is not just an IP address. DHCP leases, ARP tables, private MACs, hostnames, stale observations, and user-confirmed labels all need to be reconciled carefully.

### 2. A scanner is only useful if the results are explainable

Raw scan output can be noisy. I learned to add context: why a target was included, why another was excluded, what evidence supports a finding, and whether the issue is active, accepted, stale, or resolved.

### 3. Privacy has to be designed in from the beginning

Home network data can expose more than expected. I built scrub/demo mode, metadata-only traffic review, `.env` secret handling, safe email attachments, and Git privacy checks to reduce that risk.

### 4. Automation should assist analysts, not replace judgment

HomeShield can collect, refresh, summarize, and report, but it does not automatically trust devices, close cases, accept risk, or change router settings. Human review remains part of the workflow.

### 5. Good security tooling needs good UX

Adding clear dashboard actions, save buttons, friendly validation, drilldowns, reports, and status summaries made the tool more practical and less like a collection of scripts.

---

## Safety Model

HomeShield is intentionally defensive and local-only.

It does not perform:

* Exploitation
* Brute force attacks
* Credential guessing
* Credential capture
* Wi-Fi cracking
* Packet injection
* ARP poisoning
* Spoofing
* Malware behavior
* Public-network scanning by default
* Router/device configuration changes
* Automatic blocking or trust decisions
* Payload capture by default

HomeShield is intended only for networks the user owns, manages, or is authorized to test.

---

## Technologies Used

* Python
* Typer / CLI tooling
* Nmap-safe scan workflows
* JSON / CSV data handling
* HTML / Markdown / PDF report generation
* Gmail SMTP
* Local dashboard UI
* pytest
* Git / GitHub
* Router, ARP, DHCP, and Wi-Fi evidence analysis
* Metadata-only traffic summaries

---

## Project Value

HomeShield demonstrates practical cybersecurity and product-engineering ability: not just scanning a network, but building a safer workflow around discovery, identity, evidence, triage, remediation, reporting, privacy, automation, and portfolio-safe presentation.

It reflects the type of work I enjoy most: turning technical findings into clear decisions, usable tools, and defensible documentation.

 
### Home Network Penetration Testing Reporting & Legal Authorization Project | Dec. 2025 | Technology Law & Cybersecurity Engagement | Focus: Computer Fraud and Abuse Act (CFAA), Cybersecurity Legal Frameworks

•	Drafted comprehensive pre-engagement legal authorization suite including Authorization to Test, Rules of Engagement, Statement of Work, and Confidentiality Agreement; analyzed CFAA (18 U.S.C. § 1030) risk exposure and structured explicit written consent to distinguish authorized testing from unlawful access.

•	Defined scope boundaries, prohibited activities, and escalation procedures to mitigate civil and criminal liability; integrated legal governance controls with NIST/PTES technical methodology.

•	Performed internal penetration test on home network, migrating devices from ISP modem to hardened GL.iNet router with segregated LAN and Guest SSIDs.

•	Performed comprehensive network security assessments, vulnerability analysis, and embedded device hardening using industry-standard tools and methodologies. Practical expertise in network architecture design, including migrating home networks from ISP modem configurations to hardened router deployments with segregated wireless networks.

[Splunk Lab Security Assessment.pdf](https://github.com/user-attachments/files/24341908/Splunk.Lab.Security.Assessment.pdf)

[Master Services Agreement (MSA) and Rules of Engagement (RoE)-Network Penetration Testing.pdf](https://github.com/user-attachments/files/24281301/Master.Services.Agreement.MSA.and.Rules.of.Engagement.RoE.-Network.Penetration.Testing.pdf)


### Home Network Penetration Testing & Router Hardening Lab | Dec. 2025 | GL.iNet OpenWRT Security Assessment | Tools: Nmap, tcpdump, Dropbear SSH, OpenWRT/Linux, netstat

•	Performed internal penetration test on home network, migrating devices from ISP modem to hardened GL.iNet router with segregated LAN and Guest SSIDs.

•	Conducted reconnaissance using Nmap to identify 9 active hosts and enumerate services: hardened SSH with key-based authentication and disabled password login.

•	Deployed tcpdump f.or traffic monitoring and validated network segmentation through ARP/neighbor table analysis.

•	Identified service exposure on endpoints (printer interfaces, VNC, SMB) and provided prioritized remediation recommendations following NIST/PTES methodology.

[Network Penetration Testing Findings Report.pdf](https://github.com/user-attachments/files/24281303/Network.Penetration.Testing.Findings.Report.pdf)


### WordPress Security Governance & Legal Authorization | Dec. 2025 | Technology Law & Cybersecurity Engagement | Focus: Computer Fraud and Abuse Act (CFAA), Risk Governance

### WordPress Security Assessment & Containerized Lab | Dec. 2025| Authorized Web Application Security Assessment | Tools: Docker, WPScan, Nikto, Nmap, Apache/PHP, cURL

Project Title: WordPress Security Assessment Lab

Description: End-to-end security testing environment featuring containerized WordPress deployment, automated vulnerability scanning, and comprehensive security analysis. Demonstrates practical application of penetration testing methodologies, security tool proficiency, and professional documentation standards.
Technologies: Docker, WPScan, Nikto, Nmap, WordPress, MySQL, Apache, PHP, Linux

Highlights:

* Containerized infrastructure for isolated security testing
* Industry-standard vulnerability assessment tools
* MITRE ATT&CK framework mapping
* Professional security documentation and remediation guidance
* Ethical hacking with formal authorization scope
  
[Legal Authorization Authorized Internal Web Application Security Assessment.pdf](https://github.com/user-attachments/files/24281296/Legal.Authorization.Authorized.Internal.Web.Application.Security.Assessment.pdf)

[Authorized Internal Web Application Security Assessment.pdf](https://github.com/user-attachments/files/24281298/Authorized.Internal.Web.Application.Security.Assessment.pdf)


 ## Previous Projects:
 
### Cloud Security Azure Lab

Check out my Cloud Security Lab project where I demonstrate key concepts in cloud security, configuration, and implementation.

[![Watch Video](https://img.youtube.com/vi/4vj_CPOLSA4/0.jpg)](https://youtu.be/4vj_CPOLSA4)

## Basic Networking Labs

These labs showcase fundamental networking skills, providing hands-on experience in configuring devices, establishing secure network connections, and exploring key management techniques. Each video offers insights into essential networking concepts and practical applications, laying the groundwork for more advanced network design and security practices.

### Configuring End Devices
[![Watch Video](https://img.youtube.com/vi/7DktR__QbMs/0.jpg)](https://www.youtube.com/watch?v=7DktR__QbMs)

### Connecting to Web Server
[![Watch Video](https://img.youtube.com/vi/tOvSarxTjEQ/0.jpg)](https://www.youtube.com/watch?v=tOvSarxTjEQ)

### Compare In Band and Out of Band Management Access
[![Watch Video](https://img.youtube.com/vi/47c8dflBwyI/0.jpg)](https://www.youtube.com/watch?v=47c8dflBwyI)

### Create Simple Network
[![Watch Video](https://img.youtube.com/vi/H1jg5xTZi18/0.jpg)](https://www.youtube.com/watch?v=H1jg5xTZi18)

### Create Simple Network II
[![Watch Video](https://img.youtube.com/vi/x0GAEUgkoMw/0.jpg)](https://www.youtube.com/watch?v=x0GAEUgkoMw)

### Observing Data Flow LAN
[![Watch Video](https://img.youtube.com/vi/6FpZkpYgauo/0.jpg)](https://www.youtube.com/watch?v=6FpZkpYgauo)

### Networking Skills Challenge
[![Watch Video](https://img.youtube.com/vi/IAlt9rksxyc/0.jpg)](https://www.youtube.com/watch?v=IAlt9rksxyc)

### Hardening Linux System
[![Watch Video](https://img.youtube.com/vi/hzUt6KSfvA0/0.jpg)](https://www.youtube.com/watch?v=hzUt6KSfvA0)

### Configuring DHCP on Wireless Router
[![Watch Video](https://img.youtube.com/vi/iQmN0QTQ8mo/0.jpg)](https://www.youtube.com/watch?v=iQmN0QTQ8mo)

### Router Switch Redundancy Lab
[![Watch Video](https://img.youtube.com/vi/wNJt91MIISU/0.jpg)](https://www.youtube.com/watch?v=wNJt91MIISU)

### Router Switch Resiliency Lab
[![Watch Video](https://img.youtube.com/vi/_x0A7zTqgjc/0.jpg)](https://www.youtube.com/watch?v=_x0A7zTqgjc)

### Observing Web Request Lab
[![Watch Video](https://img.youtube.com/vi/RQYWxVCVkrg/0.jpg)](https://www.youtube.com/watch?v=RQYWxVCVkrg)

### Using Ipconfig Command Lab
[![Watch Video](https://img.youtube.com/vi/_Yqa3oteKJA/0.jpg)](https://www.youtube.com/watch?v=_Yqa3oteKJA)

### WEP WPA2 PSK WPA2 RADIUS Lab
[![Watch Video](https://img.youtube.com/vi/kieis8NLx5M/0.jpg)](https://www.youtube.com/watch?v=kieis8NLx5M)

### Configuring VPN Transport Mode
[![Watch Video](https://img.youtube.com/vi/2NSNxCUx4jg/0.jpg)](https://www.youtube.com/watch?v=2NSNxCUx4jg)

### Using John Ripper Password Lab
[![Watch Video](https://img.youtube.com/vi/ejJclx-qMXI/0.jpg)](https://www.youtube.com/watch?v=ejJclx-qMXI)

## Cybersecurity Cysa+ Labs

These labs demonstrate practical skills in cybersecurity, focusing on threat detection, system hardening, and vulnerability management. Each project emphasizes real-world applications of cybersecurity principles, from threat hunting to asset discovery, providing hands-on experience in securing and monitoring systems against evolving threats.

### Threat Hunting Lab
[![Watch Video](https://img.youtube.com/vi/ZQyzyI9br7Y/0.jpg)](https://www.youtube.com/watch?v=ZQyzyI9br7Y)

### Detecting Threats
[![Watch Video](https://img.youtube.com/vi/RUIQRG2rGKg/0.jpg)](https://www.youtube.com/watch?v=RUIQRG2rGKg)

### System Hardening Lab
[![Watch Video](https://img.youtube.com/vi/YVf9izcrY-E/0.jpg)](https://www.youtube.com/watch?v=YVf9izcrY-E)

### Asset Discovery Lab
[![Watch Video](https://img.youtube.com/vi/9R9d8obkwpM/0.jpg)](https://www.youtube.com/watch?v=9R9d8obkwpM)

### Vulnerability Scanning Lab
[![Watch Video](https://img.youtube.com/vi/QOqhN9nnaPI/0.jpg)](https://www.youtube.com/watch?v=QOqhN9nnaPI)

## Splunk Certified Core User Labs 1-5

These labs focus on mastering Splunk's core features, including data ingestion, searching, reporting, and visualizations. Through these exercises, I gained hands-on experience in efficiently utilizing Splunk to monitor, analyze, and respond to system events—critical skills for any cybersecurity professional working with SIEM solutions.

### Lab 1
[![Watch Video](https://img.youtube.com/vi/VdoEWeNhZe4/0.jpg)](https://www.youtube.com/watch?v=VdoEWeNhZe4)

### Lab 2
[![Watch Video](https://img.youtube.com/vi/bari74DNWuM/0.jpg)](https://www.youtube.com/watch?v=bari74DNWuM)

### Lab 3
[![Watch Video](https://img.youtube.com/vi/QnNuyItH6o8/0.jpg)](https://www.youtube.com/watch?v=QnNuyItH6o8)

### Lab 4
[![Watch Video](https://img.youtube.com/vi/waYtE13zYXw/0.jpg)](https://www.youtube.com/watch?v=waYtE13zYXw)

### Lab 5
[![Watch Video](https://img.youtube.com/vi/NPLhtgsQzjA/0.jpg)](https://www.youtube.com/watch?v=NPLhtgsQzjA)

## Contact
Feel free to connect with me on LinkedIn.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/smithmichael11/)


Thank you for visiting my portfolio!
