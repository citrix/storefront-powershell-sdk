# Update-STFSecureTicketAuthority

Update a NetScaler gateway STA configuration

## Syntax

```
Update-STFSecureTicketAuthority [-StaConfigurationObject] <IStaServerData> [-StaServers] <Hashtable> [<CommonParameters>]
```

## Detailed Description

Update a PowerShell object populated with a NetScaler gateway STA configuration. The cmdlet can be used to update invalid or uncontactable STA servers.

## Related Commands

* [Read-STFNetScalerConfiguration](Read-STFNetScalerConfiguration.md)
* [Test-STFSecureTicketAuthority](Test-STFSecureTicketAuthority.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|StaConfigurationObject|A configuration object supporting validation of STA servers.|true|true (ByValue)| |
|StaServers|A hashtable of STA urls present in the configuration mapped to the required STA urls.|true|false| |

## Input Type

### Citrix.StoreFront.Model.Roaming.NetScalerConfiguration.IStaServerData

Parameter StaConfigurationObject: The .NET `Citrix.StoreFront.Model.Roaming.NetScalerConfiguration.IStaServerData` reference type

### System.Collections.Hashtable

Parameter StaServers: The .NET `System.Collections.Hashtable` reference type

## Return Values

### None

## Examples

### EXAMPLE 1 Update a NetScaler gateway STA configuration

```
$netscalerConfiguration = Read-STFNetScalerConfiguration –Path C:\NSG\Configuration.zip
# Test cmdlet returns two invalid STA servers that cannot be resolved
$results = Test-STFSecureTicketAuthority -StaConfigurationObject
# Update the invalid STA servers
Update-STFSecureTicketAuthority -StaConfigurationObject $netscalerConfiguration –StaServers @{ “https://invalidsta1.com” = “https://validsta1.com”, “https://invalidsta2.com” = “https://validsta2.com” }
```

**REMARKS**

Updates STA server urls within the configuration object with new STA urls.

An STA url provided by NetScaler may not resolve on an internal network so 

will need updating to a StoreFront local address.
