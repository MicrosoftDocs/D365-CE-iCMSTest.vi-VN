---
title: 'Sample: Use QueryExpression with a paging cookie (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: The following sample shows how to use the QueryBase) method to return the 1:N related entities of an entity along with the primary entity
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 9999be1f-59fa-41f9-baff-e02ab92e5dc4
caps.latest.revision: 9
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 3a9de2101f53b96ae37ef3baf35506b2e26a554e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385473"
---
# <a name="sample-use-queryexpression-with-a-paging-cookie"></a><span data-ttu-id="5ff2d-103">Sample: Use QueryExpression with a paging cookie</span><span class="sxs-lookup"><span data-stu-id="5ff2d-103">Sample: Use QueryExpression with a paging cookie</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="5ff2d-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="5ff2d-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span></span> <span data-ttu-id="5ff2d-105">Download the complete sample from [Sample: Work with Queries](https://code.msdn.microsoft.com/Sample-Work-with-Queries-8265a78e).</span><span class="sxs-lookup"><span data-stu-id="5ff2d-105">Download the complete sample from [Sample: Work with Queries](https://code.msdn.microsoft.com/Sample-Work-with-Queries-8265a78e).</span></span>   

## <a name="prerequisites"></a><span data-ttu-id="5ff2d-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="5ff2d-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
   
## <a name="requirements"></a><span data-ttu-id="5ff2d-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="5ff2d-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
 
## <a name="example"></a><span data-ttu-id="5ff2d-108">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="5ff2d-108">Example</span></span>  
 <span data-ttu-id="5ff2d-109">This sample shows how to use the paging cookie in a QueryExpression query to retrieve successive pages of query results.</span><span class="sxs-lookup"><span data-stu-id="5ff2d-109">This sample shows how to use the paging cookie in a QueryExpression query to retrieve successive pages of query results.</span></span> <span data-ttu-id="5ff2d-110">It uses the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*></span><span class="sxs-lookup"><span data-stu-id="5ff2d-110">It uses the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*></span></span> <span data-ttu-id="5ff2d-111">method.</span><span class="sxs-lookup"><span data-stu-id="5ff2d-111">method.</span></span>  
  
 [!code-csharp[Query#QueryExpressionPagingWithCookie](../../snippets/csharp/CRMV8/query/cs/queryexpressionpagingwithcookie.cs#queryexpressionpagingwithcookie)]  
  
### <a name="see-also"></a><span data-ttu-id="5ff2d-112">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="5ff2d-112">See also</span></span>  
 <span data-ttu-id="5ff2d-113">[Page large result sets with QueryExpression](page-large-result-sets-with-queryexpression.md) </span><span class="sxs-lookup"><span data-stu-id="5ff2d-113">[Page large result sets with QueryExpression](page-large-result-sets-with-queryexpression.md) </span></span>  
 <span data-ttu-id="5ff2d-114">[Build Queries with QueryExpression](build-queries-with-queryexpression.md) </span><span class="sxs-lookup"><span data-stu-id="5ff2d-114">[Build Queries with QueryExpression](build-queries-with-queryexpression.md) </span></span>  
 <span data-ttu-id="5ff2d-115">[Sample: Convert queries between Fetch and QueryExpression](sample-convert-queries-fetch-queryexpression.md) </span><span class="sxs-lookup"><span data-stu-id="5ff2d-115">[Sample: Convert queries between Fetch and QueryExpression](sample-convert-queries-fetch-queryexpression.md) </span></span>  
 <span data-ttu-id="5ff2d-116">[Sample: CrmServiceHelper Class](helper-code-serverconnection-class.md) </span><span class="sxs-lookup"><span data-stu-id="5ff2d-116">[Sample: CrmServiceHelper Class](helper-code-serverconnection-class.md) </span></span>  
<xref:Microsoft.Xrm.Sdk.IOrganizationService>
