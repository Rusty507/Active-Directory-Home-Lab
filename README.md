# Active Directory Home Lab

This repository documents a hands-on Active Directory lab built in VirtualBox.
The goal is to simulate enterprise identity infrastructure, implement least privilege access control, and document identity lifecycle processes using Active Directory.

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
- Installed Active Directory Domain Services role on DC01 (pre-domain promotion)

- Promoted DC01 to a Domain Controller and created a new Active Directory forest (lab.local)

