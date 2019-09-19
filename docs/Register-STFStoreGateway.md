# Register-STFStoreGateway

Register an authentication Gateway with a Store

## Syntax

```
Register-STFStoreGateway [-Gateway] <RoamingGateway> [-StoreService] <StoreService> [[-DefaultGateway] <SwitchParameter>] [[-UseFullVpn] <SwitchParameter>] [<CommonParameters>]
```

## Detailed Description

Register an authentication Gateway with the Store for use when users access StoreFront from the internet.

## Related Commands

* [Register-STFStoreOptimalLaunchGateway](Register-STFStoreOptimalLaunchGateway.md)
* [Unregister-STFStoreOptimalLaunchGateway](Unregister-STFStoreOptimalLaunchGateway.md)
* [Unregister-STFStoreGateway](Unregister-STFStoreGateway.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|Gateway|Gateway to register|true|true (ByValue)| |
|StoreService|Store to register Gateway with|true|false| |
|DefaultGateway|Use this Gateway as the default if more than one is defined|false|false| |
|UseFullVpn|Use full VPN access when accessing the Store through this Gateway|false|false| |

## Input Type

### Citrix.StoreFront.Model.Roaming.RoamingGateway

Parameter Gateway: The .NET `Citrix.StoreFront.Model.Roaming.RoamingGateway` reference type

### Citrix.StoreFront.Model.Store.StoreService

Parameter StoreService: A .NET class representing the configuration of a StoreFront Store service

### System.Management.Automation.SwitchParameter

Parameter DefaultGateway: The .NET `System.Management.Automation.SwitchParameter` value type

### System.Management.Automation.SwitchParameter

Parameter UseFullVpn: The .NET `System.Management.Automation.SwitchParameter` value type

## Return Values

### None

## Examples

### EXAMPLE 1 Register a gateway

```
$gateway9 = Get-STFRoamingGateway -Name Netscaler9
$storeService = Get-STFStoreService
Register-STFStoreGateway -Gateway $gateway9 -StoreService $storeService -DefaultGateway -UseFullVpn
```

**REMARKS**

Get the Gateway "Netscaler9" from the global list and register it to the only 

Store for full VPN access.
