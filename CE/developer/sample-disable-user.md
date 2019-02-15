---
title: 'Sample: Disable a user (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The sample shows how to create a user in an Active Directory environment using the SetStateRequest message.
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
ms.openlocfilehash: 9d18902258ec345c612bfff164135dc32bdf9914
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388681"
---
# <a name="sample-disable-a-user"></a><span data-ttu-id="9d38b-103">Sample: Disable a user</span><span class="sxs-lookup"><span data-stu-id="9d38b-103">Sample: Disable a user</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="9d38b-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="9d38b-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="9d38b-105">Download the complete sample from [Sample: Work with Users and Roles](https://code.msdn.microsoft.com/Users-and-Roles-Samples-a4f33f3f).</span><span class="sxs-lookup"><span data-stu-id="9d38b-105">Download the complete sample from [Sample: Work with Users and Roles](https://code.msdn.microsoft.com/Users-and-Roles-Samples-a4f33f3f).</span></span>   

## <a name="prerequisites"></a><span data-ttu-id="9d38b-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="9d38b-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="9d38b-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="9d38b-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="9d38b-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="9d38b-108">Demonstrates</span></span>  
 <span data-ttu-id="9d38b-109">This sample shows how to create a user in an [!INCLUDE[pn_Active_Directory](../includes/pn-active-directory.md)] environment using the <xref:Microsoft.Crm.Sdk.Messages.SetStateRequest> message.</span><span class="sxs-lookup"><span data-stu-id="9d38b-109">This sample shows how to create a user in an [!INCLUDE[pn_Active_Directory](../includes/pn-active-directory.md)] environment using the <xref:Microsoft.Crm.Sdk.Messages.SetStateRequest> message.</span></span> <span data-ttu-id="9d38b-110">A snippet showing just the key sections of the sample is shown first, followed by the [complete sample code](sample-create-on-premises-user.md#complete_sample).</span><span class="sxs-lookup"><span data-stu-id="9d38b-110">A snippet showing just the key sections of the sample is shown first, followed by the [complete sample code](sample-create-on-premises-user.md#complete_sample).</span></span> <span data-ttu-id="9d38b-111">Note that this sample can only be run in an on-premises environment because it creates a user.</span><span class="sxs-lookup"><span data-stu-id="9d38b-111">Note that this sample can only be run in an on-premises environment because it creates a user.</span></span> <span data-ttu-id="9d38b-112">However, the portion of the sample that demonstrates disabling the user will work for all environments.</span><span class="sxs-lookup"><span data-stu-id="9d38b-112">However, the portion of the sample that demonstrates disabling the user will work for all environments.</span></span>  
  
[!INCLUDE[cc_sdk_onpremises_note](../includes/cc-sdk-onpremises-note.md)] 

## <a name="example"></a><span data-ttu-id="9d38b-113">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="9d38b-113">Example</span></span>  
 [!code-csharp[UsersAndRoles#DisableOrEnableUser1](../snippets/csharp/CRMV8/usersandroles/cs/disableorenableuser1.cs#disableorenableuser1)]  
  
<a name="complete_sample"></a>   
### <a name="complete-sample-code"></a><span data-ttu-id="9d38b-114">Complete sample code</span><span class="sxs-lookup"><span data-stu-id="9d38b-114">Complete sample code</span></span>  
 [!code-csharp[UsersAndRoles#DisableOrEnableUser](../snippets/csharp/CRMV8/usersandroles/cs/disableorenableuser.cs#disableorenableuser)]  
  
### <a name="see-also"></a><span data-ttu-id="9d38b-115">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="9d38b-115">See also</span></span>  
 <span data-ttu-id="9d38b-116">[User and Team Entities](user-team-entities.md) </span><span class="sxs-lookup"><span data-stu-id="9d38b-116">[User and Team Entities](user-team-entities.md) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.SetStateRequest>   
 [<span data-ttu-id="9d38b-117">Sample: CrmServiceHelper Class</span><span class="sxs-lookup"><span data-stu-id="9d38b-117">Sample: CrmServiceHelper Class</span></span>](org-service/helper-code-serverconnection-class.md)   
