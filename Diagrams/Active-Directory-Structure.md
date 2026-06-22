# Active Directory Structure

```text
company.local
│
├── Users
│   │
│   ├── Management
│   ├── Human Resources
│   ├── Architectural Engineering
│   ├── Structural Engineering
│   ├── Mechanical Engineering
│   └── Electrical Engineering
│
├── Computers
│   │
│   ├── Workstations
│   └── Servers
│
├── Groups
│   │
│   ├── GG_Employees
│   ├── GG_Managers
│   ├── GG_IT_Admins
│   ├── GG_Local_Admins
│   ├── GG_Managerial
│   └── GG_OsosDocs
│
└── Resources
    │
    ├── InProgress
    ├── Final
    ├── Managerial
    ├── Scans
    └── OsosDocs
```

## Overview

Active Directory was deployed as the centralized identity and access management platform.

### Functions

- User Authentication
- Computer Authentication
- Group Policy Management
- Resource Authorization
- Security Administration

---

## User Organization

Users are organized according to departmental structure.

### Departments

- Management
- Human Resources
- Architectural Engineering
- Structural Engineering
- Mechanical Engineering
- Electrical Engineering

Benefits:

- Easier Administration
- Simplified Delegation
- Department-Based Policy Assignment

---

## Computer Organization

### Workstations

- 21 Domain Joined Computers

### Servers

- Windows Server 2025

Benefits:

- Centralized Management
- Simplified Group Policy Deployment

---

## Security Groups

Access is assigned through security groups rather than individual user permissions.

Benefits:

- Simplified Administration
- Easier Auditing
- Improved Scalability

---

## Resource Access Model

Users receive access through:

User
→ Security Group
→ Resource

Example:

Employee
→ GG_Employees
→ InProgress

Manager
→ GG_Managers
→ Managerial

Management
→ GG_OsosDocs
→ OsosDocs

Benefits:

- Least Privilege
- Easier Permission Management
- Reduced Administrative Overhead
```
