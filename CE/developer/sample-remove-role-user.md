---
title: 'Sample: Remove a role for a user (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The sample shows how to disassociate a role from a user by using the IOrganizationService.EntityReferenceCollection) method.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 6f25132e-30d2-4a20-9395-3e42aafdd959
caps.latest.revision: 16
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 0c9ef2affc5dbef33e470fd4bedb7702df9b215f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388680"
---
# <a name="sample-remove-a-role-for-a-user"></a>Sample: Remove a role for a user

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. Download the complete sample from [Sample: Work with Users and Roles](https://code.msdn.microsoft.com/Users-and-Roles-Samples-a4f33f3f).  

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to disassociate a role from a user by using the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Disassociate*> method. A snippet showing just the key sections of the sample is shown first, followed by the [complete sample code](sample-create-on-premises-user.md#complete_sample). Note that this sample can only be run in an on-premises environment because it creates a user. However, the section of the sample that demonstrates disassociating a role from a user will work for all environments.  
  
[!INCLUDE[cc_sdk_onpremises_note](../includes/cc-sdk-onpremises-note.md)]

## <a name="example"></a>Ví dụ  
 [!code-csharp[UsersAndRoles#RemoveRoleFromUser1](../snippets/csharp/CRMV8/usersandroles/cs/removerolefromuser1.cs#removerolefromuser1)]  
  
<a name="complete_sample"></a>   
### <a name="complete-sample-code"></a>Complete sample code  
 [!code-csharp[UsersAndRoles#RemoveRoleFromUser](../snippets/csharp/CRMV8/usersandroles/cs/removerolefromuser.cs#removerolefromuser)]  
  
### <a name="see-also"></a>Xem thêm  
 [Privilege and Role Entities](privilege-role-entities.md)   
 [Sample: Retrieve the Roles for an Organization](sample-retrieve-roles-organization.md)   
 [User and Team Entities](user-team-entities.md)   
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 [Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md)   
 
