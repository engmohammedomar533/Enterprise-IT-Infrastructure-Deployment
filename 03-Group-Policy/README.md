# Group Policy Management

## Overview

Group Policy was implemented to centralize workstation configuration, automate resource deployment, enforce security standards, and simplify administration across the organization.

The environment utilizes Organizational Units (OUs) and Group Policy Objects (GPOs) to apply settings based on user roles and workstation requirements.

---

# Current GPO Deployment

## Drive Mapping

### Status
Implemented

### Purpose

Automatically map departmental file shares when users sign in.

### Mapped Resources

- InProgress
- Final
- Managerial
- Scans
- OsosDocs (Management Only)

### Benefits

- Consistent user experience
- Simplified file access
- Centralized management
- Reduced support requirements

---

## Printer Deployment

### Status
Implemented

### Purpose

Automatically deploy network printers to domain users.

### Printer

- Canon 4056i

### Deployment Method

- Group Policy Printer Deployment

### Benefits

- Automatic installation
- Centralized management
- Consistent printer configuration

---

## Manager Local Administrator Rights

### Status
Implemented

### Purpose

Provide local administrative access to authorized management personnel while maintaining security controls.

### Benefits

- Controlled privilege elevation
- Reduced dependency on IT support
- Improved workstation management

---

## Power Management Policy

### Status
Implemented

### Purpose

Standardize workstation power settings and reduce unnecessary power consumption.

### Benefits

- Energy efficiency
- Consistent workstation behavior
- Improved hardware longevity

---

## Windows Defender Management

### Status
Implemented

### Purpose

Control Windows Defender configuration across managed systems.

### Benefits

- Consistent security posture
- Centralized administration
- Reduced user configuration errors

---

# Planned Security Hardening Policies

## Software Restriction Policy

### Status
Planned

### Deployment Timing

After all engineering applications have been fully tested and approved.

### Objective

Prevent execution of unauthorized applications.

### Restricted Locations

- Downloads
- Desktop
- Temp
- AppData

### Allowed Locations

- Program Files
- Program Files (x86)
- Approved Application Directories

### Benefits

- Malware prevention
- Ransomware mitigation
- Reduced unauthorized software installation

---

## USB Device Control

### Status
Planned

### Objective

Control removable storage device usage.

### Proposed Configuration

- Standard Users: USB Storage Blocked
- IT Administration: Allowed
- Management: As Required

### Benefits

- Data Loss Prevention
- Malware Protection
- Improved Security

---

## Control Panel Restrictions

### Status
Planned

### Objective

Prevent unauthorized system modifications.

### Proposed Restrictions

- Network Configuration
- User Account Changes
- Installed Programs
- System Settings

### Benefits

- Configuration Consistency
- Reduced Support Incidents

---

## Command Prompt Restrictions

### Status
Planned

### Objective

Prevent unauthorized script execution and system modifications.

### Scope

- Standard Users
- Engineering Workstations

### Benefits

- Reduced Attack Surface
- Improved Endpoint Security

---

## PowerShell Restrictions

### Status
Planned

### Objective

Limit unauthorized PowerShell execution.

### Benefits

- Reduced Security Risks
- Improved Administrative Control

---

## Application Whitelisting

### Status
Future Phase

### Objective

Allow only approved software to execute.

### Examples

- AutoCAD
- Revit
- ETABS
- SAFE
- SAP2000
- Microsoft Office
- Approved Engineering Tools

---

# Administrative Strategy

The organization follows a centralized management model where:

- User accounts are managed through Active Directory.
- Resource access is controlled through Security Groups.
- Workstation configuration is managed through Group Policy.
- Administrative privileges are limited to authorized personnel.

---

# Lessons Learned

- Group Policy significantly reduces workstation administration effort.
- Automated printer deployment simplifies onboarding.
- Automated drive mapping improves usability and consistency.
- Security hardening should be phased to avoid disrupting business operations.
- Engineering software requirements must be fully validated before applying restrictive policies.

---

# Technologies Used

- Active Directory
- Group Policy Management Console (GPMC)
- Organizational Units (OUs)
- Security Groups
- Windows Defender
- Windows Server 2025
