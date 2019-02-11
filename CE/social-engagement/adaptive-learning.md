---
title: Adaptive learning in Social Engagement | Microsoft Docs
description: Learn about sentiment analysis and the organization-based machine learning models which learn from your inputs.
keywords: ''
ms.date: 12/08/2017
ms.service: dynamics-365-marketing
ms.topic: article
applies_to:
- Social Engagement
ms.assetid: 2c056a5c-d890-4106-837a-d4b403e011a1
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
ms.openlocfilehash: 758e04bd6cbed6f78fba3f17c79407e2f5c93ee6
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "375610"
---
# <a name="adaptive-learning-based-on-changes-to-organizations-sentiment-values"></a><span data-ttu-id="aed34-103">Adaptive learning based on changes to organization’s sentiment values</span><span class="sxs-lookup"><span data-stu-id="aed34-103">Adaptive learning based on changes to organization’s sentiment values</span></span>
[!INCLUDE[pn_netbreeze_long](../includes/pn-social-engagement-long.md)] <span data-ttu-id="aed34-104">now uses *adaptive learning* to gain information about your edits and confirmations on sentiment values.</span><span class="sxs-lookup"><span data-stu-id="aed34-104">now uses *adaptive learning* to gain information about your edits and confirmations on sentiment values.</span></span> <span data-ttu-id="aed34-105">With adaptive learning, every edit on the sentiment value of posts contributes to the way that sentiments are determined for your organization.</span><span class="sxs-lookup"><span data-stu-id="aed34-105">With adaptive learning, every edit on the sentiment value of posts contributes to the way that sentiments are determined for your organization.</span></span>  
  
<span data-ttu-id="aed34-106">To manage adaptive learning in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)], you need to be a [!INCLUDE[pn-social-engagement-short](../includes/pn-social-engagement-short.md)] Administrator.</span><span class="sxs-lookup"><span data-stu-id="aed34-106">To manage adaptive learning in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)], you need to be a [!INCLUDE[pn-social-engagement-short](../includes/pn-social-engagement-short.md)] Administrator.</span></span> <span data-ttu-id="aed34-107">Every user role in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] is able to edit the sentiment value of a post.</span><span class="sxs-lookup"><span data-stu-id="aed34-107">Every user role in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] is able to edit the sentiment value of a post.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="aed34-108">[Understand user roles](user-roles.md)</span><span class="sxs-lookup"><span data-stu-id="aed34-108">[Understand user roles](user-roles.md)</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="aed34-109">Edited and confirmed sentiment values only apply to your organization database.</span><span class="sxs-lookup"><span data-stu-id="aed34-109">Edited and confirmed sentiment values only apply to your organization database.</span></span> <span data-ttu-id="aed34-110">Edits and confirmations performed on other organizations’ databases have no impact on how the sentiment is determined for your organization.</span><span class="sxs-lookup"><span data-stu-id="aed34-110">Edits and confirmations performed on other organizations’ databases have no impact on how the sentiment is determined for your organization.</span></span>  
  
## <a name="activate-or-deactivate-machine-learning-for-your-organization"></a><span data-ttu-id="aed34-111">Activate or deactivate machine learning for your organization</span><span class="sxs-lookup"><span data-stu-id="aed34-111">Activate or deactivate machine learning for your organization</span></span>  
<span data-ttu-id="aed34-112">By default, machine learning is active for your organization, but you can turn it off at any time.</span><span class="sxs-lookup"><span data-stu-id="aed34-112">By default, machine learning is active for your organization, but you can turn it off at any time.</span></span>  
  
1.  <span data-ttu-id="aed34-113">Navigate to **Settings** > **Global Settings**.</span><span class="sxs-lookup"><span data-stu-id="aed34-113">Navigate to **Settings** > **Global Settings**.</span></span>  
  
2.  <span data-ttu-id="aed34-114">In the list, click **Sentiment**.</span><span class="sxs-lookup"><span data-stu-id="aed34-114">In the list, click **Sentiment**.</span></span>  
  
3.  <span data-ttu-id="aed34-115">On the **Sentiment** pane, clear the **Adaptive learning** check box.</span><span class="sxs-lookup"><span data-stu-id="aed34-115">On the **Sentiment** pane, clear the **Adaptive learning** check box.</span></span>  
  
4.  <span data-ttu-id="aed34-116">Click **Save** ![Save button](media/save-icon.png "Save button").</span><span class="sxs-lookup"><span data-stu-id="aed34-116">Click **Save** ![Save button](media/save-icon.png "Save button").</span></span>  
  
<span data-ttu-id="aed34-117">Your organization’s sentiment analysis no longer learns from your users’ edits.</span><span class="sxs-lookup"><span data-stu-id="aed34-117">Your organization’s sentiment analysis no longer learns from your users’ edits.</span></span>  
  
<span data-ttu-id="aed34-118">To turn machine learning on, select the **Adaptive learning** check box and click **Save** ![Save button](media/save-icon.png "Save button").</span><span class="sxs-lookup"><span data-stu-id="aed34-118">To turn machine learning on, select the **Adaptive learning** check box and click **Save** ![Save button](media/save-icon.png "Save button").</span></span> <span data-ttu-id="aed34-119">Your organization’s sentiment analysis will now be able to learn from your users’ edits.</span><span class="sxs-lookup"><span data-stu-id="aed34-119">Your organization’s sentiment analysis will now be able to learn from your users’ edits.</span></span>  
## <a name="reset-your-organizations-sentiment-analysis"></a><span data-ttu-id="aed34-120">Reset your organization’s sentiment analysis</span><span class="sxs-lookup"><span data-stu-id="aed34-120">Reset your organization’s sentiment analysis</span></span>  
<span data-ttu-id="aed34-121">If you aren’t happy with the results of the sentiment analysis, you can always reset your organization’s sentiment analysis to the system default.</span><span class="sxs-lookup"><span data-stu-id="aed34-121">If you aren’t happy with the results of the sentiment analysis, you can always reset your organization’s sentiment analysis to the system default.</span></span> <span data-ttu-id="aed34-122">This will discard all previously made edits and confirmations to sentiment values, and restart the learning from the system default.</span><span class="sxs-lookup"><span data-stu-id="aed34-122">This will discard all previously made edits and confirmations to sentiment values, and restart the learning from the system default.</span></span>  
  
 [!INCLUDE[proc_permissions_social_listening_admin](../includes/proc-permissions-social-listening-admin.md)]  
  
1.  <span data-ttu-id="aed34-123">Navigate to **Settings** > **Global Settings**.</span><span class="sxs-lookup"><span data-stu-id="aed34-123">Navigate to **Settings** > **Global Settings**.</span></span>  
  
2.  <span data-ttu-id="aed34-124">In the list, click **Sentiment**.</span><span class="sxs-lookup"><span data-stu-id="aed34-124">In the list, click **Sentiment**.</span></span>  
  
3.  <span data-ttu-id="aed34-125">On the **Sentiment** pane, click **Reset**.</span><span class="sxs-lookup"><span data-stu-id="aed34-125">On the **Sentiment** pane, click **Reset**.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="aed34-126">If you restart the learning for the sentiment analysis, you’ll find the date of the restart at the bottom of the page when you go to **Global Settings** > **Sentiment**.</span><span class="sxs-lookup"><span data-stu-id="aed34-126">If you restart the learning for the sentiment analysis, you’ll find the date of the restart at the bottom of the page when you go to **Global Settings** > **Sentiment**.</span></span>  
  
> [!CAUTION]
>  <span data-ttu-id="aed34-127">There’s no way of undoing this reset.</span><span class="sxs-lookup"><span data-stu-id="aed34-127">There’s no way of undoing this reset.</span></span> <span data-ttu-id="aed34-128">Use this functionality careful to avoid accidental loss of all your users’ edits and confirmation to sentiment values.</span><span class="sxs-lookup"><span data-stu-id="aed34-128">Use this functionality careful to avoid accidental loss of all your users’ edits and confirmation to sentiment values.</span></span>  
  
> [!TIP]
>  <span data-ttu-id="aed34-129">If you compare several months of Sentiment KPI, make sure that you account for the matured sentiment calculation when comparing the findings.</span><span class="sxs-lookup"><span data-stu-id="aed34-129">If you compare several months of Sentiment KPI, make sure that you account for the matured sentiment calculation when comparing the findings.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="aed34-130">See Also</span><span class="sxs-lookup"><span data-stu-id="aed34-130">See Also</span></span>  
<span data-ttu-id="aed34-131">[Manage global settings](manage-global-settings.md) </span><span class="sxs-lookup"><span data-stu-id="aed34-131">[Manage global settings](manage-global-settings.md) </span></span>  
[<span data-ttu-id="aed34-132">Understand the public perception using sentiment analysis</span><span class="sxs-lookup"><span data-stu-id="aed34-132">Understand the public perception using sentiment analysis</span></span>](analytics-sentiment.md)
 
