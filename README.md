# Royal Enterprise Home Lab

## Enterprise Infrastructure, Cybersecurity & Network Defense

The Royal Enterprise Home Lab is a multi-server virtual enterprise environment designed, implemented, secured, monitored, and maintained as a hands-on cybersecurity and systems administration project.

The lab is built around the **Royalty.Local** Active Directory domain and simulates the infrastructure of a small-to-mid-sized organization. It integrates centralized identity and access management, DNS and DHCP services, web hosting, host-based firewall controls, intrusion detection, infrastructure monitoring, centralized Windows event collection, and enterprise backup and recovery.

Rather than demonstrating isolated technologies, this project focuses on how multiple infrastructure and security services work together within a functioning Windows and Linux environment.

### Core Technologies

- Windows Server 2025
- Windows 10
- Active Directory Domain Services (AD DS)
- DNS and DHCP
- Group Policy
- Internet Information Services (IIS)
- Microsoft Defender Firewall
- Snort IDS
- PRTG Network Monitor
- Windows Event Collector / Windows Event Forwarding
- Veeam Backup & Replication Community Edition
- Ubuntu Server
- Oracle VirtualBox
- PowerShell

 ## Project Objectives

The objective of this project was to design and operate a realistic enterprise lab where infrastructure, security, monitoring, and recovery technologies could be implemented and validated together.

Key objectives included:

- Build and administer a centralized Active Directory domain environment.
- Configure DNS and DHCP services for enterprise network resource management.
- Organize users, computers, security groups, and Organizational Units within Active Directory.
- Implement and manage Group Policy Objects (GPOs).
- Deploy an IIS web server hosting the Royal Technology Solutions website.
- Apply host-based firewall policies and validate allowed and blocked network traffic.
- Deploy Snort to detect network activity and generate IDS alerts.
- Monitor server availability, performance, disk capacity, and web services with PRTG.
- Centralize Windows Security events using Windows Event Collector and Windows Event Forwarding.
- Implement Veeam server backup, repository management, and file-level recovery.
- Test configurations and security controls to verify that they operate as intended.
- Document implementation, validation, troubleshooting, and recovery procedures.

- Lab Architecture & Server Roles

The Royalty.Local environment uses multiple virtual machines with dedicated infrastructure, security, monitoring, backup, and client roles.

DC01 — Primary Active Directory Domain Controller and DNS

BDC01 — Secondary Domain Controller

DNS01 — Dedicated DNS Server

DHCP — Dedicated DHCP Server

WEB01 — IIS Web Server hosting the Royal Technology Solutions website

FW_01 — Windows Server host-based firewall and security policy testing

IDS/IPS Ubuntu — Ubuntu Server running Snort IDS

MON01 — PRTG Network Monitoring Server

Veeam Backup Server — Veeam Backup & Replication and backup repository

Windows 10 Client — Domain client used for authentication, DNS, connectivity, and service testing

## Security Architecture

The lab uses multiple layers of security controls to protect systems, detect suspicious activitiy, restrict network access, and provide centralized visibility into windows security events.

Identity and Access Management: Active Directory provides centralized authentication, user and group administration, Organizational Units, and Group Policy management.

Host Firewall Security: Microsoft Defender Firewall is configured with a default inbound-block policy and custom rules to permit authorized traffic while restricting selected network connections.

Intrusion Detection: Snort monitors network traffic and generates alerts when configured detection rules are triggered.

Centralized Security Logging: Windows Event Collector and Windows Event Forwarding centralize Windows Security events from monitored systems for auditing and investigation.

Infrastructure Monitoring: PRTG monitors server availability, CPU, memory, disk capacity, and web-service availability.

Data Protection: Veeam Backup & Replication provides server backup, repository management, restore points, and tested file-level recovery.

Identity and Access Management: Active Directory provides centralized authentication, user and group administration, Organizational Units, and Group Policy management.

Host Firewall Security: Microsoft Defender Firewall is configured with a default inbound-block policy and custom rules to permit authorized traffic while restricting selected network connections.

Intrusion Detection: Snort monitors network traffic and generates alerts when configured detection rules are triggered.

Centralized Security Logging: Windows Event Collector and Windows Event Forwarding centralize Windows Security events from monitored systems for auditing and investigation.

Infrastructure Monitoring: PRTG Network Monitor provides centralized visibility into server availability, CPU utilization, memory, disk capacity, and web-service availability.

Data Protection and Recovery: Veeam Backup & Replication provides server backup, dedicated repository management, restore points, and tested file-level recovery.

Implementation & Validation

Each major component of the Royal Enterprise Home Lab was configured and tested to verify functionality. Validation included Active Directory and DNS health checks, DHCP scope verification, web-service testing, firewall rule enforcement, live IDS detection, infrastructure monitoring, backup and recovery testing, and centralized Windows Security event collection.

Active Directory & Identity Services

The Royalty.Local domain was validated through Active Directory health checks and administrative testing. The environment includes domain controllers, Organizational Units, user accounts, security groups, and Group Policy Objects used to provide centralized identity and access management.

DNS & DHCP Services

DNS resolution was validated for internal Royalty.Local resources, including the WEB01 web server. DHCP was configured as a dedicated network service with an active IPv4 scope and network configuration options for client systems.

Active Directory & Identity Services

The Royalty.Local domain was validated through Active Directory health checks and administrative testing. The environment includes domain controllers, Organizational Units, user accounts, security groups, and Group Policy Objects used to provide centralized identity and access management.

DNS & DHCP Services

DNS resolution was validated for internal Royalty.Local resources, including the WEB01 web server. DHCP was configured as a dedicated network service with an active IPv4 scope and network configuration options for client systems.

Snort Intrusion Detection

An Ubuntu Server running Snort was configured as a network intrusion detection system. Snort was configured with the Royal lab network as its HOME_NET, and a custom ICMP detection rule was created and tested. Live traffic generated from another system successfully triggered Snort alerts, demonstrating real-time network traffic detection.

PRTG Infrastructure Monitoring

PRTG Network Monitor was deployed on MON01 to provide centralized infrastructure monitoring. WEB01 and BACKUP01 were monitored for availability and system health using sensors for ping, CPU utilization, memory, disk capacity, and web-service availability. The Royal Technology Solutions website was also monitored through an HTTP sensor to verify application availability.

Veeam Backup & Recovery

Veeam Backup & Replication Community Edition was deployed on BACKUP01 with a dedicated backup repository. WEB01 was protected using an agent-based backup job, and successful backup operations were verified. File-level recovery was also tested by restoring the Royal Technology Solutions website file from a backup restore point. After repository storage maintenance, the repository was revalidated and a new WEB01 backup completed successfully with zero warnings and zero errors.

Centralized Windows Event Collection

Windows Event Collector was configured on DC01 to centralize Windows Security events from WEB01SERVER.Royalty.Local. A collector-initiated subscription was implemented using Windows Event Forwarding, and the source computer reached an Active state. Forwarded Security events, including successful logon, logoff, and special-logon activity, were received in the Forwarded Events log, validating centralized security-event collection.

Implementation Evidence

The following screenshots document the configuration, testing, and validation performed throughout the Royal Enterprise Home Lab.

Key Skills Demonstrated

This project demonstrates hands-on experience across enterprise systems administration, cybersecurity, network services, monitoring, and disaster recovery.

Then add these lines underneath:

Windows Server Administration: Active Directory Domain Services, DNS, DHCP, Group Policy, SMB services, IIS, Windows Event Collection, and PowerShell administration.

Cybersecurity: Identity and access management, host-based firewall configuration, traffic filtering, Snort intrusion detection, security-event monitoring, and centralized Windows Security logging.

Network Administration: TCP/IP configuration, internal DNS resolution, DHCP address management, service connectivity testing, ICMP testing, and network troubleshooting.

Monitoring & Observability: PRTG deployment and administration, availability monitoring, CPU and memory monitoring, disk-capacity monitoring, and HTTP service monitoring.

Backup & Recovery: Veeam Backup & Replication, dedicated repository configuration, server backup operations, restore-point management, and tested file-level recovery.

Virtualization: Multi-server enterprise lab deployment and administration using Oracle VirtualBox with both Windows Server and Ubuntu Server systems.

Troubleshooting & Lessons Learned

Building the Royal Enterprise Home Lab required troubleshooting across multiple infrastructure layers. Several issues provided opportunities to apply structured diagnostic methods and validate solutions rather than simply changing configurations until a service worked.

DNS & Service Connectivity: Internal name-resolution and connectivity issues were diagnosed using tools such as Resolve-DnsName, Test-NetConnection, ping, and PowerShell. Testing helped isolate DNS configuration and firewall-related connectivity problems between systems.

Veeam Remote Access: WEB01 initially could not be accessed successfully by Veeam for backup management. Testing identified blocked SMB connectivity, and the required inbound SMB firewall rule was enabled. TCP port 445 connectivity and Veeam credential access were then successfully validated.

Backup Storage Recovery: BACKUP01 experienced a storage configuration issue involving the dedicated Veeam repository disk. The disk configuration was corrected, the NTFS repository volume was verified, Veeam recognized the repository again, and a fresh WEB01 backup completed successfully with zero warnings and zero errors.

PRTG Monitoring: Monitoring required troubleshooting ICMP, Windows management access, and individual sensor configurations. Rather than disabling firewall protection broadly, specific required traffic was enabled and monitoring was validated through successful PRTG sensors.

Windows Event Forwarding: Centralized Security event collection required troubleshooting subscription status, WinRM connectivity, event-log permissions, and Security-channel access. The final configuration successfully forwarded Windows Security events from WEB01SERVER.Royalty.Local to DC01.

Key Lesson: Successful infrastructure administration depends on validating each layer independently—name resolution, network connectivity, firewall access, authentication, service availability, permissions, and application configuration—before assuming the source of a failure.

Security Limitations & Future Enhancements

The Royal Enterprise Home Lab is designed as a controlled learning and testing environment rather than a production network. Current security capabilities were documented according to what was actually implemented and validated.

Current Limitations: FW_01 currently demonstrates Windows Server host-based firewall policy rather than a dual-interface perimeter firewall. Snort has been validated as an intrusion detection system (IDS), but inline intrusion prevention and automated traffic blocking have not been implemented. Windows Event Forwarding provides centralized Security event collection but does not provide the correlation, analytics, and response capabilities of a full SIEM platform.

Future Enhancements: Planned improvements include deploying a dedicated perimeter firewall, implementing network segmentation and VLANs, expanding Snort monitoring capabilities, integrating centralized logs with a SIEM platform, strengthening least-privilege administration, expanding Windows Event Forwarding coverage to additional servers, and developing additional automated monitoring and response capabilities.

Security Hardening: Future iterations can also incorporate dedicated administrative accounts, stronger service-account separation, additional Group Policy security baselines, expanded auditing, and further firewall rule refinement.

This section is valuable because we're not pretending the lab does things we haven't built. It tells an experienced infrastructure or cybersecurity recruiter that you understand the difference between IDS vs. IPS, host firewall vs. perimeter firewall, and centralized logging vs. SIEM.

Implementation Evidence

Detailed screenshots documenting the configuration, testing, and validation of this environment are available in the [Evidence Guide](evidence/README.md).

Project Summary

The Royal Enterprise Home Lab demonstrates the design, implementation, administration, security, monitoring, and recovery of a multi-server enterprise environment. The project combines Windows and Linux systems with centralized identity services, network services, web hosting, intrusion detection, firewall controls, infrastructure monitoring, enterprise backup and recovery, and centralized security-event collection.

More importantly, the environment was tested as an integrated system. Services were validated from client and server perspectives, security controls were tested for expected behavior, monitoring was configured against live systems, backups and restoration were performed, and infrastructure issues were diagnosed and corrected through hands-on troubleshooting.

Author

LaVon Thomas
B.S. Computer Information Systems — Cybersecurity
Post University
