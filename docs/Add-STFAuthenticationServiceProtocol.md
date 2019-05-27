# Add-STFAuthenticationServiceProtocol

Add an authentication protocol to an Authentication service

## Syntax

```
Add-STFAuthenticationServiceProtocol [-Name] <String[]> [-AuthenticationService] <AuthenticationService> [<CommonParameters>]
```

## Detailed Description

Adds one or more authentication protocols to the specified Authentication service.

## Related Commands

* [Get-STFAuthenticationProtocolsAvailable](Get-STFAuthenticationProtocolsAvailable.md)
* [Remove-STFAuthenticationServiceProtocol](Remove-STFAuthenticationServiceProtocol.md)
* [Enable-STFAuthenticationServiceProtocol](Enable-STFAuthenticationServiceProtocol.md)
* [Disable-STFAuthenticationServiceProtocol](Disable-STFAuthenticationServiceProtocol.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|Name|The name of the authentication protocol.|true|false| |
|AuthenticationService|The Authentication service to add the feature to.|true|true (ByValue)| |

## Input Type

### System.String[]

Parameter Name: The .NET `System.String` reference type

### Citrix.StoreFront.Model.Authentication.AuthenticationService

Parameter AuthenticationService: A .NET class representing the configuration of a StoreFront Authentication service

## Return Values

### None

## Examples

### EXAMPLE 1 Add an authentication protocol

```
$authentication = Get-STFAuthenticationService
Add-STFAuthenticationServiceProtocol -Name CustomProtocol -AuthenticationService $authentication
```

**REMARKS**

Add the protocol "CustomProtocol" to the Authentication service $authentication
