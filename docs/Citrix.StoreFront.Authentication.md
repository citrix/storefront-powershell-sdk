#Citrix.StoreFront.Authentication

##Topic

about_Citrix.StoreFront.Authentication
##Short Description

The Citrix.StoreFront.Authentication PowerShell module provides administrative functions for the Authentication Services.

##COMMAND PREFIX

All commands in this module have 'STF' in their name to denote they are part of the StoreFront product.
##Long Description
The Citrix.StoreFront.Authentication PowerShell module enables local administration of StoreFront Authentication Services. It provides facilities to add, remove and configure authentication methods. Examples of usage can be found in <InstallPath>\PowerShellSDK\Examples. 

The module provides the following main entities: 

* **AuthenticationService**: The authentication service authenticates users to Microsoft Active Directory or XenApp and XenDesktop farms, ensuring that users do not need to log on again to access their desktops and applications.
##Cmdlets

* [Get-STFAuthenticationProtocolsAvailable](Get-STFAuthenticationProtocolsAvailable)
* [Add-STFAuthenticationService](Add-STFAuthenticationService)
* [Get-STFAuthenticationService](Get-STFAuthenticationService)
* [Remove-STFAuthenticationService](Remove-STFAuthenticationService)
* [Add-STFAuthenticationServiceProtocol](Add-STFAuthenticationServiceProtocol)
* [Remove-STFAuthenticationServiceProtocol](Remove-STFAuthenticationServiceProtocol)
* [Get-STFAuthenticationServiceProtocol](Get-STFAuthenticationServiceProtocol)
* [Enable-STFAuthenticationServiceProtocol](Enable-STFAuthenticationServiceProtocol)
* [Disable-STFAuthenticationServiceProtocol](Disable-STFAuthenticationServiceProtocol)
* [Set-STFClaimsFactoryNames](Set-STFClaimsFactoryNames)