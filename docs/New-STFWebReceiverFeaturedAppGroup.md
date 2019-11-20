#New-STFWebReceiverFeaturedAppGroup
Creates a new Featured App group
##Syntax
```New-STFWebReceiverFeaturedAppGroup [-Title] <String> [[-Description] <String>] [-TileId] <String> [-ContentType] <Keyword | Category | AppName> [-Contents] <String[]> [<CommonParameters>]
```
##Detailed Description
The cmdlet gets a new Featured App group containing the data specified in the parameters.
##Related Commands
*[Clear-STFWebReceiverFeaturedAppGroup](Clear-STFWebReceiverFeaturedAppGroup)
*[Get-STFWebReceiverFeaturedAppGroup](Get-STFWebReceiverFeaturedAppGroup)
*[Remove-STFWebReceiverFeaturedAppGroup](Remove-STFWebReceiverFeaturedAppGroup)
*[Set-STFWebReceiverFeaturedAppGroup](Set-STFWebReceiverFeaturedAppGroup)
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||Title|This text is displayed as the App group header text. This text should be unique across the Featured App groups|true|true (ByValue)||Description|This is an optional parameter and the text is displayed as the Featured App group description text.|false|false||TileId|This is the unique identifier for the background style of the Featured App group. The permissible values are: 'appBundle1', 'appBundle2', 'appBundle3', 'appBundle4', 'appBundle5', 'appBundle6', 'appBundle7' or 'appBundle8'.|true|false||ContentType|This parameter defines the type of Contents provided in the Contents parameter. The permissible values are: 'Keyword', 'Category' or 'AppName'.|true|false|The permissible values for this is based on the ContentType parameter:
1. Keyword: The list must have only 1 value. All the Apps which have keywords matching with the value in the list will appear as a Featured App group.
2. Category: The list must have only 1 value. All the Apps which have category defined as the value in the list will appear as a Featured App group.
3. AppName: The list must have 1 or more unique values. All the Apps which have names (for users) which partially or fully matches any of the values in this list will appear as a Featured App group.
|Contents|The parameter defines the content for the Featured App group.|true|false|##Input Type
###System.String
Parameter Title: The .NET 'System.String' reference type
###System.String
Parameter Description: The .NET 'System.String' reference type
###System.String
Parameter TileId: The .NET 'System.String' reference type
###Citrix.StoreFront.Model.ReceiverForWeb.FeaturedAppContentType
Parameter ContentType: The .NET 'Citrix.StoreFront.Model.ReceiverForWeb.FeaturedAppContentType' value type
###System.String[]
Parameter Contents: The .NET 'System.String' reference type
##Return Values
###FeaturedAppGroup
The .NET 'Citrix.StoreFront.Model.ReceiverForWeb.FeaturedAppGroup' reference type
##Examples
###EXAMPLE 1 Create a new FeaturedAppGroup
```$group = New-STFWebReceiverFeaturedAppGroup -Title "Worx Suite" `
-Description "Improve productivity with a suite of secure mobile apps made for business." `
-TileId appBundle1 `
-ContentType Keyword `
-Contents Worx
```
