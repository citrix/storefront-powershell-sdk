# Set-STFFeatureState

Sets a FeatureState Object

## Syntax

```
Set-STFFeatureState [-FeatureStates] <FeatureState[]> [<CommonParameters>]
```

## Detailed Description

Sets a FeatureState Object

## Related Commands

* [Add-STFFeatureState](Add-STFFeatureState.md)
* [Get-STFFeatureState](Get-STFFeatureState.md)
* [Get-STFFeatureStateNames](Get-STFFeatureStateNames.md)
* [New-STFFeatureState](New-STFFeatureState.md)
* [New-STFFeatureStateProperty](New-STFFeatureStateProperty.md)
* [Remove-STFFeatureState](Remove-STFFeatureState.md)
* [Reset-STFFeatureData](Reset-STFFeatureData.md)
* [Clear-STFFeatureStates](Clear-STFFeatureStates.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|FeatureStates|A list of FeatureState objects|true|false| |

## Input Type

### Citrix.DeliveryServices.Framework.FeatureToggle.FeatureState[]

Parameter FeatureStates: The .NET `Citrix.DeliveryServices.Framework.FeatureToggle.FeatureState` reference type

## Return Values

### None

## Examples

### EXAMPLE 1 Set FeatureState

```
Set-STFFeatureState -FeatureStates @(featureStateObj1,featureStateObj2)
```

**REMARKS**

Saves two FeatureState objects
