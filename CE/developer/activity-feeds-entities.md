---
title: Activity feeds entities (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: The activity feeds help promote internal collaboration through quick and short updates in Dynamics 365 for Customer Engagement apps. The activity feeds do not replace emails or in-person communications.
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
- integrating activity feeds with other applications
- activity feeds, collaborating internally
- collaborating internally, activity feeds
- activity feeds, definition of
- activity feeds, benefits of
- activity feeds, integrating with other applications
- activity feeds, introduction
ms.assetid: e475491b-179a-4c26-9acd-3d6557173d9d
caps.latest.revision: 56
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 35a7147c27a118535e3a3e7b18f8f9c091159d6e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386476"
---
# <a name="activity-feeds-entities"></a><span data-ttu-id="17006-104">Activity feeds entities</span><span class="sxs-lookup"><span data-stu-id="17006-104">Activity feeds entities</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="17006-105">The *activity feeds* help promote internal collaboration through quick and short updates in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="17006-105">The *activity feeds* help promote internal collaboration through quick and short updates in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span> <span data-ttu-id="17006-106">The activity feeds do not replace emails or in-person communications.</span><span class="sxs-lookup"><span data-stu-id="17006-106">The activity feeds do not replace emails or in-person communications.</span></span> <span data-ttu-id="17006-107">Instead, they augment these traditional methods with non-intrusive and non-urgent ways of communication.</span><span class="sxs-lookup"><span data-stu-id="17006-107">Instead, they augment these traditional methods with non-intrusive and non-urgent ways of communication.</span></span>  
  
 <span data-ttu-id="17006-108">The activity feeds enable a salesperson to stay on top of situations that involve people, accounts, leads, contacts, or opportunities.</span><span class="sxs-lookup"><span data-stu-id="17006-108">The activity feeds enable a salesperson to stay on top of situations that involve people, accounts, leads, contacts, or opportunities.</span></span> <span data-ttu-id="17006-109">They provide easy and convenient ways of monitoring important information that can be critical for closing a deal.</span><span class="sxs-lookup"><span data-stu-id="17006-109">They provide easy and convenient ways of monitoring important information that can be critical for closing a deal.</span></span>  
  
 <span data-ttu-id="17006-110">With activity feeds you can easily accomplish important tasks, such as:</span><span class="sxs-lookup"><span data-stu-id="17006-110">With activity feeds you can easily accomplish important tasks, such as:</span></span>  
  
- <span data-ttu-id="17006-111">Share information about users, accounts, leads, and other entity records.</span><span class="sxs-lookup"><span data-stu-id="17006-111">Share information about users, accounts, leads, and other entity records.</span></span>  
  
- <span data-ttu-id="17006-112">Receive important updates regarding opportunities, users, or other records.</span><span class="sxs-lookup"><span data-stu-id="17006-112">Receive important updates regarding opportunities, users, or other records.</span></span>  
  
- <span data-ttu-id="17006-113">Follow users, accounts, and other records.</span><span class="sxs-lookup"><span data-stu-id="17006-113">Follow users, accounts, and other records.</span></span>  
  
- <span data-ttu-id="17006-114">Learn, in a timely manner, about updates regarding users, accounts, or opportunities and items that are related to them.</span><span class="sxs-lookup"><span data-stu-id="17006-114">Learn, in a timely manner, about updates regarding users, accounts, or opportunities and items that are related to them.</span></span>  
  
- <span data-ttu-id="17006-115">Take quick actions on specific updates to move your work towards successful completion.</span><span class="sxs-lookup"><span data-stu-id="17006-115">Take quick actions on specific updates to move your work towards successful completion.</span></span>  
  
  <span data-ttu-id="17006-116">As a developer you can consume and create activity feeds data programmatically.</span><span class="sxs-lookup"><span data-stu-id="17006-116">As a developer you can consume and create activity feeds data programmatically.</span></span> <span data-ttu-id="17006-117">You can integrate activity feeds with other applications, and extend activity feeds to meet the needs of the organization.</span><span class="sxs-lookup"><span data-stu-id="17006-117">You can integrate activity feeds with other applications, and extend activity feeds to meet the needs of the organization.</span></span> <span data-ttu-id="17006-118">The following are examples of custom applications that you can build around activity feeds:</span><span class="sxs-lookup"><span data-stu-id="17006-118">The following are examples of custom applications that you can build around activity feeds:</span></span>  
  
- <span data-ttu-id="17006-119">Build full-featured activity feeds clients to complement [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps out-of-the-box client experiences that include Web, Outlook, and Mobile clients.</span><span class="sxs-lookup"><span data-stu-id="17006-119">Build full-featured activity feeds clients to complement [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps out-of-the-box client experiences that include Web, Outlook, and Mobile clients.</span></span> <span data-ttu-id="17006-120">For example, you can develop a desktop client.</span><span class="sxs-lookup"><span data-stu-id="17006-120">For example, you can develop a desktop client.</span></span>  
  
- <span data-ttu-id="17006-121">Build surfaces to expose activity feeds data inside other applications, such as [!INCLUDE[pn_SharePoint_short](../includes/pn-sharepoint-short.md)] or enterprise resource planning (ERP).</span><span class="sxs-lookup"><span data-stu-id="17006-121">Build surfaces to expose activity feeds data inside other applications, such as [!INCLUDE[pn_SharePoint_short](../includes/pn-sharepoint-short.md)] or enterprise resource planning (ERP).</span></span>  
  
- <span data-ttu-id="17006-122">Build custom business logic to create activity feed posts when internal [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] app events or external events occur.</span><span class="sxs-lookup"><span data-stu-id="17006-122">Build custom business logic to create activity feed posts when internal [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] app events or external events occur.</span></span> <span data-ttu-id="17006-123">An example of an external event is an invoice creation in an external ERP system.</span><span class="sxs-lookup"><span data-stu-id="17006-123">An example of an external event is an invoice creation in an external ERP system.</span></span>  
  
- <span data-ttu-id="17006-124">Perform specific actions when posts are created or deleted.</span><span class="sxs-lookup"><span data-stu-id="17006-124">Perform specific actions when posts are created or deleted.</span></span> <span data-ttu-id="17006-125">For example, use a workflow to send an email when a post is created.</span><span class="sxs-lookup"><span data-stu-id="17006-125">For example, use a workflow to send an email when a post is created.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="17006-126">In addition to activity feeds, from [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps you can directly connect to [!INCLUDE[pn_yammer](../includes/pn-yammer.md)], a powerful tool for collaborating in your organization.</span><span class="sxs-lookup"><span data-stu-id="17006-126">In addition to activity feeds, from [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps you can directly connect to [!INCLUDE[pn_yammer](../includes/pn-yammer.md)], a powerful tool for collaborating in your organization.</span></span> <span data-ttu-id="17006-127">For more information, see [Connect to Yammer](connect-yammer.md).</span><span class="sxs-lookup"><span data-stu-id="17006-127">For more information, see [Connect to Yammer](connect-yammer.md).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="17006-128">In This Section</span><span class="sxs-lookup"><span data-stu-id="17006-128">In This Section</span></span>  
 [<span data-ttu-id="17006-129">Introduction to Activity Feeds</span><span class="sxs-lookup"><span data-stu-id="17006-129">Introduction to Activity Feeds</span></span>](introduction-activity-feeds.md)  
  
 [<span data-ttu-id="17006-130">Configure Activity Feeds</span><span class="sxs-lookup"><span data-stu-id="17006-130">Configure Activity Feeds</span></span>](configure-activity-feeds.md)  
  
 [<span data-ttu-id="17006-131">Kết nối với Yammer</span><span class="sxs-lookup"><span data-stu-id="17006-131">Connect to Yammer</span></span>](connect-yammer.md)  

 [<span data-ttu-id="17006-132">Post Entity</span><span class="sxs-lookup"><span data-stu-id="17006-132">Post Entity</span></span>](entities/post.md)  
  
 [<span data-ttu-id="17006-133">PostComment Entity</span><span class="sxs-lookup"><span data-stu-id="17006-133">PostComment Entity</span></span>](entities/postcomment.md)  
  
 [<span data-ttu-id="17006-134">PostFollow Entity</span><span class="sxs-lookup"><span data-stu-id="17006-134">PostFollow Entity</span></span>](entities/postfollow.md)  
  
 [<span data-ttu-id="17006-135">PostLike Entity</span><span class="sxs-lookup"><span data-stu-id="17006-135">PostLike Entity</span></span>](entities/postlike.md)  
  
 [<span data-ttu-id="17006-136">msdyn_PostAlbum Entity</span><span class="sxs-lookup"><span data-stu-id="17006-136">msdyn_PostAlbum Entity</span></span>](entities/msdyn_postalbum.md)  
  
 [<span data-ttu-id="17006-137">msdyn_PostConfig Entity</span><span class="sxs-lookup"><span data-stu-id="17006-137">msdyn_PostConfig Entity</span></span>](entities/msdyn_postconfig.md)
  
 [<span data-ttu-id="17006-138">msdyn_PostRuleConfig Entity</span><span class="sxs-lookup"><span data-stu-id="17006-138">msdyn_PostRuleConfig Entity</span></span>](entities/msdyn_postruleconfig.md)
  
 [<span data-ttu-id="17006-139">Sample: Collaborate with Activity Feeds</span><span class="sxs-lookup"><span data-stu-id="17006-139">Sample: Collaborate with Activity Feeds</span></span>](sample-collaborate-with-activity-feeds.md)  
  
## <a name="related-sections"></a><span data-ttu-id="17006-140">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="17006-140">Related Sections</span></span>  
 [<span data-ttu-id="17006-141">Model Your Business Data With Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="17006-141">Model Your Business Data With Dynamics 365 for Customer Engagement apps</span></span>](model-business-data.md)  
  
 [<span data-ttu-id="17006-142">Customer Entities (Account, Contact)</span><span class="sxs-lookup"><span data-stu-id="17006-142">Customer Entities (Account, Contact)</span></span>](customer-entities-account-contact.md)
