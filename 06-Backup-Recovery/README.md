# Backup and Disaster Recovery

## Overview

A multi-layered backup and disaster recovery strategy was designed and implemented to protect business-critical systems, engineering documents, Active Directory services, and company data.

The objective was to minimize downtime, reduce data loss risk, and provide multiple recovery options for different failure scenarios.

---

# Objectives

- Protect critical business data
- Reduce downtime
- Minimize data loss
- Support rapid recovery
- Protect Active Directory
- Protect engineering documentation
- Provide multiple recovery methods

---

# Disaster Recovery Strategy

The environment utilizes a layered recovery model.

## Layer 1 - RAID 1 Storage Protection

### Configuration

- 2 × 8TB Enterprise Drives
- Windows Dynamic Disk Mirroring
- RAID 1

### Purpose

Protect against:

- Single disk failure
- Hardware storage failure

### Benefits

- High availability
- Immediate redundancy
- No interruption during single disk failure

### Important Note

RAID is not a backup solution.

RAID protects availability but does not protect against:

- Accidental deletion
- Malware
- Ransomware
- Data corruption

---

## Layer 2 - Shadow Copies

### Status

Implemented

### Purpose

Provide rapid file-level recovery.

### Use Cases

- Accidental file deletion
- File overwrite recovery
- Previous version restoration

### Benefits

- Self-service recovery
- Reduced IT support requests
- Fast restoration process

---

## Layer 3 - Windows Server Backup

### Status

Implemented

### Backup Platform

Windows Server Backup

### Backup Scope

Protected Components:

- EFI Partition
- System Partition
- Data Volume
- Active Directory
- DNS
- System State
- Bare Metal Recovery

### Backup Destination

Dedicated External Backup Storage

### Benefits

- Full system recovery
- Operating system recovery
- Active Directory recovery
- Server rebuild capability

---

## Layer 4 - Bare Metal Recovery

### Purpose

Recover entire server infrastructure following catastrophic failure.

### Recovery Scope

- Windows Server
- Active Directory
- DNS
- File Shares
- NTFS Permissions
- Group Policies
- Server Configuration

### Recovery Method

Windows Server Recovery Environment

---

# Backup Architecture

## Protected Services

### Active Directory

Protected Through:

- System State Backup
- Bare Metal Backup

### DNS

Protected Through:

- System State Backup
- Full Server Backup

### File Services

Protected Through:

- Volume Backup
- Shadow Copies

### Print Services

Protected Through:

- Full Server Backup

### Group Policy

Protected Through:

- System State Backup

---

# Recovery Scenarios

## Scenario 1 - Accidental File Deletion

### Recovery Method

Shadow Copies

### Estimated Recovery Time

Less than 5 minutes

---

## Scenario 2 - Corrupted File

### Recovery Method

Previous Versions

### Estimated Recovery Time

Less than 5 minutes

---

## Scenario 3 - Single Disk Failure

### Recovery Method

RAID 1 Mirror

### Estimated Recovery Time

Immediate

---

## Scenario 4 - Server Failure

### Recovery Method

Windows Server Backup Restore

### Estimated Recovery Time

Several Hours

---

## Scenario 5 - Complete Server Loss

### Recovery Method

Bare Metal Recovery

### Estimated Recovery Time

Same Day Recovery

---

# Backup Validation

## Verification Process

Backups should be reviewed regularly to confirm:

- Successful completion
- Storage availability
- Backup integrity
- Recovery readiness

### Recommended Validation

- Daily Backup Review
- Weekly Backup Verification
- Monthly Restore Testing

---

# Operational Procedures

## Daily Tasks

- Verify backup completion
- Review backup logs
- Confirm storage availability

## Weekly Tasks

- Review backup history
- Validate backup capacity
- Review Windows Event Logs

## Monthly Tasks

- Perform test restore
- Validate recovery procedures
- Review disaster recovery documentation

---

# Lessons Learned

- RAID does not replace backups.
- Multiple recovery layers provide significantly better protection.
- Shadow Copies greatly reduce recovery effort for common user mistakes.
- Active Directory protection is critical in domain environments.
- Backup verification is as important as backup creation.

---

# Future Enhancements

## Planned

- Backup Failure Email Alerts
- UPS Integration and Automated Shutdown
- Backup Monitoring Dashboard
- Offsite Backup Replication
- Cloud Backup Integration

---

# Technologies Used

- Windows Server 2025
- Windows Server Backup
- System State Backup
- Bare Metal Recovery
- RAID 1
- Dynamic Disks
- Shadow Copies
- NTFS File System
