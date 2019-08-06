# Get-STFCitrixAGBasicOptions

Get the CitrixAGBasic protocol options

## Syntax

```
Get-STFCitrixAGBasicOptions [-AuthenticationService] <AuthenticationService> [<CommonParameters>]
```

## Detailed Description

Get the CitrixAGBasic Authentication service protocol options.

## Related Commands

* [Set-STFCitrixAGBasicOptions](Set-STFCitrixAGBasicOptions.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|AuthenticationService|The Authentication service from which to get the CitrixAGBasic options|true|true (ByValue)| |

## Input Type

### Citrix.StoreFront.Model.Authentication.AuthenticationService

Parameter AuthenticationService: A .NET class representing the configuration of a StoreFront Authentication service

## Return Values

### NetscalerAuthentication

The .NET `Citrix.StoreFront.Model.Authentication.NetscalerAuthentication` reference type

## Examples

### EXAMPLE 1 Get CitrixAGBasic protocol options

```
$authentication = Get-STFAuthenticationService
Get-STFCitrixAGBasicOptions -AuthenticationService $authentication
```

**REMARKS**

Get the CitrixAGBasic options from the specified Authentication service

**OUTPUT**

```
CredentialValidationMode NetscalerGateways
------------------------ -----------------
            Password {}
```
