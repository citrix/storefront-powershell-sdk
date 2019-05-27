# Get-STFExplicitCommonOptions

Get the ExplicitCommon protocol options

## Syntax

```
Get-STFExplicitCommonOptions [-AuthenticationService] <AuthenticationService> [<CommonParameters>]
```

## Detailed Description

Get the ExplicitCommon Authentication service protocol options.

## Related Commands

* [Set-STFExplicitCommonOptions](Set-STFExplicitCommonOptions.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|AuthenticationService|The Authentication service from which to get the ExplicitCommon options|true|true (ByValue)| |

## Input Type

### Citrix.StoreFront.Model.Authentication.AuthenticationService

Parameter AuthenticationService: A .NET class representing the configuration of a StoreFront Authentication service

## Return Values

### ExplicitBL

The .NET `Citrix.StoreFront.Model.Authentication.ExplicitBL` reference type

## Examples

### EXAMPLE 1 Get ExplicitCommon protocol options

```
$authentication = Get-STFAuthenticationService
Get-STFExplicitCommonOptions - AuthenticationService $authentication
```

**REMARKS**

Get the ExplicitCommon options from the specified Authentication service

**OUTPUT**

```
Authenticator               : defaultDelegatedAuthenticator
HideDomainField             : True
AllowUserPasswordChange     : Never
AllowZeroLengthPassword     : False
ShowPasswordExpiryWarning   : Windows
PasswordExpiryWarningPeriod : 10
RequireAccountSIDs          : True
DomainSelection             : {}
```
