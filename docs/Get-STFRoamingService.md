#Get-STFRoamingService
Get the Roaming Service
##Syntax
```Get-STFRoamingService [[-SiteId] <Int64>] [<CommonParameters>]
```
##Detailed Description
Get the Roaming Service. The Roaming Service is where the list of global gateways, account and service records and account redirect rules are configured.
##Related Commands
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||SiteId|The IIS Site to which the Roaming service should belong|false|false|##Input Type
###System.Int64
Parameter SiteId: The .NET 'System.Int64' value type
##Return Values
###RoamingService
A .NET class representing the configuration of a StoreFront Roaming service
##Examples
###EXAMPLE 1 Get the Roaming Service
```Get-STFRoamingService
```
REMARKS

Get the roaming service
OUTPUT
```Roaming           : Gateways:0, Data:2, Accounts:0, Records:0, Beacons:Internal:0, External:0
SiteId            : 1
VirtualPath       : /Citrix/Roaming
FriendlyName      : RoamingFeature
Name              : Roaming
Hmacs             : {}
Certificates      : {5B9386733F1227C4B1104E6AEB55DBEE9A16B304}
TokenManagers     : {Roaming Consumer}
Routing           : :
ServiceRef        : 1__Citrix_Roaming
PhysicalPath      : C:\inetpub\wwwroot\Citrix\Roaming
ConfigurationFile : C:\inetpub\wwwroot\Citrix\Roaming\web.config
TenantId          : 860e9401-39c8-4f2c-928d-34251102b840
```
