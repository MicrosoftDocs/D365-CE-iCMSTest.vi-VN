---
title: 'Sample: Share records using GrantAccess, ModifyAccess and RevokeAccess messages (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: The sample shows how to share a record using the following messages:GrantAccessRequest, ModifyAccessRequest, and RevokeAccessRequest.
keywords: ''
ms.date: 12/15/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 791aa59d-b217-4e8d-93d3-edd4ecfc8403
author: KumarVivek
ms.author: kvivek
manager: jdaly
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
helpviewer_keywords:
- sharing records sample
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 2e119c4028a1215e290bad296cc5aad334f6ddb0
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387560"
---
# <a name="sample-share-records-using-grantaccess-modifyaccess-and-revokeaccess-messages"></a><span data-ttu-id="240a2-103">Sample: Share records using GrantAccess, ModifyAccess and RevokeAccess messages</span><span class="sxs-lookup"><span data-stu-id="240a2-103">Sample: Share records using GrantAccess, ModifyAccess and RevokeAccess messages</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="240a2-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="240a2-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="240a2-105">Download the Sample: [Work with early bound entity classes in code](https://code.msdn.microsoft.com/Work-with-early-bound-6914f6e7).</span><span class="sxs-lookup"><span data-stu-id="240a2-105">Download the Sample: [Work with early bound entity classes in code](https://code.msdn.microsoft.com/Work-with-early-bound-6914f6e7).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="240a2-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="240a2-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="240a2-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="240a2-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="240a2-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="240a2-108">Demonstrates</span></span>  
 <span data-ttu-id="240a2-109">This sample shows how to share a record using the following messages:</span><span class="sxs-lookup"><span data-stu-id="240a2-109">This sample shows how to share a record using the following messages:</span></span>  
  
-   <xref:Microsoft.Crm.Sdk.Messages.GrantAccessRequest>  
  
-   <xref:Microsoft.Crm.Sdk.Messages.ModifyAccessRequest>  
  
-   <xref:Microsoft.Crm.Sdk.Messages.RevokeAccessRequest>  
  
## <a name="example"></a><span data-ttu-id="240a2-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="240a2-110">Example</span></span>  
 [!code-csharp[strongtypes#UserAccess](../snippets/csharp/CRMV8/strongtypes/cs/useraccess.cs#useraccess)]  
  
### <a name="see-also"></a><span data-ttu-id="240a2-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="240a2-111">See also</span></span>  
 <span data-ttu-id="240a2-112">[User and Team Entities](user-team-entities.md) </span><span class="sxs-lookup"><span data-stu-id="240a2-112">[User and Team Entities](user-team-entities.md) </span></span>  
 <span data-ttu-id="240a2-113">[Introduction to Entities in Dynamics 365 for Customer Engagement apps](introduction-entities.md#Share) </span><span class="sxs-lookup"><span data-stu-id="240a2-113">[Introduction to Entities in Dynamics 365 for Customer Engagement apps](introduction-entities.md#Share) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.GrantAccessRequest>   
 <span data-ttu-id="240a2-114">[Sample: Create an On-Premises User](sample-create-on-premises-user.md) </span><span class="sxs-lookup"><span data-stu-id="240a2-114">[Sample: Create an On-Premises User](sample-create-on-premises-user.md) </span></span>  
 [<span data-ttu-id="240a2-115">Introduction to Entities in Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="240a2-115">Introduction to Entities in Dynamics 365 for Customer Engagement apps</span></span>](introduction-entities.md)
