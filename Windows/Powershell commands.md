# Powershell commands
## List installed software

```power
Get-WmiObject -Class Win32_Product

```

## Find file

```powershell
Get-Childitem -Path c:\ -Include <filename> -File -Recurse -ErrorAction SilentlyContinue
```

## File transfer

```powershell
wget http://<url>/<file> -outfile <file>
```

