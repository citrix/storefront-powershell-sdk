# Install-STFFeature

Install a StoreFront feature

## Syntax

```
Install-STFFeature [-FileLocation] <String[]> [[-PassThru] <SwitchParameter>] [<CommonParameters>]



Install-STFFeature [-PackageName] <String[]> [[-PassThru] <SwitchParameter>] [<CommonParameters>]
```

## Detailed Description

Install a StoreFront feature that is not installed by default as part of a new deployment or when joining an existing server group.

## Related Commands

* [Uninstall-STFFeature](./Uninstall-STFFeature)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|FileLocation|Path of the feature packages to install. StoreFront feature packages are compressed archives containing all the files and data required for a single feature.|true|true (ByValue)| |
|PackageName|The name of the packages to install from the default StoreFront <install folder>\FeaturePackages.|true|false| |
|PassThru|Output the installed feature class.|false|false| |

## Input Type

### System.String[]

Parameter FileLocation: The .NET `System.String` reference type

### System.String[]

Parameter PackageName: The .NET `System.String` reference type

### System.Management.Automation.SwitchParameter

Parameter PassThru: The .NET `System.Management.Automation.SwitchParameter` value type

## Return Values

### None

## Examples

### EXAMPLE 1 Install a custom feature

```
Install-STFFeature -FileLocation C:\Files\CustomAuthentication.zip
```

**REMARKS**

Installs a custom feature named CustomAuthentication.zip.
