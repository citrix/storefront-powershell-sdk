# Set-STFDiagnostics

Configure StoreFront diagnostics

## Syntax

```
Set-STFDiagnostics [-Service] <IConfigBasedFeature> [-TraceLevel] <Off | Error | Warning | Info | Verbose> [-FileSizeKb <Int32>] [-FileCount <Int32>] [<CommonParameters>]



Set-STFDiagnostics [-All] <SwitchParameter> [-TraceLevel] <Off | Error | Warning | Info | Verbose> [-FileSizeKb <Int32>] [-FileCount <Int32>] [<CommonParameters>]



Set-STFDiagnostics [-AllUserFacingServices] <SwitchParameter> [-TraceLevel] <Off | Error | Warning | Info | Verbose> [-FileSizeKb <Int32>] [-FileCount <Int32>] [<CommonParameters>]



Set-STFDiagnostics [-ConfigFile] <String> [-TraceLevel] <Off | Error | Warning | Info | Verbose> [-FileSizeKb <Int32>] [-FileCount <Int32>] [<CommonParameters>]
```

## Detailed Description

Configure StoreFront service tracing and logging.

## Related Commands


## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|Service|The StoreFront service for which tracing should be updated. For example: StoreService, AuthenticationService, WebReceiver.|true|true (ByValue)| |
|All|A flag indicating that tracing should be updated for all instances and services.|true|false| |
|AllUserFacingServices|A flag indicating that tracing should be updated for all instances and services except the credential Wallet.|true|false| |
|ConfigFile|A specific configuration file for which tracing should be updated.|true|true (ByValue)| |
|TraceLevel|The trace level to set.|true|false| |
|FileSizeKb|The trace file size in KB.|false|false| |
|FileCount|The number of trace files to maintain.|false|false| |

## Input Type

### Citrix.StoreFrontConfiguration.Interfaces.IConfigBasedFeature

Parameter Service: The .NET `Citrix.StoreFrontConfiguration.Interfaces.IConfigBasedFeature` reference type

### System.Management.Automation.SwitchParameter

Parameter All: The .NET `System.Management.Automation.SwitchParameter` value type

### System.Management.Automation.SwitchParameter

Parameter AllUserFacingServices: The .NET `System.Management.Automation.SwitchParameter` value type

### System.String

Parameter ConfigFile: The .NET `System.String` reference type

### System.Diagnostics.TraceLevel

Parameter TraceLevel: The .NET `System.Diagnostics.TraceLevel` value type

### System.Int32

Parameter FileSizeKb: The .NET `System.Int32` value type

### System.Int32

Parameter FileCount: The .NET `System.Int32` value type

## Return Values

### None

## Examples

### EXAMPLE 1 Enable all tracing

```
Set-STFDiagnostics -All 'Verbose'
```

**REMARKS**

Configures all StoreFront services to perform verbose level tracing useful for 

identifying configuration issues.

### EXAMPLE 2 Enable tracing on the Store

```
$store = Get-STFStoreService /Citrix/Store
Set-STFDiagnostics -Service $store -TraceLevel Verbose
```

**REMARKS**

Configures the Store service at /Citrix/Store to perform verbose level tracing 

useful for identifying configuration issues.
