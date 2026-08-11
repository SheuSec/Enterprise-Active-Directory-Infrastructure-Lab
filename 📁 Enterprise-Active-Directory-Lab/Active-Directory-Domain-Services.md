# Deploying Active Directory Domain Services (AD DS)

## Objective

With the server fully prepared, the next phase of the deployment was to install **Active Directory Domain Services (AD DS)**. This role transforms a Windows Server into a **Domain Controller**, enabling centralized management of users, computers, authentication, and security policies across the network.

The objective was not simply to install a server role, but to establish the identity management platform that would serve as the foundation for every enterprise service deployed throughout the project.

---

## Implementation

I began by opening **Server Manager** and selecting **Add Roles and Features**. Using the installation wizard, I chose the **Active Directory Domain Services (AD DS)** role and accepted the additional management tools that Windows recommended.

After the role installation completed successfully, Server Manager displayed a notification indicating that further configuration was required before the role could become operational. I selected **Promote this server to a domain controller** to begin the Active Directory deployment process.

Because this was a new enterprise environment, I selected **Add a new forest** and specified **olalab.local** as the root domain name. This domain became the central identity for every user account, computer, security group, and policy created throughout the deployment.

During the promotion process, I configured the **Directory Services Restore Mode (DSRM)** password, which provides administrative access for recovery and maintenance operations if Active Directory ever needs to be restored.

Before the installation continued, the deployment wizard automatically performed a series of prerequisite checks to verify that the server met the requirements for becoming a Domain Controller. After confirming that no critical issues were detected, I proceeded with the installation.

The server restarted automatically to complete the promotion process. Once the restart was complete, I signed in using my domain credentials and confirmed that the server was now operating as the Domain Controller for the **olalab.local** domain.

---

## Verification

To verify that Active Directory Domain Services had been deployed successfully, I confirmed that:

- The server had been successfully promoted to a Domain Controller.
- The **olalab.local** domain was created successfully.
- Active Directory management tools were installed and accessible.
- **Active Directory Users and Computers (ADUC)** opened without errors.
- DNS was automatically installed and integrated with Active Directory.
- The server accepted domain authentication using the newly created domain.

These verification steps confirmed that the Active Directory deployment was successful and that the enterprise identity infrastructure was fully operational.

---

## Outcome

The Windows Server 2022 system was successfully promoted to the Domain Controller for the **olalab.local** domain.

At this stage, the server became responsible for centralized authentication, directory services, computer management, and security policy enforcement across the enterprise environment.

This marked the most significant milestone of the deployment, as every remaining configuration—including DNS, DHCP, Organizational Units, users, security groups, Group Policy, and domain-joined clients—would depend on the successful deployment of Active Directory.

---

## Reflection

Deploying Active Directory fundamentally changed how the environment operated. Rather than managing users and permissions individually on each computer, the infrastructure now provided centralized identity management through a single Domain Controller.

This meant that users could authenticate using domain credentials and securely access resources based on centrally managed permissions and policies. It also demonstrated how enterprise administrators manage thousands of users and devices from a unified platform while maintaining consistency, security, and scalability.

Successfully deploying the **olalab.local** domain represented the turning point of the project. The planning, network configuration, and server preparation completed during the earlier stages came together to create a fully functional enterprise identity infrastructure.

Seeing the domain come online and successfully signing in after the promotion process was a rewarding milestone. It reinforced the importance of careful planning, proper sequencing, and thorough validation when deploying enterprise infrastructure.

---

## Screenshots

The following screenshots support this stage:
https://github.com/SheuSec/Enterprise-Active-Directory-Infrastructure-Lab/blob/main/Screenshots/Screenshots%20Deploying%20Active%20Directory%20Domain%20Services.pdf
