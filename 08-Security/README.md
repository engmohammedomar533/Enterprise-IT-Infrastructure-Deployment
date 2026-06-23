# Security Architecture

## Overview

Security was a core consideration throughout the design and deployment of the infrastructure. The environment was designed to provide centralized authentication, controlled resource access, network segmentation, and data protection while maintaining operational efficiency for engineering and administrative departments.

The security strategy follows a layered defense approach combining Active Directory, network segmentation, access controls, backup protection, and future hardening initiatives.

---

# Security Objectives

- Centralized Identity Management
- Controlled Access to Resources
- Network Segmentation
- Protection Against Data Loss
- Controlled Administrative Access
- Secure Department Collaboration
- Business Continuity
- Future Security Scalability

---

# Identity and Access Management

## Active Directory Authentication

### Status

Implemented

### Purpose

Provide centralized authentication and authorization for all users and workstations.

### Benefits

- Single Sign-On (SSO)
- Centralized Account Management
- Password Policy Enforcement
- Simplified Administration

---

## Domain Membership

### Status

Implemented

### Scope

- 21 Workstations
- Windows Server Infrastructure

### Benefits

- Centralized Control
- Group Policy Management
- Improved Security Monitoring

---

# Role-Based Access Control

## Security Groups

### Status

Implemented

Access to resources is controlled through Active Directory Security Groups rather than individual user permissions.

### Benefits

- Easier Administration
- Simplified Auditing
- Reduced Permission Errors
- Better Scalability

---

## Department-Based Permissions

### Status

Implemented

Departments have access only to resources required for their responsibilities.

### Examples

- Management Resources
- HR Resources
- Engineering Resources
- Shared Resources

### Benefits

- Principle of Least Privilege
- Reduced Data Exposure
- Improved Security

---

# File Server Security

## NTFS Permissions

### Status

Implemented

Permissions are applied using:

- Security Groups
- Folder-Level Permissions
- Inheritance Controls

### Benefits

- Granular Access Control
- Improved Data Protection
- Simplified Administration

---

## Restricted Shares

### Status

Implemented

Restricted resources include:

- Management Shares
- Confidential Documentation
- Administrative Resources

### Benefits

- Protect Sensitive Information
- Limit Unauthorized Access

---

# Network Security

## VLAN Segmentation

### Status

Implemented

The network is separated into multiple security zones.

### VLAN 10 - Corporate Network

Used For:

- Domain Workstations
- Servers
- Printers
- Attendance Systems
- Network Infrastructure

### VLAN 20 - Guest Network

Used For:

- Mobile Devices
- Visitors
- Guest Wireless Access

---

## Inter-VLAN Isolation

### Status

Implemented

Communication between VLANs is restricted.

### Benefits

- Reduced Attack Surface
- Protection of Corporate Resources
- Separation of Personal Devices

---

# Endpoint Protection

## Microsoft Defender

### Status

Implemented

Used to provide:

- Malware Protection
- Threat Detection
- Real-Time Scanning

### Benefits

- Baseline Endpoint Security
- Centralized Security Posture

---

# Administrative Security

## Administrative Accounts

### Status

Implemented

Dedicated administrative accounts are used for infrastructure management.

### Responsibilities

- Active Directory Administration
- Group Policy Management
- File Server Administration
- Backup Administration
- Print Services Administration

### Benefits

- Separation of Duties
- Reduced Risk
- Improved Accountability

---

## Local Administrator Control

### Status

Implemented

Administrative rights are restricted to authorized personnel.

### Benefits

- Reduced Unauthorized Changes
- Improved Security Control

---

# Data Protection

## RAID 1 Storage

### Status

Implemented

Provides protection against:

- Single Disk Failure
- Storage Hardware Failure

### Important Note

RAID improves availability but is not a backup solution.

---

## Shadow Copies

### Status

Implemented

Provides:

- File Recovery
- Previous Version Recovery
- Accidental Deletion Recovery

---

## Backup Protection

### Status

Implemented

Protected Components:

- Active Directory
- DNS
- File Server
- Group Policies
- Operating System
- User Data

---

# Attendance System Security

## BioTime Access Control

### Status

Implemented

Access to attendance management is restricted to authorized personnel.

### Security Features

- User Authentication
- Role-Based Access
- Biometric Verification

---

## Biometric Authentication

### Status

Implemented

Authentication Methods:

- Fingerprint Recognition
- Facial Recognition

### Benefits

- Reduced Attendance Fraud
- Improved Accuracy
- Strong User Verification

---

# Security Monitoring

## Current Monitoring

### Status

Basic Monitoring Implemented

Activities Include:

- Backup Verification
- Event Log Review
- User Administration
- Device Status Monitoring

---

# Planned Security Enhancements

## Windows LAPS

### Status

Planned

### Objective

Provide unique local administrator passwords for every workstation.

### Benefits

- Reduced Credential Exposure
- Improved Endpoint Security

---

## Software Restriction Policies

### Status

Planned

### Deployment Timing

After all engineering applications have been installed and validated.

### Restricted Locations

- Downloads
- Desktop
- Temp
- AppData

### Benefits

- Malware Prevention
- Ransomware Protection
- Reduced Unauthorized Software

---

## USB Device Control

### Status

Planned

### Objective

Control removable storage usage.

### Benefits

- Data Loss Prevention
- Malware Mitigation

---

## PowerShell Restrictions

### Status

Planned

### Objective

Reduce unauthorized scripting activity.

---

## Command Prompt Restrictions

### Status

Planned

### Objective

Reduce unauthorized system modifications.

---

## Application Whitelisting

### Status

Future Phase

### Objective

Allow execution only for approved software.

### Examples

- AutoCAD
- Revit
- ETABS
- SAFE
- SAP2000
- Microsoft Office

---
## Time Synchronization

Configured the Domain Controller as the authoritative time source for the domain.

Implementation:

- External NTP synchronization via pool.ntp.org
- Domain hierarchy time distribution
- Automatic workstation synchronization through Active Directory

Benefits:

- Accurate Kerberos authentication
- Consistent logging and auditing
- Reliable certificate validation
- Centralized time management
## Security Auditing

### Status

Planned

### Future Audit Events

- File Deletions
- Permission Changes
- Logon Events
- Administrative Activities
- USB Usage

---

# Security Design Principles

The environment was designed around the following principles:

- Least Privilege
- Defense in Depth
- Centralized Management
- Role-Based Access Control
- Network Segmentation
- Business Continuity
- Secure Growth Planning

---

# Lessons Learned

- Security must be integrated from the beginning of infrastructure design.
- Group-based permissions are easier to manage than individual permissions.
- Network segmentation significantly improves security posture.
- Backup and recovery are essential security components.
- Business requirements must be balanced with security controls.
- Security hardening should be phased to avoid disrupting operations.

---

# Future Security Roadmap

## Phase 1

- Windows LAPS
- Software Restriction Policies
- USB Control

## Phase 2

- Security Auditing
- PowerShell Restrictions
- Command Prompt Restrictions

## Phase 3

- Application Whitelisting
- Security Monitoring Enhancements
- Reporting and Alerting

---

# Technologies Used

- Windows Server 2025
- Active Directory
- Group Policy
- NTFS Permissions
- Microsoft Defender
- Omada SDN
- VLAN Segmentation
- Windows Server Backup
- RAID 1
- Shadow Copies
- BioTime
- Biometric Authentication

---

# Project Outcome

The deployed security architecture provides layered protection through centralized authentication, role-based access control, network segmentation, data protection mechanisms, and a structured roadmap for future hardening initiatives.

The environment is designed to support current business requirements while providing a foundation for future security growth and operational maturity.
