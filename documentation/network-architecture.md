
# Network Architecture

## 1. Overview

This document describes the network architecture of the Cybersecurity Homelab.

The project uses a local home network to connect the Lenovo server, Windows workstation, router and other authorized devices.

The main objectives are:

- Centralized server management.
- Secure remote access.
- NAS file sharing.
- Media streaming.
- Network monitoring.
- Authorized cybersecurity testing.

## 2. Network Components

| Device | Role |
|---|---|
| Lenovo G580 | Main Ubuntu Server |
| Windows 11 PC | Administration and cybersecurity workstation |
| Home Router | Network gateway and internet connectivity |
| Other Devices | Authorized clients accessing server services |

## 3. Network Configuration

The following table describes the network configuration using example private IP addresses.

| Device | IP Address |
|---|---|
| Home Router | `<ROUTER_IP>` |
| Windows Workstation | `<WINDOWS_PC_IP>` |
| Lenovo Server | `<SERVER_IP>` |
| Network Subnet | `<NETWORK_SUBNET>` |

**Privacy Notice:** Actual home network configuration and private IP addresses are not published in this public repository.

## 4. Network Architecture Diagram

The planned network architecture:

```text
                 INTERNET
                     |
                     |
                HOME ROUTER
                     |
          +----------+----------+
          |                     |
          |                     |
     LENOVO G580           WINDOWS 11 PC
     UBUNTU SERVER         ADMIN WORKSTATION
          |                     |
          |                     |
    SERVER SERVICES        SECURITY TOOLS
          |
    +-----+------+----------------+
    |            |                |
   NAS         JELLYFIN       MONITORING
  SAMBA        MEDIA SERVER   UPTIME KUMA
    |
    |
  SHARED FILES

     FUTURE SECURITY SERVICES
     ------------------------
     ADGUARD HOME
     SURICATA
     WAZUH
```

## 5. Planned Network Services

| Service | Purpose | Status |
|---|---|---|
| SSH | Remote server administration | Working |
| Docker | Container management | Planned |
| Samba | NAS file sharing | Planned |
| Jellyfin | Media streaming | Planned |
| Tailscale | Secure remote access | Planned |
| AdGuard Home | DNS filtering and ad blocking | Planned |
| Uptime Kuma | Server availability monitoring | Planned |
| Suricata | Network intrusion detection | Planned |
| Wazuh | Security monitoring and SIEM | Planned |

## 6. Network Security

The following security measures are planned:

- Configure UFW firewall.
- Restrict unnecessary network ports.
- Secure SSH administration.
- Use Tailscale for remote access.
- Monitor network activity.
- Deploy Suricata for intrusion detection.
- Deploy Wazuh for centralized security monitoring.
- Keep cybersecurity testing inside authorized lab environments.

## 7. Remote Access Architecture

The server will support two types of access:

### Local Network Access

Authorized devices on the home network will access server services through the local network.

### Remote Access

Tailscale will be configured to allow secure access to the server from authorized devices outside the home network.

## 8. NAS and Media Architecture

The Hitachi 512 GB HDD is reserved for future storage services.

Planned configuration:

- Samba: Shared network storage.
- Jellyfin: Personal media streaming.
- Backups: Important files and server data.

Existing HDD partitions and files are being preserved until storage configuration is approved.

## 9. Cybersecurity Lab Architecture

The Windows workstation will be used for cybersecurity administration and authorized security testing.

The Lenovo server will host selected defensive monitoring and self-hosted services.

Future security tools:

- Suricata IDS.
- Wazuh SIEM.
- Firewall monitoring.
- Security event analysis.

Vulnerable lab machines and penetration-testing activities will be isolated from networks and systems that are not part of the authorized lab.


- Improve remote access security.
- Document network traffic and security events.
