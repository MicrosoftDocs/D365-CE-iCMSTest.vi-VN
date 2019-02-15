---
title: Create a dashboard (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Organization-owned dashboards can be created by using the Dynamics 365 for Customer Engagement web services (SDK) or by customizing the entity form in Dynamics 365 for Customer Engagement by editing the customizations.xml file.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 155a627a-fae8-4154-89a7-28b7fc912db0
caps.latest.revision: 28
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ee994ff5271fa13e64a0988e518085e62c93ad5f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386497"
---
# <a name="create-a-dashboard"></a><span data-ttu-id="883f7-103">Create a dashboard</span><span class="sxs-lookup"><span data-stu-id="883f7-103">Create a dashboard</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="883f7-104">Organization-owned dashboards can be created by using the [!INCLUDE[cc-dyn365-ce-web-services](../../includes/cc-dyn365-ce-web-services.md)] or by customizing the entity form in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement by editing the customizations.xml file.</span><span class="sxs-lookup"><span data-stu-id="883f7-104">Organization-owned dashboards can be created by using the [!INCLUDE[cc-dyn365-ce-web-services](../../includes/cc-dyn365-ce-web-services.md)] or by customizing the entity form in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement by editing the customizations.xml file.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="883f7-105">Some dashboards that are created by using the SDK or by customizing the entity form are not supported by the Dashboard Designer in the Web application.</span><span class="sxs-lookup"><span data-stu-id="883f7-105">Some dashboards that are created by using the SDK or by customizing the entity form are not supported by the Dashboard Designer in the Web application.</span></span> <span data-ttu-id="883f7-106">For more information, see [Limitations: Creating dashboards by using the SDK or through form customization](#Limitations) later in this topic.</span><span class="sxs-lookup"><span data-stu-id="883f7-106">For more information, see [Limitations: Creating dashboards by using the SDK or through form customization](#Limitations) later in this topic.</span></span>  
  
 <span data-ttu-id="883f7-107">Before creating a dashboard, consider the following:</span><span class="sxs-lookup"><span data-stu-id="883f7-107">Before creating a dashboard, consider the following:</span></span>  
  
- <span data-ttu-id="883f7-108">**Type of dashboard**: If you want your dashboards to be available across the organization and do not want to manage the access levels at a more detailed level, you might want to create an organization-owned dashboard.</span><span class="sxs-lookup"><span data-stu-id="883f7-108">**Type of dashboard**: If you want your dashboards to be available across the organization and do not want to manage the access levels at a more detailed level, you might want to create an organization-owned dashboard.</span></span> <span data-ttu-id="883f7-109">However, if you are concerned about the access privileges and security of your dashboard, consider creating a user-owned dashboard where you have more control on who can access it.</span><span class="sxs-lookup"><span data-stu-id="883f7-109">However, if you are concerned about the access privileges and security of your dashboard, consider creating a user-owned dashboard where you have more control on who can access it.</span></span>  
  
     <span data-ttu-id="883f7-110">To create organization-owned dashboards, you must have the System Administrator or System Customizer role.</span><span class="sxs-lookup"><span data-stu-id="883f7-110">To create organization-owned dashboards, you must have the System Administrator or System Customizer role.</span></span>  
  
- <span data-ttu-id="883f7-111">**Dashboard layout**: While creating dashboards, you have to use the FormXML to define the dashboard components and layout.</span><span class="sxs-lookup"><span data-stu-id="883f7-111">**Dashboard layout**: While creating dashboards, you have to use the FormXML to define the dashboard components and layout.</span></span> <span data-ttu-id="883f7-112">For information about working with FormXML to define a dashboard, see [Dashboard Components and FormXML Elements](understand-dashboards-dashboard-components-formxml.md#DashboardComponentsandFormXML).</span><span class="sxs-lookup"><span data-stu-id="883f7-112">For information about working with FormXML to define a dashboard, see [Dashboard Components and FormXML Elements](understand-dashboards-dashboard-components-formxml.md#DashboardComponentsandFormXML).</span></span> <span data-ttu-id="883f7-113">For some sample FormXMLs of different types of dashboards, see [Sample Dashboards](sample-dashboards.md).</span><span class="sxs-lookup"><span data-stu-id="883f7-113">For some sample FormXMLs of different types of dashboards, see [Sample Dashboards](sample-dashboards.md).</span></span>  
  
<a name="UsingSDK"></a>   
## <a name="create-a-dashboard-by-using-the-sdk"></a><span data-ttu-id="883f7-114">Create a dashboard by using the SDK</span><span class="sxs-lookup"><span data-stu-id="883f7-114">Create a dashboard by using the SDK</span></span>  
 <span data-ttu-id="883f7-115">To create a dashboard, create an instance of `SystemForm` for an organization-owned dashboard, or `UserForm` for a user-owned dashboard.</span><span class="sxs-lookup"><span data-stu-id="883f7-115">To create a dashboard, create an instance of `SystemForm` for an organization-owned dashboard, or `UserForm` for a user-owned dashboard.</span></span> <span data-ttu-id="883f7-116">The following sample shows how to create an organization-owned dashboard.</span><span class="sxs-lookup"><span data-stu-id="883f7-116">The following sample shows how to create an organization-owned dashboard.</span></span>  
  
 [!code-csharp[VisualizationsAndDashboards#CRUDDashboards2](../../snippets/csharp/CRMV8/visualizationsanddashboards/cs/cruddashboards2.cs#cruddashboards2)]  
  
 <span data-ttu-id="883f7-117">For a complete sample, see [Sample: Create, Retrieve, Update and Delete (CRUD) a Dashboard](sample-create-retrieve-update-delete-dashboard.md).</span><span class="sxs-lookup"><span data-stu-id="883f7-117">For a complete sample, see [Sample: Create, Retrieve, Update and Delete (CRUD) a Dashboard](sample-create-retrieve-update-delete-dashboard.md).</span></span> <span data-ttu-id="883f7-118">For a sample to create a user-owned dashboard, and assign it to another user, see [Sample: Assign a User-Owned Dashboard to Another User](sample-assign-user-owned-dashboard-another-user.md).</span><span class="sxs-lookup"><span data-stu-id="883f7-118">For a sample to create a user-owned dashboard, and assign it to another user, see [Sample: Assign a User-Owned Dashboard to Another User](sample-assign-user-owned-dashboard-another-user.md).</span></span>  
  
<a name="UsingFormCustomization"></a>   
## <a name="create-an-organization-owned-dashboard-by-customizing-the-entity-form"></a><span data-ttu-id="883f7-119">Create an organization-owned dashboard by customizing the entity form</span><span class="sxs-lookup"><span data-stu-id="883f7-119">Create an organization-owned dashboard by customizing the entity form</span></span>  
 <span data-ttu-id="883f7-120">The customizations.xml file that is exported with an unmanaged solution contains definitions for entity forms and dashboards.</span><span class="sxs-lookup"><span data-stu-id="883f7-120">The customizations.xml file that is exported with an unmanaged solution contains definitions for entity forms and dashboards.</span></span> <span data-ttu-id="883f7-121">You can add or modify the customizations.xml file to add or update a dashboard.</span><span class="sxs-lookup"><span data-stu-id="883f7-121">You can add or modify the customizations.xml file to add or update a dashboard.</span></span>  
  
#### <a name="create-a-dashboard-by-customizing-an-entity-form"></a><span data-ttu-id="883f7-122">Create a dashboard by customizing an entity form</span><span class="sxs-lookup"><span data-stu-id="883f7-122">Create a dashboard by customizing an entity form</span></span>  
  
1. <span data-ttu-id="883f7-123">Log on to [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)].</span><span class="sxs-lookup"><span data-stu-id="883f7-123">Log on to [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)].</span></span>  
  
2. <span data-ttu-id="883f7-124">Export a solution.</span><span class="sxs-lookup"><span data-stu-id="883f7-124">Export a solution.</span></span> <span data-ttu-id="883f7-125">For information about doing so, see [Exporting, Preparing to Edit, and Importing the Ribbon](export-prepare-edit-import-ribbon.md).</span><span class="sxs-lookup"><span data-stu-id="883f7-125">For information about doing so, see [Exporting, Preparing to Edit, and Importing the Ribbon](export-prepare-edit-import-ribbon.md).</span></span>  
  
3. <span data-ttu-id="883f7-126">Browse to the customizations.xml file in the exported solution folder, and open it for editing.</span><span class="sxs-lookup"><span data-stu-id="883f7-126">Browse to the customizations.xml file in the exported solution folder, and open it for editing.</span></span>  
  
4. <span data-ttu-id="883f7-127">Browse to the end of the dashboards area in the customizations.xml file by searching for the following tag: `</Dashboards>`</span><span class="sxs-lookup"><span data-stu-id="883f7-127">Browse to the end of the dashboards area in the customizations.xml file by searching for the following tag: `</Dashboards>`</span></span>  
  
5. <span data-ttu-id="883f7-128">Before the `</Dashboards>` tag, add the following to define a new dashboard:</span><span class="sxs-lookup"><span data-stu-id="883f7-128">Before the `</Dashboards>` tag, add the following to define a new dashboard:</span></span>  
  
   ```xml  
   <Dashboard>  
      <LocalizedNames>  
         <LocalizedName description="Dashboard_Name" languagecode="1033" />  
      </LocalizedNames>     
      <IsCustomizable>1</IsCustomizable>  
      <IsDefault>0</IsDefault>  
      <FormXml>  
         <forms type="dashboard">  
   *** Dashboard definition goes here. *** // See “Sample Dashboards” topic for the FormXML content to be used here.  
         </forms>  
      </FormXml>  
   </Dashboard>  
   ```  
  
6. <span data-ttu-id="883f7-129">Save the customizations.xml file.</span><span class="sxs-lookup"><span data-stu-id="883f7-129">Save the customizations.xml file.</span></span>  
  
7. <span data-ttu-id="883f7-130">Import the .zip file as a solution in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)].</span><span class="sxs-lookup"><span data-stu-id="883f7-130">Import the .zip file as a solution in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)].</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="883f7-131">[Exporting, Preparing to Edit, and Importing the Ribbon](export-prepare-edit-import-ribbon.md).</span><span class="sxs-lookup"><span data-stu-id="883f7-131">[Exporting, Preparing to Edit, and Importing the Ribbon](export-prepare-edit-import-ribbon.md).</span></span>  
  
<a name="Limitations"></a>   

## <a name="limitations-creating-dashboards-by-using-the-sdk-or-through-form-customization"></a><span data-ttu-id="883f7-132">Limitations: Creating dashboards by using the SDK or through form customization</span><span class="sxs-lookup"><span data-stu-id="883f7-132">Limitations: Creating dashboards by using the SDK or through form customization</span></span>  

 <span data-ttu-id="883f7-133">Certain dashboards that are created or modified using the [!INCLUDE[cc-dyn365-ce-web-services](../../includes/cc-dyn365-ce-web-services.md)] or through form customization are not supported by the dashboard designer in the Web application.</span><span class="sxs-lookup"><span data-stu-id="883f7-133">Certain dashboards that are created or modified using the [!INCLUDE[cc-dyn365-ce-web-services](../../includes/cc-dyn365-ce-web-services.md)] or through form customization are not supported by the dashboard designer in the Web application.</span></span> <span data-ttu-id="883f7-134">Avoid the following while creating or modifying a dashboard using the SDK or through form customization.</span><span class="sxs-lookup"><span data-stu-id="883f7-134">Avoid the following while creating or modifying a dashboard using the SDK or through form customization.</span></span>  
  
### <a name="general"></a><span data-ttu-id="883f7-135">Chung</span><span class="sxs-lookup"><span data-stu-id="883f7-135">General</span></span>  
  
- <span data-ttu-id="883f7-136">**Problem**: You can create a dashboard that contains a tab without any section defined in the FormXML.</span><span class="sxs-lookup"><span data-stu-id="883f7-136">**Problem**: You can create a dashboard that contains a tab without any section defined in the FormXML.</span></span>  
  
  <span data-ttu-id="883f7-137">**Resolution**: Make sure that you create a dashboard with at least one section defined for each tab in the FormXML.</span><span class="sxs-lookup"><span data-stu-id="883f7-137">**Resolution**: Make sure that you create a dashboard with at least one section defined for each tab in the FormXML.</span></span>  
  
- <span data-ttu-id="883f7-138">**Problem**: You can create a dashboard that does not have the same number of `<row>` elements for a section as specified in the `rowspan` property of a `<cell>` element of the section in the FormXML.</span><span class="sxs-lookup"><span data-stu-id="883f7-138">**Problem**: You can create a dashboard that does not have the same number of `<row>` elements for a section as specified in the `rowspan` property of a `<cell>` element of the section in the FormXML.</span></span> <span data-ttu-id="883f7-139">Ideally, the `rowspan` property value of a `<cell>` element and the number of `<row>` elements in a section must be same.</span><span class="sxs-lookup"><span data-stu-id="883f7-139">Ideally, the `rowspan` property value of a `<cell>` element and the number of `<row>` elements in a section must be same.</span></span>  
  
  <span data-ttu-id="883f7-140">**Resolution**: Make sure that you create a dashboard that has the same number of `<row>` elements for a section as specified in the `rowspan` property of a `<cell>` element in the section.</span><span class="sxs-lookup"><span data-stu-id="883f7-140">**Resolution**: Make sure that you create a dashboard that has the same number of `<row>` elements for a section as specified in the `rowspan` property of a `<cell>` element in the section.</span></span>  
  
### <a name="grids"></a><span data-ttu-id="883f7-141">Lưới</span><span class="sxs-lookup"><span data-stu-id="883f7-141">Grids</span></span>  
 <span data-ttu-id="883f7-142">**Problem**: You can create a dashboard that contains grids with the `<AutoExpand>` parameter value set to `Auto` for the grid.</span><span class="sxs-lookup"><span data-stu-id="883f7-142">**Problem**: You can create a dashboard that contains grids with the `<AutoExpand>` parameter value set to `Auto` for the grid.</span></span>  
  
 <span data-ttu-id="883f7-143">**Resolution**: Make sure that you specify the `<AutoExpand>` parameter value as `Fixed` for the grids in the FormXML while creating a dashboard.</span><span class="sxs-lookup"><span data-stu-id="883f7-143">**Resolution**: Make sure that you specify the `<AutoExpand>` parameter value as `Fixed` for the grids in the FormXML while creating a dashboard.</span></span>  
  
### <a name="iframes"></a><span data-ttu-id="883f7-144">Các IFRAME</span><span class="sxs-lookup"><span data-stu-id="883f7-144">IFRAMEs</span></span>  
 <span data-ttu-id="883f7-145">**Problem**: You can create a dashboard that contains an IFRAME.</span><span class="sxs-lookup"><span data-stu-id="883f7-145">**Problem**: You can create a dashboard that contains an IFRAME.</span></span> <span data-ttu-id="883f7-146">This happens when you do not specify any value for the `<Url>` parameter for the IFRAME control in the FormXML.</span><span class="sxs-lookup"><span data-stu-id="883f7-146">This happens when you do not specify any value for the `<Url>` parameter for the IFRAME control in the FormXML.</span></span>  
  
 <span data-ttu-id="883f7-147">**Resolution**: Make sure that you specify a value for the `<Url>` parameter while creating an IFRAME in the FormXML.</span><span class="sxs-lookup"><span data-stu-id="883f7-147">**Resolution**: Make sure that you specify a value for the `<Url>` parameter while creating an IFRAME in the FormXML.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="883f7-148">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="883f7-148">See also</span></span>  
 <span data-ttu-id="883f7-149">[Dashboards for Microsoft Dynamics 365 for Customer Engagement](analyze-data-with-dashboards.md) </span><span class="sxs-lookup"><span data-stu-id="883f7-149">[Dashboards for Microsoft Dynamics 365 for Customer Engagement](analyze-data-with-dashboards.md) </span></span>  
 <span data-ttu-id="883f7-150">[Using FormXML for Dashboards](understand-dashboards-dashboard-components-formxml.md) </span><span class="sxs-lookup"><span data-stu-id="883f7-150">[Using FormXML for Dashboards](understand-dashboards-dashboard-components-formxml.md) </span></span>  
 <span data-ttu-id="883f7-151">[Actions on Dashboards](actions-dashboards.md) </span><span class="sxs-lookup"><span data-stu-id="883f7-151">[Actions on Dashboards](actions-dashboards.md) </span></span>  
 <span data-ttu-id="883f7-152">[Sample dashboards](sample-dashboards.md) </span><span class="sxs-lookup"><span data-stu-id="883f7-152">[Sample dashboards](sample-dashboards.md) </span></span>  
 <span data-ttu-id="883f7-153">[Sample: Create, Retrieve, Update and Delete (CRUD) a Dashboard](sample-create-retrieve-update-delete-dashboard.md) </span><span class="sxs-lookup"><span data-stu-id="883f7-153">[Sample: Create, Retrieve, Update and Delete (CRUD) a Dashboard](sample-create-retrieve-update-delete-dashboard.md) </span></span>  
 [<span data-ttu-id="883f7-154">Customize Entity Forms in Microsoft Dynamics 365 for Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="883f7-154">Customize Entity Forms in Microsoft Dynamics 365 for Customer Engagement</span></span>](customize-entity-forms.md)
