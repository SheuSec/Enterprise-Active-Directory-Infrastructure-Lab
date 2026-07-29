# Configuring Dynamic Host Configuration Protocol (DHCP)

## Objective

After successfully deploying Active Directory Domain Services (AD DS) and verifying that Domain Name System (DNS) was functioning correctly, the next step was to configure the **Dynamic Host Configuration Protocol (DHCP)** service.

In an enterprise environment, manually assigning IP addresses to every computer is inefficient and difficult to manage. DHCP automates this process by assigning IP addresses and other network settings whenever a client device joins the network.

The objective of this stage was to deploy a DHCP server capable of automatically assigning IP addresses, subnet masks, default gateways, DNS server information, and domain settings to client devices connected to the lab network.

---

## Implementation

I began by opening **Server Manager** and installing the **DHCP Server** role using the **Add Roles and Features Wizard**. After the installation completed successfully, I performed the required post-installation tasks and authorized the DHCP server in Active Directory.

Authorizing the DHCP server is an important security measure because it ensures that only trusted DHCP servers within the domain can distribute IP address information to client computers.

Once authorization was complete, I opened the **DHCP Management Console** and created a new IPv4 scope for the lab environment. During the scope configuration, I defined the range of IP addresses that would be assigned to client devices.

To prevent address conflicts, I excluded the static IP address assigned to the Domain Controller from the available address pool.

Next, I configured the scope options, including the subnet mask, default gateway, preferred DNS server, and the DNS domain name (**olalab.local**). These settings ensured that every client receiving an IP address from the DHCP server would automatically receive the network configuration required to communicate correctly within the domain.

After completing the scope configuration, I activated the scope and confirmed that the DHCP service was ready to lease IP addresses to client devices.

---

## Verification

To verify that DHCP was functioning correctly, I confirmed that:

- The DHCP Server role was installed successfully.
- The DHCP server was authorized in Active Directory.
- The IPv4 scope was created and activated.
- The Windows 10 client successfully renewed its IP configuration.
- The client received an IP address from the configured DHCP scope.
- The client also received the correct subnet mask, default gateway, preferred DNS server, and domain information.

These verification steps confirmed that the DHCP service was successfully providing automatic network configuration to client devices.

---

## Outcome

The DHCP deployment was completed successfully, allowing the Windows 10 client to automatically obtain a valid IP address and all required network settings.

This eliminated the need for manual network configuration on client computers and provided a scalable method for managing network connectivity across the enterprise environment.

With DHCP fully operational, the infrastructure was prepared for client computers to join the **olalab.local** Active Directory domain.

---

## Reflection

Configuring DHCP demonstrated how enterprise networks automate routine administrative tasks while reducing configuration errors. Rather than manually assigning network settings to each workstation, the DHCP server centrally distributes consistent network information whenever a client connects to the network.

This stage also highlighted the close relationship between DHCP, DNS, and Active Directory. Together, these services provide seamless network connectivity, name resolution, and centralized authentication, forming the core of a modern Windows enterprise infrastructure.

Watching the Windows 10 client automatically receive its IP configuration reinforced the value of centralized network services and provided a practical understanding of how enterprise administrators simplify network management.

---

## Screenshots

The following screenshots support this stage:
https://github.com/SheuSec/Enterprise-Active-Directory-Infrastructure-Lab/blob/main/Screenshots/Screenshots%20DHCP-Configuration.md.pdf
