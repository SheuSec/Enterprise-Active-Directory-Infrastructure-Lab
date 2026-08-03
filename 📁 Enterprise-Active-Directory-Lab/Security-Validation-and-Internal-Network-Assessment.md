# Security Validation and Internal Network Assessment

## Objective

After completing the deployment of the Active Directory environment, the final implementation stage was to validate the infrastructure from a security perspective. Rather than assuming that every service was functioning correctly, I performed a controlled internal network assessment using Kali Linux within the isolated lab environment.

The objective of this assessment was to verify network connectivity, identify the services exposed by the Domain Controller, and confirm that the deployed infrastructure was operating as expected. All testing was conducted within my own virtual lab for educational, administrative, and defensive purposes.

---

## Implementation

To begin the assessment, I connected the Kali Linux virtual machine to the same **Hyper-V Internal Virtual Switch** used by the Windows Server and Windows 10 client. This ensured that all systems were on the same isolated network while remaining separated from the physical production network.

After confirming the network configuration, I verified that Kali Linux could successfully communicate with the Domain Controller. Basic connectivity tests were performed before proceeding with service discovery.

Using **Nmap**, I scanned the Domain Controller to identify active hosts, open ports, and the network services available within the environment. The scan detected services commonly associated with an Active Directory infrastructure, including **DNS**, **Kerberos**, **LDAP**, **SMB**, and **RPC**.

Rather than treating every open port as a security issue, I evaluated the scan results based on the role of the server. Since the system was functioning as a Domain Controller, these services were expected and required to support authentication, directory services, file sharing, and communication between domain-joined devices.

Throughout the assessment, I compared the scan results with the services intentionally deployed during the project to ensure that the infrastructure behaved as expected and that no unnecessary services were exposed.

---

## Verification

To verify that the environment was functioning correctly, I confirmed that:

- Kali Linux successfully communicated with the Domain Controller.
- The Domain Controller responded to network discovery.
- Nmap identified the expected Active Directory services.
- DNS, Kerberos, LDAP, SMB, and RPC services were available.
- No unexpected network services were exposed within the lab environment.

These verification steps confirmed that the deployed infrastructure was operating correctly and that the expected enterprise services were available to authorized systems within the internal network.

---

## Outcome

The internal security assessment confirmed that the Active Directory environment had been deployed successfully and that the required enterprise services were operating as expected.

The assessment also demonstrated that the environment exposed only the services necessary for its intended role, providing additional confidence in the stability, functionality, and security of the deployed infrastructure.

---

## Reflection

This stage reinforced the importance of validating infrastructure after deployment rather than assuming that every configuration is functioning correctly. Deploying enterprise services is only part of a system administrator's responsibility; verifying that those services operate as intended is equally important.

Conducting the assessment using Kali Linux also strengthened my understanding of how Windows Server administration and cybersecurity complement one another. Rather than viewing port scanning solely as an offensive technique, I learned how it can be used defensively to verify deployed services, identify unnecessary exposures, and confirm that enterprise systems are operating according to design.

Completing this assessment provided confidence that the Active Directory environment was not only functional but also correctly configured from both an administrative and security perspective.

---

## Screenshots
The following screenshots support this stage:
https://github.com/SheuSec/Enterprise-Active-Directory-Infrastructure-Lab/blob/main/Screenshots/Screenshots%20Security-Validation-and-Internal-Network-Assessment.md.pdf
