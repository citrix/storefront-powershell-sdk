# Get-STFStoreFarmConfiguration

Get common Store farm options

## Syntax

```
Get-STFStoreFarmConfiguration [-StoreService] <StoreService> [<CommonParameters>]
```

## Detailed Description

Get the details of an existing farm.

## Related Commands

* [Set-STFStoreFarmConfiguration](Set-STFStoreFarmConfiguration.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|StoreService|The Store service the farm options are required from|true|true (ByValue)| |

## Input Type

### Citrix.StoreFront.Model.Store.StoreService

Parameter StoreService: A .NET class representing the configuration of a StoreFront Store service

## Return Values

### Farm

A .NET class representing the configuration of a Farm in StoreFront Store service

## Examples

### EXAMPLE 1 Get all the farm configuration settings for the Store

```
$storeService = Get-STFStoreService  -SiteId 1 -VirtualPath '/Citrix/Store'
Get -STFStoreFarmConfiguration -StoreService $storeService
```

**REMARKS**

Returns all of the farm configuration options for the Store.

### EXAMPLE 2 Get the certificate revocation policy for the Store

```
$storeService = Get-STFStoreService  -SiteId 1 -VirtualPath '/Citrix/Store'
(Get-STFStoreFarmConfiguration -StoreService $storeService).CertRevocationPolicy
```

**REMARKS**

Returns just the certificate revocation policy for the Store.
