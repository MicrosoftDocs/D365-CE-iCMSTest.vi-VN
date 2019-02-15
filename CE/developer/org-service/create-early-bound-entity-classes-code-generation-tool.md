---
title: Create early bound entity classes with the code generation tool (CrmSvcUtil.exe) (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: ''
keywords: ''
ms.date: 05/11/2018
ms.service: crm-online
ms.custom: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 06abab26-40fc-4b85-9a2a-5e68903ea138
author: JimDaly
ms.author: jdaly
manager: amyla
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 8e74be6b2e0a930f965b59c7153a525aef60aed4
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385638"
---
# <a name="create-early-bound-entity-classes-with-the-code-generation-tool-crmsvcutilexe"></a><span data-ttu-id="56a15-102">Create early bound entity classes with the code generation tool (CrmSvcUtil.exe)</span><span class="sxs-lookup"><span data-stu-id="56a15-102">Create early bound entity classes with the code generation tool (CrmSvcUtil.exe)</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="56a15-103">**CrmSvcUtil.exe** is a command-line code generation tool for use with [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="56a15-103">**CrmSvcUtil.exe** is a command-line code generation tool for use with [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span></span> <span data-ttu-id="56a15-104">This tool generates early-bound [!INCLUDE[pn_NET_Framework](../../includes/pn-net-framework.md)] classes that represent the entity data model used by [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="56a15-104">This tool generates early-bound [!INCLUDE[pn_NET_Framework](../../includes/pn-net-framework.md)] classes that represent the entity data model used by [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span></span>

<span data-ttu-id="56a15-105">The code generation tool (CrmSvcUtil.exe) is distributed as part of the [Microsoft.CrmSdk.CoreTools](https://www.nuget.org/packages/Microsoft.CrmSdk.CoreTools) NuGet package.</span><span class="sxs-lookup"><span data-stu-id="56a15-105">The code generation tool (CrmSvcUtil.exe) is distributed as part of the [Microsoft.CrmSdk.CoreTools](https://www.nuget.org/packages/Microsoft.CrmSdk.CoreTools) NuGet package.</span></span> <span data-ttu-id="56a15-106">For information about downloading the code generation tool (CrmSvcUtil.exe), see [Download tools from NuGet](../download-tools-NuGet.md).</span><span class="sxs-lookup"><span data-stu-id="56a15-106">For information about downloading the code generation tool (CrmSvcUtil.exe), see [Download tools from NuGet](../download-tools-NuGet.md).</span></span>

<a name="bkmk_about"></a>
## <a name="about-the-code-generation-tool"></a><span data-ttu-id="56a15-107">About the code generation tool</span><span class="sxs-lookup"><span data-stu-id="56a15-107">About the code generation tool</span></span>

<span data-ttu-id="56a15-108">The **CrmSvcUtil.exe** tool creates a [!INCLUDE[pn_MS_Visual_C#](../../includes/pn-ms-visual-csharp.md)] or [!INCLUDE[pn_Visual_Basic](../../includes/pn-visual-basic.md)] output file that contains strongly-typed classes for entities in your organization.</span><span class="sxs-lookup"><span data-stu-id="56a15-108">The **CrmSvcUtil.exe** tool creates a [!INCLUDE[pn_MS_Visual_C#](../../includes/pn-ms-visual-csharp.md)] or [!INCLUDE[pn_Visual_Basic](../../includes/pn-visual-basic.md)] output file that contains strongly-typed classes for entities in your organization.</span></span> <span data-ttu-id="56a15-109">This includes custom entities and attributes.</span><span class="sxs-lookup"><span data-stu-id="56a15-109">This includes custom entities and attributes.</span></span> <span data-ttu-id="56a15-110">This output file contains one class for each entity, providing early binding and [!INCLUDE[pn_IntelliSense](../../includes/pn-intellisense.md)] support in [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)] to aid you as you write custom code.</span><span class="sxs-lookup"><span data-stu-id="56a15-110">This output file contains one class for each entity, providing early binding and [!INCLUDE[pn_IntelliSense](../../includes/pn-intellisense.md)] support in [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)] to aid you as you write custom code.</span></span> <span data-ttu-id="56a15-111">The generated classes are partial classes that can be extended with custom business logic in separate files.</span><span class="sxs-lookup"><span data-stu-id="56a15-111">The generated classes are partial classes that can be extended with custom business logic in separate files.</span></span> <span data-ttu-id="56a15-112">You can also create extensions to this tool.</span><span class="sxs-lookup"><span data-stu-id="56a15-112">You can also create extensions to this tool.</span></span> <span data-ttu-id="56a15-113">For more information, see [Create Extensions for the Code Generation Tool](extend-code-generation-tool.md).</span><span class="sxs-lookup"><span data-stu-id="56a15-113">For more information, see [Create Extensions for the Code Generation Tool](extend-code-generation-tool.md).</span></span>  

<span data-ttu-id="56a15-114">The tool can also be used to generate a class derived from the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext> class that acts as an entity container in the entity data model.</span><span class="sxs-lookup"><span data-stu-id="56a15-114">The tool can also be used to generate a class derived from the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext> class that acts as an entity container in the entity data model.</span></span> <span data-ttu-id="56a15-115">This service context provides the facilities for tracking changes and managing identities, concurrency, and relationships.</span><span class="sxs-lookup"><span data-stu-id="56a15-115">This service context provides the facilities for tracking changes and managing identities, concurrency, and relationships.</span></span> <span data-ttu-id="56a15-116">This class also exposes a <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext.SaveChanges> method that writes inserts, updates, and deletes records in [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="56a15-116">This class also exposes a <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext.SaveChanges> method that writes inserts, updates, and deletes records in [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span></span> <span data-ttu-id="56a15-117">For more information, see [Use the Organization Service Context Class](use-the-organizationservicecontext-class.md).</span><span class="sxs-lookup"><span data-stu-id="56a15-117">For more information, see [Use the Organization Service Context Class](use-the-organizationservicecontext-class.md).</span></span>  

<span data-ttu-id="56a15-118">The code generation tool takes several parameters that determine the contents of the file that is created.</span><span class="sxs-lookup"><span data-stu-id="56a15-118">The code generation tool takes several parameters that determine the contents of the file that is created.</span></span> <span data-ttu-id="56a15-119">The parameters can be passed in from the command line when you run the tool or in a .NET-connected application configuration file.</span><span class="sxs-lookup"><span data-stu-id="56a15-119">The parameters can be passed in from the command line when you run the tool or in a .NET-connected application configuration file.</span></span>  

<span data-ttu-id="56a15-120">The classes created by the code generation tool are designed to be built into a class library that can be referenced by projects that use [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="56a15-120">The classes created by the code generation tool are designed to be built into a class library that can be referenced by projects that use [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span></span> <span data-ttu-id="56a15-121">After you have generated the class file using the tool, you should add the file to your [!INCLUDE[pn_Visual_Studio_short](../../includes/pn-visual-studio-short.md)] project.</span><span class="sxs-lookup"><span data-stu-id="56a15-121">After you have generated the class file using the tool, you should add the file to your [!INCLUDE[pn_Visual_Studio_short](../../includes/pn-visual-studio-short.md)] project.</span></span> <span data-ttu-id="56a15-122">You must also add references to several assemblies that the generated classes are dependent upon.</span><span class="sxs-lookup"><span data-stu-id="56a15-122">You must also add references to several assemblies that the generated classes are dependent upon.</span></span>  

<span data-ttu-id="56a15-123">The following lists assemblies that must be referenced in your project when you use the generated code file.</span><span class="sxs-lookup"><span data-stu-id="56a15-123">The following lists assemblies that must be referenced in your project when you use the generated code file.</span></span>  

- <span data-ttu-id="56a15-124">Microsoft.Crm.Sdk.Proxy.dll</span><span class="sxs-lookup"><span data-stu-id="56a15-124">Microsoft.Crm.Sdk.Proxy.dll</span></span>  
- <span data-ttu-id="56a15-125">Microsoft.Xrm.Sdk.dll</span><span class="sxs-lookup"><span data-stu-id="56a15-125">Microsoft.Xrm.Sdk.dll</span></span>  

<span data-ttu-id="56a15-126">You can find these assemblies in the folder where you download the tools.</span><span class="sxs-lookup"><span data-stu-id="56a15-126">You can find these assemblies in the folder where you download the tools.</span></span>
<span data-ttu-id="56a15-127">Folder path: `<Download_directory>\tools\CoreTools`.</span><span class="sxs-lookup"><span data-stu-id="56a15-127">Folder path: `<Download_directory>\tools\CoreTools`.</span></span>
<span data-ttu-id="56a15-128">For example, if you download the tools in devtools folder on your D drive, you can find the assemblies in `D:\devtools\Tools\CoreTools`.</span><span class="sxs-lookup"><span data-stu-id="56a15-128">For example, if you download the tools in devtools folder on your D drive, you can find the assemblies in `D:\devtools\Tools\CoreTools`.</span></span>

<a name="bkmk_RuntheCodeGenerationUtility"></a>

## <a name="run-the-code-generation-tool"></a><span data-ttu-id="56a15-129">Run the code generation tool</span><span class="sxs-lookup"><span data-stu-id="56a15-129">Run the code generation tool</span></span>

<span data-ttu-id="56a15-130">Run the CrmSvcUtil.exe tool from the SDK\Bin folder.</span><span class="sxs-lookup"><span data-stu-id="56a15-130">Run the CrmSvcUtil.exe tool from the SDK\Bin folder.</span></span> <span data-ttu-id="56a15-131">If you run the tool from another folder location, make sure that a copy of the Microsoft.Xrm.Sdk.dll assembly is in that same folder.</span><span class="sxs-lookup"><span data-stu-id="56a15-131">If you run the tool from another folder location, make sure that a copy of the Microsoft.Xrm.Sdk.dll assembly is in that same folder.</span></span>  

<span data-ttu-id="56a15-132">The following sample shows the format for running the tool from the command line for an on-premises installation of [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="56a15-132">The following sample shows the format for running the tool from the command line for an on-premises installation of [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span></span> <span data-ttu-id="56a15-133">You supply the parameter values for your installation.</span><span class="sxs-lookup"><span data-stu-id="56a15-133">You supply the parameter values for your installation.</span></span>

```ms-dos
CrmSvcUtil.exe /url:http://<serverName>/<organizationName>/XRMServices/2011/Organization.svc    /out:<outputFilename>.cs /username:<username> /password:<password> /domain:<domainName>    /namespace:<outputNamespace> /serviceContextName:<serviceContextName>  
```

<span data-ttu-id="56a15-134">The following sample shows the format for running the tool from the command line with [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="56a15-134">The following sample shows the format for running the tool from the command line with [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] apps.</span></span> <span data-ttu-id="56a15-135">You supply the parameter values appropriate for your account and server.</span><span class="sxs-lookup"><span data-stu-id="56a15-135">You supply the parameter values appropriate for your account and server.</span></span>  

```ms-dos
CrmSvcUtil.exe /url:https://<organizationUrlName>.api.crm.dynamics.com/XRMServices/2011/Organization.svc    /out:<outputFilename>.cs /username:<username> /password:<password>     /namespace:<outputNamespace> /serviceContextName:<serviceContextName>  
```

<span data-ttu-id="56a15-136">For the `username` parameter, type the user name that is used to sign in to [!INCLUDE[pn_Windows_Live_ID](../../includes/pn-windows-live-id.md)] or [!INCLUDE[pn_MS_Office_365](../../includes/pn-ms-office-365.md)].</span><span class="sxs-lookup"><span data-stu-id="56a15-136">For the `username` parameter, type the user name that is used to sign in to [!INCLUDE[pn_Windows_Live_ID](../../includes/pn-windows-live-id.md)] or [!INCLUDE[pn_MS_Office_365](../../includes/pn-ms-office-365.md)].</span></span> <span data-ttu-id="56a15-137">You can look up the correct URL in the web application by selecting **Settings**, navigating to **Customizations**, and then choosing **Developer Resources**.</span><span class="sxs-lookup"><span data-stu-id="56a15-137">You can look up the correct URL in the web application by selecting **Settings**, navigating to **Customizations**, and then choosing **Developer Resources**.</span></span> <span data-ttu-id="56a15-138">The URL is shown under **Organization Service**.</span><span class="sxs-lookup"><span data-stu-id="56a15-138">The URL is shown under **Organization Service**.</span></span>  

<span data-ttu-id="56a15-139">To list the supported command-line parameters, use the following command.</span><span class="sxs-lookup"><span data-stu-id="56a15-139">To list the supported command-line parameters, use the following command.</span></span>

```ms-dos
CrmSvcUtil.exe /?  
```

> [!NOTE]
> <span data-ttu-id="56a15-140">When you run the tool against [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] apps using the [!INCLUDE[pn_Windows_Live_ID](../../includes/pn-windows-live-id.md)] identity provider, you no longer have to supply the `deviceid` and `devicepassword` parameters from the command line.</span><span class="sxs-lookup"><span data-stu-id="56a15-140">When you run the tool against [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] apps using the [!INCLUDE[pn_Windows_Live_ID](../../includes/pn-windows-live-id.md)] identity provider, you no longer have to supply the `deviceid` and `devicepassword` parameters from the command line.</span></span> <span data-ttu-id="56a15-141">The tool registers your device automatically.</span><span class="sxs-lookup"><span data-stu-id="56a15-141">The tool registers your device automatically.</span></span>

<a name="bkmk_parameters"></a>

## <a name="parameters"></a><span data-ttu-id="56a15-142">Tham số</span><span class="sxs-lookup"><span data-stu-id="56a15-142">Parameters</span></span>

<span data-ttu-id="56a15-143">The following table lists the code generation tool parameters and a gives a brief description of their use.</span><span class="sxs-lookup"><span data-stu-id="56a15-143">The following table lists the code generation tool parameters and a gives a brief description of their use.</span></span>  
  
|<span data-ttu-id="56a15-144">Tham số</span><span class="sxs-lookup"><span data-stu-id="56a15-144">Parameter</span></span>|<span data-ttu-id="56a15-145">Shortcut</span><span class="sxs-lookup"><span data-stu-id="56a15-145">Shortcut</span></span>|<span data-ttu-id="56a15-146">Mô tả</span><span class="sxs-lookup"><span data-stu-id="56a15-146">Description</span></span>|<span data-ttu-id="56a15-147">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="56a15-147">Required</span></span>|
|---------------|--------------|-----------------|--------------|
|<span data-ttu-id="56a15-148">deviceid</span><span class="sxs-lookup"><span data-stu-id="56a15-148">deviceid</span></span>|<span data-ttu-id="56a15-149">di</span><span class="sxs-lookup"><span data-stu-id="56a15-149">di</span></span>|<span data-ttu-id="56a15-150">No longer needed</span><span class="sxs-lookup"><span data-stu-id="56a15-150">No longer needed</span></span>|<span data-ttu-id="56a15-151">Sai</span><span class="sxs-lookup"><span data-stu-id="56a15-151">False</span></span>|
|<span data-ttu-id="56a15-152">devicepassword</span><span class="sxs-lookup"><span data-stu-id="56a15-152">devicepassword</span></span>|<span data-ttu-id="56a15-153">dp</span><span class="sxs-lookup"><span data-stu-id="56a15-153">dp</span></span>|<span data-ttu-id="56a15-154">No longer needed</span><span class="sxs-lookup"><span data-stu-id="56a15-154">No longer needed</span></span>|<span data-ttu-id="56a15-155">Sai</span><span class="sxs-lookup"><span data-stu-id="56a15-155">False</span></span>|
|<span data-ttu-id="56a15-156">domain</span><span class="sxs-lookup"><span data-stu-id="56a15-156">domain</span></span>|<span data-ttu-id="56a15-157">d</span><span class="sxs-lookup"><span data-stu-id="56a15-157">d</span></span>|<span data-ttu-id="56a15-158">The domain to authenticate against when you connect to the server.</span><span class="sxs-lookup"><span data-stu-id="56a15-158">The domain to authenticate against when you connect to the server.</span></span>|<span data-ttu-id="56a15-159">Sai</span><span class="sxs-lookup"><span data-stu-id="56a15-159">False</span></span>|
|<span data-ttu-id="56a15-160">url</span><span class="sxs-lookup"><span data-stu-id="56a15-160">url</span></span>||<span data-ttu-id="56a15-161">The URL for the Organization service.</span><span class="sxs-lookup"><span data-stu-id="56a15-161">The URL for the Organization service.</span></span>|<span data-ttu-id="56a15-162">Đúng</span><span class="sxs-lookup"><span data-stu-id="56a15-162">True</span></span>|
|<span data-ttu-id="56a15-163">out</span><span class="sxs-lookup"><span data-stu-id="56a15-163">out</span></span>|<span data-ttu-id="56a15-164">o</span><span class="sxs-lookup"><span data-stu-id="56a15-164">o</span></span>|<span data-ttu-id="56a15-165">The file name for the generated code.</span><span class="sxs-lookup"><span data-stu-id="56a15-165">The file name for the generated code.</span></span>|<span data-ttu-id="56a15-166">Đúng</span><span class="sxs-lookup"><span data-stu-id="56a15-166">True</span></span>|
|<span data-ttu-id="56a15-167">language</span><span class="sxs-lookup"><span data-stu-id="56a15-167">language</span></span>|<span data-ttu-id="56a15-168">l</span><span class="sxs-lookup"><span data-stu-id="56a15-168">l</span></span>|<span data-ttu-id="56a15-169">The language to generate the code in.</span><span class="sxs-lookup"><span data-stu-id="56a15-169">The language to generate the code in.</span></span> <span data-ttu-id="56a15-170">This can be either “CS” or “VB”.</span><span class="sxs-lookup"><span data-stu-id="56a15-170">This can be either “CS” or “VB”.</span></span> <span data-ttu-id="56a15-171">The default value is “CS”.</span><span class="sxs-lookup"><span data-stu-id="56a15-171">The default value is “CS”.</span></span>|<span data-ttu-id="56a15-172">Sai</span><span class="sxs-lookup"><span data-stu-id="56a15-172">False</span></span>|
|<span data-ttu-id="56a15-173">vùng tên</span><span class="sxs-lookup"><span data-stu-id="56a15-173">namespace</span></span>|<span data-ttu-id="56a15-174">n</span><span class="sxs-lookup"><span data-stu-id="56a15-174">n</span></span>|<span data-ttu-id="56a15-175">The namespace for the generated code.</span><span class="sxs-lookup"><span data-stu-id="56a15-175">The namespace for the generated code.</span></span> <span data-ttu-id="56a15-176">The default is the global namespace.</span><span class="sxs-lookup"><span data-stu-id="56a15-176">The default is the global namespace.</span></span>|<span data-ttu-id="56a15-177">Sai</span><span class="sxs-lookup"><span data-stu-id="56a15-177">False</span></span>|  
|<span data-ttu-id="56a15-178">username</span><span class="sxs-lookup"><span data-stu-id="56a15-178">username</span></span>|<span data-ttu-id="56a15-179">u</span><span class="sxs-lookup"><span data-stu-id="56a15-179">u</span></span>|<span data-ttu-id="56a15-180">The user name to use when you connect to the server for authentication.</span><span class="sxs-lookup"><span data-stu-id="56a15-180">The user name to use when you connect to the server for authentication.</span></span>|<span data-ttu-id="56a15-181">Sai</span><span class="sxs-lookup"><span data-stu-id="56a15-181">False</span></span>|  
|<span data-ttu-id="56a15-182">password</span><span class="sxs-lookup"><span data-stu-id="56a15-182">password</span></span>|<span data-ttu-id="56a15-183">p</span><span class="sxs-lookup"><span data-stu-id="56a15-183">p</span></span>|<span data-ttu-id="56a15-184">The password to use when you connect to the server for authentication.</span><span class="sxs-lookup"><span data-stu-id="56a15-184">The password to use when you connect to the server for authentication.</span></span>|<span data-ttu-id="56a15-185">Sai</span><span class="sxs-lookup"><span data-stu-id="56a15-185">False</span></span>|  
|<span data-ttu-id="56a15-186">servicecontextname</span><span class="sxs-lookup"><span data-stu-id="56a15-186">servicecontextname</span></span>||<span data-ttu-id="56a15-187">The name of the generated organization service context class.</span><span class="sxs-lookup"><span data-stu-id="56a15-187">The name of the generated organization service context class.</span></span> <span data-ttu-id="56a15-188">If no value is supplied, no service context is created.</span><span class="sxs-lookup"><span data-stu-id="56a15-188">If no value is supplied, no service context is created.</span></span>|<span data-ttu-id="56a15-189">Sai</span><span class="sxs-lookup"><span data-stu-id="56a15-189">False</span></span>|
|<span data-ttu-id="56a15-190">trợ giúp</span><span class="sxs-lookup"><span data-stu-id="56a15-190">help</span></span>|<span data-ttu-id="56a15-191">?</span><span class="sxs-lookup"><span data-stu-id="56a15-191">?</span></span>|<span data-ttu-id="56a15-192">Show usage information.</span><span class="sxs-lookup"><span data-stu-id="56a15-192">Show usage information.</span></span>|<span data-ttu-id="56a15-193">Sai</span><span class="sxs-lookup"><span data-stu-id="56a15-193">False</span></span>|
|<span data-ttu-id="56a15-194">nologo</span><span class="sxs-lookup"><span data-stu-id="56a15-194">nologo</span></span>||<span data-ttu-id="56a15-195">Suppress the banner at runtime.</span><span class="sxs-lookup"><span data-stu-id="56a15-195">Suppress the banner at runtime.</span></span>|<span data-ttu-id="56a15-196">Sai</span><span class="sxs-lookup"><span data-stu-id="56a15-196">False</span></span>|
|<span data-ttu-id="56a15-197">generateActions</span><span class="sxs-lookup"><span data-stu-id="56a15-197">generateActions</span></span>||<span data-ttu-id="56a15-198">Generate request and response classes for actions.</span><span class="sxs-lookup"><span data-stu-id="56a15-198">Generate request and response classes for actions.</span></span>||
|<span data-ttu-id="56a15-199">interactivelogin</span><span class="sxs-lookup"><span data-stu-id="56a15-199">interactivelogin</span></span>|<span data-ttu-id="56a15-200">il</span><span class="sxs-lookup"><span data-stu-id="56a15-200">il</span></span>|<span data-ttu-id="56a15-201">When set to **true**, a dialog to log into the Dynamics 365 for Customer Engagement apps service is displayed.</span><span class="sxs-lookup"><span data-stu-id="56a15-201">When set to **true**, a dialog to log into the Dynamics 365 for Customer Engagement apps service is displayed.</span></span> <span data-ttu-id="56a15-202">All other connection related parameters specified on the command line are   ignored.</span><span class="sxs-lookup"><span data-stu-id="56a15-202">All other connection related parameters specified on the command line are   ignored.</span></span>|<span data-ttu-id="56a15-203">Sai</span><span class="sxs-lookup"><span data-stu-id="56a15-203">False</span></span>|  
|<span data-ttu-id="56a15-204">connectionstring</span><span class="sxs-lookup"><span data-stu-id="56a15-204">connectionstring</span></span>|<span data-ttu-id="56a15-205">connstr</span><span class="sxs-lookup"><span data-stu-id="56a15-205">connstr</span></span>|<span data-ttu-id="56a15-206">Contains information, provided as a single string, for connecting to a Dynamics 365 for Customer Engagement apps organization.</span><span class="sxs-lookup"><span data-stu-id="56a15-206">Contains information, provided as a single string, for connecting to a Dynamics 365 for Customer Engagement apps organization.</span></span> <span data-ttu-id="56a15-207">All other connection related parameters specified on the command line are ignored.</span><span class="sxs-lookup"><span data-stu-id="56a15-207">All other connection related parameters specified on the command line are ignored.</span></span> <span data-ttu-id="56a15-208">For more information see [Use connection strings in XRM tooling to connect to Dynamics 365 for Customer Engagement apps](../xrm-tooling/use-connection-strings-xrm-tooling-connect.md).</span><span class="sxs-lookup"><span data-stu-id="56a15-208">For more information see [Use connection strings in XRM tooling to connect to Dynamics 365 for Customer Engagement apps](../xrm-tooling/use-connection-strings-xrm-tooling-connect.md).</span></span>|<span data-ttu-id="56a15-209">Sai</span><span class="sxs-lookup"><span data-stu-id="56a15-209">False</span></span>|

<a name="bkmk_examples"></a>

## <a name="usage-examples"></a><span data-ttu-id="56a15-210">Usage examples</span><span class="sxs-lookup"><span data-stu-id="56a15-210">Usage examples</span></span>

<span data-ttu-id="56a15-211">The following examples show how to use of the code generation tool from the command line for each deployment type.</span><span class="sxs-lookup"><span data-stu-id="56a15-211">The following examples show how to use of the code generation tool from the command line for each deployment type.</span></span> <span data-ttu-id="56a15-212">Note that user name and password are optional parameters.</span><span class="sxs-lookup"><span data-stu-id="56a15-212">Note that user name and password are optional parameters.</span></span> <span data-ttu-id="56a15-213">If your credentials for the target [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps server are stored in the [!INCLUDE[pn_ms_Windows_short](../../includes/pn-ms-windows-short.md)] credential vault, you do not have to provide them to run the code generation tool.</span><span class="sxs-lookup"><span data-stu-id="56a15-213">If your credentials for the target [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps server are stored in the [!INCLUDE[pn_ms_Windows_short](../../includes/pn-ms-windows-short.md)] credential vault, you do not have to provide them to run the code generation tool.</span></span>

### <a name="claims-authentication--active-directory"></a><span data-ttu-id="56a15-214">Claims authentication – Active Directory</span><span class="sxs-lookup"><span data-stu-id="56a15-214">Claims authentication – Active Directory</span></span>

<span data-ttu-id="56a15-215">The following sample shows how to run the code generation tool by using claims authentication in [!INCLUDE[pn_Active_Directory](../../includes/pn-active-directory.md)].</span><span class="sxs-lookup"><span data-stu-id="56a15-215">The following sample shows how to run the code generation tool by using claims authentication in [!INCLUDE[pn_Active_Directory](../../includes/pn-active-directory.md)].</span></span> <span data-ttu-id="56a15-216">Note the use of https because this sample server is using Transport Layer Security (TLS) or Secure Sockets Layer (SSL).</span><span class="sxs-lookup"><span data-stu-id="56a15-216">Note the use of https because this sample server is using Transport Layer Security (TLS) or Secure Sockets Layer (SSL).</span></span>  

```ms-dos  
CrmSvcUtil.exe /url:https://myport:555/MyOrg/XRMServices/2011/Organization.svc /out:GeneratedCode.cs /username:administrator /password:password
```

### <a name="dynamics-365-for-customer-engagement-online"></a><span data-ttu-id="56a15-217">Dynamics 365 for Customer Engagement (online)</span><span class="sxs-lookup"><span data-stu-id="56a15-217">Dynamics 365 for Customer Engagement (online)</span></span>

<span data-ttu-id="56a15-218">The following sample shows how to run the code generation tool for [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="56a15-218">The following sample shows how to run the code generation tool for [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] apps.</span></span> <span data-ttu-id="56a15-219">The first example is for the [!INCLUDE[pn_Windows_Live_ID](../../includes/pn-windows-live-id.md)] identity provider and the second is for the [!INCLUDE[pn_Office_365](../../includes/pn-office-365.md)] identity provider.</span><span class="sxs-lookup"><span data-stu-id="56a15-219">The first example is for the [!INCLUDE[pn_Windows_Live_ID](../../includes/pn-windows-live-id.md)] identity provider and the second is for the [!INCLUDE[pn_Office_365](../../includes/pn-office-365.md)] identity provider.</span></span>

```ms-dos
CrmSvcUtil.exe /url:https://myorg.api.crm.dynamics.com/XRMServices/2011/Organization.svc /out:GeneratedCode.cs /username:"myname@live.com" /password:"myp@ssword!"   
```

```ms-dos
CrmSvcUtil.exe /url:https://myorg.api.crm.dynamics.com/XRMServices/2011/Organization.svc /out:GeneratedCode.cs /username:"myname@myorg.onmicrosoft.com" /password:"myp@ssword!"   
```

### <a name="claims-authentication---ifd"></a><span data-ttu-id="56a15-220">Claims authentication - IFD</span><span class="sxs-lookup"><span data-stu-id="56a15-220">Claims authentication - IFD</span></span>

<span data-ttu-id="56a15-221">The following sample shows how to run the code generation tool using claims authentication.</span><span class="sxs-lookup"><span data-stu-id="56a15-221">The following sample shows how to run the code generation tool using claims authentication.</span></span>  

```ms-dos
CrmSvcUtil.exe /url:https://myorg.crm.com:555/XRMServices/2011/Organization.svc /out:GeneratedCode.cs /username:administrator /password:p@ssword!
```

<a name="bkmk_sampleconfig"></a>

## <a name="use-the-configuration-file"></a><span data-ttu-id="56a15-222">Use the configuration File</span><span class="sxs-lookup"><span data-stu-id="56a15-222">Use the configuration File</span></span>

<span data-ttu-id="56a15-223">The CrmSvcUtil.exe.config configuration file must be in the same folder as the CrmSvcUtil.exe tool.</span><span class="sxs-lookup"><span data-stu-id="56a15-223">The CrmSvcUtil.exe.config configuration file must be in the same folder as the CrmSvcUtil.exe tool.</span></span> <span data-ttu-id="56a15-224">The configuration file uses the standard key/value pairs in the `appSettings` section.</span><span class="sxs-lookup"><span data-stu-id="56a15-224">The configuration file uses the standard key/value pairs in the `appSettings` section.</span></span> <span data-ttu-id="56a15-225">However, if you enter a value at the command line, that value will be used instead of the one in the configuration file.</span><span class="sxs-lookup"><span data-stu-id="56a15-225">However, if you enter a value at the command line, that value will be used instead of the one in the configuration file.</span></span> <span data-ttu-id="56a15-226">Any key/value pairs found in the application configuration file that do not match any of the expected parameters are ignored.</span><span class="sxs-lookup"><span data-stu-id="56a15-226">Any key/value pairs found in the application configuration file that do not match any of the expected parameters are ignored.</span></span>  

<span data-ttu-id="56a15-227">Do not include the `url` and `namespace` parameters in the configuration file.</span><span class="sxs-lookup"><span data-stu-id="56a15-227">Do not include the `url` and `namespace` parameters in the configuration file.</span></span> <span data-ttu-id="56a15-228">These must be entered from the command line when the CrmSvcUtil.exe tool is being run.</span><span class="sxs-lookup"><span data-stu-id="56a15-228">These must be entered from the command line when the CrmSvcUtil.exe tool is being run.</span></span>  

<span data-ttu-id="56a15-229">The following sample shows how to configure the output file and the domain name parameters in the application configuration file using shortcut keys.</span><span class="sxs-lookup"><span data-stu-id="56a15-229">The following sample shows how to configure the output file and the domain name parameters in the application configuration file using shortcut keys.</span></span>  

```xml
<appSettings>    
    <add key="o" value="CrmProxy.cs"/>    
    <add key="d" value="mydomain"/>
</appSettings>  
```

<a name="bkmk_enabletrace"></a>

## <a name="enable-tracing"></a><span data-ttu-id="56a15-230">Enable tracing</span><span class="sxs-lookup"><span data-stu-id="56a15-230">Enable tracing</span></span>
 <span data-ttu-id="56a15-231">To enable tracing when you run the tool, add the following lines to the configuration file:</span><span class="sxs-lookup"><span data-stu-id="56a15-231">To enable tracing when you run the tool, add the following lines to the configuration file:</span></span>  

```xml
<system.diagnostics>   
   <trace autoflush="false" indentsize="4">   
      <listeners>   
         <add name="configConsoleListener" type="System.Diagnostics.ConsoleTraceListener">   
            <filter type="System.Diagnostics.EventTypeFilter" initializeData="Error" />   
         </add>   
      </listeners>   
   </trace>   
</system.diagnostics>  
```

<span data-ttu-id="56a15-232">For more information on supported tracing options see [Configure tracing for XRM tooling](../xrm-tooling/configure-tracing-xrm-tooling.md).</span><span class="sxs-lookup"><span data-stu-id="56a15-232">For more information on supported tracing options see [Configure tracing for XRM tooling](../xrm-tooling/configure-tracing-xrm-tooling.md).</span></span>  

## <a name="community-tools"></a><span data-ttu-id="56a15-233">Các công cụ dành cho cộng đồng</span><span class="sxs-lookup"><span data-stu-id="56a15-233">Community tools</span></span>

<span data-ttu-id="56a15-234">**Early Bound Generator** is a tool that XrmToolbox community developed for [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="56a15-234">**Early Bound Generator** is a tool that XrmToolbox community developed for [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps.</span></span> <span data-ttu-id="56a15-235">Vui lòng xem chủ đề [Công cụ dành cho nhà phát triển](../developer-tools.md) về các công cụ được cộng đồng phát triển.</span><span class="sxs-lookup"><span data-stu-id="56a15-235">Please see the [Developer tools](../developer-tools.md) topic for community developed tools.</span></span>

> [!NOTE]
> <span data-ttu-id="56a15-236">Các công cụ dành cho cộng đồng không phải là sản phẩm của [!include[pn_microsoft_dynamics](../../includes/pn-microsoft-dynamics.md)] và không mở rộng hỗ trợ đối với các công cụ dành cho cộng đồng.</span><span class="sxs-lookup"><span data-stu-id="56a15-236">The community tools are not a product of [!include[pn_microsoft_dynamics](../../includes/pn-microsoft-dynamics.md)] and does not extend support to the community tools.</span></span> <span data-ttu-id="56a15-237">Nếu bạn có các câu hỏi liên quan đến công cụ, vui lòng liên hệ với nhà xuất bản.</span><span class="sxs-lookup"><span data-stu-id="56a15-237">If you have questions pertaining to the tool, please contact the publisher.</span></span> <span data-ttu-id="56a15-238">Thông tin Khác: [XrmToolBox](https://www.xrmtoolbox.com).</span><span class="sxs-lookup"><span data-stu-id="56a15-238">More Information: [XrmToolBox](https://www.xrmtoolbox.com).</span></span> 


### <a name="see-also"></a><span data-ttu-id="56a15-239">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="56a15-239">See Also</span></span>

 [<span data-ttu-id="56a15-240">Developer Tools for Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="56a15-240">Developer Tools for Dynamics 365 for Customer Engagement apps</span></span>](../developer-tools.md)<br />
 [<span data-ttu-id="56a15-241">Browse the Metadata for Your Organization</span><span class="sxs-lookup"><span data-stu-id="56a15-241">Browse the Metadata for Your Organization</span></span>](../browse-your-metadata.md)<br />
 [<span data-ttu-id="56a15-242">Create an Extensions for the Code Generation Tool</span><span class="sxs-lookup"><span data-stu-id="56a15-242">Create an Extensions for the Code Generation Tool</span></span>](extend-code-generation-tool.md)<br />
 [<span data-ttu-id="56a15-243">Use the Early Bound Entity Classes for Create, Update and Delete</span><span class="sxs-lookup"><span data-stu-id="56a15-243">Use the Early Bound Entity Classes for Create, Update and Delete</span></span>](use-entity-class-create-update-delete.md)<br />
 [<span data-ttu-id="56a15-244">Troubleshooting Tips</span><span class="sxs-lookup"><span data-stu-id="56a15-244">Troubleshooting Tips</span></span>](troubleshooting-tips.md)<br />
 [<span data-ttu-id="56a15-245">Run a simple program using Customer Engagement web services</span><span class="sxs-lookup"><span data-stu-id="56a15-245">Run a simple program using Customer Engagement web services</span></span>](../simple-program-web-services.md)<br />
