# Get-STFStoreGatewayService

Get the gateway service settings for a Store

## Syntax

```
Get-STFStoreGatewayService [-StoreService] <StoreService> [<CommonParameters>]
```

## Detailed Description

Get the gateway service settings for a Store.

## Related Commands

* [Set-STFStoreGatewayService](Set-STFStoreGatewayService.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|StoreService|The Store service from which to get the gateway service settings|true|true (ByValue)| |

## Input Type

### Citrix.StoreFront.Model.Store.StoreService

Parameter StoreService: A .NET class representing the configuration of a StoreFront Store service

## Return Values

### StoreGateway

The .NET `Citrix.StoreFront.Model.Store.StoreGateway` reference type

## Examples

### EXAMPLE 1 Get gateway service settings for a Store

```
$storeService = Get-STFStoreGatewayServiceSettings
Get-STFStoreGatewayServiceSettings -StoreService $storeService
```

**REMARKS**

Get gateway service settings for a Store.

**OUTPUT**

```
Enabled                   : True
GetGatewayServiceUrl      : https://gatewaycontrolpane/GetGateway
ServiceKey                : base64string
ServiceName               : 9ecdb90c-3bf8-4d77-9401-4a39584ae882
SecureTicketAuthorityUrl  : https://cwcstaservice
SecureTicketLifetime      : 00:01:00
SessionReliability        : True
RequestTwoTickets         : False
```
