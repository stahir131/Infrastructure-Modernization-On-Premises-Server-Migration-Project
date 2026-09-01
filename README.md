🚀 **Infrastructure Modernization & On-Premises Server Migration Project**

Recently, I completed an infrastructure modernization project for a school that was running a traditional on-premises environment consisting of two Hyper-V virtual machines:

VM1: Domain Controller — Active Directory, DNS, DHCP, FSMO roles, and Group Policy

VM2: File Server — Shared folders, Folder Redirection, and Print Services

The objective was to modernize the environment, improve redundancy, move file services toward the cloud, and retire the legacy infrastructure while keeping business disruption to a minimum.

### 🔹 Infrastructure & Active Directory Migration

I deployed and configured a new **HP Proliant server with RAID 1** for disk redundancy and configured **iLO** for remote management.

The new server was promoted to a Domain Controller, and I migrated the critical Active Directory services and roles from the legacy server, including:

✅ FSMO roles
✅ DHCP
✅ DNS
✅ Active Directory
✅ Group Policy
✅ Entra Connect synchronization

### 🔹 File Server → Microsoft 365 Migration

One of the major components of the project was moving the customer's traditional file-server architecture toward cloud-based file management.

I migrated shared data from the legacy file server to **SharePoint Online** for the management team, with appropriate permissions configured for users and groups. Where appropriate, faculty data was migrated to **Google Shared Drives**.

The migration was performed using the **SharePoint Migration Tool**, allowing the organization's data to be moved while maintaining the required access structure.

### 🔹 Folder Redirection → OneDrive

The existing user Folder Redirection architecture was retired and replaced with **OneDrive Known Folder Move**.

I configured Group Policy to:

✅ Automatically sign users into OneDrive using their Windows credentials

✅ Redirect/sync known folders such as Desktop, Documents, and Pictures to OneDrive

✅ Synchronize SharePoint libraries/sites to user endpoints

✅ Provide users with seamless access to their migrated data

✅ Disable the legacy Folder Redirection policies

This significantly reduced the organization's dependency on the traditional file server and established a more modern Microsoft 365-based data management model.

### 🔹 Print Server Migration

Print services were also migrated from the legacy file server to the new server.

I updated the relevant Group Policies to point endpoints to the new print server and deployed the configuration across domain-joined devices using:

`gpupdate /force`

This ensured endpoints received the updated configuration without requiring manual configuration on individual machines.

### 🔹 Decommissioning & Validation

After completing the migrations, I performed validation of:

• Active Directory functionality
• DNS/DHCP services
• FSMO role ownership
• Entra ID synchronization
• SharePoint permissions and data access
• OneDrive synchronization
• Group Policy application
• Print services
• User access to migrated data

Once the environment was verified and all critical services were operating successfully, the legacy Domain Controller and File Server were safely **decommissioned**.

📋 I also documented the completed changes to provide an accurate record of the customer's new environment and configuration.

### 🎯 Project Outcome

The project successfully transformed a traditional two-server on-premises environment into a more modern and resilient infrastructure leveraging:

**Active Directory + Microsoft Entra ID + Microsoft 365 + SharePoint Online + OneDrive + Group Policy**

The biggest achievement for me was completing the migration with **minimal downtime and minimal impact to end users**, while ensuring that critical identity, networking, file, printing, and synchronization services remained operational throughout the transition.

This project gave me valuable hands-on experience across **Windows Server, Active Directory, Hyper-V, Group Policy, DHCP, DNS, Microsoft Entra ID, Entra Connect, SharePoint, OneDrive, Microsoft 365, server migration, and infrastructure decommissioning.**

Another infrastructure modernization project completed successfully. 💪

#SystemEngineer #ITInfrastructure #Microsoft365 #Azure #MicrosoftEntra #ActiveDirectory #SharePoint #OneDrive #WindowsServer #GroupPolicy #HyperV #CloudMigration #InfrastructureMigration #ITEngineering
