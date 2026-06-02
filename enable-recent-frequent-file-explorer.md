# Enable Recent and Frequent Items in File Explorer (Home)

## Issue

- Recent files and frequent folders are not showing in File Explorer Home  
- File Explorer appears empty or only shows pinned locations  

---

## Cause

- Windows Explorer history tracking is disabled via settings or registry  

**Registry path:**

HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer  

---

## Fix (Registry)

- Navigate to the registry path above  

Set or create the following values:

**Value Name:** ShowRecent  
**Type:** REG_DWORD  
**Value:** 1  

**Value Name:** ShowFrequent  
**Type:** REG_DWORD  
**Value:** 1  

---

## Alternative Fix (File Explorer Settings)

- Open File Explorer  
- Click View  
- Options  
- Privacy section  

Enable:

- Show recently used files in Quick access  
- Show frequently used folders in Quick access  

Click Apply  

---

## Optional Step (Refresh Explorer)

```cmd
taskkill /f /im explorer.exe
start explorer.exe