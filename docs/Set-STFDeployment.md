#Set-STFDeployment
Update the existing deployment
##Syntax
```Set-STFDeployment [-HostBaseUrl] <String> [[-SiteId] <Int64>] [<CommonParameters>]
```
##Detailed Description
Update existing deployment settings including the host base url.
##Related Commands
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||HostBaseUrl|The host base url|true|true (ByValue)||SiteId|The IIS site id of the deployment|false|false|##Input Type
###System.String
Parameter HostBaseUrl: The .NET 'System.String' reference type
###System.Int64
Parameter SiteId: The .NET 'System.Int64' value type
##Return Values
###StoreFrontDeployment
The .NET 'Citrix.StoreFront.Model.StoreFrontDeployment' reference type
##Examples
###EXAMPLE 1 Update the host base url
```Set-STFDeployment -HostBaseUrl http://new.storefront.com
```
REMARKS

Change the host base url of the exsiting deployment to new.storefront.com.
