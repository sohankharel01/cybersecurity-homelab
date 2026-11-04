# Troubleshooting Guide

## 1. Overview

This document records the actual technical problems encountered while installing and configuring Ubuntu Server on the Lenovo G580.

It includes the problems, troubleshooting steps, solutions and current status of each issue.

The purpose is to maintain a technical record of the server setup process and provide a reference for future troubleshooting.

## 2. Ubuntu Server Installation Issues

### Issue 1: Ubuntu Package Mirror Timeout

**Problem:**

During Ubuntu Server installation, the installer attempted to test the configured package mirror but displayed a timeout message.

The package mirror is used to download Ubuntu software packages and updates.

**Troubleshooting Performed:**

1. Waited for the mirror test to complete.
2. Observed the timeout message.
3. Continued with the installation process.
4. Allowed the installer to proceed.

**Result:**

Ubuntu Server installation was eventually completed successfully.

**Verification:**

- Ubuntu Server booted successfully.
- Login was available.
- Package updates were completed after installation.

**Status:** Resolved.

---

### Issue 2: Installation Storage Not Immediately Visible

**Problem:**

During Ubuntu Server installation, the intended installation storage was not immediately visible in the installer's storage configuration screen.

**Troubleshooting Performed:**

1. Inspected the available storage devices.
2. Checked the existing partition layout.
3. Identified the intended operating system installation destination.
4. Selected the correct installation destination.

**Solution:**

Ubuntu Server was successfully installed on the intended operating system storage.

**Verification:**

The server booted successfully into Ubuntu Server.

**Status:** Resolved.

---

### Issue 3: Installer Update Check Delay

**Problem:**

During installation, the installer displayed a message indicating that it was checking for installer updates.

The process took some time, and it was unclear whether to wait or continue.

**Troubleshooting Performed:**

1. Waited for the installer update check.
2. Observed the installation progress.
3. Continued with the installation process.

**Result:**

The installation continued successfully.

**Status:** Installation completed.

---

### Issue 4: Waiting for Cloud-init

**Problem:**

During the installation process, the screen displayed a message indicating that it was waiting for cloud-init.

This caused uncertainty about whether the installation was still progressing.

**Troubleshooting Performed:**

1. Observed the initialization message.
2. Allowed the process to continue.
3. Continued with the server setup after initialization.

**Result:**

Ubuntu Server became accessible.

**Status:** Installation completed.

## 3. BIOS and Boot Troubleshooting

### Issue 5: Difficulty Accessing Lenovo BIOS

**Problem:**

We attempted to access the Lenovo G580 BIOS configuration interface but could not open it using the initial startup methods.

**Troubleshooting Performed:**

1. Attempted to enter BIOS during startup.
2. Tried different keyboard timing methods.
3. Explored Windows advanced startup settings.
4. Investigated alternative ways to access firmware settings.

**Result:**

The BIOS interface did not open during these attempts.

However, Ubuntu Server installation was completed successfully.

**Status:** Requires further investigation.

## 4. Network and SSH Troubleshooting

### Issue 6: Initial Ping Test Timeout

**Problem:**

During the initial network configuration, a ping test from the Windows computer to the reported Lenovo server IP address timed out.

**Troubleshooting Performed:**

1. Identified the router gateway address.
2. Checked the Windows computer's IPv4 configuration.
3. Tested communication from the Lenovo server to the router.
4. Confirmed that the router ping from the Lenovo server was successful.

**Result:**

The Lenovo server successfully communicated with the router.

The initial failed ping from Windows was not conclusively diagnosed.

**Status:** Partially investigated.

---

### Issue 7: SSH Remote Access

**Objective:**

Enable remote administration of the Ubuntu Server from another computer.

**Configuration and Testing:**

1. Connected the Lenovo server to the network using Ethernet.
2. Configured SSH access.
3. Tested the remote connection.
4. Successfully accessed the server through a remote terminal.

**Result:**

SSH remote administration is working.

**Verification:**

- Remote SSH connection: Successful.
- Remote terminal access: Successful.
- Server command execution: Working.

**Status:** Resolved.

## 5. Storage Management and Data Protection

### Issue 8: Preserving Existing Storage Data

**Problem:**

The computer contained existing partitions and files that needed to be preserved during the Ubuntu Server installation.

The secondary storage was reserved for future NAS and Jellyfin configuration.

**Actions Taken:**

1. Inspected the available storage devices and partitions.
2. Identified existing filesystem types and partition labels.
3. Selected the intended operating system installation destination.
4. Avoided unnecessary formatting.
5. Preserved the existing secondary storage.
6. Postponed NAS and Samba configuration.

**Result:**

The existing secondary storage was left untouched.

No unnecessary partition deletion or formatting was performed.

**Status:** Data preserved.

## 6. Ubuntu System Preparation

### Issue 9: Initial System Updates and Essential Utilities

**Objective:**

Prepare the newly installed Ubuntu Server for administration and future configuration.

**Commands Executed:**

Update package information:

```bash
sudo apt update
```

Install available system upgrades:

```bash
sudo apt upgrade -y
```

Install essential utilities:

```bash
sudo apt install -y curl wget git nano htop unzip ca-certificates gnupg
```

**System Verification:**

Operating system information:

```bash
lsb_release -a
```

CPU information:

```bash
lscpu
```

Memory usage:

```bash
free -h
```

Storage information:

```bash
lsblk
```

System architecture:

```bash
dpkg --print-architecture
```

**Result:**

- Ubuntu Server 24.04.5 LTS installed.
- System updates completed.
- Essential administration utilities installed.
- CPU information verified.
- Memory information verified.
- Storage layout inspected.
- System architecture checked.

**Status:** Completed.

## 7. Current Troubleshooting Status

| Issue | Current Status |
|---|---|
| Package mirror timeout | Resolved |
| Installation storage detection | Resolved |
| Installer update check delay | Completed |
| Cloud-init waiting message | Completed |
| BIOS access difficulty | Needs investigation |
| Initial ping timeout | Partially investigated |
| Router connectivity | Successful |
| SSH remote access | Successful |
| Existing storage preservation | Completed |
| Ubuntu system updates | Completed |

## 8. Documentation Maintenance

This document will be updated whenever a new technical problem occurs during the development of the Lenovo Cybersecurity Homelab.

Each issue should include:

- The actual problem encountered.
- The troubleshooting steps performed.
- Commands used, where applicable.
- The solution or current findings.
- Verification results.
- Final issue status.

Only tested solutions should be marked as resolved.

**Current Milestone:** Ubuntu Server installation, initial system preparation and SSH remote access completed.
