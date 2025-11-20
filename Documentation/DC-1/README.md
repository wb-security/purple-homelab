# DC-1 — Windows Server 2019 Domain Controller
**Role:** Primary Domain Controller  
**Hostname:** DC-1  
**Domain:** purple.local  
**OS:** Windows Server 2019 Standard (Evaluation)

---

## 1. Purpose
DC-1 acts as the core of the homelab environment. It provides centralized authentication, DNS, and Group Policy management. All Windows clients in the lab domain authenticate through this server.

---

## 2. Installation & Configuration

### 2.1 Base Installation
- Installed Windows Server 2019 from ISO  
- Set Administrator password  
- Assigned static networking:  
  - **IP:** 192.168.56.10  
  - **Subnet:** 255.255.255.0  
  - **Gateway:** 192.168.56.1  
  - **DNS:** 127.0.0.1 (after promotion)

### 2.2 Promote to Domain Controller
Steps performed:
1. Installed **Active Directory Domain Services (AD DS)**  
2. Promoted server to Domain Controller  
3. Created new forest: **purple.local**  
4. Configured DNS  
5. Restarted and verified domain functional level

---

## 3. Domain Objects Created

### 3.1 Organizational Units (Planned)
purple.local
└── _ADMINS
└── _COMPUTERS
└── _USERS
└── _GROUPS
### 3.2 Domain Accounts
- `wbowen` — admin user  
- Future accounts will be created for endpoint simulation.

---

## 4. Security Configuration (Planned)
This section will grow as the lab develops:

- Group Policy Objects (GPOs)  
- Password policies  
- Logging via Sysmon  
- Windows Event Forwarding  
- Firewall baselines  
- Hardening checklist  

---

## 5. Tasks Completed
- [x] Installed Server 2019  
- [x] Promoted to Domain Controller  
- [x] Created first domain admin user  
- [ ] Create baseline OUs  
- [ ] Install Sysmon  
- [ ] Configure forwarding rules  

---

## 6. Notes / Issues
Document any installation challenges, fixes, or errors here.


