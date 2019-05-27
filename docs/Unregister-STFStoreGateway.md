# Unregister-STFStoreGateway

Unregister a Gateway from a Store

## Syntax

```
Unregister-STFStoreGateway [-Gateway] <ICommonGateway> [-StoreService] <StoreService> [<CommonParameters>]



Unregister-STFStoreGateway [-Name] <String> [-StoreService] <StoreService> [<CommonParameters>]



Unregister-STFStoreGateway [-AllGateways] <SwitchParameter> [-StoreService] <StoreService> [<CommonParameters>]
```

## Detailed Description

Unregister a Gateway from a Store used for authentication and launch (if configured for launch)

## Related Commands

* [Register-STFStoreOptimalLaunchGateway](Register-STFStoreOptimalLaunchGateway.md)
* [Register-STFStoreGateway](Register-STFStoreGateway.md)
* [Unregister-STFStoreOptimalLaunchGateway](Unregister-STFStoreOptimalLaunchGateway.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|Gateway|The Gateway object to remove, either a Roaming or Store gateway|true|true (ByValue)| |
|Name|Name of the Gateway to remove|true|true (ByValue)| |
|AllGateways|Remove all Gateways|true|true (ByValue)| |
|StoreService|Store service to unregister from|true|false| |

## Input Type

### Citrix.StoreFront.Model.Common.ICommonGateway

Parameter Gateway: The .NET `Citrix.StoreFront.Model.Common.ICommonGateway` reference type

### System.String

Parameter Name: The .NET `System.String` reference type

### System.Management.Automation.SwitchParameter

Parameter AllGateways: The .NET `System.Management.Automation.SwitchParameter` value type

### Citrix.StoreFront.Model.Store.StoreService

Parameter StoreService: A .NET class representing the configuration of a StoreFront Store service

## Return Values

### None

## Examples

### EXAMPLE 1 Remove Gateway by name

```
$storeService = Get-STFStoreService
UnRegister-STFStoreGateway -StoreService $storeService -Name Netscaler10x
```

**REMARKS**

Remove the Gateway object by name

### EXAMPLE 2 Remove Gateway by object

```
$storeService = Get-STFStoreService
$gateway = Get-STFRoamingGateway -Name Netscaler10x
UnRegister-STFStoreGateway -StoreService $storeService -Gateway $gateway
```

**REMARKS**

Remove the Gateway object Netscaler10x from the only Store
