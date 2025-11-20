# WIN10-1 — Windows 10 Enterprise Workstation
**Role:** Domain-joined workstation  
**Hostname:** WIN10-1  
**OS:** Windows 10 Enterprise

---

## 1. Purpose
This workstation acts as the primary domain-joined endpoint for:
- Endpoint logging & monitoring  
- Sysmon configuration  
- Lateral movement testing  
- Malware/attack simulation  

---

## 2. Installation & Configuration

### 2.1 Base OS Setup
- Installed Windows 10 Enterprise  
- Applied all updates  
- Assigned static networking (if needed)  
- Renamed system to **WIN10-1**

### 2.2 Domain Join
Steps completed:
1. Set DNS to DC-1 IP  
2. Joined domain **purple.local**  
3. Restarted and verified domain membership  
4. Logged in using `purple\wbowen`

---

## 3. Software Installed (Planned)
- Sysmon  
- Event collection agents  
- PowerShell logging GPO  
- Attack tools for testing (as needed)  
- Windows Security Baseline

---

## 4. Logging Configuration (Planned)
This workstation will feed logs to:
- Sysmon logging directory  
- Event Viewer (Security, System, Application)  
- Future SIEM (Splunk or Elasticsearch)

---

## 5. Tasks Completed
- [x] Installed OS  
- [x] Domain-joined the machine  
- [ ] Install Sysmon  
- [ ] Apply endpoint hardening  
- [ ] Configure log forwarding  

---

## 6. Notes / Issues
Document any problems encountered during domain join or networking setup.


