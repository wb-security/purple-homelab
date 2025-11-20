# DC-1 Troubleshooting Log

This file documents the REAL issues encountered during the build of DC-1 and how each problem was resolved.

---

## ❌ Issue: Password Did Not Meet Complexity Requirements
**What happened:**  
While creating the “Warren Bowen” domain user, multiple password attempts failed.

**Reason:**  
Windows enforces:
- Minimum 8 characters  
- Uppercase + lowercase  
- Number  
- Special character  

**Fix:**  
Created a compliant password:  
`Warren1994!`

---

## ❌ Issue: Could Not Create "_Admins" OU
**What happened:**  
Attempted to create an OU named `_Admins` but got the error:  
“A file exists where you’re trying to create a subdirectory.”

**Reason:**  
The OU already existed (possibly created earlier).

**Fix:**  
Refreshed ADUC, confirmed OU existed, and proceeded without creating a duplicate.

---

## ❌ Issue: Could Not Find User in ADUC
**What happened:**  
The newly created user did not appear under expected OUs.

**Reason:**  
User was created under the default **Users** container, not `_Admins`.

**Fix:**  
Used ADUC’s **Find** feature, located the user, opened Properties → Object → “Locate”  
→ Correctly moved user into `_Admins`.

---

## ❌ Issue: VirtualBox Menu Bar Disappeared
**What happened:**  
Menu bar vanished, making it impossible to adjust VM settings.

**Reason:**  
VirtualBox hides menus if certain UI modes are toggled.

**Fix:**  
Returned to host window → clicked:  
**File → Preferences → Input → Virtual Machine → Restore Default UI**  
Menu bar returned.

---

These issues were resolved successfully, and DC-1 now operates normally.
