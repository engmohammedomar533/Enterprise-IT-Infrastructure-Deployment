# Lessons Learned

## Overview

This document captures the key technical challenges, decisions, troubleshooting activities, and operational lessons learned throughout the design and deployment of the Enterprise IT Infrastructure project.

The goal is to document not only what was implemented, but also the reasoning, challenges, and practical experience gained during deployment.

---

# Lesson 1 - Infrastructure Planning Matters

## Challenge

The project required deployment of multiple interconnected services:

- Active Directory
- DNS
- File Services
- Print Services
- Attendance Management
- Backup Systems
- Network Infrastructure

Without proper planning, dependencies between systems can create deployment complexity and operational issues.

## Solution

A phased deployment approach was used:

1. Network Infrastructure
2. Active Directory
3. File Services
4. Print Services
5. Backup Systems
6. Attendance Management
7. Security Controls

## Lesson Learned

Well-structured planning significantly reduces implementation complexity and future support requirements.

---

# Lesson 2 - Group-Based Permissions Scale Better

## Challenge

Managing permissions directly on individual users becomes difficult as organizations grow.

## Solution

Access control was implemented through Active Directory Security Groups.

Model:

User
→ Security Group
→ Resource

Examples:

- Employees → InProgress
- Managers → Managerial
- Management → OsosDocs

## Lesson Learned

Group-based access control is easier to maintain, audit, and expand than user-based permissions.

---

# Lesson 3 - Printer Deployments Can Persist Unexpectedly

## Challenge

An incorrect Canon printer driver remained deployed across workstations even after printer cleanup.

## Symptoms

- Multiple Canon drivers appeared on workstations.
- Incorrect printer deployment remained active.
- Deployment inconsistencies occurred.

## Investigation

Activities performed:

- Reviewed printer deployments.
- Reviewed Group Policy assignments.
- Reviewed Print Management.
- Verified deployed printers.
- Removed legacy printer references.

## Resolution

- Removed incorrect deployment.
- Removed obsolete drivers.
- Redeployed approved Canon driver package.
- Verified successful deployment.

## Lesson Learned

Printer deployments and drivers can persist in multiple locations. Validation should always be performed after deployment changes.

---

# Lesson 4 - Backup Configuration Requires Validation

## Challenge

Windows Server Backup initially reported failures related to system volumes and recovery partitions.

## Investigation

Activities performed:

- Reviewed backup logs.
- Reviewed Windows Event Viewer.
- Verified protected volumes.
- Validated backup configuration.

## Resolution

- Corrected backup scope.
- Verified system volume protection.
- Confirmed Bare Metal Recovery support.
- Successfully completed backup jobs.

## Lesson Learned

Successful backup creation is not enough. Backup validation and recovery planning are equally important.

---

# Lesson 5 - RAID Is Not A Backup

## Observation

RAID 1 provides redundancy but does not protect against:

- Accidental deletion
- Malware
- Ransomware
- Corruption

## Solution

Additional protection layers were implemented:

- Shadow Copies
- Windows Server Backup
- Bare Metal Recovery

## Lesson Learned

Availability and backup are different objectives and both are required.

---

# Lesson 6 - Power Protection Is Part Of Disaster Recovery

## Challenge

A server can be fully protected by backups yet still suffer downtime due to unstable power.

## Solution

Implemented:

- APC Easy UPS On-Line SRVS 3000VA

Benefits:

- Zero Transfer Time
- Voltage Regulation
- Surge Protection
- Improved Reliability

## Lesson Learned

Business continuity begins with preventing outages before recovery becomes necessary.

---

# Lesson 7 - Network Segmentation Improves Security

## Challenge

Guest devices should not have access to corporate resources.

## Solution

Implemented:

### VLAN 10

Corporate Network

### VLAN 20

Guest Network

Additional Controls:

- Inter-VLAN Isolation
- Guest Network Restrictions

## Lesson Learned

Network segmentation is one of the most effective security controls available in small and medium business environments.

---

# Lesson 8 - Attendance Systems Must Follow Business Requirements

## Challenge

Management required flexible attendance rather than fixed shift scheduling.

Requirements:

- Flexible Arrival Time
- Flexible Departure Time
- Monthly Evaluation
- Friday and Saturday Off

## Solution

Implemented:

- Flexible Shift
- First and Last Pairing
- 8 Hour Daily Requirement
- Department-Based Assignment

## Lesson Learned

Technology should adapt to business requirements rather than forcing business processes to adapt to technology.

---

# Lesson 9 - Biometric Redundancy Improves Reliability

## Challenge

Employees may occasionally experience fingerprint recognition issues.

## Solution

Each employee receives:

- Left Index Finger
- Right Index Finger
- Facial Recognition

## Lesson Learned

Multiple authentication methods improve user experience and operational reliability.

---

# Lesson 10 - Documentation Is Critical

## Observation

Infrastructure becomes significantly easier to support when every major configuration is documented.

## Benefits

- Faster Troubleshooting
- Easier Knowledge Transfer
- Improved Disaster Recovery
- Reduced Dependency On Individuals

## Lesson Learned

Documentation should be created during deployment rather than after deployment.

---

# Lesson 11 - Security Hardening Should Be Phased

## Challenge

Engineering staff require specialized applications and tools.

Immediate lockdown policies could disrupt operations.

## Solution

Security roadmap created:

Phase 1

- Infrastructure Deployment

Phase 2

- Application Validation

Phase 3

- Software Restriction Policies
- LAPS
- USB Controls

## Lesson Learned

Security controls should be implemented in a structured and operationally aware manner.

---

# Key Takeaways

The most important lessons from this project were:

- Planning reduces complexity.
- Documentation is essential.
- Group-based permissions scale effectively.
- Validation is as important as deployment.
- Backup strategies require multiple layers.
- Security should be built into the design.
- Business requirements should drive technical decisions.
- Monitoring and validation reduce operational risk.

---

# Project Impact

The project successfully transformed a collection of standalone systems into a centralized, manageable, secure, and scalable infrastructure platform supporting:

- 21 Workstations
- Multiple Departments
- Centralized Authentication
- Centralized Storage
- Automated Printing
- Attendance Management
- Backup and Disaster Recovery
- Network Segmentation
- Power Protection
- Future Security Growth
