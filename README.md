# Purple Homelab  
### A Fully Documented Purple Team Cybersecurity Lab (Blue + Red Focus)

---

## 🎯 Overview  
This repository documents the complete build, configuration, and ongoing development of my personal cybersecurity homelab.  
The goal of this lab is to gain hands-on, real-world experience across **Purple Team**, **SOC**, **DFIR**, **Windows Security**, **Linux Security**, **Active Directory**, **SIEM**, **EDR**, **Threat Emulation**, and **Offensive Security** techniques.

Everything here is built from scratch using:
- Windows Server 2019 (Domain Controller)
- Windows 10 Enterprise endpoints
- Kali Linux attacker machine
- VirtualBox
- Custom network segmentation
- Active Directory security hardening
- Logging + SIEM integration (Splunk)
- Threat simulation tools

This repository grows as I grow. Every configuration, success, mistake, fix, and lesson is documented here.

---

## 🧠 Purpose of the Lab  
This lab enables me to:
- Learn and practice **Active Directory administration**
- Build realistic **enterprise-class environments**
- Perform **Blue Team detection engineering**
- Develop **Red Team tradecraft** in a safe environment
- Understand how attackers move and how defenders detect them
- Create a portfolio that proves hands-on technical skill  
- Build toward SOC Analyst → Blue Team → Purple Team Engineer

---

## 🟪 Purple Team Goals  
This lab focuses on BOTH sides:
- **Blue Team** → Logging, alerting, detection, defense  
- **Red Team** → Exploitation, lateral movement, persistence  
- **Purple Team** → Running attacks, observing logs, writing detections

Practical outcomes:
- Understanding how the entire kill-chain works  
- Ability to emulate attackers using tools like:
  - Kali Linux
  - Metasploit
  - Covenant
  - Evil-WinRM
  - BloodHound/SharpHound
- Ability to detect attacks using:
  - Splunk
  - Sysmon
  - Windows Event Logs
  - Winlogbeat/Elastic (later)
  - Sigma rules

---

## 🏗 Lab Components  
### **Virtual Machines**
- **DC-1**  
  - Windows Server 2019  
  - Active Directory Domain Services  
  - DNS  
  - Group Policy  
  - Security Hardening  

- **WIN10-1**  
  - Windows 10 Enterprise  
  - Domain-joined endpoint  
  - Sysmon enabled  
  - Splunk Universal Forwarder installed  

- **Kali-1**  
  - Kali Linux Rolling  
  - Attacker host  
  - Enumeration + exploitation tools  

---

## 🔧 Core Security Tools  
This lab will eventually include:
- Splunk (SIEM)
- Wazuh (later)
- Sysmon
- Sysmon Modular Config
- Sysinternals Live Tools
- Atomic Red Team
- ATT&CK Navigator
- BloodHound
- Kerbrute
- Impacket tools
- Hashcat
- Wireshark
- PCAP analysis tools

---

## 📚 Documentation Style  
Every task is documented in a **consistent, professional format**:

### ✔ Task Format:  
- Purpose  
- Steps taken  
- Screenshots (when applicable)  
- Issues encountered  
- Fixes applied  
- Lessons learned  
- Commands used  

### ✔ Commit Style  
Each commit message will follow:

[DC-1] Added new OU structure + admin account work
[WIN10-1] Installed Sysmon + base configuration
[KALI-1] Ran initial enumeration tests against DC
[LAB] Updated README + folder structure

yaml
Copy code

---

## 📁 Repository Structure

purple-homelab/
│
├── README.md
├── /documentation/
│ ├── dc-1/
│ ├── win10-1/
│ ├── kali-1/
│ ├── troubleshooting/
│ └── lessons-learned/
│
├── /configs/
│ ├── sysmon/
│ ├── splunk/
│ └── gpo/
│
├── /screenshots/
│ ├── dc-1/
│ ├── win10-1/
│ └── kali-1/
│
└── /attacks/
├── credential-access/
├── lateral-movement/
├── privilege-escalation/
└── persistence/

yaml
Copy code

---

## 🧪 Offensive + Defensive Scenarios  
This lab will include full write-ups for:

### **Red Team Techniques**
- Password spraying  
- Kerberoasting  
- AS-REP roasting  
- Lateral movement via WinRM / RDP  
- Service account enumeration  
- Token impersonation  
- Credential dumping  
- Attack path mapping (BloodHound)

### **Blue Team Techniques**
- Building detection rules  
- Reviewing logs in Splunk  
- Mapping alerts to MITRE ATT&CK  
- Investigating malicious authentication attempts  
- Creating dashboards  
- SIEM alerting logic  
- Windows Event Log deep dives  

### **Purple Team Exercises**
- Run the attack  
- Capture logs  
- Analyze logs  
- Build a detection rule  
- Validate the detection rule by rerunning attack  

---

## 🧩 What This Lab Proves About Me  
This repository demonstrates:
- Hands-on experience beyond certifications  
- Ability to build production-like environments  
- Experience with real tooling (SIEM, GPO, AD, Sysmon, Kali)  
- Understanding of attacker methodology  
- Ability to write detections  
- Documentation and engineering discipline  
- Independent problem-solving  

---

## 🚀 Roadmap  
### **Phase 1 – Core Build**
- Build VMs  
- Configure network  
- Install AD DS  
- Join domain  
- Install Sysmon  
- Install Splunk Universal Forwarder  

### **Phase 2 – Logging + Monitoring**
- Forward logs into Splunk  
- Configure Sysmon modular  
- Build dashboards  

### **Phase 3 – Attack Simulation**
- Run privilege escalation attacks  
- Run credential attacks  
- Run lateral movement  

### **Phase 4 – Detection Engineering**
- Build SIEM rules  
- Map detections to ATT&CK  
- Document findings  

---

## 🧵 Lessons Learned Section  
Every challenge, error, or fix goes into `/documentation/lessons-learned/`.

This is an important part of the portfolio — it shows:
- Troubleshooting skill  
- Understanding of system behavior  
- Growth over time  

---

## 🤝 Contributions  
This is a personal learning environment, but feedback is welcome.

---

## 📬 Contact  
**Warren Bowen Jr. (wb-security)**  
GitHub: https://github.com/wb-security  

---

## 🌟 Final Note  
This homelab represents my growth as a cybersecurity professional.  
It will expand continuously as I learn new tools, new techniques, and new ways to think like both an attacker and a defender.

Feedback, suggestions, and ideas for new lab scenarios are always welcome.
