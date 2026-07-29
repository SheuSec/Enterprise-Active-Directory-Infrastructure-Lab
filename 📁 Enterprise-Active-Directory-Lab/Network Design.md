# Network Design

## Overview

A reliable network foundation was essential before deploying any Windows Server roles or enterprise services. To achieve this, I designed a simple yet effective virtual network that allowed all virtual machines to communicate securely while remaining isolated from my physical home network.

The lab environment was built around a **Hyper-V Internal Virtual Switch**, which provided private communication between the Domain Controller, Windows 10 client, Kali Linux, and the host computer. This isolated network allowed configuration, testing, and validation to be performed without affecting the production network.

To enable internet connectivity, **Network Address Translation (NAT)** was configured on the host machine. This allowed the virtual machines to download Windows updates, install required server roles and features, and access online resources while maintaining the security and isolation of the lab environment.

The Domain Controller (**DC01**) was assigned a **static IP address** to ensure that essential services such as Active Directory Domain Services (AD DS), Domain Name System (DNS), and Dynamic Host Configuration Protocol (DHCP) remained consistently available. The Windows 10 client was configured to obtain its network configuration automatically from the DHCP server, closely reflecting how client devices are managed in enterprise environments.

This network design provided a stable, secure, and scalable foundation for the deployment of enterprise services throughout the project.

---

## Network Architecture

| Component | Configuration |
|----------|---------------|
| Hypervisor | Microsoft Hyper-V |
| Network Type | Internal Virtual Switch |
| Internet Access | Network Address Translation (NAT) |
| Domain Controller | DC01 |
| Server IP Address | Static |
| Client IP Address | DHCP |
| Connected Systems | Windows Server 2022, Windows 10 Enterprise, Kali Linux |

---

## Design Objectives

The network was designed to:

- Provide secure communication between all virtual machines.
- Isolate the lab environment from the physical network.
- Enable internet connectivity through NAT.
- Support centralized enterprise services such as AD DS, DNS, and DHCP.
- Simulate a realistic enterprise network architecture.

---

## Outcome

The completed network provided a secure and reliable foundation for the deployment of Active Directory, DNS, DHCP, Group Policy, file sharing, and other enterprise services documented throughout this project.

---

## Screenshots
