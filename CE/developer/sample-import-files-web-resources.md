---
title: 'Sample: Import files as web resources (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: The sample provides a simplified example of importing files as web resources.
keywords: ''
ms.date: 10/31/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 0f9bca5b-b876-4f68-8e4e-e844da8598d6
author: JimDaly
ms.author: jdaly
manager: jdaly
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
caps.latest.revision: 19
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 6de9168d529ca9ba937d6df886671388cf9d509e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386544"
---
# <a name="sample-import-files-as-web-resources"></a><span data-ttu-id="d0ddd-103">Sample: Import files as web resources</span><span class="sxs-lookup"><span data-stu-id="d0ddd-103">Sample: Import files as web resources</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="d0ddd-104">When you develop a large number of files to use as Web resources you can save yourself the work of manually adding them through the application.</span><span class="sxs-lookup"><span data-stu-id="d0ddd-104">When you develop a large number of files to use as Web resources you can save yourself the work of manually adding them through the application.</span></span> <span data-ttu-id="d0ddd-105">Many Web resources can be developed and tested outside of [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] and then imported.</span><span class="sxs-lookup"><span data-stu-id="d0ddd-105">Many Web resources can be developed and tested outside of [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] and then imported.</span></span>  
  
 <span data-ttu-id="d0ddd-106">This sample provides a simplified example of this process.</span><span class="sxs-lookup"><span data-stu-id="d0ddd-106">This sample provides a simplified example of this process.</span></span> <span data-ttu-id="d0ddd-107">For a more complex sample that provides a WPF application you can use to import Web resources, see the [Sample: Web Resource Utility](sample-web-resource-utility.md).</span><span class="sxs-lookup"><span data-stu-id="d0ddd-107">For a more complex sample that provides a WPF application you can use to import Web resources, see the [Sample: Web Resource Utility](sample-web-resource-utility.md).</span></span>  
    
 <!--[!INCLUDE[pn-crm-2015-and-online-full](../includes/pn-crm-2015-and-online-full.md)] -->
<!-- [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] -->
 
 <span data-ttu-id="d0ddd-108">Download the sample: [Import files as web resources](https://code.msdn.microsoft.com/Import-files-as-web-f84ad8dc).</span><span class="sxs-lookup"><span data-stu-id="d0ddd-108">Download the sample: [Import files as web resources](https://code.msdn.microsoft.com/Import-files-as-web-f84ad8dc).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="d0ddd-109">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="d0ddd-109">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="d0ddd-110">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="d0ddd-110">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
 <span data-ttu-id="d0ddd-111">The sample code included in the SDK download package includes the following files required by this sample:</span><span class="sxs-lookup"><span data-stu-id="d0ddd-111">The sample code included in the SDK download package includes the following files required by this sample:</span></span>  
  
 <span data-ttu-id="d0ddd-112">**ImportJob.xml**</span><span class="sxs-lookup"><span data-stu-id="d0ddd-112">**ImportJob.xml**</span></span>  
 <span data-ttu-id="d0ddd-113">This file provides data about the Web Resource records that will be created.</span><span class="sxs-lookup"><span data-stu-id="d0ddd-113">This file provides data about the Web Resource records that will be created.</span></span> <span data-ttu-id="d0ddd-114">For each file it contains the following data:</span><span class="sxs-lookup"><span data-stu-id="d0ddd-114">For each file it contains the following data:</span></span>  
  
- <span data-ttu-id="d0ddd-115">**path:** The path to each file from the FilesToImport folder.</span><span class="sxs-lookup"><span data-stu-id="d0ddd-115">**path:** The path to each file from the FilesToImport folder.</span></span>  
  
- <span data-ttu-id="d0ddd-116">**displayName:** The display name for the Web resource.</span><span class="sxs-lookup"><span data-stu-id="d0ddd-116">**displayName:** The display name for the Web resource.</span></span>  
  
- <span data-ttu-id="d0ddd-117">**description:** A description of what each file does.</span><span class="sxs-lookup"><span data-stu-id="d0ddd-117">**description:** A description of what each file does.</span></span>  
  
- <span data-ttu-id="d0ddd-118">**name:** The name that will be used for the Web Resource.</span><span class="sxs-lookup"><span data-stu-id="d0ddd-118">**name:** The name that will be used for the Web Resource.</span></span>  
  
  > [!NOTE]
  > - <span data-ttu-id="d0ddd-119">Each of these names begin with an underscore character.</span><span class="sxs-lookup"><span data-stu-id="d0ddd-119">Each of these names begin with an underscore character.</span></span> <span data-ttu-id="d0ddd-120">The customization prefix of the solution publisher will be prepended to the name when the Web resource is created.</span><span class="sxs-lookup"><span data-stu-id="d0ddd-120">The customization prefix of the solution publisher will be prepended to the name when the Web resource is created.</span></span> <span data-ttu-id="d0ddd-121">Rather than hard-coding a specific customization prefix, this sample will detect the current customization prefix for a publisher record that may already exist in the organization.</span><span class="sxs-lookup"><span data-stu-id="d0ddd-121">Rather than hard-coding a specific customization prefix, this sample will detect the current customization prefix for a publisher record that may already exist in the organization.</span></span>  
  >   - <span data-ttu-id="d0ddd-122">Because each of these files was developed outside of [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] and depend on relative paths to access each other, the names include backslash “/” characters to create a virtual folder structure so the relative links will continue to function within [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].</span><span class="sxs-lookup"><span data-stu-id="d0ddd-122">Because each of these files was developed outside of [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] and depend on relative paths to access each other, the names include backslash “/” characters to create a virtual folder structure so the relative links will continue to function within [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].</span></span>  
  
- <span data-ttu-id="d0ddd-123">**type:** Specifies the type of Web Resource to create using the integer values found in [Web Resource Types](web-resources.md#BKMK_WebResourceTypes).</span><span class="sxs-lookup"><span data-stu-id="d0ddd-123">**type:** Specifies the type of Web Resource to create using the integer values found in [Web Resource Types](web-resources.md#BKMK_WebResourceTypes).</span></span>
  
  <span data-ttu-id="d0ddd-124">**FilesToImport/ShowData.htm**</span><span class="sxs-lookup"><span data-stu-id="d0ddd-124">**FilesToImport/ShowData.htm**</span></span>  
  <span data-ttu-id="d0ddd-125">This HTML Web resource requires each of the other files to display the following table.</span><span class="sxs-lookup"><span data-stu-id="d0ddd-125">This HTML Web resource requires each of the other files to display the following table.</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="d0ddd-126">**Tên**</span><span class="sxs-lookup"><span data-stu-id="d0ddd-126">**First Name**</span></span>|<span data-ttu-id="d0ddd-127">**Họ**</span><span class="sxs-lookup"><span data-stu-id="d0ddd-127">**Last Name**</span></span>|  
|<span data-ttu-id="d0ddd-128">Apurva</span><span class="sxs-lookup"><span data-stu-id="d0ddd-128">Apurva</span></span>|<span data-ttu-id="d0ddd-129">Dalia</span><span class="sxs-lookup"><span data-stu-id="d0ddd-129">Dalia</span></span>|  
|<span data-ttu-id="d0ddd-130">Ofer</span><span class="sxs-lookup"><span data-stu-id="d0ddd-130">Ofer</span></span>|<span data-ttu-id="d0ddd-131">Daliot</span><span class="sxs-lookup"><span data-stu-id="d0ddd-131">Daliot</span></span>|  
|<span data-ttu-id="d0ddd-132">Jim</span><span class="sxs-lookup"><span data-stu-id="d0ddd-132">Jim</span></span>|<span data-ttu-id="d0ddd-133">Daly</span><span class="sxs-lookup"><span data-stu-id="d0ddd-133">Daly</span></span>|  
|<span data-ttu-id="d0ddd-134">Ryan</span><span class="sxs-lookup"><span data-stu-id="d0ddd-134">Ryan</span></span>|<span data-ttu-id="d0ddd-135">Danner</span><span class="sxs-lookup"><span data-stu-id="d0ddd-135">Danner</span></span>|  
|<span data-ttu-id="d0ddd-136">Mike</span><span class="sxs-lookup"><span data-stu-id="d0ddd-136">Mike</span></span>|<span data-ttu-id="d0ddd-137">Danseglio</span><span class="sxs-lookup"><span data-stu-id="d0ddd-137">Danseglio</span></span>|  
|<span data-ttu-id="d0ddd-138">Alex</span><span class="sxs-lookup"><span data-stu-id="d0ddd-138">Alex</span></span>|<span data-ttu-id="d0ddd-139">Darrow</span><span class="sxs-lookup"><span data-stu-id="d0ddd-139">Darrow</span></span>|  
  
 <span data-ttu-id="d0ddd-140">**FilesToImport/CSS/Styles.css**</span><span class="sxs-lookup"><span data-stu-id="d0ddd-140">**FilesToImport/CSS/Styles.css**</span></span>  
 <span data-ttu-id="d0ddd-141">This file provides the CSS Styles used in ShowData.htm.</span><span class="sxs-lookup"><span data-stu-id="d0ddd-141">This file provides the CSS Styles used in ShowData.htm.</span></span>  
  
 <span data-ttu-id="d0ddd-142">**FilesToImport/Data/Data.xml**</span><span class="sxs-lookup"><span data-stu-id="d0ddd-142">**FilesToImport/Data/Data.xml**</span></span>  
 <span data-ttu-id="d0ddd-143">This file contains the list of names that is displayed in the table.</span><span class="sxs-lookup"><span data-stu-id="d0ddd-143">This file contains the list of names that is displayed in the table.</span></span>  
  
 <span data-ttu-id="d0ddd-144">**FilesToImport/Script/Script.js**</span><span class="sxs-lookup"><span data-stu-id="d0ddd-144">**FilesToImport/Script/Script.js**</span></span>  
 <span data-ttu-id="d0ddd-145">This file contains a JScript library that contains information about the relative location of the Data.xml file and the Transform.xslt file.</span><span class="sxs-lookup"><span data-stu-id="d0ddd-145">This file contains a JScript library that contains information about the relative location of the Data.xml file and the Transform.xslt file.</span></span> <span data-ttu-id="d0ddd-146">It also contains the `showData` function that transforms the data and adds it to the ShowData.htm page.</span><span class="sxs-lookup"><span data-stu-id="d0ddd-146">It also contains the `showData` function that transforms the data and adds it to the ShowData.htm page.</span></span>  
  
 <span data-ttu-id="d0ddd-147">**FilesToImport/XSL/Transform.xslt**</span><span class="sxs-lookup"><span data-stu-id="d0ddd-147">**FilesToImport/XSL/Transform.xslt**</span></span>  
 <span data-ttu-id="d0ddd-148">This file contains the XSL definition of how to transform the data into an HTML table.</span><span class="sxs-lookup"><span data-stu-id="d0ddd-148">This file contains the XSL definition of how to transform the data into an HTML table.</span></span>  
  
## <a name="demonstrates"></a><span data-ttu-id="d0ddd-149">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="d0ddd-149">Demonstrates</span></span>  
  
### <a name="creating-web-resources-in-the-context-of-a-solution"></a><span data-ttu-id="d0ddd-150">Creating Web Resources in the Context of a Solution</span><span class="sxs-lookup"><span data-stu-id="d0ddd-150">Creating Web Resources in the Context of a Solution</span></span>  
 <span data-ttu-id="d0ddd-151">Web Resources are organization-owned records so they can be created using either the<xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*></span><span class="sxs-lookup"><span data-stu-id="d0ddd-151">Web Resources are organization-owned records so they can be created using either the<xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*></span></span> <span data-ttu-id="d0ddd-152">method or by using the <xref:Microsoft.Xrm.Sdk.Messages.CreateRequest> message and the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Execute*></span><span class="sxs-lookup"><span data-stu-id="d0ddd-152">method or by using the <xref:Microsoft.Xrm.Sdk.Messages.CreateRequest> message and the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Execute*></span></span> <span data-ttu-id="d0ddd-153">method.</span><span class="sxs-lookup"><span data-stu-id="d0ddd-153">method.</span></span> <span data-ttu-id="d0ddd-154">This sample will show how to use the `SolutionUniqueName` optional parameter to associate a Web resource with a specific solution when it is created.</span><span class="sxs-lookup"><span data-stu-id="d0ddd-154">This sample will show how to use the `SolutionUniqueName` optional parameter to associate a Web resource with a specific solution when it is created.</span></span> <span data-ttu-id="d0ddd-155">This requires using the <xref:Microsoft.Xrm.Sdk.Messages.CreateRequest> message.</span><span class="sxs-lookup"><span data-stu-id="d0ddd-155">This requires using the <xref:Microsoft.Xrm.Sdk.Messages.CreateRequest> message.</span></span>  
  
### <a name="uploading-files-from-disk"></a><span data-ttu-id="d0ddd-156">Uploading Files from Disk</span><span class="sxs-lookup"><span data-stu-id="d0ddd-156">Uploading Files from Disk</span></span>  
 <span data-ttu-id="d0ddd-157">The WebResource.Content property requires a Base 64 string representing the binary contents of the file.</span><span class="sxs-lookup"><span data-stu-id="d0ddd-157">The WebResource.Content property requires a Base 64 string representing the binary contents of the file.</span></span> <span data-ttu-id="d0ddd-158">The following sample is the method used to convert the file into the required type.</span><span class="sxs-lookup"><span data-stu-id="d0ddd-158">The following sample is the method used to convert the file into the required type.</span></span>  
  
 [!code-csharp[ImportWebResources#ImportWebResources3](../snippets/csharp/CRMV8/importwebresources/cs/importwebresources3.cs#importwebresources3)]  
  
### <a name="combining-web-resource-record-data-with-file-data"></a><span data-ttu-id="d0ddd-159">Combining Web Resource Record Data with File Data</span><span class="sxs-lookup"><span data-stu-id="d0ddd-159">Combining Web Resource Record Data with File Data</span></span>  
 <span data-ttu-id="d0ddd-160">The ImportJob.xml file demonstrates how the data about the files being imported and the data about the Web Resource to create are combined.</span><span class="sxs-lookup"><span data-stu-id="d0ddd-160">The ImportJob.xml file demonstrates how the data about the files being imported and the data about the Web Resource to create are combined.</span></span> <span data-ttu-id="d0ddd-161">In particular, in order for relative links between related files to continue to function, the name of the Web resources you create must preserve information about the relative position of the files on disk using simulated directories in the file name.</span><span class="sxs-lookup"><span data-stu-id="d0ddd-161">In particular, in order for relative links between related files to continue to function, the name of the Web resources you create must preserve information about the relative position of the files on disk using simulated directories in the file name.</span></span> <span data-ttu-id="d0ddd-162">Because of the data in the ImportJob.xml file all these related Web resource files will be created under a common virtual folder.</span><span class="sxs-lookup"><span data-stu-id="d0ddd-162">Because of the data in the ImportJob.xml file all these related Web resource files will be created under a common virtual folder.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d0ddd-163">It is not necessary to publish Web resources when they are created.</span><span class="sxs-lookup"><span data-stu-id="d0ddd-163">It is not necessary to publish Web resources when they are created.</span></span> <span data-ttu-id="d0ddd-164">It is necessary to publish them when they are updated.</span><span class="sxs-lookup"><span data-stu-id="d0ddd-164">It is necessary to publish them when they are updated.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d0ddd-165">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="d0ddd-165">Example</span></span>  
 <span data-ttu-id="d0ddd-166">The following portion of the ImportWebResources.cs file expects the following variables:</span><span class="sxs-lookup"><span data-stu-id="d0ddd-166">The following portion of the ImportWebResources.cs file expects the following variables:</span></span>  
  
- <span data-ttu-id="d0ddd-167">`_customizationPrefix` : The customization prefix of the **Dynamics 365 for Customer Engagement apps SDK Samples** publisher.</span><span class="sxs-lookup"><span data-stu-id="d0ddd-167">`_customizationPrefix` : The customization prefix of the **Dynamics 365 for Customer Engagement apps SDK Samples** publisher.</span></span> <span data-ttu-id="d0ddd-168">If this publisher does not exist it will be created with the customization prefix of “sample”.</span><span class="sxs-lookup"><span data-stu-id="d0ddd-168">If this publisher does not exist it will be created with the customization prefix of “sample”.</span></span>  
  
- <span data-ttu-id="d0ddd-169">`_ImportWebResourcesSolutionUniqueName` : The unique name of the **Import Web Resources Sample Solution** created in this sample.</span><span class="sxs-lookup"><span data-stu-id="d0ddd-169">`_ImportWebResourcesSolutionUniqueName` : The unique name of the **Import Web Resources Sample Solution** created in this sample.</span></span> <span data-ttu-id="d0ddd-170">The value is `ImportWebResourcesSample`.</span><span class="sxs-lookup"><span data-stu-id="d0ddd-170">The value is `ImportWebResourcesSample`.</span></span>  
  
  [!code-csharp[ImportWebResources#ImportWebResources1](../snippets/csharp/CRMV8/importwebresources/cs/importwebresources1.cs#importwebresources1)]  
  
  <span data-ttu-id="d0ddd-171">It is not necessary to publish Web resources when they are created.</span><span class="sxs-lookup"><span data-stu-id="d0ddd-171">It is not necessary to publish Web resources when they are created.</span></span> <span data-ttu-id="d0ddd-172">It is necessary to publish them when they are updated.</span><span class="sxs-lookup"><span data-stu-id="d0ddd-172">It is necessary to publish them when they are updated.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="d0ddd-173">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="d0ddd-173">See also</span></span>  
 <span data-ttu-id="d0ddd-174">[Sample: Web Resource Utility](sample-web-resource-utility.md) </span><span class="sxs-lookup"><span data-stu-id="d0ddd-174">[Sample: Web Resource Utility](sample-web-resource-utility.md) </span></span>  
 <span data-ttu-id="d0ddd-175">[Web Resource Messages and Methods](webresource-entity-messages-methods.md) </span><span class="sxs-lookup"><span data-stu-id="d0ddd-175">[Web Resource Messages and Methods](webresource-entity-messages-methods.md) </span></span>  
 [<span data-ttu-id="d0ddd-176">Web Resources for Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="d0ddd-176">Web Resources for Dynamics 365 for Customer Engagement apps</span></span>](web-resources.md)
