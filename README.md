# Active Directory Enterprise Identity Lab

## Objective
Design and implement a simulated enterprise Active Directory environment that demonstrates identity architecture, least-privilege access control, and lifecycle governance using structured documentation and change control.

## Business Scenario
CorpTech Solutions is a mid-sized organization with 150 employees across four departments:
- HR
- Finance
- IT
- Sales

The company requires:
- Structured OU design
- Role-based access control
- Least privilege enforcement
- Scalable group management
- Identity lifecycle governance

This lab simulates the foundational identity infrastructure for that environment

## Environment
- Oracle VirtualBox
- Windows Server 2022 (Domain Controller - DC01)
- NAT networking
- Domain: lab.local
- Static IP: 10.0.2.15

## Architecture Overview
<pre>lab.local
└── Corporate
    ├── Users
    │   ├── HR
    │   ├── Finance
    │   ├── IT
    │   └── Sales
    ├── Groups
    ├── Workstations
    ├── Servers
    └── Disabled_Accounts </pre>
Design decisions:
- Separated Users, Computers, and Servers for GPO scoping
- Created department OUs for delegation and policy targeting
- Centralized group management in a dedicated Groups OU
- Created Disabled_Accounts OU for lifecycle control

## Access Control Model (AGDLP)
Implemented the AGDLP model:

Accounts -> Global -> Domain Local -> Permissions
- Created department-based Global security groups
- Created resource-based Domain Local groups
- Nested Global groups into Domain Local groups
- Prepared structure for NTFS-based resource control

This enables scalable RBAC modeling and simplifies access auditing.

## Phase 1 Progress
- Configured static IP and DNS [self-referencing]
- Disabled DHCP on DC01
- Installed and promoted AD DS
- Designed structured OU hierarchy
- Implemented AGDLP group strategy
- Established snapshot-based change control

## What This Demonstrates
- Enterprise OU architecture design
- Role-based access modeling
- Least privilege implementation
- Identity structure planning
- Change management discipline
- Documentation clarity

## Repository Structure
Architecture/
Design diagrams and logical models

Implementataion/
Step-by-step configuration documentation

Automation/
PowerShell provisioning scripts [Phase 1 upcoming]

Incidents/
Troubleshooting and root cause analysis scenarios

Screenshots/
Supporting evidence of configuration










- Change management via snapshots
