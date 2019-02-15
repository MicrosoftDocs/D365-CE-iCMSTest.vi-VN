---
title: Organize your team to develop solutions (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: This document lists down some strategies to use when multiple developers are working on the same solution
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
- deploying solutions from development through testing and production, organizing your team to develop solutions
- strategies for team development, organizing your team to develop solutions
- organizing your team to develop solutions, deploying solutions from development through testing and production
- organizing your team to develop solutions, strategies for team development
- solutions deployment, organizing your team to develop solutions
ms.assetid: 9baa169b-17f7-4dfd-8305-8e2f53bc5acc
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: c819eb0fccebc72912177195a4375486164e8b88
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388585"
---
# <a name="organize-your-team-to-develop-solutions"></a><span data-ttu-id="e763a-103">Organize your team to develop solutions</span><span class="sxs-lookup"><span data-stu-id="e763a-103">Organize your team to develop solutions</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="e763a-104">When multiple developers have to work on the same solution, you may want to create an environment where each developer can create customizations that will not interfere with the work of other developers.</span><span class="sxs-lookup"><span data-stu-id="e763a-104">When multiple developers have to work on the same solution, you may want to create an environment where each developer can create customizations that will not interfere with the work of other developers.</span></span> <span data-ttu-id="e763a-105">You may also need to move your solution from development environments to test environments and user acceptance testing (UAT) environments.</span><span class="sxs-lookup"><span data-stu-id="e763a-105">You may also need to move your solution from development environments to test environments and user acceptance testing (UAT) environments.</span></span>  
  
<a name="BKMK_StrategiesForTeamDev"></a>   
## <a name="strategies-for-team-development"></a><span data-ttu-id="e763a-106">Strategies for team development</span><span class="sxs-lookup"><span data-stu-id="e763a-106">Strategies for team development</span></span>  
 <span data-ttu-id="e763a-107">Some strategies to manage team development of solutions are as follows:</span><span class="sxs-lookup"><span data-stu-id="e763a-107">Some strategies to manage team development of solutions are as follows:</span></span>  
  
-   [<span data-ttu-id="e763a-108">Single Organization: One Master Solution</span><span class="sxs-lookup"><span data-stu-id="e763a-108">Single Organization: One Master Solution</span></span>](organize-team-develop-solutions.md#BKMK_SingleOrgMasterSolution)  
  
-   [<span data-ttu-id="e763a-109">Single Organization: Multiple Developer Solutions + Master Solution</span><span class="sxs-lookup"><span data-stu-id="e763a-109">Single Organization: Multiple Developer Solutions + Master Solution</span></span>](organize-team-develop-solutions.md#BKMK_SingleOrgMultipleDeveloper)  
  
-   [<span data-ttu-id="e763a-110">One Organization per Developer</span><span class="sxs-lookup"><span data-stu-id="e763a-110">One Organization per Developer</span></span>](organize-team-develop-solutions.md#BKMK_OneOrgPerDev)  
  
<a name="BKMK_SingleOrgMasterSolution"></a>   
### <a name="single-organization-one-master-solution"></a><span data-ttu-id="e763a-111">Single organization: One master solution</span><span class="sxs-lookup"><span data-stu-id="e763a-111">Single organization: One master solution</span></span>  
 <span data-ttu-id="e763a-112">Multiple developers can work on a single organization; however, they have to be careful to work on separate components.</span><span class="sxs-lookup"><span data-stu-id="e763a-112">Multiple developers can work on a single organization; however, they have to be careful to work on separate components.</span></span> <span data-ttu-id="e763a-113">This is easier when any prerequisite managed solutions (shared libraries) are installed first.</span><span class="sxs-lookup"><span data-stu-id="e763a-113">This is easier when any prerequisite managed solutions (shared libraries) are installed first.</span></span>  
  
<a name="BKMK_SingleOrgMultipleDeveloper"></a>   
### <a name="single-organization-multiple-developer-solutions--master-solution"></a><span data-ttu-id="e763a-114">Single organization: Multiple developer solutions + master solution</span><span class="sxs-lookup"><span data-stu-id="e763a-114">Single organization: Multiple developer solutions + master solution</span></span>  
 <span data-ttu-id="e763a-115">In a single organization, you can create separate unmanaged solutions for each developer.</span><span class="sxs-lookup"><span data-stu-id="e763a-115">In a single organization, you can create separate unmanaged solutions for each developer.</span></span> <span data-ttu-id="e763a-116">Each solution contains a sub set of a master solution.</span><span class="sxs-lookup"><span data-stu-id="e763a-116">Each solution contains a sub set of a master solution.</span></span> <span data-ttu-id="e763a-117">Each solution component exists in only one unmanaged solution.</span><span class="sxs-lookup"><span data-stu-id="e763a-117">Each solution component exists in only one unmanaged solution.</span></span> <span data-ttu-id="e763a-118">Developers do not add existing solution components to the unmanaged solutions assigned to them.</span><span class="sxs-lookup"><span data-stu-id="e763a-118">Developers do not add existing solution components to the unmanaged solutions assigned to them.</span></span> <span data-ttu-id="e763a-119">This provides a clear separation of components that are being modified.</span><span class="sxs-lookup"><span data-stu-id="e763a-119">This provides a clear separation of components that are being modified.</span></span> <span data-ttu-id="e763a-120">You do not have to merge changes because each developer’s solution contains a reference to components that are contained in the master solution.</span><span class="sxs-lookup"><span data-stu-id="e763a-120">You do not have to merge changes because each developer’s solution contains a reference to components that are contained in the master solution.</span></span>  
  
<a name="BKMK_OneOrgPerDev"></a>   
### <a name="one-organization-per-developer"></a><span data-ttu-id="e763a-121">One organization per developer</span><span class="sxs-lookup"><span data-stu-id="e763a-121">One organization per developer</span></span>  
 <span data-ttu-id="e763a-122">Each developer can work on their own organization.</span><span class="sxs-lookup"><span data-stu-id="e763a-122">Each developer can work on their own organization.</span></span> <span data-ttu-id="e763a-123">To check their changes into [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps, they must export their solution as an unmanaged solution.</span><span class="sxs-lookup"><span data-stu-id="e763a-123">To check their changes into [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps, they must export their solution as an unmanaged solution.</span></span> <span data-ttu-id="e763a-124">The solution from each developer’s organization is then imported into a master solution.</span><span class="sxs-lookup"><span data-stu-id="e763a-124">The solution from each developer’s organization is then imported into a master solution.</span></span> <span data-ttu-id="e763a-125">Use the master solution to export the managed solution.</span><span class="sxs-lookup"><span data-stu-id="e763a-125">Use the master solution to export the managed solution.</span></span>  
  
<a name="BKMK_DeployingSolutionsFromDevThroughToProduction"></a>   
## <a name="deploy-solutions-from-development-through-test-and-production-environments"></a><span data-ttu-id="e763a-126">Deploy solutions from development through test and production environments</span><span class="sxs-lookup"><span data-stu-id="e763a-126">Deploy solutions from development through test and production environments</span></span>  
 <span data-ttu-id="e763a-127">In development organizations, solutions are deployed into various test and staging environments for analysis before they are deployed into a production environment.</span><span class="sxs-lookup"><span data-stu-id="e763a-127">In development organizations, solutions are deployed into various test and staging environments for analysis before they are deployed into a production environment.</span></span> <span data-ttu-id="e763a-128">The white paper [Deploying Microsoft Dynamics CRM 2011 and CRM Online Solutions from Development through Test and Production Environments](http://go.microsoft.com/fwlink/p/?LinkId=232288) explores how to deploy real-world Dynamics 365 for Customer Engagement apps solutions across test and production environments in reliable and repeatable ways by using automation.</span><span class="sxs-lookup"><span data-stu-id="e763a-128">The white paper [Deploying Microsoft Dynamics CRM 2011 and CRM Online Solutions from Development through Test and Production Environments](http://go.microsoft.com/fwlink/p/?LinkId=232288) explores how to deploy real-world Dynamics 365 for Customer Engagement apps solutions across test and production environments in reliable and repeatable ways by using automation.</span></span> <span data-ttu-id="e763a-129">The paper also highlights specific constraints that exist when you deploy and test solutions in [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="e763a-129">The paper also highlights specific constraints that exist when you deploy and test solutions in [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)] apps.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="e763a-130">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="e763a-130">See also</span></span>  
 <span data-ttu-id="e763a-131">[Planning for Solution Development](plan-solution-development.md) </span><span class="sxs-lookup"><span data-stu-id="e763a-131">[Planning for Solution Development](plan-solution-development.md) </span></span>  
 <span data-ttu-id="e763a-132">[Modularize your Solutions](organize-solutions.md) </span><span class="sxs-lookup"><span data-stu-id="e763a-132">[Modularize your Solutions](organize-solutions.md) </span></span>  
 [<span data-ttu-id="e763a-133">White Paper: Deploying Dynamics 365 for Customer Engagement apps Solutions from Development through Test and Production Environments</span><span class="sxs-lookup"><span data-stu-id="e763a-133">White Paper: Deploying Dynamics 365 for Customer Engagement apps Solutions from Development through Test and Production Environments</span></span>](http://www.microsoft.com/download/en/details.aspx?displaylang=en&id=27824)
