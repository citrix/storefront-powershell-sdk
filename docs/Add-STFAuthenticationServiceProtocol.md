#Add-STFAuthenticationServiceProtocol
Add an authentication protocol to an Authentication service
##Syntax
```Add-STFAuthenticationServiceProtocol [-Name] <String[]> [-AuthenticationService] <AuthenticationService> [<CommonParameters>]
```
##Detailed Description
Adds one or more authentication protocols to the specified Authentication service.
##Related Commands
*[Get-STFAuthenticationProtocolsAvailable](Get-STFAuthenticationProtocolsAvailable)
*[Remove-STFAuthenticationServiceProtocol](Remove-STFAuthenticationServiceProtocol)
*[Enable-STFAuthenticationServiceProtocol](Enable-STFAuthenticationServiceProtocol)
*[Disable-STFAuthenticationServiceProtocol](Disable-STFAuthenticationServiceProtocol)
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||Name|The name of the authentication protocol.|true|false||AuthenticationService|The Authentication service to add the feature to.|true|true (ByValue)|##Input Type
###System.String[]
Parameter Name: The .NET 'System.String' reference type
###Citrix.StoreFront.Model.Authentication.AuthenticationService
Parameter AuthenticationService: A .NET class representing the configuration of a StoreFront Authentication service
##Return Values
##Examples
###EXAMPLE 1 Add an authentication protocol
```$authentication = Get-STFAuthenticationService
Add-STFAuthenticationServiceProtocol -Name CustomProtocol -AuthenticationService $authentication
```
REMARKS

Add the protocol "CustomProtocol" to the Authentication service $authentication
