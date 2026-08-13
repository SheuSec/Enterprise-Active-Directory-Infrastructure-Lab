# Installing Windows Server 2022

## Objective

With the network infrastructure fully configured, the next phase of the project was to deploy Windows Server 2022. This server would later be promoted to the Domain Controller and host the core services required for the enterprise environment, including Active Directory Domain Services (AD DS), Domain Name System (DNS), and Dynamic Host Configuration Protocol (DHCP).

Before configuring these services, it was important to establish a stable and properly installed server operating system that would serve as the foundation of the entire lab.

---

## Implementation

I created a new virtual machine in Microsoft Hyper-V and selected **Windows Server 2022** as the operating system. During the virtual machine creation process, I allocated appropriate system resources, including memory, processor cores, and virtual storage, to ensure the server could support the enterprise services that would be deployed later.

After attaching the Windows Server 2022 installation media, I started the virtual machine and followed the installation wizard. I selected the appropriate edition of Windows Server and completed the installation until the operating system was successfully deployed.

Once the installation was complete, I signed in using the local **Administrator** account and confirmed that the operating system started without errors.

Before proceeding with additional configuration, I reviewed the server to ensure that all virtual hardware had been detected correctly. This included verifying the virtual network adapter, checking the system status through Server Manager, and confirming that the operating system was functioning as expected.

Rather than immediately installing server roles, I first ensured that the operating system was stable. Establishing a reliable foundation at this stage reduced the likelihood of issues during the deployment of Active Directory and other enterprise services.

---

## Verification

To verify that Windows Server 2022 had been installed successfully, I confirmed that:

- The operating system booted successfully.
- I was able to log in using the local Administrator account.
- Server Manager launched without errors.
- The virtual network adapter was detected and operational.
- No critical errors or warnings were reported after installation.

These checks confirmed that the server was ready for further configuration and the deployment of enterprise roles.

---

## Outcome

Windows Server 2022 was successfully installed, providing a stable and reliable platform for the remainder of the project.

With the operating system in place, the next step was to prepare the server for enterprise deployment by assigning a meaningful hostname, configuring a static IP address, and completing the initial system configuration before promoting it to a Domain Controller.

---

## Reflection

This stage reinforced the importance of establishing a stable operating system before deploying enterprise services. Every component configured later in the project—including Active Directory, DNS, DHCP, file sharing, and Group Policy—would rely on the health and stability of this server.

Taking the time to verify the installation before proceeding reflects a common enterprise practice where administrators validate a server's readiness before assigning critical infrastructure roles. Completing this stage marked the transition from preparing the lab environment to building the enterprise infrastructure itself.

---

## Screenshots

Include the following screenshots to support this stage:
(https://github.com/SheuSec/Enterprise-Active-Directory-Infrastructure-Lab/blob/main/Screenshots/Screenshots%20Installing%20Windows%20Server%202022.pdf)

