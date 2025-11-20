# DC-1 Overview  
Domain Controller (DC-1)  
===========================================  
DC-1 is the primary Windows Server domain controller for the `purple.local` Active Directory forest.  
It provides domain authentication, DNS, organizational unit structure, and GPO management.

### **System Specs**
- **Host OS:** Windows Server 2019 / 2022 Datacenter  
- **Hostname:** DC-1  
- **IP Address:** 192.168.50.10  
- **DNS:** Points to itself  
- **Roles Installed:**
  - Active Directory Domain Services (AD DS)
  - DNS Server

### **Purpose**
DC-1 acts as the core authentication and administrative server for the homelab.  
It is the first machine created and must be fully functional before creating:
- WIN10-1 (domain-joined workstation)
- KALI-1 (attacker box)
