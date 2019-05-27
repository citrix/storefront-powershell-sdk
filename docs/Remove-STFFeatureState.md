# Remove-STFFeatureState

Removes the FeatureState object

## Syntax

```
Remove-STFFeatureState [-Name] <String> [<CommonParameters>]
```

## Detailed Description

Removes the FeatureState object

## Related Commands

* [Add-STFFeatureState](Add-STFFeatureState.md)
* [Get-STFFeatureState](Get-STFFeatureState.md)
* [Get-STFFeatureStateNames](Get-STFFeatureStateNames.md)
* [New-STFFeatureState](New-STFFeatureState.md)
* [New-STFFeatureStateProperty](New-STFFeatureStateProperty.md)
* [Clear-STFFeatureStates](Clear-STFFeatureStates.md)
* [Reset-STFFeatureData](Reset-STFFeatureData.md)
* [Set-STFFeatureState](Set-STFFeatureState.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|Name|The unique identifier of the FeatureState|true|false| |

## Input Type

### System.String

Parameter Name: The .NET `System.String` reference type

## Return Values

### None

## Examples

### EXAMPLE 1 Removes the FeatureState object

```
Remove-STFFeatureState -Name feature1
```

**REMARKS**

Removes the FeatureState object registered as feature1
