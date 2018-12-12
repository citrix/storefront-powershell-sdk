# Set-STFFeatureState

Sets a FeatureState Object

## Syntax

```
Set-STFFeatureState [-FeatureStates] <FeatureState[]> [<CommonParameters>]
```

## Detailed Description

Sets a FeatureState Object

## Related Commands

* [Add-STFFeatureState](./Add-STFFeatureState)
* [Get-STFFeatureState](./Get-STFFeatureState)
* [Get-STFFeatureStateNames](./Get-STFFeatureStateNames)
* [New-STFFeatureState](./New-STFFeatureState)
* [New-STFFeatureStateProperty](./New-STFFeatureStateProperty)
* [Remove-STFFeatureState](./Remove-STFFeatureState)
* [Reset-STFFeatureData](./Reset-STFFeatureData)
* [Clear-STFFeatureStates](./Clear-STFFeatureStates)

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
