---
title: Register and Deploy Plug-Ins (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn about programmatically register plug-ins and custom workflow activities with Dynamics 365 for Customer Engagement apps by writing registration code using certain SDK classes.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
f1_keywords:
- plugins
- plugin
ms.assetid: c3ee3447-ec0d-494e-8b35-4ec58ce93eea
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 390164280f1e3ccbc1b69a4f592a1bd72e8adff9
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385744"
---
# <a name="register-and-deploy-plug-ins"></a><span data-ttu-id="74897-103">Register and Deploy Plug-Ins</span><span class="sxs-lookup"><span data-stu-id="74897-103">Register and Deploy Plug-Ins</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="74897-104">Plug-ins and custom workflow activities are custom code that you develop to extend the existing functionality of [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="74897-104">Plug-ins and custom workflow activities are custom code that you develop to extend the existing functionality of [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps.</span></span> <span data-ttu-id="74897-105">Before a plug-in or custom workflow activity can be used, it must be registered with the server.</span><span class="sxs-lookup"><span data-stu-id="74897-105">Before a plug-in or custom workflow activity can be used, it must be registered with the server.</span></span> <span data-ttu-id="74897-106">You can programmatically register plug-ins and custom workflow activities with [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps by writing registration code using certain SDK classes.</span><span class="sxs-lookup"><span data-stu-id="74897-106">You can programmatically register plug-ins and custom workflow activities with [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps by writing registration code using certain SDK classes.</span></span> <span data-ttu-id="74897-107">However, to ease the learning curve and to speed up development and deployment of custom code, a plug-in and custom workflow activity registration tool is available for download.</span><span class="sxs-lookup"><span data-stu-id="74897-107">However, to ease the learning curve and to speed up development and deployment of custom code, a plug-in and custom workflow activity registration tool is available for download.</span></span>

<span data-ttu-id="74897-108">The plug-in and custom workflow activity registration tool is distributed as part of the [Microsoft.CrmSdk.XrmTooling.PluginRegistrationTool](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PluginRegistrationTool) NuGet package.</span><span class="sxs-lookup"><span data-stu-id="74897-108">The plug-in and custom workflow activity registration tool is distributed as part of the [Microsoft.CrmSdk.XrmTooling.PluginRegistrationTool](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PluginRegistrationTool) NuGet package.</span></span> <span data-ttu-id="74897-109">For information about downloading the tool, see [Download tools from NuGet](download-tools-NuGet.md).</span><span class="sxs-lookup"><span data-stu-id="74897-109">For information about downloading the tool, see [Download tools from NuGet](download-tools-NuGet.md).</span></span>

 <span data-ttu-id="74897-110">While this topic focuses primarily on plug-ins, most of the information is also applicable to custom workflow activities.</span><span class="sxs-lookup"><span data-stu-id="74897-110">While this topic focuses primarily on plug-ins, most of the information is also applicable to custom workflow activities.</span></span> <span data-ttu-id="74897-111">One difference between the two is that for custom workflow activity assemblies, you register just the assembly.</span><span class="sxs-lookup"><span data-stu-id="74897-111">One difference between the two is that for custom workflow activity assemblies, you register just the assembly.</span></span> <span data-ttu-id="74897-112">For plug-ins, you register the plug-in assembly and one or more steps per plug-in.</span><span class="sxs-lookup"><span data-stu-id="74897-112">For plug-ins, you register the plug-in assembly and one or more steps per plug-in.</span></span> <span data-ttu-id="74897-113">For more information about custom workflow activities, see [Custom Workflow Activities (Workflow Assemblies)](custom-workflow-activities-workflow-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="74897-113">For more information about custom workflow activities, see [Custom Workflow Activities (Workflow Assemblies)](custom-workflow-activities-workflow-assemblies.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="74897-114">Do not register any plug-in or custom workflow activity unless it is obtained from a reliable and trusted source.</span><span class="sxs-lookup"><span data-stu-id="74897-114">Do not register any plug-in or custom workflow activity unless it is obtained from a reliable and trusted source.</span></span>

 <span data-ttu-id="74897-115">For more information about how to package your plug-ins as solution components, see [Package and Distribute Extensions with Dynamics 365 for Customer Engagement apps Solutions](package-distribute-extensions-use-solutions.md).</span><span class="sxs-lookup"><span data-stu-id="74897-115">For more information about how to package your plug-ins as solution components, see [Package and Distribute Extensions with Dynamics 365 for Customer Engagement apps Solutions](package-distribute-extensions-use-solutions.md).</span></span> 

<a name="bkmk_pluginregistration"></a>

## <a name="plug-in-registration-tool"></a><span data-ttu-id="74897-116">Plug-in Registration Tool</span><span class="sxs-lookup"><span data-stu-id="74897-116">Plug-in Registration Tool</span></span>

 <span data-ttu-id="74897-117">The Plug-in Registration tool provides a graphical user interface and supports registering plug-ins and custom workflow activities with [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="74897-117">The Plug-in Registration tool provides a graphical user interface and supports registering plug-ins and custom workflow activities with [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps.</span></span> <span data-ttu-id="74897-118">However, plug-ins and custom workflow activities can only be registered in the sandbox (isolation mode) of [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="74897-118">However, plug-ins and custom workflow activities can only be registered in the sandbox (isolation mode) of [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)] apps.</span></span>

 <span data-ttu-id="74897-119">For more information about how to register and deploy a plug-in by using the tool, see [Walkthrough: Register a Plug-in using the Plug-in Registration Tool](walkthrough-register-plugin-using-plugin-registration-tool.md).</span><span class="sxs-lookup"><span data-stu-id="74897-119">For more information about how to register and deploy a plug-in by using the tool, see [Walkthrough: Register a Plug-in using the Plug-in Registration Tool](walkthrough-register-plugin-using-plugin-registration-tool.md).</span></span> <span data-ttu-id="74897-120">The tool can be added to the [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] **Tools** menu as an external tool to speed up the development process.</span><span class="sxs-lookup"><span data-stu-id="74897-120">The tool can be added to the [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] **Tools** menu as an external tool to speed up the development process.</span></span>

<a name="bkmk_pluginstor"></a>

## <a name="plug-in-storage"></a><span data-ttu-id="74897-121">Plug-in Storage</span><span class="sxs-lookup"><span data-stu-id="74897-121">Plug-in Storage</span></span>

[!INCLUDE[cc_sdk_onpremises_note](../includes/cc-sdk-onpremises-note.md)] 
<span data-ttu-id="74897-122">For an on-premises deployment, plug-ins that are not registered in the sandbox can be stored in the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps server's database or the *on-disk* file system.</span><span class="sxs-lookup"><span data-stu-id="74897-122">For an on-premises deployment, plug-ins that are not registered in the sandbox can be stored in the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps server's database or the *on-disk* file system.</span></span> <span data-ttu-id="74897-123">We strongly recommend that you store your production-ready plug-ins in the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps database, instead of on-disk.</span><span class="sxs-lookup"><span data-stu-id="74897-123">We strongly recommend that you store your production-ready plug-ins in the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps database, instead of on-disk.</span></span> <span data-ttu-id="74897-124">Plug-ins stored in the database are automatically distributed across multiple [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps servers in a data center cluster.</span><span class="sxs-lookup"><span data-stu-id="74897-124">Plug-ins stored in the database are automatically distributed across multiple [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps servers in a data center cluster.</span></span> <span data-ttu-id="74897-125">On-disk storage of plug-ins is useful for debugging plug-ins using [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)].</span><span class="sxs-lookup"><span data-stu-id="74897-125">On-disk storage of plug-ins is useful for debugging plug-ins using [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)].</span></span> <span data-ttu-id="74897-126">However, you can debug a plug-in that is stored in the database.</span><span class="sxs-lookup"><span data-stu-id="74897-126">However, you can debug a plug-in that is stored in the database.</span></span> <span data-ttu-id="74897-127">For more information, see [Debug a Plug-in](debug-plugin.md).</span><span class="sxs-lookup"><span data-stu-id="74897-127">For more information, see [Debug a Plug-in](debug-plugin.md).</span></span>  

<span data-ttu-id="74897-128">Plug-ins registered in the sandbox must be stored in the database regardless of the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps deployment (on-premises, IFD, or Online).</span><span class="sxs-lookup"><span data-stu-id="74897-128">Plug-ins registered in the sandbox must be stored in the database regardless of the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps deployment (on-premises, IFD, or Online).</span></span>

<a name="bkmk_deployment"></a>

## <a name="deployment"></a><span data-ttu-id="74897-129">Triển khai</span><span class="sxs-lookup"><span data-stu-id="74897-129">Deployment</span></span>

[!INCLUDE[cc_sdk_onpremises_note](../includes/cc-sdk-onpremises-note.md)] 
<span data-ttu-id="74897-130">For on-premises or Internet-facing (IFD) [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps installations, when you deploy plug-ins from another computer to the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps server disk (on-disk deployment), the plug-in assembly must be manually copied to the server before registration.</span><span class="sxs-lookup"><span data-stu-id="74897-130">For on-premises or Internet-facing (IFD) [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps installations, when you deploy plug-ins from another computer to the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps server disk (on-disk deployment), the plug-in assembly must be manually copied to the server before registration.</span></span> <span data-ttu-id="74897-131">The assembly must be deployed to the `<installdir>`\Program Files\Microsoft CRM\server\bin\assembly folder on each server where the plug-in is to execute.</span><span class="sxs-lookup"><span data-stu-id="74897-131">The assembly must be deployed to the `<installdir>`\Program Files\Microsoft CRM\server\bin\assembly folder on each server where the plug-in is to execute.</span></span>  

<span data-ttu-id="74897-132">Plug-in registration should be done after the assembly has been copied to the …\bin\assembly folder on the server to prevent the situation where a system user causes an event in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps to be raised but the registered plug-in assembly does not yet exist on the server.</span><span class="sxs-lookup"><span data-stu-id="74897-132">Plug-in registration should be done after the assembly has been copied to the …\bin\assembly folder on the server to prevent the situation where a system user causes an event in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps to be raised but the registered plug-in assembly does not yet exist on the server.</span></span> <span data-ttu-id="74897-133">For server database deployment, the plug-in assembly is automatically copied during plug-in registration so that the earlier situation is not an issue.</span><span class="sxs-lookup"><span data-stu-id="74897-133">For server database deployment, the plug-in assembly is automatically copied during plug-in registration so that the earlier situation is not an issue.</span></span>  

<span data-ttu-id="74897-134">Depending on your plug-in’s design, your plug-ins may require other referenced assemblies to run.</span><span class="sxs-lookup"><span data-stu-id="74897-134">Depending on your plug-in’s design, your plug-ins may require other referenced assemblies to run.</span></span> <span data-ttu-id="74897-135">Regardless of whether you deploy your plug-in to the database or disk, if your plug-in requires other assemblies to run, you must put copies of these assemblies in the global assembly cache on each server where the plug-in is to execute.</span><span class="sxs-lookup"><span data-stu-id="74897-135">Regardless of whether you deploy your plug-in to the database or disk, if your plug-in requires other assemblies to run, you must put copies of these assemblies in the global assembly cache on each server where the plug-in is to execute.</span></span> <span data-ttu-id="74897-136">This does not apply to a [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)] apps server because you do not have access to the global assembly cache on that server.</span><span class="sxs-lookup"><span data-stu-id="74897-136">This does not apply to a [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)] apps server because you do not have access to the global assembly cache on that server.</span></span>  

<span data-ttu-id="74897-137">**To move a plug-in from a development environment to a staging or production server**</span><span class="sxs-lookup"><span data-stu-id="74897-137">**To move a plug-in from a development environment to a staging or production server**</span></span>

1. <span data-ttu-id="74897-138">On the development computer, build the plug-in code.</span><span class="sxs-lookup"><span data-stu-id="74897-138">On the development computer, build the plug-in code.</span></span> <span data-ttu-id="74897-139">Do not include debug information.</span><span class="sxs-lookup"><span data-stu-id="74897-139">Do not include debug information.</span></span> <span data-ttu-id="74897-140">Optimize the plug-in for performance.</span><span class="sxs-lookup"><span data-stu-id="74897-140">Optimize the plug-in for performance.</span></span>
2. <span data-ttu-id="74897-141">Register the plug-in in the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps server database.</span><span class="sxs-lookup"><span data-stu-id="74897-141">Register the plug-in in the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps server database.</span></span>
3. <span data-ttu-id="74897-142">Using the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] web application, create a solution or use an existing one, and add the plug-in to that solution.</span><span class="sxs-lookup"><span data-stu-id="74897-142">Using the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] web application, create a solution or use an existing one, and add the plug-in to that solution.</span></span>
4. <span data-ttu-id="74897-143">After you have added any other desired components to the solution, export the solution.</span><span class="sxs-lookup"><span data-stu-id="74897-143">After you have added any other desired components to the solution, export the solution.</span></span>
5. <span data-ttu-id="74897-144">Import the solution on to the staging or production server.</span><span class="sxs-lookup"><span data-stu-id="74897-144">Import the solution on to the staging or production server.</span></span>

<a name="bkmk_versioning"></a>

## <a name="assembly-versioning-and-solutions"></a><span data-ttu-id="74897-145">Assembly Versioning and Solutions</span><span class="sxs-lookup"><span data-stu-id="74897-145">Assembly Versioning and Solutions</span></span>

<span data-ttu-id="74897-146">Plug-in assemblies can be versioned using a number format of *major.minor.build.revision* defined in the Assembly.info file of the [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)] project.</span><span class="sxs-lookup"><span data-stu-id="74897-146">Plug-in assemblies can be versioned using a number format of *major.minor.build.revision* defined in the Assembly.info file of the [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)] project.</span></span> <span data-ttu-id="74897-147">Depending on what part of the assembly version number is changed in a newer solution, the following behavior applies when an existing solution is updated through import.</span><span class="sxs-lookup"><span data-stu-id="74897-147">Depending on what part of the assembly version number is changed in a newer solution, the following behavior applies when an existing solution is updated through import.</span></span>

- <span data-ttu-id="74897-148">**The build or revision assembly version number is changed.**</span><span class="sxs-lookup"><span data-stu-id="74897-148">**The build or revision assembly version number is changed.**</span></span><br />
  <span data-ttu-id="74897-149">This is considered an in-place upgrade.</span><span class="sxs-lookup"><span data-stu-id="74897-149">This is considered an in-place upgrade.</span></span> <span data-ttu-id="74897-150">The older version of the assembly is removed when the solution containing the updated assembly is imported.</span><span class="sxs-lookup"><span data-stu-id="74897-150">The older version of the assembly is removed when the solution containing the updated assembly is imported.</span></span> <span data-ttu-id="74897-151">Any pre-existing steps from the older solution are automatically changed to refer to the newer version of the assembly.</span><span class="sxs-lookup"><span data-stu-id="74897-151">Any pre-existing steps from the older solution are automatically changed to refer to the newer version of the assembly.</span></span>  

- <span data-ttu-id="74897-152">**The major or minor assembly version number, except for the build or revision numbers, is changed.**</span><span class="sxs-lookup"><span data-stu-id="74897-152">**The major or minor assembly version number, except for the build or revision numbers, is changed.**</span></span><br />
  <span data-ttu-id="74897-153">When an updated solution containing the revised assembly is imported, the assembly is considered a completely different assembly than the previous version of that assembly in the existing solution.</span><span class="sxs-lookup"><span data-stu-id="74897-153">When an updated solution containing the revised assembly is imported, the assembly is considered a completely different assembly than the previous version of that assembly in the existing solution.</span></span> <span data-ttu-id="74897-154">Plug-in registration steps in the existing solution will continue to refer to the previous version of the assembly.</span><span class="sxs-lookup"><span data-stu-id="74897-154">Plug-in registration steps in the existing solution will continue to refer to the previous version of the assembly.</span></span> <span data-ttu-id="74897-155">If you want existing plug-in registration steps for the previous assembly to point to the revised assembly, you will need to use the Plug-in Registration tool to manually change the step configuration to refer to the revised assembly type.</span><span class="sxs-lookup"><span data-stu-id="74897-155">If you want existing plug-in registration steps for the previous assembly to point to the revised assembly, you will need to use the Plug-in Registration tool to manually change the step configuration to refer to the revised assembly type.</span></span> <span data-ttu-id="74897-156">This should be done before exporting the updated assembly into a solution for later import.</span><span class="sxs-lookup"><span data-stu-id="74897-156">This should be done before exporting the updated assembly into a solution for later import.</span></span>  

  <span data-ttu-id="74897-157">For more information about solutions, refer to [Introduction to Solutions](introduction-solutions.md).</span><span class="sxs-lookup"><span data-stu-id="74897-157">For more information about solutions, refer to [Introduction to Solutions](introduction-solutions.md).</span></span>

<a name="bkmk_securityrestrictions"></a>

## <a name="security-restrictions"></a><span data-ttu-id="74897-158">Security Restrictions</span><span class="sxs-lookup"><span data-stu-id="74897-158">Security Restrictions</span></span>

 <span data-ttu-id="74897-159">There is a security restriction that enables only privileged users to register plug-ins. For plug-ins that are not registered in isolation, the system user account under which the plug-in is being registered must exist in the **Deployment Administrators** group of Deployment Manager.</span><span class="sxs-lookup"><span data-stu-id="74897-159">There is a security restriction that enables only privileged users to register plug-ins. For plug-ins that are not registered in isolation, the system user account under which the plug-in is being registered must exist in the **Deployment Administrators** group of Deployment Manager.</span></span> <span data-ttu-id="74897-160">Only the System Administrator user account or any user account included in the **Deployment Administrators** group can run Deployment Manager.</span><span class="sxs-lookup"><span data-stu-id="74897-160">Only the System Administrator user account or any user account included in the **Deployment Administrators** group can run Deployment Manager.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="74897-161">For non-isolated plug-ins, failure to include the registering user account in the **Deployment Administrators** group results in an exception being thrown during plug-in registration.</span><span class="sxs-lookup"><span data-stu-id="74897-161">For non-isolated plug-ins, failure to include the registering user account in the **Deployment Administrators** group results in an exception being thrown during plug-in registration.</span></span> <span data-ttu-id="74897-162">The exception description states "Not have enough privilege to complete Create operation for an SDK entity."</span><span class="sxs-lookup"><span data-stu-id="74897-162">The exception description states "Not have enough privilege to complete Create operation for an SDK entity."</span></span>  

 <span data-ttu-id="74897-163">The system user account under which the plug-in is being registered must have the following organization-wide security privileges:</span><span class="sxs-lookup"><span data-stu-id="74897-163">The system user account under which the plug-in is being registered must have the following organization-wide security privileges:</span></span>
- <span data-ttu-id="74897-164">prvCreatePluginAssembly</span><span class="sxs-lookup"><span data-stu-id="74897-164">prvCreatePluginAssembly</span></span>
- <span data-ttu-id="74897-165">prvCreatePluginType</span><span class="sxs-lookup"><span data-stu-id="74897-165">prvCreatePluginType</span></span>
- <span data-ttu-id="74897-166">prvCreateSdkMessageProcessingStep</span><span class="sxs-lookup"><span data-stu-id="74897-166">prvCreateSdkMessageProcessingStep</span></span>
- <span data-ttu-id="74897-167">prvCreateSdkMessageProcessingStepImage</span><span class="sxs-lookup"><span data-stu-id="74897-167">prvCreateSdkMessageProcessingStepImage</span></span>
- <span data-ttu-id="74897-168">prvCreateSdkMessageProcessingStepSecureConfig</span><span class="sxs-lookup"><span data-stu-id="74897-168">prvCreateSdkMessageProcessingStepSecureConfig</span></span>

  <span data-ttu-id="74897-169">For more information, see [The Security Model of Dynamics 365 for Customer Engagement apps](security-dev/Security-model.md).</span><span class="sxs-lookup"><span data-stu-id="74897-169">For more information, see [The Security Model of Dynamics 365 for Customer Engagement apps](security-dev/Security-model.md).</span></span>  

  <span data-ttu-id="74897-170">For plug-ins registered in the sandbox (isolation mode), the system user account under which the plug-in is being registered must have the System Administrator role.</span><span class="sxs-lookup"><span data-stu-id="74897-170">For plug-ins registered in the sandbox (isolation mode), the system user account under which the plug-in is being registered must have the System Administrator role.</span></span> <span data-ttu-id="74897-171">Membership in the **Deployment Administrators** group is not required.</span><span class="sxs-lookup"><span data-stu-id="74897-171">Membership in the **Deployment Administrators** group is not required.</span></span>  
  
<a name="bkmk_registerprog"></a>

## <a name="register-plug-ins-programmatically"></a><span data-ttu-id="74897-172">Register Plug-ins Programmatically</span><span class="sxs-lookup"><span data-stu-id="74897-172">Register Plug-ins Programmatically</span></span>

 <span data-ttu-id="74897-173">The key entity types used to register plug-ins and images are:    `PluginAssembly`,    `PluginType`,  `SdkMessageProcessingStep`, and `SdkMessageProcessingStepImage`.</span><span class="sxs-lookup"><span data-stu-id="74897-173">The key entity types used to register plug-ins and images are:    `PluginAssembly`,    `PluginType`,  `SdkMessageProcessingStep`, and `SdkMessageProcessingStepImage`.</span></span> <span data-ttu-id="74897-174">The key entity types used to register custom workflow activities are `PluginAssembly` and `PluginType`.</span><span class="sxs-lookup"><span data-stu-id="74897-174">The key entity types used to register custom workflow activities are `PluginAssembly` and `PluginType`.</span></span> <span data-ttu-id="74897-175">Use these entities with the create, update, retrieve, and delete operations.</span><span class="sxs-lookup"><span data-stu-id="74897-175">Use these entities with the create, update, retrieve, and delete operations.</span></span>

 <span data-ttu-id="74897-176">For more information on images, see [Understand the Data Context Passed to a Plug-in](understand-data-context-passed-plugin.md).</span><span class="sxs-lookup"><span data-stu-id="74897-176">For more information on images, see [Understand the Data Context Passed to a Plug-in](understand-data-context-passed-plugin.md).</span></span>  

<a name="bkmk_enablecode"></a>

## <a name="enable-or-disable-custom-code-execution"></a><span data-ttu-id="74897-177">Enable or Disable Custom Code Execution</span><span class="sxs-lookup"><span data-stu-id="74897-177">Enable or Disable Custom Code Execution</span></span>

 <span data-ttu-id="74897-178">You can use [!INCLUDE[pn_PowerShell](../includes/pn-powershell.md)] to enable or disable custom code, including plug-ins and custom workflow activities, on the server as described here.</span><span class="sxs-lookup"><span data-stu-id="74897-178">You can use [!INCLUDE[pn_PowerShell](../includes/pn-powershell.md)] to enable or disable custom code, including plug-ins and custom workflow activities, on the server as described here.</span></span> <span data-ttu-id="74897-179">Alternatively, you can use the Deployment Web service.</span><span class="sxs-lookup"><span data-stu-id="74897-179">Alternatively, you can use the Deployment Web service.</span></span> <span data-ttu-id="74897-180">For more information, see [Deployment Entities and Deployment Configuration Settings](https://msdn.microsoft.com/library/gg328063.aspx) to set the `CustomCodeSettings`.<xref:Microsoft.Xrm.Sdk.Deployment.CustomCodeSettings.AllowExternalCode></span><span class="sxs-lookup"><span data-stu-id="74897-180">For more information, see [Deployment Entities and Deployment Configuration Settings](https://msdn.microsoft.com/library/gg328063.aspx) to set the `CustomCodeSettings`.<xref:Microsoft.Xrm.Sdk.Deployment.CustomCodeSettings.AllowExternalCode></span></span> <span data-ttu-id="74897-181">property.</span><span class="sxs-lookup"><span data-stu-id="74897-181">property.</span></span>

### <a name="to-enable-custom-code-execution"></a><span data-ttu-id="74897-182">To enable custom code execution</span><span class="sxs-lookup"><span data-stu-id="74897-182">To enable custom code execution</span></span>

1. <span data-ttu-id="74897-183">Mở cửa sổ lệnh [!INCLUDE[pn_PowerShell](../includes/pn-powershell.md)].</span><span class="sxs-lookup"><span data-stu-id="74897-183">Open a [!INCLUDE[pn_PowerShell](../includes/pn-powershell.md)] command window.</span></span>

2. <span data-ttu-id="74897-184">Add the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps PowerShell snap-in:</span><span class="sxs-lookup"><span data-stu-id="74897-184">Add the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps PowerShell snap-in:</span></span>

    ```powershell
    Add-PSSnapin Microsoft.Crm.PowerShell
    ```

3. <span data-ttu-id="74897-185">Retrieve the current setting:</span><span class="sxs-lookup"><span data-stu-id="74897-185">Retrieve the current setting:</span></span>

    ```powershell
    $setting = get-crmsetting customcodesettings
    ```

4. <span data-ttu-id="74897-186">Modify the current setting:</span><span class="sxs-lookup"><span data-stu-id="74897-186">Modify the current setting:</span></span>

    ```powershell
    $setting.AllowExternalCode="True"
    set-crmsetting $setting
    ```

5. <span data-ttu-id="74897-187">Verify the setting:</span><span class="sxs-lookup"><span data-stu-id="74897-187">Verify the setting:</span></span>

    ```powershell
    get-crmsetting customcodesettings
    ```

### <a name="to-disable-custom-code-execution"></a><span data-ttu-id="74897-188">To disable custom code execution</span><span class="sxs-lookup"><span data-stu-id="74897-188">To disable custom code execution</span></span>

1. <span data-ttu-id="74897-189">Open a [!INCLUDE[pn_PowerShell](../includes/pn-powershell.md)] command window.</span><span class="sxs-lookup"><span data-stu-id="74897-189">Open a [!INCLUDE[pn_PowerShell](../includes/pn-powershell.md)] command window.</span></span>
2. <span data-ttu-id="74897-190">Add the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps PowerShell snap-in:</span><span class="sxs-lookup"><span data-stu-id="74897-190">Add the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps PowerShell snap-in:</span></span>
    ```powershell
    Add-PSSnapin Microsoft.Crm.PowerShell
    ```
3. <span data-ttu-id="74897-191">Retrieve the current setting:</span><span class="sxs-lookup"><span data-stu-id="74897-191">Retrieve the current setting:</span></span>
    ```powershell
    $setting = get-crmsetting customcodesettings
    ```

4. <span data-ttu-id="74897-192">Modify the current setting:</span><span class="sxs-lookup"><span data-stu-id="74897-192">Modify the current setting:</span></span>
    ```powershell
    $setting.AllowExternalCode=0
    set-crmsetting $setting
    ```

5. <span data-ttu-id="74897-193">Verify the setting:</span><span class="sxs-lookup"><span data-stu-id="74897-193">Verify the setting:</span></span>
    ```powershell
    get-crmsetting customcodesettings
    ```

### <a name="see-also"></a><span data-ttu-id="74897-194">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="74897-194">See also</span></span>

 [<span data-ttu-id="74897-195">Plug-in Development</span><span class="sxs-lookup"><span data-stu-id="74897-195">Plug-in Development</span></span>](plugin-development.md)<br />
 [<span data-ttu-id="74897-196">Debug a Plug-in</span><span class="sxs-lookup"><span data-stu-id="74897-196">Debug a Plug-in</span></span>](debug-plugin.md)<br />
 [<span data-ttu-id="74897-197">Plug-in Isolation, Trust, and the Disallowed List</span><span class="sxs-lookup"><span data-stu-id="74897-197">Plug-in Isolation, Trust, and the Disallowed List</span></span>](plugin-isolation-trusts-statistics.md)<br />
 [<span data-ttu-id="74897-198">Package and Distribute Extensions with Dynamics 365 for Customer Engagement apps Solutions</span><span class="sxs-lookup"><span data-stu-id="74897-198">Package and Distribute Extensions with Dynamics 365 for Customer Engagement apps Solutions</span></span>](package-distribute-extensions-use-solutions.md)<br />
