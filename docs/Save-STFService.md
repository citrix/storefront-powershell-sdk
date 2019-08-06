# Save-STFService

Save changes to a StoreFront service

## Syntax

```
Save-STFService [-Service] <IConfigBasedFeature> [<CommonParameters>]
```

## Detailed Description

Save changes made to a StoreFront service in memory object.

## Related Commands


## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|Service|StoreFront service to save the configuration of|true|true (ByValue)| |

## Input Type

### Citrix.StoreFrontConfiguration.Interfaces.IConfigBasedFeature

Parameter Service: The .NET `Citrix.StoreFrontConfiguration.Interfaces.IConfigBasedFeature` reference type

## Return Values

### None

## Notes

With the exception of those commands that state they don't in the help the save action is executed implicitly on a service when executing StoreFront PowerShell against that object.

## Examples

### EXAMPLE 1 Save changes to the Store service

```
$store = Get-STFStoreService
$store.Service.AllowSessionReconnect = $false
Save-STFService $store
```

**REMARKS**

Disable session reconnect and save the changes.
