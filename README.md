# Windows Server Configuration Enterprise Lab

## Overview

This project demonstrates the design and implementation of a **secure enterprise Windows Server environment** using Active Directory, Group Policy, DNS, and file services.

It represents a production-like setup for a fictional company, focusing on structure, security, and best practices.

---

## Key Features

- Active Directory Domain: `corp.local`
- Windows Server 2022 Domain Controller
- Structured OU design (Lund & Stockholm)
- Delegated administration using security groups
- Group Policy configuration (user & computer)
- DNS with forwarders and conditional forwarding
- Centralized file server with NTFS & share permissions
- Printer deployment via GPO
- PowerShell automation for user creation
- AGDLP-based access control model

---

## Environment Summary

- **Domain Controller**: DC1
- **File Server**: FS1
- **Static IP setup (No DHCP)**
- Designed for scalability and future redundancy

---

## Architecture

- Two locations:
  - Lund
  - Stockholm
- Separation of:
  - Users
  - Computers
  - Groups
- Access is controlled strictly through groups (no direct user permissions)

---

## Security Design

- Role-Based Access Control (RBAC)
- Fine-grained password policies for administrators
- No cross-department write access
- Restricted user environment (Stockholm)
- Centralized and controlled data storage

---

## Automation

- Bulk user creation via PowerShell
- Automatic group assignment based on department and location

---

## Lab Goals

- Build a structured Active Directory environment
- Implement delegation and OU design
- Apply Group Policies for security and usability
- Configure secure file services
- Follow enterprise-level best practices

---

## Demo Video

https://youtu.be/BpLBVum34lA
