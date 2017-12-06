#Set-STFWebReceiverPluginAssistant
Set the WebReceiver Plug-in Assistant options
##Syntax
```Set-STFWebReceiverPluginAssistant [-WebReceiverService] <WebReceiverService> [[-Enabled] <Boolean>] [[-UpgradeAtLogin] <Boolean>] [[-ShowAfterLogin] <Boolean>] [[-Win32Path] <String>] [[-MacOSPath] <String>] [[-MacOSMinimumSupportedVersion] <String>] [[-Html5Enabled] <Off | Always | Fallback>] [[-Html5Platforms] <String>] [[-Html5Preferences] <String>] [[-Html5SingleTabLaunch] <Boolean>] [[-Html5ChromeAppOrigins] <String>] [[-Html5ChromeAppPreferences] <String>] [[-ProtocolHandlerEnabled] <Boolean>] [[-ProtocolHandlerPlatforms] <String>] [[-ProtocolHandlerSkipDoubleHopCheckWhenDisabled] <Boolean>] [<CommonParameters>]
```
##Detailed Description
Set the WebReceiver Plug-in Assistant client options.
##Related Commands
*[Get-STFWebReceiverPluginAssistant](Get-STFWebReceiverPluginAssistant)
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||WebReceiverService|The WebReceiver service.|true|true (ByValue)||Enabled|Enable Receiver client detection.|false|false||UpgradeAtLogin|Prompt to upgrade older clients.|false|false||ShowAfterLogin|Show Receiver client detection after the user logs in.|false|false||Win32Path|Path to the Windows Receiver.|false|false||MacOSPath|Path to the MacOS Receiver.|false|false||MacOSMinimumSupportedVersion|Minimum version of the MacOS supported.|false|false||Html5Enabled|Method of deploying and using the Html5 Receiver.|false|false||Html5Platforms|The supported Html5 platforms.|false|false||Html5Preferences|Html5 Receiver preferences.|false|false||Html5SingleTabLaunch|Launch Html5 Receiver in the same browser tab.|false|false||Html5ChromeAppOrigins|The Html5 Chrome Application Origins settings.|false|false||Html5ChromeAppPreferences|The Html5 Chrome Application preferences.|false|false||ProtocolHandlerEnabled|Enable the Receiver Protocol Handler.|false|false||ProtocolHandlerPlatforms|The supported Protocol Handler platforms.|false|false||ProtocolHandlerSkipDoubleHopCheckWhenDisabled|Skip the Protocol Handle double hop check.|false|false|##Input Type
###Citrix.StoreFront.Model.ReceiverForWeb.WebReceiverService
Parameter WebReceiverService: A .NET class representing the configuration of a StoreFront Web Receiver service
###System.Boolean
Parameter Enabled: The .NET 'System.Boolean' value type
###System.Boolean
Parameter UpgradeAtLogin: The .NET 'System.Boolean' value type
###System.Boolean
Parameter ShowAfterLogin: The .NET 'System.Boolean' value type
###System.String
Parameter Win32Path: The .NET 'System.String' reference type
###System.String
Parameter MacOSPath: The .NET 'System.String' reference type
###System.String
Parameter MacOSMinimumSupportedVersion: The .NET 'System.String' reference type
###Citrix.StoreFront.Model.ReceiverForWeb.Html5ClientMode
Parameter Html5Enabled: The .NET 'Citrix.StoreFront.Model.ReceiverForWeb.Html5ClientMode' value type
###System.String
Parameter Html5Platforms: The .NET 'System.String' reference type
###System.String
Parameter Html5Preferences: The .NET 'System.String' reference type
###System.Boolean
Parameter Html5SingleTabLaunch: The .NET 'System.Boolean' value type
###System.String
Parameter Html5ChromeAppOrigins: The .NET 'System.String' reference type
###System.String
Parameter Html5ChromeAppPreferences: The .NET 'System.String' reference type
###System.Boolean
Parameter ProtocolHandlerEnabled: The .NET 'System.Boolean' value type
###System.String
Parameter ProtocolHandlerPlatforms: The .NET 'System.String' reference type
###System.Boolean
Parameter ProtocolHandlerSkipDoubleHopCheckWhenDisabled: The .NET 'System.Boolean' value type
##Return Values
##Examples
###EXAMPLE 1 Set WebReceiver Plug-in Assistant options
```$receiver = Get-STFWebReceiverService
Set-STFWebReceiverPluginAssistant -WebReceiverService $receiver -UpgradeAtLogin $true
```
REMARKS

Set the WebReceiver Plug-in Assistant client options to upgrade Receiver at login.
