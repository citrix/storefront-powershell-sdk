# Get-STFServerGroup

Get the Server Group members

## Syntax

```
Get-STFServerGroup [<CommonParameters>]
```

## Detailed Description

Get the server members that a part of the StoreFront server group.

## Related Commands


## Input Type

### 



## Return Values

### ClusterManagement

The .NET `Citrix.StoreFront.Model.Cluster.ClusterManagement` reference type

## Examples

### EXAMPLE 1 Get Server Group

```
Get-STFServerGroup
```

**REMARKS**

Get the StoreFront server group configuration

**OUTPUT**

```
ClusterMembers                            ConfigurationFile                    
     TenantId                                
--------------                            -----------------                    
     --------                                
{ServerA, ServerB}                        C:\Program Files\Citrix\Receiver 
Store... 860e9401-39c8-4f2c-928d-34251102b840
```
