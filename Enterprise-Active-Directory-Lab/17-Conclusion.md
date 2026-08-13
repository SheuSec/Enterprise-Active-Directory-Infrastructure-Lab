# Conclusion

This project successfully demonstrated the complete design, deployment, configuration, validation, and documentation of a Windows Server 2022 Active Directory environment using Microsoft Hyper-V.

Beginning with an empty virtual environment, I designed and implemented a fully functional enterprise infrastructure by deploying Windows Server 2022 as the Domain Controller and configuring the core services that support modern Windows-based networks. These included Active Directory Domain Services (AD DS), Domain Name System (DNS), Dynamic Host Configuration Protocol (DHCP), File Services, Group Policy Objects (GPOs), and centralized user and resource management.

To simulate a realistic business environment, I created Organizational Units (OUs), domain user accounts, security groups, departmental shared folders, and role-based access controls using NTFS and Share Permissions. A Windows 10 workstation was successfully joined to the **olalab.local** domain, where centralized authentication, automated network configuration, policy enforcement, and secure resource access were validated.

To further assess the environment, Kali Linux was connected to the isolated enterprise network to perform internal security validation. Network reconnaissance confirmed that the expected Active Directory services—including DNS, Kerberos, LDAP, SMB, and RPC—were available and functioning as intended.

Throughout the deployment, I encountered several technical challenges involving networking, DNS configuration, domain authentication, Group Policy application, and permission management. Resolving these issues strengthened my troubleshooting methodology and reinforced the importance of structured planning, systematic validation, and careful documentation throughout an infrastructure deployment.

More importantly, this project transformed theoretical concepts into practical experience. It provided valuable hands-on exposure to enterprise Windows administration while demonstrating how multiple infrastructure services work together to deliver secure, centralized, and scalable network management.

The successful completion of this project demonstrates my ability to design, deploy, troubleshoot, validate, and document a Windows-based enterprise environment using industry-standard technologies and best practices.



