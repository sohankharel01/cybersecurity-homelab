# 🛡️ Cybersecurity Homelab

### A Self-Hosted Environment for Cybersecurity, Networking & Infrastructure Engineering

A practical home-lab project built using a Lenovo G580 laptop and Ubuntu Server. The goal is to develop real-world skills in Linux administration, network security, infrastructure management, containerization, remote access, and self-hosted services.

**Project Status:** Active Development

---

## Overview

This project transforms an old Lenovo laptop into a self-hosted server and cybersecurity learning environment.

Rather than relying entirely on cloud services, the lab provides a platform to deploy, configure, secure, monitor, and troubleshoot real services.

### Objectives

- Build practical Linux server administration skills.
- Understand networking and network security.
- Deploy and manage containerized applications.
- Implement secure remote server access.
- Configure DNS filtering and firewall protection.
- Develop backup and storage infrastructure.
- Build a foundation for future cybersecurity projects.

---

## Hardware & Infrastructure

| Component | Specification |
|---|---|
| Device | Lenovo G580 |
| CPU | Intel Core i3-2328M |
| Memory | 8 GB RAM |
| Primary Storage | 128 GB Kingston SSD |
| Secondary Storage | 512 GB Hitachi HDD |
| Operating System | Ubuntu Server 24.04 LTS |

Ubuntu Server and core services run from the SSD. The secondary HDD is being prepared for dedicated storage services.

---

## Technology Stack

| Technology | Purpose | Status |
|---|---|---|
| Ubuntu Server | Server operating system | Operational |
| Docker | Container management | Operational |
| CasaOS | Application management | Operational |
| Cockpit | Server administration | Operational |
| Tailscale | Private remote access | Operational |
| AdGuard Home | DNS filtering and ad blocking | Operational |
| UFW | Host firewall | Operational |
| Samba | Network file sharing | Planned |
| Jellyfin | Media streaming | Planned |

---

## Architecture

```text
              REMOTE DEVICES
             (Phone / Laptop)
                     |
                  Tailscale
                     |
                     |
             HOME NETWORK
                     |
               Router / LAN
                     |
                     |
          LENOVO G580 SERVER
              Ubuntu Server
                     |
       +-------------+-------------+
       |             |             |
     Docker        UFW          SSH
       |
   +---+---------------------+
   |          |              |
 CasaOS    Cockpit       AdGuard Home
   |          |              |
   +----------+--------------+
                     |
              Storage Layer
                     |
             SSD + HDD
```

*Architecture represents the current and planned infrastructure. Storage services are not yet deployed.*

---

## Implemented Services

### 1. Ubuntu Server

Installed Ubuntu Server 24.04 LTS as the foundation of the infrastructure.

### 2. Docker

Installed and enabled Docker for containerized service deployment and management.

### 3. CasaOS

Deployed CasaOS to simplify application and container management through a web interface.

### 4. Cockpit

Configured Cockpit for browser-based Linux server administration and monitoring.

### 5. Tailscale

Implemented private remote access through a Tailscale network.

**Verification:** Successfully accessed the server's CasaOS dashboard from a mobile device using mobile data with Wi-Fi disabled.

### 6. AdGuard Home

Deployed AdGuard Home using Docker Compose.

Configured DNS filtering and tested domain blocking.

**Verification:** A DNS query for `doubleclick.net` returned `0.0.0.0`.

### 7. UFW Firewall

Enabled UFW with a default-deny incoming policy and configured rules for required server services.

---

## Backup & Reliability

Created a manual backup script to archive:

- AdGuard Home configuration and data.
- Docker Compose configuration.
- Selected system configuration files.

The backup script was manually executed and tested successfully.

Automatic scheduling and off-device backup are future improvements.

---

## Security Considerations

- Private remote access through Tailscale.
- Host firewall enabled.
- Incoming traffic restricted by firewall policy.
- Service management through controlled administrative interfaces.
- No credentials, private keys or sensitive configuration files committed to this repository.

---

## Roadmap

- [x] Install Ubuntu Server.
- [x] Configure SSH access.
- [x] Install Docker.
- [x] Deploy CasaOS.
- [x] Install Cockpit.
- [x] Configure Tailscale remote access.
- [x] Deploy AdGuard Home.
- [x] Configure UFW.
- [x] Create and test manual backup script.
- [ ] Complete personal data backup from secondary HDD.
- [ ] Configure NAS storage with Samba.
- [ ] Deploy Jellyfin.
- [ ] Implement multi-user storage permissions.
- [ ] Configure automated backups.
- [ ] Improve SSH and firewall hardening.
- [ ] Add monitoring and alerting.
- [ ] Document deployment and verification procedures.

---

## Skills Demonstrated

- Linux system administration
- Networking and DNS
- Firewall configuration
- Docker and container management
- Remote access infrastructure
- Service deployment and troubleshooting
- Backup scripting
- Server security fundamentals

---

## Project Philosophy

**Build it. Secure it. Test it. Document it.**

This is an ongoing hands-on learning project focused on developing practical infrastructure and cybersecurity engineering skills.

*Built and maintained as a personal cybersecurity homelab.*
