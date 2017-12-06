#Get-STFWebReceiverApplicationShortcuts
Get the WebReceiver application shortcuts
##Syntax
```Get-STFWebReceiverApplicationShortcuts [-WebReceiverService] <WebReceiverService> [<CommonParameters>]
```
##Detailed Description
Get the WebReceiver application shortcuts.
##Related Commands
*[Set-STFWebReceiverApplicationShortcuts](Set-STFWebReceiverApplicationShortcuts)
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||WebReceiverService|The WebReceiver service.|true|true (ByValue)|##Input Type
###Citrix.StoreFront.Model.ReceiverForWeb.WebReceiverService
Parameter WebReceiverService: A .NET class representing the configuration of a StoreFront Web Receiver service
##Return Values
###AppShortcutsServer
The .NET 'Citrix.StoreFront.Model.ReceiverForWeb.AppShortcutsServer' reference type
##Examples
###EXAMPLE 1 Get WebReceiver Application Shortcuts
```$receiver = Get-STFWebReceiverService
Get-STFWebReceiverApplicationShortcuts -WebReceiverService $receiver
```
REMARKS

Get the WebReceiver application shortcuts of the only configured WebReceiver.
OUTPUT
```PromptForUntrustedShortcuts : True
TrustedUrls                 : {http://mycompany.com/}
GatewayUrls                 : {https://mycompanygateway.com/}
```
