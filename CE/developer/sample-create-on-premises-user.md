---
title: 'Sample: Create an on-premises user (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
ms.custom: ''
description: The sample shows how to create a user in an Active Directory environment using the IOrganizationService.Entity) method. A snippet showing just the key sections of the sample is shown first, followed by the Complete Sample Code.
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: d3ea30ab-e55e-4aa7-8406-3441c71903a2
caps.latest.revision: 16
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 5aa9a2eae4aee0ac65a604853c6f37e115213282
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386583"
---
# <a name="sample-create-an-on-premises-user"></a><span data-ttu-id="ec55a-104">Sample: Create an on-premises user</span><span class="sxs-lookup"><span data-stu-id="ec55a-104">Sample: Create an on-premises user</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="ec55a-105">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="ec55a-105">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="ec55a-106">Download the complete sample from [Sample: Work with Users and Roles](https://code.msdn.microsoft.com/Users-and-Roles-Samples-a4f33f3f).</span><span class="sxs-lookup"><span data-stu-id="ec55a-106">Download the complete sample from [Sample: Work with Users and Roles](https://code.msdn.microsoft.com/Users-and-Roles-Samples-a4f33f3f).</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="ec55a-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="ec55a-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]

## <a name="prerequisites"></a><span data-ttu-id="ec55a-108">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="ec55a-108">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="ec55a-109">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="ec55a-109">Demonstrates</span></span>  
 <span data-ttu-id="ec55a-110">This sample shows how to create a user in an [!INCLUDE[pn_Active_Directory](../includes/pn-active-directory.md)] environment using the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*></span><span class="sxs-lookup"><span data-stu-id="ec55a-110">This sample shows how to create a user in an [!INCLUDE[pn_Active_Directory](../includes/pn-active-directory.md)] environment using the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*></span></span> <span data-ttu-id="ec55a-111">method.</span><span class="sxs-lookup"><span data-stu-id="ec55a-111">method.</span></span> <span data-ttu-id="ec55a-112">A snippet showing just the key sections of the sample is shown first, followed by the [Complete Sample Code](sample-create-on-premises-user.md#complete_sample).</span><span class="sxs-lookup"><span data-stu-id="ec55a-112">A snippet showing just the key sections of the sample is shown first, followed by the [Complete Sample Code](sample-create-on-premises-user.md#complete_sample).</span></span>  
  
## <a name="example"></a><span data-ttu-id="ec55a-113">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="ec55a-113">Example</span></span>  
 [!code-csharp[UsersAndRoles#CreateAUser1](../snippets/csharp/CRMV8/usersandroles/cs/createauser1.cs#createauser1)]  
  
<a name="complete_sample"></a>   
### <a name="complete-sample-code"></a><span data-ttu-id="ec55a-114">Complete Sample Code</span><span class="sxs-lookup"><span data-stu-id="ec55a-114">Complete Sample Code</span></span>  
 [!code-csharp[UsersAndRoles#CreateAUser](../snippets/csharp/CRMV8/usersandroles/cs/createauser.cs#createauser)]  
  
### <a name="see-also"></a><span data-ttu-id="ec55a-115">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="ec55a-115">See also</span></span>  
 <span data-ttu-id="ec55a-116">[User and Team Entities](user-team-entities.md) </span><span class="sxs-lookup"><span data-stu-id="ec55a-116">[User and Team Entities](user-team-entities.md) </span></span>  
 <span data-ttu-id="ec55a-117">[Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md) </span><span class="sxs-lookup"><span data-stu-id="ec55a-117">[Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md) </span></span>  
 [<span data-ttu-id="ec55a-118">Sample: Disable a User</span><span class="sxs-lookup"><span data-stu-id="ec55a-118">Sample: Disable a User</span></span>](sample-disable-user.md)
