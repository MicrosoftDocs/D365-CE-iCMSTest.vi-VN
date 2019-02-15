---
title: 'Sample: Distribute a quick campaign (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The sample code demonstrates how to create and distribute a quick campaign.
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
- distributing a quick campaign, marketing entities sample
- sample for distributing a quick campaign
ms.assetid: adc93a60-1736-4ea0-a90b-4ca6c8fcfa35
caps.latest.revision: 23
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: fdcd2fc0f22ae8088b6a4884574f7ad9f7c33d76
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385798"
---
# <a name="sample-distribute-a-quick-campaign"></a><span data-ttu-id="efcf7-103">Sample: Distribute a quick campaign</span><span class="sxs-lookup"><span data-stu-id="efcf7-103">Sample: Distribute a quick campaign</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="efcf7-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="efcf7-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="efcf7-105">Download the complete sample from [Sample: Work with Marketing entities](https://code.msdn.microsoft.com/Marketing-Samples-c5429380).</span><span class="sxs-lookup"><span data-stu-id="efcf7-105">Download the complete sample from [Sample: Work with Marketing entities](https://code.msdn.microsoft.com/Marketing-Samples-c5429380).</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="efcf7-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="efcf7-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="efcf7-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="efcf7-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="efcf7-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="efcf7-108">Demonstrates</span></span>  
 <span data-ttu-id="efcf7-109">This sample shows how to create and distribute a quick campaign.</span><span class="sxs-lookup"><span data-stu-id="efcf7-109">This sample shows how to create and distribute a quick campaign.</span></span>  
  
## <a name="example"></a><span data-ttu-id="efcf7-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="efcf7-110">Example</span></span>  
 [!code-csharp[Marketing#QuickCampaign](../snippets/csharp/CRMV8/marketing/cs/quickcampaign.cs#quickcampaign)]  
  
### <a name="see-also"></a><span data-ttu-id="efcf7-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="efcf7-111">See also</span></span>  
 <span data-ttu-id="efcf7-112">[Campaign Entities](campaign-entities.md) </span><span class="sxs-lookup"><span data-stu-id="efcf7-112">[Campaign Entities](campaign-entities.md) </span></span>  
 <span data-ttu-id="efcf7-113">[BulkOperation Entity](entities/bulkoperation.md) </span><span class="sxs-lookup"><span data-stu-id="efcf7-113">[BulkOperation Entity](entities/bulkoperation.md) </span></span>  
 <span data-ttu-id="efcf7-114">[Sample: Distribute Campaign Activities to Dynamic and Static Lists](sample-distribute-campaign-activities-dynamic-static-lists.md) </span><span class="sxs-lookup"><span data-stu-id="efcf7-114">[Sample: Distribute Campaign Activities to Dynamic and Static Lists](sample-distribute-campaign-activities-dynamic-static-lists.md) </span></span>  
 <span data-ttu-id="efcf7-115">[List (Marketing List) Entity](list-marketing-list-entity.md) </span><span class="sxs-lookup"><span data-stu-id="efcf7-115">[List (Marketing List) Entity](list-marketing-list-entity.md) </span></span>  
 <span data-ttu-id="efcf7-116">[Marketing Entities (Campaign, List)](marketing-entities-campaign-list.md) </span><span class="sxs-lookup"><span data-stu-id="efcf7-116">[Marketing Entities (Campaign, List)](marketing-entities-campaign-list.md) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.AddMemberListRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.PropagateByExpressionRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.CreateActivitiesListRequest>
