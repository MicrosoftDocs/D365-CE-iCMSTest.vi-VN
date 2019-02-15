---
title: 'Sample: Use duplicate detection when creating and updating records (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: Sample demonstrating how to detect duplicate records when when creating and updating entity records.
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
- running duplicate detection to create and update records sample
- duplicate detection, sample for invoking duplicate detection to create and update records
- detecting duplicate data in Microsoft Dynamics CRM, sample for invoking duplicate detection to create and update records
- sample for running duplicate detection to create and update records
- sample for invoking duplicate detection to create and update records
- invoking duplicate detection to create and update records sample
ms.assetid: 99e3570c-39d6-46a2-9574-e8dedc99fd65
caps.latest.revision: 14
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 1e92107eca75408cb81049b72e41d889f8ff19f3
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386400"
---
# <a name="sample-use-duplicate-detection-when-creating-and-updating-records"></a><span data-ttu-id="1a84d-103">Sample: Use duplicate detection when creating and updating records</span><span class="sxs-lookup"><span data-stu-id="1a84d-103">Sample: Use duplicate detection when creating and updating records</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="1a84d-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="1a84d-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span></span> <span data-ttu-id="1a84d-105">Download the sample: [work with duplicate detections](https://code.msdn.microsoft.com/Work-with-duplicate-9c7d6f59).</span><span class="sxs-lookup"><span data-stu-id="1a84d-105">Download the sample: [work with duplicate detections](https://code.msdn.microsoft.com/Work-with-duplicate-9c7d6f59).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1a84d-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="1a84d-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="1a84d-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="1a84d-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="1a84d-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="1a84d-108">Demonstrates</span></span>  
 <span data-ttu-id="1a84d-109">This sample shows how to invoke duplicate detection for creating and updating entity records.</span><span class="sxs-lookup"><span data-stu-id="1a84d-109">This sample shows how to invoke duplicate detection for creating and updating entity records.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1a84d-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="1a84d-110">Example</span></span>  
 [!code-csharp[DuplicateDetection#InvokeDuplicateDetectionForCreateAndUpdate](../../snippets/csharp/CRMV8/duplicatedetection/cs/invokeduplicatedetectionforcreateandupdate.cs#invokeduplicatedetectionforcreateandupdate)]  
  
### <a name="see-also"></a><span data-ttu-id="1a84d-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="1a84d-111">See also</span></span>  
 <span data-ttu-id="1a84d-112">[Detect Duplicate Data in Dynamics 365 for Customer Engagement apps](../detect-duplicate-data-for-developers.md) </span><span class="sxs-lookup"><span data-stu-id="1a84d-112">[Detect Duplicate Data in Dynamics 365 for Customer Engagement apps](../detect-duplicate-data-for-developers.md) </span></span>  
 <span data-ttu-id="1a84d-113">[Run Duplicate Detection](../run-duplicate-detection.md) </span><span class="sxs-lookup"><span data-stu-id="1a84d-113">[Run Duplicate Detection](../run-duplicate-detection.md) </span></span>  
 <span data-ttu-id="1a84d-114">[Use Messages (Request and Response Classes) with the Execute Method](use-messages-request-response-classes-execute-method.md) </span><span class="sxs-lookup"><span data-stu-id="1a84d-114">[Use Messages (Request and Response Classes) with the Execute Method](use-messages-request-response-classes-execute-method.md) </span></span>  
 <span data-ttu-id="1a84d-115">[Pass Optional Parameters in Messages](use-messages-request-response-classes-execute-method.md#bkmk_optional_params) </span><span class="sxs-lookup"><span data-stu-id="1a84d-115">[Pass Optional Parameters in Messages](use-messages-request-response-classes-execute-method.md#bkmk_optional_params) </span></span>  
 <span data-ttu-id="1a84d-116">[Sample: Detect Multiple Duplicate Records](sample-detect-multiple-duplicate-records.md) [Sample: Enable duplicate detection and retrieve duplicates](sample-enable-duplicate-detection-and-retrieve-duplicates.md)</span><span class="sxs-lookup"><span data-stu-id="1a84d-116">[Sample: Detect Multiple Duplicate Records](sample-detect-multiple-duplicate-records.md) [Sample: Enable duplicate detection and retrieve duplicates](sample-enable-duplicate-detection-and-retrieve-duplicates.md)</span></span>  
 [<span data-ttu-id="1a84d-117">Duplicate detection messages</span><span class="sxs-lookup"><span data-stu-id="1a84d-117">Duplicate detection messages</span></span>](../duplicate-detection-messages.md)
