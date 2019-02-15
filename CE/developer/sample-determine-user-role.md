---
title: 'Sample: Determine whether a user has a role (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The sample shows how to determine whether a user in Dynamics 365 for Customer Engagement has been associated with a specific role.
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
ms.openlocfilehash: b3e144bbb91e52c190a2031fd4a39027437b5e8b
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388668"
---
# <a name="sample-determine-whether-a-user-has-a-role"></a><span data-ttu-id="49971-103">Sample: Determine whether a user has a role</span><span class="sxs-lookup"><span data-stu-id="49971-103">Sample: Determine whether a user has a role</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="49971-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="49971-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="49971-105">Download the complete sample from [Work with Users and Roles](https://code.msdn.microsoft.com/Users-and-Roles-Samples-a4f33f3f).</span><span class="sxs-lookup"><span data-stu-id="49971-105">Download the complete sample from [Work with Users and Roles](https://code.msdn.microsoft.com/Users-and-Roles-Samples-a4f33f3f).</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="49971-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="49971-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="49971-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="49971-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="49971-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="49971-108">Demonstrates</span></span>  
 <span data-ttu-id="49971-109">This sample shows how to determine whether a user in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] has been associated with a specific role.</span><span class="sxs-lookup"><span data-stu-id="49971-109">This sample shows how to determine whether a user in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] has been associated with a specific role.</span></span> <span data-ttu-id="49971-110">This is performed by using a query with the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*></span><span class="sxs-lookup"><span data-stu-id="49971-110">This is performed by using a query with the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*></span></span> <span data-ttu-id="49971-111">method.</span><span class="sxs-lookup"><span data-stu-id="49971-111">method.</span></span> <span data-ttu-id="49971-112">A snippet that shows the key sections of the sample is shown first, followed by the [complete sample code](sample-create-on-premises-user.md#complete_sample).</span><span class="sxs-lookup"><span data-stu-id="49971-112">A snippet that shows the key sections of the sample is shown first, followed by the [complete sample code](sample-create-on-premises-user.md#complete_sample).</span></span> <span data-ttu-id="49971-113">Note that this sample can only be run in an on-premises environment because it creates a user.</span><span class="sxs-lookup"><span data-stu-id="49971-113">Note that this sample can only be run in an on-premises environment because it creates a user.</span></span> <span data-ttu-id="49971-114">However, the section of the sample that demonstrates retrieving the roles for a user will work for all environments.</span><span class="sxs-lookup"><span data-stu-id="49971-114">However, the section of the sample that demonstrates retrieving the roles for a user will work for all environments.</span></span>  

[!INCLUDE[cc_sdk_onpremises_note](../includes/cc-sdk-onpremises-note.md)]

## <a name="example"></a><span data-ttu-id="49971-115">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="49971-115">Example</span></span>  
 [!code-csharp[UsersAndRoles#DoesUserBelongToRole1](../snippets/csharp/CRMV8/usersandroles/cs/doesuserbelongtorole1.cs#doesuserbelongtorole1)]  
  
<a name="complete_sample"></a>   
### <a name="complete-sample-code"></a><span data-ttu-id="49971-116">Complete Sample Code</span><span class="sxs-lookup"><span data-stu-id="49971-116">Complete Sample Code</span></span>  
 [!code-csharp[UsersAndRoles#DoesUserBelongToRole](../snippets/csharp/CRMV8/usersandroles/cs/doesuserbelongtorole.cs#doesuserbelongtorole)]  
  
### <a name="see-also"></a><span data-ttu-id="49971-117">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="49971-117">See also</span></span>  
 <span data-ttu-id="49971-118">[Privilege and Role Entities](privilege-role-entities.md) </span><span class="sxs-lookup"><span data-stu-id="49971-118">[Privilege and Role Entities](privilege-role-entities.md) </span></span>  
 <span data-ttu-id="49971-119">[Sample: Remove a Role for a User](sample-remove-role-user.md) </span><span class="sxs-lookup"><span data-stu-id="49971-119">[Sample: Remove a Role for a User](sample-remove-role-user.md) </span></span>  
 <span data-ttu-id="49971-120">[User and Team Entities](user-team-entities.md) </span><span class="sxs-lookup"><span data-stu-id="49971-120">[User and Team Entities](user-team-entities.md) </span></span>  
 [<span data-ttu-id="49971-121">Sample: CrmServiceHelper Class</span><span class="sxs-lookup"><span data-stu-id="49971-121">Sample: CrmServiceHelper Class</span></span>](org-service/helper-code-serverconnection-class.md)   
