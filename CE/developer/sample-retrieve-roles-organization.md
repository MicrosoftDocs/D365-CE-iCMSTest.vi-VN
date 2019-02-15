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
# <a name="sample-retrieve-the-roles-for-an-organization"></a><span data-ttu-id="1f2ea-103">Sample: Retrieve the roles for an organization</span><span class="sxs-lookup"><span data-stu-id="1f2ea-103">Sample: Retrieve the roles for an organization</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="1f2ea-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="1f2ea-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="1f2ea-105">Download the complete sample from [Sample: Work with Users and Roles](https://code.msdn.microsoft.com/Users-and-Roles-Samples-a4f33f3f).</span><span class="sxs-lookup"><span data-stu-id="1f2ea-105">Download the complete sample from [Sample: Work with Users and Roles](https://code.msdn.microsoft.com/Users-and-Roles-Samples-a4f33f3f).</span></span>   

## <a name="prerequisites"></a><span data-ttu-id="1f2ea-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="1f2ea-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="1f2ea-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="1f2ea-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="1f2ea-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="1f2ea-108">Demonstrates</span></span>  
 <span data-ttu-id="1f2ea-109">This sample shows how to retrieve the roles for an organization by using the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*></span><span class="sxs-lookup"><span data-stu-id="1f2ea-109">This sample shows how to retrieve the roles for an organization by using the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*></span></span> <span data-ttu-id="1f2ea-110">method.</span><span class="sxs-lookup"><span data-stu-id="1f2ea-110">method.</span></span> <span data-ttu-id="1f2ea-111">A snippet that shows just the key sections of the sample is shown first, followed by the [complete sample code](sample-create-on-premises-user.md#complete_sample).</span><span class="sxs-lookup"><span data-stu-id="1f2ea-111">A snippet that shows just the key sections of the sample is shown first, followed by the [complete sample code](sample-create-on-premises-user.md#complete_sample).</span></span>  
  
## <a name="example"></a><span data-ttu-id="1f2ea-112">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="1f2ea-112">Example</span></span>  
 [!code-csharp[UsersAndRoles#RetrieveRolesForOrg1](../snippets/csharp/CRMV8/usersandroles/cs/retrieverolesfororg1.cs#retrieverolesfororg1)]  
  
<a name="complete_sample"></a>   
### <a name="complete-sample-code"></a><span data-ttu-id="1f2ea-113">Complete sample code</span><span class="sxs-lookup"><span data-stu-id="1f2ea-113">Complete sample code</span></span>  
 [!code-csharp[UsersAndRoles#RetrieveRolesForOrg](../snippets/csharp/CRMV8/usersandroles/cs/retrieverolesfororg.cs#retrieverolesfororg)]  
  
### <a name="see-also"></a><span data-ttu-id="1f2ea-114">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="1f2ea-114">See also</span></span>  
 <span data-ttu-id="1f2ea-115">[Privilege and Role Entities](privilege-role-entities.md) </span><span class="sxs-lookup"><span data-stu-id="1f2ea-115">[Privilege and Role Entities](privilege-role-entities.md) </span></span>  
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 [<span data-ttu-id="1f2ea-116">Sample: CrmServiceHelper Class</span><span class="sxs-lookup"><span data-stu-id="1f2ea-116">Sample: CrmServiceHelper Class</span></span>](org-service/helper-code-serverconnection-class.md)
