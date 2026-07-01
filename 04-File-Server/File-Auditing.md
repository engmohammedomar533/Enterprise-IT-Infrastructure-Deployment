# Enterprise File Auditing Configuration

## Overview

To improve accountability and security within the engineering office, Windows File Auditing was implemented on the production file server.

This configuration provides a complete audit trail for file operations performed by domain users on shared folders.

---

## Objectives

The implementation allows administrators to identify:

- File creation
- File modification
- File deletion
- File rename
- File move
- Permission changes
- Ownership changes

Each audit event records:

- User Account
- Computer Name
- File Path
- Operation Performed
- Date & Time
- Process Name

---

# Environment

| Component | Value |
|-----------|-------|
| Domain | tanta.local |
| Server | TANTA-DC01 |
| Operating System | Windows Server 2025 |
| Server Roles | Active Directory, DNS, File Server |
| File System | NTFS |

---

# Group Policy Configuration

A dedicated Group Policy Object was created.

## GPO Name

```
File Server Auditing
```

Linked to:

```
Domain Controllers
```

---

# Advanced Audit Policy

Navigate to:

```
Computer Configuration
    Policies
        Windows Settings
            Security Settings
                Advanced Audit Policy Configuration
                    Audit Policies
                        Object Access
                            Audit File System
```

Configuration:

- Success
- Failure

---

# Verification

Execute:

```powershell
auditpol /get /subcategory:"File System"
```

Expected Result

```
Object Access

File System      Success and Failure
```

---

# NTFS Auditing Configuration

Location

```
Properties
    Security
        Advanced
            Auditing
```

Principal

```
Everyone
```

Type

```
Success
```

Applies To

```
This folder, subfolders and files
```

---

# Audited Operations

Enabled

- Create files / Write data
- Create folders / Append data
- Write attributes
- Write extended attributes
- Delete
- Delete subfolders and files
- Change permissions
- Take ownership

Excluded

- Read Data
- Read Attributes
- Read Extended Attributes
- Read Permissions
- List Folder Contents

Read operations were intentionally excluded to prevent excessive Security Event Log generation.

---

# Security Event Log

Audit events are stored in:

```
Event Viewer
    Windows Logs
        Security
```

Useful Event IDs

| Event ID | Description |
|----------|-------------|
| 4656 | Handle requested |
| 4663 | File accessed or modified |
| 4660 | Object deleted |
| 4659 | Handle closed |

Recommended Filter

```
4663,4656,4660,4659
```

---

# Investigation Workflow

When a user reports a missing or modified file:

1. Open Event Viewer
2. Navigate to Windows Logs → Security
3. Filter using the required Event IDs
4. Search for the file name
5. Review:
   - Account Name
   - Object Name
   - Process Name
   - Access Type
   - Timestamp

---

# Result

The file server now provides centralized auditing for all critical file operations performed by domain users.

This configuration significantly improves:

- Security
- Accountability
- Troubleshooting
- Incident Investigation
- Compliance
