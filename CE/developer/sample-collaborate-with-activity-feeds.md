---
title: 'Sample: Collaborate with activity feeds (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The sample shows how to create posts with comments and mentions and how to follow Dynamics 365 for Customer Engagement records. It also demonstrates how to retrieve information for the personal and record walls.
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
- collaborating with activity feeds sample, requirements
- personal wall sample, retrieving information from
- records sample, following
- posts with comments sample, creating
- updating posts, sample
- multiple pages of posts, retrieving information from
- activity feeds sample, downloading MicrosoftCRMActivityFeeds.zip.cab
- following records, sample
- activity feeds sample, collaborating
- MicrosoftCRMActivityFeeds.zip.cab, downloading
ms.assetid: d680463c-09d4-4cd8-bdbe-2ca4309c12a3
caps.latest.revision: 24
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 26a81846241199a686916ac28cd4a5ca02be23e5
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387121"
---
# <a name="sample-collaborate-with-activity-feeds"></a><span data-ttu-id="d0cb1-104">Sample: Collaborate with activity feeds</span><span class="sxs-lookup"><span data-stu-id="d0cb1-104">Sample: Collaborate with activity feeds</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="d0cb1-105">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="d0cb1-105">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="d0cb1-106">Download the complete sample from [Sample: Work with Activity Feeds](https://code.msdn.microsoft.com/Activity-Feeds-Samples-944942ff).</span><span class="sxs-lookup"><span data-stu-id="d0cb1-106">Download the complete sample from [Sample: Work with Activity Feeds](https://code.msdn.microsoft.com/Activity-Feeds-Samples-944942ff).</span></span>  
  
## <a name="prerequisites"></a><span data-ttu-id="d0cb1-107">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="d0cb1-107">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]

## <a name="requirements"></a><span data-ttu-id="d0cb1-108">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="d0cb1-108">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="d0cb1-109">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="d0cb1-109">Demonstrates</span></span>  
 <span data-ttu-id="d0cb1-110">This sample shows how to create posts with comments and mentions and how to follow [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] records.</span><span class="sxs-lookup"><span data-stu-id="d0cb1-110">This sample shows how to create posts with comments and mentions and how to follow [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] records.</span></span> <span data-ttu-id="d0cb1-111">It also demonstrates how to retrieve information for the personal and record walls.</span><span class="sxs-lookup"><span data-stu-id="d0cb1-111">It also demonstrates how to retrieve information for the personal and record walls.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d0cb1-112">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="d0cb1-112">Example</span></span>  
 [!code-csharp[ActivityFeeds#WorkingWithActivityFeeds](../snippets/csharp/CRMV8/activityfeeds/cs/workingwithactivityfeeds.cs#workingwithactivityfeeds)]  
  
### <a name="see-also"></a><span data-ttu-id="d0cb1-113">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="d0cb1-113">See also</span></span>  
 <span data-ttu-id="d0cb1-114">[Activity Feeds Entities](activity-feeds-entities.md) </span><span class="sxs-lookup"><span data-stu-id="d0cb1-114">[Activity Feeds Entities](activity-feeds-entities.md) </span></span>  
 <span data-ttu-id="d0cb1-115">[Introduction to Activity Feeds](introduction-activity-feeds.md) </span><span class="sxs-lookup"><span data-stu-id="d0cb1-115">[Introduction to Activity Feeds](introduction-activity-feeds.md) </span></span>  
 <span data-ttu-id="d0cb1-116">[Configure Activity Feeds](configure-activity-feeds.md) </span><span class="sxs-lookup"><span data-stu-id="d0cb1-116">[Configure Activity Feeds](configure-activity-feeds.md) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.RetrievePersonalWallRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.RetrieveRecordWallRequest>   
 <span data-ttu-id="d0cb1-117">[Post Entity](entities/post.md) </span><span class="sxs-lookup"><span data-stu-id="d0cb1-117">[Post Entity](entities/post.md) </span></span>  
 <span data-ttu-id="d0cb1-118">[PostComment Entity](entities/postcomment.md) </span><span class="sxs-lookup"><span data-stu-id="d0cb1-118">[PostComment Entity](entities/postcomment.md) </span></span>  
 [<span data-ttu-id="d0cb1-119">PostFollow Entity</span><span class="sxs-lookup"><span data-stu-id="d0cb1-119">PostFollow Entity</span></span>](entities/postfollow.md)
