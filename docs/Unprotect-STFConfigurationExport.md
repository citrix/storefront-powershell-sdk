# Unprotect-STFConfigurationExport

Creates a decrypted copy of the supplied ctxzip file containing configuration elements that form a Citrix StoreFront deployment using the supplied PSCredential.

## Syntax

```
Unprotect-STFConfigurationExport -EncryptedConfigurationZip <String> -Credential <PSCredential> -OutputFolder <String> [<CommonParameters>]
```

## Detailed Description

Creates a decrypted copy of the supplied ctxzip file containing configuration elements that form a Citrix StoreFront deployment using the supplied PSCredential.

## Related Commands


## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|EncryptedConfigurationZip|The path to the backup archive WITH its correct file extension .ctxzip|true|true (ByValue)| |
|Credential|A predefined PowerShell credential object containing the same password that was used to export the backup archive.|true|false| |
|OutputFolder|The folder that the resultant decrypted configuration zip file should be saved to.|true|false| |

## Input Type

### System.String

Parameter EncryptedConfigurationZip: The .NET `System.String` reference type

### System.Management.Automation.PSCredential

Parameter Credential: The .NET `System.Management.Automation.PSCredential` reference type

### System.String

Parameter OutputFolder: The .NET `System.String` reference type

## Return Values

### None

## Examples

### EXAMPLE 1 Decrypt Config Export

```
Unprotect-STFConfigurationExport -encryptedConfigurationZip '$env:userprofile\desktop\ConfigBackup.ctxzip' -credential $CredObject -outputFolder 'C:\exampleFolder\exampleSubfolder' -Force
```

**REMARKS**

Using the password supplied in $CredObject this will decrypt and convert the 

ConfigBackup.ctxzip backup archive to an unencrypted .zip backup archive and 

save it to C:\exampleFolder\exampleSubfolder\ConfigBackup.zip overwriting any 

existing ConfigBackup.zip files that may exist at that location.

Example PSCredential:

$User = Any non empty string will suffice here. The exported configuration is 

secured by only using the $Password.

$Password = 'Secret'

$Password = $Password | ConvertTo-SecureString -asPlainText -Force

$CredObject = New-Object 

System.Management.Automation.PSCredential($User,$Password)

Create a PowerShell credential object containing a username and password for 

symmetric encryption and decryption of configuration backup archives. 

PowerShell credential objects store passwords as secure strings in memory.

The user is irrelevant but mandatory to create a PowerShell credential object. 

The example code uses the currently logged in user.

The password is used for symmetric encryption/decryption of the backup 

archive. NOTE: The password DOES NOT need to match the user's password to 

create a valid credential object.
