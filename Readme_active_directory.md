# Active-Directory--Simulation  
Active Directory- Simulation  
# Active Directory Simulation – 'Cybertech Corporate Services'  
This project is the deployment of a Windows Server Domain Controller (Active Directory) for a company called \*\*Cybertech Corporate Services\*\*. It includes domain setup, client configuration, OU design, group policies, and access control in an enterprise environment.

---

## Company Overview/ Operating System

**Cybertech Corporate Service\*\* is a small Management consultancy activities other than financial management. The following are its structure:

- 1 x Windows Server (AD Domain Controller)  
- 1 x Windows 8 Client PC (HR)  
- 1 x Windows 8 Client PC (IT)

---

\#\# Project Objectives

\- Configure an AD Domain Controller on Windows Server  
\- Join client PCs to the domain  
\- Create Organizational Units (OUs)  
\- Implement basic Group Policies for access control  
\- Simulate a centralized IT environment

\---  
\#\# Network Design

\`\`\`  
Internet  
   ↓  
Router (Gateway: 10.0.2.1)  
   ↓  
Switch  
 ┌──────┬─────────────┬──────────────┐  
 │      │             │              │  
Server  PC1 (Win 8\)   PC2 (Win 8\)  
\`\`\`

| Device        | IP Address      | Role                        |  
|---------------|----------------|-----------------------------|  
| Windows Server| 10.0.2.3  | AD Domain Controller (DC)   |  
| Windows 8 PC  | DHCP    | Client (HR)           |  
| Windows 8 PC  | DHCP    | Client (IT)               |

\---

\#\# Domain Configuration

\- \*\*Domain Name\*\*: \`cybertech.local\`  
\- \*\*Server Name\*\*: \`CYBERTECH\`  
\- \*\*Static IP\*\*: \`10.0.2.3\`  
\- \*\*AD Roles Installed\*\*: AD DS, DNS (DHCP)  
\---

\#\# Organizational Units (OUs)

Created using \*\*Active Directory Users and Computers\*\*:

\`\`\`  
cybertech.local  
├── OU: HR Team  
│   └── Users: kim.HR  
    

├── OU: IT  
│   └── Users:alex.IT  
\`\`\`

\---  
\#\# Group Policy (GPO)

Created and linked using \*\*Group Policy Management Console (gpmc.msc)\*\*:

\- \*\*GPO Name\*\*: \`Real disable restart\`  
\- \*\*Linked to\*\*: OU: HR Department  
\- \*\*Policy Configured\*\*:  
  \- \`User Configuration\` \> \`Policies\` \> \`Administrative Templates\` \> \`Start Menu and Taskbar\` \> \`Remove and Prevent Access to the Shut Down, Restart, Sleep and Hibernate commands\`  
  \- Set \*\*"Remove and Prevent Access to the Shut Down, Restart, Sleep and Hibernate commands"\*\* to \*\*Enabled\*\*

Result: Access to shutdown, restart, sleep and hibernate are disabled for all users in the \*\*Accounts OU\*\*.

\---  
\#\# Screenshots

\- AD Domain Structure  
\- GPO Editor Screenshot  
\- PC joined to domain  
\- Result of access denied to shutdown, restart, sleep and hibernate

\---

\#\# Key Takeaways

\- Gained practical experience with Windows Server roles and domain setup  
\- Implemented centralized access control using Group Policy  
\- Learned how to structure users and departments with OUs  
\- Applied IAM concepts in a real-world simulated environment

\---

\#\# Author

\*\*Olaniran Andrew Oladimeji\*\*    
Cybersecurity Analyst   
