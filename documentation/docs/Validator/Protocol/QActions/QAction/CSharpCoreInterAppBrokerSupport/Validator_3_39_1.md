---  
uid: Validator_3_39_1  
---

# CSharpCoreInterAppBrokerSupport

## InvalidInterAppReplyLogic

### Description

Invocation of method '{methodClassType}.{incompatibleMethod}' is not compatible with 'DataMiner.Core.InterApp \>\= v1.0.1.1'. QAction ID '{qactionId}'.

### Properties

| Name         | Value       |
| ------------ | ----------- |
| Category     | QAction     |
| Full Id      | 3.39.1      |
| Severity     | Critical    |
| Certainty    | Certain     |
| Source       | Validator   |
| Fix Impact   | NonBreaking |
| Has Code Fix | False       |

### How to fix

To ensure correct handling of messages, always respond to incoming interapp messages by invoking the \`.Reply()\` method on the original message object received from an external source.   
It is incorrect to use the \`.Reply()\` method on newly created message objects.   
Additionally, avoid performing \`.SetParameter(9000001, data);\` or invoking \`.Send\` to the \`ReturnAddress\`, as these actions are also incorrect.

### Example code

```xml
foreach (var receivedMessage in receivedCall.Messages)
{
    Message response;
    receivedMessage.TryExecute(protocol, protocol, Shared.Mapping, out response);
    
    if (response != null)
    {
         receivedMessage.Reply(protocol.SLNet.RawConnection, response, Shared.KnownTypes);
    }
}
```

### Details

To maintain proper message handling, always use the .Reply() method on the original incoming message object received from an external source.  
Do not use .Reply() on messages you create anew.   
Also, refrain from using .SetParameter(9000001, data); or .Send to the ReturnAddress, as these practices are incorrect.  
Using the .Reply() method is crucial because it incorporates specific logic that optimizes communication between applications. It dynamically chooses the best delivery method, utilizing either SLNet Subscriptions or a more efficient message broker when available, ensuring that responses are handled efficiently and effectively based on the current configuration of the running agent.   
This optimization helps maintain system integrity and improves performance.
