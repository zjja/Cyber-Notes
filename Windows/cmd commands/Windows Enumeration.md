# Windows Enumeration

## List users

```bash
net users
```

## System Information

```bash
systeminfo
systeminfo | findstr /B /C: "OS Name" /C: "OS Version"
```

## Service list

```bash
wmic service list
```

## Environment Variables

```bash
set
```

