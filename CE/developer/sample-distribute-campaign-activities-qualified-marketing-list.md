---
title: 'Sample: Distribute campaign activities to qualified marketing list (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The sample code demonstrates how to distribute campaign activities to the qualified members of a marketing list.
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
- distributing campaign activities to marketing list members, marketing entities sample
- sample for distributing campaign activities to marketing list members
ms.assetid: 204308af-df43-41d2-9382-50a01aff8f3c
caps.latest.revision: 14
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: be6b7ceadbbc81777f9dae86d8e94409d14b6181
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385906"
---
# <a name="sample-distribute-campaign-activities-to-qualified-marketing-list"></a><span data-ttu-id="c7251-103">Sample: Distribute campaign activities to qualified marketing list</span><span class="sxs-lookup"><span data-stu-id="c7251-103">Sample: Distribute campaign activities to qualified marketing list</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="c7251-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="c7251-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="c7251-105">Download the complete sample from [Sample: Work with Marketing entities](https://code.msdn.microsoft.com/Marketing-Samples-c5429380).</span><span class="sxs-lookup"><span data-stu-id="c7251-105">Download the complete sample from [Sample: Work with Marketing entities](https://code.msdn.microsoft.com/Marketing-Samples-c5429380).</span></span>   

## <a name="prerequisites"></a><span data-ttu-id="c7251-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="c7251-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="c7251-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="c7251-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="c7251-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="c7251-108">Demonstrates</span></span>  
 <span data-ttu-id="c7251-109">This sample shows how to distribute campaign activities to the qualified members of a marketing list.</span><span class="sxs-lookup"><span data-stu-id="c7251-109">This sample shows how to distribute campaign activities to the qualified members of a marketing list.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c7251-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="c7251-110">Example</span></span>  
 [!code-csharp[Marketing#DistributeCampaignFromMarketingList](../snippets/csharp/CRMV8/marketing/cs/distributecampaignfrommarketinglist.cs#distributecampaignfrommarketinglist)]  
  
### <a name="see-also"></a><span data-ttu-id="c7251-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="c7251-111">See also</span></span>  
 <span data-ttu-id="c7251-112">[Campaign Entities](campaign-entities.md) </span><span class="sxs-lookup"><span data-stu-id="c7251-112">[Campaign Entities](campaign-entities.md) </span></span>  
 <span data-ttu-id="c7251-113">[Sample: Distribute a Quick Campaign](sample-distribute-a-quick-campaign.md) </span><span class="sxs-lookup"><span data-stu-id="c7251-113">[Sample: Distribute a Quick Campaign](sample-distribute-a-quick-campaign.md) </span></span>  
 <span data-ttu-id="c7251-114">[Sample: Distribute Campaign Activities to Dynamic and Static Lists](sample-distribute-campaign-activities-dynamic-static-lists.md) </span><span class="sxs-lookup"><span data-stu-id="c7251-114">[Sample: Distribute Campaign Activities to Dynamic and Static Lists](sample-distribute-campaign-activities-dynamic-static-lists.md) </span></span>  
 <span data-ttu-id="c7251-115">[List (Marketing List) Entity](list-marketing-list-entity.md) </span><span class="sxs-lookup"><span data-stu-id="c7251-115">[List (Marketing List) Entity](list-marketing-list-entity.md) </span></span>  
 <span data-ttu-id="c7251-116">[Marketing Entities (Campaign, List)](marketing-entities-campaign-list.md) </span><span class="sxs-lookup"><span data-stu-id="c7251-116">[Marketing Entities (Campaign, List)](marketing-entities-campaign-list.md) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.AddMemberListRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.AddItemCampaignRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.AddItemCampaignActivityRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.QualifyMemberListRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.DistributeCampaignActivityRequest>
