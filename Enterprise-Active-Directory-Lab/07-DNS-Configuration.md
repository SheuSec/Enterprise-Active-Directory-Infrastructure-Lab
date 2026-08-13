# Configuring Domain Name System (DNS)

## Objective

After successfully deploying Active Directory Domain Services (AD DS), the next step was to configure and verify the **Domain Name System (DNS)** service required for the Active Directory environment.

DNS is a critical component of Active Directory because domain clients rely on DNS to locate the Domain Controller and access services provided by the domain.

The objective of this stage was to configure DNS for the **olalab.local** domain, verify the required DNS records, and ensure that the Windows 10 client could successfully resolve the domain and communicate with the Domain Controller.

---

## Implementation

I began by opening **Server Manager** and verifying that the **DNS Server** role was installed on the Windows Server 2022 Domain Controller.

Because DNS is closely integrated with Active Directory Domain Services, the DNS configuration was reviewed after the domain controller was successfully promoted and the **olalab.local** domain had been created.

I opened the **DNS Manager** console through:

**Server Manager → Tools → DNS**

Within DNS Manager, I verified the **Forward Lookup Zones** and confirmed that a DNS zone for the **olalab.local** domain was available.

The forward lookup zone provides name resolution by translating domain hostnames into their corresponding IP addresses.

I then reviewed the DNS records associated with the domain and confirmed that the Domain Controller had the required records for the Active Directory environment.

The DNS configuration was also checked to ensure that the Windows 10 client would use the Domain Controller as its preferred DNS server rather than an external DNS server.

On the Windows 10 client, I used the following command to review the current network configuration:

ipconfig /all
The DNS server information was checked to confirm that the client was pointing to the internal DNS server provided by the Windows Server 2022 Domain Controller.

DNS Resolution Testing

After configuring the DNS service, I tested name resolution from the Windows 10 client.

The nslookup command was used to verify that the client could communicate with the configured DNS server:

nslookup

I then tested the olalab.local domain:

nslookup olalab.local

The response was reviewed to confirm that the domain could be resolved successfully through the internal DNS server.

I also tested connectivity to the Domain Controller using its IP address to confirm that the underlying network connection was functioning correctly.

ping <Domain-Controller-IP>

These tests helped verify both network connectivity and DNS name resolution within the laboratory environment.

DNS Cache Verification

The DNS cache on the Windows 10 client was also reviewed using:

ipconfig /displaydns

This command displayed DNS records currently stored in the local resolver cache.

When required, the DNS cache could be cleared using:

ipconfig /flushdns

After clearing the cache, DNS resolution was tested again to ensure that the client could obtain fresh DNS information from the configured internal DNS server.

Active Directory DNS Records

I also reviewed the DNS records associated with the olalab.local domain.

Active Directory uses special DNS service records to allow clients to locate domain controllers and other domain services.

The presence of these records was important because they support functions such as:

Domain controller discovery
Domain authentication
Active Directory service location
Group Policy processing
Domain joining

The DNS configuration was therefore treated as a core dependency of the Active Directory environment rather than simply a general network service.

Verification

To verify that DNS was functioning correctly, I confirmed that:

The DNS Server role was installed on Windows Server 2022.
The olalab.local DNS zone was available.
The Domain Controller had the required DNS records.
The Windows 10 client was configured to use the internal DNS server.
The Windows 10 client could communicate with the DNS server.
The olalab.local domain could be resolved successfully.
DNS resolution supported communication with the Active Directory environment.

These verification steps confirmed that DNS was functioning correctly and was ready to support the remaining domain infrastructure.

Outcome

The DNS configuration was successfully completed and verified for the olalab.local Active Directory environment.

The Windows Server 2022 Domain Controller provided the internal DNS service required by the domain, while the Windows 10 client was configured to use the internal DNS server for domain name resolution.

With DNS functioning correctly, the environment was prepared for the next stage of network infrastructure deployment: DHCP configuration.

Reflection

Configuring DNS demonstrated the important relationship between DNS and Active Directory.

Before this project, DNS could be viewed simply as a service used to translate domain names into IP addresses. However, during the Active Directory deployment, it became clear that DNS performs a much more important role in a Windows domain environment.

Active Directory relies on DNS for locating domain controllers and discovering domain services. A client using an incorrect DNS server can therefore experience problems with domain authentication, domain joining, Group Policy, and other Active Directory functions.

Successfully testing DNS resolution against the olalab.local domain provided practical experience with one of the most important dependencies in a Windows enterprise environment.

Screenshots
The following screenshots support this stage:
