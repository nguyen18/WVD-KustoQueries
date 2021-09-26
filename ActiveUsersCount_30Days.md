# Active Users Count over 30 Days
Counts how many users were active over 30 day period

```OQL
ITPC_CTX_Session_CL
| where TimeGenerated > ago(30d)
| summarize AggregatedValue = dcount(SessionHash_s) by TimeInterval = format_datetime(bin(TimeGenerated - 7h, 1h), 'M/d/yyyy'), ConnectionState_s  //bin(TimeGenerated, 1h) -7h
| sort by TimeInterval desc
| where ConnectionState_s  == "Active"
| project TimeInterval, ConnectionState_s , Active_User_Count = AggregatedValue
```
