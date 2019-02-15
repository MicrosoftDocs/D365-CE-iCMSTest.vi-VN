---
title: 'Sample: Associate a Security Role to a User (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The sample shows how to associate a role with a user by using the IOrganizationService.EntityReferenceCollection) method.
keywords: ''
ms.date: 10/31/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: c962101c-65f0-4e49-8c23-99c2a9e7dcbf
author: JimDaly
ms.author: jdaly
manager: jdaly
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
caps.latest.revision: 17
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4d275497f43b0d24228d6111a5f897bf7daaaeea
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385922"
---
# <a name="sample-associate-a-security-role-to-a-user"></a><span data-ttu-id="03aee-103">Sample: Associate a Security Role to a User</span><span class="sxs-lookup"><span data-stu-id="03aee-103">Sample: Associate a Security Role to a User</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="03aee-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="03aee-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span>

## <a name="prerequisites"></a><span data-ttu-id="03aee-105">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="03aee-105">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="03aee-106">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="03aee-106">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="03aee-107">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="03aee-107">Demonstrates</span></span>  
 <span data-ttu-id="03aee-108">This sample shows how to associate a role with a user by using the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Associate*></span><span class="sxs-lookup"><span data-stu-id="03aee-108">This sample shows how to associate a role with a user by using the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Associate*></span></span> <span data-ttu-id="03aee-109">method.</span><span class="sxs-lookup"><span data-stu-id="03aee-109">method.</span></span> <span data-ttu-id="03aee-110">A snippet showing just the key portions of the sample is shown first, followed by the [Complete Sample Code](sample-create-on-premises-user.md#complete_sample).</span><span class="sxs-lookup"><span data-stu-id="03aee-110">A snippet showing just the key portions of the sample is shown first, followed by the [Complete Sample Code](sample-create-on-premises-user.md#complete_sample).</span></span> <span data-ttu-id="03aee-111">Note that this sample can only be run in an on-premises environment because it creates a user.</span><span class="sxs-lookup"><span data-stu-id="03aee-111">Note that this sample can only be run in an on-premises environment because it creates a user.</span></span> <span data-ttu-id="03aee-112">However, the section of the sample that demonstrates associating a role with a user will work for all environments.</span><span class="sxs-lookup"><span data-stu-id="03aee-112">However, the section of the sample that demonstrates associating a role with a user will work for all environments.</span></span>  
  
[!INCLUDE[cc_sdk_onpremises_note](../includes/cc-sdk-onpremises-note.md)] 
## <a name="example"></a><span data-ttu-id="03aee-113">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="03aee-113">Example</span></span>  
 [!code-csharp[UsersAndRoles#AddRoleToUser1](../snippets/csharp/CRMV8/usersandroles/cs/addroletouser1.cs#addroletouser1)]  
  
<a name="complete_sample"></a>   
### <a name="complete-sample-code"></a><span data-ttu-id="03aee-114">Complete Sample Code</span><span class="sxs-lookup"><span data-stu-id="03aee-114">Complete Sample Code</span></span>  
 [!code-csharp[UsersAndRoles#AddRoleToUser](../snippets/csharp/CRMV8/usersandroles/cs/addroletouser.cs#addroletouser)]  
  
### <a name="see-also"></a><span data-ttu-id="03aee-115">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="03aee-115">See also</span></span>  
 <span data-ttu-id="03aee-116">[Privilege and Role Entities](privilege-role-entities.md) </span><span class="sxs-lookup"><span data-stu-id="03aee-116">[Privilege and Role Entities](privilege-role-entities.md) </span></span>  
 <span data-ttu-id="03aee-117">[Sample: Determine Whether a User has a Role](sample-determine-user-role.md) </span><span class="sxs-lookup"><span data-stu-id="03aee-117">[Sample: Determine Whether a User has a Role](sample-determine-user-role.md) </span></span>  
 <span data-ttu-id="03aee-118">[User and Team Entities](user-team-entities.md) </span><span class="sxs-lookup"><span data-stu-id="03aee-118">[User and Team Entities](user-team-entities.md) </span></span>  
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 [<span data-ttu-id="03aee-119">Sample: CrmServiceHelper Class</span><span class="sxs-lookup"><span data-stu-id="03aee-119">Sample: CrmServiceHelper Class</span></span>](org-service/helper-code-serverconnection-class.md)  
