---
title: Create solutions that support multiple languages (Developer Guide for Dynamics 365 for Customer Engagement apps)| MicrosoftDocs
description: ''
keywords: ''
ms.date: 10/31/2017
ms.service:
- crm-online
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 2f601c9e-b1d1-47be-a8ea-afca16780751
author: JimDaly
ms.author: jdaly
manager: amyla
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7ba0a35de9d7bef4429e6e43e89d32ae0bb789fc
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386077"
---
# <a name="create-solutions-that-support-multiple-languages"></a><span data-ttu-id="2e41a-102">Create solutions that support multiple languages</span><span class="sxs-lookup"><span data-stu-id="2e41a-102">Create solutions that support multiple languages</span></span>

[!INCLUDE[cc_applies_to_update_9_0_0](../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] <span data-ttu-id="2e41a-103">apps support multiple languages.</span><span class="sxs-lookup"><span data-stu-id="2e41a-103">apps support multiple languages.</span></span> <span data-ttu-id="2e41a-104">If you want your solution to be installed for organizations that include different base languages or that have multiple languages provisioned, take this into account when planning your solution.</span><span class="sxs-lookup"><span data-stu-id="2e41a-104">If you want your solution to be installed for organizations that include different base languages or that have multiple languages provisioned, take this into account when planning your solution.</span></span> <span data-ttu-id="2e41a-105">The following table lists tactics to use along with solution components to include in a solution that supports multiple languages.</span><span class="sxs-lookup"><span data-stu-id="2e41a-105">The following table lists tactics to use along with solution components to include in a solution that supports multiple languages.</span></span>  
  
|<span data-ttu-id="2e41a-106">Tactic</span><span class="sxs-lookup"><span data-stu-id="2e41a-106">Tactic</span></span>|<span data-ttu-id="2e41a-107">Solution component type</span><span class="sxs-lookup"><span data-stu-id="2e41a-107">Solution component type</span></span>|  
|------------|-----------------------------|  
|[<span data-ttu-id="2e41a-108">String (RESX) web resources</span><span class="sxs-lookup"><span data-stu-id="2e41a-108">String (RESX) web resources</span></span>](#BKMK_Localizable_Web_Resources)|<span data-ttu-id="2e41a-109">Tài nguyên web</span><span class="sxs-lookup"><span data-stu-id="2e41a-109">Web Resources</span></span>|  
|[<span data-ttu-id="2e41a-110">Embedded labels</span><span class="sxs-lookup"><span data-stu-id="2e41a-110">Embedded labels</span></span>](#BKMK_EmbeddedLabels)|<span data-ttu-id="2e41a-111">Application Navigation (SiteMap)</span><span class="sxs-lookup"><span data-stu-id="2e41a-111">Application Navigation (SiteMap)</span></span> <br /><span data-ttu-id="2e41a-112">Ribbons</span><span class="sxs-lookup"><span data-stu-id="2e41a-112">Ribbons</span></span>|  
|[<span data-ttu-id="2e41a-113">Export and import translations</span><span class="sxs-lookup"><span data-stu-id="2e41a-113">Export and import translations</span></span>](#BKMK_ExportAndImportTranslations)|<span data-ttu-id="2e41a-114">Thuộc tính</span><span class="sxs-lookup"><span data-stu-id="2e41a-114">Attributes</span></span><br /><span data-ttu-id="2e41a-115">Biểu đồ</span><span class="sxs-lookup"><span data-stu-id="2e41a-115">Charts</span></span><br /><span data-ttu-id="2e41a-116">Bảng thông tin</span><span class="sxs-lookup"><span data-stu-id="2e41a-116">Dashboards</span></span><br /><span data-ttu-id="2e41a-117">Thực thể</span><span class="sxs-lookup"><span data-stu-id="2e41a-117">Entity</span></span><br /><span data-ttu-id="2e41a-118">Entity Relationships</span><span class="sxs-lookup"><span data-stu-id="2e41a-118">Entity Relationships</span></span><br /><span data-ttu-id="2e41a-119">Biểu mẫu</span><span class="sxs-lookup"><span data-stu-id="2e41a-119">Forms</span></span><br /><span data-ttu-id="2e41a-120">Messages</span><span class="sxs-lookup"><span data-stu-id="2e41a-120">Messages</span></span><br /><span data-ttu-id="2e41a-121">Option Sets</span><span class="sxs-lookup"><span data-stu-id="2e41a-121">Option Sets</span></span><br /><span data-ttu-id="2e41a-122">Dạng xem</span><span class="sxs-lookup"><span data-stu-id="2e41a-122">Views</span></span>|  
|[<span data-ttu-id="2e41a-123">Localization in base language strings</span><span class="sxs-lookup"><span data-stu-id="2e41a-123">Localization in base language strings</span></span>](#BKMK_LocalizationInBaseLanguageStrings)|<span data-ttu-id="2e41a-124">Contract Templates</span><span class="sxs-lookup"><span data-stu-id="2e41a-124">Contract Templates</span></span><br /> <span data-ttu-id="2e41a-125">Connection Roles</span><span class="sxs-lookup"><span data-stu-id="2e41a-125">Connection Roles</span></span><br /><span data-ttu-id="2e41a-126">Processes (Workflow)</span><span class="sxs-lookup"><span data-stu-id="2e41a-126">Processes (Workflow)</span></span><br /><span data-ttu-id="2e41a-127">Vai trò Bảo mật</span><span class="sxs-lookup"><span data-stu-id="2e41a-127">Security Roles</span></span><br /><span data-ttu-id="2e41a-128">Cấu hình Bảo mật Trường</span><span class="sxs-lookup"><span data-stu-id="2e41a-128">Field Security Profiles</span></span>|  
|[<span data-ttu-id="2e41a-129">Localization not required</span><span class="sxs-lookup"><span data-stu-id="2e41a-129">Localization not required</span></span>](#BKMK_LocalizationNotRequired)|<span data-ttu-id="2e41a-130">SDK Message Processing Steps</span><span class="sxs-lookup"><span data-stu-id="2e41a-130">SDK Message Processing Steps</span></span><br /><span data-ttu-id="2e41a-131">Service Endpoints</span><span class="sxs-lookup"><span data-stu-id="2e41a-131">Service Endpoints</span></span>|  
|[<span data-ttu-id="2e41a-132">Separate component for each language</span><span class="sxs-lookup"><span data-stu-id="2e41a-132">Separate component for each language</span></span>](#BKMK_SeparateComponentForEachLanguage)|<span data-ttu-id="2e41a-133">Mẫu Bài viết</span><span class="sxs-lookup"><span data-stu-id="2e41a-133">Article Templates</span></span><br /><span data-ttu-id="2e41a-134">Các mẫu email</span><span class="sxs-lookup"><span data-stu-id="2e41a-134">Email Templates</span></span><br /><span data-ttu-id="2e41a-135">Mail Merge Templates</span><span class="sxs-lookup"><span data-stu-id="2e41a-135">Mail Merge Templates</span></span><br /><span data-ttu-id="2e41a-136">Báo cáo</span><span class="sxs-lookup"><span data-stu-id="2e41a-136">Reports</span></span><br /><span data-ttu-id="2e41a-137">Hộp thoại</span><span class="sxs-lookup"><span data-stu-id="2e41a-137">Dialogs</span></span>|  
|[<span data-ttu-id="2e41a-138">Use XML web resources as language resources</span><span class="sxs-lookup"><span data-stu-id="2e41a-138">Use XML web resources as language resources</span></span>](#BKMK_UseXMLWebResourcesAsLanguageResources)|<span data-ttu-id="2e41a-139">Plug-in Assemblies</span><span class="sxs-lookup"><span data-stu-id="2e41a-139">Plug-in Assemblies</span></span>|  
  
 <span data-ttu-id="2e41a-140">The following sections provide additional details for each tactic.</span><span class="sxs-lookup"><span data-stu-id="2e41a-140">The following sections provide additional details for each tactic.</span></span>  

 <a name="BKMK_Localizable_Web_Resources"></a>
 ## <a name="string-resx-web-resources"></a><span data-ttu-id="2e41a-141">String (RESX) web resources</span><span class="sxs-lookup"><span data-stu-id="2e41a-141">String (RESX) web resources</span></span>
 <span data-ttu-id="2e41a-142">With string (RESX) web resources added with [!INCLUDE[pn-crm-9-0-0-online](../includes/pn-crm-9-0-0-online.md)] developers have a more robust option to create web resources that support multiple languages.</span><span class="sxs-lookup"><span data-stu-id="2e41a-142">With string (RESX) web resources added with [!INCLUDE[pn-crm-9-0-0-online](../includes/pn-crm-9-0-0-online.md)] developers have a more robust option to create web resources that support multiple languages.</span></span> <span data-ttu-id="2e41a-143">More information [String (RESX) web resources](resx-web-resources.md).</span><span class="sxs-lookup"><span data-stu-id="2e41a-143">More information [String (RESX) web resources](resx-web-resources.md).</span></span>

 <span data-ttu-id="2e41a-144">For earlier versions, see [Developer option](https://msdn.microsoft.com/library/hh670609(v=crm.8).aspx#BKMK_DeveloperOption)</span><span class="sxs-lookup"><span data-stu-id="2e41a-144">For earlier versions, see [Developer option](https://msdn.microsoft.com/library/hh670609(v=crm.8).aspx#BKMK_DeveloperOption)</span></span>
  
<a name="BKMK_EmbeddedLabels"></a>   
## <a name="embedded-labels"></a><span data-ttu-id="2e41a-145">Embedded labels</span><span class="sxs-lookup"><span data-stu-id="2e41a-145">Embedded labels</span></span>  
 <span data-ttu-id="2e41a-146">Each of the solution components that use this tactic requires that any localized text be included in the solution component.</span><span class="sxs-lookup"><span data-stu-id="2e41a-146">Each of the solution components that use this tactic requires that any localized text be included in the solution component.</span></span>  
  
### <a name="ribbons"></a><span data-ttu-id="2e41a-147">Ribbons</span><span class="sxs-lookup"><span data-stu-id="2e41a-147">Ribbons</span></span>  
 <span data-ttu-id="2e41a-148">When a language pack is installed, the application ribbon automatically displays localized text for all of the default text in the ribbon.</span><span class="sxs-lookup"><span data-stu-id="2e41a-148">When a language pack is installed, the application ribbon automatically displays localized text for all of the default text in the ribbon.</span></span> <span data-ttu-id="2e41a-149">System labels are defined in a `ResourceId` attribute value that is for internal use only.</span><span class="sxs-lookup"><span data-stu-id="2e41a-149">System labels are defined in a `ResourceId` attribute value that is for internal use only.</span></span> <span data-ttu-id="2e41a-150">When you add your own text you should use the `<LocLabels>` element to provide localized text for the languages you support.</span><span class="sxs-lookup"><span data-stu-id="2e41a-150">When you add your own text you should use the `<LocLabels>` element to provide localized text for the languages you support.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="2e41a-151">[Use Localized Labels with Ribbons](customize-dev/use-localized-labels-ribbons.md)</span><span class="sxs-lookup"><span data-stu-id="2e41a-151">[Use Localized Labels with Ribbons](customize-dev/use-localized-labels-ribbons.md)</span></span>  
  
### <a name="sitemap"></a><span data-ttu-id="2e41a-152">SiteMap</span><span class="sxs-lookup"><span data-stu-id="2e41a-152">SiteMap</span></span>  
 <span data-ttu-id="2e41a-153">When a language pack is installed, the default text in the application navigation bar automatically displays localized text.</span><span class="sxs-lookup"><span data-stu-id="2e41a-153">When a language pack is installed, the default text in the application navigation bar automatically displays localized text.</span></span> <span data-ttu-id="2e41a-154">To override the default text or to provide your own text, use the `<Titles>` element.</span><span class="sxs-lookup"><span data-stu-id="2e41a-154">To override the default text or to provide your own text, use the `<Titles>` element.</span></span> <span data-ttu-id="2e41a-155">The `Titles` element should contain a `<Title>` element that contains localized text for any languages your solution supports.</span><span class="sxs-lookup"><span data-stu-id="2e41a-155">The `Titles` element should contain a `<Title>` element that contains localized text for any languages your solution supports.</span></span> <span data-ttu-id="2e41a-156">If a `Title` element isn’t available for the user’s preferred language, the title that corresponds to the organization base language is displayed.</span><span class="sxs-lookup"><span data-stu-id="2e41a-156">If a `Title` element isn’t available for the user’s preferred language, the title that corresponds to the organization base language is displayed.</span></span>  
  
 <span data-ttu-id="2e41a-157">The `<SubArea>` element allows for passing the user’s language preference by using the `userlcid` parameter so that content that is the target of the `SubArea.Url` attribute can be aware of the user’s language preference and adjust accordingly.</span><span class="sxs-lookup"><span data-stu-id="2e41a-157">The `<SubArea>` element allows for passing the user’s language preference by using the `userlcid` parameter so that content that is the target of the `SubArea.Url` attribute can be aware of the user’s language preference and adjust accordingly.</span></span> 
 [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="2e41a-158">[Passing Parameters to a URL Using SiteMap](customize-dev/pass-parameters-url-using-sitemap.md)</span><span class="sxs-lookup"><span data-stu-id="2e41a-158">[Passing Parameters to a URL Using SiteMap](customize-dev/pass-parameters-url-using-sitemap.md)</span></span>  
  
<a name="BKMK_ExportAndImportTranslations"></a>   
## <a name="export-and-import-translations"></a><span data-ttu-id="2e41a-159">Export and import translations</span><span class="sxs-lookup"><span data-stu-id="2e41a-159">Export and import translations</span></span>  
 <span data-ttu-id="2e41a-160">Localizable labels for the solution components in the following table can be exported for localization.</span><span class="sxs-lookup"><span data-stu-id="2e41a-160">Localizable labels for the solution components in the following table can be exported for localization.</span></span>  
  
||||  
|-|-|-|  
|<span data-ttu-id="2e41a-161">Thực thể</span><span class="sxs-lookup"><span data-stu-id="2e41a-161">Entities</span></span>|<span data-ttu-id="2e41a-162">Thuộc tính</span><span class="sxs-lookup"><span data-stu-id="2e41a-162">Attributes</span></span>|<span data-ttu-id="2e41a-163">Mối quan hệ</span><span class="sxs-lookup"><span data-stu-id="2e41a-163">Relationships</span></span>|  
|<span data-ttu-id="2e41a-164">Global Option Sets</span><span class="sxs-lookup"><span data-stu-id="2e41a-164">Global Option Sets</span></span>|<span data-ttu-id="2e41a-165">Thông báo của Thực thể</span><span class="sxs-lookup"><span data-stu-id="2e41a-165">Entity Messages</span></span>|<span data-ttu-id="2e41a-166">Biểu mẫu Thực thể</span><span class="sxs-lookup"><span data-stu-id="2e41a-166">Entity Forms</span></span>|  
|<span data-ttu-id="2e41a-167">Entity Views (SavedQuery)</span><span class="sxs-lookup"><span data-stu-id="2e41a-167">Entity Views (SavedQuery)</span></span>|<span data-ttu-id="2e41a-168">Biểu đồ</span><span class="sxs-lookup"><span data-stu-id="2e41a-168">Charts</span></span>|<span data-ttu-id="2e41a-169">Bảng thông tin</span><span class="sxs-lookup"><span data-stu-id="2e41a-169">Dashboards</span></span>|  
  
### <a name="translating-labels-and-display-strings"></a><span data-ttu-id="2e41a-170">Translating labels and display strings</span><span class="sxs-lookup"><span data-stu-id="2e41a-170">Translating labels and display strings</span></span>  
 <span data-ttu-id="2e41a-171">You can only perform customizations in the application by using the base language.</span><span class="sxs-lookup"><span data-stu-id="2e41a-171">You can only perform customizations in the application by using the base language.</span></span> <span data-ttu-id="2e41a-172">Therefore, when you want to provide localized labels and display strings for these customizations, you must export the text of the labels so that they can be localized for any other languages enabled for the organization.</span><span class="sxs-lookup"><span data-stu-id="2e41a-172">Therefore, when you want to provide localized labels and display strings for these customizations, you must export the text of the labels so that they can be localized for any other languages enabled for the organization.</span></span> <span data-ttu-id="2e41a-173">Use the following steps:</span><span class="sxs-lookup"><span data-stu-id="2e41a-173">Use the following steps:</span></span>  
  
1. <span data-ttu-id="2e41a-174">Ensure that the organization that you’re working on has all the MUI packs installed and languages provisioned for languages you want to provide translations for.</span><span class="sxs-lookup"><span data-stu-id="2e41a-174">Ensure that the organization that you’re working on has all the MUI packs installed and languages provisioned for languages you want to provide translations for.</span></span>  
  
2. <span data-ttu-id="2e41a-175">Create your solution and modify the components.</span><span class="sxs-lookup"><span data-stu-id="2e41a-175">Create your solution and modify the components.</span></span>  
  
3. <span data-ttu-id="2e41a-176">After you have finished developing your solution use the “Export Translations” functionality.</span><span class="sxs-lookup"><span data-stu-id="2e41a-176">After you have finished developing your solution use the “Export Translations” functionality.</span></span> <span data-ttu-id="2e41a-177">This generates a [!INCLUDE[pn_MS_Excel_Full](../includes/pn-ms-excel-full.md)] spreadsheet (CrmTranslations.xml) that contains all the labels that need translation.</span><span class="sxs-lookup"><span data-stu-id="2e41a-177">This generates a [!INCLUDE[pn_MS_Excel_Full](../includes/pn-ms-excel-full.md)] spreadsheet (CrmTranslations.xml) that contains all the labels that need translation.</span></span>  
  
4. <span data-ttu-id="2e41a-178">In the spreadsheet, provide the corresponding translations.</span><span class="sxs-lookup"><span data-stu-id="2e41a-178">In the spreadsheet, provide the corresponding translations.</span></span>  
  
5. <span data-ttu-id="2e41a-179">Import translations back into the same [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps organization using the “Import Translations” functionality and publish your changes.</span><span class="sxs-lookup"><span data-stu-id="2e41a-179">Import translations back into the same [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps organization using the “Import Translations” functionality and publish your changes.</span></span>  
  
6. <span data-ttu-id="2e41a-180">The next time the solution is exported it carries all the translations that you provided.</span><span class="sxs-lookup"><span data-stu-id="2e41a-180">The next time the solution is exported it carries all the translations that you provided.</span></span>  
  
   <span data-ttu-id="2e41a-181">When a solution is imported, labels for languages that aren’t available in the target system are discarded and a warning is logged.</span><span class="sxs-lookup"><span data-stu-id="2e41a-181">When a solution is imported, labels for languages that aren’t available in the target system are discarded and a warning is logged.</span></span>  
  
   <span data-ttu-id="2e41a-182">If labels for the base language of the target system are not provided in the solution package, the labels of the base language of the source are used instead.</span><span class="sxs-lookup"><span data-stu-id="2e41a-182">If labels for the base language of the target system are not provided in the solution package, the labels of the base language of the source are used instead.</span></span> <span data-ttu-id="2e41a-183">For example, if you import a solution that contains labels for English and French with English as the base language, but the target system has Japanese and French with Japanese as the base language, English labels are used instead of Japanese labels.</span><span class="sxs-lookup"><span data-stu-id="2e41a-183">For example, if you import a solution that contains labels for English and French with English as the base language, but the target system has Japanese and French with Japanese as the base language, English labels are used instead of Japanese labels.</span></span> <span data-ttu-id="2e41a-184">The base languages labels cannot be **null** or empty.</span><span class="sxs-lookup"><span data-stu-id="2e41a-184">The base languages labels cannot be **null** or empty.</span></span>  
  
#### <a name="exporting-translations"></a><span data-ttu-id="2e41a-185">Exporting translations</span><span class="sxs-lookup"><span data-stu-id="2e41a-185">Exporting translations</span></span>  
 <span data-ttu-id="2e41a-186">Before you export translations you must first install the language packs and provision all the languages you want to have localized.</span><span class="sxs-lookup"><span data-stu-id="2e41a-186">Before you export translations you must first install the language packs and provision all the languages you want to have localized.</span></span> <span data-ttu-id="2e41a-187">You can export the translations in the web application or by using the <xref:Microsoft.Crm.Sdk.Messages.ExportTranslationRequest> message.</span><span class="sxs-lookup"><span data-stu-id="2e41a-187">You can export the translations in the web application or by using the <xref:Microsoft.Crm.Sdk.Messages.ExportTranslationRequest> message.</span></span> <span data-ttu-id="2e41a-188">For more information, see [Export Customized Entity and Field Text for Translation](../customize/export-customized-entity-field-text-translation.md).</span><span class="sxs-lookup"><span data-stu-id="2e41a-188">For more information, see [Export Customized Entity and Field Text for Translation](../customize/export-customized-entity-field-text-translation.md).</span></span>  
  
#### <a name="translating-text"></a><span data-ttu-id="2e41a-189">Translating text</span><span class="sxs-lookup"><span data-stu-id="2e41a-189">Translating text</span></span>  
 <span data-ttu-id="2e41a-190">When you open the CrmTranslations.xml file in [!INCLUDE[pn_Excel_short](../includes/pn-excel-short.md)] you will see the three worksheets listed in the following table.</span><span class="sxs-lookup"><span data-stu-id="2e41a-190">When you open the CrmTranslations.xml file in [!INCLUDE[pn_Excel_short](../includes/pn-excel-short.md)] you will see the three worksheets listed in the following table.</span></span>  
  
|<span data-ttu-id="2e41a-191">Worksheet</span><span class="sxs-lookup"><span data-stu-id="2e41a-191">Worksheet</span></span>|<span data-ttu-id="2e41a-192">Mô tả</span><span class="sxs-lookup"><span data-stu-id="2e41a-192">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="2e41a-193">Thông tin</span><span class="sxs-lookup"><span data-stu-id="2e41a-193">Information</span></span>|<span data-ttu-id="2e41a-194">Displays information about the organization and solution that the labels and strings were exported from.</span><span class="sxs-lookup"><span data-stu-id="2e41a-194">Displays information about the organization and solution that the labels and strings were exported from.</span></span>|  
|<span data-ttu-id="2e41a-195">Display Strings</span><span class="sxs-lookup"><span data-stu-id="2e41a-195">Display Strings</span></span>|<span data-ttu-id="2e41a-196">Display strings that represent the text of any messages associated with a metadata component.</span><span class="sxs-lookup"><span data-stu-id="2e41a-196">Display strings that represent the text of any messages associated with a metadata component.</span></span> <span data-ttu-id="2e41a-197">This table includes error messages and strings used for system ribbon elements.</span><span class="sxs-lookup"><span data-stu-id="2e41a-197">This table includes error messages and strings used for system ribbon elements.</span></span>|  
|<span data-ttu-id="2e41a-198">Localized Labels</span><span class="sxs-lookup"><span data-stu-id="2e41a-198">Localized Labels</span></span>|<span data-ttu-id="2e41a-199">Displays all of the text for any metadata component labels.</span><span class="sxs-lookup"><span data-stu-id="2e41a-199">Displays all of the text for any metadata component labels.</span></span>|  
  
 <span data-ttu-id="2e41a-200">Bạn có thể gửi tập tin này đến một chuyên gia ngôn ngữ, đại lý cung cấp dịch vụ dịch thuật hoặc công ty địa phương hóa.</span><span class="sxs-lookup"><span data-stu-id="2e41a-200">You can send this file to a linguistic expert, translation agency, or localization firm.</span></span> <span data-ttu-id="2e41a-201">They will need to provide localized strings for any of the empty cells.</span><span class="sxs-lookup"><span data-stu-id="2e41a-201">They will need to provide localized strings for any of the empty cells.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="2e41a-202">For custom entities there are some common labels that are shared with system entities, such as **Created On** or **Created By**.</span><span class="sxs-lookup"><span data-stu-id="2e41a-202">For custom entities there are some common labels that are shared with system entities, such as **Created On** or **Created By**.</span></span> <span data-ttu-id="2e41a-203">Because you have already installed and provisioned the languages, if you export languages for the default solution you may be able to match some labels in your custom entities with localized text for identical labels used by other entities.</span><span class="sxs-lookup"><span data-stu-id="2e41a-203">Because you have already installed and provisioned the languages, if you export languages for the default solution you may be able to match some labels in your custom entities with localized text for identical labels used by other entities.</span></span> <span data-ttu-id="2e41a-204">This can reduce the localization costs and improve consistency.</span><span class="sxs-lookup"><span data-stu-id="2e41a-204">This can reduce the localization costs and improve consistency.</span></span>  
  
 <span data-ttu-id="2e41a-205">After the text in the worksheets has been localized, add both the CrmTranslations.xml and [Content_Types].xml files to a single compressed .zip file.</span><span class="sxs-lookup"><span data-stu-id="2e41a-205">After the text in the worksheets has been localized, add both the CrmTranslations.xml and [Content_Types].xml files to a single compressed .zip file.</span></span> <span data-ttu-id="2e41a-206">You can now import this file.</span><span class="sxs-lookup"><span data-stu-id="2e41a-206">You can now import this file.</span></span>  
  
 <span data-ttu-id="2e41a-207">If you prefer to work with the exported files programmatically as an XML document, see [Office 2003 XML Reference Schemas](http://www.microsoft.com/downloads/details.aspx?FamilyID=fe118952-3547-420a-a412-00a2662442d9) for information about the schemas these files use.</span><span class="sxs-lookup"><span data-stu-id="2e41a-207">If you prefer to work with the exported files programmatically as an XML document, see [Office 2003 XML Reference Schemas](http://www.microsoft.com/downloads/details.aspx?FamilyID=fe118952-3547-420a-a412-00a2662442d9) for information about the schemas these files use.</span></span>  
  
#### <a name="importing-translated-text"></a><span data-ttu-id="2e41a-208">Importing translated text</span><span class="sxs-lookup"><span data-stu-id="2e41a-208">Importing translated text</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="2e41a-209">You can only import translated text back into the same organization it was exported from.</span><span class="sxs-lookup"><span data-stu-id="2e41a-209">You can only import translated text back into the same organization it was exported from.</span></span>  
  
 <span data-ttu-id="2e41a-210">After you have exported the customized entity or attribute text and had it translated, you can import the translated text strings in the web application by using the <xref:Microsoft.Crm.Sdk.Messages.ImportTranslationRequest> message.</span><span class="sxs-lookup"><span data-stu-id="2e41a-210">After you have exported the customized entity or attribute text and had it translated, you can import the translated text strings in the web application by using the <xref:Microsoft.Crm.Sdk.Messages.ImportTranslationRequest> message.</span></span> <span data-ttu-id="2e41a-211">Tệp mà bạn nhập phải là tệp nén có chứa tệp CrmTranslations.xml và tệp the [Content_Types] ở dạng gốc.</span><span class="sxs-lookup"><span data-stu-id="2e41a-211">The file that you import must be a compressed file that contains the CrmTranslations.xml and the [Content_Types].xml file at the root.</span></span> <span data-ttu-id="2e41a-212">For more information, see [Import Translated Entity and Field Text](../customize/import-translated-entity-field-text.md).</span><span class="sxs-lookup"><span data-stu-id="2e41a-212">For more information, see [Import Translated Entity and Field Text](../customize/import-translated-entity-field-text.md).</span></span>  
  
 <span data-ttu-id="2e41a-213">After you import the completed translations, customized text appears for users who work in the languages that you had the text translated into.</span><span class="sxs-lookup"><span data-stu-id="2e41a-213">After you import the completed translations, customized text appears for users who work in the languages that you had the text translated into.</span></span>  
  
> [!NOTE]
> [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] <span data-ttu-id="2e41a-214">apps cannot import translated text that is over 500 characters long.</span><span class="sxs-lookup"><span data-stu-id="2e41a-214">apps cannot import translated text that is over 500 characters long.</span></span> <span data-ttu-id="2e41a-215">If any of the items in your translation file are longer than 500 characters, the import process fails.</span><span class="sxs-lookup"><span data-stu-id="2e41a-215">If any of the items in your translation file are longer than 500 characters, the import process fails.</span></span> <span data-ttu-id="2e41a-216">Nếu tiến trình nhập bị thất bại, hãy xem lại dòng nào trong tệp đó gây ra sự thất bại, giảm số lượng các ký tự và cố gắng nhập lại.</span><span class="sxs-lookup"><span data-stu-id="2e41a-216">If the import process fails, review the line in the file that caused the failure, reduce the number of characters, and try to import again.</span></span>  
  
 <span data-ttu-id="2e41a-217">Because customization is supported only in the base language, you may be working in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps with the base language set as your language preference.</span><span class="sxs-lookup"><span data-stu-id="2e41a-217">Because customization is supported only in the base language, you may be working in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps with the base language set as your language preference.</span></span> <span data-ttu-id="2e41a-218">To verify that the translated text appears, you must change your language preference for the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps user interface.</span><span class="sxs-lookup"><span data-stu-id="2e41a-218">To verify that the translated text appears, you must change your language preference for the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps user interface.</span></span> <span data-ttu-id="2e41a-219">Để thực hiện công việc thêm tuỳ biến, bạn phải thay đổi trở lại ngôn ngữ cơ sở.</span><span class="sxs-lookup"><span data-stu-id="2e41a-219">To perform additional customization work, you must change back to the base language.</span></span>  
  
<a name="BKMK_LocalizationInBaseLanguageStrings"></a>   
## <a name="localization-in-base-language-strings"></a><span data-ttu-id="2e41a-220">Localization in base language strings</span><span class="sxs-lookup"><span data-stu-id="2e41a-220">Localization in base language strings</span></span>  
 <span data-ttu-id="2e41a-221">Some solution components do not support multiple languages.</span><span class="sxs-lookup"><span data-stu-id="2e41a-221">Some solution components do not support multiple languages.</span></span> <span data-ttu-id="2e41a-222">These components include names or text that can only be meaningful in a specific language.</span><span class="sxs-lookup"><span data-stu-id="2e41a-222">These components include names or text that can only be meaningful in a specific language.</span></span> <span data-ttu-id="2e41a-223">If you create a solution for a specific language, define these solution components for the intended organization base language.</span><span class="sxs-lookup"><span data-stu-id="2e41a-223">If you create a solution for a specific language, define these solution components for the intended organization base language.</span></span>  
  
 <span data-ttu-id="2e41a-224">If you need to support multiple languages, one tactic is to include localization within the base language strings.</span><span class="sxs-lookup"><span data-stu-id="2e41a-224">If you need to support multiple languages, one tactic is to include localization within the base language strings.</span></span> <span data-ttu-id="2e41a-225">For example, if you have a Connection Role named “Friend” and you need to support English, Spanish, and German, you might use the text “Friend (Amigo / Freund)” as the name of the connection role.</span><span class="sxs-lookup"><span data-stu-id="2e41a-225">For example, if you have a Connection Role named “Friend” and you need to support English, Spanish, and German, you might use the text “Friend (Amigo / Freund)” as the name of the connection role.</span></span> <span data-ttu-id="2e41a-226">Due to issues of the length of the text there are limitations on how many languages can be supported using this tactic.</span><span class="sxs-lookup"><span data-stu-id="2e41a-226">Due to issues of the length of the text there are limitations on how many languages can be supported using this tactic.</span></span>  
  
 <span data-ttu-id="2e41a-227">Some solution components in this group are only visible to administrators.</span><span class="sxs-lookup"><span data-stu-id="2e41a-227">Some solution components in this group are only visible to administrators.</span></span> <span data-ttu-id="2e41a-228">Because customization of the system can only be done in the organization base language it is not necessary to provide multiple language versions.</span><span class="sxs-lookup"><span data-stu-id="2e41a-228">Because customization of the system can only be done in the organization base language it is not necessary to provide multiple language versions.</span></span> <span data-ttu-id="2e41a-229">**Security Roles** and **Field Security Profile** components belong to this group.</span><span class="sxs-lookup"><span data-stu-id="2e41a-229">**Security Roles** and **Field Security Profile** components belong to this group.</span></span>  
  
 <span data-ttu-id="2e41a-230">**Contract Templates** provide a description of a type of service contract.</span><span class="sxs-lookup"><span data-stu-id="2e41a-230">**Contract Templates** provide a description of a type of service contract.</span></span> <span data-ttu-id="2e41a-231">These require text for the **Name** and **Abbreviation** fields.</span><span class="sxs-lookup"><span data-stu-id="2e41a-231">These require text for the **Name** and **Abbreviation** fields.</span></span> <span data-ttu-id="2e41a-232">You should consider using names and abbreviations that are unique and appropriate for all users of the organization.</span><span class="sxs-lookup"><span data-stu-id="2e41a-232">You should consider using names and abbreviations that are unique and appropriate for all users of the organization.</span></span>  
  
 <span data-ttu-id="2e41a-233">**Connection Roles** rely on a person selecting descriptive Connection Role categories and names.</span><span class="sxs-lookup"><span data-stu-id="2e41a-233">**Connection Roles** rely on a person selecting descriptive Connection Role categories and names.</span></span> <span data-ttu-id="2e41a-234">Because these may be relatively short, it is recommended that you include localization in base language strings.</span><span class="sxs-lookup"><span data-stu-id="2e41a-234">Because these may be relatively short, it is recommended that you include localization in base language strings.</span></span>  
  
 <span data-ttu-id="2e41a-235">**Processes (Workflows)** that are initiated for events can work well as long as they do not need to update records with text that is to be localized.</span><span class="sxs-lookup"><span data-stu-id="2e41a-235">**Processes (Workflows)** that are initiated for events can work well as long as they do not need to update records with text that is to be localized.</span></span> <span data-ttu-id="2e41a-236">It is possible to use a workflow assembly so that logic that might apply to localized text could use the same strategy as plug-in assemblies ([Use XML Web Resources as Language Resources](#BKMK_UseXMLWebResourcesAsLanguageResources)).</span><span class="sxs-lookup"><span data-stu-id="2e41a-236">It is possible to use a workflow assembly so that logic that might apply to localized text could use the same strategy as plug-in assemblies ([Use XML Web Resources as Language Resources](#BKMK_UseXMLWebResourcesAsLanguageResources)).</span></span>  
  
 <span data-ttu-id="2e41a-237">**On-Demand workflows** require a name so that people can select them.</span><span class="sxs-lookup"><span data-stu-id="2e41a-237">**On-Demand workflows** require a name so that people can select them.</span></span> <span data-ttu-id="2e41a-238">In addition to including localization within the name of the on-demand workflow, another tactic is to create multiple workflows with localized names that each call the same child process.</span><span class="sxs-lookup"><span data-stu-id="2e41a-238">In addition to including localization within the name of the on-demand workflow, another tactic is to create multiple workflows with localized names that each call the same child process.</span></span> <span data-ttu-id="2e41a-239">However, all users will see the complete list of on-demand workflows, not just the ones in their preferred user interface language.</span><span class="sxs-lookup"><span data-stu-id="2e41a-239">However, all users will see the complete list of on-demand workflows, not just the ones in their preferred user interface language.</span></span>  
  
<a name="BKMK_LocalizationNotRequired"></a>   
## <a name="localization-not-required"></a><span data-ttu-id="2e41a-240">Localization not required</span><span class="sxs-lookup"><span data-stu-id="2e41a-240">Localization not required</span></span>  
 <span data-ttu-id="2e41a-241">**SDK Message Processing Step** and **Service Endpoint** solution components do not expose localizable text to users.</span><span class="sxs-lookup"><span data-stu-id="2e41a-241">**SDK Message Processing Step** and **Service Endpoint** solution components do not expose localizable text to users.</span></span> <span data-ttu-id="2e41a-242">If it is important that these components have names and descriptions that correspond to the organization’s base language, you can create and export a managed solution with names and descriptions in that language.</span><span class="sxs-lookup"><span data-stu-id="2e41a-242">If it is important that these components have names and descriptions that correspond to the organization’s base language, you can create and export a managed solution with names and descriptions in that language.</span></span>  
  
<a name="BKMK_SeparateComponentForEachLanguage"></a>   
## <a name="separate-component-for-each-language"></a><span data-ttu-id="2e41a-243">Separate component for each language</span><span class="sxs-lookup"><span data-stu-id="2e41a-243">Separate component for each language</span></span>  
 <span data-ttu-id="2e41a-244">The following solution components each may contain a considerable amount of text to be localized:</span><span class="sxs-lookup"><span data-stu-id="2e41a-244">The following solution components each may contain a considerable amount of text to be localized:</span></span>  
  
- <span data-ttu-id="2e41a-245">Mẫu Bài viết</span><span class="sxs-lookup"><span data-stu-id="2e41a-245">Article Templates</span></span>  
  
- <span data-ttu-id="2e41a-246">Các mẫu email</span><span class="sxs-lookup"><span data-stu-id="2e41a-246">Email Templates</span></span>  
  
- <span data-ttu-id="2e41a-247">Mail Merge Templates</span><span class="sxs-lookup"><span data-stu-id="2e41a-247">Mail Merge Templates</span></span>  
  
- <span data-ttu-id="2e41a-248">Báo cáo</span><span class="sxs-lookup"><span data-stu-id="2e41a-248">Reports</span></span>  
  
- <span data-ttu-id="2e41a-249">Hộp thoại</span><span class="sxs-lookup"><span data-stu-id="2e41a-249">Dialogs</span></span>  
  
  <span data-ttu-id="2e41a-250">For these types of solution components, the recommended tactic is to create separate components for each language.</span><span class="sxs-lookup"><span data-stu-id="2e41a-250">For these types of solution components, the recommended tactic is to create separate components for each language.</span></span> <span data-ttu-id="2e41a-251">This means that you typically create a base managed solution that contains your core solution components and then a separate managed solution that contains these solution components for each language.</span><span class="sxs-lookup"><span data-stu-id="2e41a-251">This means that you typically create a base managed solution that contains your core solution components and then a separate managed solution that contains these solution components for each language.</span></span> <span data-ttu-id="2e41a-252">After customers install the base solution, they can install the managed solutions for the languages they have provisioned for the organization.</span><span class="sxs-lookup"><span data-stu-id="2e41a-252">After customers install the base solution, they can install the managed solutions for the languages they have provisioned for the organization.</span></span>  
  
  <span data-ttu-id="2e41a-253">Unlike **Processes (Workflows)**, you can create **Dialogs** that will reflect the user’s current language preference settings and display the dialogs only to users of that language.</span><span class="sxs-lookup"><span data-stu-id="2e41a-253">Unlike **Processes (Workflows)**, you can create **Dialogs** that will reflect the user’s current language preference settings and display the dialogs only to users of that language.</span></span>  
  
#### <a name="create-a-localized-dialog-box"></a><span data-ttu-id="2e41a-254">Create a localized dialog box</span><span class="sxs-lookup"><span data-stu-id="2e41a-254">Create a localized dialog box</span></span>  
  
1. <span data-ttu-id="2e41a-255">Install the appropriate language pack and provision the language.</span><span class="sxs-lookup"><span data-stu-id="2e41a-255">Install the appropriate language pack and provision the language.</span></span>  
  
    <span data-ttu-id="2e41a-256">For more information, see [Language Pack Installation Instructions](https://technet.microsoft.com/library/hh699674.aspx).</span><span class="sxs-lookup"><span data-stu-id="2e41a-256">For more information, see [Language Pack Installation Instructions](https://technet.microsoft.com/library/hh699674.aspx).</span></span>  
  
2. <span data-ttu-id="2e41a-257">Change your personal options to specify the **User Interface Language** for the language you want for the dialog.</span><span class="sxs-lookup"><span data-stu-id="2e41a-257">Change your personal options to specify the **User Interface Language** for the language you want for the dialog.</span></span>  
  
3. <span data-ttu-id="2e41a-258">Navigate to **Settings** and, in the **Process Center** group, select **Processes**.</span><span class="sxs-lookup"><span data-stu-id="2e41a-258">Navigate to **Settings** and, in the **Process Center** group, select **Processes**.</span></span>  
  
4. <span data-ttu-id="2e41a-259">Click **New** and create the dialog in the language that you specified.</span><span class="sxs-lookup"><span data-stu-id="2e41a-259">Click **New** and create the dialog in the language that you specified.</span></span>  
  
5. <span data-ttu-id="2e41a-260">After you have created the dialog, change your personal options to specify the organization base language.</span><span class="sxs-lookup"><span data-stu-id="2e41a-260">After you have created the dialog, change your personal options to specify the organization base language.</span></span>  
  
6. <span data-ttu-id="2e41a-261">While using the organization base language you can navigate to the **Solutions** area in **Settings** and add the localized dialog as part of a solution.</span><span class="sxs-lookup"><span data-stu-id="2e41a-261">While using the organization base language you can navigate to the **Solutions** area in **Settings** and add the localized dialog as part of a solution.</span></span>  
  
   <span data-ttu-id="2e41a-262">The dialog created in the other language will only be displayed to users who view [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps using that language.</span><span class="sxs-lookup"><span data-stu-id="2e41a-262">The dialog created in the other language will only be displayed to users who view [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps using that language.</span></span>  
  
<a name="BKMK_UseXMLWebResourcesAsLanguageResources"></a>   
## <a name="use-xml-web-resources-as-language-resources"></a><span data-ttu-id="2e41a-263">Use XML web resources as language resources</span><span class="sxs-lookup"><span data-stu-id="2e41a-263">Use XML web resources as language resources</span></span>  
 <span data-ttu-id="2e41a-264">Plug-in assembly solution components can send messages to an end user by throwing an <xref:Microsoft.Xrm.Sdk.InvalidPluginExecutionException> as well as creating and updating records.</span><span class="sxs-lookup"><span data-stu-id="2e41a-264">Plug-in assembly solution components can send messages to an end user by throwing an <xref:Microsoft.Xrm.Sdk.InvalidPluginExecutionException> as well as creating and updating records.</span></span> <span data-ttu-id="2e41a-265">Unlike Silverlight web resources, plug-ins cannot use resource files.</span><span class="sxs-lookup"><span data-stu-id="2e41a-265">Unlike Silverlight web resources, plug-ins cannot use resource files.</span></span>  
  
 <span data-ttu-id="2e41a-266">When a plug-in requires localized text, you can use an XML web resource to store the localized strings so the plug-in can access them when needed.</span><span class="sxs-lookup"><span data-stu-id="2e41a-266">When a plug-in requires localized text, you can use an XML web resource to store the localized strings so the plug-in can access them when needed.</span></span> <span data-ttu-id="2e41a-267">The structure of the XML is your option, but you may want to follow the structure used by ASP.NET Resource (.resx) files to create separate XML web resources for each language.</span><span class="sxs-lookup"><span data-stu-id="2e41a-267">The structure of the XML is your option, but you may want to follow the structure used by ASP.NET Resource (.resx) files to create separate XML web resources for each language.</span></span> <span data-ttu-id="2e41a-268">For example, the following is an XML web resource named **localizedString.en_US** that follows the pattern used by .</span><span class="sxs-lookup"><span data-stu-id="2e41a-268">For example, the following is an XML web resource named **localizedString.en_US** that follows the pattern used by .</span></span> <span data-ttu-id="2e41a-269">resx files.</span><span class="sxs-lookup"><span data-stu-id="2e41a-269">resx files.</span></span>  
  
```xml  
<root>  
 <data name="ErrorMessage">  
  <value>There was an error completing this action. Please try again.</value>  
 </data>  
 <data name="Welcome">  
  <value>Welcome</value>  
 </data>  
</root>  
```  
  
 <span data-ttu-id="2e41a-270">The following code shows how a localized message can be passed back in a plug-in to display a message to a user.</span><span class="sxs-lookup"><span data-stu-id="2e41a-270">The following code shows how a localized message can be passed back in a plug-in to display a message to a user.</span></span> <span data-ttu-id="2e41a-271">It is for the pre-validation stage of a `Delete` event for the `Account` entity:</span><span class="sxs-lookup"><span data-stu-id="2e41a-271">It is for the pre-validation stage of a `Delete` event for the `Account` entity:</span></span>  
  
```csharp  
protected void ExecutePreValidateAccountDelete(LocalPluginContext localContext)  
  {  
   if (localContext == null)  
   {  
    throw new ArgumentNullException("localContext");  
   }  
   int OrgLanguage = RetrieveOrganizationBaseLanguageCode(localContext.OrganizationService);  
   int UserLanguage = RetrieveUserUILanguageCode(localContext.OrganizationService,  
 localContext.PluginExecutionContext.InitiatingUserId);  
   String fallBackResourceFile = "";  
   switch (OrgLanguage)  
   {  
    case 1033:  
     fallBackResourceFile = "new_localizedStrings.en_US";  
     break;  
    case 1041:  
     fallBackResourceFile = "new_localizedStrings.ja_JP";  
     break;  
    case 1031:  
     fallBackResourceFile = "new_localizedStrings.de_DE";  
     break;  
    case 1036:  
     fallBackResourceFile = "new_localizedStrings.fr_FR";  
     break;  
    case 1034:  
     fallBackResourceFile = "new_localizedStrings.es_ES";  
     break;  
    case 1049:  
     fallBackResourceFile = "new_localizedStrings.ru_RU";  
     break;  
    default:  
     fallBackResourceFile = "new_localizedStrings.en_US";  
     break;  
   }  
   String ResourceFile = "";  
   switch (UserLanguage)  
   {  
    case 1033:  
     ResourceFile = "new_localizedStrings.en_US";  
     break;  
    case 1041:  
     ResourceFile = "new_localizedStrings.ja_JP";  
     break;  
    case 1031:  
     ResourceFile = "new_localizedStrings.de_DE";  
     break;  
    case 1036:  
     ResourceFile = "new_localizedStrings.fr_FR";  
     break;  
    case 1034:  
     ResourceFile = "new_localizedStrings.es_ES";  
     break;  
    case 1049:  
     ResourceFile = "new_localizedStrings.ru_RU";  
     break;  
    default:  
     ResourceFile = fallBackResourceFile;  
     break;  
   }  
   XmlDocument messages = RetrieveXmlWebResourceByName(localContext, ResourceFile);  
   String message = RetrieveLocalizedStringFromWebResource(localContext, messages, "ErrorMessage");  
   throw new InvalidPluginExecutionException(message);  
  }  
  protected static int RetrieveOrganizationBaseLanguageCode(IOrganizationService service)  
  {  
   QueryExpression organizationEntityQuery = new QueryExpression("organization");  
   organizationEntityQuery.ColumnSet.AddColumn("languagecode");  
   EntityCollection organizationEntities = service.RetrieveMultiple(organizationEntityQuery);  
   return (int)organizationEntities[0].Attributes["languagecode"];  
  }  
  protected static int RetrieveUserUILanguageCode(IOrganizationService service, Guid userId)  
  {  
   QueryExpression userSettingsQuery = new QueryExpression("usersettings");  
   userSettingsQuery.ColumnSet.AddColumns("uilanguageid", "systemuserid");  
   userSettingsQuery.Criteria.AddCondition("systemuserid", ConditionOperator.Equal, userId);  
   EntityCollection userSettings = service.RetrieveMultiple(userSettingsQuery);  
   if (userSettings.Entities.Count > 0)  
   {  
    return (int)userSettings.Entities[0]["uilanguageid"];  
   }  
   return 0;  
  }  
  protected static XmlDocument RetrieveXmlWebResourceByName(LocalPluginContext context, string webresourceSchemaName)  
  {  
   context.TracingService.Trace("Begin:RetrieveXmlWebResourceByName, webresourceSchemaName={0}", webresourceSchemaName);  
   QueryExpression webresourceQuery = new QueryExpression("webresource");  
   webresourceQuery.ColumnSet.AddColumn("content");  
   webresourceQuery.Criteria.AddCondition("name", ConditionOperator.Equal, webresourceSchemaName);  
   EntityCollection webresources = context.OrganizationService.RetrieveMultiple(webresourceQuery);  
   context.TracingService.Trace("Webresources Returned from server. Count={0}", webresources.Entities.Count);  
   if (webresources.Entities.Count > 0)  
   {  
    byte[] bytes = Convert.FromBase64String((string)webresources.Entities[0]["content"]);  
    // The bytes would contain the ByteOrderMask. Encoding.UTF8.GetString() does not remove the BOM.  
    // Stream Reader auto detects the BOM and removes it on the text  
    XmlDocument document = new XmlDocument();  
    document.XmlResolver = null;  
    using (MemoryStream ms = new MemoryStream(bytes))  
    {  
     using (StreamReader sr = new StreamReader(ms))  
     {  
      document.Load(sr);  
     }  
    }  
    context.TracingService.Trace("End:RetrieveXmlWebResourceByName , webresourceSchemaName={0}", webresourceSchemaName);  
    return document;  
   }  
   else  
   {  
    context.TracingService.Trace("{0} Webresource missing. Reinstall the solution", webresourceSchemaName);  
    throw new InvalidPluginExecutionException(String.Format("Unable to locate the web resource {0}.", webresourceSchemaName));  
    return null;  
 // This line never reached  
   }  
  }  
  protected static string RetrieveLocalizedStringFromWebResource(LocalPluginContext context, XmlDocument resource, string resourceId)  
  {  
   XmlNode valueNode = resource.SelectSingleNode(string.Format(CultureInfo.InvariantCulture, "./root/data[@name='{0}']/value", resourceId));  
   if (valueNode != null)  
   {  
    return valueNode.InnerText;  
   }  
   else  
   {  
    context.TracingService.Trace("No Node Found for {0} ", resourceId);  
    throw new InvalidPluginExecutionException(String.Format("ResourceID {0} was not found.", resourceId));  
   }  
  }  
```  
  
### <a name="see-also"></a><span data-ttu-id="2e41a-272">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="2e41a-272">See also</span></span>  
 <span data-ttu-id="2e41a-273">[Package and Distribute Extensions with Dynamics 365 for Customer Engagement apps Solution](package-distribute-extensions-use-solutions.md) </span><span class="sxs-lookup"><span data-stu-id="2e41a-273">[Package and Distribute Extensions with Dynamics 365 for Customer Engagement apps Solution](package-distribute-extensions-use-solutions.md) </span></span>  
 <span data-ttu-id="2e41a-274">[Introduction to Solutions](introduction-solutions.md) </span><span class="sxs-lookup"><span data-stu-id="2e41a-274">[Introduction to Solutions](introduction-solutions.md) </span></span>  
 <span data-ttu-id="2e41a-275">[Plan For Solution Development](plan-solution-development.md) </span><span class="sxs-lookup"><span data-stu-id="2e41a-275">[Plan For Solution Development](plan-solution-development.md) </span></span>  
 <span data-ttu-id="2e41a-276">[Dependency Tracking for Solution Components](dependency-tracking-solution-components.md) </span><span class="sxs-lookup"><span data-stu-id="2e41a-276">[Dependency Tracking for Solution Components](dependency-tracking-solution-components.md) </span></span>  
 <span data-ttu-id="2e41a-277">[Create, Export, or Import an Unmanaged Solution](create-export-import-unmanaged-solution.md) </span><span class="sxs-lookup"><span data-stu-id="2e41a-277">[Create, Export, or Import an Unmanaged Solution](create-export-import-unmanaged-solution.md) </span></span>  
 <span data-ttu-id="2e41a-278">[Tạo, cài đặt và cập nhật giải pháp được quản lý](create-install-update-managed-solution.md) </span><span class="sxs-lookup"><span data-stu-id="2e41a-278">[Create, Install, and Update a Managed Solution](create-install-update-managed-solution.md) </span></span>  
 <span data-ttu-id="2e41a-279">[Uninstall or Delete a solution](uninstall-delete-solution.md) </span><span class="sxs-lookup"><span data-stu-id="2e41a-279">[Uninstall or Delete a solution](uninstall-delete-solution.md) </span></span>  
 <span data-ttu-id="2e41a-280">[Solution entities](solution-entities.md) </span><span class="sxs-lookup"><span data-stu-id="2e41a-280">[Solution entities](solution-entities.md) </span></span>  
 [<span data-ttu-id="2e41a-281">Localize product property values</span><span class="sxs-lookup"><span data-stu-id="2e41a-281">Localize product property values</span></span>](localize-product-property-values.md)
