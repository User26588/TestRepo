---  
uid: Validator_2_21_23  
---

# CheckOptionsAttribute

## HeaderTrailerConnectionShouldBeValid

### Description

The connection '{connectionId}' needs to be a valid connection type when used on a {headerOrTrailer} with PID '{paramId}'.

### Properties

| Name         | Value       |
| ------------ | ----------- |
| Category     | Param       |
| Full Id      | 2.21.23     |
| Severity     | Minor       |
| Certainty    | Certain     |
| Source       | Validator   |
| Fix Impact   | NonBreaking |
| Has Code Fix | False       |

### How to fix

Assign the connection to an ID of a valid connection type

### Example code

```xml
<Type options="headerTrailerLink=1;connection=0">
```

### Details

When a connection is specified then this header\/trailer parameter will only be taken into account when the connection ID matches.  
If the connection id is being specified on a different connection type, like SNMP, then it makes no sense to specify the parameter as header\/trailer type on such a connection type.
