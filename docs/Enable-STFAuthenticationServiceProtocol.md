# Enable-STFAuthenticationServiceProtocol

Enable an authentication protocol

## Syntax

```
Enable-STFAuthenticationServiceProtocol [-Name] <String[]> [-AuthenticationService] <AuthenticationService> [<CommonParameters>]
```

## Detailed Description

Enable one or more authentication protocols on the specified Authentication service.

## Related Commands

* [Remove-STFAuthenticationServiceProtocol](Remove-STFAuthenticationServiceProtocol.md)
* [Disable-STFAuthenticationServiceProtocol](Disable-STFAuthenticationServiceProtocol.md)
* [Get-STFAuthenticationProtocolsAvailable](Get-STFAuthenticationProtocolsAvailable.md)
* [Add-STFAuthenticationServiceProtocol](Add-STFAuthenticationServiceProtocol.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|Name|The name of the protocol to enable|true|false| |
|AuthenticationService|The Authentication service the protocol should be enabled for|true|true (ByValue)| |

## Input Type

### System.String[]

Parameter Name: The .NET `System.String` reference type

### Citrix.StoreFront.Model.Authentication.AuthenticationService

Parameter AuthenticationService: A .NET class representing the configuration of a StoreFront Authentication service

## Return Values

### None

## Examples

### EXAMPLE 1 Enable all authentication protocols

```
Enable-STFAuthenticationServiceProtocol -Name (Get-STFAuthenticationProtocolsAvailable) -AuthenticationService (Get-STFAuthenticationService)
```

**REMARKS**

Enable all authentication protocols for the only configured Authentication 

service.

### EXAMPLE 2 Enable authentication protocol

```
Enable-STFAuthenticationServiceProtocol -Name HttpBasic -AuthenticationService (Get-STFAuthenticationService)
```

**REMARKS**

Enable the HttpBasic authentication protocol.
