# Virtualized Windows Environment Documented Lab

**Prepared by:** Douglas Babcock  
**Date:** 2025-11-01  
**Lab focus:** Virtualized Windows environment setup and connectivity verification

## Skim Summary

Built a small VirtualBox-based Windows lab environment for a fictional healthcare startup, Evergreen Diagnostics. The environment included one Windows Server 2022 system and two Windows 11 Enterprise workstations on a NAT network. The lab demonstrated operating-system installation, virtual machine cloning, IP/network configuration, and connectivity verification between systems and the internet.

## Environment Built

| VM | Operating System | RAM | CPU | IP Address |
|---|---|---:|---:|---|
| `ED-SRV01` | Windows Server 2022 Standard | 4 GB | 2 cores | `10.0.2.3` |
| `ED-PC01` | Windows 11 Enterprise / Pro | 4 GB | 2 cores | `10.0.2.4` |
| `ED-PC02` | Windows 11 Enterprise / Pro | 4 GB | 2 cores | `10.0.2.5` |

## Main Tasks

### 1. Server installation and configuration

- Created a new VirtualBox VM for `ED-SRV01`.
- Installed Windows Server 2022 Standard with Desktop Experience.
- Allocated appropriate VM resources, including RAM, CPU, and virtual disk.
- Verified successful installation through the administrator logon screen.

### 2. Windows workstation installation

- Created and configured the first Windows 11 workstation, `ED-PC01`.
- Installed Windows 11 Enterprise.
- Created a local account for the workstation.
- Verified initial network connectivity to the server.

### 3. Workstation cloning

- Created `ED-PC02` as a full clone of `ED-PC01`.
- Used cloning to save setup time and maintain workstation consistency.

### 4. Connectivity verification

Verified network communication between the virtual machines and external internet access.

| Test | Outcome |
|---|---|
| `ED-SRV01` → `ED-PC01` | Success |
| `ED-PC01` → `ED-SRV01` | Success |
| `ED-SRV01` → `ED-PC02` | Success |
| `ED-SRV01` → Gateway | Success |
| `ED-SRV01` → `www.bing.com` | Success |

Additional ping tests were performed between `ED-PC01`, `ED-PC02`, `ED-SRV01`, the default gateway, and `bing.com`.

## Skills Demonstrated

- VirtualBox VM creation and configuration
- Windows Server 2022 installation
- Windows 11 workstation installation
- NAT network setup
- VM cloning
- IP addressing and connectivity testing
- Basic Windows lab documentation
- Screenshot-based evidence collection

## Portfolio Value

This lab shows hands-on ability to build a controlled Windows infrastructure lab from scratch, verify network connectivity, and document implementation steps clearly. It supports entry-level IT support, help desk, desktop support, junior systems administration, and networking roles.

## Source Document

Full source document with evidence/screenshots:

- `Virtualized_Windows_Environment_Documented_Lab.docx`
