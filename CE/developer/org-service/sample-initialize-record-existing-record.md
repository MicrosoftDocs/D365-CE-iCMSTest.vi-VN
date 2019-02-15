---
title: 'Sample: Initialize a record from an existing record (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: This sample shows how to use the IOrganizationService.InitializeFromRequest message to create new records from an existing record
keywords: ''
ms.date: 12/15/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 1d0d6df3-e905-4b63-beaa-3f72f73bfa17
author: JimDaly
ms.author: jdaly
manager: jdaly
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: e2b96d1f5054aa65bb12b1723cc37e2f61ade13d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385898"
---
# <a name="sample-initialize-a-record-from-an-existing-record"></a><span data-ttu-id="5ccaa-103">Sample: Initialize a record from an existing record</span><span class="sxs-lookup"><span data-stu-id="5ccaa-103">Sample: Initialize a record from an existing record</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="5ccaa-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="5ccaa-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span></span> <span data-ttu-id="5ccaa-105">Download the Sample: [Work with early bound entity classes in code](https://code.msdn.microsoft.com/Work-with-early-bound-6914f6e7).</span><span class="sxs-lookup"><span data-stu-id="5ccaa-105">Download the Sample: [Work with early bound entity classes in code](https://code.msdn.microsoft.com/Work-with-early-bound-6914f6e7).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="5ccaa-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="5ccaa-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="5ccaa-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="5ccaa-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
-   [<span data-ttu-id="5ccaa-108">Full Sample – C#</span><span class="sxs-lookup"><span data-stu-id="5ccaa-108">Full Sample – C#</span></span>](sample-initialize-record-existing-record.md#full_C)  
  
## <a name="demonstrates"></a><span data-ttu-id="5ccaa-109">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="5ccaa-109">Demonstrates</span></span>  
 <span data-ttu-id="5ccaa-110">This sample shows how to use the<xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Crm.Sdk.Messages.InitializeFromRequest></span><span class="sxs-lookup"><span data-stu-id="5ccaa-110">This sample shows how to use the<xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Crm.Sdk.Messages.InitializeFromRequest></span></span> <span data-ttu-id="5ccaa-111">message to create new records from an existing record.</span><span class="sxs-lookup"><span data-stu-id="5ccaa-111">message to create new records from an existing record.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5ccaa-112">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="5ccaa-112">Example</span></span>  
 [!code-csharp[StrongTypes#InitializeFrom1](../../snippets/csharp/CRMV8/strongtypes/cs/initializefrom1.cs#initializefrom1)]  
  
<a name="full_C"></a>   
## <a name="full-sample--c"></a><span data-ttu-id="5ccaa-113">Full Sample – C#</span><span class="sxs-lookup"><span data-stu-id="5ccaa-113">Full Sample – C#</span></span>  
 [!code-csharp[StrongTypes#InitializeFrom](../../snippets/csharp/CRMV8/strongtypes/cs/initializefrom.cs#initializefrom)]  
  
### <a name="see-also"></a><span data-ttu-id="5ccaa-114">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="5ccaa-114">See also</span></span>  
 <span data-ttu-id="5ccaa-115">[Use the Early Bound Entity Classes in Code](use-early-bound-entity-classes-code.md) </span><span class="sxs-lookup"><span data-stu-id="5ccaa-115">[Use the Early Bound Entity Classes in Code](use-early-bound-entity-classes-code.md) </span></span>  
 <span data-ttu-id="5ccaa-116">[Sample: Retrieve license information](sample-retrieve-license-information.md) </span><span class="sxs-lookup"><span data-stu-id="5ccaa-116">[Sample: Retrieve license information](sample-retrieve-license-information.md) </span></span>  
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 <xref:Microsoft.Crm.Sdk.Messages.InitializeFromRequest>   
 <xref:Microsoft.Xrm.Sdk.IOrganizationService.Associate*>
