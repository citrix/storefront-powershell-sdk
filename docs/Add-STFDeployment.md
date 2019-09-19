# Add-STFDeployment

Create a new StoreFront deployment

## Syntax

```
Add-STFDeployment [[-SiteId] <Int64>] [[-HostBaseUrl] <String>] [<CommonParameters>]
```

## Detailed Description

Creates a new StoreFront deployment with the required features installed and configured.

## Related Commands


## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|SiteId|The IIS site id of the deployment|false|false| |
|HostBaseUrl|Url used to access the StoreFront server group|false|false| |

## Input Type

### System.Int64

Parameter SiteId: The .NET `System.Int64` value type

### System.String

Parameter HostBaseUrl: The .NET `System.String` reference type

## Return Values

### StoreFrontDeployment

The .NET `Citrix.StoreFront.Model.StoreFrontDeployment` reference type

## Examples

### EXAMPLE 1 Create a new deployment

```
Add-STFDeployment https://example.storefront.com -Confirm:$false
```

**REMARKS**

Creates a new StoreFront server that will be accessed by Receivers using the 

url https://example.storefront.com.

**OUTPUT**

```
HostbaseUrl             : https://example.storefront.com/
IISSiteId               : 1
DeploymentExists        : True
InstalledFeatureClasses : {WebApplication, WING, XmlServiceAuthentication, 
ResourcesCommon...}
FeatureClassInstances   : {82545fc5-2809-4d69-941f-21163d8bca30, 
a56e0a1b-661b-4cd9-8802-89e34c0e989f,
                          ad5777f8-573c-4b1c-b608-32e16068f80b, 
1406c90b-095f-4ea4-9b24-ec3ccc590cc1...}
```
