# Unregister-STFStoreOptimalLaunchGateway

Unregister an optimal launch Gateway from a Store

## Syntax

```
Unregister-STFStoreOptimalLaunchGateway [-GatewayName] <String> [-StoreService] <StoreService> [<CommonParameters>]



Unregister-STFStoreOptimalLaunchGateway [-Gateway] <ICommonGateway> [-StoreService] <StoreService> [<CommonParameters>]



Unregister-STFStoreOptimalLaunchGateway [-AllOptimalGateways] <SwitchParameter> [-StoreService] <StoreService> [<CommonParameters>]
```

## Detailed Description

Unregister an optimal launch Gateway from a Store used for specified farm connections

## Related Commands

* [Unregister-STFStoreGateway](Unregister-STFStoreGateway.md)
* [Register-STFStoreGateway](Register-STFStoreGateway.md)
* [Register-STFStoreOptimalLaunchGateway](Register-STFStoreOptimalLaunchGateway.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|GatewayName|Name of the gateway|true|true (ByValue)| |
|Gateway|Gateway object to register, either a Roaming or Store optimal gateway|true|true (ByValue)| |
|AllOptimalGateways|Remove all Optimal Gateways|true|false| |
|StoreService|Store service to unregister from|true|false| |

## Input Type

### System.String

Parameter GatewayName: The .NET `System.String` reference type

### Citrix.StoreFront.Model.Common.ICommonGateway

Parameter Gateway: The .NET `Citrix.StoreFront.Model.Common.ICommonGateway` reference type

### System.Management.Automation.SwitchParameter

Parameter AllOptimalGateways: The .NET `System.Management.Automation.SwitchParameter` value type

### Citrix.StoreFront.Model.Store.StoreService

Parameter StoreService: A .NET class representing the configuration of a StoreFront Store service

## Return Values

### None

## Examples

### EXAMPLE 1 Remove Gateway by name

```
$storeService = Get-STFStoreService
UnRegister-STFStoreOptimalLaunchGateway -StoreService $storeService -GatewayName Netscaler10x
```

**REMARKS**

Remove the Gateway object by name

### EXAMPLE 2 Remove Gateway by object

```
$storeService = Get-STFStoreService
$gateway = Get-STFRoamingGateway -Name Netscaler10x
UnRegister-STFStoreOptimalLaunchGateway -StoreService $storeService -Gateway $gateway
```


