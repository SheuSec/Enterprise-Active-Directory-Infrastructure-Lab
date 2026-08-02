# Implementing Group Policy Objects (GPOs)

## Objective

After configuring the Active Directory structure, users, Security Groups, and shared resources, the next stage was to implement **Group Policy Objects (GPOs)** to centrally manage security and administrative settings across the domain.

Rather than configuring each computer individually, Group Policy enables administrators to enforce consistent configurations across all domain-joined devices from a single location.

The objective of this stage was to strengthen the security of the environment by implementing password policies, account lockout policies, and an interactive logon message using Group Policy.

---

## Implementation

I began by opening the **Group Policy Management Console (GPMC)** from the Windows Administrative Tools. Since these security settings were intended to apply across the entire environment, I created and configured a Group Policy Object linked to the **olalab.local** domain.

The first configuration involved the **Password Policy**, where I enforced password complexity requirements, configured a minimum password length, and enabled password history. These settings help strengthen authentication by encouraging users to create secure passwords and reducing the likelihood of password reuse.

Next, I configured the **Account Lockout Policy**. This policy automatically locks a user account after a specified number of failed authentication attempts, helping protect the environment against password-guessing and brute-force attacks.

To improve security awareness, I also configured an **Interactive Logon Message** that is displayed before users sign in. The message informs users that the system is intended for authorized access only and that activities may be monitored.

After completing the configuration, I linked the Group Policy Object to the domain and updated the policies using the **gpupdate /force** command. Finally, I verified that the configured policies were successfully applied to the Windows 10 domain client.

---

## Verification

To verify that the Group Policy configuration was successful, I confirmed that:

- The Group Policy Object was successfully linked to the **olalab.local** domain.
- Group Policy was refreshed using the **gpupdate /force** command.
- The configured Password Policy was applied successfully.
- The Account Lockout Policy was functioning as expected.
- The Interactive Logon Message appeared before user authentication.
- The **gpresult** command confirmed that the Windows 10 client received the configured policies.

These verification steps confirmed that the security policies were successfully deployed and enforced across the domain.

---

## Outcome

The Group Policy deployment was completed successfully, allowing security settings to be centrally managed through Active Directory.

Password policies, account lockout settings, and the interactive logon message were automatically applied to domain-joined systems, eliminating the need to configure each computer individually.

This implementation demonstrated how centralized policy management improves administrative efficiency while strengthening the overall security posture of the enterprise environment.

---

## Reflection

Implementing Group Policy provided valuable insight into how enterprise administrators maintain consistency and security across large environments. Instead of manually configuring individual workstations, policies can be created once and automatically applied whenever users sign in or computers start.

This stage reinforced the importance of centralized administration and demonstrated how Group Policy simplifies security management while supporting organizational compliance and operational efficiency.

Seeing the configured policies successfully applied to the Windows 10 client highlighted how Active Directory, Organizational Units, Security Groups, and Group Policy work together to create a secure and well-managed enterprise infrastructure.

---

## Screenshots

The following screenshots support this stage:
https://github.com/SheuSec/Enterprise-Active-Directory-Infrastructure-Lab/blob/main/Screenshots/Screenshots%20Group-Policy-Management.md.pdf


