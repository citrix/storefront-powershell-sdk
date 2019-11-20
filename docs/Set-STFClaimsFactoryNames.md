# Set-STFClaimsFactoryNames

Sets all the claims factory names.

## Syntax

```
Set-STFClaimsFactoryNames -ClaimsFactoryName <String> -AuthenticationService <AuthenticationService> [<CommonParameters>]
```

## Detailed Description

Sets all the claims factory names.

## Related Commands


## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|ClaimsFactoryName|The name of the claims factory to use|true|true (ByValue)| |
|AuthenticationService|The authentication service to update|true|true (ByValue)| |

## Input Type

### System.String

Parameter ClaimsFactoryName: The .NET `System.String` reference type

### Citrix.StoreFront.Model.Authentication.AuthenticationService

Parameter AuthenticationService: A .NET class representing the configuration of a StoreFront Authentication service

## Return Values

### None

## Examples

### EXAMPLE 1 Simple example

```
Set-STFClaimsFactoryNames -AuthenticationService $authenticationService -ClaimsFactoryName 'FASClaimsFactory'
```

**REMARKS**

This example sets all the claims factory names to be: FASClaimsFactory in the specified authentication service.
