---
title: Activity Logs
---
***Activity Logs*** provide a robust logging solution. With this feature, it is possible to monitor an open session for all users using [Advanced Data Sources](/rdm/windows/data-sources/data-sources-types/advanced-data-sources/) . The log is available in the ***View*** tab.  
![Activity Logs Button](https://webdevolutions.azureedge.net/docs/en/rdm/windows/RDMWin2020.png) 

{% snippet icon.badgeInfo %} 
Depending on the permissions each user has, they may only be able to access [***Local Connection Logs***](/rdm/windows/commands/view/logs/) . 
{% endsnippet %}
 
### Search 

All activities in the data source are automatically displayed when opening the ***Activity Logs*** without having to apply any settings. However, search fields are available and can be useful when there are many activity entries. The results can be refined by specifying the ***Date*** or a custom period, the ***Username*** , the ***Message*** , the ***Machine name*** , the ***Folder*** , the ***On open comment*** , ***On close comment*** and the ***Ticket #*** . Select ***All Vaults*** to see entries from all other vaults you have access to. It is also possible to choose between ***Local Time*** and ***UTC Time*** and to search in all vaults or in the current vault only. When all the criteria have been chosen, the ***Search*** button will apply them to the results.  
![Activity Logs Search Fields](https://webdevolutions.azureedge.net/docs/en/rdm/windows/clip10252.png) 

### Logs 

The log contains all the CRUD operations (add, edit, and delete), passwords being viewed, credentials being used by other sessions, etc. It is possible to right-click an entry to access more options.  
![Logs](https://webdevolutions.azureedge.net/docs/en/rdm/windows/RDMWin2021.png) 

The information available for each activity line is presented in the following table. 

<table>
	<tr>
		<th>
		
OPTION 
		</th>
		<th>
DESCRIPTION 
		</th>
	</tr>
	<tr>
		<td>
Folder 
		</td>
		<td>
Indicates the folder where your entry is located. 
		</td>
	</tr>
	<tr>
		<td>
Connection 
		</td>
		<td>
Indicates the connection being used to open your entry. 
		</td>
	</tr>
	<tr>
		<td>
Vault 
		</td>
		<td>
Indicates the vault in which the action was executed. 
		</td>
	</tr>
	<tr>
		<td>
Message 
		</td>
		<td>
Indicates the action that has been executed on your entry or session. 
		</td>
	</tr>
	<tr>
		<td>
On Open Comment 
		</td>
		<td>
The ***On Open Comment*** is defined in the ***Log*** tab of your session. 
		</td>
	</tr>
	<tr>
		<td>
On Close Comment 
		</td>
		<td>
The ***On Close Comment*** is defined in the ***Log*** tab of your session. 
		</td>
	</tr>
	<tr>
		<td>
Log Date 
		</td>
		<td>
Indicates the date and time your session was opened or your entry was edited. 
		</td>
	</tr>
	<tr>
		<td>
End Date/Time 
		</td>
		<td>
Indicates the date and time your session or entry was closed. 
		</td>
	</tr>
	<tr>
		<td>
Active Time 
		</td>
		<td>
This information is only available for embedded mode sessions. The active time of your session, meaning the time at which your session was open in embedded mode and the time you were active on your session, will be recorded. If your session is open, but you are on the ***Dashboard*** tab, for example, and not on you session tab, no active time will be recorded. 
		</td>
	</tr>
	<tr>
		<td>
Duration 
		</td>
		<td>
This information is only available for embedded mode sessions. When sessions are open in embedded mode, the duration of the session will be recorded. This means that even if you are on the ***Dashboard*** tab, for example, and not actively working in your session, but your session tab is open, the session duration will be recorded. 
		</td>
	</tr>
	<tr>
		<td>
Machine User 
		</td>
		<td>
Indicates the name of the machine user. 
		</td>
	</tr>
	<tr>
		<td>
User 
		</td>
		<td>
Indicates the connected user's name. 
		</td>
	</tr>
	<tr>
		<td>
Connection user 
		</td>
		<td>
Indicates the connection user. 
		</td>
	</tr>
	<tr>
		<td>
Ticket # 
		</td>
		<td>
Indicates the ticket number. 
		</td>
	</tr>
	<tr>
		<td>
Machine 
		</td>
		<td>
Indicates the machine name. 
		</td>
	</tr>
	<tr>
		<td>
Connection Type 
		</td>
		<td>
Indicates the connection type that was used. 
		</td>
	</tr>
	<tr>
		<td>
Connection Logs ID 
		</td>
		<td>
Indicates the unique identifier of the connection log. 
		</td>
	</tr>
</table>


