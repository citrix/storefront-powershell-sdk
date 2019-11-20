#Get-STFStoreRegisteredGateway
Get the gateways for Store used for authentication
##Syntax
```Get-STFStoreRegisteredGateway [-StoreService] <StoreService> [<CommonParameters>]
```
##Detailed Description
Get the gateways that have been registered to a Store for authentication.
##Related Commands
*[Register-STFStoreGateway](Register-STFStoreGateway)
*[Unregister-STFStoreGateway](Unregister-STFStoreGateway)
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||StoreService|The Store service from which to obtain the registered gateways.|true|true (ByValue)|##Input Type
###Citrix.StoreFront.Model.Store.StoreService
Parameter StoreService: A .NET class representing the configuration of a StoreFront Store service
##Return Values
###RegisteredGatewaySummary
The .NET 'Citrix.StoreFront.Model.Store.RegisteredGatewaySummary' reference type
##Examples
###EXAMPLE 1 Get gateways for a Store
```$storeService = Get-STFStoreService
Get-STFStoreRegisteredGateway -StoreService $storeService
```
REMARKS

Get gateways used for authentication for a Store.
OUTPUT
```EnabledOnDirectAccess     : False
Farms                     : {}
NeverLaunchThroughGateway : False
Id                        : 9ecdb90c-3bf8-4d77-9401-4a39584ae882
Name                      : Netscaler9
IPAddress                 : 255.255.240.0
SessionReliability        : True
RequestTicketTwoSTAs      : True
Hostnames                 : {https://eunetscaler.storefront.com/}
SecureTicketAuthorityUrls : {https://XA1/scripts/ctxsta.dll}
StasBypassDuration        : 01:00:00
StasUseLoadBalancing      : False
AuthenticationCapable     : True
HDXRoutingCapable         : True
```
