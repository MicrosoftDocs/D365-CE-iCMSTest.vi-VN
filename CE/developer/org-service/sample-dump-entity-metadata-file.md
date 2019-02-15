---
title: 'Sample: Dump entity metadata to a file (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: 'The sample demonstrates how to write out all the entity metadata to an XML file. It uses the RetrieveAllEntitiesRequest message. '
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 0a0247f3-3a59-42d1-b865-54d0f34e4aad
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4304e62f9000ba321f26906f14c1ab7c28457b7f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388620"
---
# <a name="sample-dump-entity-metadata-to-a-file"></a><span data-ttu-id="95454-104">Sample: Dump entity metadata to a file</span><span class="sxs-lookup"><span data-stu-id="95454-104">Sample: Dump entity metadata to a file</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="95454-105">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="95454-105">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span></span> <span data-ttu-id="95454-106">Download the sample: [Work with entity metadata](https://code.msdn.microsoft.com/Samples-of-entities-916efa41).</span><span class="sxs-lookup"><span data-stu-id="95454-106">Download the sample: [Work with entity metadata](https://code.msdn.microsoft.com/Samples-of-entities-916efa41).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="95454-107">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="95454-107">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="95454-108">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="95454-108">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="95454-109">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="95454-109">Demonstrates</span></span>  
 <span data-ttu-id="95454-110">This sample shows how to write out all the entity metadata to an XML file.</span><span class="sxs-lookup"><span data-stu-id="95454-110">This sample shows how to write out all the entity metadata to an XML file.</span></span> <span data-ttu-id="95454-111">It uses the <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllEntitiesRequest> message.</span><span class="sxs-lookup"><span data-stu-id="95454-111">It uses the <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllEntitiesRequest> message.</span></span>  
  
 <span data-ttu-id="95454-112">The following sample creates a new file at \Entities\bin\Debug\EntityInfo.xml.</span><span class="sxs-lookup"><span data-stu-id="95454-112">The following sample creates a new file at \Entities\bin\Debug\EntityInfo.xml.</span></span> <span data-ttu-id="95454-113">You can open this file in [!INCLUDE[pn_MS_Excel_Full](../../includes/pn-ms-excel-full.md)] to see a tabular report.</span><span class="sxs-lookup"><span data-stu-id="95454-113">You can open this file in [!INCLUDE[pn_MS_Excel_Full](../../includes/pn-ms-excel-full.md)] to see a tabular report.</span></span> <span data-ttu-id="95454-114">You may need this information to discover the entity type code for a custom entity for use in reports.</span><span class="sxs-lookup"><span data-stu-id="95454-114">You may need this information to discover the entity type code for a custom entity for use in reports.</span></span>  
  
## <a name="example"></a><span data-ttu-id="95454-115">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="95454-115">Example</span></span>  
 [!code-csharp[entities#DumpEntityInfo](../../snippets/csharp/CRMV8/entities/cs/dumpentityinfo.cs#dumpentityinfo)]  
  
### <a name="see-also"></a><span data-ttu-id="95454-116">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="95454-116">See also</span></span>  
 <span data-ttu-id="95454-117">[Customize Entity Metadata](../customize-entity-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="95454-117">[Customize Entity Metadata](../customize-entity-metadata.md) </span></span>  
 <span data-ttu-id="95454-118">[Sample: Dump Entity Privilege Information to a File](sample-dump-entity-privilege-information-file.md) </span><span class="sxs-lookup"><span data-stu-id="95454-118">[Sample: Dump Entity Privilege Information to a File](sample-dump-entity-privilege-information-file.md) </span></span>  
 <span data-ttu-id="95454-119">[Extend the Metadata Model for Dynamics 365 for Customer Engagement apps](use-organization-service-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="95454-119">[Extend the Metadata Model for Dynamics 365 for Customer Engagement apps](use-organization-service-metadata.md) </span></span>  
 <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllEntitiesRequest>   
 <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllEntitiesResponse>
