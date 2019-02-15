---
title: Roll up goal totals (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: RecalculateRequest message can be used to roll up data in a goal hierarchy. It recalculates the goal rollup field values, such as Goal.ActualMoney or Goal.ActualInteger, for all goals in the hierarchy
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
- goal management entities, rolling up goal totals
- overriding values for rollup goal totals
- goal management entities, recalculating goal rollup values
- goal management entities, expiration time for goal rollup fields
- goal management entities, rolling up data in goal hierarchies
- rolling up goal totals
- expiration time for goal rollup fields
- goal management entities, overriding values for rollup goal totals
- rolling up data in goal hierarchies
- recalculating goal rollup values
ms.assetid: e7e706f7-0f65-480a-87bc-e11857ad084f
caps.latest.revision: 25
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 38d3d5b0dda66cfac4ee014d83551c5e233d1ac5
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387690"
---
# <a name="roll-up-goal-totals"></a><span data-ttu-id="21e1b-104">Roll up goal totals</span><span class="sxs-lookup"><span data-stu-id="21e1b-104">Roll up goal totals</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="21e1b-105">To roll up data in the goal hierarchy, use the <xref:Microsoft.Crm.Sdk.Messages.RecalculateRequest> message.</span><span class="sxs-lookup"><span data-stu-id="21e1b-105">To roll up data in the goal hierarchy, use the <xref:Microsoft.Crm.Sdk.Messages.RecalculateRequest> message.</span></span> <span data-ttu-id="21e1b-106">It recalculates the goal rollup field values, such as `Goal.ActualMoney` or `Goal.ActualInteger`, for all goals in the hierarchy.</span><span class="sxs-lookup"><span data-stu-id="21e1b-106">It recalculates the goal rollup field values, such as `Goal.ActualMoney` or `Goal.ActualInteger`, for all goals in the hierarchy.</span></span> <span data-ttu-id="21e1b-107">A rollup for each goal is performed in the context of the goal manager.</span><span class="sxs-lookup"><span data-stu-id="21e1b-107">A rollup for each goal is performed in the context of the goal manager.</span></span> <span data-ttu-id="21e1b-108">This means that only the records that a manager of a goal has Read access to participate in the rollup.</span><span class="sxs-lookup"><span data-stu-id="21e1b-108">This means that only the records that a manager of a goal has Read access to participate in the rollup.</span></span> <span data-ttu-id="21e1b-109">The system automatically switches the manager’s context for each goal during rollup, as every goal may have a different goal manager.</span><span class="sxs-lookup"><span data-stu-id="21e1b-109">The system automatically switches the manager’s context for each goal during rollup, as every goal may have a different goal manager.</span></span>  
  
 <span data-ttu-id="21e1b-110">The totals are rolled up from the child goals to the parent goals, from the bottom of the hierarchy to the top.</span><span class="sxs-lookup"><span data-stu-id="21e1b-110">The totals are rolled up from the child goals to the parent goals, from the bottom of the hierarchy to the top.</span></span> <span data-ttu-id="21e1b-111">The ending total for the root goal at the top of the hierarchy is an aggregate sum of all totals in the hierarchy.</span><span class="sxs-lookup"><span data-stu-id="21e1b-111">The ending total for the root goal at the top of the hierarchy is an aggregate sum of all totals in the hierarchy.</span></span> <span data-ttu-id="21e1b-112">For example, if revenue metric is used, the total is an aggregate sum of the money amounts.</span><span class="sxs-lookup"><span data-stu-id="21e1b-112">For example, if revenue metric is used, the total is an aggregate sum of the money amounts.</span></span> <span data-ttu-id="21e1b-113">If a count metric is used, the total is an aggregate count of the actual records in the system, such as telephone calls.</span><span class="sxs-lookup"><span data-stu-id="21e1b-113">If a count metric is used, the total is an aggregate count of the actual records in the system, such as telephone calls.</span></span> <span data-ttu-id="21e1b-114">Regardless of which particular goal is a target of the recalculate operation, all totals in a given hierarchy are updated.</span><span class="sxs-lookup"><span data-stu-id="21e1b-114">Regardless of which particular goal is a target of the recalculate operation, all totals in a given hierarchy are updated.</span></span>  
  
 <span data-ttu-id="21e1b-115">If you set `Goal.RollupOnlyFromChildGoals` to `true`, only child goal records are used in the rollup.</span><span class="sxs-lookup"><span data-stu-id="21e1b-115">If you set `Goal.RollupOnlyFromChildGoals` to `true`, only child goal records are used in the rollup.</span></span> <span data-ttu-id="21e1b-116">If you set it to `false`, the rollup includes the child records and other goal’s participating records.</span><span class="sxs-lookup"><span data-stu-id="21e1b-116">If you set it to `false`, the rollup includes the child records and other goal’s participating records.</span></span> <span data-ttu-id="21e1b-117">A participating record must satisfy the following conditions:</span><span class="sxs-lookup"><span data-stu-id="21e1b-117">A participating record must satisfy the following conditions:</span></span>  
  
-   <span data-ttu-id="21e1b-118">The source date of the record must be between the start date and the end date of the goal time period, or fall on the start date or the end date of the goal period.</span><span class="sxs-lookup"><span data-stu-id="21e1b-118">The source date of the record must be between the start date and the end date of the goal time period, or fall on the start date or the end date of the goal period.</span></span>  
  
-   <span data-ttu-id="21e1b-119">The state and status of the record must match the values defined in the goal metric.</span><span class="sxs-lookup"><span data-stu-id="21e1b-119">The state and status of the record must match the values defined in the goal metric.</span></span>  
  
-   <span data-ttu-id="21e1b-120">If a rollup query is specified for the goal, all query conditions must be met.</span><span class="sxs-lookup"><span data-stu-id="21e1b-120">If a rollup query is specified for the goal, all query conditions must be met.</span></span>  
  
-   <span data-ttu-id="21e1b-121">The goal manager must have Read access to the record.</span><span class="sxs-lookup"><span data-stu-id="21e1b-121">The goal manager must have Read access to the record.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="21e1b-122">The goal rollup fields that do not participate in the rollup are not updated, their values are **null**.</span><span class="sxs-lookup"><span data-stu-id="21e1b-122">The goal rollup fields that do not participate in the rollup are not updated, their values are **null**.</span></span>  
  
 <span data-ttu-id="21e1b-123">To specify the rollup expiration time, use the `Organization.GoalRollupExpiryTime` attribute.</span><span class="sxs-lookup"><span data-stu-id="21e1b-123">To specify the rollup expiration time, use the `Organization.GoalRollupExpiryTime` attribute.</span></span> <span data-ttu-id="21e1b-124">For example, if the rollup expiration time is set to six months, the goals older than six months will not be rolled up automatically.</span><span class="sxs-lookup"><span data-stu-id="21e1b-124">For example, if the rollup expiration time is set to six months, the goals older than six months will not be rolled up automatically.</span></span> <span data-ttu-id="21e1b-125">To specify the frequency of goal rollup, use the `Organization.GoalRollupFrequency` attribute.</span><span class="sxs-lookup"><span data-stu-id="21e1b-125">To specify the frequency of goal rollup, use the `Organization.GoalRollupFrequency` attribute.</span></span> <span data-ttu-id="21e1b-126">The frequency can be set on an hourly basis.</span><span class="sxs-lookup"><span data-stu-id="21e1b-126">The frequency can be set on an hourly basis.</span></span> <span data-ttu-id="21e1b-127">By default, the goal actual values are recalculated every 24 hours.</span><span class="sxs-lookup"><span data-stu-id="21e1b-127">By default, the goal actual values are recalculated every 24 hours.</span></span>  
  
 <span data-ttu-id="21e1b-128">**Override Calculated Values**</span><span class="sxs-lookup"><span data-stu-id="21e1b-128">**Override Calculated Values**</span></span>  
  
 <span data-ttu-id="21e1b-129">To override the system calculated actual, in-progress, or custom goal rollup field values, use the <xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest> message to update the goal record.</span><span class="sxs-lookup"><span data-stu-id="21e1b-129">To override the system calculated actual, in-progress, or custom goal rollup field values, use the <xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest> message to update the goal record.</span></span> <span data-ttu-id="21e1b-130">You must set the `Goal.IsOverride` attribute to `true` to notify the system that the rollup field values can be updated.</span><span class="sxs-lookup"><span data-stu-id="21e1b-130">You must set the `Goal.IsOverride` attribute to `true` to notify the system that the rollup field values can be updated.</span></span> <span data-ttu-id="21e1b-131">To signal the system that the goal’s rollup field values were overridden and must not be updated during next recalculate operation, set the `Goal.IsOverridden` attribute to `true`.</span><span class="sxs-lookup"><span data-stu-id="21e1b-131">To signal the system that the goal’s rollup field values were overridden and must not be updated during next recalculate operation, set the `Goal.IsOverridden` attribute to `true`.</span></span> <span data-ttu-id="21e1b-132">If `Goal.IsOverride` is `false`, an exception is thrown during the update operation.</span><span class="sxs-lookup"><span data-stu-id="21e1b-132">If `Goal.IsOverride` is `false`, an exception is thrown during the update operation.</span></span> <span data-ttu-id="21e1b-133">If `Goal.IsOverridden` is `false`, the goal rollup field values will be overwritten during next recalculate operation with system calculated values.</span><span class="sxs-lookup"><span data-stu-id="21e1b-133">If `Goal.IsOverridden` is `false`, the goal rollup field values will be overwritten during next recalculate operation with system calculated values.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="21e1b-134">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="21e1b-134">See also</span></span>  
 <span data-ttu-id="21e1b-135">[Goal Management Entities](goal-management-entities.md) </span><span class="sxs-lookup"><span data-stu-id="21e1b-135">[Goal Management Entities](goal-management-entities.md) </span></span>  
 <span data-ttu-id="21e1b-136">[Sample: Roll Up Goal Data for a Custom Period Against the Target Revenue](sample-rollup-goal-data-custom-period-target-revenue.md) </span><span class="sxs-lookup"><span data-stu-id="21e1b-136">[Sample: Roll Up Goal Data for a Custom Period Against the Target Revenue](sample-rollup-goal-data-custom-period-target-revenue.md) </span></span>  
 <span data-ttu-id="21e1b-137">[Sample: Roll Up Goal Data for a Fiscal Period Against the Stretch Target Count](sample-rollup-goal-data-fiscal-period-stretch-target-count.md) </span><span class="sxs-lookup"><span data-stu-id="21e1b-137">[Sample: Roll Up Goal Data for a Fiscal Period Against the Stretch Target Count](sample-rollup-goal-data-fiscal-period-stretch-target-count.md) </span></span>  
 [<span data-ttu-id="21e1b-138">Goal Entity</span><span class="sxs-lookup"><span data-stu-id="21e1b-138">Goal Entity</span></span>](entities/goal.md)
