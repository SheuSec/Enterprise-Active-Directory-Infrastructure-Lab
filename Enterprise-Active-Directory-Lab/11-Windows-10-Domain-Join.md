# Joining the Windows 10 Client to the Domain

## Objective

With the Domain Controller and core network services fully configured, the next stage was to join the Windows 10 client to the **olalab.local** domain. Joining the client to the domain enables centralized authentication, policy enforcement, and secure access to shared network resources managed through Active Directory.

The objective of this stage was to integrate the client computer into the enterprise environment and verify successful communication with the Domain Controller.

---

## Implementation

Before joining the client to the domain, I confirmed that the Windows 10 workstation had received a valid IP address from the DHCP server and that its preferred DNS server was configured to point to the Domain Controller. These settings were essential because the client needed to locate the Domain Controller before domain authentication could take place.

After verifying the network configuration, I opened the **System Properties** window and changed the computer's membership from a workgroup to the **olalab.local** domain. When prompted, I entered the credentials of a domain administrator to authorize the domain join operation.

After successful authentication, Windows displayed a confirmation message indicating that the computer had successfully joined the domain. I then restarted the workstation to complete the process and apply the new domain membership.

Once the computer restarted, I signed in using a domain user account that had previously been created in Active Directory. This confirmed that authentication was now being performed by the Domain Controller rather than through local user accounts.

During the deployment, I encountered several authentication issues, including incorrect password entries and domain login errors. Instead of rebuilding the environment, I followed a structured troubleshooting process by verifying user credentials, confirming domain membership, checking DNS configuration, and validating network connectivity. After resolving these issues, the Windows 10 client successfully authenticated with the domain.

---

## Verification

To verify that the Windows 10 client had successfully joined the domain, I confirmed that:

- The Windows 10 computer appeared in Active Directory Users and Computers (ADUC).
- Domain user accounts could successfully log in.
- Group Policy settings were applied to the client computer.
- Shared folders were accessible using domain credentials.
- The client communicated successfully with the Domain Controller using both its hostname and IP address.
- System information confirmed that the computer was a member of the **olalab.local** domain.

These verification steps confirmed that the client computer had been successfully integrated into the Active Directory environment.

---

## Outcome

The Windows 10 workstation was successfully joined to the **olalab.local** domain and became a fully managed client within the enterprise environment.

Users were able to authenticate using their domain accounts, receive centrally managed Group Policies, and access shared network resources according to their assigned permissions.

This stage represented a major milestone in the project because the environment had evolved from an isolated server deployment into a fully functional enterprise client-server infrastructure.

---

## Reflection

Joining the Windows 10 client to the domain demonstrated how the various infrastructure services deployed throughout the project work together to provide centralized management. Active Directory, DNS, DHCP, Group Policy, and file services all played an essential role in enabling seamless authentication and resource access.

Troubleshooting the authentication issues during this stage strengthened my understanding of the domain join process and reinforced the importance of accurate DNS configuration, proper user account management, and network connectivity.

Successfully signing in with a domain account and accessing centrally managed resources was one of the most rewarding moments of the project. It confirmed that the planning, deployment, and configuration completed during the earlier stages had resulted in a fully operational enterprise environment.

---

## Screenshots

The following screenshots support this stage:

https://github.com/SheuSec/Enterprise-Active-Directory-Infrastructure-Lab/blob/main/Screenshots/Screenshots%20Windows-10-Domain-Join.md.pdf

