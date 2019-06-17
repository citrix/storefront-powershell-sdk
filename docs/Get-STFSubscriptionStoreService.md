# Get-STFSubscriptionStoreService

Get the Subscription Store Service

## Syntax

```
Get-STFSubscriptionStoreService [<CommonParameters>]
```

## Detailed Description

Get the Subscription Store Service. The Subscription Store Service is the data store for self-service application and desktop subscriptions.

## Related Commands


## Input Type

### 



## Return Values

### SubscriptionStoreService

A .NET class representing the configuration of a StoreFront Subscriptions Store service

## Examples

### EXAMPLE 1 Get Subscription Store Service

```
Get-STFSubscriptionStoreService
```

**REMARKS**

Get the Subscription Store service.

**OUTPUT**

```
HostedServices              : {subscriptionsManagementService: Enabled, 
LocalDataStore: Enabled, RemoteDataStore: Enabled,
SubscriptionsSynchronisation: Enabled...}
SubscriptionDataStores      : {Name:1__Citrix_Store,Location:%APPDATA%\Citrix\S
ubscriptionsStore\1__Citrix_Store,EP:net.p2p://citrix-subscriptions-1__citrix_s
tore/}
SubscriptionSynchronisation : Citrix.StoreFront.Model.WindowsServices.Subscript
ionStore.SubscriptionSynchronization
ConfigurationFile           : C:\Program Files\Citrix\Receiver StoreFront\Servi
ces\SubscriptionsStoreService\Citrix.DeliveryServices.SubscriptionsStore.Servic
eHost.exe.config
TenantId                    : 860e9401-39c8-4f2c-928d-34251102b840
```
