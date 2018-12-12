# Get-STFPackage

Get the details of the Storefront packages on the system

## Syntax

```
Get-STFPackage [<CommonParameters>]
```

## Detailed Description

Get the details of the Storefront packages on the system. This includes, the package location, exposed properties and Feature class details.

## Related Commands


## Input Type

### 



## Return Values

### PackageInfo

The .NET `Citrix.DeliveryServices.Framework.Install.ZipPackage.PackageInfo` reference type

## Examples

### EXAMPLE 1 Get all feature packages

```
Get-STFPackage
```

**REMARKS**

Get all on disk feature packages.

**OUTPUT**

```
Identifier       : f604acd2-dba2-4ea9-9f30-b12a5fdfad32
FileLocation     : AGDiscover.zip
Title            : AGDiscover
Version          : 3.5.0.0
FeatureClass     : Citrix.DeliveryServices.Framework.Feature.FeatureClass
ParentIdentifier : 1a6f66d6-1128-4c79-ad96-a7a0589f2d58
Dependencies     : {}
Properties       : {[parent, 1a6f66d6-1128-4c79-ad96-a7a0589f2d58]}

Identifier       : 3722c484-d4a6-4bc1-84a6-270d74f9704a
FileLocation     : AnonymousStore.zip
Title            : AnonymousStore
Version          : 3.5.0.0
FeatureClass     : Citrix.DeliveryServices.Framework.Feature.FeatureClass
ParentIdentifier : 5af80ac4-488f-43bb-a162-3cfef90ea5ff
Dependencies     : {}
Properties       : {[parent, 5af80ac4-488f-43bb-a162-3cfef90ea5ff]}
...
```
