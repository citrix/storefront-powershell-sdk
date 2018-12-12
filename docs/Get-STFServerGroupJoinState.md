# Get-STFServerGroupJoinState

Get the current server join state

## Syntax

```
Get-STFServerGroupJoinState [<CommonParameters>]
```

## Detailed Description

Gets the current state of the server group join. Can be used on either the existing group member or the joining server to determine the current status.

## Related Commands


## Input Type

### 



## Return Values

### None

## Examples

### EXAMPLE 1 Get the Join State

```
Get-STFServerGroupJoinState
```

**REMARKS**

Get the server join state while waiting for the joining server.

**OUTPUT**

```
RemoteServer                                                                 Status StatusMessage                           
------------                                                                 ------ -------------                           
                                                                               Idle Idle
```
