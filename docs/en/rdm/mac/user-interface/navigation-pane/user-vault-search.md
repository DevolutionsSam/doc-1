---
eleventyComputed:
  title: Search in {{ en.UVLT }}
keywords:
- Private vault
---
The {{ en.UVLT }} Search allows to link a {{ en.UVLT }} credential entry to a session by providing the name of the credential entry. Once the credential is found it will automatically be used to open your remote session.  

## Settings 

1. Create a credential entry in the {{ en.UVLT }} .  
![User Vault](https://webdevolutions.azureedge.net/docs/en/rdm/mac/clip6004.png) 
1. In the remote session, set the Credentials property to {{ en.UVLT }} search and enter the exact name of the {{ en.UVLT }} credential. The search is not case sensitive, if more than one entry has the same name or if no entry matches the searched name, you will be prompted with a list of all available {{ en.UVLT }} credentials. Variables are supported as well.  
![RDP Session - User Vault Search](https://webdevolutions.azureedge.net/docs/en/rdm/mac/clip6006.png) 
1. Open the session as you would normally proceed. Once the credential is found it will automatically be used to open the remote session. 

{% snippet icon.badgeInfo %} 
The {{ en.UVLT }} is linked to the database user. Another user will never be able to see your {{ en.UVLT }} credentials. 
{% endsnippet %}
 

