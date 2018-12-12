# Get-STFAccountSelfService

Gets the Account self-service configuration

## Syntax

```
Get-STFAccountSelfService [-AuthenticationService] <AuthenticationService> [<CommonParameters>]
```

## Detailed Description

Gets the Account self-service configuration from the Authentication service.

## Related Commands

* [Set-STFAccountSelfService](./Set-STFAccountSelfService)
* [Get-STFPasswordManagerAccountSelfService](./Get-STFPasswordManagerAccountSelfService)
* [Set-STFPasswordManagerAccountSelfService](./Set-STFPasswordManagerAccountSelfService)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|AuthenticationService|The Authentication service for which account self-service settings will be supplied|true|true (ByValue)| |

## Input Type

### Citrix.StoreFront.Model.Authentication.AuthenticationService

Parameter AuthenticationService: A .NET class representing the configuration of a StoreFront Authentication service

## Return Values

### AccountSelfServiceSummary

The .NET `Citrix.StoreFront.Model.Authentication.AccountSelfServiceSummary` reference type

## Examples

### EXAMPLE 1 Get Account self-service settings

```
$auth = Get-STFAuthenticationService
Get-STFAuthenticationServiceAccountSelfService -AuthenticationService $auth
```

**REMARKS**

Get the Account self-service details for the only configured Authentication service.
