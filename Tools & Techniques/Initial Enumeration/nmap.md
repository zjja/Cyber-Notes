# Nmap commands

```bash
# Do nmap default scripts, get version and save output to nmap folder
nmap -sC -sV -oA nmap/nmap-scripts <ip>

# Run all safe scripts on a port, disable ping and name resolution
nmap -p <port> --script safe -Pn -n <ip>

# Run all safe and vuln scripts on a part, disable ping and name resolution
nmap -p <port> --script "vuln and safe" -Pn -n <ip>
```

