---
title: 'Sample: Retrieve the roles for an organization (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The sample shows how to retrieve the roles for an organization by using the IOrganizationService.QueryBase) method.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 8b0e6460-46cb-436b-b689-91f11085b8c7
caps.latest.revision: 13
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 8c4b747456dac4baae28ae90ea62e3769bcf054f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387000"
---
# <a name="sample-retrieve-the-roles-for-an-organization"></a>Sample: Retrieve the roles for an organization

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. Download the complete sample from [Sample: Work with Users and Roles](https://code.msdn.microsoft.com/Users-and-Roles-Samples-a4f33f3f).   

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to retrieve the roles for an organization by using the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*> method. A snippet that shows just the key sections of the sample is shown first, followed by the [complete sample code](sample-create-on-premises-user.md#complete_sample).  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[UsersAndRoles#RetrieveRolesForOrg1](../snippets/csharp/CRMV8/usersandroles/cs/retrieverolesfororg1.cs#retrieverolesfororg1)]  
  
<a name="complete_sample"></a>   
### <a name="complete-sample-code"></a>Complete sample code  
 [!code-csharp[UsersAndRoles#RetrieveRolesForOrg](../snippets/csharp/CRMV8/usersandroles/cs/retrieverolesfororg.cs#retrieverolesfororg)]  
  
### <a name="see-also"></a>Xem thêm  
 [Privilege and Role Entities](privilege-role-entities.md)   
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 [Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md)
