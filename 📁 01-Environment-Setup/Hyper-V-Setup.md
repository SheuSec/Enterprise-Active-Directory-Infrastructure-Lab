# Hyper-V Setup

## Overview

Microsoft Hyper-V was selected as the virtualization platform for this project because it provides a reliable environment for deploying and managing multiple virtual machines on a single physical computer. Using Hyper-V made it possible to simulate an enterprise network without requiring additional physical hardware.

The virtualization environment served as the foundation for the deployment of Windows Server 2022, Windows 10 Enterprise, and Kali Linux. These virtual machines were connected through an Internal Virtual Switch to create an isolated enterprise network for administration, testing, and security validation.

---

## Objective

The objective of this stage was to prepare the virtualization platform required for the deployment of the enterprise infrastructure.

---

## Environment

| Component | Description |
|----------|-------------|
| Virtualization Platform | Microsoft Hyper-V |
| Host Operating System | Windows 11 |
| Server VM | Windows Server 2022 |
| Client VM | Windows 10 Enterprise |
| Security VM | Kali Linux |

---

## Implementation

The Hyper-V feature was enabled on the host operating system before creating the virtual machines required for the project.

Three virtual machines were created to simulate an enterprise environment:

- **DC01** running Windows Server 2022
- **Windows 10 Enterprise** acting as the domain client
- **Kali Linux** for internal network validation and security testing

Each virtual machine was configured with appropriate hardware resources, including memory, processor allocation, virtual hard disks, and network adapters.

The virtual machines were connected using an Internal Virtual Switch to ensure secure communication within the lab environment.

---

## Verification

The virtualization environment was verified by confirming that:

- Hyper-V Manager launched successfully.
- All virtual machines were created.
- Each virtual machine powered on successfully.
- The virtual machines were connected to the correct virtual network.
- Resource allocation was functioning as expected.

---

## Result

The Hyper-V environment was successfully prepared and provided the infrastructure required to deploy the enterprise Windows network.

---

## Screenshots
https://github.com/SheuSec/Enterprise-Active-Directory-Infrastructure-Lab/blob/main/Screenshots%20Hyper-V%20Setup.pdf
---
