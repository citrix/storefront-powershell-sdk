#Set-STFExplicitAuthenticator
Sets the password validator
##Syntax
```Set-STFExplicitAuthenticator [-AuthenticationService <AuthenticationService>] [-DefaultManagerFactory <SwitchParameter>] [-AuthenticationService] <AuthenticationService> [[-DefaultManagerFactory] <SwitchParameter>] [[-Name] <String>] [<CommonParameters>]
Set-STFExplicitAuthenticator [-AuthenticationService <AuthenticationService>] [-Name <String>] [-AuthenticationService] <AuthenticationService> [[-DefaultManagerFactory] <SwitchParameter>] [[-Name] <String>] [<CommonParameters>]
```
##Detailed Description
Sets the password validator used for explicit configuration.
##Related Commands
*[Get-STFExplicitAuthenticator](Get-STFExplicitAuthenticator)
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||AuthenticationService|The Authentication service for which Explicit authentication settings will be configured.|true|true (ByValue)||DefaultManagerFactory|Set the default password validator to be Delegated Authentication.|false|false||Name|The name of the authenticator to use for Explicit authentication.|false|false|##Input Type
###Citrix.StoreFront.Model.Authentication.AuthenticationService
Parameter AuthenticationService: A .NET class representing the configuration of a StoreFront Authentication service
###System.Management.Automation.SwitchParameter
Parameter DefaultManagerFactory: The .NET 'System.Management.Automation.SwitchParameter' value type
###System.String
Parameter Name: The .NET 'System.String' reference type
##Return Values
##Examples
###EXAMPLE 1 Set Password Validator
```$auth = Get-STFAuthenticationService
Set-STFExplicitAuthenticator -AuthenticationService $auth -Name "xmlServiceAuthenticator"
```
REMARKS

Configure the single authentication service to use the XmlService authenticator for explict authentication.
###EXAMPLE 2 Reset Password Validator
```$auth = Get-STFAuthenticationService
Set-STFExplicitAuthenticator -AuthenticationService $auth -DefaultManagerFactory
```
REMARKS

Configure the single authentication service to use the default authenticator for explict authentication.
