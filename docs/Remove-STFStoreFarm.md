# Remove-STFStoreFarm

Remove Farm from a Store

## Syntax

```
Remove-STFStoreFarm [-Farm] <Farm[]> [-StoreService] <StoreService> [<CommonParameters>]



Remove-STFStoreFarm [-FarmName] <String[]> [-StoreService] <StoreService> [<CommonParameters>]
```

## Detailed Description

Removes a XenDesktop\XenApp farm from a Store service.

## Related Commands

* [Add-STFStoreFarm](Add-STFStoreFarm.md)
* [Set-STFStoreFarm](Set-STFStoreFarm.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|Farm|Farm object to remove|true|false| |
|FarmName|Name of farm to remove from the Store service|true|false| |
|StoreService|Store service from which to remove the named farm|true|true (ByValue)| |

## Input Type

### Citrix.StoreFront.Model.Store.Farm[]

Parameter Farm: A .NET class representing the configuration of a Farm in StoreFront Store service

### System.String[]

Parameter FarmName: The .NET `System.String` reference type

### Citrix.StoreFront.Model.Store.StoreService

Parameter StoreService: A .NET class representing the configuration of a StoreFront Store service

## Return Values

### None

## Examples

### EXAMPLE 1 Remove Farm from Store by name

```
$storeService = Get-STFStoreService
Remove-STFStoreFarm -FarmName XenDesktop75 -StoreService $storeService
```

**REMARKS**

Remove the Farm XenDesktop75 with the specified name from the Store service.

### EXAMPLE 2 Remove a Farm from the Store service

```
$storeService = Get-STFStoreService
$farm = Get-STFStoreFarm -StoreService $storeService -FarmName XenDesktop75
Remove-STFStoreFarm $farm -StoreService $storeService
```

**REMARKS**

Remove the Farm XenDesktop75 from the Store service.
