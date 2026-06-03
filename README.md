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
## Findings

### Open Ports

| Port | Service |
|--------|---------|
| 135 | MSRPC |
| 445 | Microsoft-DS (SMB) |

### Service Enumeration

- Microsoft Windows RPC detected on port 135
- SMB file sharing service detected on port 445
- Host identified as Windows system
## Security Relevance

- Port 135 is used for Windows administrative services.
- Port 445 provides SMB file sharing capabilities.
- Open services represent potential attack surfaces that security analysts must monitor and secure.
## Screenshots

### Nmap Installation Verification
![Nmap Version](screenshots/nmap-version.png)

### Localhost Port Scan
![Localhost Scan](screenshots/localhost-scan.png)

### Service Enumeration
![Service Scan](screenshots/service-scan.png)
