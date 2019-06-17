# Restore-STFStoreSubscriptions

Restore subscriptions to given Store

## Syntax

```
Restore-STFStoreSubscriptions [-StoreService] <StoreService> [-FilePath] <String> [<CommonParameters>]



Restore-STFStoreSubscriptions [-FilePath] <String> [-StoreService] <StoreService> [<CommonParameters>]
```

## Detailed Description

Restore user subscriptions to a Store from a text file in the correct csv format.

## Related Commands

* [Export-STFStoreSubscriptions](Export-STFStoreSubscriptions.md)
* [Import-STFStoreSubscriptions](Import-STFStoreSubscriptions.md)

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

The cmdlet replaces the all of the existing data with what is contained in the file.

## Examples

### EXAMPLE 1 Restore subscriptions

```
$store = Get-STFStoreService
Restore-STFStoreSubscriptions -Store $store -FilePath "$env:userprofile\desktop\Export.txt"
```

**REMARKS**

Restore subscriptions into the only configured Store.
