---
title: Sales literature entities (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Create and manage sales literature items to associate attachments and articles to enrich an organization’s sales information.
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
- sales literature entities, sales literature items and attachments
- file attachments, see 'sales literature entities'
- CAD files, see 'sales literature entities'
- organizing sales literature into categories and types, sales literature entities
- brochures, see 'sales literature entities'
- literature library
- sales literature items, defined and explained
- marketing encyclopedia
- sales literature items
- sales literature entities, central repository for sales literature
- subject manager, see 'sales literature entities'
- sales literature entities, brochures, CAD files, and other attachments to sales literature
- sales literature entities, introduction
- knowledge base, see 'sales literature entities'
- sales literature entities, organizing sales literature into categories and types
- sales literature entities, sales literature records
ms.assetid: ef65e4bf-d29c-48f6-9325-eccf8e6bba8f
caps.latest.revision: 20
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 01dd1d1baaa71cfb8a76054539cde1ce02b29295
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387897"
---
# <a name="sales-literature-entities"></a><span data-ttu-id="3621c-103">Sales literature entities</span><span class="sxs-lookup"><span data-stu-id="3621c-103">Sales literature entities</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="3621c-104">A *sales literature* item is the basic unit of the marketing encyclopedia in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].</span><span class="sxs-lookup"><span data-stu-id="3621c-104">A *sales literature* item is the basic unit of the marketing encyclopedia in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].</span></span> <span data-ttu-id="3621c-105">For example, a business unit might decide to create an article about a specific product.</span><span class="sxs-lookup"><span data-stu-id="3621c-105">For example, a business unit might decide to create an article about a specific product.</span></span> <span data-ttu-id="3621c-106">The article can contain multiple sales literature items (sales attachments) such as a brochure, detailed specifications, and a CAD file, together with appropriate search terms, for example, "bolt" or "stainless steel."</span><span class="sxs-lookup"><span data-stu-id="3621c-106">The article can contain multiple sales literature items (sales attachments) such as a brochure, detailed specifications, and a CAD file, together with appropriate search terms, for example, "bolt" or "stainless steel."</span></span> <span data-ttu-id="3621c-107">Any PC-compatible file format can be uploaded and attached to an article in the marketing encyclopedia.</span><span class="sxs-lookup"><span data-stu-id="3621c-107">Any PC-compatible file format can be uploaded and attached to an article in the marketing encyclopedia.</span></span> <span data-ttu-id="3621c-108">Specific search terms can be specified for each item.</span><span class="sxs-lookup"><span data-stu-id="3621c-108">Specific search terms can be specified for each item.</span></span>  
  
 <span data-ttu-id="3621c-109">You can use the sales literature management entities to create a central repository for your organization’s sales information (in the form of  sales literature items (sales attachments)) that provides an easy way to distribute information to users, both online and offline.</span><span class="sxs-lookup"><span data-stu-id="3621c-109">You can use the sales literature management entities to create a central repository for your organization’s sales information (in the form of  sales literature items (sales attachments)) that provides an easy way to distribute information to users, both online and offline.</span></span> <span data-ttu-id="3621c-110">Sales literature can be organized into categories and types to provide easier management and searching.</span><span class="sxs-lookup"><span data-stu-id="3621c-110">Sales literature can be organized into categories and types to provide easier management and searching.</span></span> [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] <span data-ttu-id="3621c-111">also supports a subject manager and knowledge base.</span><span class="sxs-lookup"><span data-stu-id="3621c-111">also supports a subject manager and knowledge base.</span></span>  
  
 <span data-ttu-id="3621c-112">A sales literature record can have one or more sales literature items (sales attachments) attached to it in various formats, such as .doc, .pub, and .pdf.</span><span class="sxs-lookup"><span data-stu-id="3621c-112">A sales literature record can have one or more sales literature items (sales attachments) attached to it in various formats, such as .doc, .pub, and .pdf.</span></span> <span data-ttu-id="3621c-113">An item cannot be shared between sales literature records.</span><span class="sxs-lookup"><span data-stu-id="3621c-113">An item cannot be shared between sales literature records.</span></span>  
  
 <span data-ttu-id="3621c-114">Sales literature records can also be attached to competitors and products (both yours and your competitors').</span><span class="sxs-lookup"><span data-stu-id="3621c-114">Sales literature records can also be attached to competitors and products (both yours and your competitors').</span></span>  
  
 <span data-ttu-id="3621c-115">The basic operations supported in the marketing encyclopedia include the following:</span><span class="sxs-lookup"><span data-stu-id="3621c-115">The basic operations supported in the marketing encyclopedia include the following:</span></span>  
  
- <span data-ttu-id="3621c-116">Create a sales literature item</span><span class="sxs-lookup"><span data-stu-id="3621c-116">Create a sales literature item</span></span>  
  
- <span data-ttu-id="3621c-117">View a sales literature item</span><span class="sxs-lookup"><span data-stu-id="3621c-117">View a sales literature item</span></span>  
  
- <span data-ttu-id="3621c-118">Edit a sales literature item</span><span class="sxs-lookup"><span data-stu-id="3621c-118">Edit a sales literature item</span></span>  
  
- <span data-ttu-id="3621c-119">Delete a sales literature item</span><span class="sxs-lookup"><span data-stu-id="3621c-119">Delete a sales literature item</span></span>  
  
- <span data-ttu-id="3621c-120">Search for a sales literature item</span><span class="sxs-lookup"><span data-stu-id="3621c-120">Search for a sales literature item</span></span>  
  
- <span data-ttu-id="3621c-121">Upload an attachment and attach it to a sales literature item</span><span class="sxs-lookup"><span data-stu-id="3621c-121">Upload an attachment and attach it to a sales literature item</span></span>  
  
  <span data-ttu-id="3621c-122">You can create a searchable marketing encyclopedia for storing various sales and marketing literature.</span><span class="sxs-lookup"><span data-stu-id="3621c-122">You can create a searchable marketing encyclopedia for storing various sales and marketing literature.</span></span> <span data-ttu-id="3621c-123">As an example, a sales literature library might include the following:</span><span class="sxs-lookup"><span data-stu-id="3621c-123">As an example, a sales literature library might include the following:</span></span>  
  
- <span data-ttu-id="3621c-124">Product information</span><span class="sxs-lookup"><span data-stu-id="3621c-124">Product information</span></span>  
  
- <span data-ttu-id="3621c-125">Presentations and brochures</span><span class="sxs-lookup"><span data-stu-id="3621c-125">Presentations and brochures</span></span>  
  
- <span data-ttu-id="3621c-126">Policies and procedures</span><span class="sxs-lookup"><span data-stu-id="3621c-126">Policies and procedures</span></span>  
  
- <span data-ttu-id="3621c-127">Tài liệu bán hàng</span><span class="sxs-lookup"><span data-stu-id="3621c-127">Sales literature</span></span>  
  
- <span data-ttu-id="3621c-128">Giấy trắng</span><span class="sxs-lookup"><span data-stu-id="3621c-128">White papers</span></span>  
  
- <span data-ttu-id="3621c-129">Competitive information</span><span class="sxs-lookup"><span data-stu-id="3621c-129">Competitive information</span></span>  
  
- <span data-ttu-id="3621c-130">Price lists</span><span class="sxs-lookup"><span data-stu-id="3621c-130">Price lists</span></span>  
  
- <span data-ttu-id="3621c-131">Annual reports</span><span class="sxs-lookup"><span data-stu-id="3621c-131">Annual reports</span></span>  
  
- <span data-ttu-id="3621c-132">Manuals</span><span class="sxs-lookup"><span data-stu-id="3621c-132">Manuals</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="3621c-133">In This Section</span><span class="sxs-lookup"><span data-stu-id="3621c-133">In This Section</span></span>  
 [<span data-ttu-id="3621c-134">SalesLiterature Entity</span><span class="sxs-lookup"><span data-stu-id="3621c-134">SalesLiterature Entity</span></span>](entities/salesliterature.md)  
  
 [<span data-ttu-id="3621c-135">SalesLiteratureItem Entity</span><span class="sxs-lookup"><span data-stu-id="3621c-135">SalesLiteratureItem Entity</span></span>](entities/salesliteratureitem.md)  
  
## <a name="related-sections"></a><span data-ttu-id="3621c-136">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="3621c-136">Related Sections</span></span>  
 [<span data-ttu-id="3621c-137">Model Your Business Data With Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="3621c-137">Model Your Business Data With Dynamics 365 for Customer Engagement apps</span></span>](model-business-data.md)  
  
 [<span data-ttu-id="3621c-138">Schedule and Appointment Entities</span><span class="sxs-lookup"><span data-stu-id="3621c-138">Schedule and Appointment Entities</span></span>](schedule-appointment-entities.md)
