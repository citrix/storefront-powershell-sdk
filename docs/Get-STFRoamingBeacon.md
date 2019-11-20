#Get-STFRoamingBeacon
Get roaming beacons
##Syntax
```Get-STFRoamingBeacon [-Internal] <SwitchParameter> [[-RoamingService] <RoamingService>] [<CommonParameters>]
Get-STFRoamingBeacon [-External] <SwitchParameter> [[-RoamingService] <RoamingService>] [<CommonParameters>]
```
##Detailed Description
Get the roaming beacons configured for the deployment.
##Related Commands
*[Set-STFRoamingBeacon](Set-STFRoamingBeacon)
*[Clear-STFRoamingBeacon](Clear-STFRoamingBeacon)
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||Internal|Show internal beacon|true|true (ByValue)||External|Show external beacons|true|true (ByValue)||RoamingService|The Roaming service|false|false|##Input Type
###System.Management.Automation.SwitchParameter
Parameter Internal: The .NET 'System.Management.Automation.SwitchParameter' value type
###System.Management.Automation.SwitchParameter
Parameter External: The .NET 'System.Management.Automation.SwitchParameter' value type
###Citrix.StoreFront.Model.Roaming.RoamingService
Parameter RoamingService: A .NET class representing the configuration of a StoreFront Roaming service
##Return Values
###String
The .NET 'System.String' reference type
##Examples
###EXAMPLE 1 Get internal beacon
```Get-STFRoamingBeacon -Internal
```
REMARKS

Gets the internal beacon
###EXAMPLE 2 Get external beacons
```Get-STFRoamingBeacon -External
```
REMARKS

Gets the external beacons
