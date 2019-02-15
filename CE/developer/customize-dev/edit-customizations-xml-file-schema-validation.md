---
title: Edit the customizations XML file with schema validation | MicrosoftDocs
description: The customizations.xml file is included within the compressed .zip file exported as a solution. Certain portions of the customizations.xml file can be edited manually. Information about the schema helps you confirm that any modifications you make are valid.
ms.custom: ''
ms.date: 12/22/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- schemas
ms.assetid: d521a59d-a542-4dce-ab1a-43582756436c
caps.latest.revision: 19
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 33ce6de2fd212e64dd5df606028bd50a54424345
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387564"
---
# <a name="edit-the-customizations-xml-file-with-schema-validation"></a><span data-ttu-id="47cc1-105">Edit the customizations XML file with schema validation</span><span class="sxs-lookup"><span data-stu-id="47cc1-105">Edit the customizations XML file with schema validation</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="47cc1-106">The customizations.xml file is included within the compressed .zip file exported as a solution.</span><span class="sxs-lookup"><span data-stu-id="47cc1-106">The customizations.xml file is included within the compressed .zip file exported as a solution.</span></span> <span data-ttu-id="47cc1-107">Certain portions of the customizations.xml file can be edited manually.</span><span class="sxs-lookup"><span data-stu-id="47cc1-107">Certain portions of the customizations.xml file can be edited manually.</span></span> <span data-ttu-id="47cc1-108">Information about the schema helps you confirm that any modifications you make are valid.</span><span class="sxs-lookup"><span data-stu-id="47cc1-108">Information about the schema helps you confirm that any modifications you make are valid.</span></span>  
  
## <a name="xsd-schema-files"></a><span data-ttu-id="47cc1-109">XSD schema files</span><span class="sxs-lookup"><span data-stu-id="47cc1-109">XSD schema files</span></span>  
 [!INCLUDE[schema_download](../../includes/schema-download.md)] <span data-ttu-id="47cc1-110">for the XSD schema files used to validate the customization.xml file in a solution.</span><span class="sxs-lookup"><span data-stu-id="47cc1-110">for the XSD schema files used to validate the customization.xml file in a solution.</span></span> <span data-ttu-id="47cc1-111">The necessary files are:</span><span class="sxs-lookup"><span data-stu-id="47cc1-111">The necessary files are:</span></span>  
  
- <span data-ttu-id="47cc1-112">CustomizationsSolution.xsd</span><span class="sxs-lookup"><span data-stu-id="47cc1-112">CustomizationsSolution.xsd</span></span>  
  
- <span data-ttu-id="47cc1-113">fetch.xsd</span><span class="sxs-lookup"><span data-stu-id="47cc1-113">fetch.xsd</span></span>  
  
- <span data-ttu-id="47cc1-114">FormXml.xsd</span><span class="sxs-lookup"><span data-stu-id="47cc1-114">FormXml.xsd</span></span>  
  
- <span data-ttu-id="47cc1-115">isv.config.xsd</span><span class="sxs-lookup"><span data-stu-id="47cc1-115">isv.config.xsd</span></span>  
  
- <span data-ttu-id="47cc1-116">RibbonCore.xsd</span><span class="sxs-lookup"><span data-stu-id="47cc1-116">RibbonCore.xsd</span></span>  
  
- <span data-ttu-id="47cc1-117">RibbonTypes.xsd</span><span class="sxs-lookup"><span data-stu-id="47cc1-117">RibbonTypes.xsd</span></span>  
  
- <span data-ttu-id="47cc1-118">RibbonWSS.xsd</span><span class="sxs-lookup"><span data-stu-id="47cc1-118">RibbonWSS.xsd</span></span>  
  
- <span data-ttu-id="47cc1-119">SiteMap.xsd</span><span class="sxs-lookup"><span data-stu-id="47cc1-119">SiteMap.xsd</span></span>  
  
- <span data-ttu-id="47cc1-120">SiteMapType.xsd</span><span class="sxs-lookup"><span data-stu-id="47cc1-120">SiteMapType.xsd</span></span>  
  
- <span data-ttu-id="47cc1-121">VisualizationDataDescription.xsd</span><span class="sxs-lookup"><span data-stu-id="47cc1-121">VisualizationDataDescription.xsd</span></span>  
  
  <span data-ttu-id="47cc1-122">These files are also installed on the on-premises [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement server at: `[Install Drive]\Program Files\Microsoft Dynamics CRM\Server\ApplicationFiles`</span><span class="sxs-lookup"><span data-stu-id="47cc1-122">These files are also installed on the on-premises [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement server at: `[Install Drive]\Program Files\Microsoft Dynamics CRM\Server\ApplicationFiles`</span></span>  
  
[!INCLUDE[cc_sdk_onpremises_note](../../includes/cc-sdk-onpremises-note.md)] <span data-ttu-id="47cc1-123">CustomizationsSolution.xsd is the schema for the exported solution.</span><span class="sxs-lookup"><span data-stu-id="47cc1-123">CustomizationsSolution.xsd is the schema for the exported solution.</span></span> <span data-ttu-id="47cc1-124">It contains references to the other XSD files.</span><span class="sxs-lookup"><span data-stu-id="47cc1-124">It contains references to the other XSD files.</span></span> <span data-ttu-id="47cc1-125">All the files should be located in the same folder.</span><span class="sxs-lookup"><span data-stu-id="47cc1-125">All the files should be located in the same folder.</span></span>  
  
<a name="BKMK_UseSchemaValidation"></a>   
## <a name="using-schema-validation"></a><span data-ttu-id="47cc1-126">Using schema validation</span><span class="sxs-lookup"><span data-stu-id="47cc1-126">Using schema validation</span></span>  
 <span data-ttu-id="47cc1-127">Because the exported XML is a text file, you can edit it using a text editor such as [!INCLUDE[pn_Notepad](../../includes/pn-notepad.md)].</span><span class="sxs-lookup"><span data-stu-id="47cc1-127">Because the exported XML is a text file, you can edit it using a text editor such as [!INCLUDE[pn_Notepad](../../includes/pn-notepad.md)].</span></span> <span data-ttu-id="47cc1-128">However, we strongly recommend that you use an application that supports XSD schema validation such as [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)].</span><span class="sxs-lookup"><span data-stu-id="47cc1-128">However, we strongly recommend that you use an application that supports XSD schema validation such as [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)].</span></span> <span data-ttu-id="47cc1-129">XSD validation in [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)] or [Visual Studio Express 2012 for Web](http://www.microsoft.com/visualstudio/eng/products/visual-studio-express-for-web) provides [!INCLUDE[pn_IntelliSense](../../includes/pn-intellisense.md)] information and schema validation to help prevent errors.</span><span class="sxs-lookup"><span data-stu-id="47cc1-129">XSD validation in [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)] or [Visual Studio Express 2012 for Web](http://www.microsoft.com/visualstudio/eng/products/visual-studio-express-for-web) provides [!INCLUDE[pn_IntelliSense](../../includes/pn-intellisense.md)] information and schema validation to help prevent errors.</span></span>  
  
 <span data-ttu-id="47cc1-130">The XSD schema files that are used to validate the customization.xml file in a solution are available here.</span><span class="sxs-lookup"><span data-stu-id="47cc1-130">The XSD schema files that are used to validate the customization.xml file in a solution are available here.</span></span> [!INCLUDE[schema_download](../../includes/schema-download.md)]<span data-ttu-id="47cc1-131">.</span><span class="sxs-lookup"><span data-stu-id="47cc1-131">.</span></span> <span data-ttu-id="47cc1-132">Make sure to copy all the files from that folder into the same directory.</span><span class="sxs-lookup"><span data-stu-id="47cc1-132">Make sure to copy all the files from that folder into the same directory.</span></span> <span data-ttu-id="47cc1-133">You will need to associate the customizations.xml file to the CustomizationsSolution.xsd file.</span><span class="sxs-lookup"><span data-stu-id="47cc1-133">You will need to associate the customizations.xml file to the CustomizationsSolution.xsd file.</span></span> <span data-ttu-id="47cc1-134">That file has links to all the other XSD files in the folder.</span><span class="sxs-lookup"><span data-stu-id="47cc1-134">That file has links to all the other XSD files in the folder.</span></span>  
  
1. <span data-ttu-id="47cc1-135">Download the XSD schema files and copy all of them to your computer.</span><span class="sxs-lookup"><span data-stu-id="47cc1-135">Download the XSD schema files and copy all of them to your computer.</span></span> <span data-ttu-id="47cc1-136">Save them in the location that [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)] uses for XSD validation files.</span><span class="sxs-lookup"><span data-stu-id="47cc1-136">Save them in the location that [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)] uses for XSD validation files.</span></span> <span data-ttu-id="47cc1-137">This location is probably `[install drive]\Program Files (x86)\Microsoft Visual Studio X.0\Xml\Schemas` where `X` represents the version of [!INCLUDE[pn_Visual_Studio_short](../../includes/pn-visual-studio-short.md)].</span><span class="sxs-lookup"><span data-stu-id="47cc1-137">This location is probably `[install drive]\Program Files (x86)\Microsoft Visual Studio X.0\Xml\Schemas` where `X` represents the version of [!INCLUDE[pn_Visual_Studio_short](../../includes/pn-visual-studio-short.md)].</span></span>  
  
2. <span data-ttu-id="47cc1-138">Right-click the customizations.xml file and select **Open With** and then select the version of [!INCLUDE[pn_Visual_Studio_short](../../includes/pn-visual-studio-short.md)].</span><span class="sxs-lookup"><span data-stu-id="47cc1-138">Right-click the customizations.xml file and select **Open With** and then select the version of [!INCLUDE[pn_Visual_Studio_short](../../includes/pn-visual-studio-short.md)].</span></span>  
  
3. <span data-ttu-id="47cc1-139">Select **View** and then select **Properties Window**.</span><span class="sxs-lookup"><span data-stu-id="47cc1-139">Select **View** and then select **Properties Window**.</span></span>  
  
4. <span data-ttu-id="47cc1-140">In the **Properties** window, in the **Schemas** field, click the ellipsis [**...**] button.</span><span class="sxs-lookup"><span data-stu-id="47cc1-140">In the **Properties** window, in the **Schemas** field, click the ellipsis [**...**] button.</span></span>  
  
5. <span data-ttu-id="47cc1-141">In the **Xml Schemas** dialog box you should see the customizationsSolution.xsd.</span><span class="sxs-lookup"><span data-stu-id="47cc1-141">In the **Xml Schemas** dialog box you should see the customizationsSolution.xsd.</span></span> <span data-ttu-id="47cc1-142">In the **Use** column, select **Use this schema**.</span><span class="sxs-lookup"><span data-stu-id="47cc1-142">In the **Use** column, select **Use this schema**.</span></span>  
  
   > [!NOTE]
   >  <span data-ttu-id="47cc1-143">If you do not see it, click **Add** and browse to where you saved it.</span><span class="sxs-lookup"><span data-stu-id="47cc1-143">If you do not see it, click **Add** and browse to where you saved it.</span></span>  
  
6. <span data-ttu-id="47cc1-144">Bấm **OK**.</span><span class="sxs-lookup"><span data-stu-id="47cc1-144">Click **OK**.</span></span>  
  
   <span data-ttu-id="47cc1-145">You are now ready to begin editing the XML with XSD validation.</span><span class="sxs-lookup"><span data-stu-id="47cc1-145">You are now ready to begin editing the XML with XSD validation.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="47cc1-146">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="47cc1-146">See also</span></span>

 <span data-ttu-id="47cc1-147">[When to Edit the Customizations File for Dynamics 365 for Customer Engagement](when-edit-customization-file.md) </span><span class="sxs-lookup"><span data-stu-id="47cc1-147">[When to Edit the Customizations File for Dynamics 365 for Customer Engagement](when-edit-customization-file.md) </span></span>  
 <span data-ttu-id="47cc1-148">[Ribbon core schema](ribbon-core-schema.md) [Ribbon types schema](ribbon-types-schema.md) [Ribbon WSS schema](ribbon-wss-schema.md) [SiteMap schema](sitemap-schema.md) </span><span class="sxs-lookup"><span data-stu-id="47cc1-148">[Ribbon core schema](ribbon-core-schema.md) [Ribbon types schema](ribbon-types-schema.md) [Ribbon WSS schema](ribbon-wss-schema.md) [SiteMap schema](sitemap-schema.md) </span></span>  
 <span data-ttu-id="47cc1-149">[Form XML schema](form-xml-schema.md)   </span><span class="sxs-lookup"><span data-stu-id="47cc1-149">[Form XML schema](form-xml-schema.md)   </span></span>  
 <span data-ttu-id="47cc1-150">[ISV Configuration File Schema](isv-configuration-file-schema.md) </span><span class="sxs-lookup"><span data-stu-id="47cc1-150">[ISV Configuration File Schema](isv-configuration-file-schema.md) </span></span>  
 [<span data-ttu-id="47cc1-151">Build Queries with FetchXML</span><span class="sxs-lookup"><span data-stu-id="47cc1-151">Build Queries with FetchXML</span></span>](../org-service/build-queries-fetchxml.md)
