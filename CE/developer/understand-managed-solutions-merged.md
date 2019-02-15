---
title: Understand how managed solutions are merged (Developer Guide for Dynamics 365 for Customer Engagement apps)| MicrosoftDocs
description: To avoid multiple installed solutions from interfering with one another, follow best practices while constructing a solution
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 79c15784-56d2-46b0-bc78-b60c3d01cbb6
caps.latest.revision: 27
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 080a8609e27f259fd3fd96d6040b166aa18c00e8
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386365"
---
# <a name="understand-how-managed-solutions-are-merged"></a><span data-ttu-id="d37cf-103">Understand how managed solutions are merged</span><span class="sxs-lookup"><span data-stu-id="d37cf-103">Understand how managed solutions are merged</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="d37cf-104">When you prepare your managed solution to be installed, remember that an organization may have multiple solutions installed or that other solutions may be installed in the future.</span><span class="sxs-lookup"><span data-stu-id="d37cf-104">When you prepare your managed solution to be installed, remember that an organization may have multiple solutions installed or that other solutions may be installed in the future.</span></span> <span data-ttu-id="d37cf-105">Construct a solution that follows best practices so that your solution will not interfere with other solutions.</span><span class="sxs-lookup"><span data-stu-id="d37cf-105">Construct a solution that follows best practices so that your solution will not interfere with other solutions.</span></span>  
  
 <span data-ttu-id="d37cf-106">The processes that [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Engagement uses to merge customizations emphasize maintaining the functionality of the solution.</span><span class="sxs-lookup"><span data-stu-id="d37cf-106">The processes that [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Engagement uses to merge customizations emphasize maintaining the functionality of the solution.</span></span> <span data-ttu-id="d37cf-107">While every effort is made to preserve the presentation, some incompatibilities between customizations may require that the computed resolution will change some presentation details in favor of maintaining the customization functionality.</span><span class="sxs-lookup"><span data-stu-id="d37cf-107">While every effort is made to preserve the presentation, some incompatibilities between customizations may require that the computed resolution will change some presentation details in favor of maintaining the customization functionality.</span></span>  
  
<a name="BKMK_MergingFormCustomizations"></a>   
## <a name="merge-form-customizations"></a><span data-ttu-id="d37cf-108">Merge form customizations</span><span class="sxs-lookup"><span data-stu-id="d37cf-108">Merge form customizations</span></span>  
 <span data-ttu-id="d37cf-109">The only form customizations that have to be merged are those that are performed on any entity forms that are already in the organization.</span><span class="sxs-lookup"><span data-stu-id="d37cf-109">The only form customizations that have to be merged are those that are performed on any entity forms that are already in the organization.</span></span> <span data-ttu-id="d37cf-110">Typically, this means that form customizations only have to be merged when your solution customizes the forms that were included for entities created when [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] was installed.</span><span class="sxs-lookup"><span data-stu-id="d37cf-110">Typically, this means that form customizations only have to be merged when your solution customizes the forms that were included for entities created when [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] was installed.</span></span> <span data-ttu-id="d37cf-111">One way to avoid form merging is to provide new forms for any [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] entities.</span><span class="sxs-lookup"><span data-stu-id="d37cf-111">One way to avoid form merging is to provide new forms for any [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] entities.</span></span> <span data-ttu-id="d37cf-112">Forms for custom entities will not require merging unless you are creating a solution that updates or modifies an existing managed solution that created the custom entities and their forms.</span><span class="sxs-lookup"><span data-stu-id="d37cf-112">Forms for custom entities will not require merging unless you are creating a solution that updates or modifies an existing managed solution that created the custom entities and their forms.</span></span>  
  
 <span data-ttu-id="d37cf-113">When a solution is packaged as a managed solution the form definitions stored in FormXML are compared to the original FormXML and only the differences are included in the managed solution.</span><span class="sxs-lookup"><span data-stu-id="d37cf-113">When a solution is packaged as a managed solution the form definitions stored in FormXML are compared to the original FormXML and only the differences are included in the managed solution.</span></span> <span data-ttu-id="d37cf-114">When the managed solution is installed in a new organization, the form customization differences are then merged with the FormXML for the existing form to create a new form definition.</span><span class="sxs-lookup"><span data-stu-id="d37cf-114">When the managed solution is installed in a new organization, the form customization differences are then merged with the FormXML for the existing form to create a new form definition.</span></span> <span data-ttu-id="d37cf-115">This new form definition is what the user sees and what a system customizer can modify.</span><span class="sxs-lookup"><span data-stu-id="d37cf-115">This new form definition is what the user sees and what a system customizer can modify.</span></span> <span data-ttu-id="d37cf-116">When the managed solution is uninstalled, only those form elements found in the managed solution are removed.</span><span class="sxs-lookup"><span data-stu-id="d37cf-116">When the managed solution is uninstalled, only those form elements found in the managed solution are removed.</span></span>  
  
 <span data-ttu-id="d37cf-117">When you add new elements to a form that is to be merged, we recommend that you include your new elements within new container elements (tabs or sections).</span><span class="sxs-lookup"><span data-stu-id="d37cf-117">When you add new elements to a form that is to be merged, we recommend that you include your new elements within new container elements (tabs or sections).</span></span> <span data-ttu-id="d37cf-118">Additions to any container will be appended to the end of the container.</span><span class="sxs-lookup"><span data-stu-id="d37cf-118">Additions to any container will be appended to the end of the container.</span></span> <span data-ttu-id="d37cf-119">For example, fields added to a section will be positioned at the end of the section.</span><span class="sxs-lookup"><span data-stu-id="d37cf-119">For example, fields added to a section will be positioned at the end of the section.</span></span> <span data-ttu-id="d37cf-120">It is expected that a customizer installing a solution will then modify the form to re-arrange elements after it is installed.</span><span class="sxs-lookup"><span data-stu-id="d37cf-120">It is expected that a customizer installing a solution will then modify the form to re-arrange elements after it is installed.</span></span>  
  
 <span data-ttu-id="d37cf-121">Managed solutions that contain forms that use new security roles depend on those roles.</span><span class="sxs-lookup"><span data-stu-id="d37cf-121">Managed solutions that contain forms that use new security roles depend on those roles.</span></span> <span data-ttu-id="d37cf-122">You should include these security roles with your managed solution.</span><span class="sxs-lookup"><span data-stu-id="d37cf-122">You should include these security roles with your managed solution.</span></span> <span data-ttu-id="d37cf-123">If there are security roles associated with a form that are not in the organization that the managed solution is being installed on, the installation will not fail but the forms may not be associated with any security roles.</span><span class="sxs-lookup"><span data-stu-id="d37cf-123">If there are security roles associated with a form that are not in the organization that the managed solution is being installed on, the installation will not fail but the forms may not be associated with any security roles.</span></span> <span data-ttu-id="d37cf-124">When the managed solution is uninstalled, any security roles included with it will be removed.</span><span class="sxs-lookup"><span data-stu-id="d37cf-124">When the managed solution is uninstalled, any security roles included with it will be removed.</span></span> <span data-ttu-id="d37cf-125">Any forms outside the managed solution can no longer be associated with those security roles.</span><span class="sxs-lookup"><span data-stu-id="d37cf-125">Any forms outside the managed solution can no longer be associated with those security roles.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d37cf-126">When a managed solution entity contains multiple forms and the organization entity form also contains multiple forms, the new forms are not appended to the bottom of the list of available forms – they are interleaved with the original entity forms.</span><span class="sxs-lookup"><span data-stu-id="d37cf-126">When a managed solution entity contains multiple forms and the organization entity form also contains multiple forms, the new forms are not appended to the bottom of the list of available forms – they are interleaved with the original entity forms.</span></span>  
  
<a name="BKMK_MergingNavigationCustomizations"></a>   
## <a name="merge-navigation-sitemap-customizations"></a><span data-ttu-id="d37cf-127">Merge navigation (SiteMap) customizations</span><span class="sxs-lookup"><span data-stu-id="d37cf-127">Merge navigation (SiteMap) customizations</span></span>  
 <span data-ttu-id="d37cf-128">When a solution is packaged as managed the SiteMap XML is compared to the original SiteMap XML and any other customizations made to the SiteMap.</span><span class="sxs-lookup"><span data-stu-id="d37cf-128">When a solution is packaged as managed the SiteMap XML is compared to the original SiteMap XML and any other customizations made to the SiteMap.</span></span> <span data-ttu-id="d37cf-129">Only the differences are included in the managed solution.</span><span class="sxs-lookup"><span data-stu-id="d37cf-129">Only the differences are included in the managed solution.</span></span> <span data-ttu-id="d37cf-130">These differences include items that are changed, moved, added or removed.</span><span class="sxs-lookup"><span data-stu-id="d37cf-130">These differences include items that are changed, moved, added or removed.</span></span> <span data-ttu-id="d37cf-131">When the managed solution is installed in a new organization, the SiteMap changes are merged with the SiteMap XML found for the organization where the managed solution is being installed.</span><span class="sxs-lookup"><span data-stu-id="d37cf-131">When the managed solution is installed in a new organization, the SiteMap changes are merged with the SiteMap XML found for the organization where the managed solution is being installed.</span></span> <span data-ttu-id="d37cf-132">A new SiteMap definition is what people see.</span><span class="sxs-lookup"><span data-stu-id="d37cf-132">A new SiteMap definition is what people see.</span></span>  
  
 <span data-ttu-id="d37cf-133">At this point, a customizer can export the SiteMap to an unmanaged solution and that SiteMap definition will include all the elements of the active SiteMap.</span><span class="sxs-lookup"><span data-stu-id="d37cf-133">At this point, a customizer can export the SiteMap to an unmanaged solution and that SiteMap definition will include all the elements of the active SiteMap.</span></span> <span data-ttu-id="d37cf-134">A customizer can then modify the SiteMap and re-import it as an unmanaged customization.</span><span class="sxs-lookup"><span data-stu-id="d37cf-134">A customizer can then modify the SiteMap and re-import it as an unmanaged customization.</span></span>  <span data-ttu-id="d37cf-135">Later, if the managed solution is uninstalled, the SiteMap XML that was imported with the managed solution will be referenced to remove the changes introduced with that managed solution.</span><span class="sxs-lookup"><span data-stu-id="d37cf-135">Later, if the managed solution is uninstalled, the SiteMap XML that was imported with the managed solution will be referenced to remove the changes introduced with that managed solution.</span></span> <span data-ttu-id="d37cf-136">A new active SiteMap is then calculated.</span><span class="sxs-lookup"><span data-stu-id="d37cf-136">A new active SiteMap is then calculated.</span></span>  
  
 <span data-ttu-id="d37cf-137">Whenever a new visible element is added to the SiteMap, it appears at the bottom of whatever container it belongs in.</span><span class="sxs-lookup"><span data-stu-id="d37cf-137">Whenever a new visible element is added to the SiteMap, it appears at the bottom of whatever container it belongs in.</span></span> <span data-ttu-id="d37cf-138">For example, a new area appears at the bottom of the Navigation area.</span><span class="sxs-lookup"><span data-stu-id="d37cf-138">For example, a new area appears at the bottom of the Navigation area.</span></span> <span data-ttu-id="d37cf-139">To position the elements that have been added, you must export the SiteMap, edit it to set the precise position and then import it again as an unmanaged solution.</span><span class="sxs-lookup"><span data-stu-id="d37cf-139">To position the elements that have been added, you must export the SiteMap, edit it to set the precise position and then import it again as an unmanaged solution.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d37cf-140">Only one SiteMap customization can be applied between publishing.</span><span class="sxs-lookup"><span data-stu-id="d37cf-140">Only one SiteMap customization can be applied between publishing.</span></span> <span data-ttu-id="d37cf-141">Any unpublished SiteMap customizations will be lost when a new SiteMap definition is imported.</span><span class="sxs-lookup"><span data-stu-id="d37cf-141">Any unpublished SiteMap customizations will be lost when a new SiteMap definition is imported.</span></span>  
  
<a name="BKMK_MergingOptionSetOptions"></a>   
## <a name="merge-option-set-options"></a><span data-ttu-id="d37cf-142">Merge option set options</span><span class="sxs-lookup"><span data-stu-id="d37cf-142">Merge option set options</span></span>  
 <span data-ttu-id="d37cf-143">Each new option set option is initialized with an integer value assigned that includes an option value prefix.</span><span class="sxs-lookup"><span data-stu-id="d37cf-143">Each new option set option is initialized with an integer value assigned that includes an option value prefix.</span></span> <span data-ttu-id="d37cf-144">The option value prefix is a set of five digits prepended to the option value.</span><span class="sxs-lookup"><span data-stu-id="d37cf-144">The option value prefix is a set of five digits prepended to the option value.</span></span> <span data-ttu-id="d37cf-145">An option value prefix is generated based on the solution publishers customization prefix but may be set to any value.</span><span class="sxs-lookup"><span data-stu-id="d37cf-145">An option value prefix is generated based on the solution publishers customization prefix but may be set to any value.</span></span> <span data-ttu-id="d37cf-146">The option value prefix helps differentiate new option set options created in the context of a specific solution publisher and reduces the opportunity for collisions of option values.</span><span class="sxs-lookup"><span data-stu-id="d37cf-146">The option value prefix helps differentiate new option set options created in the context of a specific solution publisher and reduces the opportunity for collisions of option values.</span></span> <span data-ttu-id="d37cf-147">Using the option value prefix is recommended but not required.</span><span class="sxs-lookup"><span data-stu-id="d37cf-147">Using the option value prefix is recommended but not required.</span></span>  
  
 <span data-ttu-id="d37cf-148">A managed solution usually updates or adds options for option sets that are already in the organization, for example, the account Category or Industry option sets.</span><span class="sxs-lookup"><span data-stu-id="d37cf-148">A managed solution usually updates or adds options for option sets that are already in the organization, for example, the account Category or Industry option sets.</span></span> <span data-ttu-id="d37cf-149">When a managed solution modifies the options available in an option set, all the options defined in the managed solution are available in the organization.</span><span class="sxs-lookup"><span data-stu-id="d37cf-149">When a managed solution modifies the options available in an option set, all the options defined in the managed solution are available in the organization.</span></span> <span data-ttu-id="d37cf-150">When the managed solution is uninstalled, the option set options will be returned to their original state.</span><span class="sxs-lookup"><span data-stu-id="d37cf-150">When the managed solution is uninstalled, the option set options will be returned to their original state.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="d37cf-151">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="d37cf-151">See also</span></span>  
 <span data-ttu-id="d37cf-152">[Plan for Solution Development](plan-solution-development.md) </span><span class="sxs-lookup"><span data-stu-id="d37cf-152">[Plan for Solution Development](plan-solution-development.md) </span></span>  
 <span data-ttu-id="d37cf-153">[Use Managed Properties](use-managed-properties.md) </span><span class="sxs-lookup"><span data-stu-id="d37cf-153">[Use Managed Properties](use-managed-properties.md) </span></span>  
 <span data-ttu-id="d37cf-154">[Package and Distribute Extensions with Dynamics 365 for Customer Engagement Solutions](package-distribute-extensions-use-solutions.md) </span><span class="sxs-lookup"><span data-stu-id="d37cf-154">[Package and Distribute Extensions with Dynamics 365 for Customer Engagement Solutions](package-distribute-extensions-use-solutions.md) </span></span>  
 <span data-ttu-id="d37cf-155">[Customize Entity Forms in Dynamics 365 for Customer Engagement apps](customize-dev/customize-entity-forms.md) </span><span class="sxs-lookup"><span data-stu-id="d37cf-155">[Customize Entity Forms in Dynamics 365 for Customer Engagement apps](customize-dev/customize-entity-forms.md) </span></span>  
 [<span data-ttu-id="d37cf-156">Change Application Navigation using the SiteMap</span><span class="sxs-lookup"><span data-stu-id="d37cf-156">Change Application Navigation using the SiteMap</span></span>](/developer/customize-dev/change-application-navigation-using-sitemap.md)