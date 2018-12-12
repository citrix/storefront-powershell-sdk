# Set-STFWebReceiverUserInterface

Set the WebReceiver User Interface options

## Syntax

```
Set-STFWebReceiverUserInterface [-WebReceiverService] <WebReceiverService> [[-AutoLaunchDesktop] <Boolean>] [[-MultiClickTimeout] <Int32>] [[-EnableAppsFolderView] <Boolean>] [[-ShowAppsView] <Boolean>] [[-ShowDesktopsView] <Boolean>] [[-DefaultView] <Auto | Desktops | Apps>] [[-WorkspaceControlEnabled] <Boolean>] [[-WorkspaceControlAutoReconnectAtLogon] <Boolean>] [[-WorkspaceControlLogoffAction] <Disconnect | Terminate | None>] [[-WorkspaceControlShowReconnectButton] <Boolean>] [[-WorkspaceControlShowDisconnectButton] <Boolean>] [[-ReceiverConfigurationEnabled] <Boolean>] [[-AppShortcutsEnabled] <Boolean>] [[-AppShortcutsAllowSessionReconnect] <Boolean>] [<CommonParameters>]
```

## Detailed Description

Set the WebReceiver User Interface client options.

## Related Commands

* [Get-STFWebReceiverUserInterface](./Get-STFWebReceiverUserInterface)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|WebReceiverService|The WebReceiver service.|true|true (ByValue)| |
|AutoLaunchDesktop|Whether to auto-launch desktop at login if there is only one desktop available for the user.|false|false| |
|MultiClickTimeout|The time period for which the spinner control is displayed, after the user clicks on the App/Desktop icon within Receiver for Web.|false|false| |
|EnableAppsFolderView|Allows the user to turn off folder view when in a locked-down store or unauthenticated store.|false|false| |
|ShowAppsView|Whether to show the apps view tab.|false|false| |
|ShowDesktopsView|Whether to show the desktops tab.|false|false| |
|DefaultView|The view to show after logon.|false|false| |
|WorkspaceControlEnabled|Whether to enable workspace control.|false|false| |
|WorkspaceControlAutoReconnectAtLogon|Whether to perform auto-reconnect at login.|false|false| |
|WorkspaceControlLogoffAction|Whether to disconnect or terminate HDX sessions when actively logging off Receiver for Web.|false|false| |
|WorkspaceControlShowReconnectButton|Whether to show the reconnect button/link.|false|false| |
|WorkspaceControlShowDisconnectButton|Whether to show the disconnect button/link.|false|false| |
|ReceiverConfigurationEnabled|Enable the Receiver Configuration .CR download file.|false|false| |
|AppShortcutsEnabled|Enable App Shortcuts.|false|false| |
|AppShortcutsAllowSessionReconnect|Enable App Shortcuts to support session reconnect.|false|false| |

## Input Type

### Citrix.StoreFront.Model.ReceiverForWeb.WebReceiverService

Parameter WebReceiverService: A .NET class representing the configuration of a StoreFront Web Receiver service

### System.Boolean

Parameter AutoLaunchDesktop: The .NET `System.Boolean` value type

### System.Int32

Parameter MultiClickTimeout: The .NET `System.Int32` value type

### System.Boolean

Parameter EnableAppsFolderView: The .NET `System.Boolean` value type

### System.Boolean

Parameter ShowAppsView: The .NET `System.Boolean` value type

### System.Boolean

Parameter ShowDesktopsView: The .NET `System.Boolean` value type

### Citrix.StoreFront.Model.ReceiverForWeb.DefaultUIView

Parameter DefaultView: The .NET `Citrix.StoreFront.Model.ReceiverForWeb.DefaultUIView` value type

### System.Boolean

Parameter WorkspaceControlEnabled: The .NET `System.Boolean` value type

### System.Boolean

Parameter WorkspaceControlAutoReconnectAtLogon: The .NET `System.Boolean` value type

### Citrix.StoreFront.Model.ReceiverForWeb.LogoffAction

Parameter WorkspaceControlLogoffAction: The .NET `Citrix.StoreFront.Model.ReceiverForWeb.LogoffAction` value type

### System.Boolean

Parameter WorkspaceControlShowReconnectButton: The .NET `System.Boolean` value type

### System.Boolean

Parameter WorkspaceControlShowDisconnectButton: The .NET `System.Boolean` value type

### System.Boolean

Parameter ReceiverConfigurationEnabled: The .NET `System.Boolean` value type

### System.Boolean

Parameter AppShortcutsEnabled: The .NET `System.Boolean` value type

### System.Boolean

Parameter AppShortcutsAllowSessionReconnect: The .NET `System.Boolean` value type

## Return Values

### None

## Examples

### EXAMPLE 1 Set WebReceiver multi-click timeout and desktop auto launch User Interface options

```
$receiver = Get-STFWebReceiverService
Set-STFWebReceiverUserInterface -WebReceiverService $receiver -AutoLaunchDesktop $false -MultiClickTimeout 10
```

**REMARKS**

Set WebReceiver multi-click timeout to 10 seconds and disable desktop auto launch in the User Interface options.
