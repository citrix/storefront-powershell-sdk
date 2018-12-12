# Set-STFStoreService

Configure the Store service

## Syntax

```
Set-STFStoreService [-StoreService] <StoreService> [[-RDPOnly] <Boolean>] [[-IcaTemplateName] <String>] [[-IcaFileSigning] <Boolean>] [[-IcaFileSigningCertificateThumbprint] <String>] [[-IcaFileSigningHashAlgorithm] <String>] [[-AuthenticationService] <AuthenticationService>] [[-KerberosDelegation] <Boolean>] [[-Force] <SwitchParameter>] [[-AllowSessionReconnect] <Boolean>] [[-SubstituteDesktopImage] <Boolean>] [[-UnifiedReceiver] <WebReceiverService>] [[-LockedDown] <Boolean>] [[-PassThru] <SwitchParameter>] [<CommonParameters>]
```

## Detailed Description

Configure high level options on the Store service.

## Related Commands

* [Get-STFStoreService](./Get-STFStoreService)
* [Remove-STFStoreService](./Remove-STFStoreService)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|StoreService|The Store service|true|true (ByValue)| |
|RDPOnly|Configure the Store to launch all requests using the RDP protocol.|false|false| |
|IcaTemplateName|Ica template to use when launching an application or desktop.|false|false| |
|IcaFileSigning|Sign the ica file used for launch.|false|false| |
|IcaFileSigningCertificateThumbprint|Thumbprint of the certificate to use for signing the ica file.|false|false| |
|IcaFileSigningHashAlgorithm|Algorithm used to sign the ica file. The setting should not normally require changing from the default.|false|false| |
|AuthenticationService|The Authentication service and the Store should use. Will result in the Store using the authentication protocols of the service.|false|false| |
|KerberosDelegation|Turn on Kerberos delegation for the Store to support XenApp 6.5 and earlier constrained delegation.|false|false| |
|Force|Force settings to be applied ignoring confirmation prompts.|false|false| |
|AllowSessionReconnect|Allow sessions to be reconnected.|false|false| |
|SubstituteDesktopImage|Substitute the desktop image provided by XenApp\XenDesktop with the StoreFront default.|false|false| |
|UnifiedReceiver|Choose the classic of unified Receiver experience.|false|false| |
|LockedDown|All the resources delivered by locked-down Store are auto subscribed and do not allow for un-subscription.|false|false| |
|PassThru|Output the resulting Store service.|false|false| |

## Input Type

### Citrix.StoreFront.Model.Store.StoreService

Parameter StoreService: A .NET class representing the configuration of a StoreFront Store service

### System.Boolean

Parameter RDPOnly: The .NET `System.Boolean` value type

### System.String

Parameter IcaTemplateName: The .NET `System.String` reference type

### System.Boolean

Parameter IcaFileSigning: The .NET `System.Boolean` value type

### System.String

Parameter IcaFileSigningCertificateThumbprint: The .NET `System.String` reference type

### System.String

Parameter IcaFileSigningHashAlgorithm: The .NET `System.String` reference type

### Citrix.StoreFront.Model.Authentication.AuthenticationService

Parameter AuthenticationService: A .NET class representing the configuration of a StoreFront Authentication service

### System.Boolean

Parameter KerberosDelegation: The .NET `System.Boolean` value type

### System.Management.Automation.SwitchParameter

Parameter Force: The .NET `System.Management.Automation.SwitchParameter` value type

### System.Boolean

Parameter AllowSessionReconnect: The .NET `System.Boolean` value type

### System.Boolean

Parameter SubstituteDesktopImage: The .NET `System.Boolean` value type

### Citrix.StoreFront.Model.ReceiverForWeb.WebReceiverService

Parameter UnifiedReceiver: A .NET class representing the configuration of a StoreFront Web Receiver service

### System.Boolean

Parameter LockedDown: The .NET `System.Boolean` value type

### System.Management.Automation.SwitchParameter

Parameter PassThru: The .NET `System.Management.Automation.SwitchParameter` value type

## Return Values

### None

## Examples

### EXAMPLE 1 Sign Ica files

```
$storeService = Get-STFStoreService
Set-STFStoreService $storeService -IcaFileSigning $true -IcaFileSigningCertificateThumbprint a909502dd82ae41433e6f83886b00d4277a32a7b
```

**REMARKS**

Configure the Store to sign ica files using the certificate with the supplied thumbprint.
