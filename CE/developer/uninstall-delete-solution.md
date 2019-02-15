---
title: Uninstall or delete a solution (Developer Guide for Dynamics 365 for Customer Engagement apps)| MicrosoftDocs
description: This doc describes how uninstall and delete actions work for managed and unmanaged solution in Dynamics 365 for Customer Engagement
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- uninstalling or deleting solutions, deleting unmanaged solutions
- uninstalling or deleting solutions, results of deleting managed vs. unmanaged solutions
- uninstalling or deleting solutions, how to
- deleting managed vs. unmanaged solutions, results of
- uninstalling or deleting solutions, deleting (uninstalling) managed solutions
- deleting (uninstalling) managed solutions
- deleting unmanaged solutions
ms.assetid: 0201e06a-2102-4ea1-a348-93714226e175
caps.latest.revision: 25
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: a7fed6b701478b02db3822361c19813c3128533e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385475"
---
# <a name="uninstall-or-delete-a-solution"></a><span data-ttu-id="efd50-103">Uninstall or delete a solution</span><span class="sxs-lookup"><span data-stu-id="efd50-103">Uninstall or delete a solution</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="efd50-104">You delete managed and unmanaged solutions in the same way, but the resulting actions are very different.</span><span class="sxs-lookup"><span data-stu-id="efd50-104">You delete managed and unmanaged solutions in the same way, but the resulting actions are very different.</span></span> <span data-ttu-id="efd50-105">Deleting a managed solution will uninstall the managed solution.</span><span class="sxs-lookup"><span data-stu-id="efd50-105">Deleting a managed solution will uninstall the managed solution.</span></span>  
  
<a name="BKMK_DeleteSolution"></a>   
## <a name="delete-a-solution"></a><span data-ttu-id="efd50-106">Delete a solution</span><span class="sxs-lookup"><span data-stu-id="efd50-106">Delete a solution</span></span>  
 <span data-ttu-id="efd50-107">Depending on the type of solution that you want to delete, you’ll see one of the following **Confirm Deletion** messages:</span><span class="sxs-lookup"><span data-stu-id="efd50-107">Depending on the type of solution that you want to delete, you’ll see one of the following **Confirm Deletion** messages:</span></span>  
  
 <span data-ttu-id="efd50-108">**Managed solution**</span><span class="sxs-lookup"><span data-stu-id="efd50-108">**Managed solution**</span></span>  
 <span data-ttu-id="efd50-109">“You are deleting a managed solution.</span><span class="sxs-lookup"><span data-stu-id="efd50-109">“You are deleting a managed solution.</span></span> <span data-ttu-id="efd50-110">The solution and all its components will be deleted.</span><span class="sxs-lookup"><span data-stu-id="efd50-110">The solution and all its components will be deleted.</span></span> <span data-ttu-id="efd50-111">This action cannot be undone.</span><span class="sxs-lookup"><span data-stu-id="efd50-111">This action cannot be undone.</span></span> <span data-ttu-id="efd50-112">This solution might take several minutes to uninstall.</span><span class="sxs-lookup"><span data-stu-id="efd50-112">This solution might take several minutes to uninstall.</span></span> <span data-ttu-id="efd50-113">You cannot cancel the uninstallation after it starts.</span><span class="sxs-lookup"><span data-stu-id="efd50-113">You cannot cancel the uninstallation after it starts.</span></span> <span data-ttu-id="efd50-114">Do you want to continue?”</span><span class="sxs-lookup"><span data-stu-id="efd50-114">Do you want to continue?”</span></span>  
  
 <span data-ttu-id="efd50-115">**Unmanaged solution**</span><span class="sxs-lookup"><span data-stu-id="efd50-115">**Unmanaged solution**</span></span>  
 <span data-ttu-id="efd50-116">“You are deleting an unmanaged solution.</span><span class="sxs-lookup"><span data-stu-id="efd50-116">“You are deleting an unmanaged solution.</span></span> <span data-ttu-id="efd50-117">The solution will be deleted but components that are contained in this solution will not be deleted.</span><span class="sxs-lookup"><span data-stu-id="efd50-117">The solution will be deleted but components that are contained in this solution will not be deleted.</span></span> <span data-ttu-id="efd50-118">This action cannot be undone.</span><span class="sxs-lookup"><span data-stu-id="efd50-118">This action cannot be undone.</span></span> <span data-ttu-id="efd50-119">Do you want to continue?”</span><span class="sxs-lookup"><span data-stu-id="efd50-119">Do you want to continue?”</span></span>  
  
 <span data-ttu-id="efd50-120">To delete a solution programmatically use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*></span><span class="sxs-lookup"><span data-stu-id="efd50-120">To delete a solution programmatically use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*></span></span> <span data-ttu-id="efd50-121">method.</span><span class="sxs-lookup"><span data-stu-id="efd50-121">method.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="efd50-122">[Delete a Solution](work-solutions.md#BKMK_DeleteSolution)</span><span class="sxs-lookup"><span data-stu-id="efd50-122">[Delete a Solution](work-solutions.md#BKMK_DeleteSolution)</span></span>  
  
<a name="BKMK_UinstallAManagedSolution"></a>   
### <a name="uninstall-a-managed-solution"></a><span data-ttu-id="efd50-123">Uninstall a managed solution</span><span class="sxs-lookup"><span data-stu-id="efd50-123">Uninstall a managed solution</span></span>  
 <span data-ttu-id="efd50-124">Deleting a managed solution will uninstall the solution.</span><span class="sxs-lookup"><span data-stu-id="efd50-124">Deleting a managed solution will uninstall the solution.</span></span> <span data-ttu-id="efd50-125">All the solution components defined in it are deleted.</span><span class="sxs-lookup"><span data-stu-id="efd50-125">All the solution components defined in it are deleted.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="efd50-126">When you uninstall a managed solution, the following data is lost: data stored in custom entities that are part of the solution and data stored in custom attributes on system entities that are part of the solution.</span><span class="sxs-lookup"><span data-stu-id="efd50-126">When you uninstall a managed solution, the following data is lost: data stored in custom entities that are part of the solution and data stored in custom attributes on system entities that are part of the solution.</span></span>  
  
<a name="BKMK_DeleteUnmanagedSolution"></a>   
### <a name="delete-an-unmanaged-solution"></a><span data-ttu-id="efd50-127">Delete an unmanaged solution</span><span class="sxs-lookup"><span data-stu-id="efd50-127">Delete an unmanaged solution</span></span>  
 <span data-ttu-id="efd50-128">An unmanaged solution is a group of solution components.</span><span class="sxs-lookup"><span data-stu-id="efd50-128">An unmanaged solution is a group of solution components.</span></span> <span data-ttu-id="efd50-129">Deleting the solution deletes a single solution record in the database.</span><span class="sxs-lookup"><span data-stu-id="efd50-129">Deleting the solution deletes a single solution record in the database.</span></span> <span data-ttu-id="efd50-130">Solution components are not affected by the solution being deleted, they remain in the system.</span><span class="sxs-lookup"><span data-stu-id="efd50-130">Solution components are not affected by the solution being deleted, they remain in the system.</span></span>  
  
<a name="BKMK_AccessSolutionsGridWithUrl"></a>   
## <a name="access-the-solutions-list-with-a-url"></a><span data-ttu-id="efd50-131">Access the solutions list with a URL</span><span class="sxs-lookup"><span data-stu-id="efd50-131">Access the solutions list with a URL</span></span>  
 <span data-ttu-id="efd50-132">If you need to navigate directly to the solutions list you can use the following URL:</span><span class="sxs-lookup"><span data-stu-id="efd50-132">If you need to navigate directly to the solutions list you can use the following URL:</span></span>  
  
```
<organization root url>/tools/Solution/home_solution.aspx?etn=solution  
```  
  
### <a name="see-also"></a><span data-ttu-id="efd50-133">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="efd50-133">See also</span></span>  
 <span data-ttu-id="efd50-134">[Package and Distribute Extensions with Dynamics 365 for Customer Engagement Solutions](package-distribute-extensions-use-solutions.md) </span><span class="sxs-lookup"><span data-stu-id="efd50-134">[Package and Distribute Extensions with Dynamics 365 for Customer Engagement Solutions](package-distribute-extensions-use-solutions.md) </span></span>  
 <span data-ttu-id="efd50-135">[Delete a Solution](work-solutions.md#BKMK_DeleteSolution) </span><span class="sxs-lookup"><span data-stu-id="efd50-135">[Delete a Solution](work-solutions.md#BKMK_DeleteSolution) </span></span>  
 <span data-ttu-id="efd50-136">[Introduction to Solutions](introduction-solutions.md) </span><span class="sxs-lookup"><span data-stu-id="efd50-136">[Introduction to Solutions](introduction-solutions.md) </span></span>  
 <span data-ttu-id="efd50-137">[Planning for Solution Development](plan-solution-development.md) </span><span class="sxs-lookup"><span data-stu-id="efd50-137">[Planning for Solution Development](plan-solution-development.md) </span></span>  
 <span data-ttu-id="efd50-138">[Solution Components and Dependency Tracking](dependency-tracking-solution-components.md) </span><span class="sxs-lookup"><span data-stu-id="efd50-138">[Solution Components and Dependency Tracking](dependency-tracking-solution-components.md) </span></span>  
 <span data-ttu-id="efd50-139">[Create a Managed Solution](create-install-update-managed-solution.md#BKMK_CreateManagedSolution) </span><span class="sxs-lookup"><span data-stu-id="efd50-139">[Create a Managed Solution](create-install-update-managed-solution.md#BKMK_CreateManagedSolution) </span></span>  
 <span data-ttu-id="efd50-140">[Export an unmanaged solution](create-export-import-unmanaged-solution.md#BKMK_UnmanagedSolution) </span><span class="sxs-lookup"><span data-stu-id="efd50-140">[Export an unmanaged solution](create-export-import-unmanaged-solution.md#BKMK_UnmanagedSolution) </span></span>  
 <span data-ttu-id="efd50-141">[Import an unmanaged solution](create-export-import-unmanaged-solution.md#BKMK_ImportUnmanagedSolution) </span><span class="sxs-lookup"><span data-stu-id="efd50-141">[Import an unmanaged solution](create-export-import-unmanaged-solution.md#BKMK_ImportUnmanagedSolution) </span></span>  
 <span data-ttu-id="efd50-142">[Create a Managed Solution](create-install-update-managed-solution.md#BKMK_CreateManagedSolution) </span><span class="sxs-lookup"><span data-stu-id="efd50-142">[Create a Managed Solution](create-install-update-managed-solution.md#BKMK_CreateManagedSolution) </span></span>  
 <span data-ttu-id="efd50-143">[Create Solutions that Support Multiple Languages](create-solutions-support-multiple-languages.md) </span><span class="sxs-lookup"><span data-stu-id="efd50-143">[Create Solutions that Support Multiple Languages](create-solutions-support-multiple-languages.md) </span></span>  
 [<span data-ttu-id="efd50-144">Install a Managed Solution</span><span class="sxs-lookup"><span data-stu-id="efd50-144">Install a Managed Solution</span></span>](create-install-update-managed-solution.md#BKMK_InstallManagedSolution)
