# Remove-STFSubscriptionSynchronizationSource

Remove a synchronization source

## Syntax

```
Remove-STFSubscriptionSynchronizationSource [-RemoteStoreFrontAddress] <String> [[-PassThru] <SwitchParameter>] [<CommonParameters>]



Remove-STFSubscriptionSynchronizationSource [-FriendlyName] <String> [[-PassThru] <SwitchParameter>] [<CommonParameters>]
```

## Detailed Description

Remove a remote StoreFront synchronization source, self service application and desktop subscriptions are pulled from.

## Related Commands

* [Get-STFSubscriptionSynchronizationSource](Get-STFSubscriptionSynchronizationSource.md)
* [Clear-STFSubscriptionSynchronizationSource](Clear-STFSubscriptionSynchronizationSource.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|RemoteStoreFrontAddress|Address of the remote source to remove|true|false| |
|FriendlyName|Friendly name of the source to remove|true|false| |
|PassThru|Output the resulting Subscription store|false|false| |

## Input Type

### System.String

Parameter RemoteStoreFrontAddress: The .NET `System.String` reference type

### System.String

Parameter FriendlyName: The .NET `System.String` reference type

### System.Management.Automation.SwitchParameter

Parameter PassThru: The .NET `System.Management.Automation.SwitchParameter` value type

## Return Values

### None

## Notes

Restarts the Citrix Subscription Store Service to read new settings.


The name of the Store on the remote StoreFront must match that on the local StoreFront group for subscriptions to correctly update.Permissions must be configured using the Grant-STFSubscriptionSynchronization cmdlet on the remote StoreFront.

## Examples

### EXAMPLE 1 Remove a named source

```
Remove-STFSubscriptionSynchronizationSource -FriendlyName APACGroup
```

**REMARKS**

Removes the source named APACGroup.

### EXAMPLE 2 Remove a source by address

```
Remove-STFSubscriptionSynchronizationSource -RemoteStoreFrontAddress apac.example.com
```

**REMARKS**

Remove the synchronization source with the address apac.example.com.
