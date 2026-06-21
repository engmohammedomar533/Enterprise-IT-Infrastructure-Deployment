# Network Topology

```text
                    Internet
                        │
                        │
                Vodafone Router
                        │
                        │
                     ER605
                        │
                        │
                   SG2218P Switch
                        │
 ┌──────────────┬──────────────┬──────────────┬──────────────┐
 │              │              │              │              │
AP1           AP2            AP3        TANTA-DC01        DVR
 │              │              │              │
 │              │              │              ├── Canon 4056i
 │              │              │              ├── MB5000
 │              │              │              └── 21 Workstations
 │              │              │
 └──────── VLAN 10 Corporate Network ────────┘

                 VLAN 20 Guest Network
                 (Mobile Devices Only)
```

## Components

### Router

- TP-Link ER605

### Switch

- TP-Link SG2218P

### Access Points

- 3 × TP-Link EAP620 HD

### Server

- Windows Server 2025
- Active Directory
- DNS
- File Server
- Print Server
- BioTime

### Power Protection

- APC Easy UPS On-Line SRVS 3000VA

### Endpoints

- 21 Domain Workstations
- Canon imageRUNNER 4056i
- MB5000 Attendance Device
- DVR System

## VLAN Design

### VLAN 10

Corporate Network

### VLAN 20

Guest Network

### Security

- Inter-VLAN Isolation Enabled
- Guest Devices Cannot Access Corporate Resources
```
