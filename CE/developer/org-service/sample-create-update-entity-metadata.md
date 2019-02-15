---
title: 'Sample: Create and update entity metadata (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The sample demonstrates how to create a custom entity by using the CreateEntityRequest message. It also uses the CreateAttributeRequest to add several different types of attributes to the entity.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 237c75a2-cae5-467b-b894-ab0f7572e7f9
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 63e691c9d2121bfe9489d06f535c6d3003206c8f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388448"
---
# <a name="sample-create-and-update-entity-metadata"></a><span data-ttu-id="521a0-104">Sample: Create and update entity metadata</span><span class="sxs-lookup"><span data-stu-id="521a0-104">Sample: Create and update entity metadata</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="521a0-105">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="521a0-105">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span></span> <span data-ttu-id="521a0-106">Download the sample: [Work with entity metadata](https://code.msdn.microsoft.com/Samples-of-entities-916efa41).</span><span class="sxs-lookup"><span data-stu-id="521a0-106">Download the sample: [Work with entity metadata](https://code.msdn.microsoft.com/Samples-of-entities-916efa41).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="521a0-107">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="521a0-107">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="521a0-108">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="521a0-108">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="521a0-109">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="521a0-109">Demonstrates</span></span>  
 <span data-ttu-id="521a0-110">This sample shows how to create a custom entity by using the <xref:Microsoft.Xrm.Sdk.Messages.CreateEntityRequest> message.</span><span class="sxs-lookup"><span data-stu-id="521a0-110">This sample shows how to create a custom entity by using the <xref:Microsoft.Xrm.Sdk.Messages.CreateEntityRequest> message.</span></span> <span data-ttu-id="521a0-111">It also uses the <xref:Microsoft.Xrm.Sdk.Messages.CreateAttributeRequest> to add several different types of attributes to the entity.</span><span class="sxs-lookup"><span data-stu-id="521a0-111">It also uses the <xref:Microsoft.Xrm.Sdk.Messages.CreateAttributeRequest> to add several different types of attributes to the entity.</span></span>  
  
## <a name="example"></a><span data-ttu-id="521a0-112">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="521a0-112">Example</span></span>  
 [!code-csharp[entities#CreateUpdateEntityMetadata](../../snippets/csharp/CRMV8/entities/cs/createupdateentitymetadata.cs#createupdateentitymetadata)]  
  
### <a name="see-also"></a><span data-ttu-id="521a0-113">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="521a0-113">See also</span></span>  
 <span data-ttu-id="521a0-114">[Customize entity metadata](../customize-entity-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="521a0-114">[Customize entity metadata](../customize-entity-metadata.md) </span></span>  
 <span data-ttu-id="521a0-115">[Sample: Create a Custom Activity Entity](sample-create-custom-activity-entity.md) </span><span class="sxs-lookup"><span data-stu-id="521a0-115">[Sample: Create a Custom Activity Entity](sample-create-custom-activity-entity.md) </span></span>  
 <span data-ttu-id="521a0-116">[Extend the Metadata Model for Dynamics 365 for Customer Engagement](use-organization-service-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="521a0-116">[Extend the Metadata Model for Dynamics 365 for Customer Engagement](use-organization-service-metadata.md) </span></span>  
 <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllEntitiesRequest>   
 <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllEntitiesResponse>
