---
title: 'Sample: Specify a queue item to work on (early bound) (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
decription: The sample code demonstrates how to use PickFromQueueRequest to specify a user who will work on a queue item.
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
- sample for specifying queue items for users to work on (early bound)
- specifying queue items for users to work on (early bound), sample
ms.assetid: be171519-f8d0-43e6-b5a7-770802da47db
caps.latest.revision: 18
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 052ce240627dad792a76a4edc1101d39d68fefa5
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387452"
---
# <a name="sample-specify-a-queue-item-to-work-on-early-bound"></a>Sample: Specify a queue item to work on (early bound)

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. Download the complete sample here [Business Management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62) 

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
   
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to use <xref:Microsoft.Crm.Sdk.Messages.PickFromQueueRequest> to specify a user who will work on a queue item.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[BusinessManagement#AssignQueueItemWorker](../snippets/csharp/CRMV8/businessmanagement/cs/assignqueueitemworker.cs#assignqueueitemworker)]  
  
### <a name="see-also"></a>Xem thêm  
 [Sample Code for Queue Entities](sample-code-queue-entities.md)   
 [Queue Entities](queue-entities.md)   
 [Sample: Release a Queue Item to the Queue Using (Early Bound)](sample-release-queue-item-queue-early-bound.md)
