---
title: Social entities (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Learn about social entites that offers social Activity to track social posts, social profile to track a contact’s presence in social media, and convert the social posts to case
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 77353550-3661-407b-8ca7-a0619f8068a0
caps.latest.revision: 13
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 0c506055862bd436d397297c206e5f41deebbf00
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387102"
---
# <a name="social-entities"></a><span data-ttu-id="5a9f2-103">Social entities</span><span class="sxs-lookup"><span data-stu-id="5a9f2-103">Social entities</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="5a9f2-104">Use [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] social care generic framework to route the social data that you obtain from various social channels into your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] system.</span><span class="sxs-lookup"><span data-stu-id="5a9f2-104">Use [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] social care generic framework to route the social data that you obtain from various social channels into your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] system.</span></span> <span data-ttu-id="5a9f2-105">Social care framework provides the general interface, data model, and necessary APIs for integrating social listening applications like Facebook and Twitter with [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] to track social messages and profile data.</span><span class="sxs-lookup"><span data-stu-id="5a9f2-105">Social care framework provides the general interface, data model, and necessary APIs for integrating social listening applications like Facebook and Twitter with [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] to track social messages and profile data.</span></span> <span data-ttu-id="5a9f2-106">Using social care framework, third party systems can push social data feed containing posts from the social channels to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] and can associate a social post with an existing [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] record.</span><span class="sxs-lookup"><span data-stu-id="5a9f2-106">Using social care framework, third party systems can push social data feed containing posts from the social channels to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] and can associate a social post with an existing [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] record.</span></span>  
  
 <span data-ttu-id="5a9f2-107">Social care framework offers following capabilities:</span><span class="sxs-lookup"><span data-stu-id="5a9f2-107">Social care framework offers following capabilities:</span></span>  
  
- <span data-ttu-id="5a9f2-108">Social Activity to track Social posts in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)]</span><span class="sxs-lookup"><span data-stu-id="5a9f2-108">Social Activity to track Social posts in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)]</span></span>  
  
- <span data-ttu-id="5a9f2-109">Social Profile to track a contact’s presence in social media</span><span class="sxs-lookup"><span data-stu-id="5a9f2-109">Social Profile to track a contact’s presence in social media</span></span>  
  
- <span data-ttu-id="5a9f2-110">Rule driven manual and automated Case creation and attribute values in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="5a9f2-110">Rule driven manual and automated Case creation and attribute values in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="5a9f2-111">[Automatically create cases from email or social monitoring](http://go.microsoft.com/fwlink/p/?LinkId=393464).</span><span class="sxs-lookup"><span data-stu-id="5a9f2-111">[Automatically create cases from email or social monitoring](http://go.microsoft.com/fwlink/p/?LinkId=393464).</span></span>  
  
  <span data-ttu-id="5a9f2-112">You can use this framework to automatically convert social posts to case, create social profiles and contact records for the author of the posts in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)], search existing records, and associate social posts and profiles to them.</span><span class="sxs-lookup"><span data-stu-id="5a9f2-112">You can use this framework to automatically convert social posts to case, create social profiles and contact records for the author of the posts in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)], search existing records, and associate social posts and profiles to them.</span></span> <span data-ttu-id="5a9f2-113">You can configure watch lists with keywords, #tags, @mentions to identify the social buzz around your brand, product or service on social channels like Twitter or Facebook.</span><span class="sxs-lookup"><span data-stu-id="5a9f2-113">You can configure watch lists with keywords, #tags, @mentions to identify the social buzz around your brand, product or service on social channels like Twitter or Facebook.</span></span> <span data-ttu-id="5a9f2-114">Sau đó, kết hợp danh sách xem với một hàng [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)], đó thiết lập để tự động tạo trường hợp từ bài viết trên mạng xã hội.</span><span class="sxs-lookup"><span data-stu-id="5a9f2-114">Then, associate the watch list with a [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] queue, which is set up to automatically create cases from social posts.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="5a9f2-115">[Automatically create cases from email or social monitoring](http://go.microsoft.com/fwlink/p/?LinkId=393464).</span><span class="sxs-lookup"><span data-stu-id="5a9f2-115">[Automatically create cases from email or social monitoring](http://go.microsoft.com/fwlink/p/?LinkId=393464).</span></span>  
  
  <span data-ttu-id="5a9f2-116">![Social care concept diagram](media/social-care-concepts.png "Social care concept diagram")</span><span class="sxs-lookup"><span data-stu-id="5a9f2-116">![Social care concept diagram](media/social-care-concepts.png "Social care concept diagram")</span></span>  
  
  <span data-ttu-id="5a9f2-117">Social care framework enhances the existing email to case settings to enable the automated case creation when a social activity is delivered to a queue.</span><span class="sxs-lookup"><span data-stu-id="5a9f2-117">Social care framework enhances the existing email to case settings to enable the automated case creation when a social activity is delivered to a queue.</span></span> <span data-ttu-id="5a9f2-118">The external system or user can recognize the scope of the social care feed (for example, Post ID, corresponding [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] record, attributes corresponding to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] record), and target the update on the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] record and its attributes using the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] Create, Retrieve, Update, and Delete operations on an entity API method delivered through the Web API of [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].</span><span class="sxs-lookup"><span data-stu-id="5a9f2-118">The external system or user can recognize the scope of the social care feed (for example, Post ID, corresponding [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] record, attributes corresponding to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] record), and target the update on the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] record and its attributes using the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] Create, Retrieve, Update, and Delete operations on an entity API method delivered through the Web API of [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].</span></span>  
  
  [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] <span data-ttu-id="5a9f2-119">allows external services to connect to it, but won’t call into any external service and connect to it.</span><span class="sxs-lookup"><span data-stu-id="5a9f2-119">allows external services to connect to it, but won’t call into any external service and connect to it.</span></span> <span data-ttu-id="5a9f2-120">The primary recipients of social data are [SocialActivity Entity](entities/socialactivity.md) and [SocialProfile Entity](entities/socialprofile.md), which are compliant with the changes in the social data.</span><span class="sxs-lookup"><span data-stu-id="5a9f2-120">The primary recipients of social data are [SocialActivity Entity](entities/socialactivity.md) and [SocialProfile Entity](entities/socialprofile.md), which are compliant with the changes in the social data.</span></span>  
  
  <span data-ttu-id="5a9f2-121">The data model and API used in social care framework provides the developers an opportunity to extend and customize the sample app to meet their business scenario.</span><span class="sxs-lookup"><span data-stu-id="5a9f2-121">The data model and API used in social care framework provides the developers an opportunity to extend and customize the sample app to meet their business scenario.</span></span> <span data-ttu-id="5a9f2-122">You can download the sample app based on [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] APIs to get visibility into [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].</span><span class="sxs-lookup"><span data-stu-id="5a9f2-122">You can download the sample app based on [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] APIs to get visibility into [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="5a9f2-123">[Sample Application Using Microsoft Dynamics CRM Social Care Framework](https://msdn.microsoft.com/library/dn744885.aspx).</span><span class="sxs-lookup"><span data-stu-id="5a9f2-123">[Sample Application Using Microsoft Dynamics CRM Social Care Framework](https://msdn.microsoft.com/library/dn744885.aspx).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="5a9f2-124">In This Section</span><span class="sxs-lookup"><span data-stu-id="5a9f2-124">In This Section</span></span>  
 [<span data-ttu-id="5a9f2-125">SocialActivity Entity</span><span class="sxs-lookup"><span data-stu-id="5a9f2-125">SocialActivity Entity</span></span>](entities/socialactivity.md)  
  
 [<span data-ttu-id="5a9f2-126">SocialProfile Entity</span><span class="sxs-lookup"><span data-stu-id="5a9f2-126">SocialProfile Entity</span></span>](entities/socialprofile.md)  
  
## <a name="related-sections"></a><span data-ttu-id="5a9f2-127">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="5a9f2-127">Related Sections</span></span>  
 [<span data-ttu-id="5a9f2-128">Model Your Business Data</span><span class="sxs-lookup"><span data-stu-id="5a9f2-128">Model Your Business Data</span></span>](model-business-data.md)  
  
 [<span data-ttu-id="5a9f2-129">Sample Application Using Microsoft Dynamics CRM Social Care Framework</span><span class="sxs-lookup"><span data-stu-id="5a9f2-129">Sample Application Using Microsoft Dynamics CRM Social Care Framework</span></span>](https://msdn.microsoft.com/library/dn744885.aspx)
