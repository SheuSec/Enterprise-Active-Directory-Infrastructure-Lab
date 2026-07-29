# 01 – Environment Setup

## Overview

The environment setup phase established the foundation for the entire enterprise infrastructure. Before deploying Active Directory and other network services, a stable and isolated virtual environment was created using Microsoft Hyper-V.

This stage involved creating the virtual machines, configuring an Internal Virtual Switch, enabling internet connectivity through Network Address Translation (NAT), installing Windows Server 2022, assigning a static IP address, renaming the server, and applying system updates. Completing these tasks ensured that the server was fully prepared for the deployment of enterprise services.

---

## Objectives

The objectives of this phase were to:

- Prepare the virtualization environment using Microsoft Hyper-V.
- Create an isolated virtual network.
- Configure NAT to provide internet connectivity.
- Install Windows Server 2022.
- Rename the server to **DC01**.
- Configure a static IP address.
- Install the latest Windows updates.
- Verify that the environment was ready for Active Directory deployment.

---

## Documents

| File | Description |
|------|-------------|
| Hyper-V-Setup.md | Creation of the virtual environment using Microsoft Hyper-V. |
| Internal-Virtual-Switch.md | Configuration of the Internal Virtual Switch for communication between virtual machines. |
| NAT-Configuration.md | Configuration of Network Address Translation (NAT) to provide internet access. |
| Windows-Server-Installation.md | Installation of Windows Server 2022. |
| Rename-Server.md | Renaming the server to DC01. |
| Static-IP-Configuration.md | Assigning a static IP address to the server. |
| Windows-Updates.md | Installing system updates before deployment. |
| Environment-Verification.md | Verifying that the environment is ready for the next deployment phase. |

---

## Expected Outcome

Upon completion of this phase:

- Microsoft Hyper-V is configured.
- The Internal Virtual Switch is operational.
- NAT provides internet connectivity to the virtual environment.
- Windows Server 2022 is successfully installed.
- The server has been renamed to **DC01**.
- A static IP address has been assigned.
- Windows updates have been installed.
- The environment is fully prepared for deploying Active Directory Domain Services (AD DS).

---
