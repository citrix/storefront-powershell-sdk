#Get-STFAuthenticationServiceProtocol
Get authentication protocols
##Syntax
```Get-STFAuthenticationServiceProtocol [-AuthenticationService] <AuthenticationService> [<CommonParameters>]
```
##Detailed Description
Gets the authentication protocols configured for a specified Authentication service.
##Related Commands
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||AuthenticationService|The Authentication service from which to get the protocols installed|true|true (ByValue)|##Input Type
###Citrix.StoreFront.Model.Authentication.AuthenticationService
Parameter AuthenticationService: A .NET class representing the configuration of a StoreFront Authentication service
##Return Values
###AuthenticationProtocolChoice
A .NET class representing an Authentication protocol offered by an Authentication service
##Examples
###EXAMPLE 1 Get the authentication protocols
```Get-STFAuthenticationServiceProtocol (Get-STFAuthenticationService)
```
REMARKS

Get the protocols configured for the only Authentication service.
OUTPUT
```Name                                                                    Enabled ChoiceProperties
----                                                                    ------- ----------------
Certificate                                                               False {}
CitrixAGBasic                                                             False {[requestFilter, CitrixAGBasicReques...
CitrixFederation                                                           True {}
ExplicitForms                                                              True {}
HttpBasic                                                                 False {}
IntegratedWindows                                                         False {}
```
