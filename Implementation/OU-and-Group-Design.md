# OU and Group Architecture Design
## Objective
Design a structured Organizational Unit hierarchy and implement a scalable access control model using the AGDLP framework.

## OU Structure

Created structured hierarchy under lab.local:

Corporate:
- Users
  - HR
  - Finance
  - IT
  - Sales
- Groups
- Workstations
- Servers
- Disabled_Accounts

## Design Decisions
### Separation of Object Types
Users, Computers, and Servers were separated to:
- Enable targeted Group Policy application
- Simplify delegation
- Improve administrative clarity

## Deparment-Based User OUs
Created departmental OUs to support:
- Role-based access control
- Policy scoping
- Lifecycle management


## Disabled_Accounts OU
A dedicated OU was created for disabled users to:
- Prevent accidental reactivation
- Enable lifecycle tracking
- Prepare for automated offboarding workflows

## Group Strategy -AGDLP Model
Implemented:

Accounts -> Global -> Domain Local -> Permissions

### Global Groups
Created department-based Global security groups:
- HR_Users_GG
- Finance_Users_GG
- IT_Users_GG
- Sales_Users_GG

Purpose:
Aggregate users by department


## Domain Local Groups
Created resrouce-level Domain Local groups:
- HR_File_RW_DL
- Finance_File_RW_DL
- IT_File_RW_DL
- Sales_File_RW_DL

Purpose:
Assign permissions to resources without modifying user memberships directly.

## Group Nesting
Nested Global groups into corresponding Domain Local groups.

This enables:
- Scalable access management
- Simplified auditing
- Centralized permission control

## Security Considerations
- Avoided direct permission assignment to user accounts
- Implemented role-based access grouping
- Structured design supports least privilege enforcement
- Prepared for scalable resource-based access control

## Validation
- Confirmed group nesting via ADUC
- Verified users are members of Global groups
- Confirmed Global groups are memberships of Domain Local groups







