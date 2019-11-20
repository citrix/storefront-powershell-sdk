#Remove-STFDesktopApplianceService
Remove a Desktop Appliance service
##Syntax
```Remove-STFDesktopApplianceService [-DesktopApplianceService] <DesktopApplianceService> [<CommonParameters>]
```
##Detailed Description
Removes the Desktop Appliance service supplied to the cmdlet.
##Related Commands
*[Set-STFDesktopApplianceService](Set-STFDesktopApplianceService)
*[Add-STFDesktopApplianceService](Add-STFDesktopApplianceService)
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||DesktopApplianceService|Desktop Appliance to remove|true|true (ByValue)|##Input Type
###Citrix.StoreFront.Model.DesktopAppliance.DesktopApplianceService
Parameter DesktopApplianceService: A .NET class representing the configuration of a StoreFront Desktop Appliance service
##Return Values
##Examples
###EXAMPLE 1 Remove a Desktop Appliance service
```$appliance = Get-STFDesktopApplianceService
Remove-STFDesktopApplianceService -DesktopApplianceService $appliance
```
REMARKS

Removes the only configured Desktop Appliance service.
