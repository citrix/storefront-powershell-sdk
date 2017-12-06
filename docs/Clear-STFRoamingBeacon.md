#Clear-STFRoamingBeacon
Clear internal or external roaming beacons
##Syntax
```Clear-STFRoamingBeacon [-Internal] <SwitchParameter> [-Internal] <SwitchParameter> [<CommonParameters>]
Clear-STFRoamingBeacon [-Internal <SwitchParameter>] [-External] <SwitchParameter> [-Internal] <SwitchParameter> [<CommonParameters>]
Clear-STFRoamingBeacon [-External] <SwitchParameter> [-Internal] <SwitchParameter> [<CommonParameters>]
```
##Detailed Description
Clear the custom internal or external beacons configured for roaming.
##Related Commands
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||Internal|Clear internal beacons|true|false||External|Clear external beacons|true|false||RoamingService|The Roaming service|false|false|##Input Type
###System.Management.Automation.SwitchParameter
Parameter Internal: The .NET 'System.Management.Automation.SwitchParameter' value type
###System.Management.Automation.SwitchParameter
Parameter External: The .NET 'System.Management.Automation.SwitchParameter' value type
###Citrix.StoreFront.Model.Roaming.RoamingService
Parameter RoamingService: A .NET class representing the configuration of a StoreFront Roaming service
##Return Values
##Examples
###EXAMPLE 1 Clear internal beacon
```Clear-STFRoamingBeacon -Internal
```
REMARKS

Clear the internal custom roaming beacon.
###EXAMPLE 2 Clear external beacons
```Clear-STFRoamingBeacon -External
```
REMARKS

Clear all external custom beacons resetting them to the default.
