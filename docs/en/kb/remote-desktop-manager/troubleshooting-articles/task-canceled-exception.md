---
title: Task Canceled Exception - A Task was Canceled
---
One or more errors occurred in {{ en.RDM }} with a {{ en.DVLS }} data source.  

AggregateException: TaskCanceledException - A task was canceled  
![!!KB4752.png](https://webdevolutions.azureedge.net/docs/en/kb/KB4752.png)
### Solution
1. Go to ***File - Data sources - Edit Data Source - Advanced*** and change the ***Connection timeout*** to 30 sec.
1. Click ***OK***  
![!!KB4751.png](https://webdevolutions.azureedge.net/docs/en/kb/KB4751.png)
