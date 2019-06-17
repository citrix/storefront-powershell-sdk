# Citrix.StoreFront.Authentication

## Topic

`about_Citrix.StoreFront.Authentication`

## Short Description

The Citrix.StoreFront.Authentication PowerShell module provides administrative functions for the Authentication Services. 

## Command Prefix

All commands in this module have 'STF' in their name to denote they are part of the StoreFront product. 

## Long Description

The Citrix.StoreFront.Authentication PowerShell module enables local administration of StoreFront Authentication Services. It provides facilities to add, remove and configure authentication methods. Examples of usage can be found in `<InstallPath>\PowerShellSDK\Examples`. 

The module provides the following main entities: 

- **AuthenticationService**: The authentication service authenticates users to Microsoft Active Directory or XenApp and XenDesktop farms, ensuring that users do not need to log on again to access their desktops and applications. 

## Cmdlets

- [Get-STFAuthenticationProtocolsAvailable](Get-STFAuthenticationProtocolsAvailable.md)
- [Add-STFAuthenticationService](Add-STFAuthenticationService.md)
- [Get-STFAuthenticationService](Get-STFAuthenticationService.md)
- [Remove-STFAuthenticationService](Remove-STFAuthenticationService.md)
- [Add-STFAuthenticationServiceProtocol](Add-STFAuthenticationServiceProtocol.md)
- [Remove-STFAuthenticationServiceProtocol](Remove-STFAuthenticationServiceProtocol.md)
- [Get-STFAuthenticationServiceProtocol](Get-STFAuthenticationServiceProtocol.md)
- [Enable-STFAuthenticationServiceProtocol](Enable-STFAuthenticationServiceProtocol.md)
- [Disable-STFAuthenticationServiceProtocol](Disable-STFAuthenticationServiceProtocol.md)
- [Set-STFClaimsFactoryNames](Set-STFClaimsFactoryNames.md)