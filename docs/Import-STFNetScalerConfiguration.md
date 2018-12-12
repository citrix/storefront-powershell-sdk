# Import-STFNetScalerConfiguration

Import a NetScaler remote access configuration

## Syntax

```
Import-STFNetScalerConfiguration [-Configuration] <NetScalerConfigurationDocument> [[-PropagateChanges] <SwitchParameter>] [[-RoamingGatewaysToOverwrite] <RoamingGateway[]>] [[-CreateNew] <SwitchParameter>] [[-LogonType] <Domain | RSA | DomainAndRSA | SMS | SmartCard | SmartCardDomain | SmartCardRSA | SmartCardDomainAndRSA | SmartCardSMS>] [[-CallbackUrl] <String>] [[-GatewayIndex] <Int32>] [<CommonParameters>]
```

## Detailed Description

Import a NetScaler remote access configuration supplied by a NetScaler administrator.

## Related Commands

* [Read-STFNetScalerConfiguration](./Read-STFNetScalerConfiguration)
* [Wait-STFPublishServerGroupConfiguration](./Wait-STFPublishServerGroupConfiguration)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|Configuration|A NetScaler configuration to be imported into StoreFront.|true|true (ByValue)| |
|PropagateChanges|Propagate configuration changes to other members of the cluster.|false|false| |
|RoamingGatewaysToOverwrite|Specify gateways that should be overwritten if the import finds more than one matching gateway that will be overwritten by the import.|false|false| |
|CreateNew|Specify that a new gateway should be created rather than update an existing gateway.|false|false| |
|LogonType|Specify the logon type for a gateway overriding whatever is specified in the configuration document.|false|false| |
|CallbackUrl|Optional callback url to replace the suggested url if it cannot be resolved.|false|false| |
|GatewayIndex|Optional ability to specify which gateway from the configuration which will be imported.|false|false| |

## Input Type

### Citrix.StoreFront.Model.Roaming.NetScalerConfiguration.NetScalerConfigurationDocument

Parameter Configuration: The .NET `Citrix.StoreFront.Model.Roaming.NetScalerConfiguration.NetScalerConfigurationDocument` reference type

### System.Management.Automation.SwitchParameter

Parameter PropagateChanges: The .NET `System.Management.Automation.SwitchParameter` value type

### Citrix.StoreFront.Model.Roaming.RoamingGateway[]

Parameter RoamingGatewaysToOverwrite: The .NET `Citrix.StoreFront.Model.Roaming.RoamingGateway` reference type

### System.Management.Automation.SwitchParameter

Parameter CreateNew: The .NET `System.Management.Automation.SwitchParameter` value type

### Citrix.StoreFront.Model.Roaming.NetScalerConfiguration.ImportLogonType

Parameter LogonType: The .NET `Citrix.StoreFront.Model.Roaming.NetScalerConfiguration.ImportLogonType` value type

### System.String

Parameter CallbackUrl: The .NET `System.String` reference type

### System.Int32

Parameter GatewayIndex: The .NET `System.Int32` value type

## Return Values

### DocumentValidation

The .NET `Citrix.StoreFront.Model.Roaming.NetScalerConfiguration.DocumentValidation` reference type

## Notes

-WhatIf parameter can be used to verify the configuration consistency.

## Examples

### EXAMPLE 1 Import a NetScaler remote access configuration

```
$netscalerConfiguration = Read-STFNetScalerConfiguration –Path C:\NSG\Configuration.zip
$stasToUpdate = Test-STFSecureTicketAuthority -StaConfigurationObject $netscalerConfiguration
Import-STFNetScalerConfiguration -Configuration $netscalerConfiguration
```

REMAR

```
KS




The example reads in a NetScaler configuration package, validates that the Secure Ticket Authorities can be resolved and imports the configuration.

If validation errors are found they are output to the pipeline. If propagating to the cluster the progress can be monitored with Wait-STFPublishServerGroupConfiguration
```

### EXAMPLE 2 Import specific vServer from NetScaler remote access configuration file.

```
$ImportedGateways = Read-STFNetScalerConfiguration -path "$env: USERPROFILE\desktop\GatewayConfig.zip"
Import-STFNetScalerConfiguration -Configuration $ImportedGateways -GatewayIndex 0
Import-STFNetScalerConfiguration -Configuration $ImportedGateways -GatewayIndex 1
Import-STFNetScalerConfiguration -Configuration $ImportedGateways -GatewayIndex 2
```

**REMARKS**

The example reads in a NetScaler configuration package and then imports the first gateway defined in the package, followed by the second and the third.
