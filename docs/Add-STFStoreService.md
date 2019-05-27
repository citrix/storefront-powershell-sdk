# Add-STFStoreService

Creates a new StoreFront Store Service at the supplied IIS VirtualPath and optional SiteId.

## Syntax

```
Add-STFStoreService [-AuthenticationService] <AuthenticationService> [-VirtualPath] <String> [[-SiteId] <Int64>] [[-FarmName] <String>] [[-FarmType] <XenApp | XenDesktop | AppController | VDIinaBox | Store>] [[-Servers] <String[]>] [[-ServiceUrls] <String[]>] [[-Port] <Int32>] [[-TransportType] <HTTP | HTTPS | SSL>] [[-SSLRelayPort] <Int32>] [[-LoadBalance] <Boolean>] [[-AllFailedBypassDuration] <Int32>] [[-BypassDuration] <Int32>] [[-FriendlyName] <String>] [[-Zones] <String[]>] [[-ConnectionString] <String>] [<CommonParameters>]



Add-STFStoreService [-Anonymous] <SwitchParameter> [-VirtualPath] <String> [[-SiteId] <Int64>] [[-FarmName] <String>] [[-FarmType] <XenApp | XenDesktop | AppController | VDIinaBox | Store>] [[-Servers] <String[]>] [[-ServiceUrls] <String[]>] [[-Port] <Int32>] [[-TransportType] <HTTP | HTTPS | SSL>] [[-SSLRelayPort] <Int32>] [[-LoadBalance] <Boolean>] [[-AllFailedBypassDuration] <Int32>] [[-BypassDuration] <Int32>] [[-FriendlyName] <String>] [[-Zones] <String[]>] [[-ConnectionString] <String>] [<CommonParameters>]
```

## Detailed Description

StoreFront stores aggregate desktops and applications, making them available to users. Stores appear in Citrix Receiver under users' accounts, so choose a VirtualPath that gives users information about the content of the store.

## Related Commands

* [Get-STFStoreService](Get-STFStoreService.md)
* [Remove-STFStoreService](Remove-STFStoreService.md)
* [Set-STFStoreService](Set-STFStoreService.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|VirtualPath|The IIS VirtualPath at which the Store will be configured to be accessed by Receivers|true|false| |
|SiteId|The IIS Site to configure the Store Service within|false|false| |
|AuthenticationService|The StoreFront Authentication Service to use for authenticating users|true|true (ByValue)| |
|Anonymous|Anonymous Store not requiring authentication|true|false| |
|FarmName|The Farm name to use for the supplied XenApp\XenDesktop servers|false|false| |
|FarmType|The type of farm being configured for the servers supplied|false|false| |
|Servers|The servers to configure for the initial XenApp\XenDesktop farm|false|false| |
|ServiceUrls|The url to the service location used to provide web and SaaS apps via this farm.|false|false| |
|Port|The XML service port used for communicating with the XenApp\XenDesktop servers|false|false| |
|TransportType|The type of transport to use for the Xml service communication|false|false| |
|SSLRelayPort|The XenApp SSLRelay port used for the XML service. Only applicable to XenApp 6.5 servers and earlier|false|false| |
|LoadBalance|Load balance the servers or use in failover order if specifying more than one|false|false| |
|AllFailedBypassDuration|The period in minutes to wait before retrying communicating will all servers should they all fail.|false|false| |
|BypassDuration|Time period in minutes to bypass a server when resources are unavailable|false|false| |
|FriendlyName|Friendly name to identify the Store|false|false| |
|Zones|List of Zone names associated with the initial XenApp\XenDesktop farm|false|false| |
|ConnectionString|Specify the Sql Server connection string to use for the Subscriptions database|false|false| |

## Input Type

### System.String

Parameter VirtualPath: The .NET `System.String` reference type

### System.Int64

Parameter SiteId: The .NET `System.Int64` value type

### Citrix.StoreFront.Model.Authentication.AuthenticationService

Parameter AuthenticationService: A .NET class representing the configuration of a StoreFront Authentication service

### System.Management.Automation.SwitchParameter

Parameter Anonymous: The .NET `System.Management.Automation.SwitchParameter` value type

### System.String

Parameter FarmName: The .NET `System.String` reference type

### Citrix.StoreFront.Model.Store.FarmType

Parameter FarmType: The .NET `Citrix.StoreFront.Model.Store.FarmType` value type

### System.String[]

Parameter Servers: The .NET `System.String` reference type

### System.String[]

Parameter ServiceUrls: The .NET `System.String` reference type

### System.Int32

Parameter Port: The .NET `System.Int32` value type

### Citrix.StoreFront.Model.Store.TransportType

Parameter TransportType: The .NET `Citrix.StoreFront.Model.Store.TransportType` value type

### System.Int32

Parameter SSLRelayPort: The .NET `System.Int32` value type

### System.Boolean

Parameter LoadBalance: The .NET `System.Boolean` value type

### System.Int32

Parameter AllFailedBypassDuration: The .NET `System.Int32` value type

### System.Int32

Parameter BypassDuration: The .NET `System.Int32` value type

### System.String

Parameter FriendlyName: The .NET `System.String` reference type

### System.String[]

Parameter Zones: The .NET `System.String` reference type

### System.String

Parameter ConnectionString: The .NET `System.String` reference type

## Return Values

### StoreService

A .NET class representing the configuration of a StoreFront Store service

## Examples

### EXAMPLE 1 Create a new Store

```
Add-STFStoreService -VirtualPath /Citrix/Store -AuthenticationService $authenticationService -FarmName "Controller" -FarmType XenApp -Servers xenapp1, xenapp2
```

**REMARKS**

Creates a new Store using an existing Authentication Service
