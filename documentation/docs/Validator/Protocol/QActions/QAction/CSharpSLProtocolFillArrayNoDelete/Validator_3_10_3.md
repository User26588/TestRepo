﻿---  
uid: Validator_3_10_3  
---

# CSharpSLProtocolFillArrayNoDelete

## HardCodedPid

### Description

Unrecommended use of magic number '{hardCodedTablePid}', use 'Parameter' class instead. QAction ID '{qactionId}'.

### Properties

| Name         | Value       |
| ------------ | ----------- |
| Category     | QAction     |
| Full Id      | 3.10.3      |
| Severity     | Warning     |
| Certainty    | Certain     |
| Source       | Validator   |
| Fix Impact   | NonBreaking |
| Has Code Fix | False       |

### Example code

```xml
protocol.FillArrayNoDelete(Parameter.TableName.tablePid, ..);
```

### Details

SLProtocol.FillArrayNoDelete is used to update a table with new values.  
Make sure to provide it with an ID of a table parameter that exists.  
Using Parameter class is recommended.
