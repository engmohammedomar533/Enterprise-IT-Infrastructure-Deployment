# Backup and Disaster Recovery Architecture

```text
                     Business Continuity Model

┌─────────────────────────────────────────────────────────┐
│ Layer 0 - Power Protection                              │
│ APC Easy UPS On-Line SRVS 3000VA                        │
│                                                         │
│ Protects Against:                                       │
│ - Power Outages                                         │
│ - Brownouts                                             │
│ - Power Surges                                          │
│ - Voltage Fluctuations                                  │
└─────────────────────────────────────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────┐
│ Layer 1 - Storage Protection                            │
│ RAID 1 Mirroring                                        │
│                                                         │
│ 8TB Drive A  ◄──── Mirror ────►  8TB Drive B           │
│                                                         │
│ Protects Against:                                       │
│ - Single Disk Failure                                   │
└─────────────────────────────────────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────┐
│ Layer 2 - Shadow Copies                                 │
│                                                         │
│ Protects Against:                                       │
│ - Accidental Deletion                                   │
│ - File Overwrites                                       │
│ - Previous Version Recovery                             │
└─────────────────────────────────────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────┐
│ Layer 3 - Windows Server Backup                         │
│                                                         │
│ Protected Components:                                   │
│ - Operating System                                      │
│ - Active Directory                                      │
│ - DNS                                                   │
│ - File Services                                         │
│ - Print Services                                        │
│ - System State                                          │
└─────────────────────────────────────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────┐
│ Layer 4 - Bare Metal Recovery                           │
│                                                         │
│ Recovery Capabilities:                                  │
│ - Full Server Restore                                   │
│ - Active Directory Restore                              │
│ - DNS Restore                                           │
│ - Complete Infrastructure Recovery                      │
└─────────────────────────────────────────────────────────┘
```

## Recovery Strategy

The environment utilizes multiple recovery layers to minimize downtime and protect business-critical services.

### Layer 0 - Power Protection

APC Easy UPS On-Line SRVS 3000VA

Purpose:

- Prevent unexpected shutdowns
- Protect infrastructure
- Maintain service availability

---

### Layer 1 - RAID 1

Purpose:

- Protect against disk failure
- Maintain data availability

Important:

RAID is not a backup solution.

---

### Layer 2 - Shadow Copies

Purpose:

- Restore previous file versions
- Recover deleted files

Recovery Time:

Less than 5 minutes

---

### Layer 3 - Windows Server Backup

Purpose:

- Protect operating system
- Protect Active Directory
- Protect business data

Recovery Time:

Several hours

---

### Layer 4 - Bare Metal Recovery

Purpose:

- Recover complete server environment

Recovery Time:

Same-day infrastructure recovery

---

## Recovery Scenarios

### Accidental File Deletion

Recovery Method:

- Shadow Copies

---

### Corrupted File

Recovery Method:

- Previous Versions

---

### Single Disk Failure

Recovery Method:

- RAID 1 Mirror

---

### Operating System Failure

Recovery Method:

- Windows Server Backup

---

### Complete Server Failure

Recovery Method:

- Bare Metal Recovery

---

## Lessons Learned

- Backup validation is critical.
- RAID improves availability but does not replace backups.
- Multiple recovery layers provide stronger protection.
- UPS protection reduces the likelihood of recovery being required.
- Disaster recovery planning should begin before deployment.
```
