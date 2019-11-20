#Get-STFRoamingGateway
Get a Gateway from the global list
##Syntax
```Get-STFRoamingGateway [[-Name] <String>] [[-RoamingService] <RoamingService>] [<CommonParameters>]
```
##Detailed Description
Get a Gateway from the global list to add to a Store to support remote access and authentication or to edit.
##Related Commands
*[Add-STFRoamingGateway](Add-STFRoamingGateway)
*[Remove-STFRoamingGateway](Remove-STFRoamingGateway)
*[Set-STFRoamingGateway](Set-STFRoamingGateway)
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||Name|Gateway friendly name|false|true (ByValue)||RoamingService|The Roaming service|false|false|##Input Type
###System.String
Parameter Name: The .NET 'System.String' reference type
###Citrix.StoreFront.Model.Roaming.RoamingService
Parameter RoamingService: A .NET class representing the configuration of a StoreFront Roaming service
##Return Values
###RoamingGateway
The .NET 'Citrix.StoreFront.Model.Roaming.RoamingGateway' reference type
##Examples
###EXAMPLE 1 Get Gateway
```Get-STFRoamingGateway -Name "Netscaler10x"
```
REMARKS

Get the Gateway with friendly name "Netscaler10x"
