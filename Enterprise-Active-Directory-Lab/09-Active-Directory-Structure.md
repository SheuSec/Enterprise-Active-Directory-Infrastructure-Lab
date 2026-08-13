# Designing the Active Directory Structure

## Objective

With the core infrastructure services successfully deployed, the next stage was to organize the Active Directory environment into a logical and manageable structure. A well-designed directory simplifies administration, strengthens security, and enables policies to be applied to specific users and computers without affecting the entire domain.

The objective of this stage was to create Organizational Units (OUs), configure domain user accounts, and organize users into security groups based on their roles. This approach reflects the administrative practices commonly used in enterprise environments.

---

## Implementation

I began by opening **Active Directory Users and Computers (ADUC)** from the Windows Administrative Tools. Rather than storing all objects in the default containers, I created dedicated **Organizational Units (OUs)** to represent the different departments within the organization.

Creating Organizational Units provided a logical directory structure that simplified administration and prepared the environment for department-specific Group Policy deployment in later stages of the project.

After creating the Organizational Units, I added domain user accounts for each department. Every user was assigned a unique username and a secure password that complied with the domain password policy.

To simplify access management, I created **Security Groups** based on departmental responsibilities. Instead of assigning permissions directly to individual users, I added each user to the appropriate security group. This follows the principle of **Role-Based Access Control (RBAC)**, making permission management more efficient and scalable as the organization grows.

Finally, I reviewed the Active Directory hierarchy to ensure that Organizational Units, user accounts, and security groups were correctly organized and reflected the intended enterprise structure.

---

## Verification

To verify that the Active Directory structure was configured successfully, I confirmed that:

- All Organizational Units were created successfully.
- User accounts were placed in the correct Organizational Units.
- Security Groups were created for each department.
- Users were assigned to the appropriate Security Groups.
- The Active Directory hierarchy reflected the planned organizational structure.

These verification steps confirmed that the directory was properly organized and ready for centralized administration and policy management.

---

## Outcome

The Active Directory environment was successfully organized into a structured and scalable directory. Organizational Units, domain user accounts, and Security Groups were configured to reflect departmental roles and administrative requirements.

This provided a clean foundation for assigning permissions, deploying Group Policy Objects (GPOs), and managing users efficiently throughout the enterprise environment.

At this stage, the domain had evolved beyond basic infrastructure deployment into a realistic enterprise directory structure.

---

## Reflection

This stage demonstrated that Active Directory is much more than a collection of user accounts. The way users, groups, and organizational units are structured directly affects administration, security, and scalability.

Using Organizational Units enables administrators to delegate management responsibilities and apply policies to specific departments without impacting the rest of the organization. Likewise, assigning permissions through Security Groups rather than individual user accounts follows industry best practices and significantly simplifies ongoing administration.

Building the directory structure also highlighted the importance of planning. Organizing users according to business functions during deployment makes future tasks—such as permission management, resource sharing, and Group Policy implementation—far more efficient.

---

## Screenshots

The following screenshots support this stage:
https://github.com/SheuSec/Enterprise-Active-Directory-Infrastructure-Lab/blob/main/Screenshots/Screenshots%20Active-Directory-Structure.pdf

