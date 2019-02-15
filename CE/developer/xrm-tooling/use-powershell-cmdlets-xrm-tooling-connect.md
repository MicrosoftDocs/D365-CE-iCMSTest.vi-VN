---
title: Use PowerShell cmdlets for XRM tooling to connect to Dynamics 365 for Customer Engagement (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Learn how to use Powershell cmdlets for XRM tooling like Get-CrmConnection and Get-CrmOrganizations to connect to Dynamics 365 for Customer Engagement and retrieve organizations that the current user has access to
ms.custom: ''
ms.date: 05/10/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: get-started-article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 81816457-c963-46ca-b350-615fa75f56a7
caps.latest.revision: 27
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ddd96c9fd5eb8affff576cc003b9f9abb32764ac
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388187"
---
# <a name="use-powershell-cmdlets-for-xrm-tooling-to-connect-to-dynamics-365-for-customer-engagement"></a><span data-ttu-id="6eeee-103">Use PowerShell cmdlets for XRM tooling to connect to Dynamics 365 for Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="6eeee-103">Use PowerShell cmdlets for XRM tooling to connect to Dynamics 365 for Customer Engagement</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="6eeee-104">XRM tooling provides you with the following [!INCLUDE[pn_PowerShell](../../includes/pn-powershell.md)] cmdlets that you can use to connect to [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps and retrieve organizations that the current user has access to: `Get-CrmConnection` and `Get-CrmOrganizations`.</span><span class="sxs-lookup"><span data-stu-id="6eeee-104">XRM tooling provides you with the following [!INCLUDE[pn_PowerShell](../../includes/pn-powershell.md)] cmdlets that you can use to connect to [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps and retrieve organizations that the current user has access to: `Get-CrmConnection` and `Get-CrmOrganizations`.</span></span>  
  
<a name="Prereq"></a>   

## <a name="prerequisites"></a><span data-ttu-id="6eeee-105">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="6eeee-105">Prerequisites</span></span>  
  
- <span data-ttu-id="6eeee-106">To use the XRM tooling cmdlets, you need [!INCLUDE[pn_PowerShell_short](../../includes/pn-powershell-short.md)] version 3.0 or later.</span><span class="sxs-lookup"><span data-stu-id="6eeee-106">To use the XRM tooling cmdlets, you need [!INCLUDE[pn_PowerShell_short](../../includes/pn-powershell-short.md)] version 3.0 or later.</span></span> <span data-ttu-id="6eeee-107">To check the version, open a [!INCLUDE[pn_PowerShell_short](../../includes/pn-powershell-short.md)] window and run the following command: `$Host`</span><span class="sxs-lookup"><span data-stu-id="6eeee-107">To check the version, open a [!INCLUDE[pn_PowerShell_short](../../includes/pn-powershell-short.md)] window and run the following command: `$Host`</span></span>  
  
- <span data-ttu-id="6eeee-108">Đặt chính sách thực hiện để chạy các mã lệnh [!INCLUDE[pn_PowerShell_short](../../includes/pn-powershell-short.md)] đã ký.</span><span class="sxs-lookup"><span data-stu-id="6eeee-108">Set the execution policy to run the signed [!INCLUDE[pn_PowerShell_short](../../includes/pn-powershell-short.md)] scripts.</span></span> <span data-ttu-id="6eeee-109">To do so, open a [!INCLUDE[pn_PowerShell_short](../../includes/pn-powershell-short.md)] window as an administrator and run the following command: `Set-ExecutionPolicy -ExecutionPolicy RemoteSigned`</span><span class="sxs-lookup"><span data-stu-id="6eeee-109">To do so, open a [!INCLUDE[pn_PowerShell_short](../../includes/pn-powershell-short.md)] window as an administrator and run the following command: `Set-ExecutionPolicy -ExecutionPolicy RemoteSigned`</span></span>  
  
<a name="register"></a>   

## <a name="register-the-cmdlets"></a><span data-ttu-id="6eeee-110">Đăng ký các lệnh ghép ngắn</span><span class="sxs-lookup"><span data-stu-id="6eeee-110">Register the cmdlets</span></span>  

 <span data-ttu-id="6eeee-111">Before you can use the [!INCLUDE[pn_PowerShell_short](../../includes/pn-powershell-short.md)] cmdlets, you have to register them.</span><span class="sxs-lookup"><span data-stu-id="6eeee-111">Before you can use the [!INCLUDE[pn_PowerShell_short](../../includes/pn-powershell-short.md)] cmdlets, you have to register them.</span></span> <span data-ttu-id="6eeee-112">The XRM tooling PowerShell cmdlets are available as a NuGet package here: [https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.CrmConnector.PowerShell](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.CrmConnector.PowerShell/).</span><span class="sxs-lookup"><span data-stu-id="6eeee-112">The XRM tooling PowerShell cmdlets are available as a NuGet package here: [https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.CrmConnector.PowerShell](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.CrmConnector.PowerShell/).</span></span> <span data-ttu-id="6eeee-113">To download and register the cmdlets:</span><span class="sxs-lookup"><span data-stu-id="6eeee-113">To download and register the cmdlets:</span></span> 
  
1. <span data-ttu-id="6eeee-114">Open notepad, and copy the following script:</span><span class="sxs-lookup"><span data-stu-id="6eeee-114">Open notepad, and copy the following script:</span></span>

    ```powershell
    @PowerShell.exe -ExecutionPolicy RemoteSigned -Command "Invoke-Expression -Command ((Get-Content -Path '%~f0' | Select-Object -Skip 2) -join [environment]::NewLine)"
    @exit /b %Errorlevel%
    $currentFolder = Get-Location
    cd $currentFolder
    $sourceNugetExe = "https://dist.nuget.org/win-x86-commandline/latest/nuget.exe"
    $targetNugetExe = ".\nuget.exe"
    Remove-Item .\Tools -Force -Recurse -ErrorAction Ignore
    Invoke-WebRequest $sourceNugetExe -OutFile $targetNugetExe
    Set-Alias nuget $targetNugetExe -Scope Global -Verbose

    ##
    ##Specify the NuGet package source
    ##
    $nugetPackageSource = "https://api.nuget.org/v3/index.json"

    ##
    ##Download XRM Tooling PowerShell cmdlets
    ##
    ./nuget install -source $nugetPackageSource Microsoft.CrmSdk.XrmTooling.CrmConnector.PowerShell -O .\Tools
    md .\Tools\XRMToolingPowerShell
    $cmdletFolder = Get-ChildItem ./Tools | Where-Object {$_.Name -match 'Microsoft.CrmSdk.XrmTooling.CrmConnector.PowerShell.'}
    move .\Tools\$cmdletFolder\tools\*.* .\Tools\XRMToolingPowerShell
    Remove-Item .\Tools\$cmdletFolder -Force -Recurse

    ##
    ##Remove NuGet.exe
    ##
    Remove-Item nuget.exe
  
2. Save the notepad file as batch file on your computer: **GetTools.bat**.
3. Navigate to the folder where you saved the file, for example C:\SDK, and double-click the **GetTools.bat** file to run the script. This will create a Tools\XRMToolingPowerShell folder in the same location as your **GetTools.bat** file. The Tools\XRMToolingPowerShell folder contains the `RegisterXRMTooling.ps1` script to register the cmdlets, and other associated files.
4. Start [!INCLUDE[pn_PowerShell](../../includes/pn-powershell.md)] on your computer with elevated privileges (run as administrator).  
  
5. At the prompt, change your directory to the folder that contains the [!INCLUDE[pn_PowerShell_short](../../includes/pn-powershell-short.md)] script for registering the cmdlets. For example:  
  
   ```powershell  
   cd c:\SDK\Tools\XRMToolingPowerShell  
   ```  
  
6. <span data-ttu-id="6eeee-115">Run the `RegisterXRMTooling.ps1` script to register the XRM tooling [!INCLUDE[pn_PowerShell_short](../../includes/pn-powershell-short.md)] cmdlets.</span><span class="sxs-lookup"><span data-stu-id="6eeee-115">Run the `RegisterXRMTooling.ps1` script to register the XRM tooling [!INCLUDE[pn_PowerShell_short](../../includes/pn-powershell-short.md)] cmdlets.</span></span> <span data-ttu-id="6eeee-116">Type the following command, and press ENTER:</span><span class="sxs-lookup"><span data-stu-id="6eeee-116">Type the following command, and press ENTER:</span></span>  
  
   ```powershell
   .\RegisterXRMTooling.ps1  
   ```
  
   <span data-ttu-id="6eeee-117">You’re now ready to use these [!INCLUDE[pn_PowerShell](../../includes/pn-powershell.md)] cmdlets.</span><span class="sxs-lookup"><span data-stu-id="6eeee-117">You’re now ready to use these [!INCLUDE[pn_PowerShell](../../includes/pn-powershell.md)] cmdlets.</span></span> <span data-ttu-id="6eeee-118">To list the cmdlets that you registered, run the following command in the [!INCLUDE[pn_PowerShell](../../includes/pn-powershell.md)] window:</span><span class="sxs-lookup"><span data-stu-id="6eeee-118">To list the cmdlets that you registered, run the following command in the [!INCLUDE[pn_PowerShell](../../includes/pn-powershell.md)] window:</span></span>  
  
```powershell
Get-Help “Crm”  
```  
  
<a name="RetrieveOrgs"></a>   

## <a name="use-the-cmdlet-to-retrieve-organizations-from-includepndynamicscrmincludespn-dynamics-crmmd-apps"></a><span data-ttu-id="6eeee-119">Use the cmdlet to retrieve organizations from [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps</span><span class="sxs-lookup"><span data-stu-id="6eeee-119">Use the cmdlet to retrieve organizations from [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps</span></span> 

 <span data-ttu-id="6eeee-120">Use the `Get-CrmOrganizations` cmdlet to retrieve the organizations that you have access to.</span><span class="sxs-lookup"><span data-stu-id="6eeee-120">Use the `Get-CrmOrganizations` cmdlet to retrieve the organizations that you have access to.</span></span>  
  
1. <span data-ttu-id="6eeee-121">Cung cấp ủy nhiệm của bạn để kết nối với phiên bản [!INCLUDE[pn_crm_op_edition](../../includes/pn-crm-onprem.md)] hoặc [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] của bạn.</span><span class="sxs-lookup"><span data-stu-id="6eeee-121">Provide your credentials to connect to your [!INCLUDE[pn_crm_op_edition](../../includes/pn-crm-onprem.md)] or [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] instance.</span></span> <span data-ttu-id="6eeee-122">Running the following command will prompt you to type your user name and password to connect to the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance, and it will be stored in the `$Cred` variable.</span><span class="sxs-lookup"><span data-stu-id="6eeee-122">Running the following command will prompt you to type your user name and password to connect to the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance, and it will be stored in the `$Cred` variable.</span></span>  
  
   ```powershell  
   $Cred = Get-Credential  
   ```  
2. <span data-ttu-id="6eeee-123">Use the following command to retrieve your organizations, and store the information in the `$CRMOrgs` variable:</span><span class="sxs-lookup"><span data-stu-id="6eeee-123">Use the following command to retrieve your organizations, and store the information in the `$CRMOrgs` variable:</span></span> 

   - <span data-ttu-id="6eeee-124">If you’re connecting to the [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] apps instance:</span><span class="sxs-lookup"><span data-stu-id="6eeee-124">If you’re connecting to the [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] apps instance:</span></span>  
  
       ```powershell  
       $CRMOrgs = Get-CrmOrganizations -Credential $Cred -DeploymentRegion NorthAmerica –OnlineType Office365  
       ```  
  
       > [!NOTE]
       >  <span data-ttu-id="6eeee-125">For the `DeploymentRegion` parameter, valid values are `NorthAmerica`, `EMEA`, `APAC`, `SouthAmerica`, `Oceania`, `JPN`, `CAN`, `IND`, and `NorthAmerica2`.</span><span class="sxs-lookup"><span data-stu-id="6eeee-125">For the `DeploymentRegion` parameter, valid values are `NorthAmerica`, `EMEA`, `APAC`, `SouthAmerica`, `Oceania`, `JPN`, `CAN`, `IND`, and `NorthAmerica2`.</span></span> <span data-ttu-id="6eeee-126">For the `OnlineType` parameter, specify `Office365`.</span><span class="sxs-lookup"><span data-stu-id="6eeee-126">For the `OnlineType` parameter, specify `Office365`.</span></span>
  
   - <span data-ttu-id="6eeee-127">If you’re connecting to the [!INCLUDE[pn_crm_op_edition](../../includes/pn-crm-onprem.md)] server:</span><span class="sxs-lookup"><span data-stu-id="6eeee-127">If you’re connecting to the [!INCLUDE[pn_crm_op_edition](../../includes/pn-crm-onprem.md)] server:</span></span>  
  
     ```powershell  
     $CRMOrgs = Get-CrmOrganizations –ServerUrl http://<CRM_Server_Host> –Credential $Cred  
     ```      
  
   - <span data-ttu-id="6eeee-128">If you’re connecting to the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] server using the claims-based authentication against the specified Home realm:</span><span class="sxs-lookup"><span data-stu-id="6eeee-128">If you’re connecting to the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] server using the claims-based authentication against the specified Home realm:</span></span>  
  
     ```powershell  
     $CRMOrgs = Get-CrmOrganizations –ServerUrl http://<CRM_Server_Host> –Credential $Cred –HomRealmURL http://<Identity_Provider_Address>  
     ```  
  
3. <span data-ttu-id="6eeee-129">Cung cấp ủy nhiệm của bạn được xác nhận khi bạn chạy lệnh trong bước 2.</span><span class="sxs-lookup"><span data-stu-id="6eeee-129">Your supplied credentials are validated when you run the command in step 2.</span></span> <span data-ttu-id="6eeee-130">On successful execution of the command, type the following command, and press ENTER to display the organizations that you have access to:</span><span class="sxs-lookup"><span data-stu-id="6eeee-130">On successful execution of the command, type the following command, and press ENTER to display the organizations that you have access to:</span></span>  
  
   ```powershell  
   $CRMOrgs  
   ```  
  
   ![Dynamics 365 for Customer Engagement organization information](../media/xrmtooling-powershell-1.png)  
  
   > [!TIP]
   >  <span data-ttu-id="6eeee-132">You can use the variable that was used to store the retrieved [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] organizations (in this case `$CRMOrgs`) with the `Get-CrmConnection` cmdlet to connect to [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="6eeee-132">You can use the variable that was used to store the retrieved [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] organizations (in this case `$CRMOrgs`) with the `Get-CrmConnection` cmdlet to connect to [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)].</span></span> <span data-ttu-id="6eeee-133">To specify the org name, use the following command: `$CRMOrgs.UniqueName`.</span><span class="sxs-lookup"><span data-stu-id="6eeee-133">To specify the org name, use the following command: `$CRMOrgs.UniqueName`.</span></span>  
   > 
   >  <span data-ttu-id="6eeee-134">If there is more than one organization value stored in the `$CRMOrgs` variable, you can refer to the `nth` organization using the following command: `$CRMOrgs[n-1]`.</span><span class="sxs-lookup"><span data-stu-id="6eeee-134">If there is more than one organization value stored in the `$CRMOrgs` variable, you can refer to the `nth` organization using the following command: `$CRMOrgs[n-1]`.</span></span> <span data-ttu-id="6eeee-135">For example, to refer to the unique name of the second organization in the `$CRMOrgs` variable, use the following command: `$CRMOrgs[1].UniqueName`.</span><span class="sxs-lookup"><span data-stu-id="6eeee-135">For example, to refer to the unique name of the second organization in the `$CRMOrgs` variable, use the following command: `$CRMOrgs[1].UniqueName`.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="6eeee-136">[Accessing Values in an Array](https://technet.microsoft.com/library/ee692791.aspx)</span><span class="sxs-lookup"><span data-stu-id="6eeee-136">[Accessing Values in an Array](https://technet.microsoft.com/library/ee692791.aspx)</span></span>  
  
<a name="ConnecttoCRM"></a>
   
## <a name="use-the-cmdlet-to-connect-to-includepndynamicscrmincludespn-dynamics-crmmd-apps"></a><span data-ttu-id="6eeee-137">Use the cmdlet to connect to [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps</span><span class="sxs-lookup"><span data-stu-id="6eeee-137">Use the cmdlet to connect to [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps</span></span> 

 <span data-ttu-id="6eeee-138">Use the `Get-CrmConnection` cmdlet to connect to a [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance.</span><span class="sxs-lookup"><span data-stu-id="6eeee-138">Use the `Get-CrmConnection` cmdlet to connect to a [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance.</span></span> <span data-ttu-id="6eeee-139">The cmdlet lets you either use the XRM tooling common login control to specify your credentials and connect to [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] or lets you specify your credentials as inline parameters.</span><span class="sxs-lookup"><span data-stu-id="6eeee-139">The cmdlet lets you either use the XRM tooling common login control to specify your credentials and connect to [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] or lets you specify your credentials as inline parameters.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="6eeee-140">[Use the XRM Tooling common login control](use-xrm-tooling-common-login-control-client-applications.md)</span><span class="sxs-lookup"><span data-stu-id="6eeee-140">[Use the XRM Tooling common login control](use-xrm-tooling-common-login-control-client-applications.md)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6eeee-141">Before using the `Get-CrmConnection` cmdlet, ensure that you use the following command to enforce usage of TLS 1.2 by PowerShell to connect to your Customer Engagement instance:</span><span class="sxs-lookup"><span data-stu-id="6eeee-141">Before using the `Get-CrmConnection` cmdlet, ensure that you use the following command to enforce usage of TLS 1.2 by PowerShell to connect to your Customer Engagement instance:</span></span><br/>
> `[System.Net.ServicePointManager]::SecurityProtocol = [System.Net.SecurityProtocolType]::Tls12`<br/>
> <span data-ttu-id="6eeee-142">More information about TLS 1.2 requirement for Customer Engagement connection: [Blog Post: Updates coming to Dynamics 365 for Customer Engagement apps connection security](https://blogs.msdn.microsoft.com/crm/2017/09/28/updates-coming-to-dynamics-365-customer-engagement-connection-security/)</span><span class="sxs-lookup"><span data-stu-id="6eeee-142">More information about TLS 1.2 requirement for Customer Engagement connection: [Blog Post: Updates coming to Dynamics 365 for Customer Engagement apps connection security](https://blogs.msdn.microsoft.com/crm/2017/09/28/updates-coming-to-dynamics-365-customer-engagement-connection-security/)</span></span>   
  
### <a name="connect-to-includepndynamicscrmincludespn-dynamics-crmmd-apps-by-using-the-common-login-control"></a><span data-ttu-id="6eeee-143">Connect to [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps by using the common login control</span><span class="sxs-lookup"><span data-stu-id="6eeee-143">Connect to [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps by using the common login control</span></span>  
  
1. <span data-ttu-id="6eeee-144">If you want to use the common login control to provide your credentials to connect to [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)], use the following command.</span><span class="sxs-lookup"><span data-stu-id="6eeee-144">If you want to use the common login control to provide your credentials to connect to [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)], use the following command.</span></span> <span data-ttu-id="6eeee-145">The connection information is stored in the `$CRMConn` variable so that you can use it later.</span><span class="sxs-lookup"><span data-stu-id="6eeee-145">The connection information is stored in the `$CRMConn` variable so that you can use it later.</span></span>  
  
   ```powershell  
   $CRMConn = Get-CrmConnection -InteractiveMode  
   ```  
  
2. <span data-ttu-id="6eeee-146">The **LoginControl** dialog box appears.</span><span class="sxs-lookup"><span data-stu-id="6eeee-146">The **LoginControl** dialog box appears.</span></span> <span data-ttu-id="6eeee-147">Provide your credentials to connect to your [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance, and click **Login**.</span><span class="sxs-lookup"><span data-stu-id="6eeee-147">Provide your credentials to connect to your [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance, and click **Login**.</span></span>  
  
### <a name="connect-to-includepndynamicscrmincludespn-dynamics-crmmd-apps-by-specifying-credentials-inline"></a><span data-ttu-id="6eeee-148">Connect to [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps by specifying credentials inline</span><span class="sxs-lookup"><span data-stu-id="6eeee-148">Connect to [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps by specifying credentials inline</span></span>  
  
1. <span data-ttu-id="6eeee-149">To connect to Dynamics 365 for Customer Engagement apps, use the following commands.</span><span class="sxs-lookup"><span data-stu-id="6eeee-149">To connect to Dynamics 365 for Customer Engagement apps, use the following commands.</span></span> <span data-ttu-id="6eeee-150">Note that these commands use the `$Cred` variable created earlier to store the credential while retrieving the organizations.</span><span class="sxs-lookup"><span data-stu-id="6eeee-150">Note that these commands use the `$Cred` variable created earlier to store the credential while retrieving the organizations.</span></span> <span data-ttu-id="6eeee-151">The connection information is stored in the `$CRMConn` variable:</span><span class="sxs-lookup"><span data-stu-id="6eeee-151">The connection information is stored in the `$CRMConn` variable:</span></span>

   - <span data-ttu-id="6eeee-152">If you’re connecting to the [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] apps instance:</span><span class="sxs-lookup"><span data-stu-id="6eeee-152">If you’re connecting to the [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] apps instance:</span></span>  
  
     ```powershell  
     $CRMConn = Get-CrmConnection -Credential $Cred -DeploymentRegion <Deployment region name> –OnlineType Office365 –OrganizationName <OrgName>  
     ```
  
     > [!NOTE]
     >  <span data-ttu-id="6eeee-153">For the `DeploymentRegion` parameter, valid values are `NorthAmerica`, `EMEA`, `APAC`, `SouthAmerica`, `Oceania`, `JPN`, `CAN`, `IND` and `NorthAmerica2`.</span><span class="sxs-lookup"><span data-stu-id="6eeee-153">For the `DeploymentRegion` parameter, valid values are `NorthAmerica`, `EMEA`, `APAC`, `SouthAmerica`, `Oceania`, `JPN`, `CAN`, `IND` and `NorthAmerica2`.</span></span> <span data-ttu-id="6eeee-154">For the `OnlineType` parameter, specify `Office365`.</span><span class="sxs-lookup"><span data-stu-id="6eeee-154">For the `OnlineType` parameter, specify `Office365`.</span></span> 
  
   - <span data-ttu-id="6eeee-155">If you’re connecting to the [!INCLUDE[pn_crm_op_edition](../../includes/pn-crm-onprem.md)] server:</span><span class="sxs-lookup"><span data-stu-id="6eeee-155">If you’re connecting to the [!INCLUDE[pn_crm_op_edition](../../includes/pn-crm-onprem.md)] server:</span></span>  
  
     ```powershell  
     $CRMConn = Get-CrmConnection –ServerUrl http://<CRM_Server_Host> -Credential $Cred -OrganizationName <OrgName>  
     ```
  
   - <span data-ttu-id="6eeee-156">If you’re connecting to the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] server using the claims-based authentication against the specified Home realm:</span><span class="sxs-lookup"><span data-stu-id="6eeee-156">If you’re connecting to the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] server using the claims-based authentication against the specified Home realm:</span></span>  
  
     ```powershell  
     $CRMConn = Get-CrmConnection –ServerUrl http://<CRM_Server_Host> -Credential $Cred -OrganizationName <OrgName> –HomRealmURL http://<Identity_Provider_Address>  
     ```  
  
   > [!NOTE]
   > <span data-ttu-id="6eeee-157">For the `OrganizationName` parameter in all the preceding commands, you can either specify the organization unique name or friendly name.</span><span class="sxs-lookup"><span data-stu-id="6eeee-157">For the `OrganizationName` parameter in all the preceding commands, you can either specify the organization unique name or friendly name.</span></span> <span data-ttu-id="6eeee-158">You can also use the organization unique name or friendly name that you retrieved using the `Get-CrmOrganizations` cmdlet and stored in the `$CRMOrgs` variable.</span><span class="sxs-lookup"><span data-stu-id="6eeee-158">You can also use the organization unique name or friendly name that you retrieved using the `Get-CrmOrganizations` cmdlet and stored in the `$CRMOrgs` variable.</span></span> <span data-ttu-id="6eeee-159">For example, you can use `$CRMOrgs[x].UniqueName` or `$CRMOrgs[x].FriendlyName`.</span><span class="sxs-lookup"><span data-stu-id="6eeee-159">For example, you can use `$CRMOrgs[x].UniqueName` or `$CRMOrgs[x].FriendlyName`.</span></span>  
  
2. <span data-ttu-id="6eeee-160">Cung cấp ủy nhiệm của bạn được xác nhận khi bạn chạy lệnh trong bước 1.</span><span class="sxs-lookup"><span data-stu-id="6eeee-160">Your supplied credentials are validated when you run the command in step 1.</span></span> <span data-ttu-id="6eeee-161">On successful execution of the cmdlet, type the following command, and press ENTER to display the connection information and status:</span><span class="sxs-lookup"><span data-stu-id="6eeee-161">On successful execution of the cmdlet, type the following command, and press ENTER to display the connection information and status:</span></span>  
  
   ```powershell  
   $CRMConn  
   ```  
  
   <span data-ttu-id="6eeee-162">![Dynamics 365 for Customer Engagement connection information and status](../media/xrm-tooling-powershell-2.png "Dynamics 365 for Customer Engagement connection information and status")</span><span class="sxs-lookup"><span data-stu-id="6eeee-162">![Dynamics 365 for Customer Engagement connection information and status](../media/xrm-tooling-powershell-2.png "Dynamics 365 for Customer Engagement connection information and status")</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="6eeee-163">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="6eeee-163">See also</span></span>
  
 <span data-ttu-id="6eeee-164">[Use XRM Tooling API to connect to Dynamics 365 for Customer Engagement apps](use-crmserviceclient-constructors-connect.md) </span><span class="sxs-lookup"><span data-stu-id="6eeee-164">[Use XRM Tooling API to connect to Dynamics 365 for Customer Engagement apps](use-crmserviceclient-constructors-connect.md) </span></span>  
 <span data-ttu-id="6eeee-165">[Build Windows client applications using the XRM tools](../build-windows-client-applications-xrm-tools.md) </span><span class="sxs-lookup"><span data-stu-id="6eeee-165">[Build Windows client applications using the XRM tools](../build-windows-client-applications-xrm-tools.md) </span></span>  
 [<span data-ttu-id="6eeee-166">Blog: PowerShell module for performing data operations and manipulating user and system settings in CRM</span><span class="sxs-lookup"><span data-stu-id="6eeee-166">Blog: PowerShell module for performing data operations and manipulating user and system settings in CRM</span></span>](http://blogs.msdn.com/b/crm/archive/2015/09/25/powershell-module-for-performing-data-operations-and-manipulating-user-and-system-settings-in-crm.aspx)
