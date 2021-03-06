---
title: 'Sample: Add a record to a queue (early bound) (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
decription: The sample code demonstrates how to add a record to a queue, and creates source and destination queues.
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
- adding records to queues (early bound), sample
- sample for adding records to queues (early bound)
ms.assetid: 250690a7-854d-4a69-adb9-d621834344fa
caps.latest.revision: 17
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 604d1a40542bfe18b4d49c1c461c0f5f68e5bf72
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386276"
---
# <a name="sample-add-a-record-to-a-queue-early-bound"></a>Sample: Add a record to a queue (early bound)

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. [Download the Business management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62).  

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
   
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to add a record to a queue. It creates source and destination queues. It adds a letter activity to the source queue and then moves it to the destination queue.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[BusinessManagement#AddToQueue](../snippets/csharp/CRMV8/businessmanagement/cs/addtoqueue.cs#addtoqueue)]  
  
### <a name="see-also"></a>Xem thêm  
 [Sample Code for Queue Entities](sample-code-queue-entities.md)   
 [Queue Entities](queue-entities.md)   
 [Sample: Clean Up History for a Queue (Early Bound)](sample-clean-up-history-queue-early-bound.md)   
 <xref:Microsoft.Crm.Sdk.Messages.AddToQueueRequest>
