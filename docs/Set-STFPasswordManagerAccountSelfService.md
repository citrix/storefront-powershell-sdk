#Set-STFPasswordManagerAccountSelfService
Sets Password Manager as the account self-service method
##Syntax
```Set-STFPasswordManagerAccountSelfService [-AuthenticationService] <AuthenticationService> [-PasswordManagerServiceUrl] <Uri> [<CommonParameters>]
```
##Detailed Description
Sets the Password Manager as the account self-service method (Password Reset).
##Related Commands
*[Get-STFPasswordManagerAccountSelfService](Get-STFPasswordManagerAccountSelfService)
*[Get-STFAccountSelfService](Get-STFAccountSelfService)
*[Set-STFAccountSelfService](Set-STFAccountSelfService)
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||AuthenticationService|The Authentication service for which Password Manager will be enabled.|true|true (ByValue)||PasswordManagerServiceUrl|The Url of the password manager account self-service service.|true|false|##Input Type
###Citrix.StoreFront.Model.Authentication.AuthenticationService
Parameter AuthenticationService: A .NET class representing the configuration of a StoreFront Authentication service
###System.Uri
Parameter PasswordManagerServiceUrl: The .NET 'System.Uri' reference type
##Return Values
##Examples
###EXAMPLE 1 Enable Password Manager
```$auth = Get-STFAuthenticationService
Set-STFAuthenticationServicePasswordManagerAccountSelfService -AuthenticationService $auth
```
REMARKS

Configure the single authentication service to use Password Manager for account self-service.
