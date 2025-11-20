# DC-1 Validation & Verification

## 1. Domain Controller Promotion Successful
- Server rebooted automatically after promotion  
- Login screen displayed domain option  

**Logged in as:**  
`purple\wbowen`

## 2. Verified AD DS + DNS Services Running
Tools confirmed working:
- Active Directory Users and Computers  
- DNS Manager  
- Group Policy Management  

## 3. Validated Network Configuration
`ipconfig /all` output confirmed:
- Hostname: **DC-1**
- Primary DNS Suffix: **purple.local**
- IPv4: **192.168.50.10**
- DNS Server: **127.0.0.1**
- DHCP: Disabled (static config)

## 4. OUs Verified
Successfully verified:
- `_Admins`
- `_Servers`
- `_Workstations`

## 5. User Account Verification
User **wbowen**:
- Exists in `_Admins` OU  
- Member of Domain Admins, Enterprise Admins, Schema Admins, Administrators  
- Can log into domain controller

## 6. System Operates Normally
- No replication errors  
- DNS queries succeed internally  
- ADUC functions as expected  

DC-1 is fully operational and stable.
