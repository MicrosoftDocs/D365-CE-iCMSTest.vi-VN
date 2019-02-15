---
title: 'Sample: Create a custom activity entity (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The sample demonstrates how to create a custom activity entity. It uses the CreateEntityRequest message and sets the EntityMetadata.IsActivity property to true.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: d227f8b1-65c7-4d08-9fdc-6162c3f0bdbb
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 82cadd9652fa7b8282529ee67f17af692eb3d4fb
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385635"
---
# <a name="sample-create-a-custom-activity-entity"></a><span data-ttu-id="dca71-104">Sample: Create a custom activity entity</span><span class="sxs-lookup"><span data-stu-id="dca71-104">Sample: Create a custom activity entity</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="dca71-105">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="dca71-105">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span></span> <span data-ttu-id="dca71-106">Download the sample: [Work with entity metadata](https://code.msdn.microsoft.com/Samples-of-entities-916efa41).</span><span class="sxs-lookup"><span data-stu-id="dca71-106">Download the sample: [Work with entity metadata](https://code.msdn.microsoft.com/Samples-of-entities-916efa41).</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="dca71-107">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="dca71-107">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="dca71-108">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="dca71-108">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="dca71-109">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="dca71-109">Demonstrates</span></span>  
 <span data-ttu-id="dca71-110">This sample shows how to create a custom activity entity.</span><span class="sxs-lookup"><span data-stu-id="dca71-110">This sample shows how to create a custom activity entity.</span></span> <span data-ttu-id="dca71-111">It uses the <xref:Microsoft.Xrm.Sdk.Messages.CreateEntityRequest> message and sets the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata>.<xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsActivity></span><span class="sxs-lookup"><span data-stu-id="dca71-111">It uses the <xref:Microsoft.Xrm.Sdk.Messages.CreateEntityRequest> message and sets the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata>.<xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsActivity></span></span> <span data-ttu-id="dca71-112">property to `true`.</span><span class="sxs-lookup"><span data-stu-id="dca71-112">property to `true`.</span></span>  
  
## <a name="example"></a><span data-ttu-id="dca71-113">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="dca71-113">Example</span></span>  
 [!code-csharp[entities#CreateCustomActivityEntity](../../snippets/csharp/CRMV8/entities/cs/createcustomactivityentity.cs#createcustomactivityentity)]  
  
### <a name="see-also"></a><span data-ttu-id="dca71-114">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="dca71-114">See also</span></span>  
 <span data-ttu-id="dca71-115">[Extend the Metadata Model for Dynamics 365 for Customer Engagement apps](use-organization-service-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="dca71-115">[Extend the Metadata Model for Dynamics 365 for Customer Engagement apps](use-organization-service-metadata.md) </span></span>  
 <span data-ttu-id="dca71-116">[Create a Custom Activity Entity](create-custom-activity-entity.md) </span><span class="sxs-lookup"><span data-stu-id="dca71-116">[Create a Custom Activity Entity](create-custom-activity-entity.md) </span></span>  
 <span data-ttu-id="dca71-117">[Customize entity metadata](../customize-entity-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="dca71-117">[Customize entity metadata](../customize-entity-metadata.md) </span></span>  
 <span data-ttu-id="dca71-118">[Sample: Create and Update an Emailable Entity](sample-create-update-emailable-entity.md) </span><span class="sxs-lookup"><span data-stu-id="dca71-118">[Sample: Create and Update an Emailable Entity](sample-create-update-emailable-entity.md) </span></span>  
 <xref:Microsoft.Xrm.Sdk.Messages.CreateEntityRequest>
