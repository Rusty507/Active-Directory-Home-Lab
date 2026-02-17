# Active Directory Home Lab

This repository documents a hands-on Active Directory lab built in VirtualBox.
The goal is to simulate enterprise identity infrastructure, implement least-privilege access control, and document identity lifecycle processes using Active Directory.

## Environment
- Oracle VirtualBox
- Windows Server 2022 (Domain Controller)
- Windows client (added later)

## Progress
- Installed Windows Server 2022
- Renamed server to DC01
- Configured basic server settings
- Created restore points using VirtualBox snapshots

## What this shows
- Understanding of Windows server setup
- Awareness of AD prerequisites
- Change control using snapshots
- Clear documentation of system changes

## Next steps
- Configure static IP
- Install Active Directory Domain Services
- Promote DC01 to Domain Controller
- Create users, groups, and OUs
- Join a client machine to the domain





## Initial Server Setup

- Created Windows Server 2022 VM in VirtualBox
- Installed Desktop Experience edition
- Renamed server to DC01
- Rebooted and verified Server Manager
- Took clean snapshot before AD installation

## Progress
### Phase 1 – Identity Infrastructure Design
### Domain Configuration
- Configured static IP (10.0.2.15) for domain controller
- Configured DNS to point to domain controller (self-referential)
- Confirmed DHCP disabled
- Verified network alignment with VirtualBox NAT

### OU Architecture
- Designed structured OU hierarchy under Corporate
- Separated Users, Groups, Workstations, Servers, and Disabled Accounts
- Created department-level OUs (HR, Finance, IT, Sales)
- Avoided use of default Users container for better policy control

### Group Strategy (AGDLP Model)
- Created Global security groups per department
- Created Domain Local groups for resource-level access
- Nested Global groups into Domain Local groups
- Implemented least privilege access modeling

## Architecture Overview
Current Logical Structure:
lab.local
└── Corporate
    ├── Users
    │   ├── HR
    │   ├── Finance
    │   ├── IT
    │   └── Sales
    ├── Groups
    ├── Workstations
    ├── Servers
    └── Disabled_Accounts
## What this shows
- understanding of enterprise OU design
- Implementation of AGDLP access model
- RBAC structure
- Least privilege princples
- Change management via snapshots
