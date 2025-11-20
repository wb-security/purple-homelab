# DC-1 Real Build Log (Unedited, Actual Process)

This log records the TRUE sequence of events during the DC-1 setup, including errors, confusion, and fixes.

---

## 🕒 2025-11-18 — Build Session

### 1. VM Creation
- Created VM named **DC-1** in VirtualBox  
- Selected Windows Server 2019 (64-bit)  
- Assigned 4096 MB RAM, 60 GB HDD  

### 2. Installed Windows Server  
- Booted from ISO  
- Installed Standard Desktop Experience  
- Logged in as local Administrator  

### 3. Menu Bar Missing  
- VirtualBox UI disappeared  
- Fixed by re-enabling it through VirtualBox preferences

### 4. Hostname + Network
- Renamed PC → **DC-1**  
- Restarted  
- Set static IP: 192.168.50.10  
- Set DNS to 127.0.0.1  

### 5. AD DS + DNS Installation
- Added roles through Server Manager  
- Chose “Add a new forest” → **purple.local**  
- Entered DSRM password  
- Server restarted  

### 6. Created OUs
Attempted to create:
- `_Admins`  
- `_Servers`  
- `_Workstations`

Got OU error:  
“A file exists where you’re trying to create a subdirectory.”  
→ Realized the OU already existed.

### 7. Created Admin User
- Created user: **Warren Bowen** / `wbowen`  
- Password initially rejected due to complexity  
- Set password: **Warren1994!**

### 8. Could Not Find User  
- User did not appear under `_Admins`  
- Used ADUC search → found user under **Users**  
- Used “Locate” → moved user to `_Admins`

### 9. Added Group Memberships
Assigned:
- Domain Admins  
- Enterprise Admins  
- Schema Admins  
- Administrators  

### 10. Final Validation
- Logged out and back in as `purple\wbowen`  
- Verified DNS suffix  
- Verified AD roles and OUs  
- DC-1 operational and stable  

---

## ✔ DC-1 Build Completed Successfully
