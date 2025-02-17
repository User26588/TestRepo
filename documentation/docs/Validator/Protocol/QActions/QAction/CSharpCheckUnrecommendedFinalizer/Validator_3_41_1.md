---  
uid: Validator_3_41_1  
---

# CSharpCheckUnrecommendedFinalizer

## UnrecommendedFinalizer

### Description

Finalizer '{finalizerName}' is unrecommended. QAction ID '{qactionId}'.

### Properties

| Name         | Value       |
| ------------ | ----------- |
| Category     | QAction     |
| Full Id      | 3.41.1      |
| Severity     | Critical    |
| Certainty    | Certain     |
| Source       | Validator   |
| Fix Impact   | NonBreaking |
| Has Code Fix | False       |

### Details

Finalizers need careful implementation as any exception thrown in a finalizer will result in a process crash as this code is executed by the finalizer thread. The performance impact arises from the delayed cleanup until the finalizer finalizes the object. Finalizers can clean up unmanaged resources in case the dispose method was not called, but it is preferred to use a SafeHandle to avoid the need for a finalizer. For resource management, it is recommended to use the IDisposable interface and the dispose pattern instead. More information can be found on the Microsoft docs (https:\/\/learn.microsoft.com\/en\-us\/dotnet\/csharp\/programming\-guide\/classes\-and\-structs\/finalizers).
