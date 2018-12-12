# Remove-STFAuthenticationService

Removes an Authentication service

## Syntax

```
Remove-STFAuthenticationService [-AuthenticationService] <AuthenticationService> [<CommonParameters>]
```

## Detailed Description

Remove an existing Authentication service.

## Related Commands


## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|AuthenticationService|Authentication service to remove|true|true (ByValue)| |

## Input Type

### Citrix.StoreFront.Model.Authentication.AuthenticationService

Parameter AuthenticationService: A .NET class representing the configuration of a StoreFront Authentication service

## Return Values

### AuthenticationService

A .NET class representing the configuration of a StoreFront Authentication service

## Examples

### EXAMPLE 1 Remove an Authentication Service

```
Remove-STFAuthenticationService (Get-STFAuthenticationService)
```

**REMARKS**

Removes the specified Authentication service
