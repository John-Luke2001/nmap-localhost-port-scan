# Nmap Localhost Port Scan

## Objective

Use Nmap to identify open ports and running services on a local Windows host.

## Tools

- Nmap 7.99
- Windows 11

## Commands Used

```bash
nmap localhost
nmap -sV localhost
```

## Findings

### Open Ports

| Port | Service |
|------|---------|
| 135 | MSRPC |
| 445 | Microsoft-DS (SMB) |

### Service Enumeration

- Microsoft Windows RPC detected on port 135
- SMB file sharing service detected on port 445
- Host identified as Windows system

## Security Relevance

- Port 135 is used for Windows administrative services.
- Port 445 provides SMB file sharing capabilities and is commonly targeted during lateral movement and ransomware attacks.
- Open services increase an organization's attack surface and should be monitored, hardened, and regularly assessed.
## Screenshots

### Nmap Installation Verification

![Nmap Version](screenshot/nmap-version.png)

### Localhost Port Scan

![Localhost Scan](screenshot/localhost-scan.png)

### Service Enumeration

![Service Scan](screenshot/service-scan.png)
