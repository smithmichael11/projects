# Projects #

I have created a series of documents and videos to showcase my key technical projects. Dive in and explore the details, highlights, valuable skills developed. I delve into various projects, extracting valuable lessons and insights from each endeavor.

## Key Projects:

### HomeShield CLI

HomeShield CLI is a local-first, defensive home-network security assessment and SOC-style dashboard project built in Python. It helps authorized users inventory devices, safely review network services, track security findings, document evidence, manage remediation decisions, and generate professional reports without exposing private network data.

HomeShield started as a safe home-network scanner and evolved into a local security operations cockpit with device identity management, SOC case workflow, safe scan profiles, metadata-only traffic summaries, remediation tracking, ATT&CK-style defensive mapping, automation, privacy controls, and portfolio-safe demo/scrub output.

<img width="1904" height="938" alt="image" src="https://github.com/user-attachments/assets/4ba74997-bc60-48cf-9851-f32ec4a6a49e" />


Project Purpose

Home networks often contain a mix of routers, phones, laptops, smart TVs, cameras, printers, IoT devices, guest devices, and stale network artifacts. A basic scan can create noise, duplicate findings, or alarming results without context.

HomeShield is designed to answer practical defensive questions:

* What devices are currently on my network?
* Which devices are known, unknown, guest, stale, or non-device artifacts?
* Which services are open, expected, or need review?
* What evidence supports each finding?
* What needs action, what has been accepted, and what has been resolved?
* Are reports and dashboards synchronized with the latest device and SOC decisions?
* Can I generate safe reports without leaking private network data?

Key Features

Local Home SOC Dashboard

HomeShield includes a local dashboard for reviewing device identity, scan results, SOC cases, remediation actions, traffic summaries, evidence, and reports.

The dashboard is built around two source-of-truth workspaces:

* Devices — authoritative source for asset identity, known IPs, known MACs, trust state, device type, owner, zone, notes, and device history.
* SOC / Issues — authoritative source for case status, analyst decisions, accepted risks, false positives, stale artifacts, remediation state, and investigation notes.

Other views such as Overview, Remediation, Threat Review, ATT&CK Map, Evidence, Traffic, and Reports inherit from these source-of-truth records.

Safe Scanner

HomeShield includes source-of-truth-aware safe scanning with:

* Authorized scope validation
* Safe scan profiles
* Scan target selection
* Excluded target reasoning
* Artifact filtering
* Scan run history
* Evidence generation
* Service review without exploitation
* Duplicate finding prevention
* Preservation of accepted/resolved/stale decisions

The scanner is designed to reduce false positives by distinguishing real active devices from stale ARP entries, broadcast addresses, guest devices, upstream observations, public DNS artifacts, and non-device records.

<img width="1897" height="812" alt="image" src="https://github.com/user-attachments/assets/33aef661-e6d2-4558-bfd4-64406198549c" />

Device Identity Management

HomeShield supports a device registry that tracks:

* Friendly device names
* Current IP and MAC
* Known IP history
* Known MAC history
* Private/randomized MAC handling
* Device type and owner
* Network zone
* Trust state
* Identity confidence
* Stale/non-device classifications
* Related SOC cases and evidence

This helps prevent the same physical device from appearing as multiple unknown devices when IPs or randomized MAC addresses change.

SOC Case Workflow

HomeShield includes a local SOC-style workflow for:

* Open findings
* Needs-review items
* Accepted / monitored risks
* Resolved cases
* False positives
* Stale / non-device artifacts
* Decision reasons
* Analyst notes
* Evidence linking
* Remediation tracking

A case decision made in SOC is reflected across the dashboard, reports, remediation views, threat review, and ATT&CK mapping.

Evidence and Reporting

HomeShield generates structured evidence and reports, including:

* One-page home brief
* Home network summary
* Technical findings
* Remediation playbook
* SOC correlation report
* Device timeline
* Source-of-truth sync report
* Traffic metadata summary
* ATT&CK-style defensive mapping
* Evidence index

Reports are designed to separate active action items from accepted risks, resolved items, false positives, and stale artifacts.

Metadata-Only Traffic Summary

HomeShield includes privacy-conscious traffic summary functionality. By default, traffic review is metadata-only and does not capture payloads, credentials, camera streams, or message contents.

<img width="1916" height="930" alt="image" src="https://github.com/user-attachments/assets/9f8b1cc4-cc26-4965-992e-b18ef01b58b1" />

Traffic summaries may include:

* Top talkers
* New destinations
* Guest activity
* Unknown device activity
* Unusual ports
* Traffic anomalies
* Device-to-traffic correlation

Safe Automation

HomeShield supports safe automation modes, including:

* daily-light
* weekly-safe
* monthly-report
* portfolio-demo
* quick-dashboard
* qa-only

Automation can run safe checks, refresh dashboard data, generate reports, produce summaries, export schedules, and draft weekly emails. It does not automatically trust devices, close cases, modify router settings, capture payloads, or perform offensive testing.

Weekly Email Reporting

HomeShield supports optional weekly email reporting with strict safety controls:

* Draft-only by default
* Explicit send-enabled mode required
* SMTP credentials loaded from environment variables only
* Gmail SMTP support
* No SMTP password stored in project config
* No raw evidence, logs, traffic data, router snapshots, or registries attached by default
* Safe attachment policy
* Dashboard email status
* Git privacy checks

Portfolio / Demo Scrub Mode

HomeShield includes scrub/demo export functionality for safe portfolio sharing. Scrubbed output removes or replaces sensitive details such as:

* Real MAC addresses
* Real device names
* Personal notes
* Router snapshots
* Raw traffic data
* Raw telemetry
* Private project artifacts

This allows the project architecture and workflow to be demonstrated without exposing private home-network details.

Safety Model

HomeShield is intentionally defensive and local-only.

It does not perform:

* Exploitation
* Brute force attacks
* Credential guessing
* Credential capture
* Wi-Fi cracking
* Packet injection
* ARP poisoning
* MAC spoofing
* IP spoofing
* Malware or RAT behavior
* Public IP scanning by default
* Router/device configuration changes
* Automatic blocking or trust decisions
* Payload capture by default

HomeShield is designed for authorized networks owned or managed by the user.

Technical Highlights

* Python CLI tooling
* Local dashboard workflow
* Safe Nmap-based service checks
* Router/DHCP/ARP evidence correlation
* Device registry and identity resolver
* SOC case registry and status resolver
* Evidence-to-case linking
* Metadata-only traffic summaries
* Report generation
* Automation workflows
* Gmail SMTP weekly reporting
* Portfolio-safe scrub/export mode
* Pytest regression suite

Testing

HomeShield has been developed through incremental releases with regression testing. Recent milestones include:

* Dashboard source-of-truth refactor
* Commercial dashboard and traffic summary polish
* Scanner source-of-truth integration
* Live dashboard QA
* Safe automation
* Gmail SMTP send verification
* Weekly report PDF attachment work in progress

The project currently includes hundreds of pytest tests covering scanner safety, device identity handling, SOC case status sync, dashboard views, traffic privacy, scrub/demo safety, automation, and email-reporting safeguards.

Example Use Cases

* Home network inventory and review
* Router and IoT hardening assessment
* Unknown-device investigation
* SOC-style alert triage practice
* Evidence documentation
* Remediation planning
* Privacy-conscious traffic summary review
* Cybersecurity portfolio demonstration
* Technical product / security automation showcase

Portfolio Value

This project demonstrates:

* Cybersecurity operations thinking
* Python automation
* Network troubleshooting
* Safe scanning methodology
* SOC workflow design
* Evidence handling
* Case management
* Dashboard/product design
* Data modeling
* Privacy-by-design
* Report generation
* QA and regression testing
* Technical documentation

### Network Security Assessment & SIEM Integration Lab| Dec. 2025 |Enterprise-Grade Security Monitoring Homelab | Focus: Network Reconnaissance, Traffic Analysis, Intrusion Detection, and Centralized Log Management

Built a fully functional security operations center (SOC) environment to identify, analyze, and mitigate network vulnerabilities across a multi-subnet home network. This project showcases practical skills in network reconnaissance, traffic analysis, intrusion detection, and centralized log management.

🛠️ Technologies & Tools

Security & Monitoring:
* Splunk Enterprise — SIEM platform for log aggregation and correlation
* Suricata IDS — Real-time intrusion detection and prevention
* Nmap — Network discovery and vulnerability assessment
* tcpdump — Packet capture and network traffic analysis
  
Environment:
* Network: Multi-subnet LAN (192.168.8.0/24, 10.0.0.0/24)
* Host OS: macOS 10.15
* Hardware: GL.iNet Router, Multiple IoT devices
* Protocols: HTTP/HTTPS, DNS, SSH, Telnet, RTSP, mDNS

🎪 Key Achievements

✅ Discovered 9 live hosts across two network subnets using Nmap reconnaissance 

✅ Analyzed 5,000+ network flow records in Splunk with custom correlation queries 

✅ Identified 28 medium-risk HTTP connections requiring security hardening 

✅ Deployed Suricata IDS capturing 2,475 packets with automated alert generation 

✅ Implemented HTTPS encryption on router management interface, reducing attack surface 

✅ Mapped threats to MITRE ATT&CK framework (T1078, T1071, T1041, T1021) 

✅ Created automated alerting for high-risk services (Telnet, unencrypted HTTP, RTSP)


📊 Project Highlights

Network Discovery & Enumeration
* Performed comprehensive host discovery across home network
* Enumerated services on all active hosts with version detection
* Identified critical vulnerabilities: unencrypted HTTP, exposed Telnet, RTSP streams

SIEM Integration & Analysis
* Configured Splunk Enterprise with custom data inputs (XML, PCAP, JSON)
* Developed SPL queries to correlate network flows with security events
* Built dashboards for real-time monitoring and historical trend analysis
* Processed multi-source telemetry from Nmap, tcpdump, and Suricata

Traffic Analysis & Threat Detection
* Captured live network traffic using tcpdump with targeted BPF filters
* Analyzed DNS patterns (1,734 queries to Cloudflare DNS)
* Identified encrypted vs unencrypted traffic ratios
* Detected anomalous connection patterns and high-volume communications

Security Hardening & Remediation
* Disabled insecure services (Telnet port 23)
* Implemented HTTPS with self-signed certificates on router GUI
* Configured automated monitoring for remaining high-risk services
* Validated remediation effectiveness through post-implementation scanning


[Splunk Lab Security Assessment.pdf](https://github.com/user-attachments/files/24341908/Splunk.Lab.Security.Assessment.pdf)

  
### Home Network Penetration Testing Reporting & Legal Authorization Project | Dec. 2025 | Technology Law & Cybersecurity Engagement | Focus: Computer Fraud and Abuse Act (CFAA), Cybersecurity Legal Frameworks

•	Drafted comprehensive pre-engagement legal authorization suite including Authorization to Test, Rules of Engagement, Statement of Work, and Confidentiality Agreement; analyzed CFAA (18 U.S.C. § 1030) risk exposure and structured explicit written consent to distinguish authorized testing from unlawful access.

•	Defined scope boundaries, prohibited activities, and escalation procedures to mitigate civil and criminal liability; integrated legal governance controls with NIST/PTES technical methodology.

•	Performed internal penetration test on home network, migrating devices from ISP modem to hardened GL.iNet router with segregated LAN and Guest SSIDs.

•	Performed comprehensive network security assessments, vulnerability analysis, and embedded device hardening using industry-standard tools and methodologies. Practical expertise in network architecture design, including migrating home networks from ISP modem configurations to hardened router deployments with segregated wireless networks.

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
