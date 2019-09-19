# Set-STFDesktopApplianceService

Configure a Desktop Appliance site

## Syntax

```
Set-STFDesktopApplianceService [-DesktopApplianceService] <DesktopApplianceService> [[-MultiDesktop] <SwitchParameter>] [[-EnableExplicit] <SwitchParameter>] [[-EnableSmartCard] <SwitchParameter>] [[-EnableEmbeddedSmartcardSSO] <SwitchParameter>] [<CommonParameters>]
```

## Detailed Description

Configure options on the supplied Desktop Appliance site.

## Related Commands

* [Add-STFDesktopApplianceService](Add-STFDesktopApplianceService.md)
* [Remove-STFDesktopApplianceService](Remove-STFDesktopApplianceService.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|DesktopApplianceService|Desktop Appliance service to configure|true|true (ByValue)| |
|MultiDesktop|Enable multi-desktops|false|false| |
|EnableExplicit|Enable explicit authentication|false|false| |
|EnableSmartCard|Enable smart card authentication|false|false| |
|EnableEmbeddedSmartcardSSO|Enable pass-through with smart card authentication|false|false| |

## Input Type

### Citrix.StoreFront.Model.DesktopAppliance.DesktopApplianceService

Parameter DesktopApplianceService: A .NET class representing the configuration of a StoreFront Desktop Appliance service

### System.Management.Automation.SwitchParameter

Parameter MultiDesktop: The .NET `System.Management.Automation.SwitchParameter` value type

### System.Management.Automation.SwitchParameter

Parameter EnableExplicit: The .NET `System.Management.Automation.SwitchParameter` value type

### System.Management.Automation.SwitchParameter

Parameter EnableSmartCard: The .NET `System.Management.Automation.SwitchParameter` value type

### System.Management.Automation.SwitchParameter

Parameter EnableEmbeddedSmartcardSSO: The .NET `System.Management.Automation.SwitchParameter` value type

## Return Values

### DesktopApplianceService

A .NET class representing the configuration of a StoreFront Desktop Appliance service

## Examples

### EXAMPLE 1 Configure Desktop Appliance site

```
$appliance = Get-STFDesktopApplianceService
Set-STFDesktopApplianceService -DesktopApplianceService $appliance -MultiDesktop:$false
```

**REMARKS**

Turn off multi-desktops on the only configured Desktop Appliance site.
