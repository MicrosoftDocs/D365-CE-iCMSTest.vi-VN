---
title: Download tools from NuGet (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Download the Plugin Registration, Package Deployment, and other core tools from Nuget.
ms.custom: ''
ms.date: 12/6/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: feb3e634-7c60-46fd-8b92-3f5682b1570b
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 9079171bde0db7b93488663c98be68a662095b38
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388321"
---
# <a name="download-tools-from-nuget"></a>Download tools from NuGet 

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

You can download tools used in development from NuGet using the  powershell script found below. These tools include:

|Tool|NuGet Package|
|-|-|
|Code generation tool `CrmSvcUtil.exe`|[Microsoft.CrmSdk.CoreTools](https://www.nuget.org/packages/Microsoft.CrmSdk.CoreTools)|
|Configuration Migration tool `DataMigrationUtility.exe`|[Microsoft.CrmSdk.XrmTooling.ConfigurationMigration.Wpf](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.ConfigurationMigration.Wpf)|
|Package Deployer `PackageDeployer.exe`|[Microsoft.CrmSdk.XrmTooling.PackageDeployment.WPF](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf)|
|Plug-in Registration Tool `PluginRegistration.exe` |[Microsoft.CrmSdk.XrmTooling.PluginRegistrationTool](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PluginRegistrationTool)|
|SolutionPackager tool `SolutionPackager.exe`|[Microsoft.CrmSdk.CoreTools](https://www.nuget.org/packages/Microsoft.CrmSdk.CoreTools)|

## <a name="download-tools-using-powershell"></a>Download tools using PowerShell

<!-- This script won't work properly until an official release is shipped. They are all pre-release as of 10/4/2017. To get the pre-release version, add the -PreRelease parameter to the nuget install call.-->

1. In your Windows Start menu, type `Windows Powershell` and open it.
1. Navigate to the folder you want to install the tools to. For example if you want to install them in a `devtools` folder on your D drive, type `cd D:\devtools`.
1. Copy and paste the following PowerShell script into the PowerShell window and press Enter.

    ```powershell
    $sourceNugetExe = "https://dist.nuget.org/win-x86-commandline/latest/nuget.exe"
    $targetNugetExe = ".\nuget.exe"
    Remove-Item .\Tools -Force -Recurse -ErrorAction Ignore
    Invoke-WebRequest $sourceNugetExe -OutFile $targetNugetExe
    Set-Alias nuget $targetNugetExe -Scope Global -Verbose
        
    ##
    ##Download Plugin Registration Tool
    ##
    ./nuget install Microsoft.CrmSdk.XrmTooling.PluginRegistrationTool -O .\Tools
    md .\Tools\PluginRegistration
    $prtFolder = Get-ChildItem ./Tools | Where-Object {$_.Name -match 'Microsoft.CrmSdk.XrmTooling.PluginRegistrationTool.'}
    move .\Tools\$prtFolder\tools\*.* .\Tools\PluginRegistration
    Remove-Item .\Tools\$prtFolder -Force -Recurse
    
    ##
    ##Download CoreTools
    ##
    ./nuget install  Microsoft.CrmSdk.CoreTools -O .\Tools
    md .\Tools\CoreTools
    $coreToolsFolder = Get-ChildItem ./Tools | Where-Object {$_.Name -match 'Microsoft.CrmSdk.CoreTools.'}
    move .\Tools\$coreToolsFolder\content\bin\coretools\*.* .\Tools\CoreTools
    Remove-Item .\Tools\$coreToolsFolder -Force -Recurse

    ##
    ##Download Configuration Migration
    ##
    ./nuget install  Microsoft.CrmSdk.XrmTooling.ConfigurationMigration.Wpf -O .\Tools
    md .\Tools\ConfigurationMigration
    $configMigFolder = Get-ChildItem ./Tools | Where-Object {$_.Name -match 'Microsoft.CrmSdk.XrmTooling.ConfigurationMigration.Wpf.'}
    move .\Tools\$configMigFolder\tools\*.* .\Tools\ConfigurationMigration
    Remove-Item .\Tools\$configMigFolder -Force -Recurse
    
    ##
    ##Download Package Deployer 
    ##
    ./nuget install  Microsoft.CrmSdk.XrmTooling.PackageDeployment.WPF -O .\Tools
    md .\Tools\PackageDeployment
    $pdFolder = Get-ChildItem ./Tools | Where-Object {$_.Name -match 'Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf.'}
    move .\Tools\$pdFolder\tools\*.* .\Tools\PackageDeployment
    Remove-Item .\Tools\$pdFolder -Force -Recurse

    ##
    ##Download Package Deployer PowerShell module
    ##
    ./nuget install Microsoft.CrmSdk.XrmTooling.PackageDeployment.PowerShell -O .\Tools
    $pdPoshFolder = Get-ChildItem ./Tools | Where-Object {$_.Name -match 'Microsoft.CrmSdk.XrmTooling.PackageDeployment.PowerShell.'}
    move .\Tools\$pdPoshFolder\tools\*.* .\Tools\PackageDeployment.PowerShell
    Remove-Item .\Tools\$pdPoshFolder -Force -Recurse

    ##
    ##Remove NuGet.exe
    ##
    Remove-Item nuget.exe    
    ```

1. You will find the tools in the following folders:

- `[Your folder]\Tools\ConfigurationMigration`
- `[Your folder]\Tools\CoreTools`
- `[Your folder]\Tools\PackageDeployment`
- `[Your folder]\Tools\PluginRegistration`

To get the latest version of these tools, repeat these steps.

## <a name="see-also"></a>Xem thêm
[Developer tools](developer-tools.md)<br />
[Visual Studio and the .NET Framework](visual-studio-dot-net-framework.md)<br />
[Create early bound entity classes](org-service/create-early-bound-entity-classes-code-generation-tool.md)<br />
[Create extensions for the code generation tool](org-service/extend-code-generation-tool.md)<br />
[Browse the metadata for your organization](browse-your-metadata.md)<br />
[Analyze plug-in performance](analyze-plugin-performance.md)<br />
[Solution tools for team development](solution-tools-team-development.md)<br />
[Deploy packages using Dynamics CRM Package Deployer and Windows PowerShell](../admin/deploy-packages-using-package-deployer-windows-powershell.md)<br />
[Walkthrough: Register a plug-in using the plug-in registration tool](walkthrough-register-plugin-using-plugin-registration-tool.md)<br />