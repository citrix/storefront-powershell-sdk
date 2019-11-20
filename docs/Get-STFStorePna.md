#Get-STFStorePna
Get the PNA state of the Store
##Syntax
```Get-STFStorePna [-StoreService] <StoreService> [<CommonParameters>]
```
##Detailed Description
Get the PNA (Program Neighborhood Agent) state of the Store. Returns a summary indicating if PNA is enabled and if it is the default PNA site for the StoreFront deployment.
##Related Commands
*[Enable-STFStorePna](Enable-STFStorePna)
*[Disable-STFStorePna](Disable-STFStorePna)
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||StoreService|The Store to get the PNA state of|true|true (ByValue)|##Input Type
###Citrix.StoreFront.Model.Store.StoreService
Parameter StoreService: A .NET class representing the configuration of a StoreFront Store service
##Return Values
###StorePnaSummary
The .NET 'Citrix.StoreFront.Model.Store.Summary.StorePnaSummary' reference type
##Examples
###EXAMPLE 1 Get PNA state
```$store = Get-STFStoreService
Get-STFStorePna -StoreService $store
```
REMARKS

Gets the PNA state of the only configured Store service.
OUTPUT
```StoreService                                                         PnaEnabled                       DefaultPnaService
------------                                                         ----------                       -----------------
Store: /Citrix/Store                                                       True                                    True
```
