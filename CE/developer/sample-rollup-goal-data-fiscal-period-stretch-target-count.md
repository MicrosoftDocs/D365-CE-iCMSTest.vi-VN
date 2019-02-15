---
title: 'Sample: Rollup goal data for a fiscal period against the stretch target count (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: This sample shows how to roll up goal data for a fiscal period against stretch target count representing a number of completed telephone calls
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- goal management entities samples, rolling up goal data in a fiscal period against stretch targets
- sample for rolling up goal data in a fiscal period against stretch targets
ms.assetid: 2f1e1939-7dd3-4a12-92b2-13fb166c0dea
caps.latest.revision: 20
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: c066ce33d1832e50901d6baa146e2c0f31b3bf0c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388746"
---
# <a name="sample-rollup-goal-data-for-a-fiscal-period-against-the-stretch-target-count"></a><span data-ttu-id="9153c-103">Sample: Rollup goal data for a fiscal period against the stretch target count</span><span class="sxs-lookup"><span data-stu-id="9153c-103">Sample: Rollup goal data for a fiscal period against the stretch target count</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="9153c-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="9153c-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="9153c-105">[Download the Goals samples](https://code.msdn.microsoft.com/Goals-Samples-539b2a34).</span><span class="sxs-lookup"><span data-stu-id="9153c-105">[Download the Goals samples](https://code.msdn.microsoft.com/Goals-Samples-539b2a34).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="9153c-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="9153c-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
   
## <a name="requirements"></a><span data-ttu-id="9153c-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="9153c-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="9153c-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="9153c-108">Demonstrates</span></span>  
 <span data-ttu-id="9153c-109">This sample shows how to roll up goal data for a fiscal period against stretch target count representing a number of completed telephone calls.</span><span class="sxs-lookup"><span data-stu-id="9153c-109">This sample shows how to roll up goal data for a fiscal period against stretch target count representing a number of completed telephone calls.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9153c-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="9153c-110">Example</span></span>  
 [!code-csharp[Goals#RollupAllGoalsForFiscalPeriodAndStretchedTargetRevenue](../snippets/csharp/CRMV8/goals/cs/rollupallgoalsforfiscalperiodandstretchedtargetrevenue.cs#rollupallgoalsforfiscalperiodandstretchedtargetrevenue)]  
  
### <a name="see-also"></a><span data-ttu-id="9153c-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="9153c-111">See also</span></span>  
 <span data-ttu-id="9153c-112">[Goal Management Entities](goal-management-entities.md) </span><span class="sxs-lookup"><span data-stu-id="9153c-112">[Goal Management Entities](goal-management-entities.md) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.RecalculateRequest>   
 [<span data-ttu-id="9153c-113">Sample: Use Rollup Queries to Track Goals</span><span class="sxs-lookup"><span data-stu-id="9153c-113">Sample: Use Rollup Queries to Track Goals</span></span>](sample-use-rollup-queries-track-goals.md)
