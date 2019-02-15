---
title: Use late-bound entity class with a LINQ query (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Read how you can use late binding with .NET Language-Integrated Query (LINQ) queries
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- LINQ queries
- LINQ queries, using late binding in join or left join clauses
- LINQ queries, using late-bound entity classes with LINQ queries
- LINQ queries
- LINQ queries, using late binding with the not equals operator
- using late-bound entity classes with LINQ queries
- LINQ queries, using late binding with the Contains or GetAttributeValue method
ms.assetid: 675f8ad0-e5f7-4fcb-a702-40962117f4cc
caps.latest.revision: 32
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ff26e44686a6b236e10d7bb9660ad57f492c8682
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387800"
---
# <a name="use-late-bound-entity-class-with-a-linq-query"></a><span data-ttu-id="b5c0c-103">Use late-bound entity class with a LINQ query</span><span class="sxs-lookup"><span data-stu-id="b5c0c-103">Use late-bound entity class with a LINQ query</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="b5c0c-104">In [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement, you can use late binding with [!INCLUDE[pn_LINQ](../../includes/pn-linq.md)] queries.</span><span class="sxs-lookup"><span data-stu-id="b5c0c-104">In [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement, you can use late binding with [!INCLUDE[pn_LINQ](../../includes/pn-linq.md)] queries.</span></span> <span data-ttu-id="b5c0c-105">Late binding uses the attribute logical name, and is resolved at runtime.</span><span class="sxs-lookup"><span data-stu-id="b5c0c-105">Late binding uses the attribute logical name, and is resolved at runtime.</span></span>  
  
<a name="usinglatebindingjoin"></a>   
## <a name="using-late-binding-in-a-join-clause"></a><span data-ttu-id="b5c0c-106">Using late binding in a join clause</span><span class="sxs-lookup"><span data-stu-id="b5c0c-106">Using late binding in a join clause</span></span>  
 <span data-ttu-id="b5c0c-107">The following examples show how to use late binding in the `join` clause of a LINQ query.</span><span class="sxs-lookup"><span data-stu-id="b5c0c-107">The following examples show how to use late binding in the `join` clause of a LINQ query.</span></span>  
  
 <span data-ttu-id="b5c0c-108">Retrieve the full name of the contact that represents the primary contact for an account and the account name.</span><span class="sxs-lookup"><span data-stu-id="b5c0c-108">Retrieve the full name of the contact that represents the primary contact for an account and the account name.</span></span>  
  
 [!code-csharp[Query#LINQExamples6](../../snippets/csharp/CRMV8/query/cs/linqexamples6.cs#linqexamples6)]  

 <span data-ttu-id="b5c0c-109">Retrieve Contact, Account and Lead data where the Lead was the originating Lead and the Contact’s last name is not “Parker”</span><span class="sxs-lookup"><span data-stu-id="b5c0c-109">Retrieve Contact, Account and Lead data where the Lead was the originating Lead and the Contact’s last name is not “Parker”</span></span>  
  
 [!code-csharp[Query#linqexamples40](../../snippets/csharp/CRMV8/query/cs/linqexamples40.cs#linqexamples40)]  

<a name="Usinglatebindingleft"></a>   
## <a name="using-late-binding-in-a-left-join"></a><span data-ttu-id="b5c0c-110">Using late binding in a left join</span><span class="sxs-lookup"><span data-stu-id="b5c0c-110">Using late binding in a left join</span></span>  
 <span data-ttu-id="b5c0c-111">The following example shows how to retrieve a list of Contact and Account information using a left join.</span><span class="sxs-lookup"><span data-stu-id="b5c0c-111">The following example shows how to retrieve a list of Contact and Account information using a left join.</span></span> <span data-ttu-id="b5c0c-112">A left join is designed to return parents with and without children from two sources.</span><span class="sxs-lookup"><span data-stu-id="b5c0c-112">A left join is designed to return parents with and without children from two sources.</span></span> <span data-ttu-id="b5c0c-113">There is a correlation between parent and child, but no child may actually exist.</span><span class="sxs-lookup"><span data-stu-id="b5c0c-113">There is a correlation between parent and child, but no child may actually exist.</span></span>  
  
 [!code-csharp[Query#linqexamples13](../../snippets/csharp/CRMV8/query/cs/linqexamples13.cs#linqexamples13)]  
  
<a name="contains"></a>   
## <a name="using-late-binding-and-the-contains-method"></a><span data-ttu-id="b5c0c-114">Using late binding and the Contains method</span><span class="sxs-lookup"><span data-stu-id="b5c0c-114">Using late binding and the Contains method</span></span>  
 <span data-ttu-id="b5c0c-115">The following example shows how to use late binding with the `Contains` method in a LINQ query.</span><span class="sxs-lookup"><span data-stu-id="b5c0c-115">The following example shows how to use late binding with the `Contains` method in a LINQ query.</span></span>  
  
 [!code-csharp[Query#linqexamples25](../../snippets/csharp/CRMV8/query/cs/linqexamples25.cs#linqexamples25)]  
  
<a name="notequals"></a>   
## <a name="using-late-binding-and-not-equals-operator"></a><span data-ttu-id="b5c0c-116">Using late binding and not equals operator</span><span class="sxs-lookup"><span data-stu-id="b5c0c-116">Using late binding and not equals operator</span></span>  
 <span data-ttu-id="b5c0c-117">The following example shows use of the not equals operator.</span><span class="sxs-lookup"><span data-stu-id="b5c0c-117">The following example shows use of the not equals operator.</span></span>  
  
 [!code-csharp[Query#linqexamples19](../../snippets/csharp/CRMV8/query/cs/linqexamples19.cs#linqexamples19)]  
  
<a name="getattribute"></a>   
## <a name="using-the-getattributevalue-method"></a><span data-ttu-id="b5c0c-118">Using the GetAttributeValue method</span><span class="sxs-lookup"><span data-stu-id="b5c0c-118">Using the GetAttributeValue method</span></span>  
 <span data-ttu-id="b5c0c-119">The following example shows how to retrieve Contact information using the `GetAttributeValue` method.</span><span class="sxs-lookup"><span data-stu-id="b5c0c-119">The following example shows how to retrieve Contact information using the `GetAttributeValue` method.</span></span>  
  
 [!code-csharp[Query#linqexamples34](../../snippets/csharp/CRMV8/query/cs/linqexamples34.cs#linqexamples34)]  
  
### <a name="see-also"></a><span data-ttu-id="b5c0c-120">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="b5c0c-120">See also</span></span>  
 <span data-ttu-id="b5c0c-121">[Build Queries with LINQ (.NET Language-Integrated Query)](build-queries-with-linq-net-language-integrated-query.md) </span><span class="sxs-lookup"><span data-stu-id="b5c0c-121">[Build Queries with LINQ (.NET Language-Integrated Query)](build-queries-with-linq-net-language-integrated-query.md) </span></span>  
 <span data-ttu-id="b5c0c-122">[Order Results Using Entity Attributes with LINQ](order-results-entity-attributes-linq.md) </span><span class="sxs-lookup"><span data-stu-id="b5c0c-122">[Order Results Using Entity Attributes with LINQ](order-results-entity-attributes-linq.md) </span></span>  
 <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext.CreateQuery``1>
