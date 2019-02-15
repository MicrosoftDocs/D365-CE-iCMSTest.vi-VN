---
title: Manage duplicate detection for create and update operations (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Read how to detect duplicates during create and update operations using the Dynamics 365 for Customer Engagement Web API and Organization service.
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
- duplicate detection, Web API, Organization Service
ms.assetid: 5B84D5F0-CFB6-4212-ACCB-03AE81271F1E
caps.latest.revision: 25
author: SushantSikka
ms.author: susikka
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 535031698f07a75832e6ceb79d9a953d829b728c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386199"
---
# <a name="manage-duplicate-detection-for-create-and-update-operations"></a><span data-ttu-id="dbc0a-103">Manage duplicate detection for create and update operations</span><span class="sxs-lookup"><span data-stu-id="dbc0a-103">Manage duplicate detection for create and update operations</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="dbc0a-104">Dynamics 365 for Customer Engagement Web API allows you to detect duplicate records of an existing record in order to maintain integrity of data.</span><span class="sxs-lookup"><span data-stu-id="dbc0a-104">Dynamics 365 for Customer Engagement Web API allows you to detect duplicate records of an existing record in order to maintain integrity of data.</span></span> 

<a name="BKMK_webapi"></a>

## <a name="using-web-api"></a><span data-ttu-id="dbc0a-105">Using Web API</span><span class="sxs-lookup"><span data-stu-id="dbc0a-105">Using Web API</span></span>

<span data-ttu-id="dbc0a-106">Use Preference header `MSCRM.SuppressDuplicateDetection` and set its value to `false` to detect creation of a duplicate record during Create and Update operations.</span><span class="sxs-lookup"><span data-stu-id="dbc0a-106">Use Preference header `MSCRM.SuppressDuplicateDetection` and set its value to `false` to detect creation of a duplicate record during Create and Update operations.</span></span>

> [!NOTE]
>  <span data-ttu-id="dbc0a-107">Make sure there are appropriate duplicate detection rules in place.</span><span class="sxs-lookup"><span data-stu-id="dbc0a-107">Make sure there are appropriate duplicate detection rules in place.</span></span> <span data-ttu-id="dbc0a-108">Dynamics 365 for Customer Engagement apps includes default duplicate detection rules for accounts, contacts, and leads, but not for other types of records.</span><span class="sxs-lookup"><span data-stu-id="dbc0a-108">Dynamics 365 for Customer Engagement apps includes default duplicate detection rules for accounts, contacts, and leads, but not for other types of records.</span></span> <span data-ttu-id="dbc0a-109">If you want the system to detect duplicates for other record types, you’ll need to create a new rule.</span><span class="sxs-lookup"><span data-stu-id="dbc0a-109">If you want the system to detect duplicates for other record types, you’ll need to create a new rule.</span></span> <span data-ttu-id="dbc0a-110">For information on how to create a duplicate detection rule, see [Duplicate detection rules](../admin/set-up-duplicate-detection-rules-keep-data-clean.md).</span><span class="sxs-lookup"><span data-stu-id="dbc0a-110">For information on how to create a duplicate detection rule, see [Duplicate detection rules](../admin/set-up-duplicate-detection-rules-keep-data-clean.md).</span></span>

<span data-ttu-id="dbc0a-111">For more information and examples on how to prohibit creation of duplicate records during create and update operations, see [Manage duplicate detection for create and update operations using Web API](webapi/manage-duplicate-detection-create-update.md).</span><span class="sxs-lookup"><span data-stu-id="dbc0a-111">For more information and examples on how to prohibit creation of duplicate records during create and update operations, see [Manage duplicate detection for create and update operations using Web API](webapi/manage-duplicate-detection-create-update.md).</span></span>

<a name="BKMK_orgservice"></a>

## <a name="using-organization-service"></a><span data-ttu-id="dbc0a-112">Using Organization Service</span><span class="sxs-lookup"><span data-stu-id="dbc0a-112">Using Organization Service</span></span>

<span data-ttu-id="dbc0a-113">Use `SuppressDuplicateDetection` parameter and set its value to `false` to activate duplicate detection and prohibit creation of a duplicate record during create and update operations.</span><span class="sxs-lookup"><span data-stu-id="dbc0a-113">Use `SuppressDuplicateDetection` parameter and set its value to `false` to activate duplicate detection and prohibit creation of a duplicate record during create and update operations.</span></span>

<span data-ttu-id="dbc0a-114">For more information and example on how to prohibit creation of duplicate records during create and update operations, see [Manage duplicate detection for create and update operations using Organization Service](org-service/manage-duplicate-detection-create-update.md).</span><span class="sxs-lookup"><span data-stu-id="dbc0a-114">For more information and example on how to prohibit creation of duplicate records during create and update operations, see [Manage duplicate detection for create and update operations using Organization Service](org-service/manage-duplicate-detection-create-update.md).</span></span>

### <a name="see-also"></a><span data-ttu-id="dbc0a-115">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="dbc0a-115">See Also</span></span>

[<span data-ttu-id="dbc0a-116">Manage duplicate detection during Create and Update operation using Web API</span><span class="sxs-lookup"><span data-stu-id="dbc0a-116">Manage duplicate detection during Create and Update operation using Web API</span></span>](webapi/manage-duplicate-detection-create-update.md)  
[<span data-ttu-id="dbc0a-117">Manage duplicate detection during Create and Update operation using Organization Service</span><span class="sxs-lookup"><span data-stu-id="dbc0a-117">Manage duplicate detection during Create and Update operation using Organization Service</span></span>](org-service/manage-duplicate-detection-create-update.md)  
[<span data-ttu-id="dbc0a-118">Sample: Use duplicate detection when creating and updating records</span><span class="sxs-lookup"><span data-stu-id="dbc0a-118">Sample: Use duplicate detection when creating and updating records</span></span>](org-service/sample-use-duplicate-detection-when-creating-and-updating-records.md)  
[<span data-ttu-id="dbc0a-119">Sample: Detect multiple duplicate records</span><span class="sxs-lookup"><span data-stu-id="dbc0a-119">Sample: Detect multiple duplicate records</span></span>](org-service/sample-detect-multiple-duplicate-records.md)  
[<span data-ttu-id="dbc0a-120">Run duplicate detection</span><span class="sxs-lookup"><span data-stu-id="dbc0a-120">Run duplicate detection</span></span>](run-duplicate-detection.md)
