# Enterprise IT Infrastructure Deployment
## Project Documentation and Executive Summary

---

# Project Overview

This project documents the design, deployment, configuration, administration, and documentation of a complete enterprise IT infrastructure for a multi-department engineering office.

The environment was designed to provide centralized authentication, secure file management, printer deployment, network segmentation, attendance automation, backup and disaster recovery, and operational scalability.

The project demonstrates practical experience in:

- Infrastructure Design
- Systems Administration
- Active Directory Administration
- Network Administration
- Security Implementation
- Backup and Disaster Recovery
- Technical Troubleshooting
- Business System Integration
- Documentation and Operational Planning

---

# Project Scope

The project included deployment and configuration of:

## Server Infrastructure

- Windows Server 2025
- Active Directory Domain Services
- DNS Services
- File Services
- Print Services
- Windows Server Backup

---

## Network Infrastructure

- TP-Link ER605 Router
- TP-Link SG2218P Managed Switch
- 3 × TP-Link EAP620 HD Access Points
- VLAN Segmentation
- Guest Network Isolation
- Omada SDN Management

---

## Power Protection Infrastructure

- APC Easy UPS On-Line SRVS 3000VA
- Schneider Electric Double Conversion Technology
- Critical Infrastructure Protection
- Business Continuity Support

Protected Systems:

- Windows Server
- Network Switch
- Router
- BioTime Attendance System
- Core Network Services

---

## Attendance Infrastructure

- ZKTeco BioTime
- ZKTeco MB5000
- Fingerprint Authentication
- Facial Recognition
- Real-Time Synchronization

---

# Business Requirements

The organization required a centralized infrastructure capable of supporting:

- 21 Domain Workstations
- Engineering Departments
- Human Resources
- Management Team
- Centralized Authentication
- Centralized File Storage
- Attendance Management
- Printer Management
- Backup and Recovery
- Secure Department Collaboration
- Future Growth

---

# Infrastructure Architecture

## Active Directory

Active Directory was implemented as the central identity platform.

Responsibilities:

- User Authentication
- Computer Authentication
- Group Policy Management
- Security Group Administration
- Resource Access Management

Benefits:

- Centralized Administration
- Consistent Security Controls
- Simplified User Management

---

## File Services

Centralized file storage was implemented using Windows Server.

Shared Resources:

- InProgress
- Final
- Managerial
- Scans
- OsosDocs

Features:

- Department-Based Permissions
- NTFS Security
- Security Group Access
- Shadow Copies
- Centralized Backup

Benefits:

- Improved Collaboration
- Improved Security
- Simplified Management

---

## Print Services

Centralized print services were deployed using:

- Canon imageRUNNER 4056i
- Windows Print Services
- Group Policy Deployment

Benefits:

- Automated Printer Installation
- Centralized Driver Management
- Simplified Support

---

# Network Design

## VLAN 10 - Corporate Network

Used For:

- Domain Workstations
- Windows Server
- Printers
- Attendance Systems
- Infrastructure Devices

---

## VLAN 20 - Guest Network

Used For:

- Mobile Devices
- Visitors
- Guest Wi-Fi
- Personal Devices

---

## Security Controls

Implemented:

- Inter-VLAN Isolation
- Guest Network Isolation
- Centralized Management
- Controlled Resource Access

Benefits:

- Reduced Attack Surface
- Improved Security
- Better Network Segmentation

---

# Security Architecture

Implemented Controls:

- Active Directory Authentication
- Security Groups
- NTFS Permissions
- VLAN Segmentation
- Windows Defender
- Administrative Access Control
- Backup Protection
- Attendance System Access Control

Planned Controls:

- Windows LAPS
- Software Restriction Policies
- USB Control
- Security Auditing
- Application Whitelisting

---

# Power Protection Strategy

Power protection was implemented using:

## APC Easy UPS On-Line SRVS 3000VA

Benefits:

- Zero Transfer Time
- Voltage Regulation
- Surge Protection
- Brownout Protection
- Equipment Protection
- Improved Service Availability

Protected Systems:

- Server Infrastructure
- Network Infrastructure
- Attendance Systems

Business Impact:

- Reduced Downtime
- Improved Reliability
- Reduced Corruption Risk

---

# Data Protection Strategy

The environment utilizes a multi-layer disaster recovery model.

## Layer 0

Power Protection

- APC Easy UPS On-Line SRVS 3000VA

---

## Layer 1

Storage Protection

- RAID 1 Mirroring
- 2 × 8TB Enterprise Drives

---

## Layer 2

Shadow Copies

Purpose:

- Previous Version Recovery
- Accidental Deletion Recovery
- Rapid File Restoration

---

## Layer 3

Windows Server Backup

Protected Components:

- Operating System
- Active Directory
- DNS
- File Services
- Print Services
- System State

---

## Layer 4

Bare Metal Recovery

Recovery Scope:

- Complete Server Recovery
- Active Directory Recovery
- File Server Recovery
- DNS Recovery
- Infrastructure Recovery

---

# Attendance Management Design

## Platform

- BioTime
- MB5000

---

## Authentication Methods

- Fingerprint
- Facial Recognition

---

## Attendance Model

Flexible Working Hours

Configuration:

- Friday and Saturday Weekend
- 8 Hour Daily Requirement
- First and Last Pairing Rule
- Monthly Attendance Evaluation
- Overtime Disabled

Benefits:

- Flexible Scheduling
- Simplified Administration
- Accurate Reporting

---

# Technical Challenges

## Printer Driver Deployment

Challenge:

Incorrect Canon printer drivers remained deployed through Group Policy.

Resolution:

- Driver Cleanup
- Deployment Review
- Printer Redeployment

Outcome:

Consistent deployment across all workstations.

---

## Backup Configuration

Challenge:

Backup failures related to system partitions and recovery volumes.

Resolution:

- Log Analysis
- Volume Verification
- Backup Configuration Review
- Recovery Validation

Outcome:

Reliable backup and recovery capability established.

---

## Attendance System Design

Challenge:

Business requirements required flexible attendance rather than traditional fixed schedules.

Resolution:

- Shift Design
- Attendance Rule Development
- Department Assignment
- Validation Testing

Outcome:

Flexible attendance successfully implemented.

---

# Lessons Learned

## Infrastructure

- Proper planning reduces deployment complexity.
- Documentation improves long-term maintainability.
- Standardization simplifies administration.

## Security

- Security should be integrated from the beginning.
- Group-based permissions scale better than user-based permissions.
- Network segmentation significantly improves security posture.

## Operations

- Backup validation is as important as backup creation.
- Monitoring improves operational reliability.
- Controlled change management reduces risk.

---

# Current Status

Production Environment Operational

Completed:

- Active Directory
- DNS
- File Services
- Print Services
- Group Policy
- Omada SDN
- VLAN Segmentation
- RAID Storage
- Shadow Copies
- Windows Server Backup
- Bare Metal Recovery
- BioTime Deployment
- MB5000 Integration
- Department Structure
- Attendance Policies
- Power Protection Infrastructure

Planned:

- Windows LAPS
- Software Restriction Policies
- USB Device Controls
- Security Auditing
- Monitoring and Alerting

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
- ER605
- SG2218P
- EAP620 HD
- Canon imageRUNNER 4056i
- ZKTeco BioTime
- ZKTeco MB5000
- APC Easy UPS On-Line SRVS 3000VA

---

# Project Outcome

The project successfully delivered a production-ready enterprise infrastructure supporting 21 workstations across multiple departments.

The environment provides:

- Centralized Authentication
- Centralized Administration
- Secure File Storage
- Automated Printer Deployment
- Attendance Automation
- Network Segmentation
- Disaster Recovery Protection
- Power Protection
- Scalable Infrastructure Design

The solution provides a solid operational foundation while maintaining a roadmap for future security and operational enhancements.

---

# Author

Mohammed Younis

Senior IT Systems Administrator | Infrastructure & Network Architect | Windows Server & Active Directory | Expanding into AWS & Azure Cloud
