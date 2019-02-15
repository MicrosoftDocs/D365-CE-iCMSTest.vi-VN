---
title: 'Sample: Create a LINQ query with late binding (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: This sample shows how to create .NET Language-Integrated Query (LINQ) queries using late-bound entities
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
- late-bound entity classes, creating LINQ queries that use late-bound entities sample
- LINQ query examples and samples, creating LINQ queries that use late-bound entities sample
- creating LINQ queries that use late-bound entities sample
- sample for using LINQ with late binding
- late binding with LINQ sample
- LINQ query examples and samples, using LINQ with late binding sample
- sample for creating LINQ queries that use late-bound entities
ms.assetid: b0b5a5f6-03b9-4c42-9394-7fa6d27ee509
caps.latest.revision: 19
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 34b141eb6c85f3a9abf295d642a88c70ac410680
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387070"
---
# <a name="sample-create-a-linq-query-with-late-binding"></a><span data-ttu-id="4f451-103">Sample: Create a LINQ query with late binding</span><span class="sxs-lookup"><span data-stu-id="4f451-103">Sample: Create a LINQ query with late binding</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="4f451-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="4f451-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span></span> <span data-ttu-id="4f451-105">Download the complete sample from [Sample: Work with Queries](https://code.msdn.microsoft.com/Sample-Work-with-Queries-8265a78e).</span><span class="sxs-lookup"><span data-stu-id="4f451-105">Download the complete sample from [Sample: Work with Queries](https://code.msdn.microsoft.com/Sample-Work-with-Queries-8265a78e).</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="4f451-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="4f451-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="4f451-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="4f451-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="4f451-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="4f451-108">Demonstrates</span></span>  
 <span data-ttu-id="4f451-109">This sample shows how to create [!INCLUDE[pn_LINQ](../../includes/pn-linq.md)] queries using late-bound entities.</span><span class="sxs-lookup"><span data-stu-id="4f451-109">This sample shows how to create [!INCLUDE[pn_LINQ](../../includes/pn-linq.md)] queries using late-bound entities.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4f451-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="4f451-110">Example</span></span>  
 [!code-csharp[query#UseLinqWithDotNetDataServicesDE](../../snippets/csharp/CRMV8/query/cs/uselinqwithdotnetdataservicesde.cs#uselinqwithdotnetdataservicesde)]  
  
### <a name="see-also"></a><span data-ttu-id="4f451-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="4f451-111">See also</span></span>  
 <span data-ttu-id="4f451-112">[Build Queries with LINQ (.NET Language-Integrated Query)](build-queries-with-linq-net-language-integrated-query.md) </span><span class="sxs-lookup"><span data-stu-id="4f451-112">[Build Queries with LINQ (.NET Language-Integrated Query)](build-queries-with-linq-net-language-integrated-query.md) </span></span>  
 <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext>     
 <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext.CreateQuery(System.String)>
