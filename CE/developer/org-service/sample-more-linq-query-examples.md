---
title: 'Sample: More LINQ query examples (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: This sample shows how to create .NET Language-Integrated Query (LINQ) queries
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: d5e5ec45-6465-4281-9e14-5f213a8c3bde
caps.latest.revision: 22
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 0b35a736e388143f857a6f6a602b8a53f9270bad
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385564"
---
# <a name="sample-more-linq-query-examples"></a><span data-ttu-id="f1fba-103">Sample: More LINQ query examples</span><span class="sxs-lookup"><span data-stu-id="f1fba-103">Sample: More LINQ query examples</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="f1fba-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="f1fba-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span></span> <span data-ttu-id="f1fba-105">Download the complete sample from [Sample: Work with Queries](https://code.msdn.microsoft.com/Sample-Work-with-Queries-8265a78e).</span><span class="sxs-lookup"><span data-stu-id="f1fba-105">Download the complete sample from [Sample: Work with Queries](https://code.msdn.microsoft.com/Sample-Work-with-Queries-8265a78e).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="f1fba-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="f1fba-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="f1fba-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="f1fba-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="f1fba-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="f1fba-108">Demonstrates</span></span>  
 <span data-ttu-id="f1fba-109">This sample shows how to create [!INCLUDE[pn_LINQ](../../includes/pn-linq.md)] queries.</span><span class="sxs-lookup"><span data-stu-id="f1fba-109">This sample shows how to create [!INCLUDE[pn_LINQ](../../includes/pn-linq.md)] queries.</span></span> <span data-ttu-id="f1fba-110">The following queries are demonstrated:</span><span class="sxs-lookup"><span data-stu-id="f1fba-110">The following queries are demonstrated:</span></span>  
  
-   <span data-ttu-id="f1fba-111">Retrieve records with `Skip`/`Take` record paging.</span><span class="sxs-lookup"><span data-stu-id="f1fba-111">Retrieve records with `Skip`/`Take` record paging.</span></span>  
  
-   <span data-ttu-id="f1fba-112">Use `orderBy` to order items retrieved.</span><span class="sxs-lookup"><span data-stu-id="f1fba-112">Use `orderBy` to order items retrieved.</span></span>  
  
-   <span data-ttu-id="f1fba-113">Filter multiple entities using LINQ.</span><span class="sxs-lookup"><span data-stu-id="f1fba-113">Filter multiple entities using LINQ.</span></span>  
  
-   <span data-ttu-id="f1fba-114">Build a complex query with LINQ.</span><span class="sxs-lookup"><span data-stu-id="f1fba-114">Build a complex query with LINQ.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f1fba-115">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="f1fba-115">Example</span></span>  
 [!code-csharp[query#UseLinqQuery](../../snippets/csharp/CRMV8/query/cs/uselinqquery.cs#uselinqquery)]  
  
### <a name="see-also"></a><span data-ttu-id="f1fba-116">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="f1fba-116">See also</span></span>  
 <span data-ttu-id="f1fba-117">[Build Queries with LINQ (.NET Language-Integrated Query)](build-queries-with-linq-net-language-integrated-query.md) </span><span class="sxs-lookup"><span data-stu-id="f1fba-117">[Build Queries with LINQ (.NET Language-Integrated Query)](build-queries-with-linq-net-language-integrated-query.md) </span></span>  
 <span data-ttu-id="f1fba-118">[Sample: Use LINQ with Late Binding](sample-create-linq-query-late-binding.md) </span><span class="sxs-lookup"><span data-stu-id="f1fba-118">[Sample: Use LINQ with Late Binding](sample-create-linq-query-late-binding.md) </span></span>  
 <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext>
