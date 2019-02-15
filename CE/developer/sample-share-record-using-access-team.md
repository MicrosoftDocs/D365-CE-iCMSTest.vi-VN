---
title: 'Sample: Share a record using an access team (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: The sample shows how to allow access to a record using an access team. All members of the team receive the same access to the record as is granted to the team.
keywords: ''
ms.date: 12/15/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 9b841889-c396-4f6e-8588-e702e94c7073
author: KumarVivek
ms.author: kvivek
manager: jdaly
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
caps.latest.revision: 9
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 9857a30f9d4f4a7e08a08443faa527ab7de74dd9
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388529"
---
# <a name="sample-share-a-record-using-an-access-team"></a><span data-ttu-id="b16ba-104">Sample: Share a record using an access team</span><span class="sxs-lookup"><span data-stu-id="b16ba-104">Sample: Share a record using an access team</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="b16ba-105">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="b16ba-105">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="b16ba-106">Download the Sample: [Work with early bound entity classes in code](https://code.msdn.microsoft.com/Work-with-early-bound-6914f6e7).</span><span class="sxs-lookup"><span data-stu-id="b16ba-106">Download the Sample: [Work with early bound entity classes in code](https://code.msdn.microsoft.com/Work-with-early-bound-6914f6e7).</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="b16ba-107">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="b16ba-107">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="b16ba-108">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="b16ba-108">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="b16ba-109">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="b16ba-109">Demonstrates</span></span>  
 <span data-ttu-id="b16ba-110">This sample shows how to allow access to a record using an access team.</span><span class="sxs-lookup"><span data-stu-id="b16ba-110">This sample shows how to allow access to a record using an access team.</span></span> <span data-ttu-id="b16ba-111">All members of the team receive the same access to the record as is granted to the team.</span><span class="sxs-lookup"><span data-stu-id="b16ba-111">All members of the team receive the same access to the record as is granted to the team.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b16ba-112">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="b16ba-112">Example</span></span>  
 [!code-csharp[strongtypes#CreateAndShareAccessTeam](../snippets/csharp/CRMV8/strongtypes/cs/createandshareaccessteam.cs#createandshareaccessteam)]  
  
### <a name="see-also"></a><span data-ttu-id="b16ba-113">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="b16ba-113">See also</span></span>  
 <span data-ttu-id="b16ba-114">[User and Team Entities](user-team-entities.md) </span><span class="sxs-lookup"><span data-stu-id="b16ba-114">[User and Team Entities](user-team-entities.md) </span></span>  
 <span data-ttu-id="b16ba-115">[Introduction to Entities in Dynamics 365 for Customer Engagement apps](introduction-entities.md#Share) </span><span class="sxs-lookup"><span data-stu-id="b16ba-115">[Introduction to Entities in Dynamics 365 for Customer Engagement apps](introduction-entities.md#Share) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.GrantAccessRequest>   
 [<span data-ttu-id="b16ba-116">Sample: Share Records Using GrantAccess, ModifyAccess and RevokeAccess Messages</span><span class="sxs-lookup"><span data-stu-id="b16ba-116">Sample: Share Records Using GrantAccess, ModifyAccess and RevokeAccess Messages</span></span>](sample-share-records-using-grantaccess-modifyaccess-revokeaccess-messages.md)
