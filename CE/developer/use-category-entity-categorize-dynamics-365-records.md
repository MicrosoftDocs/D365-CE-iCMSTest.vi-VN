---
title: Use the Category entity to categorize Dynamics 365 for Customer Engagement records (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn about categorizing the entity records using category entity.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: ee0b24ea-c0f5-4f6a-bd66-53b7617f62cc
caps.latest.revision: 9
author: KumarVivek
ms.author: kvivek
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 8106a3c20d5a8881d3deecd1e8e3ffbc45d01053
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387468"
---
# <a name="use-the-category-entity-to-categorize-dynamics-365-for-customer-engagement-records"></a><span data-ttu-id="ea077-103">Sử dụng thực thể Thể loại để phân loại các bản ghi Dynamics 365 for Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="ea077-103">Use the Category entity to categorize Dynamics 365 for Customer Engagement records</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="ea077-104">Categorizing entity records in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] helps you tag the records so that you can easily search them.</span><span class="sxs-lookup"><span data-stu-id="ea077-104">Categorizing entity records in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] helps you tag the records so that you can easily search them.</span></span> <span data-ttu-id="ea077-105">Use the  `Category` entity to create and manage a hierarchical structure of categories in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)], and then associate entity records to one or more categories.</span><span class="sxs-lookup"><span data-stu-id="ea077-105">Use the  `Category` entity to create and manage a hierarchical structure of categories in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)], and then associate entity records to one or more categories.</span></span>  
  
> [!NOTE]
> [!INCLUDE[cc_feature_included_with_update_8_1_0_admins](../includes/cc-feature-included-with-update-8-1-0-admins.md)]  
  
 <span data-ttu-id="ea077-106">A category can have multiple child categories, but a child category can have only one parent category.</span><span class="sxs-lookup"><span data-stu-id="ea077-106">A category can have multiple child categories, but a child category can have only one parent category.</span></span> <span data-ttu-id="ea077-107">Deleting a parent `Category` record automatically deletes all its child records and entity associations.</span><span class="sxs-lookup"><span data-stu-id="ea077-107">Deleting a parent `Category` record automatically deletes all its child records and entity associations.</span></span> <span data-ttu-id="ea077-108">You define a parent category for a category using the `Category.ParentCategoryId` attribute.</span><span class="sxs-lookup"><span data-stu-id="ea077-108">You define a parent category for a category using the `Category.ParentCategoryId` attribute.</span></span>  
  
 <span data-ttu-id="ea077-109">Use the `Category.SequenceNumber` attribute to programmatically define the display order for categories in the hierarchy.</span><span class="sxs-lookup"><span data-stu-id="ea077-109">Use the `Category.SequenceNumber` attribute to programmatically define the display order for categories in the hierarchy.</span></span>  <span data-ttu-id="ea077-110">When you a add a new category using the web client, it is automatically added after the last category in the hierarchy.</span><span class="sxs-lookup"><span data-stu-id="ea077-110">When you a add a new category using the web client, it is automatically added after the last category in the hierarchy.</span></span> <span data-ttu-id="ea077-111">You can also use the `Category.CategoryNumber` attribute to programmatically set or update a number for category to help you easily distinguish a group of categories.</span><span class="sxs-lookup"><span data-stu-id="ea077-111">You can also use the `Category.CategoryNumber` attribute to programmatically set or update a number for category to help you easily distinguish a group of categories.</span></span> <span data-ttu-id="ea077-112">Category number can be set to any value programmatically, but is automatically set when you create a category using the web client based on the auto-numbering prefix specified by the administrator for categories in the web client (**Settings** > **Administration** > **Auto-Numbering** > **Categories** tab).</span><span class="sxs-lookup"><span data-stu-id="ea077-112">Category number can be set to any value programmatically, but is automatically set when you create a category using the web client based on the auto-numbering prefix specified by the administrator for categories in the web client (**Settings** > **Administration** > **Auto-Numbering** > **Categories** tab).</span></span>  
  
 <span data-ttu-id="ea077-113">You can associate `Category` records with system and custom entity records by using relationships and connections.</span><span class="sxs-lookup"><span data-stu-id="ea077-113">You can associate `Category` records with system and custom entity records by using relationships and connections.</span></span> <span data-ttu-id="ea077-114">A category record can be associated with different entity records.</span><span class="sxs-lookup"><span data-stu-id="ea077-114">A category record can be associated with different entity records.</span></span> <span data-ttu-id="ea077-115">For example, you can programmatically associate a `Category` record with an `Account`, `Contact` and `Incident` records.</span><span class="sxs-lookup"><span data-stu-id="ea077-115">For example, you can programmatically associate a `Category` record with an `Account`, `Contact` and `Incident` records.</span></span>  
  
 <span data-ttu-id="ea077-116">By default, there is a many-to-many relationship available between the `Category` and `KnowledgeArticle` entity, and the entity record associations are stored in the `KnowledgeArticlesCategories` entity.</span><span class="sxs-lookup"><span data-stu-id="ea077-116">By default, there is a many-to-many relationship available between the `Category` and `KnowledgeArticle` entity, and the entity record associations are stored in the `KnowledgeArticlesCategories` entity.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="ea077-117">In This Section</span><span class="sxs-lookup"><span data-stu-id="ea077-117">In This Section</span></span>  
 [<span data-ttu-id="ea077-118">Category Entity</span><span class="sxs-lookup"><span data-stu-id="ea077-118">Category Entity</span></span>](entities/category.md)  
  
### <a name="see-also"></a><span data-ttu-id="ea077-119">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="ea077-119">See also</span></span>  
 <span data-ttu-id="ea077-120">[Work with knowledge articles in Dynamics 365 for Customer Engagement](work-knowledge-articles.md) </span><span class="sxs-lookup"><span data-stu-id="ea077-120">[Work with knowledge articles in Dynamics 365 for Customer Engagement](work-knowledge-articles.md) </span></span>  
 [<span data-ttu-id="ea077-121">Service entities in Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="ea077-121">Service entities in Customer Engagement</span></span>](service-entities.md)
