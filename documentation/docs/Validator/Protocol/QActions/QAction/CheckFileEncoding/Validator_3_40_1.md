---  
uid: Validator_3_40_1  
---

# CheckFileEncoding

## InvalidFileEncoding

### Description

Invalid file encoding '{invalidFileEncoding}' detected in file '{fileName}'. QAction ID '{qactionId}'.

### Properties

| Name         | Value       |
| ------------ | ----------- |
| Category     | QAction     |
| Full Id      | 3.40.1      |
| Severity     | Minor       |
| Certainty    | Certain     |
| Source       | Validator   |
| Fix Impact   | NonBreaking |
| Has Code Fix | True        |

### Details

Each file in a QAction needs to be UTF\-8 as otherwise certain characters could be converted to invalid characters.
