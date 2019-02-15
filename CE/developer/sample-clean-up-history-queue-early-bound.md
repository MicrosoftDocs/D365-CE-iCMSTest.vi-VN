---
title: 'Sample: Clean up history for a queue (early bound) (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
decription: The sample code demonstrates how to clean up the history for the queue using RemoveFromQueueRequest with inactive items.
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
- cleaning up history in queues (early bound), sample
- sample for deleting inactive items from queues (early bound)
- sample for cleaning up history in queues (early bound)
- deleting inactive items from queues (early bound), sample
ms.assetid: 81d686b0-7c5d-45e5-b2df-b74b0413bf6b
caps.latest.revision: 19
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 9f772d02ee162f607580567dfecdf1dc54637da7
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387451"
---
# <a name="sample-clean-up-history-for-a-queue-early-bound"></a>Sample: Clean up history for a queue (early bound)

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. Download the complete sample here [Business management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62)   

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
   
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to clean up the history for the queue by using <xref:Microsoft.Crm.Sdk.Messages.RemoveFromQueueRequest> with inactive items. It finds completed phone calls in the queue and removes the associated queue items.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[BusinessManagement#CleanUpQueueItems](../snippets/csharp/CRMV8/businessmanagement/cs/cleanupqueueitems.cs#cleanupqueueitems)]  
  
### <a name="see-also"></a>Xem thêm  
 [Sample Code for Queue Entities](sample-code-queue-entities.md)   
 [Queue Entities](queue-entities.md)   
 [Sample: Specify a Queue Item to Work On (Early Bound)](sample-specify-queue-item-work-early-bound.md)   
 <xref:Microsoft.Crm.Sdk.Messages.AddToQueueRequest>
