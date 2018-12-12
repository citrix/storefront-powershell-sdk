# Get-STFInstalledFeatures

Get the details of the Storefront features on the system

## Syntax

```
Get-STFInstalledFeatures [<CommonParameters>]
```

## Detailed Description

Get the details of the Storefront features on the system.

## Related Commands


## Input Type

### 



## Return Values

### FeatureClass

The .NET `Citrix.DeliveryServices.Framework.Feature.FeatureClass` reference type

## Examples

### EXAMPLE 1 Get all features installed

```
Get-STFInstalledFeatures
```

**REMARKS**

Get all the features that are installed.

**OUTPUT**

```
Path                           : C:\Program Files\Citrix\Receiver StoreFront\ClusterManagement
ConfigLocation                 : C:\Program Files\Citrix\Receiver StoreFront\ClusterManagement\feature.config
ConfigTypeName                 : Executable
Id                             : 82545fc5-2809-4d69-941f-21163d8bca30
ClassType                      : 4a9f261e-db72-4980-a8ca-09e81927a766
FrameworkController            : Citrix.DeliveryServices.Framework.FileBased.FrameworkController
ParentInstance                 : 00000000-0000-0000-0000-000000000000
RootInstance                   : 82545fc5-2809-4d69-941f-21163d8bca30
TenantId                       : 860e9401-39c8-4f2c-928d-34251102b840
Data                           : {[DeployFolder, C:\Program Files\Citrix\Receiver StoreFront\ClusterManagement],
                                 [EventSource, ], [Name, ClusterManagement], [ConfigLocation, C:\Program
                                 Files\Citrix\Receiver StoreFront\ClusterManagement\feature.config]...}
ReadOnlyData                   : {[Name, ClusterManagement], [Cmdlet, Add-DSBasicFeature], [Snapin,
                                 Citrix.DeliveryServices.Framework.Commands], [Tenant,
                                 860e9401-39c8-4f2c-928d-34251102b840]}
ParameterData                  : {[Folder, C:\Program Files\Citrix\Receiver StoreFront\ClusterManagement],
                                 [RequiredInstanceId, 82545fc5-2809-4d69-941f-21163d8bca30], [FeatureClassId,
                                 4a9f261e-db72-4980-a8ca-09e81927a766]}
AdditionalInstanceDependencies : {}
IsDeployed                     : True
FeatureClass                   : Citrix.DeliveryServices.Framework.Feature.FeatureClass

Path                           : C:\Program Files\Citrix\Receiver StoreFront\Services\ConfigurationReplication
ConfigLocation                 : C:\Program Files\Citrix\Receiver StoreFront\Services\ConfigurationReplication\Citrix.D
                                 eliveryServices.ConfigurationReplicationService.ServiceHost.exe.config
ConfigTypeName                 : Executable
Id                             : a56e0a1b-661b-4cd9-8802-89e34c0e989f
ClassType                      : e6bb3590-d9bd-4e76-8d4d-a340a8635413
FrameworkController            : Citrix.DeliveryServices.Framework.FileBased.FrameworkController
ParentInstance                 : 00000000-0000-0000-0000-000000000000
RootInstance                   : a56e0a1b-661b-4cd9-8802-89e34c0e989f
TenantId                       : 860e9401-39c8-4f2c-928d-34251102b840
Data                           : {[DeployFolder, C:\Program Files\Citrix\Receiver
                                 StoreFront\Services\ConfigurationReplication], [EventSource, ], [StartService, True],
                                 [WindowsServiceName, CitrixConfigurationReplication]...}
ReadOnlyData                   : {[WindowsServiceName, CitrixConfigurationReplication], [Name,
                                 ConfigurationReplication], [Cmdlet, Add-DSConfigurationReplication], [Snapin,
                                 Citrix.DeliveryServices.ConfigurationReplication.Commands]...}
ParameterData                  : {[Folder, C:\Program Files\Citrix\Receiver
                                 StoreFront\Services\ConfigurationReplication], [StartService, ]}
AdditionalInstanceDependencies : {}
IsDeployed                     : True
FeatureClass                   : Citrix.DeliveryServices.Framework.Feature.FeatureClass
...
```
