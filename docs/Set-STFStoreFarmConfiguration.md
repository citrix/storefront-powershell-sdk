# Set-STFStoreFarmConfiguration

Configure common Store farm options

## Syntax

```
Set-STFStoreFarmConfiguration [-StoreService] <StoreService> [[-EnableFileTypeAssociation] <Boolean>] [[-CommunicationTimeout] <TimeSpan>] [[-ConnectionTimeout] <TimeSpan>] [[-LeasingStatusExpiryFailed] <TimeSpan>] [[-LeasingStatusExpiryLeasing] <TimeSpan>] [[-LeasingStatusExpiryPending] <TimeSpan>] [[-PooledSockets] <Boolean>] [[-ServerCommunicationAttempts] <Int32>] [[-BackgroundHealthCheckPollingPeriod] <TimeSpan>] [[-AdvancedHealthCheck] <Boolean>] [[-CertRevocationPolicy] <String>] [<CommonParameters>]
```

## Detailed Description

Configure Store wide settings common to all configured farms.

## Related Commands

* [Set-STFStoreLaunchOptions](Set-STFStoreLaunchOptions.md)
* [Get-STFStoreLaunchOptions](Get-STFStoreLaunchOptions.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|StoreService|Store service to configure global farm options for|true|true (ByValue)| |
|EnableFileTypeAssociation|Enable file type association|false|false| |
|CommunicationTimeout|Communication timeout when using to the Xml service in seconds or timespan format|false|false| |
|ConnectionTimeout|Connection timeout when connecting to the Xml service in seconds or timespan format|false|false| |
|LeasingStatusExpiryFailed|Period of time before retrying a XenDesktop 7 and greater farm in failed leasing mode in seconds or timespan format|false|false| |
|LeasingStatusExpiryLeasing|Period of time before retrying a XenDesktop 7 and greater farm in leasing mode in seconds or timespan format|false|false| |
|LeasingStatusExpiryPending|Period of time before retrying a XenDesktop 7 and greater farm pending leasing mode in seconds or timespan format|false|false| |
|PooledSockets|Use pooled sockets|false|false| |
|ServerCommunicationAttempts|Number of server connection attempts before failing|false|false| |
|BackgroundHealthCheckPollingPeriod|Period of time between polling XenApp\XenDesktop server health in seconds or timespan format|false|false| |
|AdvancedHealthCheck|Indicates whether an advanced health-check should be performed. The advanced health-check should spot more potential server health issues but may not be compatible with servers older than XenApp 6.5.|false|false| |
|CertRevocationPolicy|Certificate Revocation Policy to use when connecting to XML services using HTTPS.  This setting has no effect on HTTP XML services.  Valid values are 'NoCheck' (Default), 'MustCheck', 'FullCheck' or 'NoNetworkAccess'|false|false| |

## Input Type

### Citrix.StoreFront.Model.Store.StoreService

Parameter StoreService: A .NET class representing the configuration of a StoreFront Store service

### System.Boolean

Parameter EnableFileTypeAssociation: The .NET `System.Boolean` value type

### System.TimeSpan

Parameter CommunicationTimeout: The .NET `System.TimeSpan` value type

### System.TimeSpan

Parameter ConnectionTimeout: The .NET `System.TimeSpan` value type

### System.TimeSpan

Parameter LeasingStatusExpiryFailed: The .NET `System.TimeSpan` value type

### System.TimeSpan

Parameter LeasingStatusExpiryLeasing: The .NET `System.TimeSpan` value type

### System.TimeSpan

Parameter LeasingStatusExpiryPending: The .NET `System.TimeSpan` value type

### System.Boolean

Parameter PooledSockets: The .NET `System.Boolean` value type

### System.Int32

Parameter ServerCommunicationAttempts: The .NET `System.Int32` value type

### System.TimeSpan

Parameter BackgroundHealthCheckPollingPeriod: The .NET `System.TimeSpan` value type

### System.Boolean

Parameter AdvancedHealthCheck: The .NET `System.Boolean` value type

### System.String

Parameter CertRevocationPolicy: The .NET `System.String` reference type

## Return Values

### None

## Examples

### EXAMPLE 1 Enable pooled sockets

```
$storeService = Get-STFStoreService –SiteID 1 –VirtualPath '/Citrix/Store'
Set -STFStoreFarmConfiguration $storeService -PooledSockets $true
```

**REMARKS**

Enable pooled sockets on the only configured store service

### EXAMPLE 2 Disable file type association

```
$storeService = Get-STFStoreService –SiteID 1 –VirtualPath '/Citrix/Store'
Set-STFStoreFarmConfiguration $storeService -EnableFileTypeAssociation $false
```

**REMARKS**

Disables FTA, file type association for the only configured Store service.

### EXAMPLE 3 Set communication timeout in seconds

```
$storeService = Get-STFStoreService –SiteID 1 –VirtualPath '/Citrix/Store'
Set-STFStoreFarmConfiguration $storeService -CommunicationTimeout 30
```

**REMARKS**

Sets the connection timeout to 30 seconds.

### EXAMPLE 4  4 Set communication timeout as timespan

```
$storeService = Get-STFStoreService –SiteID 1 –VirtualPath '/Citrix/Store'
Set-STFStoreFarmConfiguration $storeService -CommunicationTimeout 00:00:30
```

**REMARKS**

Sets the connection timeout to 30 seconds.

### EXAMPLE 5 Set certificate revocation policy for a store

```
$storeService = Get-STFStoreService –SiteID 1 –VirtualPath '/Citrix/Store'
Set-STFStoreFarmConfiguration $storeService -CertRevocationPolicy 'MustCheck'
```

**REMARKS**

Sets the certificate revocation policy to be MustCheck.
