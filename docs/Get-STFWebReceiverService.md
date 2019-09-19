# Get-STFWebReceiverService

Get Receiver for Web service

## Syntax

```
Get-STFWebReceiverService [[-VirtualPath] <String>] [[-SiteId] <Int64>] [<CommonParameters>]



Get-STFWebReceiverService [-StoreService] <StoreService> [[-VirtualPath] <String>] [[-SiteId] <Int64>] [<CommonParameters>]



Get-STFWebReceiverService [-AuthenticationService] <AuthenticationService> [[-VirtualPath] <String>] [[-SiteId] <Int64>] [<CommonParameters>]
```

## Detailed Description

Get the Receiver for Web services that match the supplied IIS site id, virtual path or are connected to the supplied Store or Authentication service.

## Related Commands

* [Add-STFWebReceiverService](Add-STFWebReceiverService.md)
* [Remove-STFWebReceiverService](Remove-STFWebReceiverService.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|VirtualPath|Virtual path filter|false|false| |
|SiteId|IIS site id filter|false|false| |
|StoreService|Store service filter|true|true (ByValue)| |
|AuthenticationService|Authentication service filter|true|false| |

## Input Type

### System.String

Parameter VirtualPath: The .NET `System.String` reference type

### System.Int64

Parameter SiteId: The .NET `System.Int64` value type

### Citrix.StoreFront.Model.Store.StoreService

Parameter StoreService: A .NET class representing the configuration of a StoreFront Store service

### Citrix.StoreFront.Model.Authentication.AuthenticationService

Parameter AuthenticationService: A .NET class representing the configuration of a StoreFront Authentication service

## Return Values

### WebReceiverService

A .NET class representing the configuration of a StoreFront Web Receiver service

## Examples

### EXAMPLE 1 Get Receiver for Web services

```
Get-STFWebReceiverService
```

**REMARKS**

Get all configured Receiver for Web services.

**OUTPUT**

```
WebReceiver                      : 
Citrix.StoreFront.Model.ReceiverForWeb.WebReceiver
ServiceId                        : 80fb5f9f-0d10-4cdf-ad1e-d36723afc33a
ProducerService                  : Receiver for Web Token Producer
ConsumerService                  : Receiver for Web Token Consumer
ServiceTokenCertificate          : F968ABF7298DB23DF9B1446C01AE7886F1BD24C9
AuthenticationServiceVirtualPath : /Citrix/StoreAuth
StoreServiceVirtualPath          : /Citrix/Store
SiteId                           : 1
VirtualPath                      : /Citrix/StoreWeb
FriendlyName                     : /Citrix/StoreWeb
Hmacs                            : {appShortcuts:waN9widXd9HfoYgORoocOM5FvW8RwD
KQcQlO+Nxu4RfDcJVBm5BKotkRn1M61AvBgQDRhX
                                   y5vmfafC7XyvWKrw==, 
rfWebGeneric:3s49B/XhMQhzhmqcjV8O9qttDQM/91Syp7VMoe7vGx69ousmpd7
                                   vag7qWjWj8IQuQO2+gQjawxaqQXDdsw9khw==}
Certificates                     : {F968ABF7298DB23DF9B1446C01AE7886F1BD24C9, 
DED6AB26AF47C2A7AD8E33D00924B5019A6AA2AD}
TokenManagers                    : {Receiver for Web Token Producer, Receiver 
for Web Token Consumer}
Routing                          : :
ServiceRef                       : 1__Citrix_StoreWeb
ConfigurationFile                : 
C:\inetpub\wwwroot\Citrix\StoreWeb\web.config
TenantId                         : 860e9401-39c8-4f2c-928d-34251102b840
```
