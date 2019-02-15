---
title: Create and retrieve entity relationships (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: The topic shows how to create and retrieve entity relationships.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
- Dynamics 365 for Customer Engagement (on-premises)
- Dynamics CRM 2016
- Dynamics CRM Online
ms.assetid: d10c5399-7e79-413c-9b8c-9e4f402fc167
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 2200bb3e6a4d1d1e4f52c2adf67ba8cbbf391c77
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388552"
---
# <a name="create-and-retrieve-entity-relationships"></a><span data-ttu-id="c3624-103">Create and retrieve entity relationships</span><span class="sxs-lookup"><span data-stu-id="c3624-103">Create and retrieve entity relationships</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="c3624-104">This topic shows how to create and retrieve entity relationships.</span><span class="sxs-lookup"><span data-stu-id="c3624-104">This topic shows how to create and retrieve entity relationships.</span></span>  
  
<a name="BKMK_Create1NEntityRelationship"></a>   
## <a name="create-a-1n-entity-relationship"></a><span data-ttu-id="c3624-105">Create a 1:N entity relationship</span><span class="sxs-lookup"><span data-stu-id="c3624-105">Create a 1:N entity relationship</span></span>  
 <span data-ttu-id="c3624-106">The following sample uses the [EligibleCreateOneToManyRelationship](#eligiblecreateonetomanyrelationship) method to verify that the `Account` and `Campaign` entities can participate in a 1:N entity relationship and then creates the entity relationship by using <xref:Microsoft.Xrm.Sdk.Messages.CreateOneToManyRequest>.</span><span class="sxs-lookup"><span data-stu-id="c3624-106">The following sample uses the [EligibleCreateOneToManyRelationship](#eligiblecreateonetomanyrelationship) method to verify that the `Account` and `Campaign` entities can participate in a 1:N entity relationship and then creates the entity relationship by using <xref:Microsoft.Xrm.Sdk.Messages.CreateOneToManyRequest>.</span></span>  
  
 [!code-csharp[Relationships#WorkWithRelationships1](../../snippets/csharp/CRMV8/relationships/cs/workwithrelationships1.cs#workwithrelationships1)]  
  
<a name="BKMK_EligibleCreateOneToManyRelationship"></a>   

### <a name="eligiblecreateonetomanyrelationship"></a><span data-ttu-id="c3624-107">EligibleCreateOneToManyRelationship</span><span class="sxs-lookup"><span data-stu-id="c3624-107">EligibleCreateOneToManyRelationship</span></span>  

 <span data-ttu-id="c3624-108">The following sample creates a `EligibleCreateOneToManyRelationship` method that uses <xref:Microsoft.Xrm.Sdk.Messages.CanBeReferencedRequest> and <xref:Microsoft.Xrm.Sdk.Messages.CanBeReferencingRequest> to verify whether two entities can participate in a 1:N entity relationship.</span><span class="sxs-lookup"><span data-stu-id="c3624-108">The following sample creates a `EligibleCreateOneToManyRelationship` method that uses <xref:Microsoft.Xrm.Sdk.Messages.CanBeReferencedRequest> and <xref:Microsoft.Xrm.Sdk.Messages.CanBeReferencingRequest> to verify whether two entities can participate in a 1:N entity relationship.</span></span>  
  
 [!code-csharp[Relationships#WorkWithRelationships4](../../snippets/csharp/CRMV8/relationships/cs/workwithrelationships4.cs#workwithrelationships4)]  
  
<a name="BKMK_CreateNNEntityRelationship"></a>   

## <a name="create-an-nn-entity-relationship"></a><span data-ttu-id="c3624-109">Create an N:N entity relationship</span><span class="sxs-lookup"><span data-stu-id="c3624-109">Create an N:N entity relationship</span></span>  

 <span data-ttu-id="c3624-110">The following sample uses a [EligibleCreateManyToManyRelationship](create-retrieve-entity-relationships.md#BKMK_EligibleCreateManyToManyRelationship) method to verify that the `Account` and `Campaign` entities can participate in a N:N entity relationship and then creates the entity relationship by using <xref:Microsoft.Xrm.Sdk.Messages.CreateManyToManyRequest>.</span><span class="sxs-lookup"><span data-stu-id="c3624-110">The following sample uses a [EligibleCreateManyToManyRelationship](create-retrieve-entity-relationships.md#BKMK_EligibleCreateManyToManyRelationship) method to verify that the `Account` and `Campaign` entities can participate in a N:N entity relationship and then creates the entity relationship by using <xref:Microsoft.Xrm.Sdk.Messages.CreateManyToManyRequest>.</span></span>  
  
 [!code-csharp[Relationships#WorkWithRelationships2](../../snippets/csharp/CRMV8/relationships/cs/workwithrelationships2.cs#workwithrelationships2)]  
  
<a name="BKMK_EligibleCreateManyToManyRelationship"></a>   

### <a name="eligiblecreatemanytomanyrelationship"></a><span data-ttu-id="c3624-111">EligibleCreateManyToManyRelationship</span><span class="sxs-lookup"><span data-stu-id="c3624-111">EligibleCreateManyToManyRelationship</span></span>  

 <span data-ttu-id="c3624-112">The following sample creates a `EligibleCreateManyToManyRelationship` method that uses <xref:Microsoft.Xrm.Sdk.Messages.CanManyToManyRequest> to verify whether an entity can participate in a N:N entity relationship.</span><span class="sxs-lookup"><span data-stu-id="c3624-112">The following sample creates a `EligibleCreateManyToManyRelationship` method that uses <xref:Microsoft.Xrm.Sdk.Messages.CanManyToManyRequest> to verify whether an entity can participate in a N:N entity relationship.</span></span>  
  
 [!code-csharp[Relationships#WorkWithRelationships3](../../snippets/csharp/CRMV8/relationships/cs/workwithrelationships3.cs#workwithrelationships3)]  
  
<a name="BKMK_RetrieveEntityRelationships"></a>   
## <a name="retrieve-entity-relationships"></a><span data-ttu-id="c3624-113">Retrieve entity relationships</span><span class="sxs-lookup"><span data-stu-id="c3624-113">Retrieve entity relationships</span></span>  
 <span data-ttu-id="c3624-114">The following sample retrieves the two entity relationships previously created using <xref:Microsoft.Xrm.Sdk.Messages.RetrieveRelationshipRequest>.</span><span class="sxs-lookup"><span data-stu-id="c3624-114">The following sample retrieves the two entity relationships previously created using <xref:Microsoft.Xrm.Sdk.Messages.RetrieveRelationshipRequest>.</span></span> <span data-ttu-id="c3624-115">The first example uses the `MetadataId` and the second uses the `Name`.</span><span class="sxs-lookup"><span data-stu-id="c3624-115">The first example uses the `MetadataId` and the second uses the `Name`.</span></span>  
  
 [!code-csharp[relationships#WorkWithRelationships.RetrieveRelationship](../../snippets/csharp/CRMV8/relationships/cs/workwithrelationships.retrieverelationship.cs#workwithrelationships.retrieverelationship)]  
  
### <a name="see-also"></a><span data-ttu-id="c3624-116">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="c3624-116">See Also</span></span>  
 <span data-ttu-id="c3624-117">[Customize entity relationship metadata](../customize-entity-relationship-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="c3624-117">[Customize entity relationship metadata](../customize-entity-relationship-metadata.md) </span></span>  
 <span data-ttu-id="c3624-118">[Entity Relationship Metadata Messages](../entity-relationship-metadata-messages.md) </span><span class="sxs-lookup"><span data-stu-id="c3624-118">[Entity Relationship Metadata Messages](../entity-relationship-metadata-messages.md) </span></span>  
 [<span data-ttu-id="c3624-119">Sample: Create Entity Relationships</span><span class="sxs-lookup"><span data-stu-id="c3624-119">Sample: Create Entity Relationships</span></span>](sample-create-retrieve-entity-relationships.md)
