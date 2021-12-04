# Powershell commands
List installed software 

`Get-WmiObject -Class Win32_Product`

Find file

`Get-Childitem -Path c:\ -Include <filename> -File -Recurse -ErrorAction SilentlyContinue`