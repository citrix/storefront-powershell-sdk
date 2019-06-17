# Get-STFStoreRegisteredOptimalLaunchGateway

Get the optimal launch gateways for Store

## Syntax

```
Get-STFStoreRegisteredOptimalLaunchGateway [-StoreService] <StoreService> [<CommonParameters>]
```

## Detailed Description

Get the optimal launch gateways that have been registered to a Store.

## Related Commands

* [Register-STFStoreOptimalLaunchGateway](Register-STFStoreOptimalLaunchGateway)
* [Unregister-STFStoreOptimalLaunchGateway](Unregister-STFStoreOptimalLaunchGateway)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|StoreService|The Store service from which to get the gateways|true|true (ByValue)| |

## Input Type

### Citrix.StoreFront.Model.Store.StoreService

Parameter StoreService: A .NET class representing the configuration of a StoreFront Store service

## Return Values

### OptimalGatewayForFarms

The .NET `Citrix.StoreFront.Model.Store.OptimalGatewayForFarms` reference type

## Examples

### EXAMPLE 1 Get all Store optimal launch gateways

```
$storeService = Get-STFStoreService
Get-STFStoreRegisteredOptimalLaunchGateway -StoreService $storeService
```

**REMARKS**

Get all optimal gateways registered to a store.

**OUTPUT**

```
EnabledOnDirectAccess     : False
Farms                     : {}
NeverLaunchThroughGateway : False
Id                        : 9ecdb90c-3bf8-4d77-9401-4a39584ae882
Name                      : Netscaler9
IPAddress                 : 255.255.240.0
SessionReliability        : True
RequestTicketTwoSTAs      : True
Hostnames                 : {https://eunetscaler.storefront.com/}
SecureTicketAuthorityUrls : {https://XA1/scripts/ctxsta.dll}
StasBypassDuration        : 01:00:00
StasUseLoadBalancing      : False
AuthenticationCapable     : True
HDXRoutingCapable         : True
```
