# Security Group Doc (Day 2)

- Domain name: NMG.com
- OUs created: Finance, HR, IT, Operations
- Security groups created (Global, Security): Finance-Users, HR-Users, IT-Users, Operations-Users

## Purpose of each OU
| OU | Security Group | Purpose |
| :--- | :--- | :--- |
| Finance | Finance-Users | Finance department that reviews financial records, audits invoices, and approves financial requests |
| HR | HR-Users | HR department that reviews payroll entries, manages schedules, submits new employee account requests, and processes exiting employee requests |
| IT | IT-Users | IT department that manages systems, performs password resets, completes service request tickets, and adjusts permissions and user groups |
| Operations | Operations-Users | Manages logistics and supply chain, and coordinates with other departments to maintain facilities |

## Questions
**Why would you put a user in the Finance OU instead of the HR OU?**
You put them in the Finance OU if they are part of the finance department. They need the policies applied to finance users, and once they are added to Finance-Users they get access to the folders and software licenses assigned to that group.

**What happens when you add a user to the Finance-Users security group?**
They get all the permissions assigned to that group and receive access to the finance specific files and software.

**If you wanted Finance users to have access to a Finance shared drive, which group would you use?**
Finance-Users.

**Why is it better to manage access through security groups instead of individually?**
It makes provisioning more automatic. Instead of giving someone access to 5 different systems manually, they get all of it by being added to the group. It also makes deprovisioning simpler when someone changes departments or leaves the company.
