---
title: 'Sample: Use FetchXML with a paging cookie (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: This sample shows how to use the paging cookie in a FetchXML query to retrieve successive pages of query results. It uses the IOrganizationService. QueryBase) method
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
- retrieving successive pages of query results by using FetchXML sample
- FetchXML queries, samples
- using FetchXML with a paging cookie sample
- building queries with FetchXML, samples
- sample for retrieving successive pages of query results by using FetchXML
- sample for using FetchXML with a paging cookie
ms.assetid: 1d8acb4e-f8c3-478a-ae4f-e462973cd63d
caps.latest.revision: 27
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ef0c1f82033c2070dff459bdc538519e96c36c35
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388018"
---
# <a name="sample-use-fetchxml-with-a-paging-cookie"></a><span data-ttu-id="1aeb2-105">Sample: Use FetchXML with a paging cookie</span><span class="sxs-lookup"><span data-stu-id="1aeb2-105">Sample: Use FetchXML with a paging cookie</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="1aeb2-106">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="1aeb2-106">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span></span> <span data-ttu-id="1aeb2-107">Download the complete sample here [Sample: Work with Queries](https://code.msdn.microsoft.com/Sample-Work-with-Queries-8265a78e)</span><span class="sxs-lookup"><span data-stu-id="1aeb2-107">Download the complete sample here [Sample: Work with Queries](https://code.msdn.microsoft.com/Sample-Work-with-Queries-8265a78e)</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="1aeb2-108">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="1aeb2-108">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="1aeb2-109">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="1aeb2-109">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="example"></a><span data-ttu-id="1aeb2-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="1aeb2-110">Example</span></span>  
 <span data-ttu-id="1aeb2-111">This sample shows how to use the paging cookie in a FetchXML query to retrieve successive pages of query results.</span><span class="sxs-lookup"><span data-stu-id="1aeb2-111">This sample shows how to use the paging cookie in a FetchXML query to retrieve successive pages of query results.</span></span> <span data-ttu-id="1aeb2-112">It uses the<xref:Microsoft.Xrm.Sdk.IOrganizationService>.</span><span class="sxs-lookup"><span data-stu-id="1aeb2-112">It uses the<xref:Microsoft.Xrm.Sdk.IOrganizationService>.</span></span> <span data-ttu-id="1aeb2-113"><xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*> method.</span><span class="sxs-lookup"><span data-stu-id="1aeb2-113"><xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*> method.</span></span>  
  
 [!code-csharp[Query#FetchPagingWithCookie](../../snippets/csharp/CRMV8/query/cs/fetchpagingwithcookie.cs#fetchpagingwithcookie)]  
  
### <a name="see-also"></a><span data-ttu-id="1aeb2-114">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="1aeb2-114">See also</span></span>  
 <span data-ttu-id="1aeb2-115">[Build Queries with FetchXML](build-queries-fetchxml.md) </span><span class="sxs-lookup"><span data-stu-id="1aeb2-115">[Build Queries with FetchXML](build-queries-fetchxml.md) </span></span>  
 <span data-ttu-id="1aeb2-116">[Sample: Convert queries between Fetch and QueryExpression](sample-convert-queries-fetch-queryexpression.md) </span><span class="sxs-lookup"><span data-stu-id="1aeb2-116">[Sample: Convert queries between Fetch and QueryExpression](sample-convert-queries-fetch-queryexpression.md) </span></span>  
 <span data-ttu-id="1aeb2-117">[Sample: CrmServiceHelper Class](helper-code-serverconnection-class.md) </span><span class="sxs-lookup"><span data-stu-id="1aeb2-117">[Sample: CrmServiceHelper Class](helper-code-serverconnection-class.md) </span></span>  
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 <xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*>   
 <span data-ttu-id="1aeb2-118">[Using FetchXML Aggregration](use-fetchxml-aggregation.md) </span><span class="sxs-lookup"><span data-stu-id="1aeb2-118">[Using FetchXML Aggregration](use-fetchxml-aggregation.md) </span></span>  
 [<span data-ttu-id="1aeb2-119">Using FetchXML</span><span class="sxs-lookup"><span data-stu-id="1aeb2-119">Using FetchXML</span></span>](use-fetchxml-construct-query.md)
