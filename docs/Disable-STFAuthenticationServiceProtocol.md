# Disable-STFAuthenticationServiceProtocol

Disable an authentication protocol

## Syntax

```
Disable-STFAuthenticationServiceProtocol [-Name] <String[]> [-AuthenticationService] <AuthenticationService> [<CommonParameters>]
```

## Detailed Description

Disable one or more authentication protocols on the specified Authentication service.

## Related Commands

* [Enable-STFAuthenticationServiceProtocol](Enable-STFAuthenticationServiceProtocol.md)
* [Remove-STFAuthenticationServiceProtocol](Remove-STFAuthenticationServiceProtocol.md)
* [Get-STFAuthenticationProtocolsAvailable](Get-STFAuthenticationProtocolsAvailable.md)
* [Add-STFAuthenticationServiceProtocol](Add-STFAuthenticationServiceProtocol.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|Name|The name of the protocol to disable|true|false| |
|AuthenticationService|The Authentication service the protocol should be disabled for|true|true (ByValue)| |

## Input Type

### System.String[]

Parameter Name: The .NET `System.String` reference type

### Citrix.StoreFront.Model.Authentication.AuthenticationService

Parameter AuthenticationService: A .NET class representing the configuration of a StoreFront Authentication service

## Return Values

### None

## Examples

### EXAMPLE 1 Disable all authentication protocols

```
Disable-STFAuthenticationServiceProtocol -Name (Get-STFAuthenticationProtocolsAvailable) -AuthenticationService (Get-STFAuthenticationService)
```

**REMARKS**

Disable all authentication protocols for the only configured Authentication 

service.

### EXAMPLE 2 Disable authentication protocol

```
Disable-STFAuthenticationServiceProtocol -Name HttpBasic -AuthenticationService (Get-STFAuthenticationService)
```

**REMARKS**

Disable the HttpBasic authentication protocol.
