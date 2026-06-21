# Active Directory Infrastructure

## Overview

A centralized Active Directory environment was deployed using Windows Server 2025 to provide authentication, authorization, policy management, and resource access control for all company users and devices.

The Active Directory infrastructure serves as the foundation for centralized identity management and security across the organization.

---

## Objectives

- Centralized user authentication
- Centralized computer management
- Group Policy deployment
- Department-based access control
- Simplified administration
- Improved security and auditing

---

## Server Role

### Domain Controller

Primary Domain Controller:

- Windows Server 2025
- Active Directory Domain Services (AD DS)
- DNS Server
- File Server
- Print Server

---

## Organizational Unit Structure

The Active Directory structure was organized using Organizational Units (OUs) to simplify administration and Group Policy application.

### User OUs

- Management
- HR
- Architectural Engineering
- Structural Engineering
- Mechanical Engineering
- Electrical Engineering

### Computer OUs

- Workstations
- Servers

---

## User Management

User accounts were created for all employees and assigned to their respective departments.

Each user receives:

- Domain Account
- Department Membership
- Appropriate Share Permissions
- Printer Access
- Drive Mapping via Group Policy

---

## Security Groups

Department-based security groups were implemented to control access to shared resources.

### Examples

- Management Group
- HR Group
- Architectural Engineering Group
- Structural Engineering Group
- Mechanical Engineering Group
- Electrical Engineering Group

---

## Access Control Model

Access to company resources is granted through security groups rather than individual user permissions.

Benefits:

- Simplified administration
- Easier auditing
- Better scalability
- Reduced permission errors

---

## Authentication

All workstations authenticate directly against Active Directory.

Benefits:

- Single Sign-On (SSO)
- Centralized Password Management
- Account Lockout Policies
- Password Complexity Enforcement

---

## DNS Integration

Active Directory integrated DNS was deployed to provide:

- Name Resolution
- Service Location
- Domain Authentication Support

DNS is used by all domain-joined workstations and servers.

---

## Administrative Model

Administration is performed using dedicated administrative accounts.

Responsibilities include:

- User Management
- Computer Management
- Group Policy Administration
- File Permission Management
- Printer Administration

---

## Benefits Achieved

- Centralized Identity Management
- Simplified User Administration
- Improved Security
- Consistent Policy Enforcement
- Scalable Infrastructure Design
- Easier Resource Management

---

## Technologies Used

- Windows Server 2025
- Active Directory Domain Services
- DNS Server
- Group Policy Management
- NTFS Permissions
- Security Groups
