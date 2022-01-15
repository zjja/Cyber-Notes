# Windows Security (bypassing)

## Allow Remote desktop

```bash
netsh advfirewall firewall set rule group="remote desktop" new enable=Yes
```

## Allow Port in

```bash
netsh advfirewall firewall add rule name="inbound 4444" dir=in action=allow protocol=TCP localport=4444
```

