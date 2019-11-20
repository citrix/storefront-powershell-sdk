# Enable-STFStoreDelegation

Enable a Store to performing delegated authentication.

## Syntax

```
Enable-STFStoreDelegation [-StoreService] <StoreService> [<CommonParameters>]
```

## Detailed Description

Enable a Store to performing delegated authentication.

## Related Commands

* [Disable-STFStoreDelegation](./Disable-STFStoreDelegation)

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

### EXAMPLE 1 Enable delegated authentication for the specified store.

```
$storeService = Get-STFStoreService
Enable-STFStoreDelegation $storeService
```

**REMARKS**

Enable delegated authentication for the specified store.
