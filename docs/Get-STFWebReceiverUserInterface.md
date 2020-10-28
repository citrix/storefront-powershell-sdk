# Get-STFWebReceiverUserInterface

Get the Receiver for Web user interface options

## Syntax

```
Get-STFWebReceiverUserInterface [-WebReceiverService] <WebReceiverService> [<CommonParameters>]
```

## Detailed Description

Get the Receiver for Web user interface client options.

## Related Commands

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|WebReceiverService|The Receiver for Web service.|true|true (ByValue)| |

## Input Type

### Citrix.StoreFront.Model.ReceiverForWeb.WebReceiverService

Parameter WebReceiverService: A .NET class representing the configuration of a StoreFront Receiver for Web service

## Return Values

### UserInterface

The .NET `Citrix.StoreFront.Model.ReceiverForWeb.UserInterface` reference type

## Examples

### EXAMPLE 1 Get WebReceiver User Interface options

```
$receiver = Get-STFWebReceiverService
Get-STFWebReceiverUserInterface -WebReceiverService $receiver
```

**REMARKS**

Get the Receiver for Web user interface options of the only configured Receiver for Web site.

**OUTPUT**

```
AutoLaunchDesktop     : True
MultiClickTimeout     : 3
CategoryViewCollapsed : False
EnableAppsFolderView  : True
WorkspaceControl      : Enabled              : True
                        AutoReconnectAtLogon : True
                        LogoffAction         : Disconnect
                        ShowReconnectButton  : False
                        ShowDisconnectButton : False
ReceiverConfiguration : Enabled     : True
                        DownloadUrl : ServiceRecord/GetDocument/receiverconfig.cr
AppShortcuts          : Enabled               : False
                        AllowSessionReconnect : False
UIViews               : ShowAppsView     : True
                        ShowDesktopsView : True
                        DefaultView      : Auto
```