# Grant-STFComputerSynchronizationPermission

Grant a computer synchronization permissions

## Syntax

```
Grant-STFComputerSynchronizationPermission [-RemoteServer] <String[]> [<CommonParameters>]
```

## Detailed Description

Grant a StoreFront server on the same domain permission to synchronize from the local Subscription Store.

## Related Commands

* [Revoke-STFComputerSynchronizationPermission](Revoke-STFComputerSynchronizationPermission.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|RemoteServer|The Netbios name of the server to grant permission to|true|true (ByValue)| |

## Input Type

### System.String[]

Parameter RemoteServer: The .NET `System.String` reference type

## Return Values

### None

## Notes

Restarts the Citrix Subscription Store Service to read new settings.

## Examples

### EXAMPLE 1 Grant multiple server synchronization permissions

```
Grant-STFComputerSynchronizationPermission -RemoteServer APACSF1,APACSF2
```

**REMARKS**

Grant StoreFront servers APACSF1 and APACSF2 from the APAC StoreFront group 

permissions to synchronize.
