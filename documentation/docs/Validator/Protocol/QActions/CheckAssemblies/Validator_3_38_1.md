---  
uid: Validator_3_38_1  
---

# CheckAssemblies

## UnconsolidatedPackageReference

### Description

Package '{packageId}' has multiple versions across different QActions.

### Properties

| Name         | Value       |
| ------------ | ----------- |
| Category     | QAction     |
| Full Id      | 3.38.1      |
| Severity     | Major       |
| Certainty    | Certain     |
| Source       | Validator   |
| Fix Impact   | NonBreaking |
| Has Code Fix | False       |

### How to fix

Consolidate the package references so they have the same version across all projects.

### Details

When multiple QActions are using different versions of a NuGet package, it can lead to runtime exceptions such as MissingMethodException or InvalidCastException.  
To fix these issues, it is important to use the same version of a NuGet package across the entire solution.  
'Skyline.DataMiner.Dev.\*' (aka DevPacks) or 'Skyline.DataMiner.Files.\*' NuGet packages should also be aligned across all projects of the solution as these packages represent the DataMiner version that is being developed against.
