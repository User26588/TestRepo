---  
uid: Validator_2_21_21  
---

# CheckOptionsAttribute

## InvalidMixOfSshOptionsAndPortSettings

### Description

Mixing option {option} and PortSettings SSH is invalid. Param ID '{pid}'.

### Properties

| Name         | Value       |
| ------------ | ----------- |
| Category     | Param       |
| Full Id      | 2.21.21     |
| Severity     | Major       |
| Certainty    | Certain     |
| Source       | Validator   |
| Fix Impact   | NonBreaking |
| Has Code Fix | False       |

### How to fix

Remove the option from the parameter.  
Reference the parameter in the PortSettings.

### Example code

```xml
<PortSettings name="SSH Connection">
    <IPport>
        <DefaultValue>22</DefaultValue>
    </IPport>
    <BusAddress>
        <Disabled>true</Disabled>
    </BusAddress>
    <PortTypeSerial>
        <Disabled>true</Disabled>
    </PortTypeSerial>
    <PortTypeUDP>
        <Disabled>true</Disabled>
    </PortTypeUDP>
    <SSH>
        <Credentials>
            <Username pid="1100"/>
            <Password pid="1101"/>
        </Credentials>
    </SSH>
</PortSettings>
```

### Details

Conflicting SSH configurations detected.  
You're using both SSH Username, SSH Password, SSH Options and 'PortSettings\/SSH'.  
SSH Username, SSH Password, SSH Options are restricted to one SSH connection on port 22 only and shouldn't be mixed with 'PortSettings\/SSH'.  
Use only one of these configurations.  
'PortSettings\/SSH' is generally better as it supports multiple SSH connections and use any port number.
