# Get-STFWebReceiverAuthenticationManager

Get the WebReceiver Authentication Manager options

## Syntax

```
Get-STFWebReceiverAuthenticationManager [-WebReceiverService] <WebReceiverService> [<CommonParameters>]
```

## Detailed Description

Get the WebReceiver Authentication Manager client options.

## Related Commands

* [Set-STFWebReceiverAuthenticationManager](Set-STFWebReceiverAuthenticationManager.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|WebReceiverService|The WebReceiver service.|true|true (ByValue)| |

## Input Type

### Citrix.StoreFront.Model.ReceiverForWeb.WebReceiverService

Parameter WebReceiverService: A .NET class representing the configuration of a StoreFront Web Receiver service

## Return Values

### AuthManager

The .NET `Citrix.StoreFront.Model.ReceiverForWeb.AuthManager` reference type

## Examples

### EXAMPLE 1 Get WebReceiver Authentication options

```
$receiver = Get-STFWebReceiverService
Get-STFWebReceiverAuthenticationManager -WebReceiverService $receiver
```

**REMARKS**

Get the WebReceiver Authentication Manager options of the only configured 

WebReceiver.

**OUTPUT**

```
GetUserNameUrl       : Authentication/GetUserName
LogoffUrl            : Authentication/Logoff
ChangeCredentialsUrl : ExplicitAuth/GetChangeCredentialForm
LoginFormTimeout     : 5
```
