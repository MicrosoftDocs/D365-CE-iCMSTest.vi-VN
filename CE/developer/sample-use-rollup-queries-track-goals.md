---
title: 'Sample: Use rollup queries to track goals (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: This sample demonstrates how to use rollup queries to track goals
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
- sample for using rollup queries to track goals
- goal management entities samples, using rollup queries to track goals
ms.assetid: 80f9b7d7-87d6-497e-9bdb-a02cf291743d
caps.latest.revision: 19
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: c8cdf4c95dd118b1be31f318b09645a1399e4f13
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387016"
---
# <a name="sample-use-rollup-queries-to-track-goals"></a>Sample: Use rollup queries to track goals

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. [Download the Goals samples](https://code.msdn.microsoft.com/Goals-Samples-539b2a34).

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
   
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to use rollup queries to track goals.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[Goals#UsingQueriesToTrackGoals](../snippets/csharp/CRMV8/goals/cs/usingqueriestotrackgoals.cs#usingqueriestotrackgoals)]  
  
### <a name="see-also"></a>Xem thêm  
 [Goal Management Entities](goal-management-entities.md)   
 <xref:Microsoft.Crm.Sdk.Messages.RecalculateRequest>   
 [Sample: Override Goal Total Count and Close the Goal](sample-override-goal-total-count-close-goal.md)
