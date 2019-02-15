---
title: 'Sample: Share records using GrantAccess, ModifyAccess and RevokeAccess messages (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: The sample shows how to share a record using the following messages:GrantAccessRequest, ModifyAccessRequest, and RevokeAccessRequest.
keywords: ''
ms.date: 12/15/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 791aa59d-b217-4e8d-93d3-edd4ecfc8403
author: KumarVivek
ms.author: kvivek
manager: jdaly
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
helpviewer_keywords:
- sharing records sample
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 2e119c4028a1215e290bad296cc5aad334f6ddb0
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387560"
---
# <a name="sample-share-records-using-grantaccess-modifyaccess-and-revokeaccess-messages"></a>Sample: Share records using GrantAccess, ModifyAccess and RevokeAccess messages

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. Download the Sample: [Work with early bound entity classes in code](https://code.msdn.microsoft.com/Work-with-early-bound-6914f6e7).

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to share a record using the following messages:  
  
-   <xref:Microsoft.Crm.Sdk.Messages.GrantAccessRequest>  
  
-   <xref:Microsoft.Crm.Sdk.Messages.ModifyAccessRequest>  
  
-   <xref:Microsoft.Crm.Sdk.Messages.RevokeAccessRequest>  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[strongtypes#UserAccess](../snippets/csharp/CRMV8/strongtypes/cs/useraccess.cs#useraccess)]  
  
### <a name="see-also"></a>Xem thêm  
 [User and Team Entities](user-team-entities.md)   
 [Introduction to Entities in Dynamics 365 for Customer Engagement apps](introduction-entities.md#Share)   
 <xref:Microsoft.Crm.Sdk.Messages.GrantAccessRequest>   
 [Sample: Create an On-Premises User](sample-create-on-premises-user.md)   
 [Introduction to Entities in Dynamics 365 for Customer Engagement apps](introduction-entities.md)
