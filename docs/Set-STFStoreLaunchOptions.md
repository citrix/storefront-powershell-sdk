# Set-STFStoreLaunchOptions

Set Store launch options

## Syntax

```
Set-STFStoreLaunchOptions [-StoreService] <StoreService> [[-AddressResolutionType] <Dns | DnsPort | IPV4 | IPV4Port | Dot | DotPort | Uri | NoChange>] [[-RequestIcaClientSecureChannel] <SSLAnyCiphers | TLSGovCipers | DetectAnyCiphers>] [[-AllowSpecialFolderRedirection] <Boolean>] [[-AllowFontSmoothing] <Boolean>] [[-RequireLaunchReference] <Boolean>] [[-OverrideIcaClientName] <Boolean>] [[-OverlayAutoLoginCredentialsWithTicket] <Boolean>] [[-IgnoreClientProvidedClientAddress] <Boolean>] [[-SetNoLoadBiasFlag] <Boolean>] [[-RDPOnly] <Boolean>] [[-IcaTemplateName] <String>] [[-VdaLogonDataProvider] <String>] [[-Force] <SwitchParameter>] [[-PassThru] <SwitchParameter>] [<CommonParameters>]
```

## Detailed Description

Set the options used by a Store when launching an application or desktop on XenApp and XenDesktop.

## Related Commands

* [Get-STFStoreLaunchOptions](Get-STFStoreLaunchOptions.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|StoreService|Store service|true|true (ByValue)| |
|AddressResolutionType|Specifies the type of address to use in the .ica launch file|false|false| |
|RequestIcaClientSecureChannel|Specifies TLS settings|false|false| |
|AllowSpecialFolderRedirection|Redirect special folders such as Documents, Computer and the Desktop|false|false| |
|AllowFontSmoothing|Specifies whether or not font smoothing is permitted for ICA sessions|false|false| |
|RequireLaunchReference|Specifies whether or not the use of launch references is enforced|false|false| |
|OverrideIcaClientName|Specifies whether or not a Web Interface-generated ID must be passed in the clientname entry of an .ica launch file|false|false| |
|OverlayAutoLoginCredentialsWithTicket|Specifies whether a logon ticket must be duplicated in a logon ticket entry or placed in a separate .ica launch file ticket entry only|false|false| |
|IgnoreClientProvidedClientAddress|Specifies whether or not to ignore the address provided by the Citrix client|false|false| |
|SetNoLoadBiasFlag|Specifies whether XenApp load bias should be used|false|false| |
|RDPOnly|Configure the Store to only launch use the RDP protocol|false|false| |
|IcaTemplateName|Ica template to use when launching an application or desktop|false|false| |
|VdaLogonDataProvider|The Vda logon data provider to use during launch|false|false| |
|Force|Force update without confirmation|false|false| |
|PassThru|The resulting Store service|false|false| |

## Input Type

### Citrix.StoreFront.Model.Store.StoreService

Parameter StoreService: A .NET class representing the configuration of a StoreFront Store service

### Citrix.StoreFront.Model.Store.AddressResolutionType

Parameter AddressResolutionType: The .NET `Citrix.StoreFront.Model.Store.AddressResolutionType` value type

### Citrix.StoreFront.Model.Store.RequestICAClientSecureChannel

Parameter RequestIcaClientSecureChannel: The .NET `Citrix.StoreFront.Model.Store.RequestICAClientSecureChannel` value type

### System.Boolean

Parameter AllowSpecialFolderRedirection: The .NET `System.Boolean` value type

### System.Boolean

Parameter AllowFontSmoothing: The .NET `System.Boolean` value type

### System.Boolean

Parameter RequireLaunchReference: The .NET `System.Boolean` value type

### System.Boolean

Parameter OverrideIcaClientName: The .NET `System.Boolean` value type

### System.Boolean

Parameter OverlayAutoLoginCredentialsWithTicket: The .NET `System.Boolean` value type

### System.Boolean

Parameter IgnoreClientProvidedClientAddress: The .NET `System.Boolean` value type

### System.Boolean

Parameter SetNoLoadBiasFlag: The .NET `System.Boolean` value type

### System.Boolean

Parameter RDPOnly: The .NET `System.Boolean` value type

### System.String

Parameter IcaTemplateName: The .NET `System.String` reference type

### System.String

Parameter VdaLogonDataProvider: The .NET `System.String` reference type

### System.Management.Automation.SwitchParameter

Parameter Force: The .NET `System.Management.Automation.SwitchParameter` value type

### System.Management.Automation.SwitchParameter

Parameter PassThru: The .NET `System.Management.Automation.SwitchParameter` value type

## Return Values

### None

## Examples

### EXAMPLE 1 Set Store launch options

```
$storeService = Get-STFStoreService
Set-STFStoreLaunchOptions $storeService -AddressResolutionType Dns -RequestIcaClientSecureChannel DetectAnyCiphers -AllowSpecialFolderRedirection $true -AllowFontSmoothing $true
```

**REMARKS**

Set the Store to use Dns address resolution type, Ica secure channel to 

DetectAnyCiphers, allow folder redirection and font smoothing.

### EXAMPLE 2 Set the Vda logon data provider

```
$storeService = Get-STFStoreService
Set-STFStoreLaunchOptions -StoreService $storeService -VdaLogonDataProvider 'FASLogonDataProvider'
```

**REMARKS**

Set the Store to use the Federated Authentication Service Vda logon data 

provider during launch.
