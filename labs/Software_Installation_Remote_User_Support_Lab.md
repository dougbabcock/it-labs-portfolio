# Software Installation and Remote User Support Lab

**Prepared by:** Douglas Babcock  
**Date:** 2025-11-16  
**Lab focus:** Software installation and supporting users remotely

## Summary

Created a centralized software repository on a Windows server and used Remote Desktop to support a client workstation. The lab demonstrated safe software sourcing, shared network repository access, remote support workflow, installation of approved applications, and post-installation verification.

## Scenario

Evergreen Diagnostics needed approved software installed on a Finance Officer's workstation. The support workflow used `ED-SRV01` as the administrative/server system and `ED-CL01` as the client workstation.

## Main Tasks

### 1. Create a centralized software repository

Created a `SoftwareRepository` folder on `ED-SRV01`.

Repository access was configured with:

- A shared network folder
- Authenticated user access for reading/installing software
- Administrator full-control access through NTFS permissions

**Purpose:** Provide a centralized, controlled location for approved installers.

### 2. Download approved software

Downloaded approved applications from official vendor websites, then copied the installers into the shared repository.

Applications included:

- Google Chrome
- Malwarebytes Anti-Malware
- Adobe Acrobat Reader
- 7-Zip

**Purpose:** Ensure installers came from legitimate sources before making them available for client installation.

### 3. Connect to the client workstation remotely

Established a Remote Desktop session from `ED-SRV01` to the Finance Officer's workstation, `ED-CL01`, using the client's IP address.

**Purpose:** Demonstrate remote administrative support for a user workstation.

### 4. Access the repository from the client

From the remote desktop session, accessed the shared software repository using the server hostname path:

```text
\\ED-SRV01\SoftwareRepository
```

**Purpose:** Verify the client could reach shared network resources over the domain/network.

### 5. Install and verify applications

Installed the required applications on `ED-CL01` from the shared repository.

Verification included:

- Installation progress/setup evidence
- Installed Apps / Start Menu confirmation
- Launching at least one installed application successfully

## Evidence Collected

The source lab document references screenshots showing:

- `C:\SoftwareRepository` created on `ED-SRV01`
- Advanced Sharing configuration
- NTFS Security tab permissions
- Downloaded installer files before and after copying
- Official vendor download page evidence
- Remote Desktop connection window
- Active remote session to `ED-CL01`
- Client access to `\\ED-SRV01\SoftwareRepository`
- Installation progress or setup window
- Installed applications list
- Successfully launched application

## Skills Demonstrated

- Windows shared-folder setup
- Basic NTFS/share permission awareness
- Safe software download practices
- Centralized software repository workflow
- Remote Desktop support
- Hostname-based access to shared network resources
- Client software installation
- Post-installation verification
- User-support documentation

## Source Document

Full source document with evidence/screenshots:

- `Software_Installation_Remote_User_Support_Lab.docx`
