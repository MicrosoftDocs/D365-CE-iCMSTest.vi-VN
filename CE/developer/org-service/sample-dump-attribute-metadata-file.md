---
title: 'Sample: Dump attribute metadata to a file (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The sample shows how to write out all the attribute metadata to an XML file. It uses the RetrieveAllEntitiesRequest message.
keywords: ''
ms.date: 10/31/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: f2321671-f4dc-4abd-ac50-edddfa170fd2
author: JimDaly
ms.author: jdaly
manager: jdaly
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 20a1f1ccdd78a4affa167e62d9cd7f9975a7f1da
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388691"
---
# <a name="sample-dump-attribute-metadata-to-a-file"></a><span data-ttu-id="d8257-104">Sample: Dump attribute metadata to a file</span><span class="sxs-lookup"><span data-stu-id="d8257-104">Sample: Dump attribute metadata to a file</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="d8257-105">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="d8257-105">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span></span> <span data-ttu-id="d8257-106">Download the sample: [Work with attribute metadata](https://code.msdn.microsoft.com/Samples-of-attributes-1c0f93e7).</span><span class="sxs-lookup"><span data-stu-id="d8257-106">Download the sample: [Work with attribute metadata](https://code.msdn.microsoft.com/Samples-of-attributes-1c0f93e7).</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="d8257-107">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="d8257-107">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="d8257-108">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="d8257-108">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="d8257-109">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="d8257-109">Demonstrates</span></span>  
 <span data-ttu-id="d8257-110">This sample shows how to write out all the attribute metadata to an XML file.</span><span class="sxs-lookup"><span data-stu-id="d8257-110">This sample shows how to write out all the attribute metadata to an XML file.</span></span> <span data-ttu-id="d8257-111">It uses the <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllEntitiesRequest> message.</span><span class="sxs-lookup"><span data-stu-id="d8257-111">It uses the <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllEntitiesRequest> message.</span></span>  
  
 <span data-ttu-id="d8257-112">The following sample creates a new file at \Entities\bin\Debug\AllAttributeDesc.xml.</span><span class="sxs-lookup"><span data-stu-id="d8257-112">The following sample creates a new file at \Entities\bin\Debug\AllAttributeDesc.xml.</span></span> <span data-ttu-id="d8257-113">You can open this file in [!INCLUDE[pn_MS_Excel_Full](../../includes/pn-ms-excel-full.md)] to see a tabular report.</span><span class="sxs-lookup"><span data-stu-id="d8257-113">You can open this file in [!INCLUDE[pn_MS_Excel_Full](../../includes/pn-ms-excel-full.md)] to see a tabular report.</span></span> <span data-ttu-id="d8257-114">You can easily look up information such as which attributes can be specified in a create, retrieve, or update operation.</span><span class="sxs-lookup"><span data-stu-id="d8257-114">You can easily look up information such as which attributes can be specified in a create, retrieve, or update operation.</span></span> <span data-ttu-id="d8257-115">This information can also be found in the “*EntityName* Entity Attribute Metadata” topic for each entity.</span><span class="sxs-lookup"><span data-stu-id="d8257-115">This information can also be found in the “*EntityName* Entity Attribute Metadata” topic for each entity.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d8257-116">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="d8257-116">Example</span></span>  
 [!code-csharp[Attributes#DumpAttributeInfo](../../snippets/csharp/CRMV8/attributes/cs/dumpattributeinfo.cs#dumpattributeinfo)]  
  
### <a name="see-also"></a><span data-ttu-id="d8257-117">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="d8257-117">See also</span></span>  
 <span data-ttu-id="d8257-118">[Customize entity attribute metadata](../customize-entity-attribute-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="d8257-118">[Customize entity attribute metadata](../customize-entity-attribute-metadata.md) </span></span>  
 <span data-ttu-id="d8257-119">[Sample: Dump attribute picklist metadata to a file](sample-dump-attribute-picklist-metadata-file.md) </span><span class="sxs-lookup"><span data-stu-id="d8257-119">[Sample: Dump attribute picklist metadata to a file](sample-dump-attribute-picklist-metadata-file.md) </span></span>  
 <span data-ttu-id="d8257-120">[Extend the Metadata Model for Dynamics 365 for Customer Engagement apps](use-organization-service-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="d8257-120">[Extend the Metadata Model for Dynamics 365 for Customer Engagement apps](use-organization-service-metadata.md) </span></span>  
 <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllEntitiesRequest>   
 <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllEntitiesResponse>
