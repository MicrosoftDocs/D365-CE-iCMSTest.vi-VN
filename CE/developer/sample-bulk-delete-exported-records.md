---
title: 'Sample: Bulk delete exported records (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: Sample demonstrates how to perform a bulk deletion of records that were previously exported by using the Export-to-Excel option.
keywords: ''
ms.date: 10/31/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: d5483d27-ee03-428f-ad70-2765765ae262
author: JimDaly
ms.author: jdaly
manager: jdaly
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
helpviewer_keywords:
- deleting data in bulk in Microsoft Dynamics CRM, sample for performing a bulk deletion of exported records
- performing a bulk deletion of exported records sample
- sample for performing a bulk deletion of exported records
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: a7158a688a5980fb1896ca27968c666a4abdd4d5
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387389"
---
# <a name="sample-bulk-delete-exported-records"></a><span data-ttu-id="1e2ae-103">Sample: Bulk delete exported records</span><span class="sxs-lookup"><span data-stu-id="1e2ae-103">Sample: Bulk delete exported records</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="1e2ae-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="1e2ae-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="1e2ae-105">Download the sample: [Work with deleting data in bulk](https://code.msdn.microsoft.com/Samples-of-delete-data-in-722dd420).</span><span class="sxs-lookup"><span data-stu-id="1e2ae-105">Download the sample: [Work with deleting data in bulk](https://code.msdn.microsoft.com/Samples-of-delete-data-in-722dd420).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1e2ae-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="1e2ae-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="1e2ae-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="1e2ae-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="1e2ae-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="1e2ae-108">Demonstrates</span></span>  
 <span data-ttu-id="1e2ae-109">This sample shows how to perform a *bulk deletion* of records that were previously exported from [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] by using the **Export to Excel** option.</span><span class="sxs-lookup"><span data-stu-id="1e2ae-109">This sample shows how to perform a *bulk deletion* of records that were previously exported from [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] by using the **Export to Excel** option.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1e2ae-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="1e2ae-110">Example</span></span>  
 [!code-csharp[BulkDelete#BulkDeleteBackup](../snippets/csharp/CRMV8/bulkdelete/cs/bulkdeletebackup.cs#bulkdeletebackup)]  
  
### <a name="see-also"></a><span data-ttu-id="1e2ae-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="1e2ae-111">See also</span></span>  
 <span data-ttu-id="1e2ae-112">[Delete Data in Bulk in Dynamics 365 for Customer Engagement apps](delete-data-bulk.md) </span><span class="sxs-lookup"><span data-stu-id="1e2ae-112">[Delete Data in Bulk in Dynamics 365 for Customer Engagement apps](delete-data-bulk.md) </span></span>  
 <span data-ttu-id="1e2ae-113">[Run Bulk Delete](run-bulk-delete.md) </span><span class="sxs-lookup"><span data-stu-id="1e2ae-113">[Run Bulk Delete](run-bulk-delete.md) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.BulkDeleteRequest>   
 <span data-ttu-id="1e2ae-114">[Recurrence Pattern in Asynchronous Job Execution](recurrence-pattern-asynchronous-job-execution.md) </span><span class="sxs-lookup"><span data-stu-id="1e2ae-114">[Recurrence Pattern in Asynchronous Job Execution](recurrence-pattern-asynchronous-job-execution.md) </span></span>  
 [<span data-ttu-id="1e2ae-115">Sample: Bulk Delete Records That Match Common Criteria</span><span class="sxs-lookup"><span data-stu-id="1e2ae-115">Sample: Bulk Delete Records That Match Common Criteria</span></span>](sample-bulk-delete-records-match-common-criteria.md)
