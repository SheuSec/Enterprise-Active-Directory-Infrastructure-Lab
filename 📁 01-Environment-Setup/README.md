# Enterprise Active Directory Infrastructure Lab

## Introduction

This project documents the planning, deployment, configuration, and validation of a Windows-based enterprise network built using Microsoft Hyper-V. The objective was to design and implement a secure, fully functional Active Directory environment that reflects the core infrastructure commonly found in modern organizations.

The deployment began with the creation of an isolated virtual network, followed by the installation and configuration of Windows Server 2022 as the Domain Controller. Core enterprise services—including Active Directory Domain Services (AD DS), Domain Name System (DNS), and Dynamic Host Configuration Protocol (DHCP)—were implemented to provide centralized authentication, name resolution, and automated network configuration.

To simulate a real-world enterprise environment, Organizational Units (OUs), domain users, security groups, and shared folders were created. NTFS and Share Permissions were configured to control access to network resources, while Group Policy Objects (GPOs) were used to enforce enterprise security settings such as password policies, account lockout policies, and interactive logon messages.

The environment was validated by joining a Windows 10 client to the domain, verifying authentication and network services, testing access to shared resources, and performing internal reconnaissance with Kali Linux to confirm the availability of essential enterprise services.

This project strengthened my practical skills in Windows Server Administration, Active Directory, enterprise networking, Group Policy, virtualization, and infrastructure validation while demonstrating how these technologies integrate to build a secure and manageable enterprise environment.

---

# Project Overview

The goal of this project was to build a complete enterprise Active Directory environment from the ground up while gaining hands-on experience with the technologies that power modern Windows networks.

Rather than focusing solely on installing Windows Server, this project followed the complete deployment lifecycle—from designing the virtual infrastructure and configuring core network services to securing the environment and validating the final implementation.

The lab was built using Microsoft Hyper-V and consisted of three virtual machines:

- **Windows Server 2022** – Domain Controller (DC01)
- **Windows 10 Enterprise** – Domain-joined client
- **Kali Linux** – Internal security validation and network testing

Throughout the deployment, enterprise services including Active Directory, DNS, DHCP, Group Policy, file sharing, and user management were configured and tested individually before being integrated into the complete infrastructure.

The completed environment demonstrates how centralized authentication, automated network configuration, secure resource sharing, and policy-based administration work together to support a functional enterprise network.

---

# Project Objectives

The primary objectives of this project were to:

- Design and build a secure enterprise network using Microsoft Hyper-V.
- Create an isolated lab using an Internal Virtual Switch.
- Configure Network Address Translation (NAT) for controlled internet access.
- Deploy Windows Server 2022 as the Domain Controller.
- Install and configure Active Directory Domain Services (AD DS).
- Configure DNS for domain name resolution.
- Deploy and configure DHCP for automatic IP address allocation.
- Create Organizational Units (OUs) for departmental administration.
- Create and manage domain users and security groups.
- Configure shared folders using NTFS and Share Permissions.
- Implement Group Policy Objects (GPOs) to enforce enterprise security policies.
- Join a Windows 10 client to the Active Directory domain.
- Validate authentication, network connectivity, and resource access.
- Perform basic internal security validation using Kali Linux.
- Document the deployment process in a structured and professional manner.

---

# Technologies and Tools

| Technology | Purpose |
|------------|---------|
| Microsoft Hyper-V | Virtualization platform |
| Windows Server 2022 | Domain Controller |
| Windows 10 Enterprise | Domain client |
| Kali Linux | Internal security validation |
| Active Directory Domain Services (AD DS) | Identity and authentication |
| DNS | Name resolution |
| DHCP | Automatic IP address allocation |
| Group Policy Management | Centralized policy enforcement |
| Active Directory Users and Computers | User and group management |
| File and Storage Services | Shared folder management |
| Command Prompt | Administration and troubleshooting |
| Nmap | Network validation |
| Event Viewer | Monitoring and log analysis |

---

# Lab Environment

The entire infrastructure was deployed within Microsoft Hyper-V to simulate a real-world enterprise environment while remaining isolated from the production network.

| Component | Configuration |
|-----------|---------------|
| Hypervisor | Microsoft Hyper-V |
| Domain Name | olalab.local |
| Domain Controller | DC01 |
| Server Operating System | Windows Server 2022 |
| Client Operating System | Windows 10 Enterprise |
| Security Testing Machine | Kali Linux |
| Network Type | Hyper-V Internal Virtual Switch |
| Internet Access | Network Address Translation (NAT) |
| Core Services | Active Directory, DNS, DHCP, Group Policy |

This configuration closely mirrors a small enterprise environment where centralized identity management, automated network services, and security controls are deployed before client systems are introduced into the domain.
