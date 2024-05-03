# Helpful commands!

Restart Windows PC to BIOS
```
shutdown /r /fw /t 1
```
`/r` - restarts; `/fw` - boot to firmware (BIOS); `/t` - delay in seconds before restart

---

Disable Bing search via Start menu in Windows, which increases search speed (paste into Powershell)
```powershell
Set-ItemProperty -Path "HKCU:\SOFTWARE\Microsoft\Windows\CurrentVersion\Search" -Name "BingSearchEnabled" -Value 0 -Type DWord
```
