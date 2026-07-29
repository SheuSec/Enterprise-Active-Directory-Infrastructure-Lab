# Configuring Network Address Translation (NAT)

## Objective

After creating the Internal Virtual Switch, the next step was to provide internet access to the virtual machines without connecting them directly to my physical network. While the Internal Virtual Switch enabled communication between the virtual machines, it did not provide access to external networks. To address this, I configured **Network Address Translation (NAT)** on the Hyper-V host.

This configuration allowed the virtual machines to download updates, install Windows features, and access online resources while remaining securely isolated within the lab environment.

---

## Implementation

I began by assigning a static IP address to the Hyper-V virtual network adapter that was automatically created for the Internal Virtual Switch on the host computer. This adapter served as the gateway between the isolated lab network and the host's internet connection.

After configuring the IP address, I opened **Windows PowerShell** with administrative privileges and created a new NAT network. The NAT configuration translated outbound traffic from the internal network, allowing the virtual machines to access the internet through the host computer while preventing direct exposure to the physical network.

Once the configuration was complete, I verified that the virtual machines could communicate with one another over the internal network while also accessing external resources when required.

Establishing internet connectivity at this stage ensured that Windows updates, server roles, and additional features could be installed without interruption before the deployment of enterprise services.

---

## Verification

To verify that the NAT configuration was successful, I confirmed that:

- The Hyper-V virtual network adapter had the correct static IP configuration.
- The NAT network was successfully created in Windows PowerShell.
- Windows Server 2022 had internet connectivity.
- Windows 10 Enterprise could access external resources.
- Kali Linux could communicate with both the internal network and the internet.
- Communication between all virtual machines remained functional after enabling NAT.

These verification steps confirmed that the lab environment provided both secure internal communication and controlled internet access.

---

## Outcome

The NAT configuration successfully provided internet access to every virtual machine connected to the Internal Virtual Switch without exposing the lab directly to the physical network.

With networking fully configured, the environment was ready for the deployment of Windows Server 2022 and enterprise services including Active Directory Domain Services (AD DS), DNS, and DHCP.

---

## Reflection

This stage demonstrated the importance of balancing security with functionality in an enterprise environment. By combining an Internal Virtual Switch with Network Address Translation, I was able to maintain an isolated lab while still providing the connectivity required for system updates, software installation, and administrative tasks.

This design closely reflects how many organizations separate development and testing environments from production networks while maintaining controlled access to external resources.

---

## Screenshots

Include the following screenshot to support this stage:
https://github.com/SheuSec/Enterprise-Active-Directory-Infrastructure-Lab/blob/main/%F0%9F%93%81%20Enterprise-Active-Directory-Lab/Screenshots%20Configuring%20Network%20Address%20Translation.pdf

