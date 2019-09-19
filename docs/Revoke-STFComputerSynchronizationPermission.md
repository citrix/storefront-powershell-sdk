# Revoke-STFComputerSynchronizationPermission

Revoke a computers synchronization permissions

## Syntax

```
Revoke-STFComputerSynchronizationPermission [-RemoteServer] <String[]> [<CommonParameters>]



Revoke-STFComputerSynchronizationPermission [-All] <SwitchParameter> [<CommonParameters>]
```

## Detailed Description

Revoke permissions for a StoreFront server on the same domain permission to synchronize from the local Subscription Store.

## Related Commands

* [Grant-STFComputerSynchronizationPermission](Grant-STFComputerSynchronizationPermission.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|RemoteServer|The Netbios name of the server to revoke permissions for|true|true (ByValue)| |
|All|Revoke all permissions|true|false| |

## Input Type

### System.String[]

Parameter RemoteServer: The .NET `System.String` reference type

### System.Management.Automation.SwitchParameter

Parameter All: The .NET `System.Management.Automation.SwitchParameter` value type

## Return Values

### None

## Notes

Restarts the Citrix Subscription Store Service to read new settings.

## Examples

### EXAMPLE 1 Revoke synchronization permissions for multiple servers

```
Revoke-STFComputerSynchronizationPermission -RemoteServer APACSF1,APACSF2
```

**REMARKS**

Revoke StoreFront servers APACSF1 and APACSF2 from the APAC StoreFront group 

the permissions to synchronize.
