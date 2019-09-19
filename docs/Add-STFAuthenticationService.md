# Add-STFAuthenticationService

Create a new Authentication service

## Syntax

```
Add-STFAuthenticationService [-VirtualPath] <String> [[-SiteId] <Int64>] [[-FriendlyName] <String>] [<CommonParameters>]
```

## Detailed Description

Create a new Authentication service for Store and Receiver for Web authentication.

## Related Commands

* [Remove-STFAuthenticationService](Remove-STFAuthenticationService.md)
* [Get-STFAuthenticationService](Get-STFAuthenticationService.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|VirtualPath|The IIS virtual path to use for the service|true|false| |
|SiteId|The IIS site to configure the Authentication service for|false|false| |
|FriendlyName|The friendly name the service should be known as|false|false| |

## Input Type

### System.String

Parameter VirtualPath: The .NET `System.String` reference type

### System.Int64

Parameter SiteId: The .NET `System.Int64` value type

### System.String

Parameter FriendlyName: The .NET `System.String` reference type

## Return Values

### AuthenticationService

A .NET class representing the configuration of a StoreFront Authentication service

## Examples

### EXAMPLE 1 Create a new Authentication service

```
Add-STFAuthenticationService /Citrix/Authentication
```

**REMARKS**

Create a new Authentication service at the /Citrix/Authentication virtual path.

**OUTPUT**

```
ProducerService         : Authentication Token Producer
ServiceTokenCertificate : ECC1138839039C2AE7DBA4B49CEA8984E0B4ABBD
TokenValidationService  : Default Token Validation Service
TokenIssuerUrl          : 
http://example.storefront.com/Citrix/Authentication/auth/v1/token
AuthenticationOptions   : Logging Level:None, Hide Errors:False, Collect 
Evidence to send to FAS:False
Authentication          : TokenServiceId:0f2216a5-4f82-4560-a5a7-2b7dd4ac5593, 
Protocol Choices:7
AuthenticationProtocols : {[citrixAGBasicAuthentication,
                          
Citrix.StoreFront.Model.Authentication.NetscalerAuthentication], 
[formsProtocol,
                          
Citrix.StoreFront.Model.Authentication.FormsProtocol], [explicitBL,
                          
Citrix.StoreFront.Model.Authentication.ExplicitAuthentication],
                          [delegatedDirectoryClaimFactory,
                          
Citrix.StoreFront.Model.Authentication.DelegatedDirectorySettings]}
PnaAuthentication       : 
Citrix.StoreFront.Model.Authentication.PnaAuthentication
SiteId                  : 1
VirtualPath             : /Citrix/Authentication
FriendlyName            : Authentication Service
Hmacs                   : {}
Certificates            : {ECC1138839039C2AE7DBA4B49CEA8984E0B4ABBD}
TokenManagers           : {Authentication Token Producer, Default Token 
Validation Service}
Routing                 : Authentication Service:http://example.storefront.com/
ServiceRef              : 1__Citrix_Authentication
ConfigurationFile       : C:\inetpub\wwwroot\Citrix\Authentication\web.config
TenantId                : 860e9401-39c8-4f2c-928d-34251102b840
```
