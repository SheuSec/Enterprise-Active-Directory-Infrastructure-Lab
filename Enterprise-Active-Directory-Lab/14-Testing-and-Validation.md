# Testing and Validation

## Objective

After completing the deployment and configuration of the Active Directory environment, the final stage was to verify that all deployed services were functioning correctly as an integrated enterprise infrastructure. Rather than testing each component independently, I validated the environment to ensure that authentication, networking, file sharing, Group Policy, and communication between systems worked together seamlessly.

The objective of this stage was to confirm that the deployed services met the project requirements and provided a stable, secure, and fully functional enterprise environment.

---

## Implementation

I began by signing in to the Windows 10 client using a domain user account created in Active Directory. Successful authentication confirmed that the client could communicate with the Domain Controller and that Active Directory was processing domain credentials correctly.

Next, I verified that the Windows 10 client had automatically received its network configuration from the DHCP server. Using **Command Prompt**, I confirmed that the assigned IP address, subnet mask, default gateway, and preferred DNS server matched the DHCP scope configured earlier in the project.

To validate DNS functionality, I tested name resolution between the client and the Domain Controller. The client successfully resolved the server's hostname and communicated with it using both its hostname and IP address.

I then accessed the shared folders hosted on the Domain Controller using domain credentials. The configured Share Permissions and NTFS Permissions worked as expected, allowing authorized users to access departmental resources while preventing unauthorized access.

To verify that Group Policy had been applied successfully, I refreshed the client policies using **gpupdate /force** and reviewed the applied policies. The configured password policy, account lockout policy, and interactive logon message were successfully enforced.

Finally, I reviewed the **Event Viewer** logs on the Domain Controller to confirm that authentication events, policy processing, and other system activities were recorded without critical errors. I also confirmed successful communication between the Windows Server, Windows 10 client, and Kali Linux virtual machine.

---

## Verification

To validate the completed deployment, I confirmed that:

- Domain users authenticated successfully through Active Directory.
- The Windows 10 client received network configuration automatically from the DHCP server.
- DNS resolved hostnames correctly within the domain.
- Shared folders were accessible according to the configured permissions.
- Group Policy settings were successfully applied to the client computer.
- Event Viewer recorded authentication and system events without critical errors.
- Communication between Windows Server, Windows 10, and Kali Linux was successful.

These verification steps confirmed that all deployed services were operating together as a stable and fully functional enterprise environment.

---

## Outcome

The testing and validation process confirmed that every major component of the Active Directory infrastructure was functioning correctly.

Active Directory authenticated users successfully, DNS resolved hostnames accurately, DHCP assigned network settings automatically, Group Policy enforced centralized security configurations, and shared resources were accessible according to assigned permissions.

The successful completion of these tests demonstrated that the project objectives had been achieved and that the environment was operating as a realistic enterprise network.

---

## Reflection

Testing and validation reinforced the importance of verifying infrastructure after deployment rather than assuming that successful installation alone guarantees functionality. Each service depended on the others, and validating their interaction demonstrated how enterprise technologies work together to provide centralized administration, secure authentication, and reliable network services.

This stage was one of the most rewarding parts of the project because it confirmed that the planning, configuration, and troubleshooting carried out throughout the deployment had resulted in a fully operational Active Directory environment.

Beyond the technical implementation, this experience strengthened my ability to test, troubleshoot, validate, and document enterprise infrastructure. It also highlighted the importance of following a structured deployment process in which every configuration is verified before an environment is considered ready for production.

---

## Screenshots

The following screenshots support this stage:
https://github.com/SheuSec/Enterprise-Active-Directory-Infrastructure-Lab/blob/main/Screenshots/Screenshots%20Testing-and-Validation%20.pdf

