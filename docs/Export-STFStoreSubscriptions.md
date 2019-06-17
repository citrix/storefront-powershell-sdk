# Export-STFStoreSubscriptions

Export subscriptions from a given Store

## Syntax

```
Export-STFStoreSubscriptions [-UpdatedSince <DateTime>] [-FilePath] <String> [-StoreService] <StoreService> [<CommonParameters>]



Export-STFStoreSubscriptions [-UpdatedSince <DateTime>] [-StoreService] <StoreService> [-FilePath] <String> [<CommonParameters>]
```

## Detailed Description

Export user subscriptions from a Store to a text file in csv format.

## Related Commands

* [Import-STFStoreSubscriptions](Import-STFStoreSubscriptions.md)
* [Restore-STFStoreSubscriptions](Restore-STFStoreSubscriptions.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|UpdatedSince|Export subscriptions older than the date time last updated|false|false| |
|StoreService|Store service to process subscriptions for|true|true (ByValue)| |
|FilePath|Path of csv file|true|false| |
|ChunkSize|Chunk size for splitting data. Only appropriate for very large datasets if connectivity issues are seen.|false|false| |

## Input Type

### System.DateTime

Parameter UpdatedSince: The .NET `System.DateTime` value type

### Citrix.StoreFront.Model.Store.StoreService

Parameter StoreService: A .NET class representing the configuration of a StoreFront Store service

### System.String

Parameter FilePath: The .NET `System.String` reference type

### System.Int32

Parameter ChunkSize: The .NET `System.Int32` value type

## Return Values

### None

## Examples

### EXAMPLE 1 Export from Store by friendly name

```
$StopWatch = [System.Diagnostics.Stopwatch]::StartNew()
Export-DSStoreSubscriptions -StoreName Store -FilePath "$env:userprofile\desktop\Export.txt"
$StopWatch.Stop()
Write-host "Total Elapsed Time: $($StopWatch.Elapsed.ToString())"
```

**REMARKS**

Exports the subscriptions from the Store named "Store" and outputs the total 

time taken.

**OUTPUT**

```
Total Elapsed Time: 00:00:05.3674858
```

### EXAMPLE 2 Export from Store by object

```
$store = Get-STFStoreService
Export-STFStoreSubscriptions -Store $store -FilePath "$env:userprofile\desktop\Export.txt"
```

**REMARKS**

Exports all subscriptions from the only configured Store.
