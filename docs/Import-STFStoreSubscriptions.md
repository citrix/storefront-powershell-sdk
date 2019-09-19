# Import-STFStoreSubscriptions

Import subscriptions from a given Store

## Syntax

```
Import-STFStoreSubscriptions [-StoreService] <StoreService> [-FilePath] <String> [<CommonParameters>]



Import-STFStoreSubscriptions [-FilePath] <String> [-StoreService] <StoreService> [<CommonParameters>]
```

## Detailed Description

Import user subscriptions to a Store from a csv formatted text file.

## Related Commands

* [Export-STFStoreSubscriptions](Export-STFStoreSubscriptions.md)
* [Restore-STFStoreSubscriptions](Restore-STFStoreSubscriptions.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|StoreService|Store service to process subscriptions for|true|true (ByValue)| |
|FilePath|Path of csv file|true|false| |
|ChunkSize|Chunk size for splitting data. Only appropriate for very large datasets if connectivity issues are seen.|false|false| |

## Input Type

### Citrix.StoreFront.Model.Store.StoreService

Parameter StoreService: A .NET class representing the configuration of a StoreFront Store service

### System.String

Parameter FilePath: The .NET `System.String` reference type

### System.Int32

Parameter ChunkSize: The .NET `System.Int32` value type

## Return Values

### None

## Notes

The cmdlet appends the entries to the existing data.

## Examples

### EXAMPLE 1 Import subscriptions

```
$store = Get-STFStoreService
Import-STFStoreSubscriptions -Store $store -FilePath "$env:userprofile\desktop\Export.txt"
```

**REMARKS**

Import subscriptions into the only configured Store.
