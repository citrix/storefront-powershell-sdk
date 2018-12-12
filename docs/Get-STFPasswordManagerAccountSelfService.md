# Get-STFPasswordManagerAccountSelfService

Gets the Password Manager account self-service method

## Syntax

```
Get-STFPasswordManagerAccountSelfService [-AuthenticationService] <AuthenticationService> [<CommonParameters>]
```

## Detailed Description

Gets the Password Manager account self-service method (Password Reset).

## Related Commands

* [Set-STFPasswordManagerAccountSelfService](./Set-STFPasswordManagerAccountSelfService)
* [Get-STFAccountSelfService](./Get-STFAccountSelfService)
* [Set-STFAccountSelfService](./Set-STFAccountSelfService)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|AuthenticationService|The Authentication service for which Password Manager settings will be supplied.|true|true (ByValue)| |

## Input Type

### Citrix.StoreFront.Model.Authentication.AuthenticationService

Parameter AuthenticationService: A .NET class representing the configuration of a StoreFront Authentication service

## Return Values

### String

The .NET `System.String` reference type

## Examples

### EXAMPLE 1 Get Password Manager settings

```
$auth = Get-STFAuthenticationService
Get-STFAuthenticationServicePasswordManagerAccountSelfService -AuthenticationService $auth
```

**REMARKS**

Get the Password Manager settings for account self-service.
