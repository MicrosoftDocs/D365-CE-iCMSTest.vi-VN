---
title: Link posts from Social Engagement to Dynamics 365 for Customer Engagement | Microsoft Docs
description: Learn how to link social posts to Dynamics 365 for Customer Engagement and create new case or lead records.
keywords: link to crm, link to customer engagement
ms.date: 03/16/2018
ms.service: dynamics-365-marketing
ms.topic: article
applies_to:
- Social Engagement
ms.assetid: e97a38d7-37c4-4dce-b02e-1076ad992cff
author: m-hartmann
ms.author: mhart
manager: sakudes
topic-status: Drafting
ms.custom:
- dyn365-socialengagement
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365SE
ms.openlocfilehash: 6e8cdf796d390824e22988a4a1868c52ddf2893f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "375590"
---
# <a name="link-posts-from-includepnnetbreezeshortincludespn-social-engagement-shortmd-to-includepndynamicscrmincludespn-dynamics-crmmd-apps"></a><span data-ttu-id="eba0e-104">Link posts from [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] to [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps</span><span class="sxs-lookup"><span data-stu-id="eba0e-104">Link posts from [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] to [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps</span></span>

[!INCLUDE[pn_netbreeze_long](../includes/pn-social-engagement-long.md)] <span data-ttu-id="eba0e-105">provides a platform for capturing public posts from social media.</span><span class="sxs-lookup"><span data-stu-id="eba0e-105">provides a platform for capturing public posts from social media.</span></span> <span data-ttu-id="eba0e-106">You link posts in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] instance and turn them into new records.</span><span class="sxs-lookup"><span data-stu-id="eba0e-106">You link posts in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] instance and turn them into new records.</span></span>

<span data-ttu-id="eba0e-107">When you link a post from [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] instance, a Social Activity record is created.</span><span class="sxs-lookup"><span data-stu-id="eba0e-107">When you link a post from [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] instance, a Social Activity record is created.</span></span> [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] <span data-ttu-id="eba0e-108">apps can turn these social activities into other types of records, for example into a lead, an opportunity, or a case.</span><span class="sxs-lookup"><span data-stu-id="eba0e-108">apps can turn these social activities into other types of records, for example into a lead, an opportunity, or a case.</span></span>
  
## <a name="steps-for-linking-posts"></a><span data-ttu-id="eba0e-109">Steps for linking posts</span><span class="sxs-lookup"><span data-stu-id="eba0e-109">Steps for linking posts</span></span>  

1. <span data-ttu-id="eba0e-110">First, [set up the feature to link social posts](connect-dynamics-365-social-engagement.md) to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] instance as social activities.</span><span class="sxs-lookup"><span data-stu-id="eba0e-110">First, [set up the feature to link social posts](connect-dynamics-365-social-engagement.md) to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] instance as social activities.</span></span> <span data-ttu-id="eba0e-111">As a [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] Administrator, you need to connect the instance to [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span><span class="sxs-lookup"><span data-stu-id="eba0e-111">As a [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] Administrator, you need to connect the instance to [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span></span>   
  
2. <span data-ttu-id="eba0e-112">Next, you can [define the attributes](create-dynamics-365-record-from-social-post.md) for the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] entities that you want to display in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span><span class="sxs-lookup"><span data-stu-id="eba0e-112">Next, you can [define the attributes](create-dynamics-365-record-from-social-post.md) for the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] entities that you want to display in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span></span>   
  
3. <span data-ttu-id="eba0e-113">As a system administrator or customizer in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)], you can configure rules to handle newly created social activities by using the [**Automatic Record Creation and Update Rules**](configure-automatic-record-creation.md) feature in your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] settings.</span><span class="sxs-lookup"><span data-stu-id="eba0e-113">As a system administrator or customizer in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)], you can configure rules to handle newly created social activities by using the [**Automatic Record Creation and Update Rules**](configure-automatic-record-creation.md) feature in your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] settings.</span></span>   
  
4. <span data-ttu-id="eba0e-114">When everything is set up, your users can start to link social posts to create or update [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] records.</span><span class="sxs-lookup"><span data-stu-id="eba0e-114">When everything is set up, your users can start to link social posts to create or update [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] records.</span></span>   
   [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="eba0e-115">[Create a new Dynamics 365 for Customer Engagement record from a social post](create-dynamics-365-record-from-social-post.md)</span><span class="sxs-lookup"><span data-stu-id="eba0e-115">[Create a new Dynamics 365 for Customer Engagement record from a social post](create-dynamics-365-record-from-social-post.md)</span></span>  
  
5. <span data-ttu-id="eba0e-116">Optionally, you can configure [automation rules](automation-rules.md) in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] to create new [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] records for posts that match a specified data set.</span><span class="sxs-lookup"><span data-stu-id="eba0e-116">Optionally, you can configure [automation rules](automation-rules.md) in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] to create new [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] records for posts that match a specified data set.</span></span>   
  
6. <span data-ttu-id="eba0e-117">Understand how to [delete or disable a connection](manage-connection-dynamics-365-social-engagement.md) and how this might affect existing linkages or linking newly acquired social posts.</span><span class="sxs-lookup"><span data-stu-id="eba0e-117">Understand how to [delete or disable a connection](manage-connection-dynamics-365-social-engagement.md) and how this might affect existing linkages or linking newly acquired social posts.</span></span>   
  
### <a name="privacy-notice"></a><span data-ttu-id="eba0e-118">Privacy notice</span><span class="sxs-lookup"><span data-stu-id="eba0e-118">Privacy notice</span></span> 
 
 [!INCLUDE[cc_privacy_mse_post_and_automation_rules](../includes/cc-privacy-mse-post-and-automation-rules.md)]  
  
### <a name="see-also"></a><span data-ttu-id="eba0e-119">See also</span><span class="sxs-lookup"><span data-stu-id="eba0e-119">See also</span></span>  

 <span data-ttu-id="eba0e-120">[Administer Microsoft Social Engagement](administer-microsoft-social-engagement.md) </span><span class="sxs-lookup"><span data-stu-id="eba0e-120">[Administer Microsoft Social Engagement](administer-microsoft-social-engagement.md) </span></span>  
 <span data-ttu-id="eba0e-121">[Set up the connection between Dynamics 365 for Customer Engagement and Social Engagement](connect-dynamics-365-social-engagement.md) </span><span class="sxs-lookup"><span data-stu-id="eba0e-121">[Set up the connection between Dynamics 365 for Customer Engagement and Social Engagement](connect-dynamics-365-social-engagement.md) </span></span>  
 [<span data-ttu-id="eba0e-122">Create a new Dynamics 365 for Customer Engagement record from a social post</span><span class="sxs-lookup"><span data-stu-id="eba0e-122">Create a new Dynamics 365 for Customer Engagement record from a social post</span></span>](create-dynamics-365-record-from-social-post.md)
