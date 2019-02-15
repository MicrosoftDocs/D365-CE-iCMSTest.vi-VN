---
title: Build queries with LINQ (.NET language-integrated query) (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Read how to use .NET Language-Integrated Query (LINQ) to write queries in Dynamics 365 for Customer Engagement (online & on-premises)
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 1c2b2e80-e85d-422c-a3f4-f48895d9c70b
caps.latest.revision: 27
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: eaf71523ee9c6ec95c8736598b713b38a50a1256
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387843"
---
# <a name="build-queries-with-linq-net-language-integrated-query"></a><span data-ttu-id="255d5-103">Build queries with LINQ (.NET language-integrated query)</span><span class="sxs-lookup"><span data-stu-id="255d5-103">Build queries with LINQ (.NET language-integrated query)</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="255d5-104">You can use [!INCLUDE[pn_LINQ](../../includes/pn-linq.md)] to write queries in [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="255d5-104">You can use [!INCLUDE[pn_LINQ](../../includes/pn-linq.md)] to write queries in [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span></span> <span data-ttu-id="255d5-105">You can use the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext> class or a deriving class created by the [!INCLUDE[sdk_CodeGenUtility](../../includes/sdk-codegenutility.md)] tool to write [LINQ](https://msdn.microsoft.com/library/bb397897.aspx) queries that access the SOAP endpoint (Organization.svc).</span><span class="sxs-lookup"><span data-stu-id="255d5-105">You can use the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext> class or a deriving class created by the [!INCLUDE[sdk_CodeGenUtility](../../includes/sdk-codegenutility.md)] tool to write [LINQ](https://msdn.microsoft.com/library/bb397897.aspx) queries that access the SOAP endpoint (Organization.svc).</span></span> <span data-ttu-id="255d5-106">The <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext> class contains an underlying LINQ query provider that translates LINQ queries from [!INCLUDE[pn_MS_Visual_C#](../../includes/pn-ms-visual-csharp.md)] or [!INCLUDE[pn_Visual_Basic](../../includes/pn-visual-basic.md)] syntax into the query API used by [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="255d5-106">The <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext> class contains an underlying LINQ query provider that translates LINQ queries from [!INCLUDE[pn_MS_Visual_C#](../../includes/pn-ms-visual-csharp.md)] or [!INCLUDE[pn_Visual_Basic](../../includes/pn-visual-basic.md)] syntax into the query API used by [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps.</span></span>  
  
 <span data-ttu-id="255d5-107">When you use early-bound programming classes you can generate a class derived from the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext> class if you specify the name of the class using the **servicecontextname** parameter when using the Code Generation Tool (CrmSvcUtil.exe).</span><span class="sxs-lookup"><span data-stu-id="255d5-107">When you use early-bound programming classes you can generate a class derived from the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext> class if you specify the name of the class using the **servicecontextname** parameter when using the Code Generation Tool (CrmSvcUtil.exe).</span></span> <span data-ttu-id="255d5-108">Use of this class allows for referencing an [IQueryable](https://msdn.microsoft.com/library/system.linq.iqueryable.aspx) entity set using the pattern `<entity schema name>+Set`, for example **AccountSet** to reference the collection of `Account` entity records.</span><span class="sxs-lookup"><span data-stu-id="255d5-108">Use of this class allows for referencing an [IQueryable](https://msdn.microsoft.com/library/system.linq.iqueryable.aspx) entity set using the pattern `<entity schema name>+Set`, for example **AccountSet** to reference the collection of `Account` entity records.</span></span> <span data-ttu-id="255d5-109">All samples in the [!INCLUDE [pn-sdk](../../includes/pn-sdk.md)] use **ServiceContext** as the name for this class but your code may use a different name.</span><span class="sxs-lookup"><span data-stu-id="255d5-109">All samples in the [!INCLUDE [pn-sdk](../../includes/pn-sdk.md)] use **ServiceContext** as the name for this class but your code may use a different name.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="255d5-110">[Create Early Bound Entity Classes with the Code Generation Tool (CrmSvcUtil.exe)](create-early-bound-entity-classes-code-generation-tool.md)</span><span class="sxs-lookup"><span data-stu-id="255d5-110">[Create Early Bound Entity Classes with the Code Generation Tool (CrmSvcUtil.exe)](create-early-bound-entity-classes-code-generation-tool.md)</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="255d5-111">In This Section</span><span class="sxs-lookup"><span data-stu-id="255d5-111">In This Section</span></span>  
 [<span data-ttu-id="255d5-112">Use LINQ to Construct a Query</span><span class="sxs-lookup"><span data-stu-id="255d5-112">Use LINQ to Construct a Query</span></span>](use-linq-construct-query.md)  
  
 [<span data-ttu-id="255d5-113">Use Late-Bound Entity Class with a LINQ Query</span><span class="sxs-lookup"><span data-stu-id="255d5-113">Use Late-Bound Entity Class with a LINQ Query</span></span>](use-late-bound-entity-class-linq-query.md)  
  
 [<span data-ttu-id="255d5-114">Use Entity Lookup Attributes with LINQ</span><span class="sxs-lookup"><span data-stu-id="255d5-114">Use Entity Lookup Attributes with LINQ</span></span>](order-results-entity-attributes-linq.md)  
  
 [<span data-ttu-id="255d5-115">Order Results Using Entity Attributes with LINQ</span><span class="sxs-lookup"><span data-stu-id="255d5-115">Order Results Using Entity Attributes with LINQ</span></span>](order-results-entity-attributes-linq.md)  
  
 [<span data-ttu-id="255d5-116">Paging Large Result Sets with LINQ</span><span class="sxs-lookup"><span data-stu-id="255d5-116">Paging Large Result Sets with LINQ</span></span>](page-large-result-sets-linq.md)  
  
 [<span data-ttu-id="255d5-117">LINQ Query Examples</span><span class="sxs-lookup"><span data-stu-id="255d5-117">LINQ Query Examples</span></span>](linq-query-examples.md)  
  
 [<span data-ttu-id="255d5-118">Sample: Create a LINQ Query</span><span class="sxs-lookup"><span data-stu-id="255d5-118">Sample: Create a LINQ Query</span></span>](sample-create-linq-query.md)  
  
 [<span data-ttu-id="255d5-119">Sample: LINQ Query Examples</span><span class="sxs-lookup"><span data-stu-id="255d5-119">Sample: LINQ Query Examples</span></span>](sample-complex-linq-queries.md)  
  
 [<span data-ttu-id="255d5-120">Sample: RetrieveMultiple With Condition Operators Using LINQ</span><span class="sxs-lookup"><span data-stu-id="255d5-120">Sample: RetrieveMultiple With Condition Operators Using LINQ</span></span>](sample-retrieve-multiple-with-condition-operators-using-linq.md)  
  
 [<span data-ttu-id="255d5-121">Sample: More LINQ Query Examples</span><span class="sxs-lookup"><span data-stu-id="255d5-121">Sample: More LINQ Query Examples</span></span>](sample-more-linq-query-examples.md)  
  
 [<span data-ttu-id="255d5-122">Sample: Use LINQ with Late Binding</span><span class="sxs-lookup"><span data-stu-id="255d5-122">Sample: Use LINQ with Late Binding</span></span>](sample-create-linq-query-late-binding.md)
