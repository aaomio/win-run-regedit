# Allow Domain PIN Logon (Windows Hello for Business)

## Issue

- PIN login not available for domain or Azure AD users  

---

## Cause

- Windows Hello PIN sign-in is disabled by policy  

**Registry path:**

HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\System  

**Value:**
AllowDomainPINLogon  

---

## Fix (Registry)

- Navigate to registry path  

**Value Name:** AllowDomainPINLogon  
**Type:** REG_DWORD  
**Value:** 1  

---

## Fix (PowerShell)

```powershell
Set-ItemProperty -Path "HKLM:\SOFTWARE\Policies\Microsoft\Windows\System" -Name "AllowDomainPINLogon" -Value 1