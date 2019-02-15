---
title: 'Sample: Rollup goal data for a custom period against the target revenue (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: This sample shows how to roll up goal data for a custom period against the target revenue
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
- goal management entities samples, rolling up goal data in a custom period against revenue targets
- sample for rolling up goal data in a custom period against revenue targets
ms.assetid: 87b5756c-b24c-4140-a3c3-3660d1cb3e01
caps.latest.revision: 22
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: b1b6e5b3c4533f70158fffbe2a6fdacfe6b1c045
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386475"
---
# <a name="sample-rollup-goal-data-for-a-custom-period-against-the-target-revenue"></a><span data-ttu-id="5e0d0-103">Sample: Rollup goal data for a custom period against the target revenue</span><span class="sxs-lookup"><span data-stu-id="5e0d0-103">Sample: Rollup goal data for a custom period against the target revenue</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="5e0d0-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="5e0d0-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="5e0d0-105">[Download the Goals samples](https://code.msdn.microsoft.com/Goals-Samples-539b2a34).</span><span class="sxs-lookup"><span data-stu-id="5e0d0-105">[Download the Goals samples](https://code.msdn.microsoft.com/Goals-Samples-539b2a34).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5e0d0-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="5e0d0-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
   
## <a name="requirements"></a><span data-ttu-id="5e0d0-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="5e0d0-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="5e0d0-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="5e0d0-108">Demonstrates</span></span>  
 <span data-ttu-id="5e0d0-109">This sample shows how to roll up goal data for a custom period against the target revenue.</span><span class="sxs-lookup"><span data-stu-id="5e0d0-109">This sample shows how to roll up goal data for a custom period against the target revenue.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5e0d0-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="5e0d0-110">Example</span></span>  
 [!code-csharp[Goals#RollupAllGoalsForCustomPeriodAgainstTargetRevenue](../snippets/csharp/CRMV8/goals/cs/rollupallgoalsforcustomperiodagainsttargetrevenue.cs#rollupallgoalsforcustomperiodagainsttargetrevenue)]  
  
### <a name="see-also"></a><span data-ttu-id="5e0d0-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="5e0d0-111">See also</span></span>  
 <span data-ttu-id="5e0d0-112">[Goal Management Entities](goal-management-entities.md) </span><span class="sxs-lookup"><span data-stu-id="5e0d0-112">[Goal Management Entities](goal-management-entities.md) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.RecalculateRequest>   
 [<span data-ttu-id="5e0d0-113">Sample: Rollup goal data for a fiscal period against the stretch target count</span><span class="sxs-lookup"><span data-stu-id="5e0d0-113">Sample: Rollup goal data for a fiscal period against the stretch target count</span></span>](sample-rollup-goal-data-fiscal-period-stretch-target-count.md)
