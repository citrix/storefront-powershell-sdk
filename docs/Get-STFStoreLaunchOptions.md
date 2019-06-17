# Get-STFStoreLaunchOptions

Get Store launch options

## Syntax

```
Get-STFStoreLaunchOptions [-StoreService] <StoreService> [<CommonParameters>]
```

## Detailed Description

Get the options used by a Store when launching an application or desktop on XenApp and XenDesktop.

## Related Commands

* [Set-STFStoreLaunchOptions](Set-STFStoreLaunchOptions.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|StoreService|The Store service to query|true|true (ByValue)| |

## Input Type

### Citrix.StoreFront.Model.Store.StoreService

Parameter StoreService: A .NET class representing the configuration of a StoreFront Store service

## Return Values

### Launch

A .NET class representing the configuration of Launch settings in a StoreFront Store service

## Examples

### EXAMPLE 1 Get the Store launch options

```
$storeservice = Get-STFStoreService
Get-STFStoreLaunchOptions -StoreService $storeservice
```

**REMARKS**

Get the launch options used by the supplied Store service.

**OUTPUT**

```
SetNoLoadBiasFlag                     : False
AddressResolutionType                 : DnsPort
RequestICAClientSecureChannel         : DetectAnyCipers
IgnoreClientProvidedClientAddress     : False
OverlayAutoLoginCredentialsWithTicket : False
OverrideIcaClientName                 : False
RequireLaunchReference                : True
AllowFontSmoothing                    : True
ShowDesktopViewer                     : False
AllowSpecialFolderRedirection         : False
ClientProxyPolicy                     : {}
RoutingPolicy                         : 
Citrix.StoreFront.Model.Store.RoutingPolicy
```
