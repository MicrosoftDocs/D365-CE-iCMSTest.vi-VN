---
title: 'Sample: Detect multiple duplicate records (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: Sample demonstrates how to detect and log multiple duplicate records for a specified entity type.
keywords: ''
ms.date: 10/31/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 5c83c1c2-25ef-480b-9195-6eabe9f6c4c7
author: JimDaly
ms.author: jdaly
manager: jdaly
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
caps.latest.revision: 13
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 99536dde5ea28cf9ff2da4962f57a89ca8616cda
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387493"
---
# <a name="sample-detect-multiple-duplicate-records"></a><span data-ttu-id="412e6-103">Sample: Detect multiple duplicate records</span><span class="sxs-lookup"><span data-stu-id="412e6-103">Sample: Detect multiple duplicate records</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="412e6-104">This sample code is for Dynamics 365 for Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="412e6-104">This sample code is for Dynamics 365 for Customer Engagement.</span></span> <span data-ttu-id="412e6-105">Download the sample: [With with duplicate detections](https://code.msdn.microsoft.com/Work-with-duplicate-9c7d6f59).</span><span class="sxs-lookup"><span data-stu-id="412e6-105">Download the sample: [With with duplicate detections](https://code.msdn.microsoft.com/Work-with-duplicate-9c7d6f59).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="412e6-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="412e6-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="412e6-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="412e6-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="412e6-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="412e6-108">Demonstrates</span></span>  
 <span data-ttu-id="412e6-109">This sample shows how to detect and log multiple duplicate records for a specified entity type.</span><span class="sxs-lookup"><span data-stu-id="412e6-109">This sample shows how to detect and log multiple duplicate records for a specified entity type.</span></span>  
  
## <a name="example"></a><span data-ttu-id="412e6-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="412e6-110">Example</span></span>  
 [!code-csharp[DuplicateDetection#BulkDetectDuplicates](../snippets/csharp/CRMV8/duplicatedetection/cs/bulkdetectduplicates.cs#bulkdetectduplicates)]  
  
### <a name="see-also"></a><span data-ttu-id="412e6-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="412e6-111">See also</span></span>  
 <span data-ttu-id="412e6-112">[Detect Duplicate Data in Dynamics 365 for Customer Engagement apps](detect-duplicate-data-for-developers.md) </span><span class="sxs-lookup"><span data-stu-id="412e6-112">[Detect Duplicate Data in Dynamics 365 for Customer Engagement apps](detect-duplicate-data-for-developers.md) </span></span>  
 <span data-ttu-id="412e6-113">[Enable and disable duplicate detection](enable-disable-duplicate-detection.md) </span><span class="sxs-lookup"><span data-stu-id="412e6-113">[Enable and disable duplicate detection](enable-disable-duplicate-detection.md) </span></span>  
 <span data-ttu-id="412e6-114">[Run Duplicate Detection](run-duplicate-detection.md) </span><span class="sxs-lookup"><span data-stu-id="412e6-114">[Run Duplicate Detection](run-duplicate-detection.md) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.BulkDetectDuplicatesRequest>  
 [<span data-ttu-id="412e6-115">Duplicate detection messages</span><span class="sxs-lookup"><span data-stu-id="412e6-115">Duplicate detection messages</span></span>](duplicate-detection-messages.md)