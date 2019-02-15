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
# <a name="sample-rollup-goal-data-for-a-custom-period-against-the-target-revenue"></a>Sample: Rollup goal data for a custom period against the target revenue

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. [Download the Goals samples](https://code.msdn.microsoft.com/Goals-Samples-539b2a34).

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
   
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to roll up goal data for a custom period against the target revenue.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[Goals#RollupAllGoalsForCustomPeriodAgainstTargetRevenue](../snippets/csharp/CRMV8/goals/cs/rollupallgoalsforcustomperiodagainsttargetrevenue.cs#rollupallgoalsforcustomperiodagainsttargetrevenue)]  
  
### <a name="see-also"></a>Xem thêm  
 [Goal Management Entities](goal-management-entities.md)   
 <xref:Microsoft.Crm.Sdk.Messages.RecalculateRequest>   
 [Sample: Rollup goal data for a fiscal period against the stretch target count](sample-rollup-goal-data-fiscal-period-stretch-target-count.md)
