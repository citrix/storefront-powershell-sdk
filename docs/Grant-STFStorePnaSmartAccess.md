# Grant-STFStorePnaSmartAccess

Grant a server PNA SmartAccess

## Syntax

```
Grant-STFStorePnaSmartAccess [-CertificatePath] <String> [-StoreService] <StoreService> [-ServerName] <String> [<CommonParameters>]



Grant-STFStorePnaSmartAccess [-Certificate] <X509Certificate2> [-StoreService] <StoreService> [-ServerName] <String> [<CommonParameters>]
```

## Detailed Description

Configures a certificate to be used for the purpose of verifying signed data supplied in PNA SmartAccess headers.

## Related Commands

* [Revoke-STFStorePnaSmartAccess](Revoke-STFStorePnaSmartAccess.md)
* [Get-STFStorePnaSmartAccess](Get-STFStorePnaSmartAccess.md)
* [Set-STFStorePnaSmartAccess](Set-STFStorePnaSmartAccess.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|StoreService|Trust the certificate supplied for SmartAccess conditions in this Store.|true|true (ByValue)| |
|ServerName|The name of the server requiring trust of the certificate.|true|false| |
|CertificatePath|The path of certificate to import and trust.|true|false| |
|Certificate|The certificate to import and trust.|true|false| |

## Input Type

### Citrix.StoreFront.Model.Store.StoreService

Parameter StoreService: A .NET class representing the configuration of a StoreFront Store service

### System.String

Parameter ServerName: The .NET `System.String` reference type

### System.String

Parameter CertificatePath: The .NET `System.String` reference type

### System.Security.Cryptography.X509Certificates.X509Certificate2

Parameter Certificate: The .NET `System.Security.Cryptography.X509Certificates.X509Certificate2` reference type

## Return Values

### None

## Notes

Verifying the signed data of a PNA SmartAccess header ensures it was provided by a trusted source.

## Examples

### EXAMPLE 1 Grant SmartAccess

```
$store = Get-STFStoreService -VirtualPath /Citrix/Store
Grant-STFStorePnaSmartAccess -StoreService $store -ServerName "XenMobile" -CertificatePath C:\Certs\cert.cer
```

**REMARKS**

Configures the certificate so it can be used for verfying signed headers.
