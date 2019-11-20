# Clear-STFDeployment

Clear the existing deployment

## Syntax

```
Clear-STFDeployment [[-SiteId] <Int64>] [<CommonParameters>]
```

## Detailed Description

Removes the deployed StoreFront configuration from the server.

## Related Commands

* [Add-STFDeployment](./Add-STFDeployment)
* [Get-STFDeployment](./Get-STFDeployment)
* [Set-STFDeployment](./Set-STFDeployment)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|SiteId|The IIS site id of the deployment to remove|false|false| |

## Input Type

### System.Int64

Parameter SiteId: The .NET `System.Int64` value type

## Return Values

### None

## Examples

### EXAMPLE 1 Clear All Configuration

```
Clear-STFDeployment
```

**REMARKS**

Removes all configured StoreFront features from the server
