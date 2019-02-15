---
title: 'Sample: Retrieve multiple with the QueryByAttribute class (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: This sample shows how to use QueryByAttribute in the QueryBase) method
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- sample for using the RetrieveMultiple method with the QueryByAttribute class
- using the RetrieveMultiple method with the QueryByAttribute class sample
- QueryByAttribute class, samples
- building queries by using QueryExpression samples
- building queries by using QueryExpression, samples
ms.assetid: f94eae17-4a1a-4f7a-8d90-5ebfb7ffe22f
caps.latest.revision: 26
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4dcb7e1d2459eea29fa30fc17d2225f80e4f358f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387516"
---
# <a name="sample-retrieve-multiple-with-the-querybyattribute-class"></a><span data-ttu-id="29b3c-103">Sample: Retrieve multiple with the QueryByAttribute class</span><span class="sxs-lookup"><span data-stu-id="29b3c-103">Sample: Retrieve multiple with the QueryByAttribute class</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="29b3c-104">This sample is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="29b3c-104">This sample is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span></span> [!INCLUDE[sdk_download](../../includes/sdk-download.md)] <span data-ttu-id="29b3c-105">Download the complete sample from [Sample: Work with Queries](https://code.msdn.microsoft.com/Sample-Work-with-Queries-8265a78e).</span><span class="sxs-lookup"><span data-stu-id="29b3c-105">Download the complete sample from [Sample: Work with Queries](https://code.msdn.microsoft.com/Sample-Work-with-Queries-8265a78e).</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="29b3c-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="29b3c-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="29b3c-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="29b3c-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="example"></a><span data-ttu-id="29b3c-108">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="29b3c-108">Example</span></span>  
 <span data-ttu-id="29b3c-109">This sample shows how to use <xref:Microsoft.Xrm.Sdk.Query.QueryByAttribute> in the <xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*> method.</span><span class="sxs-lookup"><span data-stu-id="29b3c-109">This sample shows how to use <xref:Microsoft.Xrm.Sdk.Query.QueryByAttribute> in the <xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*> method.</span></span>  
  
 [!code-csharp[Query#QueryByAttribute](../../snippets/csharp/CRMV8/query/cs/querybyattribute.cs#querybyattribute)]  
  
### <a name="see-also"></a><span data-ttu-id="29b3c-110">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="29b3c-110">See also</span></span>  
 <span data-ttu-id="29b3c-111">[Build Queries with QueryExpression](build-queries-with-queryexpression.md) </span><span class="sxs-lookup"><span data-stu-id="29b3c-111">[Build Queries with QueryExpression](build-queries-with-queryexpression.md) </span></span>  
 <span data-ttu-id="29b3c-112">[Sample: Retrieve multiple with the QueryExpression class](sample-retrieve-multiple-queryexpression-class.md) </span><span class="sxs-lookup"><span data-stu-id="29b3c-112">[Sample: Retrieve multiple with the QueryExpression class](sample-retrieve-multiple-queryexpression-class.md) </span></span>  
 <span data-ttu-id="29b3c-113">[Use the QueryByAttribute Class](use-querybyattribute-class.md) </span><span class="sxs-lookup"><span data-stu-id="29b3c-113">[Use the QueryByAttribute Class](use-querybyattribute-class.md) </span></span>  
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 <xref:Microsoft.Xrm.Sdk.Query.QueryByAttribute>   
 <xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*>
