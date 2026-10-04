# Role-Based Access Control (RBAC) Structure

| Department | Organizational Unit (OU) | Security Group Name | Assigned Users (Usernames) | Access Level / Permissions |
| :--- | :--- | :--- | :--- | :--- |
| Finance | OU=Finance,DC=NMG,DC=com | Finance-Users | dchen, kmills, rhayes, lpark | Access to Finance files, payroll systems, and departmental share drives |
| HR | OU=HR,DC=NMG,DC=com | HR-Users | storres, jwhitfield, mgrant, jcooper | Access to employee records, payroll systems, benefits portal, and onboarding documentation |
| IT | OU=IT,DC=NMG,DC=com | IT-Users | mjohnson, ppatel, tbrooks, acoleman | Domain administration, service desk systems, and core network configuration access |
| Operations | OU=Operations,DC=NMG,DC=com | Operations-Users | bfoster, crivera, nross | Access to facility controls, scheduling applications, and logistics shared folders |

Note: jcooper (Jane Cooper) was originally placed in the Operations OU and Operations-Users group. She was moved to HR as part of ticket NMG-0047. See `/Incident-Reports`.
