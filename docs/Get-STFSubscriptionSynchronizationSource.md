#Get-STFSubscriptionSynchronizationSource
Get subscription synchronization sources
##Syntax
```Get-STFSubscriptionSynchronizationSource [<CommonParameters>]
```
##Detailed Description
Get all the remote StoreFront clusters configured to synchronization subscriptions from.
##Related Commands
*[Add-STFSubscriptionSynchronizationSource](Add-STFSubscriptionSynchronizationSource)
*[Clear-STFSubscriptionSynchronizationSource](Clear-STFSubscriptionSynchronizationSource)
##Input Type
##Return Values
###RemoteCluster
The .NET 'Citrix.StoreFront.Model.WindowsServices.SubscriptionStore.RemoteCluster' reference type
##Notes
Restarts the Citrix Subscription Store Service to read new settings.
##Examples
###EXAMPLE 1 Get synchronization sources
```Get-STFSubscriptionSynchronizationSource
```
REMARKS

Get the StoreFront clusters that subscriptions will be synchronized from.
OUTPUT
```Name               : APACRegion
Address            : apac.example.com
Enabled            : True
AuthenticationMode : Windows
RemoteStores       : {Store}
OpenTimeOut        : 00:01:00
CloseTimeOut       : 00:01:00
SendTimeOut        : 00:10:00
```
