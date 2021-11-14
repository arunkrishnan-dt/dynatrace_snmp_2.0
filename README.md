# Dynatrace Extension 2.0 How To

This repo walks throught the process of creating and testing a Dynatrace SNMP extension based off Extension 2.0 framework.

Please note that this is not Dynatrace Official Documentation. Refer to [Extension 2.0 | Dynatrace Documentation](https://www.dynatrace.com/support/help/extend-dynatrace/extensions20/) for official documentation and latest changes. 

## Simple Network Management Protocol (SNMP)

SNMP is an Internet Protocol commonly used to gather performance on network devices like Routers, Switch etc. SNMP can also be used to gather metrics from computers but is seldom used.

SNMP provides 2 capabilities:
-  SNMP Poll
-  SNMP Trap

**SNMP Poll** is the process by which an SNMP manager queries a target device for metrics. This is done by presenting an OID (Object Identifier) to the device and retrieving value corresponding to the OID. SNMP Poll port is done to device port 161 of target device.

**SNMP Trap** is the process by which a device sends a notification to the SNMP manager. This is usually generated to notifiy the SNMP manager of some change on the device, like high resource utilization. SNMP Trap messages are received on port 162 of SNMP Manager.

Dynatrace currently support SNMP Poll feature. SNMP Trap is planned to be released in near future. 

<br/>

This documentation only covers **SNMP Poll**. 
