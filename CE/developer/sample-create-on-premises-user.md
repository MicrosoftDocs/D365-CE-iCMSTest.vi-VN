---
title: 'Sample: Create an on-premises user (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
ms.custom: ''
description: The sample shows how to create a user in an Active Directory environment using the IOrganizationService.Entity) method. A snippet showing just the key sections of the sample is shown first, followed by the Complete Sample Code.
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: d3ea30ab-e55e-4aa7-8406-3441c71903a2
caps.latest.revision: 16
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 5aa9a2eae4aee0ac65a604853c6f37e115213282
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386583"
---
# <a name="sample-create-an-on-premises-user"></a>Sample: Create an on-premises user

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. Download the complete sample from [Sample: Work with Users and Roles](https://code.msdn.microsoft.com/Users-and-Roles-Samples-a4f33f3f). 
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to create a user in an [!INCLUDE[pn_Active_Directory](../includes/pn-active-directory.md)] environment using the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*> method. A snippet showing just the key sections of the sample is shown first, followed by the [Complete Sample Code](sample-create-on-premises-user.md#complete_sample).  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[UsersAndRoles#CreateAUser1](../snippets/csharp/CRMV8/usersandroles/cs/createauser1.cs#createauser1)]  
  
<a name="complete_sample"></a>   
### <a name="complete-sample-code"></a>Complete Sample Code  
 [!code-csharp[UsersAndRoles#CreateAUser](../snippets/csharp/CRMV8/usersandroles/cs/createauser.cs#createauser)]  
  
### <a name="see-also"></a>Xem thêm  
 [User and Team Entities](user-team-entities.md)   
 [Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md)   
 [Sample: Disable a User](sample-disable-user.md)
