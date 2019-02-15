---
title: 'Sample: Dump entity relationship information to a file (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: 'The sample shows how to write out all the entity relationship metadata to an XML file. It uses the RetrieveAllEntitiesRequest message. '
keywords: ''
ms.date: 10/31/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 41d4f199-7004-4458-a39a-5f9025550932
author: JimDaly
ms.author: jdaly
manager: jdaly
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 2eb28003528cf9b72a96807b5ecc003cfc409158
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388367"
---
# <a name="sample-dump-entity-relationship-information-to-a-file"></a><span data-ttu-id="27cba-104">Sample: Dump entity relationship information to a file</span><span class="sxs-lookup"><span data-stu-id="27cba-104">Sample: Dump entity relationship information to a file</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="27cba-105">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="27cba-105">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span></span> <span data-ttu-id="27cba-106">Download the sample: [Work with entity relationships](https://code.msdn.microsoft.com/Samples-of-entity-218db099).</span><span class="sxs-lookup"><span data-stu-id="27cba-106">Download the sample: [Work with entity relationships](https://code.msdn.microsoft.com/Samples-of-entity-218db099).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="27cba-107">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="27cba-107">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="27cba-108">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="27cba-108">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="27cba-109">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="27cba-109">Demonstrates</span></span>  
 <span data-ttu-id="27cba-110">This sample shows how to write out all the entity relationship metadata to an XML file.</span><span class="sxs-lookup"><span data-stu-id="27cba-110">This sample shows how to write out all the entity relationship metadata to an XML file.</span></span> <span data-ttu-id="27cba-111">It uses the <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllEntitiesRequest> message.</span><span class="sxs-lookup"><span data-stu-id="27cba-111">It uses the <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllEntitiesRequest> message.</span></span>  
  
 <span data-ttu-id="27cba-112">The following sample creates a new file at \Relationships\bin\Debug\RelationshipInfo.xml.</span><span class="sxs-lookup"><span data-stu-id="27cba-112">The following sample creates a new file at \Relationships\bin\Debug\RelationshipInfo.xml.</span></span> <span data-ttu-id="27cba-113">You can open this file in [!INCLUDE[pn_MS_Excel_Full](../../includes/pn-ms-excel-full.md)] to see a tabular report.</span><span class="sxs-lookup"><span data-stu-id="27cba-113">You can open this file in [!INCLUDE[pn_MS_Excel_Full](../../includes/pn-ms-excel-full.md)] to see a tabular report.</span></span> <span data-ttu-id="27cba-114">You may need this information to discover the entity type code for a custom entity for use in reports.</span><span class="sxs-lookup"><span data-stu-id="27cba-114">You may need this information to discover the entity type code for a custom entity for use in reports.</span></span>  
  
## <a name="example"></a><span data-ttu-id="27cba-115">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="27cba-115">Example</span></span>  
 [!code-csharp[entities#DumpEntityInfo](../../snippets/csharp/CRMV8/entities/cs/dumpentityinfo.cs#dumpentityinfo)]  
  
### <a name="see-also"></a><span data-ttu-id="27cba-116">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="27cba-116">See also</span></span>  
 <span data-ttu-id="27cba-117">[Customize Entity Relationship Metadata](../customize-entity-relationship-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="27cba-117">[Customize Entity Relationship Metadata](../customize-entity-relationship-metadata.md) </span></span>  
 <span data-ttu-id="27cba-118">[Extend the Metadata Model for Dynamics 365 for Customer Engagement apps](use-organization-service-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="27cba-118">[Extend the Metadata Model for Dynamics 365 for Customer Engagement apps](use-organization-service-metadata.md) </span></span>  
 <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllEntitiesRequest>   
 <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllEntitiesResponse>
