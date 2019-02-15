---
title: 'Sample: Associate a security role to a team (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The sample shows how to assign a security role to a team by using the AssignRequest message.
ms.custom: ''
ms.date: 12/15/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- assigning a role to a team, sample
- assigning a security role, sample
- team security sample, assigning roles
ms.assetid: 6097b89f-b3a6-472b-8fed-4f1aef62817f
caps.latest.revision: 21
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 8c047d37b5b623c7acae60de61d482db4a363ee3
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387293"
---
# <a name="sample-associate-a-security-role-to-a-team"></a><span data-ttu-id="adffb-103">Sample: Associate a security role to a team</span><span class="sxs-lookup"><span data-stu-id="adffb-103">Sample: Associate a security role to a team</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="adffb-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="adffb-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="adffb-105">Download the Sample: [Work with early bound entity classes in code](https://code.msdn.microsoft.com/Work-with-early-bound-6914f6e7).</span><span class="sxs-lookup"><span data-stu-id="adffb-105">Download the Sample: [Work with early bound entity classes in code](https://code.msdn.microsoft.com/Work-with-early-bound-6914f6e7).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="adffb-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="adffb-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="adffb-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="adffb-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="adffb-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="adffb-108">Demonstrates</span></span>  
 <span data-ttu-id="adffb-109">This sample shows how to assign a security role to a team by using the <xref:Microsoft.Crm.Sdk.Messages.AssignRequest> message.</span><span class="sxs-lookup"><span data-stu-id="adffb-109">This sample shows how to assign a security role to a team by using the <xref:Microsoft.Crm.Sdk.Messages.AssignRequest> message.</span></span> <span data-ttu-id="adffb-110">Note that this example does not take into consideration that a team or user can only be assigned a role from its business unit.</span><span class="sxs-lookup"><span data-stu-id="adffb-110">Note that this example does not take into consideration that a team or user can only be assigned a role from its business unit.</span></span> <span data-ttu-id="adffb-111">The role to be assigned is the first from the collection that is returned by the `RetrieveMultiple` method.</span><span class="sxs-lookup"><span data-stu-id="adffb-111">The role to be assigned is the first from the collection that is returned by the `RetrieveMultiple` method.</span></span> <span data-ttu-id="adffb-112">If that record is from a business unit that is different from the requesting team, the assignment fails.</span><span class="sxs-lookup"><span data-stu-id="adffb-112">If that record is from a business unit that is different from the requesting team, the assignment fails.</span></span>  
  
## <a name="example"></a><span data-ttu-id="adffb-113">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="adffb-113">Example</span></span>  
 [!code-csharp[StrongTypes#AssignSecurityRoleToTeam1](../snippets/csharp/CRMV8/strongtypes/cs/assignsecurityroletoteam1.cs#assignsecurityroletoteam1)]  
  
### <a name="see-also"></a><span data-ttu-id="adffb-114">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="adffb-114">See also</span></span>  
 <span data-ttu-id="adffb-115">[Gán](introduction-entities.md#Assign) </span><span class="sxs-lookup"><span data-stu-id="adffb-115">[Assign](introduction-entities.md#Assign) </span></span>  
 <span data-ttu-id="adffb-116">[Privilege and Role Entities](privilege-role-entities.md) </span><span class="sxs-lookup"><span data-stu-id="adffb-116">[Privilege and Role Entities](privilege-role-entities.md) </span></span>  
 <span data-ttu-id="adffb-117">[Sample: Associate a Security Role to a User](sample-associate-security-role-user.md) </span><span class="sxs-lookup"><span data-stu-id="adffb-117">[Sample: Associate a Security Role to a User](sample-associate-security-role-user.md) </span></span>  
 <span data-ttu-id="adffb-118">[User and Team Entities](user-team-entities.md) </span><span class="sxs-lookup"><span data-stu-id="adffb-118">[User and Team Entities](user-team-entities.md) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.AssignRequest>
