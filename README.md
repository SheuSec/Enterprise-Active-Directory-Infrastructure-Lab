# 🏢 Enterprise Active Directory Infrastructure Lab

### Building a Secure and Scalable Windows Server 2022 Enterprise Environment

<p align="center">
A hands-on enterprise infrastructure project that demonstrates the deployment, configuration, testing, and validation of a Windows Server 2022 Active Directory environment using Microsoft Hyper-V.
</p>

<p>

![Windows Server](https://img.shields.io/badge/Windows_Server_2022-0078D4?style=for-the-badge&logo=windows)
![Hyper-V](https://img.shields.io/badge/Hyper--V-Virtualization-0089D6?style=for-the-badge)
![Active Directory](https://img.shields.io/badge/Active_Directory-0066CC?style=for-the-badge)
![DNS](https://img.shields.io/badge/DNS-Configured-success?style=for-the-badge)
![DHCP](https://img.shields.io/badge/DHCP-Configured-success?style=for-the-badge)
![Group Policy](https://img.shields.io/badge/Group_Policy-Implemented-blue?style=for-the-badge)
![Windows 10](https://img.shields.io/badge/Windows_10-Domain_Joined-success?style=for-the-badge)
![Kali Linux](https://img.shields.io/badge/Kali_Linux-Security_Testing-purple?style=for-the-badge)

</p>

---

*"Enterprise infrastructure isn't built by installing server roles. It's built by connecting services, solving problems, validating configurations, and creating a foundation that users can rely on."*

</div>

---

# 📖 Overview

Modern organizations depend on centralized systems to manage users, computers, network services, and security policies efficiently. Rather than configuring every computer individually, enterprise environments rely on Windows Server technologies to simplify administration, improve consistency, and strengthen security.

This project documents the complete deployment of a Windows Server 2022 enterprise environment built entirely in Microsoft Hyper-V. Starting from an isolated virtual lab, the infrastructure was transformed into a fully operational Active Directory domain capable of managing user authentication, network services, device administration, and shared resources from a single centralized platform.

The deployment included the implementation of Active Directory Domain Services (AD DS), Domain Name System (DNS), Dynamic Host Configuration Protocol (DHCP), Group Policy Objects (GPOs), file sharing, Windows 10 domain integration, and internal network validation using Kali Linux.

Beyond configuring services, this project captures the planning, implementation, testing, troubleshooting, and validation process, providing a practical demonstration of enterprise Windows administration in a virtual environment.

---

# 🎯 Why This Project Was Built

The purpose of this lab was to simulate how enterprise Windows infrastructure is deployed and managed in a real organizational environment.

The project focuses on building practical experience with Microsoft's enterprise technologies while understanding how core services interact to provide centralized authentication, automated network configuration, policy enforcement, and secure resource management.

Instead of following isolated tutorials, every component was integrated into a single environment to demonstrate how enterprise systems operate together.

---

# ⭐ Key Highlights

- Complete enterprise deployment using Windows Server 2022
- Active Directory Domain Services (AD DS)
- Domain Name System (DNS)
- Dynamic Host Configuration Protocol (DHCP)
- Group Policy implementation
- Organizational Unit (OU) design
- User and Group Management
- Shared Folder Configuration
- Windows 10 Domain Integration
- Hyper-V Virtual Networking
- Internal Security Validation using Kali Linux
- Enterprise Troubleshooting and Validation
- Comprehensive Technical Documentation

---

# 📑 Contents

- Overview
- Enterprise Scenario
- Project Objectives
- Technologies Used
- Lab Environment
- Network Architecture
- Deployment Workflow
- Implementation
- Testing and Validation
- Challenges Encountered
- Lessons Learned
- Skills Demonstrated
- Project Documentation
- Repository Structure
- Future Improvements
- Author

---

# 🏢 Enterprise Scenario

Imagine an organization expanding its workforce from a few employees to multiple departments. As the number of users and computers grows, managing each device individually becomes inefficient, inconsistent, and difficult to secure. Employees require centralized authentication, reliable access to shared resources, automatic network configuration, and consistent security policies across the organization.

To address these requirements, an enterprise infrastructure was designed and deployed using Windows Server 2022 within a Microsoft Hyper-V virtual environment. The environment was built around Active Directory Domain Services (AD DS), providing centralized identity management and serving as the core of the organization's network.

Supporting services such as Domain Name System (DNS) and Dynamic Host Configuration Protocol (DHCP) were configured to automate name resolution and IP address allocation. Organizational Units (OUs), domain users, security groups, shared folders, and Group Policy Objects (GPOs) were implemented to simulate a structured enterprise environment.

To complete the deployment, a Windows 10 Enterprise client was joined to the domain to verify centralized administration, while Kali Linux was connected to the internal network to validate connectivity and assess the deployed services.

This lab represents a practical implementation of enterprise infrastructure principles in a controlled virtual environment.

---

# 🎯 Project Objectives

The primary objective of this project was to design, deploy, and validate a functional Windows Server 2022 enterprise infrastructure using Microsoft Hyper-V.

The specific objectives included:

- Design an isolated enterprise network using Hyper-V.
- Deploy Windows Server 2022 as the Domain Controller.
- Configure Active Directory Domain Services (AD DS).
- Implement Domain Name System (DNS).
- Configure Dynamic Host Configuration Protocol (DHCP).
- Create Organizational Units (OUs).
- Manage domain users and security groups.
- Configure shared folders and NTFS permissions.
- Implement Group Policy Objects (GPOs).
- Join a Windows 10 client to the domain.
- Validate communication between all virtual machines.
- Perform internal security validation using Kali Linux.
- Document the deployment and troubleshooting process.

---

# 🛠 Technologies Used

| Technology | Purpose |
|------------|---------|
| Microsoft Hyper-V | Virtualization platform used to host all virtual machines |
| Windows Server 2022 | Enterprise server operating system configured as the Domain Controller |
| Windows 10 Enterprise | Domain-joined client workstation |
| Kali Linux | Internal security validation and network testing |
| Active Directory Domain Services (AD DS) | Centralized identity and authentication |
| DNS | Internal name resolution |
| DHCP | Automatic IP address assignment |
| Group Policy Management | Centralized configuration and policy enforcement |
| Active Directory Users and Computers | User, group, and Organizational Unit management |
| File and Storage Services | Shared resource management |
| Event Viewer | Monitoring and troubleshooting |
| Command Prompt | Network testing and administration |
| Nmap | Internal network discovery and service validation |

---

# 💻 Lab Environment

The project was deployed entirely inside Microsoft Hyper-V to create an isolated enterprise environment for testing and administration.

| Virtual Machine | Operating System | Role |
|-----------------|------------------|------|
| DC01 | Windows Server 2022 | Domain Controller |
| WIN10 | Windows 10 Enterprise | Domain Client |
| Kali | Kali Linux | Security Validation |

---

# 🌐 Network Architecture

```text
                        Host Computer
                              │
                     Microsoft Hyper-V
                              │
                  Internal Virtual Switch
                              │
        ┌─────────────────────┼─────────────────────┐
        │                     │                     │
   ┌──────────┐         ┌────────────┐       ┌──────────┐
   │   DC01   │         │   WIN10    │       │   Kali   │
   │ Domain   │         │ Enterprise │       │  Linux   │
   │Controller│         │   Client   │       │ Security │
   └──────────┘         └────────────┘       └──────────┘
```

---

# 📊 Project at a Glance

| Category | Details |
|----------|---------|
| Virtualization Platform | Microsoft Hyper-V |
| Server Operating System | Windows Server 2022 |
| Client Operating System | Windows 10 Enterprise |
| Security Platform | Kali Linux |
| Directory Service | Active Directory Domain Services |
| Network Services | DNS, DHCP |
| Policy Management | Group Policy |
| File Services | Shared Folders and NTFS Permissions |
| Virtual Machines | 3 |
| Domain Controller | DC01 |

---

# 🚀 Deployment Workflow

The deployment followed a structured implementation process to ensure each enterprise service was correctly configured and validated before introducing the next component.

```text
Planning
    │
    ▼
Hyper-V Environment Setup
    │
    ▼
Internal Virtual Switch Configuration
    │
    ▼
Network Address Translation (NAT)
    │
    ▼
Windows Server 2022 Installation
    │
    ▼
Static IP Address Configuration
    │
    ▼
Active Directory Domain Services (AD DS)
    │
    ▼
DNS Configuration
    │
    ▼
DHCP Configuration
    │
    ▼
Organizational Units (OUs)
    │
    ▼
Users & Security Groups
    │
    ▼
Shared Folder Configuration
    │
    ▼
Group Policy Objects (GPOs)
    │
    ▼
Windows 10 Domain Integration
    │
    ▼
Internal Security Validation (Kali Linux)
    │
    ▼
Testing & Troubleshooting
    │
    ▼
Completed Enterprise Infrastructure
```

---

# 📂 Repository Structure

```text
Enterprise-Active-Directory-Lab
│
├── 📄 README.md
│
├── 📁 Documentation
│   └── Enterprise Active Directory Infrastructure Deployment.pdf
│
├── 📁 Assets
│   ├── Network-Topology.png
│   ├── Lab-Architecture.png
│   └── Project-Banner.png
│
├── 📁 Screenshots
│   ├── 01-Hyper-V
│   ├── 02-Internal-Switch
│   ├── 03-NAT
│   ├── 04-Windows-Server
│   ├── 05-Active-Directory
│   ├── 06-DNS
│   ├── 07-DHCP
│   ├── 08-Organizational-Units
│   ├── 09-Users-and-Groups
│   ├── 10-Shared-Folder
│   ├── 11-Group-Policy
│   ├── 12-Windows10-Domain
│   ├── 13-Kali-Linux
│   └── 14-Testing
│
└── 📜 LICENSE
```

---

# 🗺️ Deployment Roadmap

The project was completed through the following phases:

| Phase | Description | Status |
|:------|:------------|:------:|
| Planning | Designed the enterprise lab environment | ✅ |
| Virtualization | Configured Microsoft Hyper-V | ✅ |
| Networking | Created Internal Virtual Switch and NAT | ✅ |
| Server Deployment | Installed Windows Server 2022 | ✅ |
| Domain Services | Deployed Active Directory Domain Services | ✅ |
| Network Services | Configured DNS and DHCP | ✅ |
| Identity Management | Created OUs, users, and security groups | ✅ |
| Resource Management | Configured shared folders and permissions | ✅ |
| Policy Management | Implemented Group Policy Objects | ✅ |
| Client Integration | Joined Windows 10 to the domain | ✅ |
| Security Validation | Connected Kali Linux and validated services | ✅ |
| Testing | Verified enterprise functionality | ✅ |
| Documentation | Produced complete technical documentation | ✅ |

---

# 🎯 Core Services Implemented

| Service | Description |
|---------|-------------|
| Active Directory Domain Services | Centralized identity and authentication |
| DNS | Internal hostname resolution |
| DHCP | Automatic IP address assignment |
| Group Policy | Centralized security and configuration management |
| File Services | Shared folders with controlled access |
| Organizational Units | Structured administrative hierarchy |
| User & Group Management | Centralized account administration |
| Windows 10 Domain Join | Enterprise client integration |
| Hyper-V Networking | Isolated virtual enterprise environment |
| Kali Linux Validation | Internal connectivity and service verification |

---

# 📸 Project Gallery

The screenshots included in this repository document each stage of the deployment process.

| Screenshot | Description |
|------------|-------------|
| Hyper-V Configuration | Virtual environment setup |
| Internal Virtual Switch | Network isolation configuration |
| NAT Configuration | Internal network connectivity |
| Windows Server Installation | Server deployment |
| Active Directory | Domain Controller promotion |
| DNS Manager | Name resolution configuration |
| DHCP Manager | IP address management |
| Organizational Units | Directory structure |
| User & Group Management | Identity administration |
| Shared Folder | Resource sharing |
| Group Policy | Centralized policy management |
| Windows 10 Domain Join | Client integration |
| Kali Linux | Internal network validation |
| Testing Results | Final validation |

---

# 📈 Project Outcomes

At the completion of the deployment, the environment successfully provided:

- Centralized authentication through Active Directory.
- Automated IP address allocation using DHCP.
- Reliable internal name resolution through DNS.
- Domain-based administration of Windows 10 clients.
- Centralized security policy enforcement with Group Policy.
- Secure access to shared folders.
- Successful communication between all virtual machines.
- Internal network validation using Kali Linux.
- A fully documented enterprise deployment suitable for learning and portfolio presentation.

---

# ⚙️ Implementation

This section documents the complete deployment of the enterprise infrastructure, from preparing the virtual environment to validating the finished network. Each stage built upon the previous one, ensuring that every service was fully operational before introducing additional components.

---

## 1. Preparing the Virtual Environment

The project began by creating a dedicated virtual environment using Microsoft Hyper-V. An **Internal Virtual Switch** was configured to allow secure communication between the virtual machines while isolating the lab from the external network.

To provide internet connectivity without exposing the internal environment directly, **Network Address Translation (NAT)** was configured on the host system. This allowed the virtual machines to access the internet for updates and package installations while maintaining an isolated enterprise network.

**Outcome**

- Hyper-V environment successfully prepared
- Internal Virtual Switch configured
- NAT enabled for internet connectivity
- Enterprise lab network isolated from the host network

---

## 2. Deploying Windows Server 2022

Windows Server 2022 was installed as the foundation of the enterprise infrastructure. After installation, the server was configured with a static IP address to ensure consistent communication with all clients and services throughout the network.

The server was renamed **DC01** to reflect its role as the primary Domain Controller before additional roles and features were installed.

**Outcome**

- Windows Server 2022 installed successfully
- Static IP address configured
- Server renamed to DC01
- Initial configuration completed

---

## 3. Deploying Active Directory Domain Services

Active Directory Domain Services (AD DS) was installed and the server was promoted to a Domain Controller. A new forest and domain were created to provide centralized authentication and directory services for the enterprise environment.

With Active Directory deployed, the infrastructure gained the ability to centrally manage users, computers, and security policies.

**Outcome**

- Active Directory Domain Services installed
- Domain Controller successfully promoted
- Enterprise domain created
- Centralized authentication enabled

---

## 4. Configuring DNS

The Domain Name System (DNS) service was configured alongside Active Directory to provide reliable hostname resolution within the enterprise network.

Correct DNS configuration ensured that domain services, authentication, and client communication functioned properly throughout the deployment.

**Outcome**

- DNS server configured
- Forward lookup zone created
- Domain name resolution validated
- Client name resolution verified

---

## 5. Configuring DHCP

Dynamic Host Configuration Protocol (DHCP) was deployed to automate IP address assignment for client computers joining the enterprise network.

A DHCP scope was created and activated to distribute IP addresses and network configuration settings automatically.

**Outcome**

- DHCP role installed
- Scope configured
- Automatic IP allocation enabled
- Client connectivity verified

---

## 6. Designing the Active Directory Structure

To simulate a structured enterprise environment, Organizational Units (OUs) were created to logically organize users, computers, and administrative resources.

Domain users and security groups were then created to demonstrate centralized identity management and role-based administration.

**Outcome**

- Organizational Units created
- Domain users configured
- Security groups created
- Directory structure organized

---

## 7. Configuring File Sharing

Shared folders were created to demonstrate centralized resource management within the domain environment.

Appropriate sharing and NTFS permissions were applied to control user access while maintaining secure file management practices.

**Outcome**

- Shared folders configured
- NTFS permissions applied
- Network sharing validated
- Domain user access verified

---

## 8. Implementing Group Policy

Group Policy Objects (GPOs) were created and linked to Organizational Units to demonstrate centralized policy management.

The policies were applied to enforce administrative configurations across domain-joined systems, illustrating how enterprise environments maintain consistent settings.

**Outcome**

- Group Policy Objects created
- Policies linked successfully
- Group Policy applied
- Centralized administration demonstrated

---

## 9. Joining Windows 10 to the Domain

A Windows 10 Enterprise virtual machine was configured and successfully joined to the Active Directory domain.

After joining the domain, authentication was performed using domain user accounts to confirm successful integration with the enterprise infrastructure.

**Outcome**

- Windows 10 joined to the domain
- Domain authentication verified
- Client communication confirmed
- Enterprise management validated

---

## 10. Internal Security Validation

Kali Linux was connected to the Internal Virtual Switch to perform internal network validation.

Connectivity tests confirmed communication between systems, while service validation verified that the deployed enterprise services were functioning as expected.

This stage demonstrated the importance of validating infrastructure after deployment to ensure network services were operating correctly.

**Outcome**

- Kali Linux connected successfully
- Internal connectivity verified
- Enterprise services validated
- Deployment confirmed operational

---

## 11. Final Validation

Following the deployment of all enterprise services, comprehensive testing was performed to confirm that the infrastructure functioned as intended.

Each service was tested individually before validating communication across the entire environment.

The successful completion of these tests confirmed that the virtual enterprise network was operating as a centralized Windows Server environment capable of supporting user authentication, network services, policy management, and secure resource sharing.

---

# 🧪 Testing and Validation

Following the deployment of the enterprise infrastructure, a series of validation tests were performed to confirm that each service was operating correctly. Every component was tested individually before verifying communication across the complete environment.

The objective of this phase was to ensure that authentication, network services, resource sharing, and policy enforcement functioned together as expected.

---

## Active Directory Validation

The deployment of Active Directory Domain Services was verified by authenticating domain user accounts and confirming successful communication between the Domain Controller and the Windows 10 client.

### Validation Results

- Domain Controller operational
- Domain successfully created
- Domain users authenticated successfully
- Organizational Units accessible
- User and group management confirmed

**Status:** ✅ Passed

---

## DNS Validation

DNS functionality was tested by verifying that domain names could be resolved correctly from domain-joined systems.

Successful name resolution confirmed that Active Directory services could locate the Domain Controller without relying on manual IP addressing.

### Validation Results

- Domain name resolved successfully
- DNS server responding correctly
- Name resolution functioning properly

**Status:** ✅ Passed

---

## DHCP Validation

DHCP was validated by confirming that client systems received network configuration automatically from the configured scope.

The assigned IP configuration was verified to ensure proper communication across the virtual network.

### Validation Results

- IP address assigned automatically
- Gateway information received
- DNS server assigned correctly
- Client communication successful

**Status:** ✅ Passed

---

## Windows 10 Domain Validation

The Windows 10 Enterprise client was successfully joined to the Active Directory domain.

Domain authentication was tested by logging in with domain credentials and confirming access to enterprise resources.

### Validation Results

- Windows 10 joined successfully
- Domain login successful
- Domain communication verified

**Status:** ✅ Passed

---

## Shared Folder Validation

Shared resources were tested to verify that authorized users could access network folders according to the configured permissions.

### Validation Results

- Shared folder accessible
- File permissions functioning correctly
- Network resource available

**Status:** ✅ Passed

---

## Group Policy Validation

Group Policy Objects (GPOs) were tested after being linked to the appropriate Organizational Units.

Policy updates were applied and verified to ensure centralized administration was functioning correctly.

### Validation Results

- Policies linked successfully
- Group Policy applied correctly
- Centralized management confirmed

**Status:** ✅ Passed

---

## Internal Network Validation

Kali Linux was connected to the Internal Virtual Switch to verify communication within the isolated enterprise environment.

Connectivity tests confirmed that deployed services were reachable from the internal network.

### Validation Results

- Internal connectivity confirmed
- Domain Controller reachable
- Network services accessible

**Status:** ✅ Passed

---

# 📸 Deployment Gallery

The screenshots included in this repository provide visual documentation of the deployment process from initial configuration to final validation.

| Screenshot | Description |
|------------|-------------|
| Hyper-V Environment | Virtual infrastructure creation |
| Internal Virtual Switch | Network isolation |
| NAT Configuration | Internet connectivity |
| Windows Server Installation | Server deployment |
| Static IP Configuration | Network configuration |
| Active Directory | Domain Controller promotion |
| DNS Configuration | Name resolution |
| DHCP Configuration | Automatic IP allocation |
| Organizational Units | Directory structure |
| User and Group Management | Identity administration |
| Shared Folder Configuration | File sharing |
| Group Policy | Policy management |
| Windows 10 Domain Join | Client integration |
| Kali Linux Validation | Internal security testing |
| Final Testing | Environment validation |

---

# ⚠️ Challenges Encountered

Like any enterprise deployment, this project involved several configuration and troubleshooting challenges. Rather than bypassing these issues, each one was investigated and resolved to ensure the infrastructure functioned as intended.

Some of the challenges included applying Group Policy successfully, resolving domain authentication issues, configuring DNS correctly for domain communication, troubleshooting Windows 10 domain integration, validating Event Viewer logs, and ensuring Kali Linux communicated properly through the Internal Virtual Switch.

Working through these issues provided valuable experience in diagnosing configuration problems, validating services, and understanding the dependencies between enterprise components.

---

# 💡 Lessons Learned

This project demonstrated that enterprise infrastructure is built through careful planning, methodical implementation, and continuous validation. Each service depended on the correct configuration of the previous one, reinforcing the importance of following a structured deployment process.

Beyond learning how to configure Windows Server roles, the project strengthened practical skills in troubleshooting, system administration, network services, and technical documentation. It also highlighted the value of testing each component thoroughly before moving to the next stage, ensuring a stable and reliable enterprise environment.

---

# 🎓 Skills Demonstrated

This project provided practical experience in deploying, managing, and validating an enterprise Windows Server environment. Throughout the implementation, the following technical skills were developed and applied:

### Windows Server Administration
- Windows Server 2022 installation and configuration
- Server role and feature management
- Static IP configuration
- System administration and maintenance

### Active Directory Administration
- Active Directory Domain Services (AD DS)
- Domain Controller deployment
- Organizational Unit (OU) management
- User and security group administration
- Domain authentication

### Network Services
- Domain Name System (DNS)
- Dynamic Host Configuration Protocol (DHCP)
- IP address management
- Name resolution
- Internal network configuration

### Group Policy Management
- Group Policy Object (GPO) creation
- Policy linking
- Centralized configuration management
- Policy validation

### Virtualization
- Microsoft Hyper-V
- Internal Virtual Switch
- Network Address Translation (NAT)
- Virtual machine deployment
- Virtual networking

### File Services
- Shared folder configuration
- NTFS permissions
- Access control
- Resource sharing

### Security Validation
- Internal network testing
- Service validation
- Connectivity verification
- Basic network enumeration using Kali Linux

### Documentation
- Technical documentation
- Deployment documentation
- Troubleshooting documentation
- Validation reporting

---

# 📂 Documentation

A complete technical report is included in this repository.

The documentation covers:

- Project planning
- Lab design
- Infrastructure deployment
- Active Directory configuration
- DNS configuration
- DHCP configuration
- File sharing
- Group Policy implementation
- Windows 10 domain integration
- Security validation
- Testing
- Troubleshooting
- Lessons learned
- Conclusion

📄 **Location**

```text
Documentation/
└── Enterprise Active Directory Infrastructure Deployment.pdf
```

---

# 🚀 Future Improvements

This lab provides a solid foundation for enterprise Windows administration and can be expanded with additional technologies and services.

Possible future enhancements include:

- Deploying a secondary Domain Controller for redundancy
- Implementing Active Directory Certificate Services (AD CS)
- Configuring Windows Server Update Services (WSUS)
- Deploying Microsoft SQL Server
- Integrating Microsoft Defender for Endpoint
- Configuring Remote Desktop Services (RDS)
- Implementing centralized log collection
- Deploying Windows Admin Center
- Creating PowerShell automation scripts
- Integrating Microsoft Azure Active Directory

---

# 📖 References

The implementation of this project was supported by official Microsoft documentation and other technical resources.

- Microsoft Learn – Windows Server Documentation
- Microsoft Learn – Active Directory Domain Services
- Microsoft Learn – DNS Documentation
- Microsoft Learn – DHCP Documentation
- Microsoft Learn – Group Policy Documentation
- Microsoft Learn – Hyper-V Documentation
- Nmap Official Documentation

---

# 🤝 Contributing

This repository was created as a personal learning and portfolio project. Feedback, suggestions, and discussions are always welcome.

If you identify improvements or alternative approaches, feel free to open an issue or submit a pull request.

---

# 📜 License

This project is licensed under the MIT License.

---

# 👨‍💻 Author

## Sheu Abduljelil

**Cybersecurity Analyst | SOC Enthusiast | Windows Server Administrator**

I enjoy building practical lab environments that strengthen my understanding of enterprise infrastructure, system administration, and cybersecurity through hands-on implementation. My focus is on continuously improving technical skills by designing, deploying, validating, and documenting real-world IT solutions.

### Connect with Me

- GitHub:(https://github.com/SheuSec)
- LinkedIn:www.linkedin.com/in/sheu-abduljelil-olamide

---

<div align="center">

## ⭐ If you found this project helpful, consider giving it a star.

It helps others discover the project and supports my learning journey.

---

**"Building enterprise infrastructure is more than installing servers. It is about creating reliable systems, understanding how technologies work together, and solving problems through continuous learning."**

Thank you for visiting this repository.

</div>
