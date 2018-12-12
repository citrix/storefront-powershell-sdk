# New-STFRoamingGateway

Create a new in memory Gateway that can be added and used for remote access and authentication.

## Syntax

```
New-STFRoamingGateway [-Name] <String> [-LogonType] <UsedForHDXOnly | Domain | RSA | DomainAndRSA | SMS | GatewayKnows | SmartCard | None> [[-SmartCardFallbackLogonType] <UsedForHDXOnly | Domain | RSA | DomainAndRSA | SMS | GatewayKnows | SmartCard | None>] [[-Version] <Version10_0_69_4 | Version9x>] [-GatewayUrl] <Uri> [[-CallbackUrl] <Uri>] [[-SessionReliability] <SwitchParameter>] [[-RequestTicketTwoSTAs] <SwitchParameter>] [[-SubnetIPAddress] <String>] [[-SecureTicketAuthorityUrls] <Uri[]>] [[-StasUseLoadBalancing] <SwitchParameter>] [[-StasBypassDuration] <TimeSpan>] [[-GslbUrl] <Uri>] [<CommonParameters>]
```

## Detailed Description

Create a new Gateway that can be added to the global gateway list. Gateways for remote access and authentication are added to Stores from the globally managed list.

## Related Commands

* [Get-STFRoamingGateway](./Get-STFRoamingGateway)
* [Remove-STFRoamingGateway](./Remove-STFRoamingGateway)
* [Set-STFRoamingGateway](./Set-STFRoamingGateway)
* [Add-STFRoamingGateway](./Add-STFRoamingGateway)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|Name|Gateway friendly name|true|true (ByValue)| |
|LogonType|The login type required and supported by the Gateway|true|false| |
|SmartCardFallbackLogonType|The login type to use when SmartCard fails|false|false| |
|Version|The Citrix NetScaler Gateway version|false|false| |
|GatewayUrl|The Gateway Url|true|false| |
|CallbackUrl|The Gateway authentication call-back Url|false|false| |
|SessionReliability|Enable session reliability. Session Reliability keeps sessions active and on the user’s screen when network connectivity is interrupted. Users continue to see the application they are using until network connectivity resumes|false|false| |
|RequestTicketTwoSTAs|Request STA tickets from two STA servers (Requires two STA servers)|false|false| |
|SubnetIPAddress|IP address|false|false| |
|SecureTicketAuthorityUrls|Secure Ticket Authority server Urls. The Secure Ticket Authority (STA) is responsible for issuing session tickets in response to connection requests for published resources on XenApp. These session tickets form the basis of authentication and authorization for access to published resources|false|false| |
|StasUseLoadBalancing|Load balance between the configured STA servers (requires two or more STA servers)|false|false| |
|StasBypassDuration|Time before retrying a failed STA server|false|false| |
|GslbUrl|An optional URL which corresponds to the GSLB domain used by multiple gateways|false|false| |

## Input Type

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

### System.Management.Automation.SwitchParameter

Parameter SessionReliability: The .NET `System.Management.Automation.SwitchParameter` value type

### System.Management.Automation.SwitchParameter

Parameter RequestTicketTwoSTAs: The .NET `System.Management.Automation.SwitchParameter` value type

### System.String

Parameter SubnetIPAddress: The .NET `System.String` reference type

### System.Uri[]

Parameter SecureTicketAuthorityUrls: The .NET `System.Uri` reference type

### System.Management.Automation.SwitchParameter

Parameter StasUseLoadBalancing: The .NET `System.Management.Automation.SwitchParameter` value type

### System.TimeSpan

Parameter StasBypassDuration: The .NET `System.TimeSpan` value type

### System.Uri

Parameter GslbUrl: The .NET `System.Uri` reference type

## Return Values

### RoamingGateway

The .NET `Citrix.StoreFront.Model.Roaming.RoamingGateway` reference type

## Examples

### EXAMPLE 1 Add Version 10x Gateway

```
$gw New-STFRoamingGateway -Name "Netscaler10x" -LogonType Domain -Version Version10_0_69_4 -GatewayUrl https://gateway.citrix.storefront -CallbackUrl https://gateway.citrix.storefront/callback -SessionReliability:$true -RequestTicketTwoSTAs:$true -SubnetIPAddress 10.80.5.170 -SecureTicketAuthorityUrls https://XenApp1STA,https://XenApp2STA -PassThru
Add-STFRoamingGateway $gw
```

**REMARKS**

Add a version 10 or greater Gateway.

### EXAMPLE 2 Add Version 9 Gateway

```
Add-STFRoamingGateway -Name "Netscaler9" -LogonType SmartCard -SmartCardFallbackLogonType Domain -Version Version9x -GatewayUrl https://EuNetscaler -CallbackUrl https://EuNetscaler/Callback -SessionReliability -RequestTicketTwoSTAs -SubnetIPAddress 10.80.5.170 -SecureTicketAuthorityUrls https://myxs/STA -PassThru
```

**REMARKS**

Add a version 9 Gateway.
