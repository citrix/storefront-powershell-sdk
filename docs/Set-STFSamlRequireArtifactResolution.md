#Set-STFSamlRequireArtifactResolution
Configure whether the SAML Artifact Resolution protocol is required for Single Signle Sign-on
##Syntax
```Set-STFSamlRequireArtifactResolution [-AuthenticationService] <AuthenticationService> [-Required] <Boolean> [<CommonParameters>]
```
##Detailed Description
Configure whether the SAML Artifact Resolution protocol is required for Single Signle Sign-on, for the specified authentication service
##Related Commands
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||AuthenticationService|The Authentication Service to set the property for.|true|true (ByValue)||Required|Whether or not Artifact Resolution is required.|true|true (ByValue)|##Input Type
###Citrix.StoreFront.Model.Authentication.AuthenticationService
Parameter AuthenticationService: A .NET class representing the configuration of a StoreFront Authentication service
###System.Boolean
Parameter Required: The .NET 'System.Boolean' value type
##Return Values
##Examples
###EXAMPLE 1 Require Artifact Resolution
```$authentication = Get-STFAuthenticationService
Set-STFSamlRequire -AuthenticationService $authentication -Required $true
```
REMARKS

Configure the SAML Service Provider in the specified authentication service, to require the use of the Artifact
Resolution protocol.
