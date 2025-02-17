---  
uid: Validator_3_42_1  
---

# CheckDataMinerDependency

## MismatchDevPack

### Description

Package '{packageName}' version '{packageVersion}' does not meet the minimum required version '{minimumRequiredVersion}'. QAction ID '{qactionId}'.

### Properties

| Name         | Value       |
| ------------ | ----------- |
| Category     | QAction     |
| Full Id      | 3.42.1      |
| Severity     | Major       |
| Certainty    | Certain     |
| Source       | Validator   |
| Fix Impact   | NonBreaking |
| Has Code Fix | False       |

### How to fix

Either increase version in the MinimumRequiredVersion tag or downgrade the package so it matches with the minimum required version.

### Details

Using a higher version of the DevPack may introduce new features that are not compatible with the specified version of DataMiner.  
This can lead to unexpected behavior or errors. Make sure that the DevPack version used in the solution does not exceed the MinimumRequiredVersion.
