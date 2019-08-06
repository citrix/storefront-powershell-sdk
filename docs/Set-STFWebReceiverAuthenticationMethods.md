# Set-STFWebReceiverAuthenticationMethods

Set the WebReceiver authentication methods

## Syntax

```
Set-STFWebReceiverAuthenticationMethods [-WebReceiverService] <WebReceiverService> [[-AuthenticationMethods] <String[]>] [[-TokenLifeTime] <TimeSpan>] [<CommonParameters>]
```

## Detailed Description

Sets the list of allowed authentication methods for a given Web Receiver site. The accepted authentication method names are:


"ExplicitForms" - explicit authentication with user credentials


"IntegratedWindows" - domain pass - through authentication


"Certificate" - smart card authentication


"CitrixAGBasic" - NetScaler Gateway single sign - on




This cmdlet is typically used to restrict the authentication methods enabled for a Web Receiver


site to a subset of those enabled for its associated Authentication service.




Note, a Web Receiver authentication method is only effective when enabled for both the Web Receiver


site and its associated Authentication service.

## Related Commands

* [Get-STFWebReceiverAuthenticationMethods](Get-STFWebReceiverAuthenticationMethods.md)
* [Get-STFWebReceiverAuthenticationMethodsAvailable](Get-STFWebReceiverAuthenticationMethodsAvailable.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|WebReceiverService|The WebReceiver service.|true|true (ByValue)| |
|AuthenticationMethods|Authentication methods to support|false|false| |
|TokenLifeTime|The lifetime of the authentication token before it expiries.|false|false| |

## Input Type

### Citrix.StoreFront.Model.ReceiverForWeb.WebReceiverService

Parameter WebReceiverService: A .NET class representing the configuration of a StoreFront Web Receiver service

### System.String[]

Parameter AuthenticationMethods: The .NET `System.String` reference type

### System.TimeSpan

Parameter TokenLifeTime: The .NET `System.TimeSpan` value type

## Return Values

### None

## Examples

### EXAMPLE 1 Set authentication methods

```
$webReceiver = Get-STFWebReceiverService "/Citrix/StoreWeb"
Set-STFWebReceiverAuthenticationMethods -WebReceiverService $webReceiver -AuthenticationMethods Get-STFWebReceiverAuthenticationMethodsAvailable
```

**REMARKS**

Set the current WebReceiver authentication methods for /Citrix/StoreWeb to be 

all those available.
