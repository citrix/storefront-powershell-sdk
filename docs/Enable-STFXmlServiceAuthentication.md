# Enable-STFXmlServiceAuthentication

Set explicit Xml Service based authentication

## Syntax

```
Enable-STFXmlServiceAuthentication [-AuthenticationService] <AuthenticationService> [-Farm] <Farm[]> [<CommonParameters>]
```

## Detailed Description

Sets authenticating user name password credentials to utilize XenApp/XenDesktop Delivery Controllers.

## Related Commands

* [Set-STFExplicitAuthenticator](./Set-STFExplicitAuthenticator)
* [Get-STFExplicitAuthenticator](./Get-STFExplicitAuthenticator)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|AuthenticationService|The Authentication service for which Xml Service authentication is to be configured for|true|true (ByValue)| |
|Farm|The collection of farms to use for authentication|true|false| |

## Input Type

### Citrix.StoreFront.Model.Authentication.AuthenticationService

Parameter AuthenticationService: A .NET class representing the configuration of a StoreFront Authentication service

### Citrix.StoreFront.Model.Store.Farm[]

Parameter Farm: A .NET class representing the configuration of a Farm in StoreFront Store service

## Return Values

### None

## Examples

### EXAMPLE 1 Enable Xml Service Authentication

```
$store = Get-STFStoreService
$auth = Get-STFAuthenticationService
$farm = Get-STFStoreFarm -StoreService $store -FarmName "Controller"
Set-STFAuthenticationServiceXmlServiceAuthentication -AuthenticationService $auth -UseXmlServiceAuthentication $true -Farm $farm
```

**REMARKS**

Configure the authentication service to use Xml Service authentication using a farm configured in the store. Use Get-STFExplicitAuthenticator to determine if XmlService authentication is configured.
