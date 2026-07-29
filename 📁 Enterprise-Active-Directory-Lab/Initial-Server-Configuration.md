# Initial Server Configuration

## Objective

After successfully installing Windows Server 2022, the next step was to prepare the server for its role within the enterprise environment. Before deploying Active Directory Domain Services (AD DS) and other infrastructure services, I needed to assign the server a meaningful hostname, configure a static IPv4 address, and verify network connectivity.

Completing these tasks ensured that the server could be consistently identified on the network and provide reliable services throughout the deployment.

---

## Implementation

After signing in to Windows Server 2022 for the first time, I reviewed the default system configuration to ensure the operating system was functioning correctly. Since this server would later become the Domain Controller, establishing a consistent identity and network configuration was essential before installing any server roles.

The first task was to rename the computer to **DC01**. Assigning a descriptive hostname simplifies server administration and makes it easier to identify the server's role within the network as the environment grows. After renaming the server, I restarted the operating system to apply the changes.

Next, I configured a static IPv4 address on the server's network adapter. Unlike client computers, a Domain Controller requires a fixed IP address because services such as Active Directory, DNS, and DHCP depend on a consistent network identity. During this process, I configured the IPv4 address, subnet mask, default gateway, and preferred DNS server.

After completing the network configuration, I verified that the server could communicate successfully with other systems on the virtual network. This confirmed that the Internal Virtual Switch and Network Address Translation (NAT) configured during the previous stages were functioning correctly.

---

## Verification

To verify that the initial server configuration was completed successfully, I confirmed that:

- The computer name had been successfully changed to **DC01**.
- The static IPv4 address was correctly assigned.
- The preferred DNS server was configured correctly.
- Network communication with the host computer and other virtual machines was successful.
- The network adapter configuration contained no errors.

These verification steps confirmed that the server was fully prepared for the installation of Active Directory Domain Services.

---

## Outcome

The initial server configuration was completed successfully. Renaming the server and assigning a static IP address established a consistent network identity that would remain unchanged throughout the deployment.

With these foundational settings in place, the server was fully prepared for the installation of Active Directory Domain Services (AD DS) and other enterprise infrastructure roles.

---

## Reflection

This stage reinforced the importance of consistency in Windows Server administration. Infrastructure servers differ from client computers because they provide services that other systems depend on. Assigning a static IP address and a meaningful hostname helps ensure those services remain stable and accessible.

Although renaming the server and configuring a static IP address are relatively simple tasks, they form the foundation for critical services such as Active Directory, DNS, and DHCP. Completing these configurations before installing server roles reduced the risk of future network issues and highlighted the value of careful planning in enterprise deployments.

---

## Screenshots

Include the following screenshots to support this stage:
https://github.com/SheuSec/Enterprise-Active-Directory-Infrastructure-Lab/blob/main/%F0%9F%93%81%20Enterprise-Active-Directory-Lab/Screenshots%20Initial-Server-Configuration.pdf
