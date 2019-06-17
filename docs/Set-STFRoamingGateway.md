# Set-STFRoamingGateway

Update the settings on a Gateway

## Syntax

```
Set-STFRoamingGateway [-Gateway] <RoamingGateway> [[-LogonType] <UsedForHDXOnly | Domain | RSA | DomainAndRSA | SMS | GatewayKnows | SmartCard | None>] [[-SmartCardFallbackLogonType] <UsedForHDXOnly | Domain | RSA | DomainAndRSA | SMS | GatewayKnows | SmartCard | None>] [[-Version] <Version10_0_69_4 | Version9x>] [[-GatewayUrl] <Uri>] [[-CallbackUrl] <Uri>] [[-SessionReliability] <Boolean>] [[-RequestTicketTwoSTAs] <Boolean>] [[-SubnetIPAddress] <String>] [[-SecureTicketAuthorityUrls] <Uri[]>] [[-PassThru] <SwitchParameter>] [[-GslbUrl] <Uri>] [[-RoamingService] <RoamingService>] [<CommonParameters>]



Set-STFRoamingGateway [-Name] <String> [[-LogonType] <UsedForHDXOnly | Domain | RSA | DomainAndRSA | SMS | GatewayKnows | SmartCard | None>] [[-SmartCardFallbackLogonType] <UsedForHDXOnly | Domain | RSA | DomainAndRSA | SMS | GatewayKnows | SmartCard | None>] [[-Version] <Version10_0_69_4 | Version9x>] [[-GatewayUrl] <Uri>] [[-CallbackUrl] <Uri>] [[-SessionReliability] <Boolean>] [[-RequestTicketTwoSTAs] <Boolean>] [[-SubnetIPAddress] <String>] [[-SecureTicketAuthorityUrls] <Uri[]>] [[-PassThru] <SwitchParameter>] [[-GslbUrl] <Uri>] [[-RoamingService] <RoamingService>] [<CommonParameters>]
```

## Detailed Description

Update the settings of an existing Gateway from the global gateways list.

## Related Commands

* [Add-STFRoamingGateway](Add-STFRoamingGateway.md)
* [Get-STFRoamingGateway](Get-STFRoamingGateway.md)
* [Remove-STFRoamingGateway](Remove-STFRoamingGateway.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|Gateway|The gateway to update|true|true (ByValue)| |
|Name|Name of Gateway to update|true|true (ByValue)| |
|LogonType|The login type required and supported by the Gateway|false|false| |
|SmartCardFallbackLogonType|The login type to use when SmartCard fails|false|false| |
|Version|The Citrix NetScaler Gateway version|false|false| |
|GatewayUrl|The Gateway Url|false|false| |
|CallbackUrl|The Gateway authentication call-back Url|false|false| |
|SessionReliability|Enable session reliability. Session Reliability keeps sessions active and on the user’s screen when network connectivity is interrupted. Users continue to see the application they are using until network connectivity resumes|false|false| |
|RequestTicketTwoSTAs|Request STA tickets from two STA servers (Requires two STA servers)|false|false| |
|SubnetIPAddress|IP address|false|false| |
|SecureTicketAuthorityUrls|Secure Ticket Authority server Urls. The Secure Ticket Authority (STA) is responsible for issuing session tickets in response to connection requests for published resources on XenApp. These session tickets form the basis of authentication and authorization for access to published resources|false|false| |
|PassThru|Output the updated Gateway|false|false| |
|GslbUrl|An optional URL which corresponds to the GSLB domain used by multiple gateways|false|false| |
|RoamingService|The Roaming service|false|false| |

## Input Type

### Citrix.StoreFront.Model.Roaming.RoamingGateway

Parameter Gateway: The .NET `Citrix.StoreFront.Model.Roaming.RoamingGateway` reference type

### System.String

Parameter Name: The .NET `System.String` reference type

### Citrix.StoreFront.Model.Roaming.GatewayLogonType

Parameter LogonType: The .NET `Citrix.StoreFront.Model.Roaming.GatewayLogonType` value type

### Citrix.StoreFront.Model.Roaming.GatewayLogonType

Parameter SmartCardFallbackLogonType: The .NET `Citrix.StoreFront.Model.Roaming.GatewayLogonType` value type

### Citrix.StoreFront.Model.Roaming.GatewayVersion

Parameter Version: The .NET `Citrix.StoreFront.Model.Roaming.GatewayVersion` value type

### System.Uri

Parameter GatewayUrl: The .NET `System.Uri` reference type

### System.Uri

Parameter CallbackUrl: The .NET `System.Uri` reference type

### System.Boolean

Parameter SessionReliability: The .NET `System.Boolean` value type

### System.Boolean

Parameter RequestTicketTwoSTAs: The .NET `System.Boolean` value type

### System.String

Parameter SubnetIPAddress: The .NET `System.String` reference type

### System.Uri[]

Parameter SecureTicketAuthorityUrls: The .NET `System.Uri` reference type

### System.Management.Automation.SwitchParameter

Parameter PassThru: The .NET `System.Management.Automation.SwitchParameter` value type

### System.Uri

Parameter GslbUrl: The .NET `System.Uri` reference type

### Citrix.StoreFront.Model.Roaming.RoamingService

Parameter RoamingService: A .NET class representing the configuration of a StoreFront Roaming service

## Return Values

### None

## Examples

### EXAMPLE 1 Update Gateway

```
Set-STFRoamingGateway -RoamingGateway $gateway -LogonType Domain
```

**REMARKS**

Updates the Gateway to use Domain logon.
