# New-STFFeatureStateProperty

Creates and returns a new FeatureStateProperty object

## Syntax

```
New-STFFeatureStateProperty [-Properties] <Hashtable> [<CommonParameters>]
```

## Detailed Description

Creates and returns a new FeatureStateProperty object

## Related Commands

* [Add-STFFeatureState](./Add-STFFeatureState)
* [Get-STFFeatureState](./Get-STFFeatureState)
* [Get-STFFeatureStateNames](./Get-STFFeatureStateNames)
* [New-STFFeatureState](./New-STFFeatureState)
* [Remove-STFFeatureState](./Remove-STFFeatureState)
* [Clear-STFFeatureStates](./Clear-STFFeatureStates)
* [Reset-STFFeatureData](./Reset-STFFeatureData)
* [Set-STFFeatureState](./Set-STFFeatureState)

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
