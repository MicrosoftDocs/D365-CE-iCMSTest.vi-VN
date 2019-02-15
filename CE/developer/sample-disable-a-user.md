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
# <a name="sample-disable-a-user"></a><span data-ttu-id="a0d34-102">Sample: Disable a user</span><span class="sxs-lookup"><span data-stu-id="a0d34-102">Sample: Disable a user</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="a0d34-103">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="a0d34-103">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="a0d34-104">Download the complete sample from [Sample: Work with Users and Roles](https://code.msdn.microsoft.com/Users-and-Roles-Samples-a4f33f3f).</span><span class="sxs-lookup"><span data-stu-id="a0d34-104">Download the complete sample from [Sample: Work with Users and Roles](https://code.msdn.microsoft.com/Users-and-Roles-Samples-a4f33f3f).</span></span>   
  
## <a name="requirements"></a><span data-ttu-id="a0d34-105">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="a0d34-105">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="a0d34-106">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="a0d34-106">Demonstrates</span></span>  
 <span data-ttu-id="a0d34-107">This sample shows how to create a user in an [!INCLUDE[pn_Active_Directory](../includes/pn-active-directory.md)] environment using the <xref:Microsoft.Crm.Sdk.Messages.SetStateRequest> message.</span><span class="sxs-lookup"><span data-stu-id="a0d34-107">This sample shows how to create a user in an [!INCLUDE[pn_Active_Directory](../includes/pn-active-directory.md)] environment using the <xref:Microsoft.Crm.Sdk.Messages.SetStateRequest> message.</span></span> <span data-ttu-id="a0d34-108">A snippet showing just the key sections of the sample is shown first, followed by the [complete sample code](sample-create-on-premises-user.md#complete_sample).</span><span class="sxs-lookup"><span data-stu-id="a0d34-108">A snippet showing just the key sections of the sample is shown first, followed by the [complete sample code](sample-create-on-premises-user.md#complete_sample).</span></span> <span data-ttu-id="a0d34-109">Note that this sample can only be run in an on-premises environment because it creates a user.</span><span class="sxs-lookup"><span data-stu-id="a0d34-109">Note that this sample can only be run in an on-premises environment because it creates a user.</span></span> <span data-ttu-id="a0d34-110">However, the portion of the sample that demonstrates disabling the user will work for all environments.</span><span class="sxs-lookup"><span data-stu-id="a0d34-110">However, the portion of the sample that demonstrates disabling the user will work for all environments.</span></span>  
  
 [!INCLUDE[cc_sdk_onpremises_note](../includes/cc-sdk-onpremises-note.md)] 
 
## <a name="example"></a><span data-ttu-id="a0d34-111">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="a0d34-111">Example</span></span>  
 [!code-csharp[UsersAndRoles#DisableOrEnableUser1](../snippets/csharp/CRMV8/usersandroles/cs/disableorenableuser1.cs#disableorenableuser1)]  
  
<a name="complete_sample"></a>   
### <a name="complete-sample-code"></a><span data-ttu-id="a0d34-112">Complete sample code</span><span class="sxs-lookup"><span data-stu-id="a0d34-112">Complete sample code</span></span>  
 [!code-csharp[UsersAndRoles#DisableOrEnableUser](../snippets/csharp/CRMV8/usersandroles/cs/disableorenableuser.cs#disableorenableuser)]  
  
### <a name="see-also"></a><span data-ttu-id="a0d34-113">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="a0d34-113">See also</span></span>  
 <span data-ttu-id="a0d34-114">[User and Team Entities](user-team-entities.md) </span><span class="sxs-lookup"><span data-stu-id="a0d34-114">[User and Team Entities](user-team-entities.md) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.SetStateRequest>   
 [<span data-ttu-id="a0d34-115">Sample: CrmServiceHelper Class</span><span class="sxs-lookup"><span data-stu-id="a0d34-115">Sample: CrmServiceHelper Class</span></span>](org-service/helper-code-serverconnection-class.md)   
