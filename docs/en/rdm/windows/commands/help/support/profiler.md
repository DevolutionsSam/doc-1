---
title: Profiler
---
{{ en.RDM }} has a built-in profiler to diagnose connectivity issues with a data source. 

{% snippet icon.badgeInfo %} 
Displaying the Profiler window might slow down the operations on the data source. Proceed with care. 
{% endsnippet %}
 
{% snippet icon.badgeNotice %} 
To diagnose startup issues, you can enable the profiler from the command line as described in [Command Line Arguments](/kb/remote-desktop-manager/how-to-articles/command-line-arguments/#usage-remotedesktopmanagerexe-parameters). 
{% endsnippet %}
 
## Procedure 

1. Once the Profiler is opened, refresh the data source. 

{% snippet icon.badgeInfo %} 
Holding the Ctrl key while performing the refresh should force a full reload of the data source, recreating the offline cache. 
{% endsnippet %}
 
![Performance Profiling](https://webdevolutions.azureedge.net/docs/en/rdm/windows/clip10442.png) 

2. The Profiler data will appear in the ***Performance Profiling*** window.  
![Refresh Data Source](https://webdevolutions.azureedge.net/docs/en/rdm/windows/clip10438.png) 
1. Click on ***Send Trace to Support*** to send the Profiler data logs to our support team. You can add a Marker when running multiple tests to separate them. 

### Debug only 

To learn more about the ***Debug only*** tab please see the Debugging topic.  
![Debug only](https://webdevolutions.azureedge.net/docs/en/rdm/windows/clip10443.png) 

