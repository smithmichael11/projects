# Projects #

I have created a series of documents and videos to showcase my key cybersecurity projects. Dive in and explore the details, highlights, valuable skills developed. I delve into various cybersecurity projects, extracting valuable lessons and insights from each endeavor.

## Key Projects:

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
