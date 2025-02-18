---
eleventyComputed:
  title: PowerShell Module
  description: The {{ en.PS }} module is a way to access, create, update, and remove elements in your {{ en.HUBB }}. This will help you to automate some operations/scripts.
  keywords:
  - PowerShell
  order: 30
---
The {{ en.PS }} module is a way to access, create, update, and remove elements in your {{ en.HUBB }}. This will help you to automate some operations/scripts. After you install the {{ en.PS }} module, you will be ready to use the module and connect to your {{ en.HUBB }}.  

### Prerequisites 

* PowerShell 7.2 or later installed:  
    * [Windows](https://learn.microsoft.com/en-us/powershell/scripting/install/installing-powershell-on-windows) 
    * [macOS](https://learn.microsoft.com/en-us/powershell/scripting/install/installing-powershell-on-macos) 
    * [Linux](https://learn.microsoft.com/en-us/powershell/scripting/install/installing-powershell-on-linux) 
* An [Application User](/hub/web-interface/hub-overview/administration/management/application-users/manage-application-users/) 

## Tutorials 

### Connecting to Your {{ en.HUBB }} 

{% snippet icon.badgeHelp %} 
For the full list of available commands, see [PowerShell Commands](/hub/powershell-module/powershell-commands/). 
{% endsnippet %}
 
1. Once PowerShell 7.2 or later is installed, open a PowerShell terminal and install the {{ en.PS }} module with the following command:  

`Install-Module -Name {{ en.PS }}`  

![Install-Module Command](https://webdevolutions.azureedge.net/docs/en/hub/Hub2136.png)

{% snippet icon.badgeInfo %} 
Other installation options can be found in the [PowerShell Gallery](https://www.powershellgallery.com/packages/devolutions.powershell/). 
{% endsnippet %}
 
2. Connect to your {{ en.HUBB }} using the command below. If you do not see an error, it means you are connected to your {{ en.HUBB }}. 

`Connect-HubAccount -Url https<area>://yourhub.devolutions.app/ -ApplicationSecret [YOUR_APPLICATION_SECRET] -ApplicationKey [YOUR_APPLICATION_KEY]` 

![Connect-HubAccount Command](https://webdevolutions.azureedge.net/docs/en/hub/Hub4062.png) 

### Command Example and Use 

1. With the `Get-HubVault` command, you can get vaults that your application user can view and edit.  
{% snippet icon.badgeInfo %} 
If you have set the permissions of your application user to multiple vaults, you will see an array of vaults. 
{% endsnippet %}   

![Get-HubVault Command](https://webdevolutions.azureedge.net/docs/en/hub/Hub4063.png) 

2. With this vault information, you can get all of the entries with the command `Get-HubEntry` and the vault ID. 

{% snippet icon.badgeInfo %} 
If you have more than one entry, you will see an array of entries. 
{% endsnippet %}
 
![Get-HubEntry Command](https://webdevolutions.azureedge.net/docs/en/hub/Hub4064.png) 

3. To view specific information, you can put the {{ en.HUBB }} command return to a variable and retrieve what you need, like the connection ID in this example:  
![{{ en.HUBB }} Command Return Variable](https://webdevolutions.azureedge.net/docs/en/hub/Hub4065.png) 
1. To edit this entry, you can change the object and update it with the `Set-HubEntry` command. 
![Set-HubEntry Command](https://webdevolutions.azureedge.net/docs/en/hub/Hub4066.png) 

At any moment, you can validate in your web version of {{ en.HUBB }} that the changes have been made. 
