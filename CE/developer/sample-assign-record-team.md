---
title: 'Sample: Assign a record to a team (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: 'The sample shows how to assign a record to a team by using the AssignRequest message. '
keywords: ''
ms.date: 12/15/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 0537eac1-c997-4091-970f-e726109b1247
author: KumarVivek
ms.author: kvivek
manager: jdaly
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
helpviewer_keywords:
- assigning records sample, team entity
- users and teams, assigning records sample
- assigning records sample, system user entity
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 370bcb8dbfd4df28d73a1611cdda31d65d99e492
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386158"
---
# <a name="sample-assign-a-record-to-a-team"></a>Sample: Assign a record to a team

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. Download the Sample: [Work with early bound entity classes in code](https://code.msdn.microsoft.com/Work-with-early-bound-6914f6e7).

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to assign a record to a team by using the <xref:Microsoft.Crm.Sdk.Messages.AssignRequest> message.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[strongtypes#AssignRecordToTeam](../snippets/csharp/CRMV8/strongtypes/cs/assignrecordtoteam.cs#assignrecordtoteam)]  
  
### <a name="see-also"></a>Xem thêm  
 <xref:Microsoft.Crm.Sdk.Messages.AssignRequest>   
 [Entity Ownership](introduction-entities.md#EntityOwnership)   
 [Gán](introduction-entities.md#Assign)   
 [User and Team Entities](user-team-entities.md)   
 [Introduction to Entities in Dynamics 365 for Customer Engagement apps](introduction-entities.md)   
 [Sample: Share Records Using GrantAccess, ModifyAccess and RevokeAccess Messages](sample-share-records-using-grantaccess-modifyaccess-revokeaccess-messages.md)
