## File transfer via netcat

Netcat - listen for incoming file

```bash
nc -nlvp 4444 > incoming.exe
```

Netcat - send file

```bash 
nc -nv <ip address> 4444 < outgoing.exe
```

