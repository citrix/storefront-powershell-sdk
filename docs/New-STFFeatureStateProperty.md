# New-STFFeatureStateProperty

Creates and returns a new FeatureStateProperty object

## Syntax

```
New-STFFeatureStateProperty [-Properties] <Hashtable> [<CommonParameters>]
```

## Detailed Description

Creates and returns a new FeatureStateProperty object

## Related Commands

* [Add-STFFeatureState](Add-STFFeatureState.md)
* [Get-STFFeatureState](Get-STFFeatureState.md)
* [Get-STFFeatureStateNames](Get-STFFeatureStateNames.md)
* [New-STFFeatureState](New-STFFeatureState.md)
* [Remove-STFFeatureState](Remove-STFFeatureState.md)
* [Clear-STFFeatureStates](Clear-STFFeatureStates.md)
* [Reset-STFFeatureData](Reset-STFFeatureData.md)
* [Set-STFFeatureState](Set-STFFeatureState.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|Properties|A list of key value pairs|true|false| |

## Input Type

### System.Collections.Hashtable

Parameter Properties: The .NET `System.Collections.Hashtable` reference type

## Return Values

### FeatureStateProperty

The .NET `Citrix.DeliveryServices.Framework.FeatureToggle.FeatureStateProperty` reference type

## Examples

### EXAMPLE 1 Creates a new FeatureStateProperty object

```
New-STFFeatureStateProperty -Properties @{'Property1' = 'Property1Value';'Property2' = 'Property2Value'}
```

**REMARKS**

Creates a new FeatureStateProperty object

**OUTPUT**

```
Name                       Value              
----                       ------               
Property1                  Property1Value       
Property2                  Property2Value
```
