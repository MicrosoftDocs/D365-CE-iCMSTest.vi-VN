---
title: UserQuery (saved view) entity (Developer Guide for Dynamics 365 for Customer Engagement apps)| MicrosoftDocs
description: Learn about saved queries which are business entities that define the parameters and criteria of a database search.
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
- saved view and saved queries, definitions
- user query (saved view) entity, as FetchXML statements
- user query (saved view) entity, Advanced Find section of Microsoft Dynamics CRM
- user query (saved view) entity, about
- saved view and saved queries, database searches
- user query (saved view) entity, import and export capabilities
- saved view and saved queries
ms.assetid: b40b50ae-70f6-4868-a1ed-f50414af1c6b
caps.latest.revision: 13
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 05dfb234de3864b51b03e2daabecc2475c5ba941
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386581"
---
# <a name="userquery-saved-view-entity"></a><span data-ttu-id="baae0-103">UserQuery (saved view) entity</span><span class="sxs-lookup"><span data-stu-id="baae0-103">UserQuery (saved view) entity</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="baae0-104">Saved queries are business entities that define the parameters and criteria of a [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] database search.</span><span class="sxs-lookup"><span data-stu-id="baae0-104">Saved queries are business entities that define the parameters and criteria of a [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] database search.</span></span> <span data-ttu-id="baae0-105">Saved queries support cross-entity searches.</span><span class="sxs-lookup"><span data-stu-id="baae0-105">Saved queries support cross-entity searches.</span></span> <span data-ttu-id="baae0-106">In [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] there are two entities available for queries against the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] database.</span><span class="sxs-lookup"><span data-stu-id="baae0-106">In [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] there are two entities available for queries against the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] database.</span></span>  
  
 <span data-ttu-id="baae0-107">A *user query*, called a saved view in the application, is owned by an individual user, can be assigned and shared with other users, and can be viewed by other users depending on the query's access privileges.</span><span class="sxs-lookup"><span data-stu-id="baae0-107">A *user query*, called a saved view in the application, is owned by an individual user, can be assigned and shared with other users, and can be viewed by other users depending on the query's access privileges.</span></span> <span data-ttu-id="baae0-108">This is appropriate for frequently used queries that span entity types and queries that perform aggregation.</span><span class="sxs-lookup"><span data-stu-id="baae0-108">This is appropriate for frequently used queries that span entity types and queries that perform aggregation.</span></span> <span data-ttu-id="baae0-109">A *saved query*, called a view in the application, is owned by an organization making it visible to all users in the organization.</span><span class="sxs-lookup"><span data-stu-id="baae0-109">A *saved query*, called a view in the application, is owned by an organization making it visible to all users in the organization.</span></span> <span data-ttu-id="baae0-110">Saved queries (views) are used for both views defined for an entity and for filters and templates for [!INCLUDE[pn_crm_for_outlook_full](../includes/pn-crm-for-outlook-full.md)].</span><span class="sxs-lookup"><span data-stu-id="baae0-110">Saved queries (views) are used for both views defined for an entity and for filters and templates for [!INCLUDE[pn_crm_for_outlook_full](../includes/pn-crm-for-outlook-full.md)].</span></span> <span data-ttu-id="baae0-111">For more information about saved views, see [Customize Entity Views in Dynamics 365 for Customer Engagement apps](customize-dev/customize-entity-views.md) and [Offline and Outlook Filters and Templates](outlook-client/offline-outlook-filters-templates.md).</span><span class="sxs-lookup"><span data-stu-id="baae0-111">For more information about saved views, see [Customize Entity Views in Dynamics 365 for Customer Engagement apps](customize-dev/customize-entity-views.md) and [Offline and Outlook Filters and Templates](outlook-client/offline-outlook-filters-templates.md).</span></span>  
  
 <span data-ttu-id="baae0-112">A query in the form of a FetchXML statement is constructed and then assigned to the `UserQuery.FetchXml` attribute.</span><span class="sxs-lookup"><span data-stu-id="baae0-112">A query in the form of a FetchXML statement is constructed and then assigned to the `UserQuery.FetchXml` attribute.</span></span> <span data-ttu-id="baae0-113">This query can be executed by using the <xref:Microsoft.Crm.Sdk.Messages.ExecuteByIdUserQueryRequest> message.</span><span class="sxs-lookup"><span data-stu-id="baae0-113">This query can be executed by using the <xref:Microsoft.Crm.Sdk.Messages.ExecuteByIdUserQueryRequest> message.</span></span>  
  
 <span data-ttu-id="baae0-114">You can see the user query (saved view) in the Advanced Find section of the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] application and also in the **View** drop-down list for an entity.</span><span class="sxs-lookup"><span data-stu-id="baae0-114">You can see the user query (saved view) in the Advanced Find section of the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] application and also in the **View** drop-down list for an entity.</span></span>  <span data-ttu-id="baae0-115">You can export the value of the `UserQuery.FetchXml` attribute by using the **Download Fetch XML** button in the **Advanced Find** dialog box.</span><span class="sxs-lookup"><span data-stu-id="baae0-115">You can export the value of the `UserQuery.FetchXml` attribute by using the **Download Fetch XML** button in the **Advanced Find** dialog box.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="baae0-116">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="baae0-116">See also</span></span>  
 <span data-ttu-id="baae0-117">[Model Your Business Data With Dynamics 365 for Customer Engagement apps](model-business-data.md) </span><span class="sxs-lookup"><span data-stu-id="baae0-117">[Model Your Business Data With Dynamics 365 for Customer Engagement apps](model-business-data.md) </span></span>  
 <span data-ttu-id="baae0-118">[UserQuery Entity](entities/userquery.md) [Building Queries with QueryExpression](org-service/build-queries-with-queryexpression.md) </span><span class="sxs-lookup"><span data-stu-id="baae0-118">[UserQuery Entity](entities/userquery.md) [Building Queries with QueryExpression](org-service/build-queries-with-queryexpression.md) </span></span>  
 [<span data-ttu-id="baae0-119">Fetch XML Schema</span><span class="sxs-lookup"><span data-stu-id="baae0-119">Fetch XML Schema</span></span>](org-service/fetchxml-schema.md)
