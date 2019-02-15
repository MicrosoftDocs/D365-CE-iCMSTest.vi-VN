---
title: 'Sample: Override goal total count and close the goal (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: This sample demonstrates how to override the goal total count and close the goal
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
- Sample for overriding total counts and closing goals
- goal management entities samples, overriding total counts and closing goals
ms.assetid: c454269e-9e58-47f4-abbc-7bbe9e8d636c
caps.latest.revision: 17
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: cc0f9044f901831d30e1fd48cf3d25682dc9ff67
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386580"
---
# <a name="sample-override-goal-total-count-and-close-the-goal"></a>Sample: Override goal total count and close the goal

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. [Download the Goals samples](https://code.msdn.microsoft.com/Goals-Samples-539b2a34). 

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
   
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to override the goal total count and close the goal.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[Goals#OverrideGoalTotalCount](../snippets/csharp/CRMV8/goals/cs/overridegoaltotalcount.cs#overridegoaltotalcount)]  
  
### <a name="see-also"></a>Xem thêm  
 [Goal Management Entities](goal-management-entities.md)   
 <xref:Microsoft.Crm.Sdk.Messages.RecalculateRequest>
