---
title: 'Sample: Enable duplicate detection and retrieve duplicates (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: Sample demonstrating how to enable duplicate detection and retrieve duplicate records based on active duplicate detection rules.
ms.custom: ''
ms.date: 11/15/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- detecting duplicate data in Microsoft Dynamics CRM, sample for enabling duplicate detection and retrieving duplicates
- duplicate detection, sample for enabling duplicate detection and retrieving duplicates
- enabling duplicate detection and retrieving duplicates sample
- sample for enabling duplicate detection and retrieving duplicates
ms.assetid: f3c2e3c0-5d17-43d8-a614-d772ae1c747e
caps.latest.revision: 14
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 11aa1b58d8d637bdeed043abe6a97886aaf0f780
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387218"
---
# <a name="sample-enable-duplicate-detection-and-retrieve-duplicates"></a><span data-ttu-id="2b1c5-103">Sample: Enable duplicate detection and retrieve duplicates</span><span class="sxs-lookup"><span data-stu-id="2b1c5-103">Sample: Enable duplicate detection and retrieve duplicates</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="2b1c5-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="2b1c5-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span></span> <span data-ttu-id="2b1c5-105">Download the sample: [work with duplicate detections](https://code.msdn.microsoft.com/Work-with-duplicate-9c7d6f59).</span><span class="sxs-lookup"><span data-stu-id="2b1c5-105">Download the sample: [work with duplicate detections](https://code.msdn.microsoft.com/Work-with-duplicate-9c7d6f59).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2b1c5-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="2b1c5-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="2b1c5-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="2b1c5-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="2b1c5-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="2b1c5-108">Demonstrates</span></span>  
 <span data-ttu-id="2b1c5-109">This sample shows how to enable duplicate detection and retrieve duplicate records.</span><span class="sxs-lookup"><span data-stu-id="2b1c5-109">This sample shows how to enable duplicate detection and retrieve duplicate records.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2b1c5-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="2b1c5-110">Example</span></span>  
 [!code-csharp[DuplicateDetection#EnableDuplicateDetectionAndRetrieveDuplicates](../../snippets/csharp/CRMV8/duplicatedetection/cs/enableduplicatedetectionandretrieveduplicates.cs#enableduplicatedetectionandretrieveduplicates)]  
  
### <a name="see-also"></a><span data-ttu-id="2b1c5-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="2b1c5-111">See also</span></span>  
 <span data-ttu-id="2b1c5-112">[Detect duplicate data in Dynamics 365 for Customer Engagement apps](../detect-duplicate-data-for-developers.md) </span><span class="sxs-lookup"><span data-stu-id="2b1c5-112">[Detect duplicate data in Dynamics 365 for Customer Engagement apps](../detect-duplicate-data-for-developers.md) </span></span>  
 [<span data-ttu-id="2b1c5-113">Enable and disable duplicate detection</span><span class="sxs-lookup"><span data-stu-id="2b1c5-113">Enable and disable duplicate detection</span></span>](../enable-disable-duplicate-detection.md)  
 [<span data-ttu-id="2b1c5-114">Manage duplicate detection during Create and Update operations</span><span class="sxs-lookup"><span data-stu-id="2b1c5-114">Manage duplicate detection during Create and Update operations</span></span>](manage-duplicate-detection-create-update.md)  
 <span data-ttu-id="2b1c5-115">[Run Duplicate Detection](../run-duplicate-detection.md) </span><span class="sxs-lookup"><span data-stu-id="2b1c5-115">[Run Duplicate Detection](../run-duplicate-detection.md) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.RetrieveDuplicatesRequest>   
 [<span data-ttu-id="2b1c5-116">Sample: Invoke Duplicate Detection For Creating and Updating Records</span><span class="sxs-lookup"><span data-stu-id="2b1c5-116">Sample: Invoke Duplicate Detection For Creating and Updating Records</span></span>](sample-use-duplicate-detection-when-creating-and-updating-records.md)
