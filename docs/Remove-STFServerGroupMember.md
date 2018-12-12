# Remove-STFServerGroupMember

Remove a member from the Server group

## Syntax

```
Remove-STFServerGroupMember [-Name] <String> [[-Notify] <SwitchParameter>] [<CommonParameters>]
```

## Detailed Description

Removes a server that was previously joined from the StoreFront server group.

## Related Commands


## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|Name|The host name of the server to remove|true|false| |
|Notify|Notify removed server to clear configuration (if it is contactable)|false|false| |

## Input Type

### System.String

Parameter Name: The .NET `System.String` reference type

### System.Management.Automation.SwitchParameter

Parameter Notify: The .NET `System.Management.Automation.SwitchParameter` value type

## Return Values

### None

## Examples

### EXAMPLE 1 Remove server from the group

```
Remove-STFServerGroupMember -Name 'ServerB'
```

**REMARKS**

Remove ServerB from the StoreFront server group.

### EXAMPLE 2 Remove server from the group and clear configuration

```
Remove-STFServerGroupMember -Name 'ServerB' -Notify
```

**REMARKS**

Removes the server from the server group and notifies that it should clear the configuration it has.
