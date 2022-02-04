# Powershell commands
## List installed software

```power
Get-WmiObject -Class Win32_Product
```

## Find file

```powershell
Get-Childitem -Path c:\ -Include <filename> -File -Recurse -ErrorAction SilentlyContinue
```

## Find string in multiple files

```powershell
Get-ChildItem -Recurse | Select-String "<string>"
```

## File transfer / download

```powershell
wget http://<url>/<file> -outfile <file>
```

