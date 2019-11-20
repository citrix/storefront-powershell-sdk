#Get-STFRoamingServiceRecord
Get the Service Record
##Syntax
```Get-STFRoamingServiceRecord [-StoreService] <StoreService> [[-RoamingService] <RoamingService>] [<CommonParameters>]
```
##Detailed Description
Get the Service record for a specific or all Stores.
##Related Commands
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||StoreService|Store service to get the account record for|true|true (ByValue)||RoamingService|The Roaming service|false|false|##Input Type
###Citrix.StoreFront.Model.Store.StoreService
Parameter StoreService: A .NET class representing the configuration of a StoreFront Store service
###Citrix.StoreFront.Model.Roaming.RoamingService
Parameter RoamingService: A .NET class representing the configuration of a StoreFront Roaming service
##Return Values
###ServiceRecords
The .NET 'Citrix.StoreFront.Model.Roaming.ServiceRecords' reference type
##Examples
###EXAMPLE 1 Get Service record for a specific Store
```$store = Get-STFStoreService
Get-STFRoamingServiceRecord -StoreService $store
```
REMARKS

Get the service record used for accessing the specified Store service
