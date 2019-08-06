# Uninstall-STFFeature

Un-install a StoreFront Feature

## Syntax

```
Uninstall-STFFeature [-PackageName] <String> [<CommonParameters>]
```

## Detailed Description

Un-install a StoreFront feature that is not installed by default as part of a new deployment or when joining an existing server group.

## Related Commands

* [Install-STFFeature](Install-STFFeature.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|PackageName|Name of the feature to uninstall. The name of the feature is usually the same as the package|true|true (ByValue)| |

## Input Type

### System.String

Parameter PackageName: The .NET `System.String` reference type

## Return Values

### None

## Examples

### EXAMPLE 1 Uninstall a custom feature

```
Uninstall-STFFeature -PackageName CustomAuthentication
```

**REMARKS**

Uninstalls the feature named 'CustomAuthentication'.
