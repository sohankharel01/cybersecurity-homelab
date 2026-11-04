
# Installation Guide

## 1. Overview

This guide documents the installation of Ubuntu Server 24.04.5 LTS on a Lenovo G580 for a dedicated cybersecurity homelab and self-hosted server.

## 2. Requirements

### Hardware
- Lenovo G580 laptop.
- 8 GB RAM.
- Kingston 128 GB SSD.
- USB flash drive (8 GB or larger).
- Ethernet connection.
- External monitor and keyboard for installation.

### Software
- Ubuntu Server 24.04.5 LTS ISO.
- Rufus for creating bootable USB media.

## 3. Creating the Bootable USB

1. Download Ubuntu Server 24.04.5 LTS.
2. Download and open Rufus on Windows.
3. Connect the USB flash drive.
4. Select the Ubuntu ISO.
5. Configure the USB for UEFI boot.
6. Start the USB creation process.

## 4. Ubuntu Server Installation

1. Connect the bootable USB to the Lenovo G580.
2. Boot from the USB drive.
3. Select Ubuntu Server installation.
4. Configure language and keyboard.
5. Configure network connectivity.
6. Select the Kingston SSD as the installation drive.
7. Complete the installation.
8. Create the server username and password.
9. Restart the system after installation.
10. Log in to Ubuntu Server.

## 5. Initial System Configuration

Update package information:

```bash
sudo apt update
```

Install available upgrades:

```bash
sudo apt upgrade -y
```

Install essential utilities:

```bash
sudo apt install -y curl wget git nano htop unzip ca-certificates gnupg
```

## 6. Verify System Information

Check Ubuntu version:

```bash
lsb_release -a
```

Check processor:

```bash
lscpu
```

Check memory:

```bash
free -h
```

Check storage:

```bash
lsblk
```

Check system architecture:

```bash
dpkg --print-architecture
```

## 7. Remote Administration

SSH access was tested successfully.

The server can be managed remotely using a terminal.

## 8. Storage 

The SSD contains the Ubuntu installation.

The HDD is reserved for  NAS and Jellyfin storage.





