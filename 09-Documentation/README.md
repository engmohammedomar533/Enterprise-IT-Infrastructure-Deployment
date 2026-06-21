# Project Documentation and Executive Summary

## Project Overview

This project documents the design, deployment, and administration of a complete enterprise IT infrastructure for a multi-department engineering office.

The environment was designed to provide centralized authentication, secure file storage, network segmentation, printer management, attendance automation, backup and disaster recovery, and centralized administration.

The project demonstrates real-world systems administration, infrastructure deployment, troubleshooting, security implementation, and operational planning.

---

# Business Requirements

The organization required a centralized IT infrastructure capable of supporting:

- 21 Workstations
- Multiple Engineering Departments
- Human Resources
- Management Staff
- Centralized File Storage
- Centralized User Management
- Secure Resource Access
- Attendance Management
- Backup and Recovery
- Future Growth

The objective was to move away from unmanaged workstation administration and establish a scalable and maintainable infrastructure platform.

---

# Infrastructure Scope

The project included deployment and configuration of:

## Server Infrastructure

- Windows Server 2025
- Active Directory Domain Services
- DNS Services
- File Services
- Print Services
- Windows Server Backup

## Network Infrastructure

- TP-Link ER605 Router
- TP-Link SG2218P Managed Switch
- TP-Link EAP620 HD Access Points
- VLAN Segmentation
- Guest Network Isolation

## Attendance Management

- ZKTeco BioTime
- ZKTeco MB5000
- Fingerprint Authentication
- Facial Recognition
- Real-Time Synchronization

---

# Infrastructure Design

## Centralized Authentication

Active Directory was implemented to provide:

- User Authentication
- Computer Authentication
- Group Policy Management
- Security Administration

Benefits achieved:

- Centralized User Management
- Consistent Security Policies
- Simplified Administration

---

## Centralized File Services

A centralized file server was implemented to provide:

- Department-Based Storage
- Shared Resources
- Secure Access Control
- Data Protection

Benefits achieved:

- Improved Collaboration
- Reduced Data Duplication
- Easier Administration

---

## Network Segmentation

The network was segmented into dedicated VLANs.

### VLAN 10

Corporate Network

Used for:

- Workstations
- Servers
- Printers
- Attendance Devices
- Infrastructure Components

### VLAN 20

Guest Network

Used for:

- Mobile Devices
- Visitors
- Personal Equipment

Benefits achieved:

- Improved Security
- Reduced Attack Surface
- Better Resource Isolation

---

# Security Design

The environment follows a layered security model.

Implemented controls include:

- Active Directory Authentication
- Security Groups
- NTFS Permissions
- VLAN Segmentation
- Guest Network Isolation
- Windows Defender
- Centralized Administration
- Backup Protection

Future controls include:

- Windows LAPS
- Software Restriction Policies
- USB Device Control
- Security Auditing

---

# Data Protection Strategy

A multi-layer protection model was implemented.

## Layer 1

RAID 1 Storage Protection

## Layer 2

Shadow Copies

## Layer 3

Windows Server Backup

## Layer 4

Bare Metal Recovery

Benefits achieved:

- Reduced Downtime
- Improved Recovery Capability
- Business Continuity

---

# Attendance Management Design

The attendance platform was designed to align with business requirements.

## Attendance Model

Flexible Working Hours

### Configuration

- Friday and Saturday Weekends
- 8 Hour Daily Requirement
- First and Last Pairing Rule
- Monthly Evaluation
- Overtime Disabled

Benefits achieved:

- Flexible Employee Scheduling
- Simplified Attendance Management
- Accurate Reporting

---

# Technical Challenges

During deployment, several challenges were encountered and resolved.

## Printer Driver Deployment

Challenge:

Incorrect printer drivers remained deployed through Group Policy.

Resolution:

- Driver Cleanup
- Policy Review
- Printer Redeployment

Outcome:

Consistent printer deployment across workstations.

---

## Backup Configuration

Challenge:

Backup failures occurred due to system volume and recovery partition requirements.

Resolution:

- Log Analysis
- Volume Validation
- Backup Configuration Review
- Recovery Testing

Outcome:

Reliable full server backup and recovery capability.

---

## Attendance Policy Development

Challenge:

The business required a flexible attendance model rather than a traditional fixed schedule.

Resolution:

- Shift Design
- Attendance Rule Configuration
- Department Assignment
- Testing and Validation

Outcome:

Successful implementation of a flexible attendance system.

---

# Lessons Learned

## Infrastructure Design

- Planning reduces implementation complexity.
- Standardization improves long-term maintainability.
- Documentation is critical for support and recovery.

## Security

- Security should be incorporated during design, not after deployment.
- Group-based permissions scale better than user-based permissions.
- Network segmentation significantly improves security posture.

## Operations

- Backup validation is as important as backup creation.
- Monitoring reduces operational risk.
- Change management improves stability.

---

# Project Results

The project successfully delivered:

- Centralized Authentication
- Centralized Administration
- Centralized File Storage
- Automated Printer Deployment
- Biometric Attendance Management
- Backup and Recovery Protection
- VLAN-Based Network Segmentation
- Department-Based Access Control

The infrastructure is operational and supports daily business activities while providing a foundation for future growth.

---

# Future Roadmap

## Infrastructure

- Monitoring and Alerting
- UPS Monitoring Integration
- VPN Services

## Security

- Windows LAPS
- Software Restriction Policies
- USB Control
- Security Auditing

## Operations

- Automated Reporting
- Backup Monitoring
- Attendance Analytics

---

# Technologies Used

- Windows Server 2025
- Active Directory
- DNS
- Group Policy
- NTFS Permissions
- Windows Server Backup
- Shadow Copies
- RAID 1
- Omada SDN
- VLAN Segmentation
- Canon Print Services
- ZKTeco BioTime
- ZKTeco MB5000

---

# About This Project

This project represents a real-world infrastructure deployment designed, implemented, documented, and administered as part of a production engineering office environment.

The project demonstrates practical experience in:

- Systems Administration
- Infrastructure Deployment
- Network Administration
- Security Implementation
- Backup and Disaster Recovery
- Technical Troubleshooting
- Documentation and Operational Planning

---

# Author

Mohammed Younis

Senior IT Systems Administrator | Infrastructure & Network Architect | Windows Server & Active Directory | Expanding into AWS & Azure Cloud
