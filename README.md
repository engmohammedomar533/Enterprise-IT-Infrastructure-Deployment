# Enterprise IT Infrastructure Deployment

## Overview

Designed and deployed a complete enterprise IT infrastructure for a multi-department engineering office supporting 21 workstations.

This project demonstrates the implementation of a production-ready Windows Server environment including centralized authentication, file services, print services, network management, backup and disaster recovery, and biometric attendance integration.

---

## Infrastructure Components

### Server Infrastructure

- Windows Server 2025
- Active Directory Domain Services (AD DS)
- DNS Server
- Group Policy Management
- File Server
- Print Server
- Windows Server Backup
- Shadow Copies

### Network Infrastructure

- TP-Link Omada SDN
- ER605 Router
- SG2218P Managed Switch
- 3 × EAP620 HD Access Points
- VLAN Segmentation
- Corporate and Guest Networks

### Security

- Active Directory Authentication
- NTFS Permissions
- Security Groups
- Department-Based Access Control
- Group Policy Management
- Enterprise NTFS File Auditing
- Advanced Audit Policy Configuration
- Security Event Monitoring
- File Modification Tracking
- File Deletion Tracking
- File Rename Tracking
- File Move Tracking
- Permission Change Auditing
- Security Event Investigation Procedures

### Attendance System

- ZKTeco BioTime
- MB5000 Biometric Terminal
- Fingerprint Authentication
- Facial Recognition
- Flexible Attendance Policies

---

## Network Design

### VLAN 10 - Corporate Network

Used for:

- Domain Workstations
- Servers
- Printers
- Biometric Systems
- Network Infrastructure

### VLAN 20 - Guest Network

Used for:

- Mobile Devices
- Guest Wi-Fi
- Personal Devices

Security Controls:

- Inter-VLAN Isolation
- Guest Access Restrictions
- Separation from Corporate Resources

---

## Storage and Backup

### Production Storage

- RAID 1 Mirror Configuration
- Centralized File Storage
- Department Shares

### Data Protection

- Windows Server Backup
- Bare Metal Recovery
- System State Backup
- Shadow Copies
- External Backup Storage

---

## Active Directory Structure

Implemented:

- Organizational Units (OUs)
- Security Groups
- Department-Based User Management
- Drive Mapping
- Printer Deployment

Departments:

- Management
- HR
- Architectural Engineering
- Structural Engineering
- Mechanical Engineering
- Electrical Engineering

---

## Technologies Used

- Windows Server 2025
- Active Directory
- DNS
- Group Policy
- NTFS Permissions
- Windows Server Backup
- Omada SDN
- VLANs
- ZKTeco BioTime
- RAID Storage
- Shadow Copies

---

## Project Goals

- Centralized Authentication
- Centralized File Storage
- Secure Department Access
- Automated Printer Deployment
- Biometric Attendance Management
- Backup and Disaster Recovery
- Scalable Infrastructure Design

---

## Current Status

Production Environment Operational

- Domain Services Operational
- File Services Operational
- Print Services Operational
- Backup System Operational
- Attendance System Operational
- VLAN Segmentation Operational

---

## Author

Mohammed Younis

Senior IT Systems Administrator | Infrastructure & Network Architect | Windows Server & Active Directory | Expanding into AWS & Azure Cloud
