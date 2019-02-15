---
title: 'Sample: Dump attribute picklist metadata to a file (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The sample shows how to write out all the attribute metadata to an XML file. It uses the RetrieveAllEntitiesRequest message.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 0cfa185c-1845-40b4-8293-ffa540b6053c
caps.latest.revision: 16
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: da613bcbd663f9d3a27fa744c26d0f7a982d55a0
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388030"
---
# <a name="sample-dump-attribute-picklist-metadata-to-a-file"></a><span data-ttu-id="2588d-104">Sample: Dump attribute picklist metadata to a file</span><span class="sxs-lookup"><span data-stu-id="2588d-104">Sample: Dump attribute picklist metadata to a file</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="2588d-105">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="2588d-105">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span></span> <span data-ttu-id="2588d-106">Download the sample: [Work with attribute metadata](https://code.msdn.microsoft.com/Samples-of-attributes-1c0f93e7).</span><span class="sxs-lookup"><span data-stu-id="2588d-106">Download the sample: [Work with attribute metadata](https://code.msdn.microsoft.com/Samples-of-attributes-1c0f93e7).</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="2588d-107">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="2588d-107">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="2588d-108">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="2588d-108">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="2588d-109">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="2588d-109">Demonstrates</span></span>  
 <span data-ttu-id="2588d-110">This sample shows how to write out all the entity metadata to an XML file.</span><span class="sxs-lookup"><span data-stu-id="2588d-110">This sample shows how to write out all the entity metadata to an XML file.</span></span> <span data-ttu-id="2588d-111">It uses the <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllEntitiesRequest> message.</span><span class="sxs-lookup"><span data-stu-id="2588d-111">It uses the <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllEntitiesRequest> message.</span></span>  
  
 <span data-ttu-id="2588d-112">The following sample creates a new file at \Entities\bin\Debug\AttributePicklistValues.xml.</span><span class="sxs-lookup"><span data-stu-id="2588d-112">The following sample creates a new file at \Entities\bin\Debug\AttributePicklistValues.xml.</span></span> <span data-ttu-id="2588d-113">You can open this file in [!INCLUDE[pn_MS_Excel_Full](../../includes/pn-ms-excel-full.md)] to see a tabular report.</span><span class="sxs-lookup"><span data-stu-id="2588d-113">You can open this file in [!INCLUDE[pn_MS_Excel_Full](../../includes/pn-ms-excel-full.md)] to see a tabular report.</span></span> <span data-ttu-id="2588d-114">This is useful to look up the valid values for each picklist.</span><span class="sxs-lookup"><span data-stu-id="2588d-114">This is useful to look up the valid values for each picklist.</span></span> <span data-ttu-id="2588d-115">This information can also be found in the “*EntityName* Entity OptionSet Attribute Metadata” topic for each entity.</span><span class="sxs-lookup"><span data-stu-id="2588d-115">This information can also be found in the “*EntityName* Entity OptionSet Attribute Metadata” topic for each entity.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2588d-116">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="2588d-116">Example</span></span>  
 [!code-csharp[Attributes#DumpPicklistInfo](../../snippets/csharp/CRMV8/attributes/cs/dumppicklistinfo.cs#dumppicklistinfo)]  
  
### <a name="see-also"></a><span data-ttu-id="2588d-117">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="2588d-117">See also</span></span>  
 <span data-ttu-id="2588d-118">[Customize entity metadata](../customize-entity-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="2588d-118">[Customize entity metadata](../customize-entity-metadata.md) </span></span>  
 <span data-ttu-id="2588d-119">[Extend the Metadata Model for Dynamics 365 for Customer Engagement apps](use-organization-service-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="2588d-119">[Extend the Metadata Model for Dynamics 365 for Customer Engagement apps](use-organization-service-metadata.md) </span></span>  
 <span data-ttu-id="2588d-120">[Customize Entity Attribute Metadata](../customize-entity-attribute-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="2588d-120">[Customize Entity Attribute Metadata](../customize-entity-attribute-metadata.md) </span></span>  
 <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllEntitiesRequest>   
 <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllEntitiesResponse>
