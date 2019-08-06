# Get-STFStoreSubscriptionsDatabase

Gets the location of the subscription data storage for the specified Store

## Syntax

```
Get-STFStoreSubscriptionsDatabase [-StoreService] <StoreService> [<CommonParameters>]
```

## Detailed Description

Gets the connection string for the SQL Server database currently used for subscription data for the specified Store.

## Related Commands

* [Set-STFStoreSubscriptionsDatabase](Set-STFStoreSubscriptionsDatabase.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|StoreService|The Store service to get the configured subscriptions storage for|true|true (ByValue)| |

## Input Type

### Citrix.StoreFront.Model.Store.StoreService

Parameter StoreService: A .NET class representing the configuration of a StoreFront Store service

## Return Values

### StoreSubscriptionDatabaseSummary

The .NET `Citrix.StoreFront.Model.Store.Summary.StoreSubscriptionDatabaseSummary` reference type

## Examples

### EXAMPLE 1 Get the subscription database connection

```
$store = Get-STFStoreService
Get-STFStoreStoreSubscriptionsDatabase -StoreService $store
```

**REMARKS**

Gets the subscription database connection for the only configured Store 

service.

**OUTPUT**

```
UseLocalStorage DatabaseConnectionString
--------------- ------------------------
False           Server=myServerAddress;Database=myDataBase;User 
Id=myUsername;Password=myPassword;
```
