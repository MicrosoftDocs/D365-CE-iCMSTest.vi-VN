---
title: When to edit the customizations file | MicrosoftDocs
description: The customizations.xml file that is exported as part of an unmanaged solution can be edited to perform specific customization tasks. After editing the file you can compress the modified file together with the other files exported in the unmanaged solution. You apply the changes by importing that modified unmanaged solution.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: a89d3bae-a10c-4f69-bad0-d5cb72e97094
caps.latest.revision: 17
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: c7bc1baecf06be5d84c47facb754cbd47466e1d2
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387128"
---
# <a name="when-to-edit-the-customizations-file"></a><span data-ttu-id="95b32-105">When to edit the customizations file</span><span class="sxs-lookup"><span data-stu-id="95b32-105">When to edit the customizations file</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="95b32-106">The customizations.xml file that is exported as part of an unmanaged solution can be edited to perform specific customization tasks.</span><span class="sxs-lookup"><span data-stu-id="95b32-106">The customizations.xml file that is exported as part of an unmanaged solution can be edited to perform specific customization tasks.</span></span> <span data-ttu-id="95b32-107">After editing the file you can compress the modified file together with the other files exported in the unmanaged solution.</span><span class="sxs-lookup"><span data-stu-id="95b32-107">After editing the file you can compress the modified file together with the other files exported in the unmanaged solution.</span></span> <span data-ttu-id="95b32-108">You apply the changes by importing that modified unmanaged solution.</span><span class="sxs-lookup"><span data-stu-id="95b32-108">You apply the changes by importing that modified unmanaged solution.</span></span>  
  
 <span data-ttu-id="95b32-109">Editing a complex XML file like the customizations.xml file is much easier and less prone to errors if you use a program designed to support schema validation.</span><span class="sxs-lookup"><span data-stu-id="95b32-109">Editing a complex XML file like the customizations.xml file is much easier and less prone to errors if you use a program designed to support schema validation.</span></span> <span data-ttu-id="95b32-110">While it is possible to edit this file using a simple text editor like [!INCLUDE[pn_Notepad](../../includes/pn-notepad.md)], this is not recommended unless you are very familiar with editing this file.</span><span class="sxs-lookup"><span data-stu-id="95b32-110">While it is possible to edit this file using a simple text editor like [!INCLUDE[pn_Notepad](../../includes/pn-notepad.md)], this is not recommended unless you are very familiar with editing this file.</span></span> <span data-ttu-id="95b32-111">For more information, see [Edit the Customizations file with Schema Validation](edit-customizations-xml-file-schema-validation.md).</span><span class="sxs-lookup"><span data-stu-id="95b32-111">For more information, see [Edit the Customizations file with Schema Validation](edit-customizations-xml-file-schema-validation.md).</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="95b32-112">Invalid XML or incorrect definition of solution components can cause errors that will prevent importing a manually edited unmanaged solution.</span><span class="sxs-lookup"><span data-stu-id="95b32-112">Invalid XML or incorrect definition of solution components can cause errors that will prevent importing a manually edited unmanaged solution.</span></span>  
  
## <a name="supported-tasks"></a><span data-ttu-id="95b32-113">Supported tasks</span><span class="sxs-lookup"><span data-stu-id="95b32-113">Supported tasks</span></span>  
 <span data-ttu-id="95b32-114">You can edit the customization.xml file to perform the following tasks.</span><span class="sxs-lookup"><span data-stu-id="95b32-114">You can edit the customization.xml file to perform the following tasks.</span></span>  
  
 <span data-ttu-id="95b32-115">**Editing the ribbon**</span><span class="sxs-lookup"><span data-stu-id="95b32-115">**Editing the ribbon**</span></span>  
 <span data-ttu-id="95b32-116">This documentation describes the process of editing the ribbon by editing the customization.xml file directly.</span><span class="sxs-lookup"><span data-stu-id="95b32-116">This documentation describes the process of editing the ribbon by editing the customization.xml file directly.</span></span> <span data-ttu-id="95b32-117">Several people have created ribbon editors that provide a user interface to make editing the ribbon easier.</span><span class="sxs-lookup"><span data-stu-id="95b32-117">Several people have created ribbon editors that provide a user interface to make editing the ribbon easier.</span></span> <span data-ttu-id="95b32-118">The most popular one so far is the [Ribbon Workbench](https://www.develop1.net/public/rwb/ribbonworkbench.aspx).</span><span class="sxs-lookup"><span data-stu-id="95b32-118">The most popular one so far is the [Ribbon Workbench](https://www.develop1.net/public/rwb/ribbonworkbench.aspx).</span></span> <span data-ttu-id="95b32-119">For support using this program, contact the program publisher.</span><span class="sxs-lookup"><span data-stu-id="95b32-119">For support using this program, contact the program publisher.</span></span>  
  
 <span data-ttu-id="95b32-120">For more information about editing the ribbon by editing the customization.xml manually, see [Customize the Ribbon for Microsoft Dynamics 365 for Customer Engagement](customize-commands-ribbon.md).</span><span class="sxs-lookup"><span data-stu-id="95b32-120">For more information about editing the ribbon by editing the customization.xml manually, see [Customize the Ribbon for Microsoft Dynamics 365 for Customer Engagement](customize-commands-ribbon.md).</span></span>  
  
 <span data-ttu-id="95b32-121">**Editing the SiteMap**</span><span class="sxs-lookup"><span data-stu-id="95b32-121">**Editing the SiteMap**</span></span>  
 <span data-ttu-id="95b32-122">The SDK describes the process of editing the SiteMap by editing the customization.xml file directly.</span><span class="sxs-lookup"><span data-stu-id="95b32-122">The SDK describes the process of editing the SiteMap by editing the customization.xml file directly.</span></span> <span data-ttu-id="95b32-123">However, its recommended that you use the site map designer in Customer Engagement to create or update site maps.</span><span class="sxs-lookup"><span data-stu-id="95b32-123">However, its recommended that you use the site map designer in Customer Engagement to create or update site maps.</span></span> <span data-ttu-id="95b32-124">More information: [Create a site map for an app using the site map designer](../../customize/create-site-map-app.md)</span><span class="sxs-lookup"><span data-stu-id="95b32-124">More information: [Create a site map for an app using the site map designer](../../customize/create-site-map-app.md)</span></span>  
  
 <span data-ttu-id="95b32-125">You can also use one of the community-developed site map editors, such as the [XrmToolBox Site Map Editor](https://www.xrmtoolbox.com/plugins/MsCrmTools.SiteMapEditor/).</span><span class="sxs-lookup"><span data-stu-id="95b32-125">You can also use one of the community-developed site map editors, such as the [XrmToolBox Site Map Editor](https://www.xrmtoolbox.com/plugins/MsCrmTools.SiteMapEditor/).</span></span>   
  
 <span data-ttu-id="95b32-126">For more information, see [Change Application Navigation using the SiteMap](/developer/customize-dev/change-application-navigation-using-sitemap.md)</span><span class="sxs-lookup"><span data-stu-id="95b32-126">For more information, see [Change Application Navigation using the SiteMap](/developer/customize-dev/change-application-navigation-using-sitemap.md)</span></span>  
  
 <span data-ttu-id="95b32-127">**Editing FormXml**</span><span class="sxs-lookup"><span data-stu-id="95b32-127">**Editing FormXml**</span></span>  
 <span data-ttu-id="95b32-128">FormXml is used to define entity forms and dashboards.</span><span class="sxs-lookup"><span data-stu-id="95b32-128">FormXml is used to define entity forms and dashboards.</span></span> <span data-ttu-id="95b32-129">The form editor and dashboard designer in the application are the most commonly used tools for this purpose.</span><span class="sxs-lookup"><span data-stu-id="95b32-129">The form editor and dashboard designer in the application are the most commonly used tools for this purpose.</span></span> <span data-ttu-id="95b32-130">Editing the customizations.xml file is an alternative method.</span><span class="sxs-lookup"><span data-stu-id="95b32-130">Editing the customizations.xml file is an alternative method.</span></span> <span data-ttu-id="95b32-131">For more information, see [Customize Entity Forms in Microsoft Dynamics 365 for Customer Engagement](customize-entity-forms.md) and [Create a Dashboard](create-dashboard.md).</span><span class="sxs-lookup"><span data-stu-id="95b32-131">For more information, see [Customize Entity Forms in Microsoft Dynamics 365 for Customer Engagement](customize-entity-forms.md) and [Create a Dashboard](create-dashboard.md).</span></span>  
  
 <span data-ttu-id="95b32-132">**Editing saved queries**</span><span class="sxs-lookup"><span data-stu-id="95b32-132">**Editing saved queries**</span></span>  
 <span data-ttu-id="95b32-133">Definitions of views for entities are included in the customizations.xml file and may be manually edited.</span><span class="sxs-lookup"><span data-stu-id="95b32-133">Definitions of views for entities are included in the customizations.xml file and may be manually edited.</span></span> <span data-ttu-id="95b32-134">The view editor in the application is the most commonly used tool for this purpose.</span><span class="sxs-lookup"><span data-stu-id="95b32-134">The view editor in the application is the most commonly used tool for this purpose.</span></span> <span data-ttu-id="95b32-135">Editing customizations.xml is an alternative method.</span><span class="sxs-lookup"><span data-stu-id="95b32-135">Editing customizations.xml is an alternative method.</span></span> <span data-ttu-id="95b32-136">For more information, see [Customize Entity Views in Microsoft Dynamics 365 for Customer Engagement](customize-entity-views.md).</span><span class="sxs-lookup"><span data-stu-id="95b32-136">For more information, see [Customize Entity Views in Microsoft Dynamics 365 for Customer Engagement](customize-entity-views.md).</span></span>  
  
 <span data-ttu-id="95b32-137">**Editing the ISV.config**</span><span class="sxs-lookup"><span data-stu-id="95b32-137">**Editing the ISV.config**</span></span>  
 <span data-ttu-id="95b32-138">In earlier versions of [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement, ISV.Config was the way to add client application extensions as well as some other configuration options.</span><span class="sxs-lookup"><span data-stu-id="95b32-138">In earlier versions of [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement, ISV.Config was the way to add client application extensions as well as some other configuration options.</span></span> <span data-ttu-id="95b32-139">For [!INCLUDE[pn_crm2011_and_online](../../includes/pn-crm2011-and-online.md)], the Ribbon provides the way to extend the application.</span><span class="sxs-lookup"><span data-stu-id="95b32-139">For [!INCLUDE[pn_crm2011_and_online](../../includes/pn-crm2011-and-online.md)], the Ribbon provides the way to extend the application.</span></span> <span data-ttu-id="95b32-140">The only remaining capability left in ISV.Config is to customize the appearance of the Service Calendar.</span><span class="sxs-lookup"><span data-stu-id="95b32-140">The only remaining capability left in ISV.Config is to customize the appearance of the Service Calendar.</span></span> <span data-ttu-id="95b32-141">For more information, see [Service Calendar Appearance Configuration](service-calendar-appearance-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="95b32-141">For more information, see [Service Calendar Appearance Configuration](service-calendar-appearance-configuration.md).</span></span>  
  
## <a name="unsupported-tasks"></a><span data-ttu-id="95b32-142">Unsupported tasks</span><span class="sxs-lookup"><span data-stu-id="95b32-142">Unsupported tasks</span></span>  
 <span data-ttu-id="95b32-143">Defining any other solution components by editing the exported customizations.xml file is not supported.</span><span class="sxs-lookup"><span data-stu-id="95b32-143">Defining any other solution components by editing the exported customizations.xml file is not supported.</span></span> <span data-ttu-id="95b32-144">This includes the following:</span><span class="sxs-lookup"><span data-stu-id="95b32-144">This includes the following:</span></span>  
  
-   <span data-ttu-id="95b32-145">Thực thể</span><span class="sxs-lookup"><span data-stu-id="95b32-145">Entities</span></span>  
  
-   <span data-ttu-id="95b32-146">Thuộc tính</span><span class="sxs-lookup"><span data-stu-id="95b32-146">Attributes</span></span>  
  
-   <span data-ttu-id="95b32-147">Entity Relationships</span><span class="sxs-lookup"><span data-stu-id="95b32-147">Entity Relationships</span></span>  
  
-   <span data-ttu-id="95b32-148">Thông báo của Thực thể</span><span class="sxs-lookup"><span data-stu-id="95b32-148">Entity Messages</span></span>  
  
-   <span data-ttu-id="95b32-149">Option Sets</span><span class="sxs-lookup"><span data-stu-id="95b32-149">Option Sets</span></span>  
  
-   <span data-ttu-id="95b32-150">Tài nguyên web</span><span class="sxs-lookup"><span data-stu-id="95b32-150">Web Resources</span></span>  
  
-   <span data-ttu-id="95b32-151">Processes (Workflows)</span><span class="sxs-lookup"><span data-stu-id="95b32-151">Processes (Workflows)</span></span>  
  
-   <span data-ttu-id="95b32-152">Plugin Assemblies</span><span class="sxs-lookup"><span data-stu-id="95b32-152">Plugin Assemblies</span></span>  
  
-   <span data-ttu-id="95b32-153">SDK Message Processing steps</span><span class="sxs-lookup"><span data-stu-id="95b32-153">SDK Message Processing steps</span></span>  
  
-   <span data-ttu-id="95b32-154">Service Endpoints</span><span class="sxs-lookup"><span data-stu-id="95b32-154">Service Endpoints</span></span>  
  
-   <span data-ttu-id="95b32-155">Báo cáo</span><span class="sxs-lookup"><span data-stu-id="95b32-155">Reports</span></span>  
  
-   <span data-ttu-id="95b32-156">Connection Roles</span><span class="sxs-lookup"><span data-stu-id="95b32-156">Connection Roles</span></span>  
  
-   <span data-ttu-id="95b32-157">Mẫu Bài viết</span><span class="sxs-lookup"><span data-stu-id="95b32-157">Article Templates</span></span>  
  
-   <span data-ttu-id="95b32-158">Contract Templates</span><span class="sxs-lookup"><span data-stu-id="95b32-158">Contract Templates</span></span>  
  
-   <span data-ttu-id="95b32-159">E-mail Templates</span><span class="sxs-lookup"><span data-stu-id="95b32-159">E-mail Templates</span></span>  
  
-   <span data-ttu-id="95b32-160">Mail Merge Templates</span><span class="sxs-lookup"><span data-stu-id="95b32-160">Mail Merge Templates</span></span>  
  
-   <span data-ttu-id="95b32-161">Vai trò Bảo mật</span><span class="sxs-lookup"><span data-stu-id="95b32-161">Security Roles</span></span>  
  
-   <span data-ttu-id="95b32-162">Field Security Profiles</span><span class="sxs-lookup"><span data-stu-id="95b32-162">Field Security Profiles</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="95b32-163">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="95b32-163">See also</span></span>  
 <span data-ttu-id="95b32-164">[Customize Microsoft Dynamics 365 for Customer Engagement and Microsoft Dynamics 365 for Customer Engagement (online)](customize-applications.md) </span><span class="sxs-lookup"><span data-stu-id="95b32-164">[Customize Microsoft Dynamics 365 for Customer Engagement and Microsoft Dynamics 365 for Customer Engagement (online)](customize-applications.md) </span></span>  
 <span data-ttu-id="95b32-165">[Customization XML Reference](../customization-xml-reference.md) </span><span class="sxs-lookup"><span data-stu-id="95b32-165">[Customization XML Reference](../customization-xml-reference.md) </span></span>  
 <span data-ttu-id="95b32-166">[Customization Solutions File Schema](customization-solutions-file-schema.md) </span><span class="sxs-lookup"><span data-stu-id="95b32-166">[Customization Solutions File Schema](customization-solutions-file-schema.md) </span></span>  
 <span data-ttu-id="95b32-167">[Ribbon core schema](ribbon-core-schema.md) [Ribbon types schema](ribbon-types-schema.md) [Ribbon WSS schema](ribbon-wss-schema.md) </span><span class="sxs-lookup"><span data-stu-id="95b32-167">[Ribbon core schema](ribbon-core-schema.md) [Ribbon types schema](ribbon-types-schema.md) [Ribbon WSS schema](ribbon-wss-schema.md) </span></span>  
 <span data-ttu-id="95b32-168">[SiteMap schema](sitemap-schema.md) </span><span class="sxs-lookup"><span data-stu-id="95b32-168">[SiteMap schema](sitemap-schema.md) </span></span>  
 <span data-ttu-id="95b32-169">[Form XML schema](form-xml-schema.md) </span><span class="sxs-lookup"><span data-stu-id="95b32-169">[Form XML schema](form-xml-schema.md) </span></span>  
 [<span data-ttu-id="95b32-170">Schema Support for the Customization File</span><span class="sxs-lookup"><span data-stu-id="95b32-170">Schema Support for the Customization File</span></span>](edit-customizations-xml-file-schema-validation.md)
