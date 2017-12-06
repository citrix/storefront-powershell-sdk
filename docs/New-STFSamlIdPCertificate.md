#New-STFSamlIdPCertificate
Create a new signing certificate to be used by a SAML Identity Provider
##Syntax
```New-STFSamlIdPCertificate [-SubjectName] <String> [-FilePath] <String> [[-Password] <String>] [<CommonParameters>]
```
##Detailed Description
Create a new signing certificate that is suitable to be used by a SAML Identity Provider.
##Related Commands
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||SubjectName|The certificate subject name.|true|true (ByValue)||FilePath|The file path of the exported certificate.|true|true (ByValue)||Password|The optional password to use to protect the private key.|false|true (ByValue)|##Input Type
###System.String
Parameter SubjectName: The .NET 'System.String' reference type
###System.String
Parameter FilePath: The .NET 'System.String' reference type
###System.String
Parameter Password: The .NET 'System.String' reference type
##Return Values
###X509Certificate2
The .NET 'System.Security.Cryptography.X509Certificates.X509Certificate2' reference type
##Examples
###EXAMPLE 1 Create a new signing certificate to be used by a SAML Identity Provider.
```$exported = New-STFSamlIdPCertificate -SubjectName 'Identity Provider Signing' -Path 'c:\temp\exported.pfx' -Password 'citrix'
```
REMARKS

Create a new signing certificate, with subject name 'Identity Provider Signing', to be used by a SAML Identity
Provider in the specified authentication service, exported to the specified path with the specified password
protecting the private key.
