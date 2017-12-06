#Set-STFStorePnaSmartAccess
Set the SmartAccess settings
##Syntax
```Set-STFStorePnaSmartAccess [-StoreService] <StoreService> [-HeaderValidity] <Int32> [<CommonParameters>]
```
##Detailed Description
Configure the settings related to the verification of PNA SmartAccess HTTP headers.
##Related Commands
*[Grant-STFStorePnaSmartAccess](Grant-STFStorePnaSmartAccess)
*[Revoke-STFStorePnaSmartAccess](Revoke-STFStorePnaSmartAccess)
*[Get-STFStorePnaSmartAccess](Get-STFStorePnaSmartAccess)
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||StoreService|The Store to set the SmartAccess conditions for.|true|true (ByValue)||HeaderValidity|The PNA SmartAccess HTTP header validity period in seconds. PNA SmartAccess requests will be invalidated if the current server UTC date time plus the HeaderValidity is older than the time stamp in the request.|true|true (ByValue)|##Input Type
###Citrix.StoreFront.Model.Store.StoreService
Parameter StoreService: A .NET class representing the configuration of a StoreFront Store service
###System.Int32
Parameter HeaderValidity: The .NET 'System.Int32' value type
##Return Values
##Examples
###EXAMPLE 1 Set SmartAccess trust settings
```$store = Get-STFStoreService
Set-STFStorePnaSmartAccess -StoreService $store -HeaderValidity 60
```
REMARKS

Sets the http headers to be trusted for up to 60 seconds after the current server date time.
