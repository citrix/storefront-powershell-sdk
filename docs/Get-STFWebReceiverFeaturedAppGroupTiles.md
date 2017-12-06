#Get-STFWebReceiverFeaturedAppGroupTiles
Gets the background styles and the associated background image path for Featured App groups
##Syntax
```Get-STFWebReceiverFeaturedAppGroupTiles [-WebReceiverService] <WebReceiverService> [<CommonParameters>]
```
##Detailed Description
The style information is retrieved from the css file of Receiver for Web.
##Related Commands
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||WebReceiverService|WebReceiver to get the featured application group tiles for|true|true (ByValue)|##Input Type
###Citrix.StoreFront.Model.ReceiverForWeb.WebReceiverService
Parameter WebReceiverService: A .NET class representing the configuration of a StoreFront Web Receiver service
##Return Values
###FeaturedAppGroupTile
The .NET 'Citrix.StoreFront.Model.ReceiverForWeb.FeaturedAppGroupTile' reference type
##Examples
###EXAMPLE 1 Get FeaturedAppGroup tiles
```$webReceiver = Get-STFWebReceiverService
Get-STFWebReceiverFeaturedAppGroupTiles
```
REMARKS

Get the FeaturedAppGroup tiles.
OUTPUT
```TileId                                                         BackgroundImage                                         
     
------                                                         ---------------                                         
     
appBundle1                                                     
C:\inetpub\wwwroot\Citrix\StoreWeb\receiver\images\1x\bund...
appBundle2                                                     
C:\inetpub\wwwroot\Citrix\StoreWeb\receiver\images\1x\bund...
appBundle3                                                     
C:\inetpub\wwwroot\Citrix\StoreWeb\receiver\images\1x\bund...
appBundle4                                                     
C:\inetpub\wwwroot\Citrix\StoreWeb\receiver\images\1x\bund...
appBundle5                                                     
C:\inetpub\wwwroot\Citrix\StoreWeb\receiver\images\1x\bund...
appBundle6                                                     
C:\inetpub\wwwroot\Citrix\StoreWeb\receiver\images\1x\bund...
appBundle7                                                     
C:\inetpub\wwwroot\Citrix\StoreWeb\receiver\images\1x\bund...
appBundle8                                                     
C:\inetpub\wwwroot\Citrix\StoreWeb\receiver\images\1x\bund...
appBundle9                                                     
C:\inetpub\wwwroot\Citrix\StoreWeb\receiver\images\1x\bund...
```
