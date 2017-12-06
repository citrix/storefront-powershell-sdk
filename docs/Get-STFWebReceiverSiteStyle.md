#Get-STFWebReceiverSiteStyle
Gets the site styles for the Receiver for web site
##Syntax
```Get-STFWebReceiverSiteStyle [-WebReceiverService] <WebReceiverService> [<CommonParameters>]
```
##Detailed Description
The style information is retrieved from css file of the site. This style is limited to the non-classic experience.
##Related Commands
*[Clear-STFWebReceiverSiteStyle](Clear-STFWebReceiverSiteStyle)
*[Get-STFWebReceiverDefaultSiteStyle](Get-STFWebReceiverDefaultSiteStyle)
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||WebReceiverService|WebReceiver from which to get the style from|true|true (ByValue)|##Input Type
###Citrix.StoreFront.Model.ReceiverForWeb.WebReceiverService
Parameter WebReceiverService: A .NET class representing the configuration of a StoreFront Web Receiver service
##Return Values
###SiteStyle
The .NET 'Citrix.StoreFront.Model.ReceiverForWeb.SiteStyle' reference type
##Notes
Following is the precedence of retrieving the style details
1. Look up in the custom style sheet
2. If 1 fails then look up in the default style sheet
3. If 1 and 2 failed then use the harcoded values
##Examples
###EXAMPLE 1 Get current site style
```$webReceiver = Get-STFWebReceiverService
Get-STFWebReceiverSiteStyle -WebReceiverService $webReceiver
```
REMARKS

Get the style of the only configured WebReceiver service.
OUTPUT
```HeaderLogoPath        : 
C:\inetpub\wwwroot\Citrix\StoreWeb\receiver\images\2x\CitrixReceiverLogo_Home@2x_3FEDFD700D66DF42.png
LogonLogoPath         : 
C:\inetpub\wwwroot\Citrix\StoreWeb\receiver\images\2x\CitrixStoreFront_auth@2x_1B99A8ADCDDFD9AB.png
HeaderBackgroundColor : #574f5b
HeaderForegroundColor : #fff
LinkColor             : #02a1c1
```
