---
eleventyComputed:
  title: Devolutions Gateway configuration with {{ en.DVLS }}
  order: 30
  description: This topic describes how to configure {{ en.DVLS }}, free or not, to connect with {{ en.DGW }}.
  keywords:
  - VPN
  - Listener
---
This topic describes how to configure {{ en.DVLS }} to connect with {{ en.DGW }}. There are two ways to install a {{ en.DGW }}: the <a href="#steps-for-side-by-side-installation">Side-by-side Installation</a> and the <a href="#steps-for-standalone-installation">Standalone Installation</a>.

## Steps for Side-by-side Installation
{% snippet icon.badgeInfo %}
To set up a free {{ en.DGW }}, it must be installed using the ***Side-by-side*** configuration. It creates a gateway capable of handling up to 5 concurrent sessions. 
{% endsnippet %}  

This method supports more sessions if there is an available {{ en.DGW }} license(s). This installation process is the easier of the two. However, this method is recommended for simpler network layouts, and only one ***Side-by-side*** installation can be done per machine.
1. From the {{ en.DVLSCONSOLE }}, click on the ***Companions*** tab.  
![Companions tab](https://webdevolutions.azureedge.net/docs/en/server/ServerOp2083.png)
1. In the {{ en.DGW }} section, click on ***Install***.  
1. Choose ***Side-by-side Installation***.
![Side-by-side](https://webdevolutions.azureedge.net/docs/en/server/ServerOp0004.png)
{% snippet icon.badgeHelp %}
It is possible to download an [.msi](https://devolutions.net/gateway/download) file to install {{ en.DGW }} on an offline {{ en.DVLS }}.
{% endsnippet %}  

4. If default values don't work for your environment, enter the desired settings.
    1. ***HTTP Listener***: HTTP(s) port to reach the Gateway. (7171 is default)
    1. ***TCP Listener***: port used for the RDP sessions. (8181 is default)
1. Click ***Ok***.  
![Ok Button](https://webdevolutions.azureedge.net/docs/en/server/ServerOp0005.png)
1. Go to the {{ en.DVLS }} web interface, connect with an administrator account.
1. Go to ***Administration – {{ en.DGW }}***.  
![{{ en.DGW }}](https://webdevolutions.azureedge.net/docs/en/server/ServerOp0006.png)
1. Click on the ***Ping*** button for the desired gateway in the list to see if a connection can successfully be made. If the page was already open, refresh it first.  
![Ping](https://webdevolutions.azureedge.net/docs/en/server/ServerOp0007.png)

## Steps for Standalone Installation
Installing by using the ***Standalone*** method will allow to install {{ en.DGW }} on a separate server than {{ en.DVLS }}. It could be for performance purposes or access networks that {{ en.DVLS }} can't access. Many {{ en.DGW }} can be used by {{ en.DVLS }}, but only one {{ en.DGW }} can be installed on a machine.
1. From the {{ en.DVLSCONSOLE }}, click on the ***Companions*** tab.  
![Companions Tab](https://webdevolutions.azureedge.net/docs/en/server/ServerOp0018.png)
1. In the {{ en.DGW }} section, click on ***Install***.
1. Choose ***Standalone Installation***.  
![Standalone](https://webdevolutions.azureedge.net/docs/en/server/ServerOp0008.png)
1. Choose between ***Download version*** & ***Install from msi file***.
{% snippet icon.badgeHelp %}
It is possible to download an [.msi](https://devolutions.net/gateway/download) file to install {{ en.DGW }} on an offline {{ en.DVLS }}.
{% endsnippet %}  

5. Click ***Next***.  
![Download version or msi file](https://webdevolutions.azureedge.net/docs/en/server/ServerOp0009.png)
1. Enter the ***Access URI*** information, for example https://gateway.example.com.
1. Choose the {{ en.DGW }} ***Listeners*** ports (by default they are 7171 and 8181).
    1. If HTTPS is chosen instead of HTTP in the step above, the ***Certificate Configuration*** will be needed.
    1. ***Certificate file***: Needs to be a full chain certificate (.pfx, .p12, .pem, .crt).
    1. ***Certificate password***: Only needed if a .pfx or .p12 certificate was used.
    1. ***Private key file***: Only needed if a .pem or .crt was used as a certificate.
{% snippet icon.shieldWarning %}
Do not share the private key with other users, as it can be used to decrypt the communication between a user and {{ en.DGW }}. Only the public key should be shared.
{% endsnippet %}  

8. Click ***Next***.  
![Listeners](https://webdevolutions.azureedge.net/docs/en/server/ServerOp0010.png)
1. Choose between: 
    * ***Use public key from DVLS instance 'Devolutions Server'***: this option is used if the installed {{ en.DGW }} is on the same server as the {{ en.DVLS }};  
    * ***From file***: If installing {{ en.DGW }} on another computer, download the public key from the {{ en.DVLS }} you want to pair with that {{ en.DGW }}. It is located under ***Administration – {{ en.DGW }}***.  
![Download public key](https://webdevolutions.azureedge.net/docs/en/server/ServerOp0016.png)
1. Click ***Next***.  
![Key Pair Configuration](https://webdevolutions.azureedge.net/docs/en/server/ServerOp0011.png)
1. Click ***Install***.  
![Summary](https://webdevolutions.azureedge.net/docs/en/server/ServerOp0012.png)
1. Click ***Close***.  
![Installation Summary](https://webdevolutions.azureedge.net/docs/en/server/ServerOp0013.png)
1. On the {{ en.DVLS }} web interface, connect with an administrator account.
1. Go to ***Administration – {{ en.DGW }}***.  
![{{ en.DGW }}](https://webdevolutions.azureedge.net/docs/en/server/ServerOp0006.png)
1. Click on the ***Add*** button on the top right corner.  
![Add Button](https://webdevolutions.azureedge.net/docs/en/server/ServerOp0014.png)
1. Enter the following information.
    1. ***Name***: Name of the gateway that will be displayed in {{ en.RDM }}.
    1. ***Description***: Description of the gateway.
    1. ***Set as default***: If enabled, this gateway will be selected by default when configuring {{ en.RDM }}.
    1. ***{{ en.DGW }} URL***: The {{ en.DVLS }} URL that the gateway will connect to.
    1. ***TCP Listening Port***: Set the port with the same TCP port value configured in the console.
1. Click on ***Save***.  
![{{ en.DGW }} Information](https://webdevolutions.azureedge.net/docs/en/server/ServerOp0015.png)

The gateway should now be visible in the list. It is possible to verify the status of the gateway with the ***Ping*** button.  
![Ping](https://webdevolutions.azureedge.net/docs/en/server/ServerOp0007.png)
