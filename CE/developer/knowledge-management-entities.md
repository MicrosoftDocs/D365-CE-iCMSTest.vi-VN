---
title: Knowledge management entities (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: ''
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
- knowledge base entities, managing knowledge bases
- knowledge base entities, service entities
- service entities, knowledge base entities
- knowledge base, definition
- KB
- knowledge base entities, introduction
- managing knowledge bases, knowledge base entities
ms.assetid: 7f481592-217a-45a7-9604-4995c142d295
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 3eb6a135b4b233c2d610034059b98b994079b8a6
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386053"
---
# <a name="knowledge-management-entities"></a><span data-ttu-id="8a3e4-102">Knowledge management entities</span><span class="sxs-lookup"><span data-stu-id="8a3e4-102">Knowledge management entities</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[pn_crm_8_1_0_both](../includes/pn-crm-8-1-0-both.md)] <span data-ttu-id="8a3e4-103">introduced a new knowledge management system that lets you create rich knowledge articles with support for embedding external multimedia contents, such as images and videos, as links.</span><span class="sxs-lookup"><span data-stu-id="8a3e4-103">introduced a new knowledge management system that lets you create rich knowledge articles with support for embedding external multimedia contents, such as images and videos, as links.</span></span> <span data-ttu-id="8a3e4-104">You can use the SDK to programmatically create and manage knowledge articles, create major and minor versions of the articles, translate the articles into multiple languages, and schedule the publishing and expiration of the articles.</span><span class="sxs-lookup"><span data-stu-id="8a3e4-104">You can use the SDK to programmatically create and manage knowledge articles, create major and minor versions of the articles, translate the articles into multiple languages, and schedule the publishing and expiration of the articles.</span></span> <span data-ttu-id="8a3e4-105">You can also increment knowledge article views, associate knowledge article records with [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] entity records, and perform a full-text search on knowledge articles from your application.</span><span class="sxs-lookup"><span data-stu-id="8a3e4-105">You can also increment knowledge article views, associate knowledge article records with [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] entity records, and perform a full-text search on knowledge articles from your application.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="8a3e4-106">[Work with knowledge articles in Dynamics 365 for Customer Engagement apps](work-knowledge-articles.md)</span><span class="sxs-lookup"><span data-stu-id="8a3e4-106">[Work with knowledge articles in Dynamics 365 for Customer Engagement apps](work-knowledge-articles.md)</span></span>  
     
<span data-ttu-id="8a3e4-107">You can set up knowledge management for your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] instance using the web client only; it can’t be done through the SDK.</span><span class="sxs-lookup"><span data-stu-id="8a3e4-107">You can set up knowledge management for your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] instance using the web client only; it can’t be done through the SDK.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="8a3e4-108">[Set up knowledge management in Dynamics 365 for Customer Engagement apps](../customer-service/set-up-knowledge-management-embedded-knowledge-search.md)</span><span class="sxs-lookup"><span data-stu-id="8a3e4-108">[Set up knowledge management in Dynamics 365 for Customer Engagement apps](../customer-service/set-up-knowledge-management-embedded-knowledge-search.md)</span></span>
  
 <span data-ttu-id="8a3e4-109">After you enable knowledge management for an entity using the web client, you can insert and configure a knowledge base search control in the entity form to display relevant knowledge articles from [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="8a3e4-109">After you enable knowledge management for an entity using the web client, you can insert and configure a knowledge base search control in the entity form to display relevant knowledge articles from [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span></span> <span data-ttu-id="8a3e4-110">The knowledge base search control provides programmability support to automate or enhance the user’s experience when using this control.</span><span class="sxs-lookup"><span data-stu-id="8a3e4-110">The knowledge base search control provides programmability support to automate or enhance the user’s experience when using this control.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="8a3e4-111">[Knowledge base search control (client-side reference)](clientapi/reference/controls.md#kbsearch-knowledge-base-search-control-type)</span><span class="sxs-lookup"><span data-stu-id="8a3e4-111">[Knowledge base search control (client-side reference)](clientapi/reference/controls.md#kbsearch-knowledge-base-search-control-type)</span></span>    
  
 <span data-ttu-id="8a3e4-112">Use the `KnowledgeArticle` and `KnowledgeArticleViews` entities to work with the knowledge articles in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="8a3e4-112">Use the `KnowledgeArticle` and `KnowledgeArticleViews` entities to work with the knowledge articles in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="8a3e4-113">Với bản phát hành [!INCLUDE[pn_crm_8_1_0_online_subsequent](../includes/pn-crm-8-1-0-online-subsequent.md)] và [!INCLUDE[pn_crm_8_1_0_op](../includes/pn-crm-8-1-0-op.md)] (tại chỗ), các thực thể sau dùng cho quản lý kiến thức không còn được dùng: `KbArticle`, `KbArticleComment` và `KbArticleTemplate`.</span><span class="sxs-lookup"><span data-stu-id="8a3e4-113">With [!INCLUDE[pn_crm_8_1_0_online_subsequent](../includes/pn-crm-8-1-0-online-subsequent.md)] and [!INCLUDE[pn_crm_8_1_0_op](../includes/pn-crm-8-1-0-op.md)] (on-premises) release, the following entities used for knowledge management are deprecated: `KbArticle`, `KbArticleComment`, and `KbArticleTemplate`.</span></span> <span data-ttu-id="8a3e4-114">Các thực thể này sẽ không được hỗ trợ trong bản phát hành chính trong tương lai của [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="8a3e4-114">These entities won't be supported in a future major release of [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span></span> <span data-ttu-id="8a3e4-115">You must use the newer `KnowledgeArticle` entity in your code for knowledge management in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="8a3e4-115">You must use the newer `KnowledgeArticle` entity in your code for knowledge management in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="8a3e4-116">[Important changes coming in future releases of Dynamics 365 for Customer Engagement apps](/get-started/whats-new/customer-engagement/important-changes-coming)</span><span class="sxs-lookup"><span data-stu-id="8a3e4-116">[Important changes coming in future releases of Dynamics 365 for Customer Engagement apps](/get-started/whats-new/customer-engagement/important-changes-coming)</span></span>  
  
  
## <a name="reference"></a><span data-ttu-id="8a3e4-117">Tham chiếu</span><span class="sxs-lookup"><span data-stu-id="8a3e4-117">Reference</span></span>  
 [<span data-ttu-id="8a3e4-118">Blog: New Knowledge Management in the Microsoft Dynamics CRM 2016 release</span><span class="sxs-lookup"><span data-stu-id="8a3e4-118">Blog: New Knowledge Management in the Microsoft Dynamics CRM 2016 release</span></span>](http://blogs.msdn.com/b/crm/archive/2015/10/15/new-knowledge-management-in-microsoft-dynamics-crm-2016-release.aspx)  
  
## <a name="related-sections"></a><span data-ttu-id="8a3e4-119">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="8a3e4-119">Related Sections</span></span>  
 [<span data-ttu-id="8a3e4-120">Knowledge base search control (client-side reference)</span><span class="sxs-lookup"><span data-stu-id="8a3e4-120">Knowledge base search control (client-side reference)</span></span>](clientapi/reference/controls.md#kbsearch-knowledge-base-search-control-type)  
  
 [<span data-ttu-id="8a3e4-121">Contract entities</span><span class="sxs-lookup"><span data-stu-id="8a3e4-121">Contract entities</span></span>](contract-entities.md)  
  
 [<span data-ttu-id="8a3e4-122">Incident (case) entities</span><span class="sxs-lookup"><span data-stu-id="8a3e4-122">Incident (case) entities</span></span>](incident-case-entities.md)  
  
 [<span data-ttu-id="8a3e4-123">Service Entities (Contract, Incident, Knowledge Base)</span><span class="sxs-lookup"><span data-stu-id="8a3e4-123">Service Entities (Contract, Incident, Knowledge Base)</span></span>](service-entities.md)
