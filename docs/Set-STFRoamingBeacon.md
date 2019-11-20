#Set-STFRoamingBeacon
Set the internal and external beacons
##Syntax
```Set-STFRoamingBeacon [-Internal] <Uri> [-Internal] <Uri> [<CommonParameters>]
Set-STFRoamingBeacon [-Internal <Uri>] [-External <Uri[]>] [-Internal] <Uri> [<CommonParameters>]
Set-STFRoamingBeacon [-External] <Uri[]> [-Internal] <Uri> [<CommonParameters>]
Set-STFRoamingBeacon [-RefreshServiceRecordOnly] <SwitchParameter> [-Internal] <Uri> [<CommonParameters>]
```
##Detailed Description
Configure the internal and external roaming beacons.
##Related Commands
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||Internal|Internal beacon address.|true|true (ByValue)||External|External beacons address.|true|true (ByValue)||RefreshServiceRecordOnly|Refresh the Store service record with any out-of-band changes.|true|true (ByValue)||RoamingService|The Roaming service|false|false|##Input Type
###System.Uri
Parameter Internal: The .NET 'System.Uri' reference type
###System.Uri[]
Parameter External: The .NET 'System.Uri' reference type
###System.Management.Automation.SwitchParameter
Parameter RefreshServiceRecordOnly: The .NET 'System.Management.Automation.SwitchParameter' value type
###Citrix.StoreFront.Model.Roaming.RoamingService
Parameter RoamingService: A .NET class representing the configuration of a StoreFront Roaming service
##Return Values
##Examples
###EXAMPLE 1 Set the internal beacon
```Set-STFRoamingBeacon -Internal http://myinternalbeacon.com
```
REMARKS

Set the internal beacon to http://myinternalbeacon.com.
###EXAMPLE 2 Set the external beacons
```Set-STFRoamingBeacon -External http://external1.com,http://external2.com
```
REMARKS

Set the external beacons to http://external1.com and http://external2.com.
