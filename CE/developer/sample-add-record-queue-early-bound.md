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
# <a name="sample-add-a-record-to-a-queue-early-bound"></a><span data-ttu-id="c102d-102">Sample: Add a record to a queue (early bound)</span><span class="sxs-lookup"><span data-stu-id="c102d-102">Sample: Add a record to a queue (early bound)</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="c102d-103">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="c102d-103">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="c102d-104">[Download the Business management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62).</span><span class="sxs-lookup"><span data-stu-id="c102d-104">[Download the Business management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62).</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="c102d-105">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="c102d-105">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
   
## <a name="requirements"></a><span data-ttu-id="c102d-106">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="c102d-106">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="c102d-107">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="c102d-107">Demonstrates</span></span>  
 <span data-ttu-id="c102d-108">This sample shows how to add a record to a queue.</span><span class="sxs-lookup"><span data-stu-id="c102d-108">This sample shows how to add a record to a queue.</span></span> <span data-ttu-id="c102d-109">It creates source and destination queues.</span><span class="sxs-lookup"><span data-stu-id="c102d-109">It creates source and destination queues.</span></span> <span data-ttu-id="c102d-110">It adds a letter activity to the source queue and then moves it to the destination queue.</span><span class="sxs-lookup"><span data-stu-id="c102d-110">It adds a letter activity to the source queue and then moves it to the destination queue.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c102d-111">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="c102d-111">Example</span></span>  
 [!code-csharp[BusinessManagement#AddToQueue](../snippets/csharp/CRMV8/businessmanagement/cs/addtoqueue.cs#addtoqueue)]  
  
### <a name="see-also"></a><span data-ttu-id="c102d-112">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="c102d-112">See also</span></span>  
 <span data-ttu-id="c102d-113">[Sample Code for Queue Entities](sample-code-queue-entities.md) </span><span class="sxs-lookup"><span data-stu-id="c102d-113">[Sample Code for Queue Entities](sample-code-queue-entities.md) </span></span>  
 <span data-ttu-id="c102d-114">[Queue Entities](queue-entities.md) </span><span class="sxs-lookup"><span data-stu-id="c102d-114">[Queue Entities](queue-entities.md) </span></span>  
 <span data-ttu-id="c102d-115">[Sample: Clean Up History for a Queue (Early Bound)](sample-clean-up-history-queue-early-bound.md) </span><span class="sxs-lookup"><span data-stu-id="c102d-115">[Sample: Clean Up History for a Queue (Early Bound)](sample-clean-up-history-queue-early-bound.md) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.AddToQueueRequest>
