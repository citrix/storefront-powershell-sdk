#Set-STFWebReceiverSiteStyle
Sets the Style info in the custom style sheet
##Syntax
```Set-STFWebReceiverSiteStyle [-WebReceiverService] <WebReceiverService> [[-HeaderLogoPath] <String>] [[-LogonLogoPath] <String>] [[-HeaderBackgroundColor] <String>] [[-HeaderForegroundColor] <String>] [[-LinkColor] <String>] [<CommonParameters>]
```
##Detailed Description
Sets the Style info in the custom style sheet for the unified experience Receiver.
##Related Commands
*[Clear-STFWebReceiverSiteStyle](Clear-STFWebReceiverSiteStyle)
*[Get-STFWebReceiverSiteStyle](Get-STFWebReceiverSiteStyle)
*[Get-STFWebReceiverDefaultSiteStyle](Get-STFWebReceiverDefaultSiteStyle)
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||WebReceiverService|The WebReceiver service to style|true|true (ByValue)||HeaderLogoPath|Header logo path|false|false||LogonLogoPath|Logon logo path|false|false||HeaderBackgroundColor|Background color of the Header|false|false||HeaderForegroundColor|Foreground color of the Header|false|false||LinkColor|Link color of the page|false|false|##Input Type
###Citrix.StoreFront.Model.ReceiverForWeb.WebReceiverService
Parameter WebReceiverService: A .NET class representing the configuration of a StoreFront Web Receiver service
###System.String
Parameter HeaderLogoPath: The .NET 'System.String' reference type
###System.String
Parameter LogonLogoPath: The .NET 'System.String' reference type
###System.String
Parameter HeaderBackgroundColor: The .NET 'System.String' reference type
###System.String
Parameter HeaderForegroundColor: The .NET 'System.String' reference type
###System.String
Parameter LinkColor: The .NET 'System.String' reference type
##Return Values
##Notes
This cmdlet supports styling the following classes
1. Standard resolution icon path
2. High resolution icon path
3. Background color of the header
4. Foreground color of the header
5. Link color of the page
##Examples
###EXAMPLE 1 Configure Receiver images
```$webReceiver = Get-STFWebReceiverService
Set-STFWebReceiverSiteStyle -WebReceiverService $webReceiver -HeaderLogoPath "C:\images\header.jpg" -LogonLogoPath "C:\images\logon.jpg"
```
REMARKS

Configure the Receiver header and logon images.
