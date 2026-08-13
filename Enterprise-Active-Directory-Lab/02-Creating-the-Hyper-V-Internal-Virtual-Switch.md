# Creating the Hyper-V Internal Virtual Switch

## Objective

Before deploying any server roles or configuring enterprise services, I needed to establish a reliable network that would allow all virtual machines to communicate securely. Rather than connecting the lab directly to my physical home network, I created an isolated virtual network using Microsoft Hyper-V.

This approach allowed me to build, test, and troubleshoot the entire environment without affecting other devices on my physical network, providing a safe and controlled workspace for the deployment.

---

## Implementation

I began by opening **Hyper-V Manager** and launching **Virtual Switch Manager**. Since the project required communication between multiple virtual machines while remaining isolated from the physical network, I selected the **Internal** virtual switch type.

After creating the Internal Virtual Switch, I assigned it a descriptive name to make it easy to identify throughout the project. This switch became the backbone of the lab environment and was later connected to every virtual machine, including the Windows Server 2022 Domain Controller (**DC01**), the Windows 10 Enterprise client, and the Kali Linux virtual machine.

Once the switch was created, I updated the network adapter settings of each virtual machine to use the newly created Internal Virtual Switch. Connecting every system to the same virtual network ensured they could communicate with one another during the deployment of enterprise services.

At this stage, the environment was intentionally isolated from the physical network. While the virtual machines could communicate internally, they could not access the internet until Network Address Translation (NAT) was configured in the next stage of the deployment.

---

## Verification

To verify that the Internal Virtual Switch had been configured successfully, I confirmed that:

- The Internal Virtual Switch appeared in Hyper-V Virtual Switch Manager.
- Windows Server 2022, Windows 10 Enterprise, and Kali Linux were all connected to the same virtual switch.
- The network adapter of each virtual machine reflected the correct virtual switch configuration.
- The virtual machines were ready to communicate within the isolated network.

These checks confirmed that the virtual networking foundation had been established successfully before proceeding to internet connectivity and server deployment.

---

## Outcome

The Internal Virtual Switch provided a dedicated and isolated network for the lab environment. This network became the foundation for every enterprise service configured later in the project, including Active Directory Domain Services (AD DS), DNS, DHCP, file sharing, and Group Policy.

With the internal network successfully established, the environment was ready for the next phase: configuring Network Address Translation (NAT) to provide controlled internet access while maintaining network isolation.

---

## Reflection

This stage reinforced the importance of building a solid network foundation before deploying enterprise services. A properly planned virtual network simplifies deployment, improves troubleshooting, and provides a stable environment for testing infrastructure components.

Using an Internal Virtual Switch also allowed me to experiment with enterprise technologies in a secure and isolated environment, closely reflecting how organizations build development, testing, and training labs without impacting production networks.

---

## Screenshots

The following screenshot support this stage of the deployment:
https://github.com/SheuSec/Enterprise-Active-Directory-Infrastructure-Lab/blob/main/%F0%9F%93%81%20Enterprise-Active-Directory-Lab/Screenshots%20Hyper-V-Internal-Virtual-Switch.pdf


