# Prepare extension.yaml

Dynatrace Extension Framework 2.0 provides us the capability to define extensions as `.yaml` files. In this page, you will learn how to prepare `extension.yaml` file for SNMP monitoring.

> Please read official [Extensions 2.0 concepts](https://www.dynatrace.com/support/help/shortlink/extensions-concepts) for how the extension works.

> This documentation does not require a deep understanding of `yaml` file structure but recommend light reading on the topic.

<br/>

### Extension folder structure

Please structure your extension working directory as below (required):

```
SNMP
 |
 --> Cisco                      # OK to rename with your device name
        |
        --extension             # DO NOT rename
             |
             -- extension.yaml  # DO NOT rename

```

<br/>

### YAML file

The `extension.yaml` file follows below basic structure:


```
name: <value>               
version: <value>
minDynatraceVersion: <value>
author:
  name: <value>

metrics:
- key: <value>
   metadata:
      displayName: <value>
      description: <value>
      unit: <value>
- key: <value>
   metadata:
      displayName: <value>
      description: <value>
      unit: <value>

snmp:
- group: <value>
  interval: <value>
  
  dimensions:
  - key: <value>
    value: <value>

  subgroups:
    - subgroup: <value>
      table: false    
      metrics:
        - key: <value>
          value: oid:<value>
          type: <value>
    - subgroup: <value>
      table: true
      dimensions:
        - key: <value>
          value: <value>
      metrics:
        - key: <value>
          value: oid:<value>
          type: <value>

```

Each parameter in order shown above:

`name`: A name for the extension. This have to be in the format `custom:<your_chosen_name>`. Example: `custom:cisco_router_snmp`

`version`: This is the your iteration. Example: `1.0.0`

`minDynatraceVersion`: Earliest version of Dynatrace that this extension can run on. For the purpose of this documentation please use `"1.217"`

`author`

  `name`: Company/your name.




