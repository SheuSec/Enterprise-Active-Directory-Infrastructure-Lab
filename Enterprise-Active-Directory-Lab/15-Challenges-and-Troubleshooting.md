# Challenges Encountered and Troubleshooting

## Overview

No infrastructure deployment is completely free of challenges, and this project was no exception. Throughout the implementation process, I encountered several technical issues that required careful investigation before the environment functioned as expected.

Rather than viewing these issues as setbacks, I approached each one using a structured troubleshooting process. Identifying the root cause, implementing the appropriate solution, and validating the outcome strengthened both my Windows Server administration skills and my understanding of enterprise networking.

The following sections summarize the major challenges encountered during the deployment and how they were resolved.

---

## Challenge 1 — Virtual Machine Network Connectivity

### Problem

The virtual machines were initially unable to communicate with one another because they were connected to different virtual network configurations.

### Root Cause

No common Hyper-V virtual switch had been configured for the lab environment.

### Resolution

I created a **Hyper-V Internal Virtual Switch** and connected the Windows Server 2022, Windows 10, and Kali Linux virtual machines to the same isolated network.

### Result

All virtual machines successfully communicated with one another, providing the networking foundation required for the remainder of the deployment.

---

## Challenge 2 — Internet Access for the Lab Environment

### Problem

Although the virtual machines could communicate internally, they were unable to access the internet.

### Root Cause

An Internal Virtual Switch does not provide external connectivity by default.

### Resolution

I configured **Network Address Translation (NAT)** on the Hyper-V host and assigned the appropriate gateway configuration.

### Result

The virtual machines gained controlled internet access while remaining isolated from the physical network.

---

## Challenge 3 — Domain Authentication Issues

### Problem

Some domain users were unable to authenticate after Active Directory deployment.

### Root Cause

User account configuration and credentials required verification.

### Resolution

I reviewed the user accounts in **Active Directory Users and Computers (ADUC)**, reset passwords where necessary, confirmed that accounts were enabled, and verified account properties.

### Result

Domain users authenticated successfully using their Active Directory credentials.

---

## Challenge 4 — Windows 10 Failed to Join the Domain

### Problem

The Windows 10 client initially failed to locate the Domain Controller during the domain join process.

### Root Cause

Incorrect network configuration prevented the client from locating the Domain Controller through DNS.

### Resolution

I verified the DHCP configuration, confirmed the assigned IP address, and ensured that the preferred DNS server pointed to the Domain Controller.

### Result

The Windows 10 client successfully joined the **olalab.local** domain.

---

## Challenge 5 — Group Policy Not Applying

### Problem

The configured Group Policies did not appear to apply immediately to the Windows 10 client.

### Root Cause

The client had not yet refreshed its Group Policy settings.

### Resolution

I refreshed the policies using:

```powershell
gpupdate /force
```

I then verified the applied policies using:

```powershell
gpresult /r
```

### Result

The configured password policies, account lockout policies, and interactive logon message were successfully applied.

---

## Challenge 6 — Shared Folder Permission Issues

### Problem

Some users could see shared folders but were unable to access them.

### Root Cause

Share Permissions and NTFS Permissions were not configured consistently.

### Resolution

I reviewed both permission models and assigned access through the appropriate Active Directory Security Groups.

### Result

Authorized users successfully accessed departmental resources, while unauthorized users remained restricted.

---

# Key Lessons Learned

Resolving these challenges reinforced several important principles of enterprise infrastructure deployment:

- Proper network design is essential before deploying server roles.
- DNS is one of the most critical services in an Active Directory environment.
- Infrastructure servers should always use static IP addressing.
- Security Groups simplify permission management and improve scalability.
- Group Policy changes should always be verified after deployment.
- Effective troubleshooting requires identifying the root cause rather than relying on trial and error.
- Careful validation after each deployment stage significantly reduces configuration issues later in the project.

---

# Reflection

One of the most valuable outcomes of this project was learning that successful infrastructure deployment is not simply about installing services—it is about understanding how those services interact and systematically resolving issues when they arise.

Each challenge improved my ability to diagnose problems, interpret system behavior, and implement effective solutions. Working through these issues strengthened my practical experience with Windows Server administration, Active Directory, DNS, DHCP, file services, Group Policy, and enterprise troubleshooting.

By the end of the project, I had not only built a fully functional Active Directory environment but also developed greater confidence in my ability to troubleshoot and support enterprise Windows infrastructure in real-world environments.




