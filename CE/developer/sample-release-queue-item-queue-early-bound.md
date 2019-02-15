---
title: 'Sample: Release a queue item to the queue (early bound) (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
decription: The sample code demonstrates how to use ReleaseToQueueRequest to dissociate a user from a queue item release a queue item back to the queue.
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
- dissociating users from queue items and returning items to queues, sample
- releasing queue items back to queues (early bound), sample
- sample for releasing queue items back to queues (early bound)
ms.assetid: 87c72e1e-3ea8-4c54-8eb2-e7fbc19ff629
caps.latest.revision: 17
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 331f771eda914ec4eb383dc3ad942f085c9517b8
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388505"
---
# <a name="sample-release-a-queue-item-to-the-queue-early-bound"></a><span data-ttu-id="02d09-102">Sample: Release a queue item to the queue (early bound)</span><span class="sxs-lookup"><span data-stu-id="02d09-102">Sample: Release a queue item to the queue (early bound)</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="02d09-103">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="02d09-103">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="02d09-104">[Download the Business Management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62).</span><span class="sxs-lookup"><span data-stu-id="02d09-104">[Download the Business Management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="02d09-105">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="02d09-105">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
   
## <a name="requirements"></a><span data-ttu-id="02d09-106">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="02d09-106">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="02d09-107">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="02d09-107">Demonstrates</span></span>  
 <span data-ttu-id="02d09-108">This sample shows how to use <xref:Microsoft.Crm.Sdk.Messages.ReleaseToQueueRequest> to dissociate a user from a queue item that he or she worked on and release a queue item back to the queue.</span><span class="sxs-lookup"><span data-stu-id="02d09-108">This sample shows how to use <xref:Microsoft.Crm.Sdk.Messages.ReleaseToQueueRequest> to dissociate a user from a queue item that he or she worked on and release a queue item back to the queue.</span></span>  
  
## <a name="example"></a><span data-ttu-id="02d09-109">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="02d09-109">Example</span></span>  
 [!code-csharp[BusinessManagement#RemoveQueueItemWorker](../snippets/csharp/CRMV8/businessmanagement/cs/removequeueitemworker.cs#removequeueitemworker)]  
  
### <a name="see-also"></a><span data-ttu-id="02d09-110">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="02d09-110">See also</span></span>  
 <span data-ttu-id="02d09-111">[Sample Code for Queue Entities](sample-code-queue-entities.md) </span><span class="sxs-lookup"><span data-stu-id="02d09-111">[Sample Code for Queue Entities](sample-code-queue-entities.md) </span></span>  
 [<span data-ttu-id="02d09-112">Queue Entities</span><span class="sxs-lookup"><span data-stu-id="02d09-112">Queue Entities</span></span>](queue-entities.md)
