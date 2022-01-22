# Windows Enumeration

## System Information

```bash
systeminfo
systeminfo | findstr /B /C: "OS Name" /C: "OS Version"
```

## Security updates

```bash
wmic qfe get Caption,Description,HotFixID,InstalledOn
```

## Service list

```bash
wmic service list
sc queryex type= service
```

## Query Service

```bash
sc query <service>
```

## List drives

```bash
wmic logicaldisk get caption,description,providername
```

## Environment Variables

```bash
set
```

## User info

```bash
# Get current user privs
whoami /priv

# Get current user groups
whoami /groups

# list users on system
net user

# list information about <username>
net user <username>

# list information about the Administrator user
net user Administrator

net localgroup

net localgroup Administrators
```

## Network information

```bash
ipconfig
arp -a
route print
netstat -ano
```

## Find Passwords

```bash
findstr /si password *.txt *.ini *.config
```

