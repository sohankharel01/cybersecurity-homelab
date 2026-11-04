# cybersecurity-homelab
Building a self-hosted Ubuntu home server with Docker, Wazuh SIEM, Suricata IDS, AdGuard Home, Samba, Jellyfin and Tailscale.
# Lenovo Cybersecurity HomeLab

**A self-hosted home server for Linux administration, infrastructure management, network security, and cybersecurity learning.**

![Status](https://img.shields.io/badge/Status-In%20Progress-orange)
![OS](https://img.shields.io/badge/OS-Ubuntu%20Server-orange)
![Platform](https://img.shields.io/badge/Platform-Lenovo%20Hardware-blue)
![Focus](https://img.shields.io/badge/Focus-Cybersecurity-red)

## Overview

This project transforms an old Lenovo computer into a multi-purpose home server.

The objective is to build an affordable self-hosted infrastructure environment that combines home-server applications with practical cybersecurity monitoring.

The server will provide file sharing, media streaming, network-wide advertisement blocking, remote access, infrastructure monitoring, and security event detection.

A separate Windows 11 computer will serve as the primary administration workstation and penetration-testing environment.

## Hardware Specifications

| Component | Specification |
|---|---|
| Processor | Intel Core i3 |
| RAM | 8 GB |
| Primary Storage | 128 GB SSD |
| Secondary Storage | 512 GB HDD |
| Network | Ethernet |
| Existing OS | Windows 10 Home |
| Planned OS | Ubuntu Server 24.04 LTS |

## Architecture

The Lenovo will act as the central server, while the Windows 11 PC will be used for administration and authorized security testing.

### Planned Software Stack

| Software | Purpose |
|---|---|
| Ubuntu Server | Server operating system |
| Docker | Container management |
| Tailscale | Secure remote access |
| OpenSSH | Remote administration |
| AdGuard Home | Network-wide DNS ad and tracker blocking |
| Samba | Network file sharing |
| Jellyfin | Media streaming |
| Uptime Kuma | Infrastructure monitoring |
| Wazuh | SIEM and security monitoring |
| Suricata | Network intrusion detection |

## Project Objectives

- Build a low-cost home server.
- Learn Linux server administration.
- Understand networking and network security.
- Deploy self-hosted applications using Docker.
- Implement network-wide DNS filtering.
- Build a practical SIEM environment.
- Monitor security events and investigate alerts.
- Practice authorized penetration testing.
- Document every installation and configuration.

## Project Roadmap

### Phase 1 — Network Preparation
- [x] Connect Lenovo to the home router.
- [x] Verify Lenovo-to-router connectivity.
- [x] Troubleshoot Lenovo-to-Windows PC connectivity.
- [x] Verify communication between computers.

### Phase 2 — Operating System Installation
- [x] Download Ubuntu Server ISO.
- [x] Configure Rufus for UEFI boot.
- [ ] Create bootable USB.
- [ ] Install Ubuntu Server.
- [ ] Configure storage.
- [ ] Configure SSH.

### Phase 3 — Core Server Configuration
- [ ] Configure static DHCP reservation.
- [ ] Configure Tailscale.
- [ ] Configure firewall.
- [ ] Install Docker Engine.
- [ ] Configure Docker Compose.

### Phase 4 — Home Server Applications
- [ ] Deploy AdGuard Home.
- [ ] Configure DNS filtering.
- [ ] Deploy Samba.
- [ ] Deploy Jellyfin.
- [ ] Deploy Uptime Kuma.
- [ ] Configure backups.

### Phase 5 — Cybersecurity Monitoring
- [ ] Deploy Wazuh.
- [ ] Install Windows monitoring agent.
- [ ] Deploy Suricata.
- [ ] Configure security alerts.
- [ ] Perform authorized detection tests.
- [ ] Document security investigations.

### Phase 6 — Final Testing
- [ ] Test remote access.
- [ ] Test shared storage.
- [ ] Test DNS filtering.
- [ ] Test media streaming.
- [ ] Test security monitoring.
- [ ] Document final architecture.

## Storage Plan

**128 GB SSD**
- Ubuntu Server
- Docker application data
- Wazuh index and logs

**512 GB HDD**
- Shared files
- Media library
- Backups

Final disk allocation will be documented after installation.

## Learning Outcomes

This project is designed to develop practical skills in:

- Linux administration
- TCP/IP networking
- DNS and network filtering
- SSH and remote access
- Docker and containerization
- SIEM operations
- Intrusion detection
- Security event analysis
- Infrastructure monitoring
- Backup and storage management

## Documentation

Installation instructions, configurations, architecture diagrams, troubleshooting notes, and test results will be maintained in the `docs/` directory.

## Disclaimer

This project is intended for educational purposes and authorized security testing only.

All penetration-testing activities will be performed in environments where permission has been granted.

## Project Status

**Currently in development.**

This repository will be updated as the server is built, tested, and documented.
