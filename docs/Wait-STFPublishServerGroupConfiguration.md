# Wait-STFPublishServerGroupConfiguration

Wait for the Server Group configuration to be published

## Syntax

```
Wait-STFPublishServerGroupConfiguration [[-WaitTimeout] <Int32>] [<CommonParameters>]
```

## Detailed Description

Waits for the Server Group configuration to be published showing a status bar to indicate activity is ongoing.

## Related Commands

* [Publish-STFServerGroupConfiguration](./Publish-STFServerGroupConfiguration)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|WaitTimeout|The length of time in minutes to wait for the configuration publish to complete. The default is to wait indefinitely.|false|false| |

## Input Type

### System.Int32

Parameter WaitTimeout: The .NET `System.Int32` value type

## Return Values

### SynchronisationState

The .NET `Citrix.DeliveryServices.ConfigurationReplication.Contract.ServiceStatus.SynchronisationState` reference type

## Examples

### EXAMPLE 1 Wait for Publish to complete

```
Wait-STFPublishServerGroupConfiguration  -Confirm:$false
```

**REMARKS**

Wait for the server group publish to complete. The command can be terminated before completion using the key combination CTRL+C.
