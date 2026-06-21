# File Server Infrastructure

## Overview

A centralized file server was deployed using Windows Server 2025 to provide secure storage, department-based access control, document management, and centralized file sharing for all company departments.

The file server serves as the primary location for engineering documents, administrative files, project data, and scanned documents.

---

# Objectives

- Centralized file storage
- Department-based access control
- Secure document management
- Simplified backup procedures
- Improved collaboration
- Data protection and recovery

---

# Storage Architecture

## Production Storage

### Configuration

- RAID 1 Mirror
- 2 × 8TB Enterprise Drives
- Dynamic Disk Mirroring

### Benefits

- Disk redundancy
- Improved fault tolerance
- Simplified recovery from disk failure
- Continuous availability

---

# Shared Folder Structure

## InProgress

### Purpose

Used for active project work and collaboration.

### Access

- Employees: Modify
- Department Managers: Modify
- IT Administrators: Full Control

### Usage

- Current projects
- Working drawings
- Active documentation

---

## Final

### Purpose

Stores completed and approved project files.

### Access

- Employees: Read Only
- Managers: Full Control
- IT Administrators: Full Control

### Usage

- Approved project files
- Final drawings
- Archived deliverables

### Benefits

- Prevents accidental modifications
- Protects finalized work

---

## Managerial

### Purpose

Stores management and executive documents.

### Access

- Management Group
- IT Administrators

### Security

Restricted from standard employees.

---

## Scans

### Purpose

Stores scanned documents from network scanners and multifunction devices.

### Access

- Authorized Employees
- Management
- IT Administrators

### Usage

- Contracts
- Administrative Documents
- Client Documentation

---

## OsosDocs

### Purpose

Private management document repository.

### Access

- General Manager
- Authorized Management Personnel
- IT Administrators

### Security

Hidden from standard users.

### Usage

- Executive Documentation
- Confidential Records
- Management Files

---

# Permission Model

## Access Control Strategy

Access is granted through Active Directory Security Groups rather than individual user permissions.

### Benefits

- Simplified administration
- Easier auditing
- Consistent permissions
- Improved scalability

---

# NTFS Permissions

## Design Principles

- Least Privilege
- Group-Based Access
- Centralized Management
- Department Isolation

### Permission Levels

- Full Control
- Modify
- Read & Execute
- Read Only

---

# Drive Mapping Integration

Mapped drives are automatically deployed through Group Policy.

### Mapped Resources

- InProgress
- Final
- Managerial
- Scans
- OsosDocs

### Benefits

- Consistent user experience
- Simplified access
- Reduced support requests

---

# Data Protection

## Shadow Copies

### Status

Implemented

### Purpose

Allow users to restore previous versions of files without administrator assistance.

### Benefits

- Accidental file recovery
- Version recovery
- Reduced support workload

---

## Backup Integration

The file server is included in the centralized backup strategy.

Protected Components:

- Shared Folders
- NTFS Permissions
- File Structure
- System State

---

# File Server Security

## Access Restrictions

- Department-based permissions
- Restricted management shares
- Centralized authentication
- Active Directory integration

## Administrative Access

Administrative access is limited to:

- Domain Administrators
- Authorized IT Personnel

---

# Capacity Planning

### Current Storage

- Approximately 7TB usable mirrored storage

### Design Considerations

- Engineering drawings
- CAD files
- Project documentation
- Long-term document retention

---

# Operational Benefits

- Centralized file management
- Simplified collaboration
- Improved security
- Easier backup management
- Faster document recovery
- Reduced data duplication

---

# Lessons Learned

- Group-based permissions scale better than individual permissions.
- Shadow Copies significantly reduce support requests.
- Separating InProgress and Final repositories improves document control.
- Dedicated management shares improve confidentiality.
- RAID is not a backup and must be combined with external backups.

---

# Technologies Used

- Windows Server 2025
- NTFS Permissions
- Active Directory
- Security Groups
- Group Policy
- RAID 1
- Shadow Copies
- Windows Server Backup
