# Get-STFStoreService

Gets the StoreFront Store Services matching the supplied parameter criteria.

## Syntax

```
Get-STFStoreService [[-VirtualPath] <String>] [[-SiteId] <Int64>] [<CommonParameters>]



Get-STFStoreService [-AuthenticationService] <AuthenticationService> [[-VirtualPath] <String>] [[-SiteId] <Int64>] [<CommonParameters>]



Get-STFStoreService [-WebReceiverService] <WebReceiverService> [[-VirtualPath] <String>] [[-SiteId] <Int64>] [<CommonParameters>]
```

## Detailed Description

StoreFront Store Services are deployed to specific IIS virtual paths and sites. The command will return all Store Services if no IIS VirtualPath or SiteId is specified.StoreFront Stores aggregate desktops and applications, making them available to users.

## Related Commands

* [Add-STFStoreService](Add-STFStoreService.md)
* [Remove-STFStoreService](Remove-STFStoreService.md)
* [Set-STFStoreService](Set-STFStoreService.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|VirtualPath|Virtual path of the Store to return|false|false| |
|SiteId|The IIS Site to which the Store should belong|false|false| |
|AuthenticationService|Stores used by an Authentication service|true|true (ByValue)| |
|WebReceiverService|Stores used by a Web Receiver service|true|false| |

## Input Type

### System.String

Parameter VirtualPath: The .NET `System.String` reference type

### System.Int64

Parameter SiteId: The .NET `System.Int64` value type

### Citrix.StoreFront.Model.Authentication.AuthenticationService

Parameter AuthenticationService: A .NET class representing the configuration of a StoreFront Authentication service

### Citrix.StoreFront.Model.ReceiverForWeb.WebReceiverService

Parameter WebReceiverService: A .NET class representing the configuration of a StoreFront Web Receiver service

## Return Values

### StoreService

A .NET class representing the configuration of a StoreFront Store service

## Examples

### EXAMPLE 1 Get all Stores

```
Get-STFStoreService
```

**REMARKS**

Gets all Stores on the StoreFront server.

### EXAMPLE 2 Get Specific Store

```
Get-STFStoreService -VirtualPath /Citrix/Store
```

**REMARKS**

Get the Store at the /Citrix/Store IIS Virtual Path.
