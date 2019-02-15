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
# <a name="use-the-category-entity-to-categorize-dynamics-365-for-customer-engagement-records"></a>Sử dụng thực thể Thể loại để phân loại các bản ghi Dynamics 365 for Customer Engagement

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

Categorizing entity records in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] helps you tag the records so that you can easily search them. Use the  `Category` entity to create and manage a hierarchical structure of categories in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)], and then associate entity records to one or more categories.  
  
> [!NOTE]
> [!INCLUDE[cc_feature_included_with_update_8_1_0_admins](../includes/cc-feature-included-with-update-8-1-0-admins.md)]  
  
 A category can have multiple child categories, but a child category can have only one parent category. Deleting a parent `Category` record automatically deletes all its child records and entity associations. You define a parent category for a category using the `Category.ParentCategoryId` attribute.  
  
 Use the `Category.SequenceNumber` attribute to programmatically define the display order for categories in the hierarchy.  When you a add a new category using the web client, it is automatically added after the last category in the hierarchy. You can also use the `Category.CategoryNumber` attribute to programmatically set or update a number for category to help you easily distinguish a group of categories. Category number can be set to any value programmatically, but is automatically set when you create a category using the web client based on the auto-numbering prefix specified by the administrator for categories in the web client (**Settings** > **Administration** > **Auto-Numbering** > **Categories** tab).  
  
 You can associate `Category` records with system and custom entity records by using relationships and connections. A category record can be associated with different entity records. For example, you can programmatically associate a `Category` record with an `Account`, `Contact` and `Incident` records.  
  
 By default, there is a many-to-many relationship available between the `Category` and `KnowledgeArticle` entity, and the entity record associations are stored in the `KnowledgeArticlesCategories` entity.  
  
## <a name="in-this-section"></a>In This Section  
 [Category Entity](entities/category.md)  
  
### <a name="see-also"></a>Xem thêm  
 [Work with knowledge articles in Dynamics 365 for Customer Engagement](work-knowledge-articles.md)   
 [Service entities in Customer Engagement](service-entities.md)
