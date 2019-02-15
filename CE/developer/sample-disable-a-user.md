---
title: 'Sample: Disable a user (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 082fc88f-a951-41c2-85ae-4b5e69e9917c
caps.latest.revision: 15
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: d136578a447c502af2a329d2ae4c5b50a459c2ff
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387339"
---
# <a name="sample-disable-a-user"></a>Sample: Disable a user

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. Download the complete sample from [Sample: Work with Users and Roles](https://code.msdn.microsoft.com/Users-and-Roles-Samples-a4f33f3f).   
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to create a user in an [!INCLUDE[pn_Active_Directory](../includes/pn-active-directory.md)] environment using the <xref:Microsoft.Crm.Sdk.Messages.SetStateRequest> message. A snippet showing just the key sections of the sample is shown first, followed by the [complete sample code](sample-create-on-premises-user.md#complete_sample). Note that this sample can only be run in an on-premises environment because it creates a user. However, the portion of the sample that demonstrates disabling the user will work for all environments.  
  
 [!INCLUDE[cc_sdk_onpremises_note](../includes/cc-sdk-onpremises-note.md)] 
 
## <a name="example"></a>Ví dụ  
 [!code-csharp[UsersAndRoles#DisableOrEnableUser1](../snippets/csharp/CRMV8/usersandroles/cs/disableorenableuser1.cs#disableorenableuser1)]  
  
<a name="complete_sample"></a>   
### <a name="complete-sample-code"></a>Complete sample code  
 [!code-csharp[UsersAndRoles#DisableOrEnableUser](../snippets/csharp/CRMV8/usersandroles/cs/disableorenableuser.cs#disableorenableuser)]  
  
### <a name="see-also"></a>Xem thêm  
 [User and Team Entities](user-team-entities.md)   
 <xref:Microsoft.Crm.Sdk.Messages.SetStateRequest>   
 [Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md)   
