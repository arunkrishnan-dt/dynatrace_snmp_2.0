# Dynatrace SNMP Extension 2.0 How To

This repo walks you through the process of creating and testing a Dynatrace SNMP extension based off Extension 2.0 framework.

> **NOTE**: This documentation assumes that the reader has some basic understanding of SNMP and is familiar with snmp commands like `snmpget` amd `snmpwalk`. 

> Please note that this is not Dynatrace Official Documentation. Refer to [Extension 2.0 | Dynatrace Documentation](https://www.dynatrace.com/support/help/extend-dynatrace/extensions20/) for official documentation and latest changes. 

## Simple Network Management Protocol (SNMP)

SNMP is an Internet Protocol commonly used to gather performance metrics & alerts on network devices like Routers, Switch etc. SNMP can also be used to gather metrics from computers but is seldom used.

SNMP provides 2 capabilities:
-  SNMP Poll
-  SNMP Trap

**SNMP Poll** is the process by which an SNMP manager queries a target device for metrics. This is done by presenting an OID (Object Identifier) to the device and retrieving value corresponding to the OID. SNMP Poll is done to device port 161 of target device.

**SNMP Trap** is the process by which a device sends a notification to the SNMP manager. This is usually generated to notifiy the SNMP manager of some change on the device, like high resource utilization. SNMP Trap messages are received on port 162 of SNMP Manager.

Dynatrace currently supports SNMP Poll feature and SNMP Trap support is planned to be released in near future. 

<br/>

This documentation only covers **SNMP Poll**. 


## Pages:

Setup Steps:
1. [Gather SNMP OIDs for extension](1_Gather_SNMP_OIDs.md)
2. [Prepare extension.yaml](2_Prepare_extension_file.md)
3. [Sign Extension](3_Sign_extension.md)
4. [Upload extension to tenancy and setup monitoring](4_Upload_and_setup_monitoring.md)
5. [Check metrics and chart](5_Check_metrics_and_chart.md)

[Troubleshooting](6_Troubleshooting.md)