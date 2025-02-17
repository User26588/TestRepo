---  
uid: Validator_2_76_3  
---

# CheckOptionsAttribute

## MissingInstanceOption

### Description

Missing value 'instance' in attribute 'SNMP\/OID@options'. Table PID '{paramId}'.

### Properties

| Name         | Value       |
| ------------ | ----------- |
| Category     | Param       |
| Full Id      | 2.76.3      |
| Severity     | Major       |
| Certainty    | Certain     |
| Source       | Validator   |
| Fix Impact   | NonBreaking |
| Has Code Fix | True        |

### Details

The instance option is always required when using the partialSNMP option. If not present, the data in the table can be incomplete or shifted.
