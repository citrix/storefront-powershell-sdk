#Revoke-STFStorePnaSmartAccess
Revoke a server PNA SmartAccess
##Syntax
```Revoke-STFStorePnaSmartAccess [-ServerName] <String> [-StoreService] <StoreService> [<CommonParameters>]
Revoke-STFStorePnaSmartAccess [-CertificateThumbprint] <String> [-StoreService] <StoreService> [<CommonParameters>]
Revoke-STFStorePnaSmartAccess [-AccessConditionsTrust] <AccessConditionsTrust> [-StoreService] <StoreService> [<CommonParameters>]
Revoke-STFStorePnaSmartAccess [-All] <SwitchParameter> [-StoreService] <StoreService> [<CommonParameters>]
```
##Detailed Description
Removes the certificate to be used for the purpose of verifying signed data supplied in PNA SmartAccess headers. The server and certificate will no longer be able to use SmartAccess.
##Related Commands
*[Grant-STFStorePnaSmartAccess](Grant-STFStorePnaSmartAccess)
*[Get-STFStorePnaSmartAccess](Get-STFStorePnaSmartAccess)
*[Set-STFStorePnaSmartAccess](Set-STFStorePnaSmartAccess)
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||StoreService|Revoke the certificate used for SmartAccess condition header verification in this Store.|true|true (ByValue)||ServerName|The name of the server with a certificate requiring revocation.|true|false||CertificateThumbprint|The thumbprint of the certificate requiring revocation.|true|false||AccessConditionsTrust|The AccessConditionTrust object requiring revocation.|true|false||All|Remove all server certificates used .|true|false|##Input Type
###Citrix.StoreFront.Model.Store.StoreService
Parameter StoreService: A .NET class representing the configuration of a StoreFront Store service
###System.String
Parameter ServerName: The .NET 'System.String' reference type
###System.String
Parameter CertificateThumbprint: The .NET 'System.String' reference type
###Citrix.StoreFront.Model.Store.AccessConditionsTrust
Parameter AccessConditionsTrust: The .NET 'Citrix.StoreFront.Model.Store.AccessConditionsTrust' reference type
###System.Management.Automation.SwitchParameter
Parameter All: The .NET 'System.Management.Automation.SwitchParameter' value type
##Return Values
##Notes
Verifying the signed data of a PNA SmartAccess header ensures it was provided by a trusted source.
##Examples
###EXAMPLE 1 Revoke SmartAccess by server name
```$store = Get-STFStoreService -VirtualPath /Citrix/Store
Revoke-STFStorePnaSmartAccess -StoreService $store -ServerName "XenMobile"
```
REMARKS

Revoke the server trust so it can no longer use SmartAccess.
###EXAMPLE 2 Revoke SmartAccess by thumbprint
```$store = Get-STFStoreService -VirtualPath /Citrix/Store
Revoke-STFStorePnaSmartAccess -StoreService $store -CertificateThumbprint "DFD2952373DAF788B494A3BB4AD45108760D5156"
```
REMARKS

Revoke the server trust using the specified certificate so it can no longer use SmartAccess.
