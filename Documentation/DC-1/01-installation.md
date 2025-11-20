# DC-1 Installation & Configuration Guide

## 1. Create the Virtual Machine
- Name: **DC-1**
- OS: Windows Server 2019 (64-bit)
- RAM: 4–8 GB
- CPU: 2+
- Disk: 60 GB

## 2. Install Windows Server 2019
- Select **Standard Evaluation (Desktop Experience)**
- Create local Administrator password
- Complete installation and first login

## 3. Set Hostname
Open PowerShell as Administrator:
```
Rename-Computer -NewName "DC-1" -Restart
```

## 4. Configure Static Network
Use the *preferred* NAT Network:
- IP: **192.168.50.10**
- Mask: 255.255.255.0
- Gateway: 192.168.50.1
- DNS: 127.0.0.1 (self)

```
New-NetIPAddress -InterfaceAlias "Ethernet" -IPAddress 192.168.50.10 -PrefixLength 24 -DefaultGateway 192.168.50.1
Set-DnsClientServerAddress -InterfaceAlias "Ethernet" -ServerAddresses 127.0.0.1
```

## 5. Install Active Directory Domain Services
Open **Server Manager → Add Roles and Features**  
Select:
- Active Directory Domain Services  
- DNS Server  

Install and continue.

## 6. Promote to Domain Controller
After installation:
- Click **Promote this server to a domain controller**
- Choose **Add a new forest**
- Root domain name: **purple.local**
- Set Directory Services Restore Mode (DSRM) password
- Complete promotion & restart

## 7. Create Organizational Units
In **Active Directory Users and Computers**:
Create top-level OUs:
- `_Admins`
- `_Servers`
- `_Workstations`

## 8. Create Administrative User
Example:
- Full Name: **Warren Bowen**
- Username: **wbowen**
- Password meeting complexity

Move user to `_Admins` OU.

## 9. Grant Admin Rights
Add user to:
- Domain Admins
- Enterprise Admins
- Schema Admins
- Administrators

## 10. Verify Domain Controller Functionality
- Log in as purple\wbowen
- Run `ipconfig /all` (check DNS suffix = purple.local)
- Open ADUC to verify OUs and users
- Confirm DNS service is running

DC-1 is now fully deployed and functional.
