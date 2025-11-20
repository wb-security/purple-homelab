# KALI-1 — Offensive Security Workstation
**Role:** Attack machine / pentest workstation  
**Hostname:** KALI-1  
**OS:** Kali Linux (Latest ISO)

---

## 1. Purpose
KALI-1 acts as the primary offensive security system in the homelab, used for:
- Reconnaissance  
- Vulnerability scanning  
- Exploitation  
- Credential harvesting  
- Lateral movement  
- Purple team testing  

---

## 2. Installation & Setup

### 2.1 Base Installation
- Installed Kali Linux from ISO  
- Enabled root login or sudo user  
- Updated system packages:  
sudo apt update && sudo apt upgrade -y
### 2.2 Networking
- Set adapter to **Host-Only** (VirtualBox)  
- Confirmed communication with domain:  
ping 192.168.56.10 (DC-1)
ping win10-1
---

## 3. Tools Installed (Planned)
- Nmap  
- BloodHound + Sharphound  
- Evil-WinRM  
- Impacket suite  
- Responder  
- CrackMapExec  
- Kerbrute  
- Wireshark  

---

## 4. Attack Scenarios (Planned)
This section documents offensive tests:
- LLMNR/NBT-NS poisoning  
- Kerberoasting  
- AS-REP Roasting  
- SMB relay  
- Pass-the-Hash  
- Pass-the-Ticket  
- DCSync  
- Privilege escalation  

---

## 5. Tasks Completed
- [x] Installed Kali  
- [ ] Install BloodHound  
- [ ] Add offensive tools  
- [ ] Build attack playbooks  

---

## 6. Notes / Issues
Document any networking, tool installation, or permission issues here.


