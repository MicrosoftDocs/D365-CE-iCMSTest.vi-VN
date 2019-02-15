---
title: Create extensions for the code generation tool | MicrosoftDocs
description: You can extend the functionality of the code generation tool by specifying additional command-line parameters and parameter values.
keywords: ''
ms.date: 10/31/2017
ms.service: crm-online
ms.custom: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
- Dynamics 365 for Customer Engagement (on-premises)
- Dynamics CRM 2016
- Dynamics CRM Online
author: JimDaly
ms.assetid: 00533626-2587-4bb2-ad82-98560024794e
ms.author: jdaly
manager: jdaly
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: f90a75940546614ed0c058efe00d80bfa52956b0
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387789"
---
# <a name="create-extensions-for-the-code-generation-tool"></a><span data-ttu-id="071f6-103">Create extensions for the code generation tool</span><span class="sxs-lookup"><span data-stu-id="071f6-103">Create extensions for the code generation tool</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="071f6-104">You can extend the functionality of the code generation tool by specifying additional command-line parameters and parameter values.</span><span class="sxs-lookup"><span data-stu-id="071f6-104">You can extend the functionality of the code generation tool by specifying additional command-line parameters and parameter values.</span></span> <span data-ttu-id="071f6-105">To specify a parameter, add the following to the command line: /\<*parametername*>:\<*class name*>,\<*assembly name*>.</span><span class="sxs-lookup"><span data-stu-id="071f6-105">To specify a parameter, add the following to the command line: /\<*parametername*>:\<*class name*>,\<*assembly name*>.</span></span> <span data-ttu-id="071f6-106">Note that assembly name does not include the .dll extension.</span><span class="sxs-lookup"><span data-stu-id="071f6-106">Note that assembly name does not include the .dll extension.</span></span> <span data-ttu-id="071f6-107">As an alternative, you can add the equivalent value to the config file in the format “<add key=”\<*parametername*>” value=”\<*class name*>,\<*assembly name*>” />”.</span><span class="sxs-lookup"><span data-stu-id="071f6-107">As an alternative, you can add the equivalent value to the config file in the format “<add key=”\<*parametername*>” value=”\<*class name*>,\<*assembly name*>” />”.</span></span>  

<span data-ttu-id="071f6-108">The following table lists the parameters that you can use.</span><span class="sxs-lookup"><span data-stu-id="071f6-108">The following table lists the parameters that you can use.</span></span>  

|<span data-ttu-id="071f6-109">Parameter name</span><span class="sxs-lookup"><span data-stu-id="071f6-109">Parameter name</span></span>|<span data-ttu-id="071f6-110">Interface Name</span><span class="sxs-lookup"><span data-stu-id="071f6-110">Interface Name</span></span>|<span data-ttu-id="071f6-111">Mô tả</span><span class="sxs-lookup"><span data-stu-id="071f6-111">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="071f6-112">/codecustomization</span><span class="sxs-lookup"><span data-stu-id="071f6-112">/codecustomization</span></span>|<span data-ttu-id="071f6-113">ICustomizeCodeDomService</span><span class="sxs-lookup"><span data-stu-id="071f6-113">ICustomizeCodeDomService</span></span>|<span data-ttu-id="071f6-114">Called after the CodeDOM generation has been completed, assuming the default instance of `ICodeGenerationService`.</span><span class="sxs-lookup"><span data-stu-id="071f6-114">Called after the CodeDOM generation has been completed, assuming the default instance of `ICodeGenerationService`.</span></span> <span data-ttu-id="071f6-115">It is useful for generating additional classes, such as the constants in picklists.</span><span class="sxs-lookup"><span data-stu-id="071f6-115">It is useful for generating additional classes, such as the constants in picklists.</span></span>|  
|<span data-ttu-id="071f6-116">/codewriterfilter</span><span class="sxs-lookup"><span data-stu-id="071f6-116">/codewriterfilter</span></span>|<span data-ttu-id="071f6-117">ICodeWriterFilterService</span><span class="sxs-lookup"><span data-stu-id="071f6-117">ICodeWriterFilterService</span></span>|<span data-ttu-id="071f6-118">Called during the process of CodeDOM generation, assuming the default instance of `ICodeGenerationService`, to determine whether a specific object or property should be generated.</span><span class="sxs-lookup"><span data-stu-id="071f6-118">Called during the process of CodeDOM generation, assuming the default instance of `ICodeGenerationService`, to determine whether a specific object or property should be generated.</span></span>|  
|<span data-ttu-id="071f6-119">/codewritermessagefilter</span><span class="sxs-lookup"><span data-stu-id="071f6-119">/codewritermessagefilter</span></span>|<span data-ttu-id="071f6-120">ICodeWriterMessageFilterService</span><span class="sxs-lookup"><span data-stu-id="071f6-120">ICodeWriterMessageFilterService</span></span>|<span data-ttu-id="071f6-121">Called during the process of CodeDOM generation, assuming the default instance of `ICodeGenerationService`, to determine whether a specific message should be generated.</span><span class="sxs-lookup"><span data-stu-id="071f6-121">Called during the process of CodeDOM generation, assuming the default instance of `ICodeGenerationService`, to determine whether a specific message should be generated.</span></span> <span data-ttu-id="071f6-122">This should not be used for requests/responses as these are already generated in Microsoft.Crm.Sdk.Proxy.dll and Microsoft.Xrm.Sdk.dll.</span><span class="sxs-lookup"><span data-stu-id="071f6-122">This should not be used for requests/responses as these are already generated in Microsoft.Crm.Sdk.Proxy.dll and Microsoft.Xrm.Sdk.dll.</span></span>|  
|<span data-ttu-id="071f6-123">/metadataproviderservice</span><span class="sxs-lookup"><span data-stu-id="071f6-123">/metadataproviderservice</span></span>|<span data-ttu-id="071f6-124">IMetadataProviderService</span><span class="sxs-lookup"><span data-stu-id="071f6-124">IMetadataProviderService</span></span>|<span data-ttu-id="071f6-125">Called to retrieve the metadata from the server.</span><span class="sxs-lookup"><span data-stu-id="071f6-125">Called to retrieve the metadata from the server.</span></span> <span data-ttu-id="071f6-126">This may be called multiple times during the generation process, so the data should be cached.</span><span class="sxs-lookup"><span data-stu-id="071f6-126">This may be called multiple times during the generation process, so the data should be cached.</span></span>|  
|<span data-ttu-id="071f6-127">/codegenerationservice</span><span class="sxs-lookup"><span data-stu-id="071f6-127">/codegenerationservice</span></span>|<span data-ttu-id="071f6-128">ICodeGenerationService</span><span class="sxs-lookup"><span data-stu-id="071f6-128">ICodeGenerationService</span></span>|<span data-ttu-id="071f6-129">Core implementation of the CodeDOM generation.</span><span class="sxs-lookup"><span data-stu-id="071f6-129">Core implementation of the CodeDOM generation.</span></span> <span data-ttu-id="071f6-130">If this is changed, the other extensions may not behave in the manner described.</span><span class="sxs-lookup"><span data-stu-id="071f6-130">If this is changed, the other extensions may not behave in the manner described.</span></span>|  
|<span data-ttu-id="071f6-131">/namingservice</span><span class="sxs-lookup"><span data-stu-id="071f6-131">/namingservice</span></span>|<span data-ttu-id="071f6-132">INamingService</span><span class="sxs-lookup"><span data-stu-id="071f6-132">INamingService</span></span>|<span data-ttu-id="071f6-133">Called during the CodeDOM generation to determine the name for objects, assuming the default implementation.</span><span class="sxs-lookup"><span data-stu-id="071f6-133">Called during the CodeDOM generation to determine the name for objects, assuming the default implementation.</span></span>|

<span data-ttu-id="071f6-134">The implementation of these interfaces must have one of the following constructors:</span><span class="sxs-lookup"><span data-stu-id="071f6-134">The implementation of these interfaces must have one of the following constructors:</span></span>

<span data-ttu-id="071f6-135">`MyNamingService`()</span><span class="sxs-lookup"><span data-stu-id="071f6-135">`MyNamingService`()</span></span><br />
<span data-ttu-id="071f6-136">`MyNamingService`(`INamingService``defaultService`)</span><span class="sxs-lookup"><span data-stu-id="071f6-136">`MyNamingService`(`INamingService``defaultService`)</span></span><br />
<span data-ttu-id="071f6-137">`MyNamingService`(`IDictionary`<`string`, `string`> `parameters`)</span><span class="sxs-lookup"><span data-stu-id="071f6-137">`MyNamingService`(`IDictionary`<`string`, `string`> `parameters`)</span></span><br />
<span data-ttu-id="071f6-138">`MyNamingService`(`INamingService``defaultService`, `IDictionary`<`string`, `string`> `parameters`)</span><span class="sxs-lookup"><span data-stu-id="071f6-138">`MyNamingService`(`INamingService``defaultService`, `IDictionary`<`string`, `string`> `parameters`)</span></span>

<span data-ttu-id="071f6-139">The `Microsoft.Crm.Services.Utility` namespace is defined in CrmSvcUtil.exe.</span><span class="sxs-lookup"><span data-stu-id="071f6-139">The `Microsoft.Crm.Services.Utility` namespace is defined in CrmSvcUtil.exe.</span></span> <span data-ttu-id="071f6-140">Add a reference to CrmSvcUtil.exe in your [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)] code generation tool extension projects.</span><span class="sxs-lookup"><span data-stu-id="071f6-140">Add a reference to CrmSvcUtil.exe in your [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)] code generation tool extension projects.</span></span>

<a name="Generate_Enums"></a>

## <a name="sample-extension-to-generate-enumerations-for-option-sets"></a><span data-ttu-id="071f6-141">Sample extension to generate enumerations for option sets</span><span class="sxs-lookup"><span data-stu-id="071f6-141">Sample extension to generate enumerations for option sets</span></span>

<span data-ttu-id="071f6-142">The following sample code demonstrates how to write an extension.</span><span class="sxs-lookup"><span data-stu-id="071f6-142">The following sample code demonstrates how to write an extension.</span></span>  

[!code-csharp[CrmSvcUtilExtensions#BasicFilteringService](../../snippets/csharp/CRMV8/crmsvcutilextensions/cs/basicfilteringservice.cs#basicfilteringservice)]  

<span data-ttu-id="071f6-143">Download the sample: [CrmSvcUtilExtensions](https://code.msdn.microsoft.com/Create-extensions-for-the-b8b24d1d) and  [GeneratePickListEnums](https://code.msdn.microsoft.com/Create-extensions-for-the-3dd56a27).</span><span class="sxs-lookup"><span data-stu-id="071f6-143">Download the sample: [CrmSvcUtilExtensions](https://code.msdn.microsoft.com/Create-extensions-for-the-b8b24d1d) and  [GeneratePickListEnums](https://code.msdn.microsoft.com/Create-extensions-for-the-3dd56a27).</span></span> 

<span data-ttu-id="071f6-144">The **GeneratePicklistEnums** sample extension outputs a source code file that contains enumerations for all option sets, state codes, and status codes.</span><span class="sxs-lookup"><span data-stu-id="071f6-144">The **GeneratePicklistEnums** sample extension outputs a source code file that contains enumerations for all option sets, state codes, and status codes.</span></span> <span data-ttu-id="071f6-145">For an example of how to use these enumerations, see the `SampleCode\CS\QuickStart` sample.</span><span class="sxs-lookup"><span data-stu-id="071f6-145">For an example of how to use these enumerations, see the `SampleCode\CS\QuickStart` sample.</span></span>  

### <a name="see-also"></a><span data-ttu-id="071f6-146">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="071f6-146">See Also</span></span>

 [<span data-ttu-id="071f6-147">Create Early-Bound Entity Classes with the Code Generation Tool (CrmSvcUtil.exe)</span><span class="sxs-lookup"><span data-stu-id="071f6-147">Create Early-Bound Entity Classes with the Code Generation Tool (CrmSvcUtil.exe)</span></span>](create-early-bound-entity-classes-code-generation-tool.md)<br />
 [<span data-ttu-id="071f6-148">Use the Early Bound Entity Classes for Create, Update and Delete</span><span class="sxs-lookup"><span data-stu-id="071f6-148">Use the Early Bound Entity Classes for Create, Update and Delete</span></span>](use-entity-class-create-update-delete.md)<br />
 [<span data-ttu-id="071f6-149">Troubleshooting Tips</span><span class="sxs-lookup"><span data-stu-id="071f6-149">Troubleshooting Tips</span></span>](troubleshooting-tips.md)<br />
 [<span data-ttu-id="071f6-150">Run a simple program using Customer Engagement web services</span><span class="sxs-lookup"><span data-stu-id="071f6-150">Run a simple program using Customer Engagement web services</span></span>](../simple-program-web-services.md)
