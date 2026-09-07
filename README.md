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
