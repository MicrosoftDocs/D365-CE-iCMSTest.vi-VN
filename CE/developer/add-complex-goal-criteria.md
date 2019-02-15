---
title: Add complex goal criteria (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: A rollup query (GoalRollupQuery) entity can be used to add complex rollup criteria for a goal
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
- adding complex goal criteria
- goal management entities, preventing double counting and other rollup query errors
- goal management entities, complex goal criteria
- rollup queries for adding complex goal criteria
- goal management entities, adding complex goal criteria
- goal management entities, rollup queries for adding complex goal criteria
- rollup queries for adding complex goal criteria, attributes and guidelines for setting; including propagation
ms.assetid: 2498859c-ca85-4893-ba08-b02ceb75278b
caps.latest.revision: 20
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ea64e9355aa3283399982d28d020b825030de172
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387525"
---
# <a name="add-complex-goal-criteria"></a><span data-ttu-id="b37a0-103">Add complex goal criteria</span><span class="sxs-lookup"><span data-stu-id="b37a0-103">Add complex goal criteria</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="b37a0-104">If you want to add complex rollup criteria for a goal, you can use a rollup query (`GoalRollupQuery`) entity.</span><span class="sxs-lookup"><span data-stu-id="b37a0-104">If you want to add complex rollup criteria for a goal, you can use a rollup query (`GoalRollupQuery`) entity.</span></span> <span data-ttu-id="b37a0-105">For example, you can specify revenue for a particular product line or revenue generated in a specific territory.</span><span class="sxs-lookup"><span data-stu-id="b37a0-105">For example, you can specify revenue for a particular product line or revenue generated in a specific territory.</span></span>  
  
 <span data-ttu-id="b37a0-106">A rollup query can be used by different goals.</span><span class="sxs-lookup"><span data-stu-id="b37a0-106">A rollup query can be used by different goals.</span></span> <span data-ttu-id="b37a0-107">However, a rollup query associated with a particular goal, applies only to that goal.</span><span class="sxs-lookup"><span data-stu-id="b37a0-107">However, a rollup query associated with a particular goal, applies only to that goal.</span></span> <span data-ttu-id="b37a0-108">A rollup query specified for a parent goal does not propagate to the child goal.</span><span class="sxs-lookup"><span data-stu-id="b37a0-108">A rollup query specified for a parent goal does not propagate to the child goal.</span></span> <span data-ttu-id="b37a0-109">A child goal can use the same query or a different query.</span><span class="sxs-lookup"><span data-stu-id="b37a0-109">A child goal can use the same query or a different query.</span></span> <span data-ttu-id="b37a0-110">A rollup query should use the same entity types that are specified in the rollup field records associated with the goal.</span><span class="sxs-lookup"><span data-stu-id="b37a0-110">A rollup query should use the same entity types that are specified in the rollup field records associated with the goal.</span></span> <span data-ttu-id="b37a0-111">If the goal tracks the sales order revenues, but the associated query uses the opportunity entity, an exception is thrown when you create or update the goal record.</span><span class="sxs-lookup"><span data-stu-id="b37a0-111">If the goal tracks the sales order revenues, but the associated query uses the opportunity entity, an exception is thrown when you create or update the goal record.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b37a0-112">The maximum number of records that can be returned in a goal rollup query is 5000.</span><span class="sxs-lookup"><span data-stu-id="b37a0-112">The maximum number of records that can be returned in a goal rollup query is 5000.</span></span>  
  
 <span data-ttu-id="b37a0-113">To specify query criteria, use the `GoalRollupQuery.FetchXml` attribute.</span><span class="sxs-lookup"><span data-stu-id="b37a0-113">To specify query criteria, use the `GoalRollupQuery.FetchXml` attribute.</span></span> <span data-ttu-id="b37a0-114">To specify the entity type for the query, use the `GoalRollupQuery.QueryEntityType` attribute.</span><span class="sxs-lookup"><span data-stu-id="b37a0-114">To specify the entity type for the query, use the `GoalRollupQuery.QueryEntityType` attribute.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b37a0-115">The entities that can be specified in the `GoalRollupQuery.QueryEntityType` attribute must have the following `EntityMetadata` attributes set to `true`: `IsValidForAdvancedFind`, `IsUserOwned`, `IsCustomizable` and `CanCreateAttributes`.</span><span class="sxs-lookup"><span data-stu-id="b37a0-115">The entities that can be specified in the `GoalRollupQuery.QueryEntityType` attribute must have the following `EntityMetadata` attributes set to `true`: `IsValidForAdvancedFind`, `IsUserOwned`, `IsCustomizable` and `CanCreateAttributes`.</span></span> <span data-ttu-id="b37a0-116">The following entities cannot be specified in this attribute: `SharePointDocumentLocation`, `SharePointSite` and `MailMergeTemplate`.</span><span class="sxs-lookup"><span data-stu-id="b37a0-116">The following entities cannot be specified in this attribute: `SharePointDocumentLocation`, `SharePointSite` and `MailMergeTemplate`.</span></span>  
  
 <span data-ttu-id="b37a0-117">Depending on the goal metric type, you can use the queries to filter actual, in-progress, and custom amount or count data.</span><span class="sxs-lookup"><span data-stu-id="b37a0-117">Depending on the goal metric type, you can use the queries to filter actual, in-progress, and custom amount or count data.</span></span> <span data-ttu-id="b37a0-118">The following table shows the goal metric types and the goal entity attributes that you can use to specify the queries for each type.</span><span class="sxs-lookup"><span data-stu-id="b37a0-118">The following table shows the goal metric types and the goal entity attributes that you can use to specify the queries for each type.</span></span>  
  
|<span data-ttu-id="b37a0-119">Goal metric type</span><span class="sxs-lookup"><span data-stu-id="b37a0-119">Goal metric type</span></span>|<span data-ttu-id="b37a0-120">Rollup query attributes</span><span class="sxs-lookup"><span data-stu-id="b37a0-120">Rollup query attributes</span></span>|  
|----------------------|-----------------------------|  
|<span data-ttu-id="b37a0-121">Amount (money)</span><span class="sxs-lookup"><span data-stu-id="b37a0-121">Amount (money)</span></span>|`Goal.RollUpQueryActualMoneyId`<br /><br /> `Goal.RollUpQueryCustomMoneyId`<br /><br /> `Goal.RollUpQueryInprogressMoneyId`|  
|<span data-ttu-id="b37a0-122">Amount (integer) or Count</span><span class="sxs-lookup"><span data-stu-id="b37a0-122">Amount (integer) or Count</span></span>|`Goal.RollupQueryActualIntegerId`<br /><br /> `Goal.RollUpQueryCustomIntegerId`<br /><br /> `Goal.RollUpQueryInprogressIntegerId`|  
|<span data-ttu-id="b37a0-123">Amount (decimal)</span><span class="sxs-lookup"><span data-stu-id="b37a0-123">Amount (decimal)</span></span>|`Goal.RollUpQueryActualDecimalId`<br /><br /> `Goal.RollUpQueryCustomDecimalId`<br /><br /> `Goal.RollUpQueryInprogressDecimalId`|  
  
 <span data-ttu-id="b37a0-124">The query for the goal's participating records for a given rollup attribute should include the following clauses:</span><span class="sxs-lookup"><span data-stu-id="b37a0-124">The query for the goal's participating records for a given rollup attribute should include the following clauses:</span></span>  
  
-   <span data-ttu-id="b37a0-125">A `Goal.ConsiderOnlyGoalOwnersRecords` value.</span><span class="sxs-lookup"><span data-stu-id="b37a0-125">A `Goal.ConsiderOnlyGoalOwnersRecords` value.</span></span>  
  
-   <span data-ttu-id="b37a0-126">A FetchXML expression specified in `GoalRollupQuery.FetchXml`.</span><span class="sxs-lookup"><span data-stu-id="b37a0-126">A FetchXML expression specified in `GoalRollupQuery.FetchXml`.</span></span>  
  
-   <span data-ttu-id="b37a0-127">Date range (`RollupField.DateAttribute`), state and status specified in the respective rollup field for the referenced goal metric.</span><span class="sxs-lookup"><span data-stu-id="b37a0-127">Date range (`RollupField.DateAttribute`), state and status specified in the respective rollup field for the referenced goal metric.</span></span>  
  
## <a name="preventing-double-counting-and-other-erroneous-results"></a><span data-ttu-id="b37a0-128">Preventing Double Counting and Other Erroneous Results</span><span class="sxs-lookup"><span data-stu-id="b37a0-128">Preventing Double Counting and Other Erroneous Results</span></span>  
 <span data-ttu-id="b37a0-129">Queries are very effective in filtering the results of a rollup.</span><span class="sxs-lookup"><span data-stu-id="b37a0-129">Queries are very effective in filtering the results of a rollup.</span></span> <span data-ttu-id="b37a0-130">However, if not used carefully, they can introduce the “double counting” or other erroneous results.</span><span class="sxs-lookup"><span data-stu-id="b37a0-130">However, if not used carefully, they can introduce the “double counting” or other erroneous results.</span></span> <span data-ttu-id="b37a0-131">The following examples demonstrate how queries may contribute in unwanted results:</span><span class="sxs-lookup"><span data-stu-id="b37a0-131">The following examples demonstrate how queries may contribute in unwanted results:</span></span>  
  
- <span data-ttu-id="b37a0-132">You are tracking the sales orders for a particular salesperson.</span><span class="sxs-lookup"><span data-stu-id="b37a0-132">You are tracking the sales orders for a particular salesperson.</span></span> <span data-ttu-id="b37a0-133">However, the rollup did not return any sales orders.</span><span class="sxs-lookup"><span data-stu-id="b37a0-133">However, the rollup did not return any sales orders.</span></span> <span data-ttu-id="b37a0-134">This can happen if the query that you used filtered out the territories where the salesperson has customers.</span><span class="sxs-lookup"><span data-stu-id="b37a0-134">This can happen if the query that you used filtered out the territories where the salesperson has customers.</span></span>  
  
- <span data-ttu-id="b37a0-135">You set two goals for a salesperson.</span><span class="sxs-lookup"><span data-stu-id="b37a0-135">You set two goals for a salesperson.</span></span> <span data-ttu-id="b37a0-136">One goal tracks the opportunities for a particular product and another goal tracks the opportunities in a particular territory.</span><span class="sxs-lookup"><span data-stu-id="b37a0-136">One goal tracks the opportunities for a particular product and another goal tracks the opportunities in a particular territory.</span></span> <span data-ttu-id="b37a0-137">If the opportunity includes selling the specified product in the specified territory, the revenue from this opportunity is included in both goals.</span><span class="sxs-lookup"><span data-stu-id="b37a0-137">If the opportunity includes selling the specified product in the specified territory, the revenue from this opportunity is included in both goals.</span></span> <span data-ttu-id="b37a0-138">If the goals have the same parent goal, their totals are added to the parent goal, resulting in double counting.</span><span class="sxs-lookup"><span data-stu-id="b37a0-138">If the goals have the same parent goal, their totals are added to the parent goal, resulting in double counting.</span></span>  
  
  <span data-ttu-id="b37a0-139">You can prevent double counting and other incorrect results by following these guidelines:</span><span class="sxs-lookup"><span data-stu-id="b37a0-139">You can prevent double counting and other incorrect results by following these guidelines:</span></span>  
  
- <span data-ttu-id="b37a0-140">Set the `Goal.ConsiderOnlyGoalOwnersRecords` attribute to `true` to use only the records owned by the goal owner.</span><span class="sxs-lookup"><span data-stu-id="b37a0-140">Set the `Goal.ConsiderOnlyGoalOwnersRecords` attribute to `true` to use only the records owned by the goal owner.</span></span>  
  
- <span data-ttu-id="b37a0-141">Do not assign multiple goals to a sales person for the same time period.</span><span class="sxs-lookup"><span data-stu-id="b37a0-141">Do not assign multiple goals to a sales person for the same time period.</span></span>  
  
- <span data-ttu-id="b37a0-142">Do not use a query if you are not sure it will provide the results that you expect.</span><span class="sxs-lookup"><span data-stu-id="b37a0-142">Do not use a query if you are not sure it will provide the results that you expect.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="b37a0-143">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="b37a0-143">See also</span></span>  
 <span data-ttu-id="b37a0-144">[Goal Management Entities](goal-management-entities.md) </span><span class="sxs-lookup"><span data-stu-id="b37a0-144">[Goal Management Entities](goal-management-entities.md) </span></span>  
 <span data-ttu-id="b37a0-145">[Sample: Use Rollup Queries to Track Goals](sample-use-rollup-queries-track-goals.md) </span><span class="sxs-lookup"><span data-stu-id="b37a0-145">[Sample: Use Rollup Queries to Track Goals](sample-use-rollup-queries-track-goals.md) </span></span>  
 [<span data-ttu-id="b37a0-146">Roll Up Goal Totals</span><span class="sxs-lookup"><span data-stu-id="b37a0-146">Roll Up Goal Totals</span></span>](roll-up-goal-totals.md)
