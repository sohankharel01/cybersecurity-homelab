# Hardware Specifications

## 1. Project Overview

The Lenovo G580 is being configured as a dedicated Ubuntu Server for a self-hosted server and cybersecurity homelab.

The system will support NAS storage, media streaming, network monitoring, security testing, remote access and self-hosted applications.

## 2. Server Hardware

| Component           | Specification       |
| ------------------- | ------------------- |
| Device              | Lenovo G580         |
| Machine Type        | 20157               |
| Processor           | Intel Core i3-2328M |
| CPU Frequency       | 2.20 GHz            |
| Physical CPU Cores  | 2                   |
| Logical CPU Threads | 4                   |
| RAM                 | 8 GB DDR3           |
| Primary Storage     | Kingston 128 GB SSD |
| Secondary Storage   | Hitachi 512 GB HDD  |
| Network             | Ethernet            |
| Firmware            | UEFI                |

## 3. Operating System

| Component          | Details                |
| ------------------ | ---------------------- |
| Operating System   | Ubuntu Server          |
| Version            | 24.04.5 LTS            |
| Architecture       | AMD64 (64-bit)         |
| Installation Drive | Kingston SSD           |
| Access Method      | SSH and local terminal |

## 4. Storage Configuration

### Primary SSD —  128 GB

Purpose:

- Ubuntu Server operating system
- System updates and packages
- Docker Engine and containers
- Application configurations
- Server logs

### Secondary HDD —  512 GB

Purpose:

- NAS file storage
- Jellyfin media library
- Shared files
- Backups

**Important:** The Hitachi HDD currently contains existing partitions. No partitions have been formatted or deleted. NAS storage configuration will be completed later.

## 5. Network Connectivity

- Primary network connection: Ethernet
- Server administration: SSH
- Planned remote access: Tailscale
- Planned file sharing: Samba

## 6. Planned Server Services

| Service      | Purpose                     | Status  |
| ------------ | --------------------------- | ------- |
| Docker       | Container management        | Planned |
| Samba        | NAS file sharing            | Planned |
| Jellyfin     | Media streaming             | Planned |
| Tailscale    | Remote access               | Planned |
| AdGuard Home | DNS ad blocking             | Planned |
| Uptime Kuma  | Server monitoring           | Planned |
| Suricata     | Network intrusion detection | Planned |
| Wazuh        | Security monitoring / SIEM  | Planned |

## 7. Hardware Limitations

The Lenovo G580 is an older laptop with limited processing power.

Important considerations:

- 8 GB RAM limits the number of heavy services running simultaneously.
- The dual-core processor requires efficient resource management.
- Wazuh and other resource-intensive applications may need separate deployment or reduced workloads.
- Storage capacity must be managed carefully.

## 8. Project Objectives

1. Build a dedicated Linux server.
2. Create a self-hosted NAS.
3. Host a Jellyfin media server.
4. Learn Docker and Linux administration.
5. Implement network monitoring.
6. Practice defensive and offensive cybersecurity in authorized lab environments.
7. Develop a practical Red Team and Blue Team homelab.
