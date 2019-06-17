# Get-STFExplicitAuthenticator

Get the password validator

## Syntax

```
Get-STFExplicitAuthenticator [-AuthenticationService] <AuthenticationService> [<CommonParameters>]
```

## Detailed Description

Gets the password validator configuration.

## Related Commands

* [Set-STFExplicitAuthenticator](Set-STFExplicitAuthenticator.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|AuthenticationService|The Authentication service for which Password Validator settings will be output.|true|true (ByValue)| |

## Input Type

### Citrix.StoreFront.Model.Authentication.AuthenticationService

Parameter AuthenticationService: A .NET class representing the configuration of a StoreFront Authentication service

## Return Values

### String

The .NET `System.String` reference type

## Examples

### EXAMPLE 1 Get Password Validator settings

```
$auth = Get-STFAuthenticationService
Get-STFExplicitAuthenticator -AuthenticationService $auth
```

**REMARKS**

Get the password validator settings for the Authentication service.
