#Export-STFConfiguration
Exports a zip file containing configuration elements that form a Citrix StoreFront deployment. This zip file may be unencrypted in the form of a '.zip' file or encrypted in the form of a '.ctxzip'.
##Syntax
```Export-STFConfiguration -TargetFolder <String> -ZipFileName <String> [-Credential <PSCredential>] [-Force <SwitchParameter>] [-NoEncryption <SwitchParameter>] [<CommonParameters>]
```
##Detailed Description
Exports a zip file containing configuration elements that form a Citrix StoreFront deployment. This zip file may be unencrypted in the form of a '.zip' file or encrypted in the form of a '.ctxzip'.
##Related Commands
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||TargetFolder|The folder to export the backup archive to.|true|true (ByValue)||ZipFileName|The name of the backup archive WITHOUT its file extension.|true|true (ByValue)||Credential|Use this parameter if you wish to encrypt the exported configuration.  The backup archive will have the file extension .ctxzip.|false|false||Force|Use the force parameter to silently overwrite any previous backups with the same name as the one you are currently exporting.|false|false||NoEncryption|Use this parameter if you wish to export the configuration unencrypted.  The backup archive will have the file extension .zip.|false|true (ByValue)|##Input Type
###System.String
Parameter TargetFolder: The .NET 'System.String' reference type
###System.String
Parameter ZipFileName: The .NET 'System.String' reference type
###System.Management.Automation.PSCredential
Parameter Credential: The .NET 'System.Management.Automation.PSCredential' reference type
###System.Management.Automation.SwitchParameter
Parameter Force: The .NET 'System.Management.Automation.SwitchParameter' value type
###System.Management.Automation.SwitchParameter
Parameter NoEncryption: The .NET 'System.Management.Automation.SwitchParameter' value type
##Return Values
##Examples
###EXAMPLE 1 Basic Config Export
```Export-STFConfiguration -$targetFolder '$env:userprofile\desktop\' -zipFileName 'ConfigBackup' -NoEncryption
```
REMARKS

This example creates an unencrypted '.zip' file at '$env:userprofile\desktop\' called ConfigBackup.
###EXAMPLE 2 Encrypted Config Export
```Export-STFConfiguration -$targetFolder '$env:userprofile\desktop' -zipFileName 'ConfigBackup' -credential $CredObject
```
REMARKS

This example creates an encrypted .ctxzip file as above using a pre-defined PSCredential object.
Example PSCredential:
$User = Any non empty string will suffice here. The exported configuration is secured by only using the $Password.
$Password = 'Secret'
$Password = $Password | ConvertTo-SecureString -asPlainText -Force
$CredObject = New-Object System.Management.Automation.PSCredential($User,$Password)
Create a PowerShell credential object containing a username and password for symmetric encryption and decryption of
configuration backup archives. PowerShell credential objects store passwords as secure strings in memory.
The user is irrelevant but mandatory to create a PowerShell credential object. The example code uses the currently
logged in user.
The password is used for symmetric encryption/decryption of the backup archive. NOTE: The password DOES NOT need to
match the user's password to create a valid credential object.
