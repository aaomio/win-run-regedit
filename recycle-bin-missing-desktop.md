# Recycle Bin CLSID Missing (Desktop + Explorer)

## Issue

- Recycle Bin missing from desktop and File Explorer  

---

## Cause

- Shell pinning disabled in registry  

**CLSID:**

{645FF040-5081-101B-9F08-00AA002F954E}  

---

## Fix (Registry)

- Navigate to:

HKEY_CURRENT_USER\Software\Classes\CLSID\{645FF040-5081-101B-9F08-00AA002F954E}  

**Value Name:** System.IsPinnedToNameSpaceTree  
**Type:** REG_DWORD  
**Value:** 1  

---

## Optional Fix

```cmd
taskkill /f /im explorer.exe
start explorer.exe