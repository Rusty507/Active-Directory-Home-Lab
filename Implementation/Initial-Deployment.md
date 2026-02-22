# Initial Deployment- Domain Controller Configuration

## Objective
Deploy and configure a Windows Server 2022 domain controller to establish the foundation for enterprise identity services.


## Environment
- Hypervisor: Oracle VirtualBox
- Network Mode: NAT
- Server Name: DC01
- Domain Name: lab.local

## Infrastructure Configuration
### Server Preparation
- Installed Windows Server 2022 (Desktop Experience)
- Renamed server to DC01
- Rebooted to apply hostname change

## Static IP Configuration

Configured static IPV4 settings:
- IP Address: 10.0.2.15
- Subnet Mask: 255.255.255.0
- Default Gateway: 10.0.2.2
- Preferred DNS Server: 10.0.2.15
DHCP was disabled to prevent dynamic address changes.

Reasoning:
Active Directory depends on reliable DNS resolution. A dynamic IP could cause authentication failures, kerberos issues, and domain join instability.

##Active Directory Domain Services Installation
- Installed AD DS role via Server Manager
- Promoted DC01 to Domain Controller
- Created new forest: lab.local

## Validation
Verified successful deployment by confirming:
- SYSVOL share present
- NETLOGON share present
- Domain accessible via Active Directory Users and Computers

## Change Control 
Created VirtualBox snapshot:
Post-OU-and-Group-Design

This proves rollback capability before implementation access control configurations.








