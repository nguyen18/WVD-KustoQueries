# Active Users Chart over 30 Days
Monitors all active users on the WVD over a 30 day period and displays in a chart.

```OQL
ITPC_CTX_Session_CL
| where TimeGenerated > ago(30d)
| where ConnectionState_s == "Active"
| summarize AggregatedValue = dcount(SessionHash_s) by TimeInterval = format_datetime(bin(TimeGenerated - 7h, 1h), 'M/d/yyyy'), UserName_s, ConnectionState_s 
| render columnchart 
```
