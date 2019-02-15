---
title: Organize your solutions (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: This document lists down some strategies to organize your solutions
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
- solutions, multiple solutions with some shared components
- solution libraries
- compartmentalizing your solutions, multiple solutions with some shared components
- solutions, compartmentalizing
- compartmentalizing your solutions, strategies for
- compartmentalizing your solutions, solution libraries
ms.assetid: 5ed0e4b8-8747-410a-afbe-beef147d986d
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: eceb5d0afb09aad7cc90acb261c37250b7bcb5d8
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385567"
---
# <a name="organize-your-solutions"></a><span data-ttu-id="ddebb-103">Organize your solutions</span><span class="sxs-lookup"><span data-stu-id="ddebb-103">Organize your solutions</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="ddebb-104">Before you create solutions, take some time to plan ahead.</span><span class="sxs-lookup"><span data-stu-id="ddebb-104">Before you create solutions, take some time to plan ahead.</span></span> <span data-ttu-id="ddebb-105">For example, think about how many solutions you want to release and whether the solutions will share components.</span><span class="sxs-lookup"><span data-stu-id="ddebb-105">For example, think about how many solutions you want to release and whether the solutions will share components.</span></span>  
  
 <span data-ttu-id="ddebb-106">Also, determine how many [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps organizations you’ll need to develop your line of solutions.</span><span class="sxs-lookup"><span data-stu-id="ddebb-106">Also, determine how many [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps organizations you’ll need to develop your line of solutions.</span></span> <span data-ttu-id="ddebb-107">You can use a single organization for most strategies described in this topic.</span><span class="sxs-lookup"><span data-stu-id="ddebb-107">You can use a single organization for most strategies described in this topic.</span></span> <span data-ttu-id="ddebb-108">However, if you decide to have only one organization and later realize that you need more, it can be challenging to change the solutions if people have already installed them.</span><span class="sxs-lookup"><span data-stu-id="ddebb-108">However, if you decide to have only one organization and later realize that you need more, it can be challenging to change the solutions if people have already installed them.</span></span> <span data-ttu-id="ddebb-109">Using multiple organizations, although introducing more complexity, can provide better flexibility.</span><span class="sxs-lookup"><span data-stu-id="ddebb-109">Using multiple organizations, although introducing more complexity, can provide better flexibility.</span></span>  
  
<a name="BKMK_OptionsToModularize"></a>   
## <a name="strategies-to-organize-your-solutions"></a><span data-ttu-id="ddebb-110">Strategies to organize your solutions</span><span class="sxs-lookup"><span data-stu-id="ddebb-110">Strategies to organize your solutions</span></span>  
 <span data-ttu-id="ddebb-111">The following are some strategies for creating solutions listed in order from simplest to most complex:</span><span class="sxs-lookup"><span data-stu-id="ddebb-111">The following are some strategies for creating solutions listed in order from simplest to most complex:</span></span>  
  
-   [<span data-ttu-id="ddebb-112">No custom solutions</span><span class="sxs-lookup"><span data-stu-id="ddebb-112">No custom solutions</span></span>](organize-solutions.md#BKMK_NoCustomSolution)  
  
-   [<span data-ttu-id="ddebb-113">Single solution</span><span class="sxs-lookup"><span data-stu-id="ddebb-113">Single solution</span></span>](organize-solutions.md#BKMK_SingleSolution)  
  
-   [<span data-ttu-id="ddebb-114">Multiple solutions</span><span class="sxs-lookup"><span data-stu-id="ddebb-114">Multiple solutions</span></span>](organize-solutions.md#BKMK_MultipleSolutions)  
  
-   [<span data-ttu-id="ddebb-115">Multiple solutions with shared components</span><span class="sxs-lookup"><span data-stu-id="ddebb-115">Multiple solutions with shared components</span></span>](organize-solutions.md#BKMK_MultipleSolutionsSharedComponents)  
  
-   [<span data-ttu-id="ddebb-116">Solution libraries</span><span class="sxs-lookup"><span data-stu-id="ddebb-116">Solution libraries</span></span>](organize-solutions.md#BKMK_SolutionLibraries)  
  
<a name="BKMK_NoCustomSolution"></a>   
### <a name="no-custom-solutions"></a><span data-ttu-id="ddebb-117">No custom solutions</span><span class="sxs-lookup"><span data-stu-id="ddebb-117">No custom solutions</span></span>  
 <span data-ttu-id="ddebb-118">You don’t have to create solutions.</span><span class="sxs-lookup"><span data-stu-id="ddebb-118">You don’t have to create solutions.</span></span> <span data-ttu-id="ddebb-119">You can customize [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps directly by using the default solution.</span><span class="sxs-lookup"><span data-stu-id="ddebb-119">You can customize [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps directly by using the default solution.</span></span>  
  
 <span data-ttu-id="ddebb-120">You can still export your default solution as an unmanaged solution to transport it between organizations.</span><span class="sxs-lookup"><span data-stu-id="ddebb-120">You can still export your default solution as an unmanaged solution to transport it between organizations.</span></span>  
  
> [!TIP]
>  <span data-ttu-id="ddebb-121">If you change the customization prefix for the default publisher to a value that matches a publisher you may want to create in the future, any new customizations that you create will include this customization prefix in the name.</span><span class="sxs-lookup"><span data-stu-id="ddebb-121">If you change the customization prefix for the default publisher to a value that matches a publisher you may want to create in the future, any new customizations that you create will include this customization prefix in the name.</span></span> <span data-ttu-id="ddebb-122">This way, if you use solutions, you can add the customizations that you created in your default solution to an unmanaged solution so they can have consistent names.</span><span class="sxs-lookup"><span data-stu-id="ddebb-122">This way, if you use solutions, you can add the customizations that you created in your default solution to an unmanaged solution so they can have consistent names.</span></span>  
  
<a name="BKMK_SingleSolution"></a>   
### <a name="single-solution"></a><span data-ttu-id="ddebb-123">Single solution</span><span class="sxs-lookup"><span data-stu-id="ddebb-123">Single solution</span></span>  
 <span data-ttu-id="ddebb-124">By creating a solution, you establish a working set of customizations.</span><span class="sxs-lookup"><span data-stu-id="ddebb-124">By creating a solution, you establish a working set of customizations.</span></span> <span data-ttu-id="ddebb-125">This makes it easier to find items that you have customized.</span><span class="sxs-lookup"><span data-stu-id="ddebb-125">This makes it easier to find items that you have customized.</span></span>  
  
 <span data-ttu-id="ddebb-126">This approach is recommended when you only want to create a single managed solution.</span><span class="sxs-lookup"><span data-stu-id="ddebb-126">This approach is recommended when you only want to create a single managed solution.</span></span> <span data-ttu-id="ddebb-127">If you think you may have to split up the solution in the future, consider using multiple solutions.</span><span class="sxs-lookup"><span data-stu-id="ddebb-127">If you think you may have to split up the solution in the future, consider using multiple solutions.</span></span>  
  
<a name="BKMK_MultipleSolutions"></a>   
### <a name="multiple-solutions"></a><span data-ttu-id="ddebb-128">Multiple solutions</span><span class="sxs-lookup"><span data-stu-id="ddebb-128">Multiple solutions</span></span>  
 <span data-ttu-id="ddebb-129">If you have two unrelated solutions that don’t share components, the most direct approach is to create two unmanaged solutions.</span><span class="sxs-lookup"><span data-stu-id="ddebb-129">If you have two unrelated solutions that don’t share components, the most direct approach is to create two unmanaged solutions.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="ddebb-130">It is very common in solutions to modify the application ribbons or the Sitemap.</span><span class="sxs-lookup"><span data-stu-id="ddebb-130">It is very common in solutions to modify the application ribbons or the Sitemap.</span></span> <span data-ttu-id="ddebb-131">If both of your solutions modify these solution components, they are shared components.</span><span class="sxs-lookup"><span data-stu-id="ddebb-131">If both of your solutions modify these solution components, they are shared components.</span></span> <span data-ttu-id="ddebb-132">See the following section to see how to work with shared components.</span><span class="sxs-lookup"><span data-stu-id="ddebb-132">See the following section to see how to work with shared components.</span></span>  
  
<a name="BKMK_MultipleSolutionsSharedComponents"></a>   
### <a name="multiple-solutions-with-shared-components"></a><span data-ttu-id="ddebb-133">Multiple solutions with shared components</span><span class="sxs-lookup"><span data-stu-id="ddebb-133">Multiple solutions with shared components</span></span>  
 <span data-ttu-id="ddebb-134">You may have multiple solutions that share components.</span><span class="sxs-lookup"><span data-stu-id="ddebb-134">You may have multiple solutions that share components.</span></span> <span data-ttu-id="ddebb-135">You may have a certain set of common functionality within multiple solutions and that common functionality is compatible with any of the other functionality unique to each solution.</span><span class="sxs-lookup"><span data-stu-id="ddebb-135">You may have a certain set of common functionality within multiple solutions and that common functionality is compatible with any of the other functionality unique to each solution.</span></span> <span data-ttu-id="ddebb-136">For example, you may have a set of utility plug-ins that each solution uses yet each of the separate solutions do not share any other components.</span><span class="sxs-lookup"><span data-stu-id="ddebb-136">For example, you may have a set of utility plug-ins that each solution uses yet each of the separate solutions do not share any other components.</span></span>  
  
 <span data-ttu-id="ddebb-137">In this case, each solution can be developed in a single organization.</span><span class="sxs-lookup"><span data-stu-id="ddebb-137">In this case, each solution can be developed in a single organization.</span></span> <span data-ttu-id="ddebb-138">Some components can be included in more than one solution as long as any changes that were made to them are compatible with all other solutions that use them.</span><span class="sxs-lookup"><span data-stu-id="ddebb-138">Some components can be included in more than one solution as long as any changes that were made to them are compatible with all other solutions that use them.</span></span> <span data-ttu-id="ddebb-139">It is important that all the solutions share the same solution publisher.</span><span class="sxs-lookup"><span data-stu-id="ddebb-139">It is important that all the solutions share the same solution publisher.</span></span> <span data-ttu-id="ddebb-140">If the solution publisher is not identical, organizations will not be able to install more than one of your solutions.</span><span class="sxs-lookup"><span data-stu-id="ddebb-140">If the solution publisher is not identical, organizations will not be able to install more than one of your solutions.</span></span>  
  
<a name="BKMK_SolutionLibraries"></a>   
### <a name="solution-libraries"></a><span data-ttu-id="ddebb-141">Solution libraries</span><span class="sxs-lookup"><span data-stu-id="ddebb-141">Solution libraries</span></span>  
 <span data-ttu-id="ddebb-142">For an ISV with multiple solutions or a large enterprise deployment, many solution components will probably have to be shared.</span><span class="sxs-lookup"><span data-stu-id="ddebb-142">For an ISV with multiple solutions or a large enterprise deployment, many solution components will probably have to be shared.</span></span> <span data-ttu-id="ddebb-143">The best ways for solutions to share components is through solution libraries.</span><span class="sxs-lookup"><span data-stu-id="ddebb-143">The best ways for solutions to share components is through solution libraries.</span></span> <span data-ttu-id="ddebb-144">Create a solution library by creating an unmanaged solution in a separate organization and then packaging those components into a managed solution.</span><span class="sxs-lookup"><span data-stu-id="ddebb-144">Create a solution library by creating an unmanaged solution in a separate organization and then packaging those components into a managed solution.</span></span> <span data-ttu-id="ddebb-145">Install the managed solution into another organization and let developers reference these shared components.</span><span class="sxs-lookup"><span data-stu-id="ddebb-145">Install the managed solution into another organization and let developers reference these shared components.</span></span>  
  
 <span data-ttu-id="ddebb-146">The [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps Solutions Framework lets you build layers of solutions that depend on each other.</span><span class="sxs-lookup"><span data-stu-id="ddebb-146">The [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps Solutions Framework lets you build layers of solutions that depend on each other.</span></span> <span data-ttu-id="ddebb-147">Typically, you create a solution library representing a ”base” solution.</span><span class="sxs-lookup"><span data-stu-id="ddebb-147">Typically, you create a solution library representing a ”base” solution.</span></span> <span data-ttu-id="ddebb-148">Other solutions can be built on top of this base solution.</span><span class="sxs-lookup"><span data-stu-id="ddebb-148">Other solutions can be built on top of this base solution.</span></span> <span data-ttu-id="ddebb-149">This allows for cleaner separation of components.</span><span class="sxs-lookup"><span data-stu-id="ddebb-149">This allows for cleaner separation of components.</span></span> <span data-ttu-id="ddebb-150">Development teams that are working on solution libraries and those working on the dependent solutions can develop at different paces.</span><span class="sxs-lookup"><span data-stu-id="ddebb-150">Development teams that are working on solution libraries and those working on the dependent solutions can develop at different paces.</span></span> <span data-ttu-id="ddebb-151">The dependent solutions must be created after the solution libraries are installed.</span><span class="sxs-lookup"><span data-stu-id="ddebb-151">The dependent solutions must be created after the solution libraries are installed.</span></span>  
  
 <span data-ttu-id="ddebb-152">This requires that you create a prerequisite solution that customers must install before they can install a dependent solution.</span><span class="sxs-lookup"><span data-stu-id="ddebb-152">This requires that you create a prerequisite solution that customers must install before they can install a dependent solution.</span></span> <span data-ttu-id="ddebb-153">Developers working on the solution libraries can continue to work on them and update them as long as they don’t break any dependent solutions that require them.</span><span class="sxs-lookup"><span data-stu-id="ddebb-153">Developers working on the solution libraries can continue to work on them and update them as long as they don’t break any dependent solutions that require them.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="ddebb-154">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="ddebb-154">See also</span></span>  
 <span data-ttu-id="ddebb-155">[Organize your team to develop solutions](organize-team-develop-solutions.md) </span><span class="sxs-lookup"><span data-stu-id="ddebb-155">[Organize your team to develop solutions](organize-team-develop-solutions.md) </span></span>  
 [<span data-ttu-id="ddebb-156">Planning for Solution Development</span><span class="sxs-lookup"><span data-stu-id="ddebb-156">Planning for Solution Development</span></span>](plan-solution-development.md)
