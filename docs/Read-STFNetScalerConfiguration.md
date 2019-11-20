#Read-STFNetScalerConfiguration
Read a NetScaler remote access configuration
##Syntax
```Read-STFNetScalerConfiguration [-Path] <String> [<CommonParameters>]
```
##Detailed Description
Reads a NetScaler remote access configuration package into a NetScalerConfigurationDocument object to be imported into StoreFront.
##Related Commands
*[Test-STFSecureTicketAuthority](Test-STFSecureTicketAuthority)
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||Path|The NetScaler configuration file path.|true|true (ByValue)|##Input Type
###System.String
Parameter Path: The .NET 'System.String' reference type
##Return Values
###NetScalerConfigurationDocument
The .NET 'Citrix.StoreFront.Model.Roaming.NetScalerConfiguration.NetScalerConfigurationDocument' reference type
##Notes
Configuration files are exported from NetScaler Gateway in .zip file format.
##Examples
###EXAMPLE 1 Read configuration package
```$netscalerConfiguration = Read-STFNetScalerConfiguration –Path C:\NSG\Configuration.zip
```
REMARKS

The populated object can be supplied to the related cmdlets for validation and import.
OUTPUT
```Certificate : [Subject]
CN=Example Certificate

[Issuer]
  CN=Example NetScaler certificate

[Serial Number]
  26E230B95A8FC3BA49E5A59C8026473E

[Not Before]
  27/02/2013 09:41:26

[Not After]
  31/12/2039 23:59:59

[Thumbprint]
  96FA87705E10654AAF0A7E88BB46A7D77DC154CA

Version     : 1.0
Time        : 2016-01-25T15:37:22.34
Document    : Citrix.StoreFront.Model.Roaming.NetScalerConfiguration.Document
```
###EXAMPLE 2 Read configuration package with verbose messaging
```Read-STFNetScalerConfiguration –Path C:\NSG\Configuration.zip -Verbose
```
REMARKS

The populated object can be supplied to the related cmdlets for validation and import. Messages related to the import
are output to the console
OUTPUT
```Certificate : [Subject]
CN=Example Certificate

[Issuer]
  CN=Example NetScaler certificate

[Serial Number]
  26E230B95A8FC3BA49E5A59C8026473E

[Not Before]
  27/02/2013 09:41:26

[Not After]
  31/12/2039 23:59:59

[Thumbprint]
  96FA87705E10654AAF0A7E88BB46A7D77DC154CA

Version     : 1.0
Time        : 2016-01-25T15:37:22.34
Document    : Citrix.StoreFront.Model.Roaming.NetScalerConfiguration.Document

VERBOSE: The gateway id us.gateway.citrix.com:443 has no Secure Ticket Authorities defined so can only be used for
authentication.
VERBOSE: The gateway id uk.gateway.citrix.com:443 has no Secure Ticket Authorities defined so can only be used for
authentication.
```
###EXAMPLE 3 Read configuration package
```$ImportedGateways = Read-STFNetScalerConfiguration -path "$env:USERPROFILE\desktop\GatewayConfig.zip" 
                           $ImportedGateways.Document.Gateways
```
REMARKS

The populated object can be inspected as shown to list all the gateway definitions. Messages related to the import are
output to the console
OUTPUT
```GatewayMode            : CVPN
                          CallbackUrl            :
                          GslbAddressUri         : https://gateway.domain.com/
                          AddressUri             : https://ukgateway.domain.com/
                          Address                : https://ukgateway.domain.com:443
                          GslbAddress            : https://gateway.domain.com.com:443
                          VipAddress             : 10.0.0.1
                          Stas                   : {STA298854503, STA909374257, STA443006025, STA490101972...}
                          StaLoadBalance         : True
                          CertificateThumbprints : {F549AFAA29EBF61E8709F2316B3981AD503AF387}
                          GatewayAuthType        : Domain
                          GatewayEdition         : Enterprise
                          ReceiverForWebSites    : 
{Citrix.StoreFront.Model.Roaming.NetScalerConfiguration.ReceiverForWebSite}

                          GatewayMode            : CVPN
                          CallbackUrl            :
                          GslbAddressUri         : https://gateway.domain.com/
                          AddressUri             : https://ukgateway.domain.com/
                          Address                : https://ukgateway.domain.com:443
                          GslbAddress            : https://gateway.domain.com.com:443
                          VipAddress             : 10.0.0.2
                          Stas                   : {STA298854503, STA909374257, STA443006025, STA490101972...}
                          StaLoadBalance         : True
                          CertificateThumbprints : {F549AFAA29EBF61E8709F2316B3981AD503AF387}
                          GatewayAuthType        : DomainAndRSA
                          GatewayEdition         : Enterprise
                          ReceiverForWebSites    : 
{Citrix.StoreFront.Model.Roaming.NetScalerConfiguration.ReceiverForWebSite}
```
###EXAMPLE 4 Read configuration package
```$ImportedGateways = Read-STFNetScalerConfiguration -path "$env:USERPROFILE\desktop\GatewayConfig.zip" -GatewayIndex 0 
                           $ImportedGateways.Document.Gateways[0]
```
REMARKS

The populated object can be inspected as shown to show an individual gateway definition. Messages related to the
import are output to the console
OUTPUT
```GatewayMode            : CVPN
                          CallbackUrl            :
                          GslbAddressUri         : https://gateway.domain.com/
                          AddressUri             : https://ukgateway.domain.com/
                          Address                : https://ukgateway.domain.com:443
                          GslbAddress            : https://gateway.domain.com.com:443
                          VipAddress             : 10.0.0.1
                          Stas                   : {STA298854503, STA909374257, STA443006025, STA490101972...}
                          StaLoadBalance         : True
                          CertificateThumbprints : {F549AFAA29EBF61E8709F2316B3981AD503AF387}
                          GatewayAuthType        : Domain
                          GatewayEdition         : Enterprise
                          ReceiverForWebSites    : 
{Citrix.StoreFront.Model.Roaming.NetScalerConfiguration.ReceiverForWebSite}
```
