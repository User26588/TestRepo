---  
uid: Validator_1_30_1  
---

# CheckBaseForAttribute

## InvalidAttribute

### Description

Invalid value '{attributeValue}' in attribute 'baseFor'.

### Properties

| Name         | Value       |
| ------------ | ----------- |
| Category     | Protocol    |
| Full Id      | 1.30.1      |
| Severity     | Critical    |
| Certainty    | Certain     |
| Source       | Validator   |
| Fix Impact   | NonBreaking |
| Has Code Fix | False       |

### How to fix

Make sure that the Protocol@baseFor attribute value is not equal to the value specified in Protocol\/ElementType.

### Details

The Protocol@baseFor attribute value must not be equal to the value specified in Protocol\/ElementType.
