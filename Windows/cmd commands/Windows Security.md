# Windows Security

## Determine if windefend is running

```bash
sc query windefend
```

## List firewall rules/status

```bash
netsh advfirewall firewall dump
netsh firewall show state
netsh fireall show config
```

## Allow Remote desktop

```bash
netsh advfirewall firewall set rule group="remote desktop" new enable=Yes
```

## Allow Port in

```bash
netsh advfirewall firewall add rule name="inbound 4444" dir=in action=allow protocol=TCP localport=4444
```

