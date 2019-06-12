Overview
========

*InsightIQ provides tools to monitor and analyze historical data from Isilon clusters.*


With InsightIQ, in the InsightIQ web application, you can view standard or customized Performance reports and File System reports, to monitor and analyze Isilon cluster activity. You can create customized reports to view information about storage cluster hardware, software, and protocol operations. You can publish, schedule, and share reports, and you can export the data to a third-party application.

You can create and view specific InsightIQ reports to identify or confirm the cause of a performance issue. For example, if users report client connectivity issues during certain dates, you can create a report that indicates the cause of the issue. InsightIQ enables you to correlate data across present and historical conditions.
If you modify the Isilon cluster environment, you can measure the effects of those changes by creating an InsightIQ report that compares the past performance with the performance after the changes were made. For example, if you add 20 new clients, you can create a report to compare the performance before the change and after the change. This comparison allows you to determine the impact of the additional clients on system performance.

Create customized reports that help to identify bottlenecks or inefficiencies in Isilon cluster systems and workflows. For example, if you want to verify that all clients can access the cluster quickly and efficiently, you can create a report that measures which client connections are faster or slower. You can then modify the report to add breakouts and filters to identify the cause of the slower connections.

Customized reports provide specific information about cluster operations. For example, if you recently deployed an Isilon cluster, you might want to view a customized report that illustrates how the cluster and its individual components are performing.

A review of past performance trends can help you predict future trends and needs. For example, if you deployed an Isilon cluster for a data-archival project 6 months ago, you might want to estimate when the cluster reaches its maximum capacity. You can customize a report to illustrate capacity usage by day, week, or month to estimate when the cluster reaches capacity.

You can install InsightIQ on a Linux computer or on a virtual machine. Configure settings such as the IP address of InsightIQ and the administrator password in the InsightIQ console interface.



Monitoring clusters with InsightIQ Dashboard
--------------------------------------------

*View the status of all the monitored clusters.*

InsightIQ Dashboard, available through the InsightIQ web application, provides you with an overview of the status of all the monitored clusters. The Cluster Status summary includes information about cluster capacity, clients, throughput, and CPU usage. Current information about the monitored clusters appears alongside graphs that show the relative changes in the statistics over the past 12 hours.

The Aggregated Cluster Overview section displays the total or average values of the status information for the monitored clusters. This information can help you decide what to include in a Performance report. For example, if the total amount of network traffic for all the monitored clusters is higher than anticipated, a customized Performance report can show you the data about network traffic. The report can show you the network throughput by direction, by using breakouts, to help you determine whether one direction of throughput is contributing to the total more than the other.


Performance reports and File System reports
-------------------------------------------

*Monitor EMC Isilon clusters with customizable reports.*

Performance reports include information about the cluster activity and capacity. The information can help you confirm that storage clusters perform as expected, and help you identify the specific cause of a performance-related issue to investigate. File System reports include information about the cluster file system, including deduplication, quotas, and usable capacity. The information can help you identify the types of data that is stored and where the data is located.

With InsightIQ, you can create live reports and view them through the InsightIQ web application. You can create live reports for Performance reports and File System reports. You can modify the attributes of live reports as you view the reports, including the period, breakouts, and filters.

You can view Performance reports as a PDF file that is generated based on a report schedule that the administrator sets up. InsightIQ can be configured to send a PDF file as an email attachment. You can use a PDF file to verify cluster health or to distribute InsightIQ information to individuals who do not have access to the InsightIQ web application.


Report configuration
--------------------

*InsightIQ reports are configured by using modules, breakouts, and filter rules.*

A module is a section of a report that displays information about a cluster. A breakout can be applied to a module so that users can view information about separate cluster components. A filter rule can be applied to a module so that users can view information about a specific component across the entire report. Filter rules can be combined into collections that are called filters. Filters can be saved and applied to multiple reports.


InsightIQ feature compatibility with OneFS
------------------------------------------
Certain InsightIQ features are supported on specific versions of OneFS.

**OneFS feature compatibility**

*Certain InsightIQ features require specific versions of OneFS.*

InsightIQ can be used with clusters that run versions of OneFS earlier than OneFS 8.0.1. However, InsightIQ includes features that OneFS versions earlier than OneFS 8.0.1 do not support.

InsightIQ features supported by OneFS versions

+---------------------------------------------------------------------------+----------------------+--------------------------------------------------------------------------------------------+
| InsightIQ feature                                                         | Requirement          | Notes                                                                                      |
+===========================================================================+======================+============================================================================================+
| Performance modules - Cache, Event Summary, Node pool, and Tier breakouts | OneFS 7.1.0 or later | To view data about L3 cache, the cluster must be running OneFS 7.1.1 or later.             |
+---------------------------------------------------------------------------+----------------------+--------------------------------------------------------------------------------------------+
| Reports - Quota, Capacity, and Deduplication                              | OneFS 7.1.0 or later | To view more than 1000 quotas at a time, the cluster must be running OneFS 7.2.0 or later. |
+---------------------------------------------------------------------------+----------------------+--------------------------------------------------------------------------------------------+
| File System Analytics - Node pool and tier breakouts                      | OneFS 8.0.0 or later | None                                                                                       |
+---------------------------------------------------------------------------+----------------------+--------------------------------------------------------------------------------------------+
