Royal Enterprise Home Lab — Implementation Evidence

This directory contains screenshots documenting the configuration, testing, security controls, monitoring, backup and recovery, and centralized event collection implemented within the Royalty.Local enterprise lab environment.

Evidence Guide

The screenshots in this directory are organized in implementation order and provide validation of the major infrastructure, security, monitoring, backup, recovery, and centralized logging capabilities implemented in the Royal Enterprise Home Lab.

Active Directory, DNS & DHCP — Evidence 01–10

Evidence 01–10 documents the core Royalty.Local infrastructure, including Active Directory domain configuration, DNS services, DHCP scope configuration, domain controller health, Organizational Units, domain users, security groups, Group Policy Objects, and SMB file-server configuration.

Web Services & Network Security — Evidence 11–16

Evidence 11–16 documents IIS web-server deployment, the internally hosted Royal Technology Solutions website, Snort intrusion detection configuration and live alert generation, and Microsoft Defender Firewall security controls with validated traffic filtering.

Backup & Recovery — Evidence 17–23

Evidence 17–23 documents the BACKUP01 storage configuration, Veeam Backup & Replication services, dedicated backup repository, successful WEB01 server backup, restore-point availability, file-level recovery, and verification of the restored Royal Technology Solutions website file.

PRTG Infrastructure Monitoring — Evidence 24–34

Evidence 24–34 documents the MON01 monitoring server, PRTG service installation, web console operation, WEB01 availability and website monitoring, CPU and system-health monitoring, BACKUP01 memory and disk monitoring, and centralized visibility across monitored Royalty.Local infrastructure.

Centralized Security Logging — Evidence 35–37

Evidence 35–37 documents centralized Windows Security event collection using Windows Event Collector and Windows Event Forwarding. The evidence demonstrates Security events forwarded from WEB01SERVER.Royalty.Local to DC01, an active collector-initiated subscription with the source computer reporting Active status, and the Windows Event Collector service running automatically.

Final Operational Validation — Evidence 38–40

Evidence 38–40 provides final operational validation of the Royal Enterprise Home Lab. The evidence confirms that the Veeam backup repository remained available and healthy, a new WEB01 backup completed successfully with zero warnings and zero errors, and the complete Royalty.Local virtual server environment is represented in the final infrastructure inventory.

