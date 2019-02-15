---
title: Maintain managed solutions (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 25aab712-8e0e-465e-8295-b0f0664c1d0b
caps.latest.revision: 40
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: c6107e6f048a7d90a996474c37f3766fe1876d44
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386203"
---
# <a name="maintain-managed-solutions"></a><span data-ttu-id="6b680-102">Maintain managed solutions</span><span class="sxs-lookup"><span data-stu-id="6b680-102">Maintain managed solutions</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="6b680-103">Before you release your managed solution you should consider how you will maintain it.</span><span class="sxs-lookup"><span data-stu-id="6b680-103">Before you release your managed solution you should consider how you will maintain it.</span></span> <span data-ttu-id="6b680-104">Uninstalling and reinstalling a managed solution is practically never an option when the solution contains entities or attributes.</span><span class="sxs-lookup"><span data-stu-id="6b680-104">Uninstalling and reinstalling a managed solution is practically never an option when the solution contains entities or attributes.</span></span> <span data-ttu-id="6b680-105">This is because data is lost when entities are deleted.</span><span class="sxs-lookup"><span data-stu-id="6b680-105">This is because data is lost when entities are deleted.</span></span> <span data-ttu-id="6b680-106">Fortunately, solutions provide a way to update your managed solution while maintaining the data.</span><span class="sxs-lookup"><span data-stu-id="6b680-106">Fortunately, solutions provide a way to update your managed solution while maintaining the data.</span></span> <span data-ttu-id="6b680-107">Exactly how you update your solutions will depend on the characteristics of the solution and the requirements of the change.</span><span class="sxs-lookup"><span data-stu-id="6b680-107">Exactly how you update your solutions will depend on the characteristics of the solution and the requirements of the change.</span></span>  

<a name="BKMK_VersionCompatibilty"></a>   
## <a name="version-compatibility"></a><span data-ttu-id="6b680-108">Version compatibility</span><span class="sxs-lookup"><span data-stu-id="6b680-108">Version compatibility</span></span>  
 <span data-ttu-id="6b680-109">Any solution exported from a newer version of [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps cannot be imported into an older version of Dynamics 365 for Customer Engagement apps.</span><span class="sxs-lookup"><span data-stu-id="6b680-109">Any solution exported from a newer version of [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps cannot be imported into an older version of Dynamics 365 for Customer Engagement apps.</span></span> <span data-ttu-id="6b680-110">This includes major and minor versions.</span><span class="sxs-lookup"><span data-stu-id="6b680-110">This includes major and minor versions.</span></span> <span data-ttu-id="6b680-111">Solutions exported from an earlier version of Dynamics 365 for Customer Engagement apps can be imported into later versions as shown in the following chart.</span><span class="sxs-lookup"><span data-stu-id="6b680-111">Solutions exported from an earlier version of Dynamics 365 for Customer Engagement apps can be imported into later versions as shown in the following chart.</span></span>  
  
![Solution version compatiblity](media/crm_v9.0_solution_compatibility_chart.png)


> [!NOTE]
> <span data-ttu-id="6b680-113">For information about solutions created before [!INCLUDE [pn-crm-2015](../includes/pn-crm-2015.md)] see [Dynamics CRM 2016 Maintain managed solutions > Version compatiblity](https://msdn.microsoft.com/library/gg328109.aspx#BKMK_VersionCompatibilty)</span><span class="sxs-lookup"><span data-stu-id="6b680-113">For information about solutions created before [!INCLUDE [pn-crm-2015](../includes/pn-crm-2015.md)] see [Dynamics CRM 2016 Maintain managed solutions > Version compatiblity](https://msdn.microsoft.com/library/gg328109.aspx#BKMK_VersionCompatibilty)</span></span>
  
 <span data-ttu-id="6b680-114">As additional update rollups or service updates are applied to [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps, solutions exported from organizations with those updates cannot be imported into organizations which do not have those updates.</span><span class="sxs-lookup"><span data-stu-id="6b680-114">As additional update rollups or service updates are applied to [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps, solutions exported from organizations with those updates cannot be imported into organizations which do not have those updates.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="6b680-115">[Introduction to Solutions: Version compatibility](introduction-solutions.md#BKMK_VersionCompat).</span><span class="sxs-lookup"><span data-stu-id="6b680-115">[Introduction to Solutions: Version compatibility](introduction-solutions.md#BKMK_VersionCompat).</span></span>  
  
 <span data-ttu-id="6b680-116">The `<ImportExportXml>` root element uses a `SolutionPackageVersion` attribute to set the value for the version that the solution is compatible with.</span><span class="sxs-lookup"><span data-stu-id="6b680-116">The `<ImportExportXml>` root element uses a `SolutionPackageVersion` attribute to set the value for the version that the solution is compatible with.</span></span> <span data-ttu-id="6b680-117">You should not manually edit this value.</span><span class="sxs-lookup"><span data-stu-id="6b680-117">You should not manually edit this value.</span></span>  
  
<a name="BKMK_CreateManagedSolutionUpdates"></a>   
## <a name="create-managed-solution-updates"></a><span data-ttu-id="6b680-118">Create managed solution updates</span><span class="sxs-lookup"><span data-stu-id="6b680-118">Create managed solution updates</span></span>  
 <span data-ttu-id="6b680-119">There are two basic approaches to updating solutions:</span><span class="sxs-lookup"><span data-stu-id="6b680-119">There are two basic approaches to updating solutions:</span></span>  
  
-   <span data-ttu-id="6b680-120">Release a new version of your managed solution</span><span class="sxs-lookup"><span data-stu-id="6b680-120">Release a new version of your managed solution</span></span>  
  
-   <span data-ttu-id="6b680-121">Release an update for your managed solution</span><span class="sxs-lookup"><span data-stu-id="6b680-121">Release an update for your managed solution</span></span>  
  
<a name="BKMK_ReleaseANewVersion"></a>   
### <a name="release-a-new-version-of-your-managed-solution"></a><span data-ttu-id="6b680-122">Release a new version of your managed solution</span><span class="sxs-lookup"><span data-stu-id="6b680-122">Release a new version of your managed solution</span></span>  
 <span data-ttu-id="6b680-123">The preferred method is to release a new version of your managed solution.</span><span class="sxs-lookup"><span data-stu-id="6b680-123">The preferred method is to release a new version of your managed solution.</span></span> <span data-ttu-id="6b680-124">Using your original unmanaged source solution, you can make necessary changes and increase the version number of the solution before packaging it as a managed solution.</span><span class="sxs-lookup"><span data-stu-id="6b680-124">Using your original unmanaged source solution, you can make necessary changes and increase the version number of the solution before packaging it as a managed solution.</span></span> <span data-ttu-id="6b680-125">When the organizations that use your solution install the new version, their capabilities will be upgraded to include your changes.</span><span class="sxs-lookup"><span data-stu-id="6b680-125">When the organizations that use your solution install the new version, their capabilities will be upgraded to include your changes.</span></span> <span data-ttu-id="6b680-126">If you want to go back to the behavior in a previous version, simply re-install the previous version.</span><span class="sxs-lookup"><span data-stu-id="6b680-126">If you want to go back to the behavior in a previous version, simply re-install the previous version.</span></span> <span data-ttu-id="6b680-127">This overwrites any solution components with the definitions from the previous version but does not remove solution components added in the newer version.</span><span class="sxs-lookup"><span data-stu-id="6b680-127">This overwrites any solution components with the definitions from the previous version but does not remove solution components added in the newer version.</span></span> <span data-ttu-id="6b680-128">Those newer solution components remain in the system but have no effect because the older solution component definitions will not use them.</span><span class="sxs-lookup"><span data-stu-id="6b680-128">Those newer solution components remain in the system but have no effect because the older solution component definitions will not use them.</span></span>  
  
 <span data-ttu-id="6b680-129">During the installation of a previous version of a solution [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps will confirm that the person installing the previous version wants to proceed.</span><span class="sxs-lookup"><span data-stu-id="6b680-129">During the installation of a previous version of a solution [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps will confirm that the person installing the previous version wants to proceed.</span></span>  
  
<a name="BKMK_ReleaseAnUpdate"></a>   
### <a name="release-an-update-for-your-managed-solution"></a><span data-ttu-id="6b680-130">Release an update for your managed solution</span><span class="sxs-lookup"><span data-stu-id="6b680-130">Release an update for your managed solution</span></span>  
 <span data-ttu-id="6b680-131">When only a small subset of solution components urgently requires a change you can release an update to address the issue.</span><span class="sxs-lookup"><span data-stu-id="6b680-131">When only a small subset of solution components urgently requires a change you can release an update to address the issue.</span></span> <span data-ttu-id="6b680-132">To release an update, create a new unmanaged solution and add any components from the original unmanaged source solution that you want to update.</span><span class="sxs-lookup"><span data-stu-id="6b680-132">To release an update, create a new unmanaged solution and add any components from the original unmanaged source solution that you want to update.</span></span> <span data-ttu-id="6b680-133">You must associate the new unmanaged solution with the same publisher record as was used for the original solution.</span><span class="sxs-lookup"><span data-stu-id="6b680-133">You must associate the new unmanaged solution with the same publisher record as was used for the original solution.</span></span> <span data-ttu-id="6b680-134">After you finish with your changes, package the new solution as a managed solution.</span><span class="sxs-lookup"><span data-stu-id="6b680-134">After you finish with your changes, package the new solution as a managed solution.</span></span>  
  
 <span data-ttu-id="6b680-135">When the update solution is installed in an organization where the original solution was installed the changes included in the update will be applied to the organization.</span><span class="sxs-lookup"><span data-stu-id="6b680-135">When the update solution is installed in an organization where the original solution was installed the changes included in the update will be applied to the organization.</span></span> <span data-ttu-id="6b680-136">If an organization needs to ‘roll back’ to the original version they can simply uninstall the update.</span><span class="sxs-lookup"><span data-stu-id="6b680-136">If an organization needs to ‘roll back’ to the original version they can simply uninstall the update.</span></span>  
  
 <span data-ttu-id="6b680-137">Any customizations applied to the solution components in the update will be overridden.</span><span class="sxs-lookup"><span data-stu-id="6b680-137">Any customizations applied to the solution components in the update will be overridden.</span></span> <span data-ttu-id="6b680-138">When you uninstall the update they will return.</span><span class="sxs-lookup"><span data-stu-id="6b680-138">When you uninstall the update they will return.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="6b680-139">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="6b680-139">See also</span></span>  
 <span data-ttu-id="6b680-140">[Plan For Solution Development](plan-solution-development.md) </span><span class="sxs-lookup"><span data-stu-id="6b680-140">[Plan For Solution Development](plan-solution-development.md) </span></span>  
 [<span data-ttu-id="6b680-141">Publish your app on AppSource</span><span class="sxs-lookup"><span data-stu-id="6b680-141">Publish your app on AppSource</span></span>](publish-app-appsource.md)
