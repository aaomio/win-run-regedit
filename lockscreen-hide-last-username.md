# Lock Screen Shows Last Logged-in User

## Issue

- Windows lock screen displays the last logged-in username  
- This can expose valid usernames on shared devices  

---

## Cause

- Windows is configured to show last signed-in user by default  

**Registry path:**

HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System  

**Value:**
dontdisplaylastusername  

---

## Fix (Registry)

- Navigate to registry path above  
- Create or modify:

**Value Name:** dontdisplaylastusername  
**Type:** REG_DWORD  
**Value:** 1  

---

## Fix (PowerShell)

```powershell
Set-ItemProperty -Path "HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System" -Name "dontdisplaylastusername" -Value 1