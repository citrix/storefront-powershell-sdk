# Get-STFWebReceiverResourcesService

Get the WebReceiver Resources Service settings

## Syntax

```
Get-STFWebReceiverResourcesService [-WebReceiverService] <WebReceiverService> [<CommonParameters>]
```

## Detailed Description

Get the WebReceiver Resources Service settings.

## Related Commands

* [Set-STFWebReceiverResourcesService](./Set-STFWebReceiverResourcesService)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|WebReceiverService|The WebReceiver service.|true|true (ByValue)| |

## Input Type

### Citrix.StoreFront.Model.ReceiverForWeb.WebReceiverService

Parameter WebReceiverService: A .NET class representing the configuration of a StoreFront Web Receiver service

## Return Values

### ResourcesService

The .NET `Citrix.StoreFront.Model.ReceiverForWeb.ResourcesService` reference type

## Examples

### EXAMPLE 1 Get WebReceiver Resources settings

```
$receiver = Get-STFWebReceiverService
Get-STFWebReceiverResourcesService -WebReceiverService $receiver
```

**REMARKS**

Get the WebReceiver Resources service settings of the only configured WebReceiver.

**OUTPUT**

```
PersistentIconCacheEnabled : True
IcaFileCacheExpiry         : 90
IconSize                   : 128
ShowDesktopViewer          : True
```
