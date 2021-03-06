---
title: 'Sample: Determine whether a user has a role (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 8976b75c-197d-4d80-b9fe-d4d7a4dfc0f5
caps.latest.revision: 18
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7692065218f6698672ee5c781b5130b4991f9821
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386315"
---
# <a name="sample-determine-whether-a-user-has-a-role"></a>Sample: Determine whether a user has a role

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. Download the complete sample from [Sample: Work with Users and Roles](https://code.msdn.microsoft.com/Users-and-Roles-Samples-a4f33f3f).  
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to determine whether a user in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] has been associated with a specific role. This is performed by using a query with the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*> method. A snippet that shows the key sections of the sample is shown first, followed by the [complete sample code](sample-create-on-premises-user.md#complete_sample). Note that this sample can only be run in an on-premises environment because it creates a user. However, the section of the sample that demonstrates retrieving the roles for a user will work for all environments.  
  
 [!INCLUDE[cc_sdk_onpremises_note](../includes/cc-sdk-onpremises-note.md)]
## <a name="example"></a>Ví dụ  
 [!code-csharp[UsersAndRoles#DoesUserBelongToRole1](../snippets/csharp/CRMV8/usersandroles/cs/doesuserbelongtorole1.cs#doesuserbelongtorole1)]  
  
<a name="complete_sample"></a>   
### <a name="complete-sample-code"></a>Complete Sample Code  
 [!code-csharp[UsersAndRoles#DoesUserBelongToRole](../snippets/csharp/CRMV8/usersandroles/cs/doesuserbelongtorole.cs#doesuserbelongtorole)]  
  
### <a name="see-also"></a>Xem thêm  
 [Privilege and Role Entities](privilege-role-entities.md)   
 [Sample: Remove a Role for a User](sample-remove-role-user.md)   
 [User and Team Entities](user-team-entities.md)   
 [Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md)   
