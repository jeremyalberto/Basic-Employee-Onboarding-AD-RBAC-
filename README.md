# Basic Employee Onboarding (AD)(RBAC)

## Problem Statement
Northstar Medical Group's Active Directory was left in bad shape after years of mismanagement by their previous MSP. There was no real structure: no department OUs, no consistent security groups, and accounts were set up by hand with no naming standard. Because access was handed out manually and inconsistently, users ended up with the wrong permissions or missing the ones they needed. For a medical group that handles patient and employee data, that is a real HIPAA risk, since nobody could clearly say who had access to what.

## Solution Overview
I rebuilt the environment from scratch by standing up a new Windows Server domain controller and creating the NMG.com domain. I then designed a department based OU structure (Finance, HR, IT, Operations) so each department can get its own policies. Inside each OU I created a Global Security group (Finance-Users, HR-Users, IT-Users, Operations-Users) and used a flat RBAC model where access is granted to the group, not to individual users. I provisioned 15 user accounts using a consistent naming convention (first initial + last name, UPN of username@NMG.com) with department and job title filled in. Finally, I worked a support ticket (NMG-0047) where a user was misplaced, and used it to recommend a more controlled provisioning process for new hires.

## Video Walkthrough
[Video walkthrough coming soon]

## Tools Used
* Windows Server 2022
* Active Directory Domain Services
* Active Directory Users and Computers
* VMware
* RBAC
* GitHub

## Project Timeline
* Day 1: Domain creation and domain controller promotion
* Day 2: Organizational unit and security group design
* Day 3: User provisioning and RBAC implementation
* Day 4: Incident response and resolution (NMG-0047)
* Day 5: Documentation and case study packaging

## Key Accomplishments
* Built NMG.com domain from scratch
* Designed department based OU structure (Finance, HR, IT, Operations)
* Implemented RBAC with security groups mapped to each department
* Provisioned 15 user accounts with consistent naming conventions and attribute standards
* Diagnosed and resolved a multi-cause access issue (wrong OU + wrong group membership)
* Documented full incident resolution with root cause analysis and a process improvement recommendation

## Repository Structure
| Folder | Contents |
| :--- | :--- |
| `/Documentation` | Domain config, OU and security group documentation, full user list, and the RBAC structure map |
| `/Screenshots` | Proof of work from Days 1 through 4, named by day and step |
| `/Incident-Reports` | NMG-0047 resolution write up (root cause, fix, verification) |

## Screenshots
| Day | File | Shows |
| :--- | :--- | :--- |
| 1 | Day1-NMG-Domain-Created.png | NMG.com in AD Users and Computers |
| 1 | Day1-Server-Manager-ADDS.png | AD DS and DNS roles installed |
| 2 | Day2-All-OUs.png | Finance, HR, IT, Operations OUs |
| 2 | Day2-Finance-Users-Group.png | Finance-Users group in Finance OU |
| 2 | Day2-HR-Users-Group.png | HR-Users group in HR OU |
| 2 | Day2-IT-Users-Group.png | IT-Users group in IT OU |
| 2 | Day2-Operations-Users-Group.png | Operations-Users group in Operations OU |
| 3 | Day3-Finance-OU-Users.png | Finance users in Finance OU |
| 3 | Day3-HR-OU-Users.png | HR users in HR OU |
| 3 | Day3-IT-OU-Users.png | IT users in IT OU |
| 3 | Day3-Operations-OU-Users.png | Operations users in Operations OU |
| 3 | Day3-Finance-Users-Members.png | Finance-Users membership |
| 3 | Day3-HR-Users-Members.png | HR-Users membership |
| 3 | Day3-IT-Users-Members.png | IT-Users membership |
| 3 | Day3-Operations-Users-Members.png | Operations-Users membership |
| 3 | Day3-Final-Expanded-Tree.png | Full NMG.com tree with all users and groups |
| 4 | Day4-Jane-Wrong-OU.png | Jane Cooper sitting in the Operations OU |
| 4 | Day4-Jane-Wrong-GroupMembership.png | Jane in Operations-Users instead of HR-Users |
| 4 | Day4-Jane-Fixed-OU.png | Jane moved into the HR OU |
| 4 | Day4-Jane-Fixed-GroupMembership.png | Jane now in HR-Users |
