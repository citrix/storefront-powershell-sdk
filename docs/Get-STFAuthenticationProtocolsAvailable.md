# Get-STFAuthenticationProtocolsAvailable

Get the installed authentication protocols

## Syntax

```
Get-STFAuthenticationProtocolsAvailable [<CommonParameters>]
```

## Detailed Description

An authentication service can support a number of authentication methods. The command gets a list of the methods that can be added or removed to\from an authentication service.

## Related Commands

* [Add-STFAuthenticationServiceProtocol](Add-STFAuthenticationServiceProtocol.md)
* [Get-STFAuthenticationServiceProtocol](Get-STFAuthenticationServiceProtocol.md)

## Input Type

### 



## Return Values

### String

The .NET `System.String` reference type

## Examples

### EXAMPLE 1 Get the available authentication protocols

```
Get-STFAuthenticationProtocolsAvailable
```

**REMARKS**

Get the authentication protocols currently installed.

**OUTPUT**

```
CitrixAGBasic
HttpBasic
CitrixFederation
Certificate
IntegratedWindows
ExplicitForms
```
