# Windows Server Lab Instructions

## Objective

Set up a functional and secure **Active Directory domain environment** for a fictional company using **Windows Server** and **Windows 10/11 clients**.

## General Requirements

- Do **not** enable **DHCP** in the lab environment
- Use a **unique domain name**
- Join at least **one Windows 10/11 client** to the domain (**two recommended**)

## OU Structure

Create the following **top-level OUs**:

- **Location 1**
  - Users
  - Computers
  - Groups
- **Location 2**
  - Users
  - Computers
  - Groups
- **Resource Groups** *(optional)*
- **Servers**

## Users and Departments

Create users for these groups:

- Management
- Sales
- Consultants
- Finance
- IT Support *(1 per location)*

User accounts must be **bulk imported** using a method such as **PowerShell**.
Include the **import file** in the final documentation.

## Administration

- Each location must have separate administrators for:
  - **User accounts**
  - **Computer accounts**
- These administrators must be assigned through **groups**, not directly to user accounts
- The same administrators must have **local administrative rights** on client computers in their own location
- Only **administrators** may log in to **file servers**
- **Administrators** must have **stricter password requirements** than normal users
- No administrator accounts should have a restricted desktop environment

## Group Policy Requirements

Use **GPOs** to configure the environment.

Required:

- Create the settings defined in the case
- Add additional **relevant GPOs** suitable for a production-like environment
- Make a **clear difference** between the user environments of the two locations or departments
- One location must have a **more locked-down** desktop environment
- Apply a desktop background showing:
  - Administrator name
  - Phone number
  - Email address

## Printers

- Create **two printers**, one per location
- Deploy printers **automatically** to client computers in the correct OU

## Software Deployment

- Automate installation of at least **one application**
- Deploy it to **computer accounts** so it installs automatically at **startup**

## File Server and Permissions

Documents must be:

- Stored **centrally**
- Protected from **unauthorized access**
- Designed with **fault tolerance** in mind

Permission model:

- Use **groups** to assign access
- Combine groups across levels to grant folder access
- One group must have **Read/Write** access
- Another group must have **Read-only** access
- Share permissions must be set to **Full Control** for **Authenticated Users** or **Everyone**
- Document both:
  - **Share permissions**
  - **NTFS permissions**

In **Resource Groups**, only **groups** may exist as members, not users.

## Networking

- Configure **name resolution** to at least one other group in the class

## Final Goal

Create a secure, usable, and well-structured **Windows Server lab environment** with:

- **Active Directory**
- **OU design**
- **Delegated administration**
- **GPO management**
- **Printer deployment**
- **Software deployment**
- **Centralized file services**
- **Professional documentation**
