---
title: Manage duplicate detection for create and update operations using Organization Service (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Read how to detect duplicates during create and update operations using the Dynamics 365 for Customer Engagement Organization service.
ms.custom: ''
ms.date: 11/15/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- duplicate detection, organization service
ms.assetid: A69EDF59-3E81-4C6E-A5C9-EF8DCCF6F936
caps.latest.revision: 25
author: SushantSikka
ms.author: susikka
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: de04767889d605e7fea7c62685aeb11ed5ebd527
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387031"
---
# <a name="manage-duplicate-detection-for-create-and-update-operations-using-organization-service"></a><span data-ttu-id="3d26e-103">Manage duplicate detection for create and update operations using Organization Service</span><span class="sxs-lookup"><span data-stu-id="3d26e-103">Manage duplicate detection for create and update operations using Organization Service</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="3d26e-104">Dynamics 365 for Customer Engagement Web API allows you to detect duplicate records of an existing record in order to maintain integrity of data.</span><span class="sxs-lookup"><span data-stu-id="3d26e-104">Dynamics 365 for Customer Engagement Web API allows you to detect duplicate records of an existing record in order to maintain integrity of data.</span></span> 

<span data-ttu-id="3d26e-105">Use `SuppressDuplicateDetection` parameter and set its value to `false` to activate duplicate detection and prohibit creation of a duplicate record during create and update operations.</span><span class="sxs-lookup"><span data-stu-id="3d26e-105">Use `SuppressDuplicateDetection` parameter and set its value to `false` to activate duplicate detection and prohibit creation of a duplicate record during create and update operations.</span></span>

<span data-ttu-id="3d26e-106">The example shown below illustrates how to create a duplicate record by suppressing duplicate detection.</span><span class="sxs-lookup"><span data-stu-id="3d26e-106">The example shown below illustrates how to create a duplicate record by suppressing duplicate detection.</span></span> <span data-ttu-id="3d26e-107">Change the value of `SuppressDuplicateDetection` parameter to `false` to prohibit creation of a duplicate record.</span><span class="sxs-lookup"><span data-stu-id="3d26e-107">Change the value of `SuppressDuplicateDetection` parameter to `false` to prohibit creation of a duplicate record.</span></span>

[!code-csharp[DuplicateDetection#DuplicateDetectionCreate](../../snippets/csharp/CRMV8/duplicatedetection/cs/duplicatedetectioncreate.cs#duplicatedetectioncreate)]

<span data-ttu-id="3d26e-108">Find the complete code sample, see [Sample: Use duplicate detection when creating and updating records](sample-use-duplicate-detection-when-creating-and-updating-records.md).</span><span class="sxs-lookup"><span data-stu-id="3d26e-108">Find the complete code sample, see [Sample: Use duplicate detection when creating and updating records](sample-use-duplicate-detection-when-creating-and-updating-records.md).</span></span>

### <a name="see-also"></a><span data-ttu-id="3d26e-109">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="3d26e-109">See Also</span></span>

[<span data-ttu-id="3d26e-110">Detect duplicate data for developers</span><span class="sxs-lookup"><span data-stu-id="3d26e-110">Detect duplicate data for developers</span></span>](../detect-duplicate-data-for-developers.md)  
[<span data-ttu-id="3d26e-111">Run duplicate detection</span><span class="sxs-lookup"><span data-stu-id="3d26e-111">Run duplicate detection</span></span>](../run-duplicate-detection.md)  
[<span data-ttu-id="3d26e-112">Sample: Use duplicate detection when creating and updating records</span><span class="sxs-lookup"><span data-stu-id="3d26e-112">Sample: Use duplicate detection when creating and updating records</span></span>](sample-use-duplicate-detection-when-creating-and-updating-records.md)  
[<span data-ttu-id="3d26e-113">Sample: Enable duplicate detection and retrieve duplicates</span><span class="sxs-lookup"><span data-stu-id="3d26e-113">Sample: Enable duplicate detection and retrieve duplicates</span></span>](sample-enable-duplicate-detection-and-retrieve-duplicates.md)
