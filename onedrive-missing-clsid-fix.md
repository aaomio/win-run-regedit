# OneDrive Missing from File Explorer

## Issue

- OneDrive not visible in File Explorer navigation pane  

---

## Cause

- OneDrive shell integration disabled  

**CLSID:**

{018D5C66-4533-4307-9B53-224DE2ED1FE6}  

---

## Fix (Registry)

- Navigate to:

HKEY_CURRENT_USER\Software\Classes\CLSID\{018D5C66-4533-4307-9B53-224DE2ED1FE6}  

**Value Name:** System.IsPinnedToNameSpaceTree  
**Type:** REG_DWORD  
**Value:** 1  

---

## Optional Fix

```cmd
taskkill /f /im explorer.exe
start explorer.exe