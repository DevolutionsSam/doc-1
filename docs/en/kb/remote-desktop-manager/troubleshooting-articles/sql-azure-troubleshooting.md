---
title: SQL Azure Troubleshooting
---
### When attempting to use a Azure SQL data source, you receive the error message below;
"UNABLE TO LOAD ADALSQL.DLL (ATHENTICATION=ACTIVEDIRECTORYPASSWORD). ERROR CODE: 0X2. FOR MORE INFORMATION, SEE HTTP<area>://GO.MICROSOFT.COM/FWLINK/?LINKID=513072"  
![!!KB2007.png](https://webdevolutions.azureedge.net/docs/en/kb/KB2007.png)
## Solution
To resolve this issue, please have a look at the topic on [Azure SQL](/rdm/windows/data-sources/data-sources-types/advanced-data-sources/microsoft-azure-sql/)
### When creating a user with azure active directory account authentication, you see the error below;
"PRINCIPAL '' COULD NOT BE CREATED. ONLY CONNECTIONS ESTABLISHED WITH ACTIVE DIRECTORY ACCOUNTS CAN CREATE OTHER ACTIVE DIRECTORY USERS."  
![!!KB2008.png](https://webdevolutions.azureedge.net/docs/en/kb/KB2008.png)
## Solution
You must first define your SQL Server Azure AD Admin via the Azure Portal, then login into Remote Desktop Manager using that Azure AD account, from there you will be able to create new Azure AD accounts (admin and non-admin). Those new admins will also be able to do the same.  

For more information, please have a look at the topic [Configure Azure SQL AD Authentication](/rdm/windows/data-sources/data-sources-types/advanced-data-sources/microsoft-azure-sql/enable-azure-active-directory-authentication/configure-admin/)
