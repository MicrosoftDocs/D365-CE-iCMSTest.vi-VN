---
title: 'Sample: Distribute a quick campaign (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The sample code demonstrates how to create and distribute a quick campaign.
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
- distributing a quick campaign, marketing entities sample
- sample for distributing a quick campaign
ms.assetid: adc93a60-1736-4ea0-a90b-4ca6c8fcfa35
caps.latest.revision: 23
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: fdcd2fc0f22ae8088b6a4884574f7ad9f7c33d76
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385798"
---
# <a name="sample-distribute-a-quick-campaign"></a>Sample: Distribute a quick campaign

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. Download the complete sample from [Sample: Work with Marketing entities](https://code.msdn.microsoft.com/Marketing-Samples-c5429380).  

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to create and distribute a quick campaign.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[Marketing#QuickCampaign](../snippets/csharp/CRMV8/marketing/cs/quickcampaign.cs#quickcampaign)]  
  
### <a name="see-also"></a>Xem thêm  
 [Campaign Entities](campaign-entities.md)   
 [BulkOperation Entity](entities/bulkoperation.md)   
 [Sample: Distribute Campaign Activities to Dynamic and Static Lists](sample-distribute-campaign-activities-dynamic-static-lists.md)   
 [List (Marketing List) Entity](list-marketing-list-entity.md)   
 [Marketing Entities (Campaign, List)](marketing-entities-campaign-list.md)   
 <xref:Microsoft.Crm.Sdk.Messages.AddMemberListRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.PropagateByExpressionRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.CreateActivitiesListRequest>
