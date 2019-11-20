# Get-STFFeatureState

Gets the registered FeatureState object

## Syntax

```
Get-STFFeatureState [[-Name] <String>] [<CommonParameters>]
```

## Detailed Description

Gets the registered FeatureState object

## Related Commands

* [Add-STFFeatureState](./Add-STFFeatureState)
* [Get-STFFeatureStateNames](./Get-STFFeatureStateNames)
* [New-STFFeatureState](./New-STFFeatureState)
* [New-STFFeatureStateProperty](./New-STFFeatureStateProperty)
* [Remove-STFFeatureState](./Remove-STFFeatureState)
* [Clear-STFFeatureStates](./Clear-STFFeatureStates)
* [Reset-STFFeatureData](./Reset-STFFeatureData)
* [Set-STFFeatureState](./Set-STFFeatureState)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|Name|The unique identifier of the FeatureState object.|false|false| |

## Input Type

### System.String

Parameter Name: The .NET `System.String` reference type

## Return Values

### FeatureState

The .NET `Citrix.DeliveryServices.Framework.FeatureToggle.FeatureState` reference type

## Examples

### EXAMPLE 1 Get FeatureState object

```
Get-STFFeatureState -name feature1
```

**REMARKS**

Gets FeatureState object identified by feature1

**OUTPUT**

```
Name                       IsEnabled Properties                       
----                       --------- ----------                        
Feature1                    True      {Property1, Property2}
```

### EXAMPLE 2 Get FeatureState objects

```
Get-STFFeatureState
```

**REMARKS**

Gets a list of registred FeatureState objects

**OUTPUT**

```
Name                       IsEnabled Properties                       
----                       --------- ----------                        
Feature1                    True      {Property1, Property2}              
Feature2                    True      {}
```
