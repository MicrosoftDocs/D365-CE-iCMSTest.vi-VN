---
title: 'Sample: Use the organization service context (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: This sample shows how to use the OrganizationServiceContext to perform basic operations such as create, retrieve, update and delete
keywords: ''
ms.date: 12/15/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 1b18abeb-faa2-461b-b36d-0db5b489dc80
author: JimDaly
ms.author: jdaly
manager: jdaly
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
helpviewer_keywords:
- sample for performing basic operations by using the organization service context
- using the organization service context to perform basic operations sample, early-bound class samples
- sample for using the organization service context to perform basic operations
- performing basic operations by using the organization service context sample, early-bound class samples
- early-bound class samples, performing basic operations by using the organization service context sample
- samples for early-bound classes, performing basic operations by using the organization service context sample
caps.latest.revision: 22
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: e7a0a05cd7bd06342721bb33b278d6ef798b4bda
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388208"
---
# <a name="sample-use-the-organization-service-context"></a><span data-ttu-id="da6e5-103">Sample: Use the organization service context</span><span class="sxs-lookup"><span data-stu-id="da6e5-103">Sample: Use the organization service context</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="da6e5-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="da6e5-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span></span> <span data-ttu-id="da6e5-105">Download the Sample: [Work with early bound entity classes in code](https://code.msdn.microsoft.com/Work-with-early-bound-6914f6e7).</span><span class="sxs-lookup"><span data-stu-id="da6e5-105">Download the Sample: [Work with early bound entity classes in code](https://code.msdn.microsoft.com/Work-with-early-bound-6914f6e7).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="da6e5-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="da6e5-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="da6e5-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="da6e5-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="da6e5-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="da6e5-108">Demonstrates</span></span>  
 <span data-ttu-id="da6e5-109">This sample shows how to use the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext> to perform basic operations such as create, retrieve, update and delete.</span><span class="sxs-lookup"><span data-stu-id="da6e5-109">This sample shows how to use the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext> to perform basic operations such as create, retrieve, update and delete.</span></span>  
  
## <a name="example"></a><span data-ttu-id="da6e5-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="da6e5-110">Example</span></span>  
 [!code-csharp[StrongTypes#BasicContextExamples](../../snippets/csharp/CRMV8/strongtypes/cs/basiccontextexamples.cs#basiccontextexamples)]  
  
### <a name="see-also"></a><span data-ttu-id="da6e5-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="da6e5-111">See also</span></span>  
 <span data-ttu-id="da6e5-112">[Use the Early Bound Entity Classes in Code](use-early-bound-entity-classes-code.md) </span><span class="sxs-lookup"><span data-stu-id="da6e5-112">[Use the Early Bound Entity Classes in Code](use-early-bound-entity-classes-code.md) </span></span>  
 <span data-ttu-id="da6e5-113">[Sample: Create, Retrieve, Update, and Delete Records (Early Bound)](sample-create-retrieve-update-delete-records-early-bound.md) </span><span class="sxs-lookup"><span data-stu-id="da6e5-113">[Sample: Create, Retrieve, Update, and Delete Records (Early Bound)](sample-create-retrieve-update-delete-records-early-bound.md) </span></span>  
 <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext>   
 <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext.AddObject(Microsoft.Xrm.Sdk.Entity)>    
 <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext.AddRelatedObject(Microsoft.Xrm.Sdk.Entity,Microsoft.Xrm.Sdk.Relationship,Microsoft.Xrm.Sdk.Entity)>   
 <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext.DeleteLink(Microsoft.Xrm.Sdk.Entity,Microsoft.Xrm.Sdk.Relationship,Microsoft.Xrm.Sdk.Entity)>  
