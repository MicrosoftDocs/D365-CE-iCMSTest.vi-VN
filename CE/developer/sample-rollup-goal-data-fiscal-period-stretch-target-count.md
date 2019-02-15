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
# <a name="sample-rollup-goal-data-for-a-fiscal-period-against-the-stretch-target-count"></a>Sample: Rollup goal data for a fiscal period against the stretch target count

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. [Download the Goals samples](https://code.msdn.microsoft.com/Goals-Samples-539b2a34). 

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
   
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to roll up goal data for a fiscal period against stretch target count representing a number of completed telephone calls.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[Goals#RollupAllGoalsForFiscalPeriodAndStretchedTargetRevenue](../snippets/csharp/CRMV8/goals/cs/rollupallgoalsforfiscalperiodandstretchedtargetrevenue.cs#rollupallgoalsforfiscalperiodandstretchedtargetrevenue)]  
  
### <a name="see-also"></a>Xem thêm  
 [Goal Management Entities](goal-management-entities.md)   
 <xref:Microsoft.Crm.Sdk.Messages.RecalculateRequest>   
 [Sample: Use Rollup Queries to Track Goals](sample-use-rollup-queries-track-goals.md)
