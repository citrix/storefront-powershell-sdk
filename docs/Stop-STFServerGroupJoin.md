# Stop-STFServerGroupJoin

Stop the server join process

## Syntax

```
Stop-STFServerGroupJoin [<CommonParameters>]
```

## Detailed Description

Terminates the server join process. The join process will be stopped if a join is not currently in progress.

## Related Commands

* [Start-STFServerGroupJoin](Start-STFServerGroupJoin.md)
* [Remove-STFServerGroupMember](Remove-STFServerGroupMember.md)
* [Wait-STFServerGroupJoin](Wait-STFServerGroupJoin.md)

## Input Type

### 



## Return Values

### None

## Examples

### EXAMPLE 1 Stop a Server Group Join

```
Stop-STFServerGroupJoin
```

**REMARKS**

Stopping an in progress join may result in corrupted configuration on the 

joining server.
