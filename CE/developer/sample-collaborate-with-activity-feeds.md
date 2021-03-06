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
# <a name="sample-collaborate-with-activity-feeds"></a>Sample: Collaborate with activity feeds

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. Download the complete sample from [Sample: Work with Activity Feeds](https://code.msdn.microsoft.com/Activity-Feeds-Samples-944942ff).  
  
## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]

## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to create posts with comments and mentions and how to follow [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] records. It also demonstrates how to retrieve information for the personal and record walls.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[ActivityFeeds#WorkingWithActivityFeeds](../snippets/csharp/CRMV8/activityfeeds/cs/workingwithactivityfeeds.cs#workingwithactivityfeeds)]  
  
### <a name="see-also"></a>Xem thêm  
 [Activity Feeds Entities](activity-feeds-entities.md)   
 [Introduction to Activity Feeds](introduction-activity-feeds.md)   
 [Configure Activity Feeds](configure-activity-feeds.md)   
 <xref:Microsoft.Crm.Sdk.Messages.RetrievePersonalWallRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.RetrieveRecordWallRequest>   
 [Post Entity](entities/post.md)   
 [PostComment Entity](entities/postcomment.md)   
 [PostFollow Entity](entities/postfollow.md)
