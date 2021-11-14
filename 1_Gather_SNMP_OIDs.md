# Gather SNMP OIDs for extension

Dynatrace Extension 2.0 SNMP framework requires that you provide the exact OIDs (Object Identifiers) you wish to monitor. This approach is different to other common SNMP managers where you can present the entire MIB file. 

### Terminology:

**OID (Object Identifier)**

An OID is a sequence of digits separated by '.' that refers to a particular metric on the device. 

For example, the OID `1.3.6.1.2.1.1.3` refers to `sysUpTime` which provides the up time of the device in TimeTicks.

**MIB (Management Information Base)**:

A MIB is a file that device manufacturer provides that contains the OIDs accepted by a device. A device usually has multiple MIBs focussing on certain set of metrics. For example, a MIB with OIDs for resource metrics like CPU, Memory etc, another for interface metrics and so on.

There are 2 types of MIBs:
- Generic MIBs that are common to all devices irrespective of make and model.
- Device specific MIBs that provide device specific metrics.

All MIBs accepted by a device are usually available to download from device management UI. If not, it will be on the manufacturer website.

<br/>

### Reading MIB files

MIB files usually come in `.txt` or `.mib` formats but can also depend on the manufacturer. The common factor is that all MIBs should be readable in a text editor.

The MIB files usually provide OIDs in string format. In order to get the numeric format you may have to use a MIB browser software. 

iReasoning is an example for a popular MIB browser. Please visit [iReasoning Website](http://www.ireasoning.com/) for details.

