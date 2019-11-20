#Remove-STFUserFarmMapping
Remove a UserFarmMapping from the Store
##Syntax
```Remove-STFUserFarmMapping [-UserFarmMapping] <UserFarmMapping> [-StoreService] <StoreService> [<CommonParameters>]
Remove-STFUserFarmMapping [-Name] <String> [-StoreService] <StoreService> [<CommonParameters>]
```
##Detailed Description
Remove the UserFarmMapping configured for or Store.
##Related Commands
*[Set-STFUserFarmMapping](Set-STFUserFarmMapping)
*[Get-STFUserFarmMapping](Get-STFUserFarmMapping)
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||StoreService|The Store service output the UserFarmMappings from.|true|true (ByValue)||UserFarmMapping|The UserFarmMapping to remove from the StoreService UserFarmMappings.|true|false||Name|The unique name used to identify the UserFarmMapping.|true|false|##Input Type
###Citrix.StoreFront.Model.Store.StoreService
Parameter StoreService: A .NET class representing the configuration of a StoreFront Store service
###Citrix.StoreFront.Model.Store.UserFarmMapping
Parameter UserFarmMapping: The .NET 'Citrix.StoreFront.Model.Store.UserFarmMapping' reference type
###System.String
Parameter Name: The .NET 'System.String' reference type
##Return Values
##Examples
###EXAMPLE 1 Remove a UserFarmMapping
```$store = Get-STFStoreService -VirtualPath /Citrix/Store
Remove-STFUserFarmMapping -StoreService $store -Name "EUMapping"
```
REMARKS

Remove the EUMapping from the UserFarmMappings for the Store service /Citrix/Store.
