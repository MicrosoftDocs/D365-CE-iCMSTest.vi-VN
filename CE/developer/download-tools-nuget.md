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
# <a name="download-tools-from-nuget"></a><span data-ttu-id="7acd5-103">Download tools from NuGet</span><span class="sxs-lookup"><span data-stu-id="7acd5-103">Download tools from NuGet</span></span> 

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="7acd5-104">You can download tools used in development from NuGet using the  powershell script found below.</span><span class="sxs-lookup"><span data-stu-id="7acd5-104">You can download tools used in development from NuGet using the  powershell script found below.</span></span> <span data-ttu-id="7acd5-105">These tools include:</span><span class="sxs-lookup"><span data-stu-id="7acd5-105">These tools include:</span></span>

|<span data-ttu-id="7acd5-106">Tool</span><span class="sxs-lookup"><span data-stu-id="7acd5-106">Tool</span></span>|<span data-ttu-id="7acd5-107">NuGet Package</span><span class="sxs-lookup"><span data-stu-id="7acd5-107">NuGet Package</span></span>|
|-|-|
|<span data-ttu-id="7acd5-108">Code generation tool `CrmSvcUtil.exe`</span><span class="sxs-lookup"><span data-stu-id="7acd5-108">Code generation tool `CrmSvcUtil.exe`</span></span>|[<span data-ttu-id="7acd5-109">Microsoft.CrmSdk.CoreTools</span><span class="sxs-lookup"><span data-stu-id="7acd5-109">Microsoft.CrmSdk.CoreTools</span></span>](https://www.nuget.org/packages/Microsoft.CrmSdk.CoreTools)|
|<span data-ttu-id="7acd5-110">Configuration Migration tool `DataMigrationUtility.exe`</span><span class="sxs-lookup"><span data-stu-id="7acd5-110">Configuration Migration tool `DataMigrationUtility.exe`</span></span>|[<span data-ttu-id="7acd5-111">Microsoft.CrmSdk.XrmTooling.ConfigurationMigration.Wpf</span><span class="sxs-lookup"><span data-stu-id="7acd5-111">Microsoft.CrmSdk.XrmTooling.ConfigurationMigration.Wpf</span></span>](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.ConfigurationMigration.Wpf)|
|<span data-ttu-id="7acd5-112">Package Deployer `PackageDeployer.exe`</span><span class="sxs-lookup"><span data-stu-id="7acd5-112">Package Deployer `PackageDeployer.exe`</span></span>|[<span data-ttu-id="7acd5-113">Microsoft.CrmSdk.XrmTooling.PackageDeployment.WPF</span><span class="sxs-lookup"><span data-stu-id="7acd5-113">Microsoft.CrmSdk.XrmTooling.PackageDeployment.WPF</span></span>](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf)|
|<span data-ttu-id="7acd5-114">Plug-in Registration Tool `PluginRegistration.exe`</span><span class="sxs-lookup"><span data-stu-id="7acd5-114">Plug-in Registration Tool `PluginRegistration.exe`</span></span> |[<span data-ttu-id="7acd5-115">Microsoft.CrmSdk.XrmTooling.PluginRegistrationTool</span><span class="sxs-lookup"><span data-stu-id="7acd5-115">Microsoft.CrmSdk.XrmTooling.PluginRegistrationTool</span></span>](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PluginRegistrationTool)|
|<span data-ttu-id="7acd5-116">SolutionPackager tool `SolutionPackager.exe`</span><span class="sxs-lookup"><span data-stu-id="7acd5-116">SolutionPackager tool `SolutionPackager.exe`</span></span>|[<span data-ttu-id="7acd5-117">Microsoft.CrmSdk.CoreTools</span><span class="sxs-lookup"><span data-stu-id="7acd5-117">Microsoft.CrmSdk.CoreTools</span></span>](https://www.nuget.org/packages/Microsoft.CrmSdk.CoreTools)|

## <a name="download-tools-using-powershell"></a><span data-ttu-id="7acd5-118">Download tools using PowerShell</span><span class="sxs-lookup"><span data-stu-id="7acd5-118">Download tools using PowerShell</span></span>

<!-- This script won't work properly until an official release is shipped. They are all pre-release as of 10/4/2017. To get the pre-release version, add the -PreRelease parameter to the nuget install call.-->

1. <span data-ttu-id="7acd5-119">In your Windows Start menu, type `Windows Powershell` and open it.</span><span class="sxs-lookup"><span data-stu-id="7acd5-119">In your Windows Start menu, type `Windows Powershell` and open it.</span></span>
1. <span data-ttu-id="7acd5-120">Navigate to the folder you want to install the tools to.</span><span class="sxs-lookup"><span data-stu-id="7acd5-120">Navigate to the folder you want to install the tools to.</span></span> <span data-ttu-id="7acd5-121">For example if you want to install them in a `devtools` folder on your D drive, type `cd D:\devtools`.</span><span class="sxs-lookup"><span data-stu-id="7acd5-121">For example if you want to install them in a `devtools` folder on your D drive, type `cd D:\devtools`.</span></span>
1. <span data-ttu-id="7acd5-122">Copy and paste the following PowerShell script into the PowerShell window and press Enter.</span><span class="sxs-lookup"><span data-stu-id="7acd5-122">Copy and paste the following PowerShell script into the PowerShell window and press Enter.</span></span>

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

1. <span data-ttu-id="7acd5-123">You will find the tools in the following folders:</span><span class="sxs-lookup"><span data-stu-id="7acd5-123">You will find the tools in the following folders:</span></span>

- `[Your folder]\Tools\ConfigurationMigration`
- `[Your folder]\Tools\CoreTools`
- `[Your folder]\Tools\PackageDeployment`
- `[Your folder]\Tools\PluginRegistration`

<span data-ttu-id="7acd5-124">To get the latest version of these tools, repeat these steps.</span><span class="sxs-lookup"><span data-stu-id="7acd5-124">To get the latest version of these tools, repeat these steps.</span></span>

## <a name="see-also"></a><span data-ttu-id="7acd5-125">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="7acd5-125">See Also</span></span>
[<span data-ttu-id="7acd5-126">Developer tools</span><span class="sxs-lookup"><span data-stu-id="7acd5-126">Developer tools</span></span>](developer-tools.md)<br />
[<span data-ttu-id="7acd5-127">Visual Studio and the .NET Framework</span><span class="sxs-lookup"><span data-stu-id="7acd5-127">Visual Studio and the .NET Framework</span></span>](visual-studio-dot-net-framework.md)<br />
[<span data-ttu-id="7acd5-128">Create early bound entity classes</span><span class="sxs-lookup"><span data-stu-id="7acd5-128">Create early bound entity classes</span></span>](org-service/create-early-bound-entity-classes-code-generation-tool.md)<br />
[<span data-ttu-id="7acd5-129">Create extensions for the code generation tool</span><span class="sxs-lookup"><span data-stu-id="7acd5-129">Create extensions for the code generation tool</span></span>](org-service/extend-code-generation-tool.md)<br />
[<span data-ttu-id="7acd5-130">Browse the metadata for your organization</span><span class="sxs-lookup"><span data-stu-id="7acd5-130">Browse the metadata for your organization</span></span>](browse-your-metadata.md)<br />
[<span data-ttu-id="7acd5-131">Analyze plug-in performance</span><span class="sxs-lookup"><span data-stu-id="7acd5-131">Analyze plug-in performance</span></span>](analyze-plugin-performance.md)<br />
[<span data-ttu-id="7acd5-132">Solution tools for team development</span><span class="sxs-lookup"><span data-stu-id="7acd5-132">Solution tools for team development</span></span>](solution-tools-team-development.md)<br />
[<span data-ttu-id="7acd5-133">Deploy packages using Dynamics CRM Package Deployer and Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="7acd5-133">Deploy packages using Dynamics CRM Package Deployer and Windows PowerShell</span></span>](../admin/deploy-packages-using-package-deployer-windows-powershell.md)<br />
[<span data-ttu-id="7acd5-134">Walkthrough: Register a plug-in using the plug-in registration tool</span><span class="sxs-lookup"><span data-stu-id="7acd5-134">Walkthrough: Register a plug-in using the plug-in registration tool</span></span>](walkthrough-register-plugin-using-plugin-registration-tool.md)<br />
