#Set-STFWebReceiverFeaturedAppGroup
Sets the Featured App group within the specified WebReceiver.
##Syntax
```Set-STFWebReceiverFeaturedAppGroup [-WebReceiverService] <WebReceiverService> [-FeaturedAppGroup] <FeaturedAppGroup> [[-Description] <String>] [[-TileId] <String>] [[-ContentType] <Keyword | Category | AppName>] [[-Contents] <String[]>] [<CommonParameters>]
```
##Detailed Description
Sets the properties of an existing Featured App group within the specified WebReceiver.
The existing Featured App group is identified by its Title property.
##Related Commands
*[New-STFWebReceiverFeaturedAppGroup](New-STFWebReceiverFeaturedAppGroup)
*[Add-STFWebReceiverFeaturedAppGroup](Add-STFWebReceiverFeaturedAppGroup)
*[Remove-STFWebReceiverFeaturedAppGroup](Remove-STFWebReceiverFeaturedAppGroup)
*[Clear-STFWebReceiverFeaturedAppGroup](Clear-STFWebReceiverFeaturedAppGroup)
*[Set-STFWebReceiverFeaturedAppGroups](Set-STFWebReceiverFeaturedAppGroups)
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||WebReceiverService|WebReceiver service to set the Featured Application group on|true|true (ByValue)||FeaturedAppGroup|The Featured Application groups to set|true|false||Description|This is an optional parameter and the text is displayed as the Featured App group description text.|false|false||TileId|This is the unique identifier for the background style of the Featured App group. The permissible values are: 'appBundle1', 'appBundle2', 'appBundle3', 'appBundle4', 'appBundle5', 'appBundle6', 'appBundle7' or 'appBundle8'.|false|false||ContentType|This parameter defines the type of Contents provided in the Contents parameter. The permissible values are: 'Keyword', 'Category' or 'AppName'.|false|false|The permissible values for this is based on the ContentType parameter:
1. Keyword: The list must have only 1 value. All the Apps which have keywords matching with the value in the list will appear as a Featured App group.
2. Category: The list must have only 1 value. All the Apps which have category defined as the value in the list will appear as a Featured App group.
3. AppName: The list must have 1 or more unique values. All the Apps which have names (for users) which partially or fully matches any of the values in this list will appear as a Featured App group.
|Contents|The parameter defines the content for the Featured App group.|false|false|##Input Type
###Citrix.StoreFront.Model.ReceiverForWeb.WebReceiverService
Parameter WebReceiverService: A .NET class representing the configuration of a StoreFront Web Receiver service
###Citrix.StoreFront.Model.ReceiverForWeb.FeaturedAppGroup
Parameter FeaturedAppGroup: The .NET 'Citrix.StoreFront.Model.ReceiverForWeb.FeaturedAppGroup' reference type
###System.String
Parameter Description: The .NET 'System.String' reference type
###System.String
Parameter TileId: The .NET 'System.String' reference type
###Citrix.StoreFront.Model.ReceiverForWeb.FeaturedAppContentType
Parameter ContentType: The .NET 'Citrix.StoreFront.Model.ReceiverForWeb.FeaturedAppContentType' value type
###System.String[]
Parameter Contents: The .NET 'System.String' reference type
##Return Values
##Examples
###EXAMPLE 1 Set the Feature Application group
```$webReceiver = Get-STFWebReceiverService
$group = New-STFWebReceiverFeaturedAppGroup -Title "Worx Suite" `
-Description "Improve productivity with a suite of secure mobile apps made for business." `
-TileId appBundle1 `
-ContentType Keyword `
-Contents Worx
Set-STFWebReceiverFeaturedAppGroups -WebReceiverService $webReceiver -FeaturedAppGroup $group
Set-STFWebReceiverFeaturedAppGroup -WebReceiverService $webReceiver -FeaturedAppGroup $group `
-ContentType AppName `
-Contents @("Worx Home", "Worx Mail")
```
REMARKS

Sets the Featured Application group for the Worx Suite to now specify the contents by app name instead of keyword.
