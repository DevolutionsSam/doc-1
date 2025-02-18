---
title: Topologies
keywords:
- high availability
- load balancing
- topology
---
{{ en.DVLS }} instances can be installed through different topologies. The following are examples of different topologies serving various purposes.  

## Single Server Topology

The {{ en.DVLS }} and the SQL Server can be installed on the same machine for a small team up to 20 users. Having {{ en.DVLS }} and SQL Server on the same machine could result in certain performance issues if you attempt to serve more than 20 users.  
![Single Server Installation](https://webdevolutions.azureedge.net/docs/en/server/RecommendedTopology-1.png)

## Recommended Basic Topology

A recommended basic topology consists of two servers, one for the {{ en.DVLS }} and one for the SQL Database. By doing so, all queries are made by the SQL server and performance is less affected on the application server.  
![Basic Topology](https://webdevolutions.azureedge.net/docs/en/server/RecommendedTopology-2.png)

## High Availability Topology

### Database layer only

For a high availability of the database, Database Mirroring can be used which replicates data to a partner server. The failover partner server will be ready at anytime when the main server becomes unavailable. This ensures that the {{ en.DVLS }} is still accessing the data source and is transparent for {{ en.RDM }} users.  
![High Availability Topology](https://webdevolutions.azureedge.net/docs/en/server/RecommendedTopology-3.png)

## Load Balancing Topology

To ensure maximum performance of the {{ en.DVLS }} , it can be deployed as a load balancing {{ en.DVLS }} topology as illustrated in the image below. It can either be a physical or software load balancing system.  
![Load Balancing Devolutions Server Topology](https://webdevolutions.azureedge.net/docs/en/server/RecommendedTopology-4.png)

## {{ en.DVLS }} Instance Manual Failover

For customers that do not wish to purchase a load balancer or are seeking a more simplified topology for their system, you can simply utilize two {{ en.DVLS }} instances on two different web servers and direct them to the same SQL Server database. By registering both instances as separate data sources in the client applications, users can manually toggle between servers in the scenario that one becomes unresponsive.  
![Manual Failover with Two Devolutions Servers](https://webdevolutions.azureedge.net/docs/en/server/RecommendedTopology-5.png)
