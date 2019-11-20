# Set-STFCitrixAGBasicOptions

Set the CitrixAGBasic protocol options

## Syntax

```
Set-STFCitrixAGBasicOptions [-CredentialValidationMode] <Password | Kerberos | Auto> [-AuthenticationService] <AuthenticationService> [<CommonParameters>]



Set-STFCitrixAGBasicOptions [-PasswordRequired] <Boolean> [-AuthenticationService] <AuthenticationService> [<CommonParameters>]
```

## Detailed Description

Set the CitrixAGBasic Authentication service protocol options.

## Related Commands

* [Set-STFCitrixAGBasicOptions](./Set-STFCitrixAGBasicOptions)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|AuthenticationService|The Authentication service from which to get the CitrixAGBasic options|true|true (ByValue)| |
|CredentialValidationMode|The credential validation mode to use for authentication|true|false| |
|PasswordRequired|Password required for authentication|true|false| |

## Input Type

### Citrix.StoreFront.Model.Authentication.AuthenticationService

Parameter AuthenticationService: A .NET class representing the configuration of a StoreFront Authentication service

### Citrix.StoreFront.Model.Authentication.CredentialValidationMode

Parameter CredentialValidationMode: The .NET `Citrix.StoreFront.Model.Authentication.CredentialValidationMode` value type

### System.Boolean

Parameter PasswordRequired: The .NET `System.Boolean` value type

## Return Values

### None

## Examples

### EXAMPLE 1 Set CredentialValidationMode to password

```
$authentication = Get-STFAuthenticationService
Set-STFCitrixAGBasicOptions -AuthenticationService $authentication -CredentialValidationMode Password
```

**REMARKS**

Sets the CitrixAGBasic CredentialValidationMode to password on the only configured authentication service.
