# Add-STFWebReceiverService

Create a new Receiver for Web service

## Syntax

```
Add-STFWebReceiverService [-VirtualPath] <String> [[-SiteId] <Int64>] [-StoreService] <StoreService> [[-ClassicReceiverExperience] <Boolean>] [[-FriendlyName] <String>] [<CommonParameters>]
```

## Detailed Description

Create and configure a new Receiver for Web service.

## Related Commands

* [Get-STFWebReceiverService](Get-STFWebReceiverService.md)
* [Remove-STFWebReceiverService](Remove-STFWebReceiverService.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|VirtualPath|Site virtual path|true|false| |
|SiteId|IIS site id|false|false| |
|StoreService|Store service to use|true|true (ByValue)| |
|ClassicReceiverExperience|Enable the classic Receiver experience. The classic experience is no longer supported. Defaulting to the unified experience to maintain compatibility with legacy scripting.|false|false| |
|FriendlyName|Friendly name to identify the Receiver for Web service|false|false| |

## Input Type

### System.String

Parameter VirtualPath: The .NET `System.String` reference type

### System.Int64

Parameter SiteId: The .NET `System.Int64` value type

### Citrix.StoreFront.Model.Store.StoreService

Parameter StoreService: A .NET class representing the configuration of a StoreFront Store service

### System.Boolean

Parameter ClassicReceiverExperience: The .NET `System.Boolean` value type

### System.String

Parameter FriendlyName: The .NET `System.String` reference type

## Return Values

### WebReceiverService

A .NET class representing the configuration of a StoreFront Web Receiver service

## Examples

### EXAMPLE 1 Create new Receiver for Web service

```
$storeService = Get-STFStoreService
$rfw = Add-STFWebReceiverService -VirtualPath /Citrix/Receiver -StoreService $store
```

**REMARKS**

Create a new Receiver for Web service at the virtual path /Citrix/Receiver 

using the only configured Store service.
