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
# <a name="sample-impersonate-using-the-actonbehalfof-privilege"></a><span data-ttu-id="e8ba4-103">Sample: Impersonate using the ActOnBehalfOf privilege</span><span class="sxs-lookup"><span data-stu-id="e8ba4-103">Sample: Impersonate using the ActOnBehalfOf privilege</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="e8ba4-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="e8ba4-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span></span>
<span data-ttu-id="e8ba4-105">Download the sample: [Work with authentication (Impersonating a user)](https://code.msdn.microsoft.com/Sample-of-impersonating-e51b6cbd).</span><span class="sxs-lookup"><span data-stu-id="e8ba4-105">Download the sample: [Work with authentication (Impersonating a user)](https://code.msdn.microsoft.com/Sample-of-impersonating-e51b6cbd).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e8ba4-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="e8ba4-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="e8ba4-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="e8ba4-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
 <span data-ttu-id="e8ba4-108">The user (impersonator) must have the ActOnBehalfOf privilege or be a member of the PrivUserGroup group in [!INCLUDE[pn_Active_Directory](../../includes/pn-active-directory.md)].</span><span class="sxs-lookup"><span data-stu-id="e8ba4-108">The user (impersonator) must have the ActOnBehalfOf privilege or be a member of the PrivUserGroup group in [!INCLUDE[pn_Active_Directory](../../includes/pn-active-directory.md)].</span></span>  
  
## <a name="demonstrates"></a><span data-ttu-id="e8ba4-109">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="e8ba4-109">Demonstrates</span></span>  
 <span data-ttu-id="e8ba4-110">This sample shows how to impersonate another user by setting the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy.CallerId> property of the organization web service proxy.</span><span class="sxs-lookup"><span data-stu-id="e8ba4-110">This sample shows how to impersonate another user by setting the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy.CallerId> property of the organization web service proxy.</span></span>  
  
## <a name="examples"></a><span data-ttu-id="e8ba4-111">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="e8ba4-111">Examples</span></span>  
 <span data-ttu-id="e8ba4-112">Code snippets that highlight the important code are shown first, followed by the [complete example](sample-impersonate-actonbehalfof-privilege.md#bkmk_complete) code.</span><span class="sxs-lookup"><span data-stu-id="e8ba4-112">Code snippets that highlight the important code are shown first, followed by the [complete example](sample-impersonate-actonbehalfof-privilege.md#bkmk_complete) code.</span></span>  
  
### <a name="code-snippet"></a><span data-ttu-id="e8ba4-113">Code snippet</span><span class="sxs-lookup"><span data-stu-id="e8ba4-113">Code snippet</span></span>  
 [!code-csharp[Authentication#ImpersonateWithOnBehalfOfPrivilege2](../../snippets/csharp/CRMV8/authentication/cs/impersonatewithonbehalfofprivilege2.cs#impersonatewithonbehalfofprivilege2)]  
  
<a name="bkmk_complete"></a>   
### <a name="complete-example"></a><span data-ttu-id="e8ba4-114">Complete example</span><span class="sxs-lookup"><span data-stu-id="e8ba4-114">Complete example</span></span>  
 [!code-csharp[Authentication#ImpersonateWithOnBehalfOfPrivilege](../../snippets/csharp/CRMV8/authentication/cs/impersonatewithonbehalfofprivilege.cs#impersonatewithonbehalfofprivilege)]  
  
### <a name="see-also"></a><span data-ttu-id="e8ba4-115">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="e8ba4-115">See also</span></span>  
 <span data-ttu-id="e8ba4-116">[Authenticate users in Dynamics 365 for Customer Engagement apps](../authenticate-users.md) </span><span class="sxs-lookup"><span data-stu-id="e8ba4-116">[Authenticate users in Dynamics 365 for Customer Engagement apps](../authenticate-users.md) </span></span>  
 <span data-ttu-id="e8ba4-117">[Sample: Authenticate users with Dynamics 365 for Customer Engagement web services](../sample-authenticate-users-web-services.md) </span><span class="sxs-lookup"><span data-stu-id="e8ba4-117">[Sample: Authenticate users with Dynamics 365 for Customer Engagement web services](../sample-authenticate-users-web-services.md) </span></span>  
 <span data-ttu-id="e8ba4-118">[Impersonate Another User](impersonate-another-user.md) </span><span class="sxs-lookup"><span data-stu-id="e8ba4-118">[Impersonate Another User](impersonate-another-user.md) </span></span>  
 <span data-ttu-id="e8ba4-119">[How role-based security can be used to control access to entities](../security-dev/how-role-based-security-control-access-entities.md) </span><span class="sxs-lookup"><span data-stu-id="e8ba4-119">[How role-based security can be used to control access to entities](../security-dev/how-role-based-security-control-access-entities.md) </span></span>  
 <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy.CallerId>
