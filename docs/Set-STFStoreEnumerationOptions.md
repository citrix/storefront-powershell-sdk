# Set-STFStoreEnumerationOptions

Set Store enumeration options

## Syntax

```
Set-STFStoreEnumerationOptions [-StoreService] <StoreService> [[-EnhancedEnumeration] <Boolean>] [[-MaximumConcurrentEnumerations] <Int32>] [[-FilterByTypesInclude] <String[]>] [[-FilterByKeywordsInclude] <String[]>] [[-FilterByKeywordsExclude] <String[]>] [[-RequestFullIconData] <None | Full | FullAndMulti>] [[-PassThru] <SwitchParameter>] [<CommonParameters>]
```

## Detailed Description

Set the Store options used when enumerating the XenApp and XenDesktop xml services.

## Related Commands

* [Get-STFStoreEnumerationOptions](Get-STFStoreEnumerationOptions.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|StoreService|Store service|true|true (ByValue)| |
|EnhancedEnumeration|Enable enhanced enumeration. Enumerate multiple farms in parallel to reduce operation time|false|false| |
|MaximumConcurrentEnumerations|Maximum farms enumerated in parallel|false|false| |
|FilterByTypesInclude|Inclusive resource filter by type (Applications, Desktops or Documents)|false|false| |
|FilterByKeywordsInclude|Only include applications and desktops that match the keywords|false|false| |
|FilterByKeywordsExclude|Exclude applications and desktops that match the keywords|false|false| |
|RequestFullIconData|Request icon data (None, Full, FullAndMulti)|false|false| |
|PassThru|The resulting Store Enumeration options|false|false| |

## Input Type

### Citrix.StoreFront.Model.Store.StoreService

Parameter StoreService: A .NET class representing the configuration of a StoreFront Store service

### System.Boolean

Parameter EnhancedEnumeration: The .NET `System.Boolean` value type

### System.Int32

Parameter MaximumConcurrentEnumerations: The .NET `System.Int32` value type

### System.String[]

Parameter FilterByTypesInclude: The .NET `System.String` reference type

### System.String[]

Parameter FilterByKeywordsInclude: The .NET `System.String` reference type

### System.String[]

Parameter FilterByKeywordsExclude: The .NET `System.String` reference type

### Citrix.StoreFront.Model.Store.RequestFullIconData

Parameter RequestFullIconData: The .NET `Citrix.StoreFront.Model.Store.RequestFullIconData` value type

### System.Management.Automation.SwitchParameter

Parameter PassThru: The .NET `System.Management.Automation.SwitchParameter` value type

## Return Values

### None

## Examples

### EXAMPLE 1 Turn off enhanced enumeration options

```
$storeService = Get-STFStoreService
Set-STFStoreEnumerationOptions $storeService -EnhancedEnumeration $false
```

**REMARKS**

Turn off parallel enumeration of Store farms.

### EXAMPLE 2 Filter by type

```
$storeService = Get-STFStoreService
Set-STFStoreEnumerationOptions $storeService -FilterByTypesInclude Applications
```

**REMARKS**

Filter resources to only show applications.

### EXAMPLE 3 Filter by keyword (include)

```
$storeService = Get-STFStoreService
Set-STFStoreEnumerationOptions $storeService -FilterByKeywordsInclude @("AppSet1","AppSet2")
```

**REMARKS**

Only publish resources in the Store that have the keywords AppSet1 or Appset2.

### EXAMPLE 4 Filter by keyword (exclude)

```
$storeService = Get-STFStoreService
Set-STFStoreEnumerationOptions $storeService -FilterByKeywordsExclude @("AppSet1","AppSet2")
```

**REMARKS**

Exclude resources from the store that have the keywords AppSet1 or Appset2

### EXAMPLE 5 Filter by keyword (include and exclude)

```
$storeService = Get-STFStoreService
Set-STFStoreEnumerationOptions $storeService -FilterByKeywordsInclude @("AppSet1","AppSet2") -FilterByKeywordsExclude @("AppSet3","AppSet4")
```

**REMARKS**

Includes resources from the store that have the keywords AppSet1 or Appset2 

and do not contain the keywords App3 or App4.  It is not possible to use the 

same keyword for both Exclude and Include filtering.

### EXAMPLE 6 Filter by keyword (clear)

```
$storeService = Get-STFStoreService
Set-STFStoreEnumerationOptions $storeService -FilterByKeywordsInclude "" -FilterByKeywordsExclude ""
```

**REMARKS**

Remove configured exclude or include keywords you have already set.
