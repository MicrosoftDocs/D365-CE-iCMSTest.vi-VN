---
title: 'Sample: Share a record using an access team (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: The sample shows how to allow access to a record using an access team. All members of the team receive the same access to the record as is granted to the team.
keywords: ''
ms.date: 12/15/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 9b841889-c396-4f6e-8588-e702e94c7073
author: KumarVivek
ms.author: kvivek
manager: jdaly
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
caps.latest.revision: 9
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 9857a30f9d4f4a7e08a08443faa527ab7de74dd9
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388529"
---
# <a name="sample-share-a-record-using-an-access-team"></a>Sample: Share a record using an access team

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. Download the Sample: [Work with early bound entity classes in code](https://code.msdn.microsoft.com/Work-with-early-bound-6914f6e7).  

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to allow access to a record using an access team. All members of the team receive the same access to the record as is granted to the team.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[strongtypes#CreateAndShareAccessTeam](../snippets/csharp/CRMV8/strongtypes/cs/createandshareaccessteam.cs#createandshareaccessteam)]  
  
### <a name="see-also"></a>Xem thêm  
 [User and Team Entities](user-team-entities.md)   
 [Introduction to Entities in Dynamics 365 for Customer Engagement apps](introduction-entities.md#Share)   
 <xref:Microsoft.Crm.Sdk.Messages.GrantAccessRequest>   
 [Sample: Share Records Using GrantAccess, ModifyAccess and RevokeAccess Messages](sample-share-records-using-grantaccess-modifyaccess-revokeaccess-messages.md)
