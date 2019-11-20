# Add-STFSubscriptionSynchronizationSource

Add a Synchronization source

## Syntax

```
Add-STFSubscriptionSynchronizationSource [-StoreService] <StoreService[]> [-RemoteStoreFrontAddress] <String> [-FriendlyName] <String> [<CommonParameters>]



Add-STFSubscriptionSynchronizationSource [-StoreName] <String[]> [-RemoteStoreFrontAddress] <String> [-FriendlyName] <String> [<CommonParameters>]
```

## Detailed Description

Add a remote StoreFront synchronization source to pull self service application and desktop subscriptions from.

## Related Commands

* [Clear-STFSubscriptionSynchronizationSource](./Clear-STFSubscriptionSynchronizationSource)
* [Get-STFSubscriptionSynchronizationSource](./Get-STFSubscriptionSynchronizationSource)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|StoreService|Store service to synchronize subscriptions to. Requires a matching store on the remote StoreFront|true|true (ByValue)| |
|StoreName|Store service to synchronize subscriptions to. Requires a matching store on the remote StoreFront|true|false| |
|RemoteStoreFrontAddress|A remote hostbase url of a StoreFront server group, server hostname, IP address or server FQDN|true|false| |
|FriendlyName|Friendly name of the synchronization source|true|false| |

## Input Type

### Citrix.StoreFront.Model.Store.StoreService[]

Parameter StoreService: A .NET class representing the configuration of a StoreFront Store service

### System.String[]

Parameter StoreName: The .NET `System.String` reference type

### System.String

Parameter RemoteStoreFrontAddress: The .NET `System.String` reference type

### System.String

Parameter FriendlyName: The .NET `System.String` reference type

## Return Values

### None

## Notes

Restarts the Citrix Subscription Store Service to read new settings.


The name of the Store on the remote StoreFront must match that on the local StoreFront group for subscriptions to correctly update.


Permissions must be configured using the Grant-STFSubscriptionSynchronization cmdlet on the remote StoreFront.


Stores to be synchronized require identical XenApp \ XenDesktop Controller configurations and Store names on both the receiving and publishing StoreFront server

## Examples

### EXAMPLE 1 Synchronize subscriptions from a StoreFront group

```
$storeService = Get-STFStoreService
Add-STFSubscriptionSynchronizationSource -StoreService $storeService -RemoteStoreFrontAddress http://another.storefront.com -FriendlyName "EU located StoreFront"
```

**REMARKS**

Synchronize the subscriptions from server group another.storefront.com to the only configured store.

### EXAMPLE 2 Synchronize Store subscriptions by Store name

```
Add-STFSubscriptionSynchronizationSource -StoreName "MyStore" -RemoteStoreFrontAddress http://another.storefront.com -FriendlyName "EU located StoreFront"
```

**REMARKS**

Synchronize the subscriptions from server group another.storefront.com for the Store name "MyStore".
