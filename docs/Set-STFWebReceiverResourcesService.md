# Set-STFWebReceiverResourcesService

Set the WebReceiver Resources Service settings

## Syntax

```
Set-STFWebReceiverResourcesService [-WebReceiverService] <WebReceiverService> [[-PersistentIconCacheEnabled] <Boolean>] [[-IcaFileCacheExpiry] <Int32>] [[-IconSize] <Int32>] [[-ShowDesktopViewer] <Boolean>] [<CommonParameters>]
```

## Detailed Description

Set the WebReceiver Resources Service settings.

## Related Commands

* [Get-STFWebReceiverResourcesService](Get-STFWebReceiverResourcesService.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|WebReceiverService|The WebReceiver service.|true|true (ByValue)| |
|PersistentIconCacheEnabled|Whether to cache icon data in the local file system.|false|false| |
|IcaFileCacheExpiry|How long the ICA file data is cached in the memory of the Web Proxy.|false|false| |
|IconSize|The desired icon size sent to the Store Service in icon requests.|false|false| |
|ShowDesktopViewer|Shows the Citrix Desktop Viewer window and toolbar when users access their desktops from legacy clients. This setting may fix problems where the Desktop Viewer is not displayed. Default: Off.|false|false| |

## Input Type

### Citrix.StoreFront.Model.ReceiverForWeb.WebReceiverService

Parameter WebReceiverService: A .NET class representing the configuration of a StoreFront Web Receiver service

### System.Boolean

Parameter PersistentIconCacheEnabled: The .NET `System.Boolean` value type

### System.Int32

Parameter IcaFileCacheExpiry: The .NET `System.Int32` value type

### System.Int32

Parameter IconSize: The .NET `System.Int32` value type

### System.Boolean

Parameter ShowDesktopViewer: The .NET `System.Boolean` value type

## Return Values

### None

## Examples

### EXAMPLE 1 Configure the Desktop viewer

```
$webReceiver = Get-STFWebReceiverService "/Citrix/StoreWeb"
Set-STFWebReceiverResourcesService -WebReceiverService $webReceiver -ShowDesktopViewer $true
```

**REMARKS**

Set the Desktop Viewer to be shown for the WebReceiver located at 

/Citrix/StoreWeb.
