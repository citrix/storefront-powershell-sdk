#Update-STFSamlIdPFromMetadata
Update the SAML Identity Provider configuration from metadata.
##Syntax
```Update-STFSamlIdPFromMetadata [-AuthenticationService] <AuthenticationService> [[-Url] <String>] [[-FilePath] <String>] [<CommonParameters>]
```
##Detailed Description
Update the SAML Identity Provider configuration from metadata, for the specified authentication service
##Related Commands
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||AuthenticationService|The Authentication Service to import the certificate into.|true|true (ByValue)||Url|The Url of the web hosted metadata.|false|true (ByValue)||FilePath|The path of the metadata file.|false|true (ByValue)|##Input Type
###Citrix.StoreFront.Model.Authentication.AuthenticationService
Parameter AuthenticationService: A .NET class representing the configuration of a StoreFront Authentication service
###System.String
Parameter Url: The .NET 'System.String' reference type
###System.String
Parameter FilePath: The .NET 'System.String' reference type
##Return Values
##Examples
###EXAMPLE 1 Update the SAML IdentityProvider configuration from a metadata url
```$authentication = Get-STFAuthenticationService
Update-STFSamlIdPFromMetadata -AuthenticationService $authentication -Url 'https://adfs.host.com/FederationMetadata/2007-06/FederationMetadata.xml'
```
REMARKS

Get the Identity Provider configuration from the specified ADFS metadata Url
