# Windows Group Policy Security Lab

**Prepared by:** Douglas Babcock  
**Date:** 2025-11-16  
**Lab focus:** Securing Windows using Group Policy

## Summary

Implemented Group Policy configurations to strengthen security and standardize a Windows domain environment for a fictional organization, Evergreen Diagnostics. The lab translated compliance-style requirements into centrally managed domain policies using Group Policy Management Console. The work included password and account lockout controls, a domain logon security message, corporate desktop branding, and verification using `gpupdate` and `gpresult`.

## Main Policies Implemented

### 1. Password and account lockout policy

Updated the Default Domain Policy to enforce stronger account security controls across the domain.

Configured policy areas included:

- Minimum password length
- Password complexity requirements
- Maximum password age
- Account lockout standards

**Purpose:** Improve credential security and reduce exposure to weak passwords or brute-force attempts.

### 2. Domain logon security message

Created and linked a new Group Policy Object named `Domain Logon Security Message`.

The policy displayed a legal/security banner before authentication, informing users that:

- Access is restricted to authorized personnel.
- Systems are intended for official business.
- User activity may be monitored.

**Purpose:** Increase user accountability and communicate acceptable-use expectations before login.

### 3. Corporate desktop branding

Created and linked a `Corporate Desktop Branding` GPO.

The configuration:

- Created a shared branding folder on `ED-SRV01`.
- Stored the approved corporate wallpaper in the shared location.
- Applied the wallpaper automatically to domain workstations.
- Prevented users from changing the desktop background.

**Purpose:** Standardize the workstation desktop experience and reinforce organizational branding.

### 4. Policy verification

Verified policy application on `ED-PC01` using:

- `gpupdate /force`
- `gpresult /r`

The required GPOs appeared in the applied policy list, confirming deployment to the workstation.

## Evidence Collected

The source lab document references screenshots showing:

- Default Domain Policy opened in GPMC
- Password policy settings
- Account lockout policy settings
- GPO links in the domain
- Security Options configuration
- Logon banner displayed on `ED-PC01`
- Shared branding folder on `ED-SRV01`
- Client access to `\\ED-SRV01\Branding`
- Desktop wallpaper policy settings
- Prevent-changing-background policy setting
- `gpupdate /force` confirmation
- `gpresult /r` applied GPO output

## Skills Demonstrated

- Group Policy Management Console usage
- Domain-level password and lockout policy configuration
- Windows security baseline implementation
- Legal logon banner configuration
- Shared folder usage for centralized policy assets
- Desktop environment standardization
- Policy deployment and verification with `gpupdate` and `gpresult`
- Evidence-based lab documentation

## Source Document

Full source document with evidence/screenshots:

- `Windows_Group_Policy_Security_Lab.docx`
