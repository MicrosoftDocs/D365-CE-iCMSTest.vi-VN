---
title: 'Sample: Remove a role for a user (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
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
ms.openlocfilehash: 0644981a4ab86f739de01b52ac757c9294ee141f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386260"
---
# <a name="sample-remove-a-role-for-a-user"></a><span data-ttu-id="9cc00-102">Sample: Remove a role for a user</span><span class="sxs-lookup"><span data-stu-id="9cc00-102">Sample: Remove a role for a user</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="9cc00-103">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="9cc00-103">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="9cc00-104">Download the complete sample from [Sample: Work with Users and Roles](https://code.msdn.microsoft.com/Users-and-Roles-Samples-a4f33f3f).</span><span class="sxs-lookup"><span data-stu-id="9cc00-104">Download the complete sample from [Sample: Work with Users and Roles](https://code.msdn.microsoft.com/Users-and-Roles-Samples-a4f33f3f).</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="9cc00-105">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="9cc00-105">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="9cc00-106">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="9cc00-106">Demonstrates</span></span>  
 <span data-ttu-id="9cc00-107">This sample shows how to disassociate a role from a user by using the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Disassociate*></span><span class="sxs-lookup"><span data-stu-id="9cc00-107">This sample shows how to disassociate a role from a user by using the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Disassociate*></span></span> <span data-ttu-id="9cc00-108">method.</span><span class="sxs-lookup"><span data-stu-id="9cc00-108">method.</span></span> <span data-ttu-id="9cc00-109">A snippet showing just the key sections of the sample is shown first, followed by the [complete sample code](sample-create-on-premises-user.md#complete_sample).</span><span class="sxs-lookup"><span data-stu-id="9cc00-109">A snippet showing just the key sections of the sample is shown first, followed by the [complete sample code](sample-create-on-premises-user.md#complete_sample).</span></span> <span data-ttu-id="9cc00-110">Note that this sample can only be run in an on-premises environment because it creates a user.</span><span class="sxs-lookup"><span data-stu-id="9cc00-110">Note that this sample can only be run in an on-premises environment because it creates a user.</span></span> <span data-ttu-id="9cc00-111">However, the section of the sample that demonstrates disassociating a role from a user will work for all environments.</span><span class="sxs-lookup"><span data-stu-id="9cc00-111">However, the section of the sample that demonstrates disassociating a role from a user will work for all environments.</span></span>  
  
 [!INCLUDE[cc_sdk_onpremises_note](../includes/cc-sdk-onpremises-note.md)] 
 
## <a name="example"></a><span data-ttu-id="9cc00-112">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="9cc00-112">Example</span></span>  
 [!code-csharp[UsersAndRoles#RemoveRoleFromUser1](../snippets/csharp/CRMV8/usersandroles/cs/removerolefromuser1.cs#removerolefromuser1)]  
  
<a name="complete_sample"></a>   
### <a name="complete-sample-code"></a><span data-ttu-id="9cc00-113">Complete sample code</span><span class="sxs-lookup"><span data-stu-id="9cc00-113">Complete sample code</span></span>  
 [!code-csharp[UsersAndRoles#RemoveRoleFromUser](../snippets/csharp/CRMV8/usersandroles/cs/removerolefromuser.cs#removerolefromuser)]  
  
### <a name="see-also"></a><span data-ttu-id="9cc00-114">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="9cc00-114">See also</span></span>  
 <span data-ttu-id="9cc00-115">[Privilege and Role Entities](privilege-role-entities.md) </span><span class="sxs-lookup"><span data-stu-id="9cc00-115">[Privilege and Role Entities](privilege-role-entities.md) </span></span>  
 <span data-ttu-id="9cc00-116">[Sample: Retrieve the Roles for an Organization](sample-retrieve-roles-organization.md) </span><span class="sxs-lookup"><span data-stu-id="9cc00-116">[Sample: Retrieve the Roles for an Organization](sample-retrieve-roles-organization.md) </span></span>  
 <span data-ttu-id="9cc00-117">[User and Team Entities](user-team-entities.md) </span><span class="sxs-lookup"><span data-stu-id="9cc00-117">[User and Team Entities](user-team-entities.md) </span></span>  
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 [<span data-ttu-id="9cc00-118">Sample: CrmServiceHelper Class</span><span class="sxs-lookup"><span data-stu-id="9cc00-118">Sample: CrmServiceHelper Class</span></span>](org-service/helper-code-serverconnection-class.md)   
 