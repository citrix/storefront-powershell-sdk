# Get-STFWebReceiverPluginAssistant

Get the WebReceiver Plug-in Assistant options

## Syntax

```
Get-STFWebReceiverPluginAssistant [-WebReceiverService] <WebReceiverService> [<CommonParameters>]
```

## Detailed Description

Get the WebReceiver Plug-in Assistant client options.

## Related Commands

* [Set-STFWebReceiverPluginAssistant](Set-STFWebReceiverPluginAssistant.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|WebReceiverService|The WebReceiver service.|true|true (ByValue)| |

## Input Type

### Citrix.StoreFront.Model.ReceiverForWeb.WebReceiverService

Parameter WebReceiverService: A .NET class representing the configuration of a StoreFront Web Receiver service

## Return Values

### PluginAssistant

The .NET `Citrix.StoreFront.Model.ReceiverForWeb.PluginAssistant` reference type

## Examples

### EXAMPLE 1 Get WebReceiver Plug-in Assistant options

```
$receiver = Get-STFWebReceiverService
Get-STFWebReceiverPluginAssistant -WebReceiverService $receiver
```

**REMARKS**

Get the WebReceiver Plug-in Assistant client options of the only configured 

WebReceiver.

**OUTPUT**

```
Enabled         : True
UpgradeAtLogin  : False
ShowAfterLogin  : False
Win32           : Path : 
http://downloadplugins.citrix.com/Windows/CitrixReceiverWeb.exe

MacOS           : Path                    : 
http://downloadplugins.citrix.com/Mac/CitrixReceiverWeb.dmg
                  MinimumSupportedVersion : 10.6
Html5           : Enabled              : Off
                  Platforms            : 
Firefox;Chrome;Version/([6-9]|\d\d).*Safari;MSIE
                  \d\d;Trident/([6-9]|\d\d);Android;iPad;iPhone;iPod;
                  LaunchUrl            : 
clients/HTML5Client/src/SessionWindow.html
                  Preferences          :
                  SingleTabLaunch      : False
                  ChromeAppOrigins     : 
chrome-extension://haiffjcadagjlijoggckpgfnoeiflnem
                  ChromeAppPreferences :
ProtocolHandler : Enabled                        : True
                  Platforms                      : (Macintosh|Windows
                  NT).*Chrome/((4[2-9]|[56789][0-9])|\d\d\d)(?!.*Edge)
                  SkipDoubleHopCheckWhenDisabled : False
```
