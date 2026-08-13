# Configuring File Services and Shared Resources

## Objective

One of the primary responsibilities of a Windows Server in an enterprise environment is providing secure and centralized access to shared resources. After creating the Active Directory structure, including Organizational Units (OUs), user accounts, and Security Groups, the next step was to configure file sharing and implement access controls based on user roles.

The objective of this stage was to create departmental shared folders that could be accessed only by authorized users. To achieve this, I configured both **Share Permissions** and **NTFS Permissions**, following the **Principle of Least Privilege** to ensure users received only the level of access required to perform their responsibilities.

---

## Implementation

I began by creating a dedicated directory on the server to store departmental resources. Within this directory, I created separate shared folders representing the different departments configured in Active Directory.

After creating the folders, I enabled file sharing and configured **Share Permissions** to allow network access. Instead of granting unrestricted permissions, I assigned access based on the Security Groups created earlier in the project.

Next, I configured **NTFS Permissions** for each folder. While Share Permissions control access over the network, NTFS Permissions provide more granular control over the actions users can perform on files and folders. By combining both permission models, I ensured that users could access only the resources appropriate for their roles.

To simplify administration, permissions were assigned to Security Groups rather than individual user accounts. This approach allows administrators to manage access efficiently by adding or removing users from the appropriate groups without modifying folder permissions.

Finally, I validated the configuration by signing in to the Windows 10 domain-joined client using different user accounts and confirming that each user could access only the folders assigned to their department.

---

## Verification

To verify that the file services and shared resources were configured successfully, I confirmed that:

- All shared folders were accessible from the Windows 10 client.
- Users could access only the folders assigned to their department.
- Unauthorized users were denied access to restricted folders.
- Share Permissions and NTFS Permissions worked together as intended.
- Changes to Security Group membership were reflected in user access after signing in again.

These verification steps confirmed that the file-sharing environment was secure, functional, and aligned with the organization's access control requirements.

---

## Outcome

The file server was successfully configured to provide centralized access to departmental resources. Users were able to access shared folders according to their assigned Security Groups, while unauthorized access was effectively restricted.

This implementation demonstrated how centralized identity management and role-based access control work together to improve both security and administrative efficiency within an enterprise environment.

---

## Reflection

This stage reinforced the importance of managing permissions through Security Groups rather than assigning access directly to individual users. This approach follows enterprise best practices by reducing administrative overhead, minimizing configuration errors, and simplifying user management as the organization grows.

It also demonstrated the practical application of the **Principle of Least Privilege**, ensuring that users receive only the permissions necessary to perform their assigned tasks. Applying this principle strengthens security, reduces the risk of accidental modifications, and helps protect sensitive organizational data from unauthorized access.

Testing access from multiple domain user accounts also provided a practical understanding of how Active Directory, Security Groups, Share Permissions, and NTFS Permissions work together to provide secure and centralized resource management.

---

## Screenshots

The following screenshots support this stage:
https://github.com/SheuSec/Enterprise-Active-Directory-Infrastructure-Lab/blob/main/Screenshots/Screenshots%20File-Services-and-Shared-Resources.md.pdf

