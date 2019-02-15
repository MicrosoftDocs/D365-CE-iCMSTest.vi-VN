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
# <a name="sample-specify-a-queue-item-to-work-on-early-bound"></a><span data-ttu-id="f40e0-102">Sample: Specify a queue item to work on (early bound)</span><span class="sxs-lookup"><span data-stu-id="f40e0-102">Sample: Specify a queue item to work on (early bound)</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="f40e0-103">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="f40e0-103">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="f40e0-104">Download the complete sample here [Business Management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62)</span><span class="sxs-lookup"><span data-stu-id="f40e0-104">Download the complete sample here [Business Management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62)</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="f40e0-105">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="f40e0-105">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
   
## <a name="requirements"></a><span data-ttu-id="f40e0-106">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="f40e0-106">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="f40e0-107">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="f40e0-107">Demonstrates</span></span>  
 <span data-ttu-id="f40e0-108">This sample shows how to use <xref:Microsoft.Crm.Sdk.Messages.PickFromQueueRequest> to specify a user who will work on a queue item.</span><span class="sxs-lookup"><span data-stu-id="f40e0-108">This sample shows how to use <xref:Microsoft.Crm.Sdk.Messages.PickFromQueueRequest> to specify a user who will work on a queue item.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f40e0-109">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="f40e0-109">Example</span></span>  
 [!code-csharp[BusinessManagement#AssignQueueItemWorker](../snippets/csharp/CRMV8/businessmanagement/cs/assignqueueitemworker.cs#assignqueueitemworker)]  
  
### <a name="see-also"></a><span data-ttu-id="f40e0-110">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="f40e0-110">See also</span></span>  
 <span data-ttu-id="f40e0-111">[Sample Code for Queue Entities](sample-code-queue-entities.md) </span><span class="sxs-lookup"><span data-stu-id="f40e0-111">[Sample Code for Queue Entities](sample-code-queue-entities.md) </span></span>  
 <span data-ttu-id="f40e0-112">[Queue Entities](queue-entities.md) </span><span class="sxs-lookup"><span data-stu-id="f40e0-112">[Queue Entities](queue-entities.md) </span></span>  
 [<span data-ttu-id="f40e0-113">Sample: Release a Queue Item to the Queue Using (Early Bound)</span><span class="sxs-lookup"><span data-stu-id="f40e0-113">Sample: Release a Queue Item to the Queue Using (Early Bound)</span></span>](sample-release-queue-item-queue-early-bound.md)
