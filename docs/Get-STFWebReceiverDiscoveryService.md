# Get-STFWebReceiverDiscoveryService

Get the WebReceiver Discovery Service settings

## Syntax

```
Get-STFWebReceiverDiscoveryService [-WebReceiverService] <WebReceiverService> [<CommonParameters>]
```

## Detailed Description

Get the WebReceiver Discovery Service settings.

## Related Commands

* [Set-STFWebReceiverDiscoveryService](Set-STFWebReceiverDiscoveryService.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|WebReceiverService|The WebReceiver service.|true|true (ByValue)| |

## Input Type

### Citrix.StoreFront.Model.ReceiverForWeb.WebReceiverService

Parameter WebReceiverService: A .NET class representing the configuration of a StoreFront Web Receiver service

## Return Values

### DiscoveryService

The .NET `Citrix.StoreFront.Model.ReceiverForWeb.DiscoveryService` reference type

## Examples

### EXAMPLE 1 Get Discovery Service settings

```
$webReceiver = Get-STFWebReceiverService "/Citrix/StoreWeb"
Get-STFWebReceiverDiscoveryService $webReceiver
```

**REMARKS**

Get the WebReceiver Discovery Service settings for /Citrix/StoreWeb.

**OUTPUT**

```
Url                 : http://mycompany.com/Citrix/Store/discovery
RunDiscoveryAtStart : True
```
