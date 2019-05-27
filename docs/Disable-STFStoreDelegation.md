# Disable-STFStoreDelegation

Disable a Store from performing delegated authentication.

## Syntax

```
Disable-STFStoreDelegation [-StoreService] <StoreService> [<CommonParameters>]
```

## Detailed Description

Disable a Store from performing delegated authentication.

## Related Commands

* [Enable-STFStoreDelegation](Enable-STFStoreDelegation.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|StoreService|Store service|true|true (ByValue)| |

## Input Type

### Citrix.StoreFront.Model.Store.StoreService

Parameter StoreService: A .NET class representing the configuration of a StoreFront Store service

## Return Values

### None

## Examples

### EXAMPLE 1 Disable delegated authentication for the specified store.

```
$storeService = Get-STFStoreService
Disable-STFStoreDelegation $storeService
```

**REMARKS**

Disable delegated authentication for the specified store.
