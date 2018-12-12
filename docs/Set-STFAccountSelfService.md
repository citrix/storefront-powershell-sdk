# Set-STFAccountSelfService

Sets Account self-service options

## Syntax

```
Set-STFAccountSelfService [-AuthenticationService <AuthenticationService>] [-ManagerFactoryName <String>] [-DefaultManagerFactory <SwitchParameter>] [-AllowResetPassword <Boolean>] [-AllowUnlockAccount <Boolean>] [<CommonParameters>]
```

## Detailed Description

Sets the options of the Account self-service on a given Authentication service.

## Related Commands

* [Get-STFAccountSelfService](./Get-STFAccountSelfService)
* [Get-STFAuthenticationServicePasswordManagerAccountSelfService](./Get-STFAuthenticationServicePasswordManagerAccountSelfService)
* [Set-STFAuthenticationServicePasswordManagerAccountSelfService](./Set-STFAuthenticationServicePasswordManagerAccountSelfService)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|AuthenticationService|The Authentication service to which Account Self-Service settings will be applied to.|true|true (ByValue)| |
|ManagerFactoryName|The Account self-service factory to use for the Authentication service.|false|false| |
|DefaultManagerFactory|Set the default account self-service method, which is to disable account self-service.|false|false| |
|AllowResetPassword|Allow self-service reset password.|false|false| |
|AllowUnlockAccount|Allow self-service account unlock.|false|false| |

## Input Type

### Citrix.StoreFront.Model.Authentication.AuthenticationService

Parameter AuthenticationService: A .NET class representing the configuration of a StoreFront Authentication service

### System.String

Parameter ManagerFactoryName: The .NET `System.String` reference type

### System.Management.Automation.SwitchParameter

Parameter DefaultManagerFactory: The .NET `System.Management.Automation.SwitchParameter` value type

### System.Boolean

Parameter AllowResetPassword: The .NET `System.Boolean` value type

### System.Boolean

Parameter AllowUnlockAccount: The .NET `System.Boolean` value type

## Return Values

### None

## Examples

### EXAMPLE 1 Configure Account Self-Service

```
$auth = Get-STFAuthenticationService
Set-STFAuthenticationServiceAccountSelfService -AuthenticationService $auth
```

**REMARKS**

Configure the single authentication service to use Account self-service 'passwordManagerSelfServiceAccountManagement' factory.

### EXAMPLE 2 Remove Account Self-Service

```
$auth = Get-STFAuthenticationService
Set-STFAuthenticationServiceAccountSelfService -AuthenticationService $auth -DefaultManagerFactory
```

**REMARKS**

Configure the single authentication service to not use account self-service.
