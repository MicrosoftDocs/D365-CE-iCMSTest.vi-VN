---
title: 'Sample: Bulk delete records that match common criteria (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: Sample demonstrates how to delete records, in bulk, that match common criteria.
keywords: ''
ms.date: 10/31/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 1e5fb8b0-5938-4af7-a21d-7365b27b6e1e
author: JimDaly
ms.author: jdaly
manager: jdaly
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
helpviewer_keywords:
- bulk deletion of records that match common criteria sample
- sample for deleting related records in bulk
- deleting data in bulk in Microsoft Dynamics CRM, sample for bulk deletion of records that match common criteria
- deleting data in bulk in Microsoft Dynamics CRM, sample for deleting related records in bulk
- deleting related records in bulk sample
- sample for bulk deletion of records that match common criteria
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: c66883bdb7996866fc265c97d799a06d24a0e92a
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388586"
---
# <a name="sample-bulk-delete-records-that-match-common-criteria"></a><span data-ttu-id="41551-103">Sample: Bulk delete records that match common criteria</span><span class="sxs-lookup"><span data-stu-id="41551-103">Sample: Bulk delete records that match common criteria</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="41551-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="41551-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="41551-105">Download the sample: [Work with deleting data in bulk](https://code.msdn.microsoft.com/Samples-of-delete-data-in-722dd420).</span><span class="sxs-lookup"><span data-stu-id="41551-105">Download the sample: [Work with deleting data in bulk](https://code.msdn.microsoft.com/Samples-of-delete-data-in-722dd420).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="41551-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="41551-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="41551-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="41551-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="41551-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="41551-108">Demonstrates</span></span>  
 <span data-ttu-id="41551-109">This sample shows how to delete records, in bulk, that match common criteria.</span><span class="sxs-lookup"><span data-stu-id="41551-109">This sample shows how to delete records, in bulk, that match common criteria.</span></span>  
  
## <a name="example"></a><span data-ttu-id="41551-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="41551-110">Example</span></span>  
 [!code-csharp[BulkDelete#BulkDeleteOperations](../snippets/csharp/CRMV8/bulkdelete/cs/bulkdeleteoperations.cs#bulkdeleteoperations)]  
  
### <a name="see-also"></a><span data-ttu-id="41551-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="41551-111">See also</span></span>  
 <span data-ttu-id="41551-112">[Delete Data in Bulk in Dynamics 365 for Customer Engagement apps](delete-data-bulk.md) </span><span class="sxs-lookup"><span data-stu-id="41551-112">[Delete Data in Bulk in Dynamics 365 for Customer Engagement apps](delete-data-bulk.md) </span></span>  
 <span data-ttu-id="41551-113">[Run Bulk Delete](run-bulk-delete.md) </span><span class="sxs-lookup"><span data-stu-id="41551-113">[Run Bulk Delete](run-bulk-delete.md) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.BulkDeleteRequest>   
 [<span data-ttu-id="41551-114">Recurrence Pattern in Asynchronous Job Execution</span><span class="sxs-lookup"><span data-stu-id="41551-114">Recurrence Pattern in Asynchronous Job Execution</span></span>](recurrence-pattern-asynchronous-job-execution.md)
