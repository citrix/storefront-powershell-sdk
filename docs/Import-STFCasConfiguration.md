# Import-STFCasConfiguration

Imports a CAS .JSON configuration file to register your Stores with the Citrix Cloud Analytics Service

## Syntax

```
Import-STFCasConfiguration [-Path] <String> [[-RoamingService] <RoamingService>] [<CommonParameters>]
```

## Detailed Description

Imports a CAS .JSON configuration file downloaded from Citrix Cloud.


The CAS configuration file contains data that registers your Stores with the Citrix Cloud Analytics Service (CAS).


The CAS data is added to the roaming web.config file and is shared by all Stores in your deployment.

## Related Commands


## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|Path|CAS configuration file path.|true|true (ByValue)| |
|RoamingService|The Roaming service|false|false| |

## Input Type

### System.String

Parameter Path: The .NET `System.String` reference type

### Citrix.StoreFront.Model.Roaming.RoamingService

Parameter RoamingService: A .NET class representing the configuration of a StoreFront Roaming service

## Return Values

### None

## Examples

### EXAMPLE 1 Import CAS data

```
Import-STFCasConfiguration -path C:\User\administrator\Desktop\StoreFrontConfigurationFile.json
```

**REMARKS**

Import a CAS configuration file downloaded from Citrix Cloud.

### EXAMPLE 2 Overwrite existing CAS data

```
Import-STFCasConfiguration -path C:\User\administrator\Desktop\StoreFrontConfigurationFile.json
```

**REMARKS**

Overwrite existing CAS configuration data with a different JSON file 

downloaded from Citrix Cloud.
