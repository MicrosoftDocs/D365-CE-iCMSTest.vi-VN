---
title: 'Sample: Dump entity privilege information to a file (Dynamics 365 for Customer Engagement apps SDK) | MicrosoftDocs'
description: This sample shows how to extract entity privilege information into a file using the organization service.
keywords: ''
ms.date: 10/31/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 22c60ceb-a0d4-460f-a3ce-d8541cf2da21
author: JimDaly
ms.author: jdaly
manager: jdaly
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: f52a1fafddb84f43150980112ffac9dc64004b2f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386028"
---
# <a name="sample-dump-entity-privilege-information-to-a-file"></a><span data-ttu-id="d76a4-103">Sample: Dump entity privilege information to a file</span><span class="sxs-lookup"><span data-stu-id="d76a4-103">Sample: Dump entity privilege information to a file</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="d76a4-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="d76a4-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span></span> <span data-ttu-id="d76a4-105">Download the sample: [Work with entity metadata](https://code.msdn.microsoft.com/Samples-of-entities-916efa41).</span><span class="sxs-lookup"><span data-stu-id="d76a4-105">Download the sample: [Work with entity metadata](https://code.msdn.microsoft.com/Samples-of-entities-916efa41).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d76a4-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="d76a4-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="d76a4-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="d76a4-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="d76a4-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="d76a4-108">Demonstrates</span></span>  
 <span data-ttu-id="d76a4-109">This sample shows how to write entity privilege information to an XML file, which will be located at \Entities\bin\Debug\EntityPrivileges.xml.</span><span class="sxs-lookup"><span data-stu-id="d76a4-109">This sample shows how to write entity privilege information to an XML file, which will be located at \Entities\bin\Debug\EntityPrivileges.xml.</span></span> <span data-ttu-id="d76a4-110">It uses the <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllEntitiesRequest> message.</span><span class="sxs-lookup"><span data-stu-id="d76a4-110">It uses the <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllEntitiesRequest> message.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d76a4-111">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="d76a4-111">Example</span></span>  
 [!code-csharp[entities#DumpEntityInfo](../../snippets/csharp/CRMV8/entities/cs/dumpentityinfo.cs#dumpentityinfo)]  
  
### <a name="see-also"></a><span data-ttu-id="d76a4-112">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="d76a4-112">See also</span></span>  
 <span data-ttu-id="d76a4-113">[Customize Entity Metadata](../customize-entity-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="d76a4-113">[Customize Entity Metadata](../customize-entity-metadata.md) </span></span>  
 <span data-ttu-id="d76a4-114">[Extend the Metadata Model for Dynamics 365 for Customer Engagement apps](use-organization-service-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="d76a4-114">[Extend the Metadata Model for Dynamics 365 for Customer Engagement apps](use-organization-service-metadata.md) </span></span>  
 <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllEntitiesRequest>   
 <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllEntitiesResponse>
