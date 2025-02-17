---  
uid: Validator_2_46_3  
---

# CheckIndexAttribute

## InvalidAttributeValue

### Description

Unsupported attribute 'index' in table '{tablePid}'. Current value '{currentValue}'.

### Properties

| Name         | Value       |
| ------------ | ----------- |
| Category     | Param       |
| Full Id      | 2.46.3      |
| Severity     | Major       |
| Certainty    | Certain     |
| Source       | Validator   |
| Fix Impact   | NonBreaking |
| Has Code Fix | False       |

### Details

The value should correspond to one of the column IDXs. '0' (corresponding to the first column) is the recommended value. The referred column should be of Interprete\/Type 'string'.  
If the table is a logger table of type DirectConnection, the index needs to be '1'.
