# Set-STFExplicitCommonOptions

Set the ExplicitCommon protocol options

## Syntax

```
Set-STFExplicitCommonOptions [-AuthenticationService] <AuthenticationService> [[-Domains] <String[]>] [[-DefaultDomain] <String>] [[-HideDomainField] <Boolean>] [[-AllowUserPasswordChange] <Always | ExpiredOnly | Never>] [[-ShowPasswordExpiryWarning] <Never | Windows | Custom>] [[-PasswordExpiryWarningPeriod] <Int32>] [[-AllowZeroLengthPassword] <Boolean>] [<CommonParameters>]
```

## Detailed Description

Set the ExplicitCommon Authentication service protocol options.

## Related Commands

* [Get-STFExplicitCommonOptions](./Get-STFExplicitCommonOptions)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|AuthenticationService|The Authentication service to set the ExplicitCommon options for|true|true (ByValue)| |
|Domains|List of trusted domains|false|false| |
|DefaultDomain|The default domain to use when omitted during login|false|false| |
|HideDomainField|Hide the domain field on the login form|false|false| |
|AllowUserPasswordChange|Configure when a user can change a password|false|false| |
|ShowPasswordExpiryWarning|Show the password expiry warning to the user|false|false| |
|PasswordExpiryWarningPeriod|The period of time in days before the expiry warning should be shown|false|false| |
|AllowZeroLengthPassword|Allow a zero length password|false|false| |

## Input Type

### Citrix.StoreFront.Model.Authentication.AuthenticationService

Parameter AuthenticationService: A .NET class representing the configuration of a StoreFront Authentication service

### System.String[]

Parameter Domains: The .NET `System.String` reference type

### System.String

Parameter DefaultDomain: The .NET `System.String` reference type

### System.Boolean

Parameter HideDomainField: The .NET `System.Boolean` value type

### Citrix.StoreFront.Model.Authentication.PasswordChange

Parameter AllowUserPasswordChange: The .NET `Citrix.StoreFront.Model.Authentication.PasswordChange` value type

### Citrix.StoreFront.Model.Authentication.PasswordExpiryWarning

Parameter ShowPasswordExpiryWarning: The .NET `Citrix.StoreFront.Model.Authentication.PasswordExpiryWarning` value type

### System.Int32

Parameter PasswordExpiryWarningPeriod: The .NET `System.Int32` value type

### System.Boolean

Parameter AllowZeroLengthPassword: The .NET `System.Boolean` value type

## Return Values

### None

## Examples

### EXAMPLE 1 Set the ExplicitCommon protocol options

```
$authentication = Get-STFAuthenticationService
Set-STFExplicitCommonOptions -AuthenticationService $authentication -Domains @("Alpha","Beta","Capa") -DefaultDomain Alpha -HideDomainField $true -AllowChangePassword Always -ShowPasswordExpiryWarning Windows -PasswordExpiryWarningPeriod 10
```

**REMARKS**

Sets the ExplicitCommon options on the only configured authentication service.
