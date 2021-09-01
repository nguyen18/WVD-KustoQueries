# WVD-KustoQueries
KQL (Kusto query language) queries for Azure monitor log analytics!

### What is KQL?
Kusto query language is a language developed by Microsoft to query their Azure log databases within Azure Monitor Logs, Azure Monitor Application Insights and others. The language is also similar to SQL so translation between the two would be fairly simple if you understand the fundamental concepts. KQL is very handdy when dealing with large amounts of log data that you would like to organize or manipulate. Because it is within the Azure monitor logs and applications, cost to run these queries is on a pay-as-you-go basis.

### Purpose of these queries
Windows Virtual Desktop (WVD) was used to replace on-campus or physical computers with virtual desktops that can be accessed anywhere. These KQL queries were created to monitor the utilization of them, users accessing them, and system resources being consumed by them such as used CPU/RAM. The queries were important to show the team a proof of concept of these virtual desktops and how they can be efectively utilized but many of the SDSU staff (such as our team) use WVD till this day.
