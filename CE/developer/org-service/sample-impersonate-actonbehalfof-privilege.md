---
title: 'Sample: Impersonate using the ActOnBehalfOf privilege (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: This sample shows how to impersonate another user by setting the CallerId property of the organization web service proxy
keywords: ''
ms.date: 10/31/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: c484a6b6-e3ca-4eae-a734-68e8d38db501
author: JimDaly
ms.author: jdaly
manager: jdaly
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 23a4a797627f87320ca3304e2620acc90765c455
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388544"
---
# <a name="sample-impersonate-using-the-actonbehalfof-privilege"></a>Sample: Impersonate using the ActOnBehalfOf privilege

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.
Download the sample: [Work with authentication (Impersonating a user)](https://code.msdn.microsoft.com/Sample-of-impersonating-e51b6cbd).

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
 The user (impersonator) must have the ActOnBehalfOf privilege or be a member of the PrivUserGroup group in [!INCLUDE[pn_Active_Directory](../../includes/pn-active-directory.md)].  
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to impersonate another user by setting the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy.CallerId> property of the organization web service proxy.  
  
## <a name="examples"></a>Ví dụ  
 Code snippets that highlight the important code are shown first, followed by the [complete example](sample-impersonate-actonbehalfof-privilege.md#bkmk_complete) code.  
  
### <a name="code-snippet"></a>Code snippet  
 [!code-csharp[Authentication#ImpersonateWithOnBehalfOfPrivilege2](../../snippets/csharp/CRMV8/authentication/cs/impersonatewithonbehalfofprivilege2.cs#impersonatewithonbehalfofprivilege2)]  
  
<a name="bkmk_complete"></a>   
### <a name="complete-example"></a>Complete example  
 [!code-csharp[Authentication#ImpersonateWithOnBehalfOfPrivilege](../../snippets/csharp/CRMV8/authentication/cs/impersonatewithonbehalfofprivilege.cs#impersonatewithonbehalfofprivilege)]  
  
### <a name="see-also"></a>Xem thêm  
 [Authenticate users in Dynamics 365 for Customer Engagement apps](../authenticate-users.md)   
 [Sample: Authenticate users with Dynamics 365 for Customer Engagement web services](../sample-authenticate-users-web-services.md)   
 [Impersonate Another User](impersonate-another-user.md)   
 [How role-based security can be used to control access to entities](../security-dev/how-role-based-security-control-access-entities.md)   
 <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy.CallerId>
