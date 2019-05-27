# Get-STFDeployment

Get details of an existing deployment

## Syntax

```
Get-STFDeployment [[-SiteId] <Int64>] [<CommonParameters>]
```

## Detailed Description

Get details of the StoreFront deployment on the current server.

## Related Commands

* [Add-STFDeployment](Add-STFDeployment.md)
* [Clear-STFDeployment](Clear-STFDeployment.md)
* [Set-STFDeployment](Set-STFDeployment.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|SiteId|The IIS site id of the deployment|false|false| |

## Input Type

### System.Int64

Parameter SiteId: The .NET `System.Int64` value type

## Return Values

### StoreFrontDeployment[]

The .NET `Citrix.StoreFront.Model.StoreFrontDeployment` reference type

## Examples

### EXAMPLE 1 Get the StoreFront deployment

```
Get-STFDeployment
```

**REMARKS**

Get the StoreFront deployment details

**OUTPUT**

```
HostbaseUrl             : http://example.storefront.com
IISSiteId               : 1
DeploymentExists        : True
InstalledFeatureClasses : {WebApplication, WING, XmlServiceAuthentication, 
ResourcesCommon...}
FeatureClassInstances   : {82545fc5-2809-4d69-941f-21163d8bca30, 
a56e0a1b-661b-4cd9-8802-89e34c0e989f,
                          64058d2a-15d7-4b0e-943b-ab05b7bb5cc3, 
0b771665-9eb0-453f-a9bc-70df7db6f847...}
```
