#Export-STFSamlEncryptionCertificate
Export the encryption certificate to be used by SAML Identity Providers
##Syntax
```Export-STFSamlEncryptionCertificate [-AuthenticationService] <AuthenticationService> [[-FilePath] <String>] [<CommonParameters>]
```
##Detailed Description
Export, from the specified authentication service, the encryption certificate to be used by SAML Identity Providers
##Related Commands
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||AuthenticationService|The Authentication service from which to export the certificate.|true|true (ByValue)||FilePath|The path of the file to export to.|false|true (ByValue)|##Input Type
###Citrix.StoreFront.Model.Authentication.AuthenticationService
Parameter AuthenticationService: A .NET class representing the configuration of a StoreFront Authentication service
###System.String
Parameter FilePath: The .NET 'System.String' reference type
##Return Values
##Examples
###EXAMPLE 1 Export the encryption certificate to be used by the SAML IdentityProvider.
```$authentication = Get-STFAuthenticationService
Export-STFSamlEncryptionCertificate -AuthenticationService $authentication -FilePath C:\windows\temp\EncryptionCertificate.cer
```
REMARKS

Export the encryption certificate to be used by the SAML Identity Provider.
