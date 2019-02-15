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
# <a name="sample-clean-up-history-for-a-queue-early-bound"></a><span data-ttu-id="73ce8-102">Sample: Clean up history for a queue (early bound)</span><span class="sxs-lookup"><span data-stu-id="73ce8-102">Sample: Clean up history for a queue (early bound)</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="73ce8-103">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="73ce8-103">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="73ce8-104">Download the complete sample here [Business management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62)</span><span class="sxs-lookup"><span data-stu-id="73ce8-104">Download the complete sample here [Business management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62)</span></span>   

## <a name="prerequisites"></a><span data-ttu-id="73ce8-105">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="73ce8-105">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
   
## <a name="requirements"></a><span data-ttu-id="73ce8-106">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="73ce8-106">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="73ce8-107">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="73ce8-107">Demonstrates</span></span>  
 <span data-ttu-id="73ce8-108">This sample shows how to clean up the history for the queue by using <xref:Microsoft.Crm.Sdk.Messages.RemoveFromQueueRequest> with inactive items.</span><span class="sxs-lookup"><span data-stu-id="73ce8-108">This sample shows how to clean up the history for the queue by using <xref:Microsoft.Crm.Sdk.Messages.RemoveFromQueueRequest> with inactive items.</span></span> <span data-ttu-id="73ce8-109">It finds completed phone calls in the queue and removes the associated queue items.</span><span class="sxs-lookup"><span data-stu-id="73ce8-109">It finds completed phone calls in the queue and removes the associated queue items.</span></span>  
  
## <a name="example"></a><span data-ttu-id="73ce8-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="73ce8-110">Example</span></span>  
 [!code-csharp[BusinessManagement#CleanUpQueueItems](../snippets/csharp/CRMV8/businessmanagement/cs/cleanupqueueitems.cs#cleanupqueueitems)]  
  
### <a name="see-also"></a><span data-ttu-id="73ce8-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="73ce8-111">See also</span></span>  
 <span data-ttu-id="73ce8-112">[Sample Code for Queue Entities](sample-code-queue-entities.md) </span><span class="sxs-lookup"><span data-stu-id="73ce8-112">[Sample Code for Queue Entities](sample-code-queue-entities.md) </span></span>  
 <span data-ttu-id="73ce8-113">[Queue Entities](queue-entities.md) </span><span class="sxs-lookup"><span data-stu-id="73ce8-113">[Queue Entities](queue-entities.md) </span></span>  
 <span data-ttu-id="73ce8-114">[Sample: Specify a Queue Item to Work On (Early Bound)](sample-specify-queue-item-work-early-bound.md) </span><span class="sxs-lookup"><span data-stu-id="73ce8-114">[Sample: Specify a Queue Item to Work On (Early Bound)](sample-specify-queue-item-work-early-bound.md) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.AddToQueueRequest>
