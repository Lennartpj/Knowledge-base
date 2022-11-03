


## PowerShell
### Install Windows Update
```powershell
Install-Module -Name PSWindowsUpdate
```
---
### List all Commands
```powershell
Get-Command -module PSWindowsUpdate
```
---
### Execute Update
```powershell
Get-WindowsUpdate -Install -Download -AcceptAll -Autoreboot
```

