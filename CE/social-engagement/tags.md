---
title: Work with tags in Social Engagement | Microsoft Docs
description: Learn how to work with tags on post and the auto-tagging capabilities in Social Engagement.
keywords: tags, tagging, auto tags, custom tags, Social Engagement
ms.date: 08/22/2018
ms.service: dynamics-365-marketing
ms.topic: article
applies_to:
- Social Engagement
ms.assetid: 1cf877c0-f5a0-43fc-9bf0-1c5ef12359e1
author: m-hartmann
ms.author: mhart
manager: shellyha
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
ms.openlocfilehash: 8c36c6bb2eb1dca328484bb6ceb308b4b488bafc
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "375558"
---
# <a name="work-with-tags"></a><span data-ttu-id="a54c6-104">Work with tags</span><span class="sxs-lookup"><span data-stu-id="a54c6-104">Work with tags</span></span>
<span data-ttu-id="a54c6-105">Intention tags and custom tags are two ways [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] allows you to prioritize and filter your posts.</span><span class="sxs-lookup"><span data-stu-id="a54c6-105">Intention tags and custom tags are two ways [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] allows you to prioritize and filter your posts.</span></span> <span data-ttu-id="a54c6-106">When authors publish posts on social media, they usually have a messaging purpose in mind.</span><span class="sxs-lookup"><span data-stu-id="a54c6-106">When authors publish posts on social media, they usually have a messaging purpose in mind.</span></span> <span data-ttu-id="a54c6-107">The larger the number of posts, the more work intensive and time consuming it gets to read through all of these posts and identify those relevant for your business—for example, to find out if authors are asking a question that you want to answer, or if they are complaining about a service that you want to follow up on.</span><span class="sxs-lookup"><span data-stu-id="a54c6-107">The larger the number of posts, the more work intensive and time consuming it gets to read through all of these posts and identify those relevant for your business—for example, to find out if authors are asking a question that you want to answer, or if they are complaining about a service that you want to follow up on.</span></span> <span data-ttu-id="a54c6-108">In [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)], once a post is acquired from a search topic, we take some of the workload off your desk.</span><span class="sxs-lookup"><span data-stu-id="a54c6-108">In [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)], once a post is acquired from a search topic, we take some of the workload off your desk.</span></span> <span data-ttu-id="a54c6-109">Acquired posts are analyzed by the machine-learning based algorithm to detect authors’ intentions or you can add your own custom tags and later promote them to auto tags.</span><span class="sxs-lookup"><span data-stu-id="a54c6-109">Acquired posts are analyzed by the machine-learning based algorithm to detect authors’ intentions or you can add your own custom tags and later promote them to auto tags.</span></span>

  
<a name="intention_analysis"></a>   
## <a name="how-intention-analysis-works"></a><span data-ttu-id="a54c6-110">How intention analysis works</span><span class="sxs-lookup"><span data-stu-id="a54c6-110">How intention analysis works</span></span>  
<span data-ttu-id="a54c6-111">Intention analysis is applied to posts when they are picked up by a search topic.</span><span class="sxs-lookup"><span data-stu-id="a54c6-111">Intention analysis is applied to posts when they are picked up by a search topic.</span></span> <span data-ttu-id="a54c6-112">Posts are scored against the algorithm and, if applicable, marked with the intentions identified.</span><span class="sxs-lookup"><span data-stu-id="a54c6-112">Posts are scored against the algorithm and, if applicable, marked with the intentions identified.</span></span> <span data-ttu-id="a54c6-113">A post can have multiple intention tags, but more commonly there’s just one.</span><span class="sxs-lookup"><span data-stu-id="a54c6-113">A post can have multiple intention tags, but more commonly there’s just one.</span></span>  
  
<span data-ttu-id="a54c6-114">The following intention tags are used by [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span><span class="sxs-lookup"><span data-stu-id="a54c6-114">The following intention tags are used by [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="a54c6-115">**Intention tag**</span><span class="sxs-lookup"><span data-stu-id="a54c6-115">**Intention tag**</span></span>|<span data-ttu-id="a54c6-116">**What the author expresses**</span><span class="sxs-lookup"><span data-stu-id="a54c6-116">**What the author expresses**</span></span>|  
|<span data-ttu-id="a54c6-117">Purchase</span><span class="sxs-lookup"><span data-stu-id="a54c6-117">Purchase</span></span>|<span data-ttu-id="a54c6-118">Interest in buying a product or service</span><span class="sxs-lookup"><span data-stu-id="a54c6-118">Interest in buying a product or service</span></span>|  
|<span data-ttu-id="a54c6-119">Complaint</span><span class="sxs-lookup"><span data-stu-id="a54c6-119">Complaint</span></span>|<span data-ttu-id="a54c6-120">Frustration about a product or service</span><span class="sxs-lookup"><span data-stu-id="a54c6-120">Frustration about a product or service</span></span>|  
|<span data-ttu-id="a54c6-121">Information request</span><span class="sxs-lookup"><span data-stu-id="a54c6-121">Information request</span></span>|<span data-ttu-id="a54c6-122">A need for additional information about a service or product</span><span class="sxs-lookup"><span data-stu-id="a54c6-122">A need for additional information about a service or product</span></span>|  
|<span data-ttu-id="a54c6-123">Support request</span><span class="sxs-lookup"><span data-stu-id="a54c6-123">Support request</span></span>|<span data-ttu-id="a54c6-124">A need for help and support in using a service or product</span><span class="sxs-lookup"><span data-stu-id="a54c6-124">A need for help and support in using a service or product</span></span>|  
  
> [!NOTE]
>  <span data-ttu-id="a54c6-125">Intention analysis is available for [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] posts found on [!INCLUDE[tn_twitter](../includes/tn-twitter.md)] and [!INCLUDE[tn_facebook](../includes/tn-facebook.md)] in the English language.</span><span class="sxs-lookup"><span data-stu-id="a54c6-125">Intention analysis is available for [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] posts found on [!INCLUDE[tn_twitter](../includes/tn-twitter.md)] and [!INCLUDE[tn_facebook](../includes/tn-facebook.md)] in the English language.</span></span>  
  
<span data-ttu-id="a54c6-126">Intention tags are predefined in [!INCLUDE[pn_netbreeze_long](../includes/pn-social-engagement-long.md)].</span><span class="sxs-lookup"><span data-stu-id="a54c6-126">Intention tags are predefined in [!INCLUDE[pn_netbreeze_long](../includes/pn-social-engagement-long.md)].</span></span> <span data-ttu-id="a54c6-127">The machine learning service makes predictions on whether posts relate to one of the supported intention tags.</span><span class="sxs-lookup"><span data-stu-id="a54c6-127">The machine learning service makes predictions on whether posts relate to one of the supported intention tags.</span></span> <span data-ttu-id="a54c6-128">We recommend that you [remove or add intention tags](work-with-posts.md#add-or-remove-tags) from posts if they aren’t accurate to improve machine learning.</span><span class="sxs-lookup"><span data-stu-id="a54c6-128">We recommend that you [remove or add intention tags](work-with-posts.md#add-or-remove-tags) from posts if they aren’t accurate to improve machine learning.</span></span>
  
<a name="add_custom"></a>   
## <a name="add-custom-tags"></a><span data-ttu-id="a54c6-129">Add custom tags</span><span class="sxs-lookup"><span data-stu-id="a54c6-129">Add custom tags</span></span>  
[!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] <span data-ttu-id="a54c6-130">lets you add one or more custom tags to posts.</span><span class="sxs-lookup"><span data-stu-id="a54c6-130">lets you add one or more custom tags to posts.</span></span> <span data-ttu-id="a54c6-131">You can then filter posts to match specific custom tags.</span><span class="sxs-lookup"><span data-stu-id="a54c6-131">You can then filter posts to match specific custom tags.</span></span> <span data-ttu-id="a54c6-132">Custom tags are different from intention tags because they are not predefined tags and they are not automatically added once a post is acquired.</span><span class="sxs-lookup"><span data-stu-id="a54c6-132">Custom tags are different from intention tags because they are not predefined tags and they are not automatically added once a post is acquired.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a54c6-133">Only Managers and Responders can create a new custom tag, but any user role can add or remove tags on posts.</span><span class="sxs-lookup"><span data-stu-id="a54c6-133">Only Managers and Responders can create a new custom tag, but any user role can add or remove tags on posts.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="a54c6-134">[Understand user roles](user-roles.md)</span><span class="sxs-lookup"><span data-stu-id="a54c6-134">[Understand user roles](user-roles.md)</span></span>  
  
1.  <span data-ttu-id="a54c6-135">Select **Posts** on the right side of any Analytics page to see the posts list.</span><span class="sxs-lookup"><span data-stu-id="a54c6-135">Select **Posts** on the right side of any Analytics page to see the posts list.</span></span>  
  
     <span data-ttu-id="a54c6-136">--OR--</span><span class="sxs-lookup"><span data-stu-id="a54c6-136">--OR--</span></span>  
  
     <span data-ttu-id="a54c6-137">Go to **Social Center** to see your streams.</span><span class="sxs-lookup"><span data-stu-id="a54c6-137">Go to **Social Center** to see your streams.</span></span>  
  
2.  <span data-ttu-id="a54c6-138">Select a post, and then next to the custom tags symbol ![Tag symbol in Social Engagement](media/tag-symbol.png "Tag symbol in Social Engagement") , select **Add** ![Add button](media/add-icon.png "Add button").</span><span class="sxs-lookup"><span data-stu-id="a54c6-138">Select a post, and then next to the custom tags symbol ![Tag symbol in Social Engagement](media/tag-symbol.png "Tag symbol in Social Engagement") , select **Add** ![Add button](media/add-icon.png "Add button").</span></span> <span data-ttu-id="a54c6-139">Start typing to enter the custom tag that you want to add, and then press **Enter** to select the tag or create a new one.</span><span class="sxs-lookup"><span data-stu-id="a54c6-139">Start typing to enter the custom tag that you want to add, and then press **Enter** to select the tag or create a new one.</span></span>  
  
3.  <span data-ttu-id="a54c6-140">Select **Confirm**.</span><span class="sxs-lookup"><span data-stu-id="a54c6-140">Select **Confirm**.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="a54c6-141">The maximum amount of custom tags you can add per post is 20 tags.</span><span class="sxs-lookup"><span data-stu-id="a54c6-141">The maximum amount of custom tags you can add per post is 20 tags.</span></span> <span data-ttu-id="a54c6-142">To add more tags, you must first remove other tags.</span><span class="sxs-lookup"><span data-stu-id="a54c6-142">To add more tags, you must first remove other tags.</span></span>  
  
<a name="promote_customtags"></a>   
## <a name="promote-custom-tags-to-auto-tags"></a><span data-ttu-id="a54c6-143">Promote custom tags to auto tags</span><span class="sxs-lookup"><span data-stu-id="a54c6-143">Promote custom tags to auto tags</span></span>  
<span data-ttu-id="a54c6-144">Enable adaptive learning on your custom tags by adding them to your list of auto tags.</span><span class="sxs-lookup"><span data-stu-id="a54c6-144">Enable adaptive learning on your custom tags by adding them to your list of auto tags.</span></span> [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] <span data-ttu-id="a54c6-145">applies adaptive learning on auto tags to predict tags for new incoming posts.</span><span class="sxs-lookup"><span data-stu-id="a54c6-145">applies adaptive learning on auto tags to predict tags for new incoming posts.</span></span>  <span data-ttu-id="a54c6-146">The system learns from posts when the user makes edits and actions on tags.</span><span class="sxs-lookup"><span data-stu-id="a54c6-146">The system learns from posts when the user makes edits and actions on tags.</span></span>  <span data-ttu-id="a54c6-147">Auto tags use text analytics and Azure Machine Learning techniques to learn patterns from posts that are manually tagged by the user, tags that are added by the system and confirmed by the user, or tags that are added by the system and removed by the user.</span><span class="sxs-lookup"><span data-stu-id="a54c6-147">Auto tags use text analytics and Azure Machine Learning techniques to learn patterns from posts that are manually tagged by the user, tags that are added by the system and confirmed by the user, or tags that are added by the system and removed by the user.</span></span>  
<span data-ttu-id="a54c6-148">To improve your workflows and increase efficiency, you can leverage auto tagged posts in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] as [email alerts](email-alerts.md), [streams](engage-on-social-networks.md), [activity maps](activity-maps.md), and [automation rules](automation-rules.md).</span><span class="sxs-lookup"><span data-stu-id="a54c6-148">To improve your workflows and increase efficiency, you can leverage auto tagged posts in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] as [email alerts](email-alerts.md), [streams](engage-on-social-networks.md), [activity maps](activity-maps.md), and [automation rules](automation-rules.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="a54c6-149">Only Administrators can promote custom tags to auto tags.</span><span class="sxs-lookup"><span data-stu-id="a54c6-149">Only Administrators can promote custom tags to auto tags.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="a54c6-150">[Understand user roles](user-roles.md)</span><span class="sxs-lookup"><span data-stu-id="a54c6-150">[Understand user roles](user-roles.md)</span></span>  
  
### <a name="add-a-custom-tag-to-your-auto-tags-list"></a><span data-ttu-id="a54c6-151">Add a custom tag to your auto tags list</span><span class="sxs-lookup"><span data-stu-id="a54c6-151">Add a custom tag to your auto tags list</span></span>  
  
1.  <span data-ttu-id="a54c6-152">Go to **Settings** > **Global Settings**</span><span class="sxs-lookup"><span data-stu-id="a54c6-152">Go to **Settings** > **Global Settings**</span></span>  
  
2.  <span data-ttu-id="a54c6-153">In the Global Settings pane, select **Auto Tags**.</span><span class="sxs-lookup"><span data-stu-id="a54c6-153">In the Global Settings pane, select **Auto Tags**.</span></span>  
  
3.  <span data-ttu-id="a54c6-154">Under Auto Tags, select **Add Auto Tag** ![Add button](media/add-icon.png "Add button")</span><span class="sxs-lookup"><span data-stu-id="a54c6-154">Under Auto Tags, select **Add Auto Tag** ![Add button](media/add-icon.png "Add button")</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="a54c6-155">You can maintain up to five auto tags simultaneously.</span><span class="sxs-lookup"><span data-stu-id="a54c6-155">You can maintain up to five auto tags simultaneously.</span></span>  
  
4.  <span data-ttu-id="a54c6-156">In the **Add Auto Tag** pane, enter a tag to search and select existing custom tags to be turned into auto tags.</span><span class="sxs-lookup"><span data-stu-id="a54c6-156">In the **Add Auto Tag** pane, enter a tag to search and select existing custom tags to be turned into auto tags.</span></span> <span data-ttu-id="a54c6-157">If you don't have any custom tags created yet, refer to the [Add custom tags](tags.md#add-custom-tags) section.</span><span class="sxs-lookup"><span data-stu-id="a54c6-157">If you don't have any custom tags created yet, refer to the [Add custom tags](tags.md#add-custom-tags) section.</span></span> 
  
5.  <span data-ttu-id="a54c6-158">Select **Save** to apply your changes.</span><span class="sxs-lookup"><span data-stu-id="a54c6-158">Select **Save** to apply your changes.</span></span>  
  
6.  <span data-ttu-id="a54c6-159">In your list of custom tags, select the tag, and then in the **Tag Details** pane, set **Auto tagging** to **On**.</span><span class="sxs-lookup"><span data-stu-id="a54c6-159">In your list of custom tags, select the tag, and then in the **Tag Details** pane, set **Auto tagging** to **On**.</span></span>  
  
     <span data-ttu-id="a54c6-160">--OR--</span><span class="sxs-lookup"><span data-stu-id="a54c6-160">--OR--</span></span>  
  
     <span data-ttu-id="a54c6-161">In your list of custom tags, set **Auto tagging** to **On** next to the custom tag title.</span><span class="sxs-lookup"><span data-stu-id="a54c6-161">In your list of custom tags, set **Auto tagging** to **On** next to the custom tag title.</span></span>  
     
    > [!NOTE]
    > <span data-ttu-id="a54c6-162">It may take up to six hours for posts to start being automatically tagged.</span><span class="sxs-lookup"><span data-stu-id="a54c6-162">It may take up to six hours for posts to start being automatically tagged.</span></span>  
  
### <a name="remove-auto-tags"></a><span data-ttu-id="a54c6-163">Remove auto tags</span><span class="sxs-lookup"><span data-stu-id="a54c6-163">Remove auto tags</span></span>  
  
1.  <span data-ttu-id="a54c6-164">Go to **Settings** > **Global Settings**.</span><span class="sxs-lookup"><span data-stu-id="a54c6-164">Go to **Settings** > **Global Settings**.</span></span>  
  
2.  <span data-ttu-id="a54c6-165">In the Global Settings pane, select **Auto Tags**.</span><span class="sxs-lookup"><span data-stu-id="a54c6-165">In the Global Settings pane, select **Auto Tags**.</span></span>  
  
3.  <span data-ttu-id="a54c6-166">In the Auto Tags panel, select **Remove**, and then select **Confirm**.</span><span class="sxs-lookup"><span data-stu-id="a54c6-166">In the Auto Tags panel, select **Remove**, and then select **Confirm**.</span></span>  
    <span data-ttu-id="a54c6-167">Removed tags will remain visible on previous posts, but auto scoring will stop for incoming posts.</span><span class="sxs-lookup"><span data-stu-id="a54c6-167">Removed tags will remain visible on previous posts, but auto scoring will stop for incoming posts.</span></span> 

## <a name="improve-accuracy-of-system-rated-tags"></a><span data-ttu-id="a54c6-168">Improve accuracy of system-rated tags</span><span class="sxs-lookup"><span data-stu-id="a54c6-168">Improve accuracy of system-rated tags</span></span>

<span data-ttu-id="a54c6-169">To further improve the underlying machine learning model for auto tags and intention tags, you can confirm and remove system-rated.</span><span class="sxs-lookup"><span data-stu-id="a54c6-169">To further improve the underlying machine learning model for auto tags and intention tags, you can confirm and remove system-rated.</span></span> <span data-ttu-id="a54c6-170">Removing a system-rated tag from a post lets the model know that it was added wrongly while confirming a tag indicates the model was adding it correctly.</span><span class="sxs-lookup"><span data-stu-id="a54c6-170">Removing a system-rated tag from a post lets the model know that it was added wrongly while confirming a tag indicates the model was adding it correctly.</span></span> 

### <a name="remove-a-system-rated-tag"></a><span data-ttu-id="a54c6-171">Remove a system-rated tag</span><span class="sxs-lookup"><span data-stu-id="a54c6-171">Remove a system-rated tag</span></span>

1.  <span data-ttu-id="a54c6-172">Select an auto tag or intention tag in the **Post Tags and Intentions** filter to create a data set that contains the tagged posts you want to review.</span><span class="sxs-lookup"><span data-stu-id="a54c6-172">Select an auto tag or intention tag in the **Post Tags and Intentions** filter to create a data set that contains the tagged posts you want to review.</span></span>   
  
2.  <span data-ttu-id="a54c6-173">Select a post.</span><span class="sxs-lookup"><span data-stu-id="a54c6-173">Select a post.</span></span>
  
3.  <span data-ttu-id="a54c6-174">Next to the tags symbol ![Tag symbol in Social Engagement](media/tag-symbol.png "Tag symbol in Social Engagement"), select **Remove this tag** ![Remove tag symbol in Social Engagement](media/delete-icon.png "Remove tag symbol in Social Engagement").</span><span class="sxs-lookup"><span data-stu-id="a54c6-174">Next to the tags symbol ![Tag symbol in Social Engagement](media/tag-symbol.png "Tag symbol in Social Engagement"), select **Remove this tag** ![Remove tag symbol in Social Engagement](media/delete-icon.png "Remove tag symbol in Social Engagement").</span></span>  
<span data-ttu-id="a54c6-175">The system-rated tag gets removed from the post and the machine learning model will take this removal into account for future assignement of system-rated tags.</span><span class="sxs-lookup"><span data-stu-id="a54c6-175">The system-rated tag gets removed from the post and the machine learning model will take this removal into account for future assignement of system-rated tags.</span></span>

### <a name="confirm-a-system-rated-tag"></a><span data-ttu-id="a54c6-176">Confirm a system-rated tag</span><span class="sxs-lookup"><span data-stu-id="a54c6-176">Confirm a system-rated tag</span></span>

1.  <span data-ttu-id="a54c6-177">Select an auto tag or intention tag in the **Post Tags and Intentions** filter to create a data set that contains the tagged posts you want to review.</span><span class="sxs-lookup"><span data-stu-id="a54c6-177">Select an auto tag or intention tag in the **Post Tags and Intentions** filter to create a data set that contains the tagged posts you want to review.</span></span>   
  
2.  <span data-ttu-id="a54c6-178">Select a post.</span><span class="sxs-lookup"><span data-stu-id="a54c6-178">Select a post.</span></span>  
  
3.  <span data-ttu-id="a54c6-179">Next to the tags symbol ![Tag symbol in Social Engagement](media/tag-symbol.png "Tag symbol in Social Engagement"), select **Confirm this auto tag** ![Confirm tag symbol in Social Engagement](media/check-icon.png "Confirm tag symbol in Social Engagement").</span><span class="sxs-lookup"><span data-stu-id="a54c6-179">Next to the tags symbol ![Tag symbol in Social Engagement](media/tag-symbol.png "Tag symbol in Social Engagement"), select **Confirm this auto tag** ![Confirm tag symbol in Social Engagement](media/check-icon.png "Confirm tag symbol in Social Engagement").</span></span>   
<span data-ttu-id="a54c6-180">![Intention tag and customer tag with confirm control highlighted](media/confirm-intention-view-custom-tag.png "Intention tag and customer tag with confirm control highlighted")  </span><span class="sxs-lookup"><span data-stu-id="a54c6-180">![Intention tag and customer tag with confirm control highlighted](media/confirm-intention-view-custom-tag.png "Intention tag and customer tag with confirm control highlighted")  </span></span>  
<span data-ttu-id="a54c6-181">A stars symbol indicates that this system-rated tag was manually confirmed and the machine learning model will take this confirmation into account for future assignment of system-rated tags.</span><span class="sxs-lookup"><span data-stu-id="a54c6-181">A stars symbol indicates that this system-rated tag was manually confirmed and the machine learning model will take this confirmation into account for future assignment of system-rated tags.</span></span> 

## <a name="review-the-quality-of-a-tagging-model"></a><span data-ttu-id="a54c6-182">Review the quality of a tagging model</span><span class="sxs-lookup"><span data-stu-id="a54c6-182">Review the quality of a tagging model</span></span>

<span data-ttu-id="a54c6-183">You can check the quality of your auto tags at any time to ensure a high quality model.</span><span class="sxs-lookup"><span data-stu-id="a54c6-183">You can check the quality of your auto tags at any time to ensure a high quality model.</span></span> <span data-ttu-id="a54c6-184">It's important to understand that quality varies over time and you should turn auto tagging on only after your quality is acceptable.</span><span class="sxs-lookup"><span data-stu-id="a54c6-184">It's important to understand that quality varies over time and you should turn auto tagging on only after your quality is acceptable.</span></span> <span data-ttu-id="a54c6-185">To achieve acceptable quality, [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] recommends that you have at least 50 posts tagged first.</span><span class="sxs-lookup"><span data-stu-id="a54c6-185">To achieve acceptable quality, [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] recommends that you have at least 50 posts tagged first.</span></span>     
<span data-ttu-id="a54c6-186">To check the quality of your auto tags, select the tag name in the list.</span><span class="sxs-lookup"><span data-stu-id="a54c6-186">To check the quality of your auto tags, select the tag name in the list.</span></span> <span data-ttu-id="a54c6-187">In the **Tag Details** pane, you can see the quality, quality history, and tagged posts history of that auto tag.</span><span class="sxs-lookup"><span data-stu-id="a54c6-187">In the **Tag Details** pane, you can see the quality, quality history, and tagged posts history of that auto tag.</span></span>  
  
<span data-ttu-id="a54c6-188">**Quality**: The quality indicates whether the score of your selected tags exceeds or doesn't meet the minimum quality requirements.</span><span class="sxs-lookup"><span data-stu-id="a54c6-188">**Quality**: The quality indicates whether the score of your selected tags exceeds or doesn't meet the minimum quality requirements.</span></span>  
  
<span data-ttu-id="a54c6-189">**Quality History**: The quality history chart shows the quality of the auto tag from the past 30 days.</span><span class="sxs-lookup"><span data-stu-id="a54c6-189">**Quality History**: The quality history chart shows the quality of the auto tag from the past 30 days.</span></span>  
  
<span data-ttu-id="a54c6-190">**Tagged posts history**: The Tagged posts history chart shows how many posts have been automatically tagged and how many have been manually edited since turning auto tagging on.</span><span class="sxs-lookup"><span data-stu-id="a54c6-190">**Tagged posts history**: The Tagged posts history chart shows how many posts have been automatically tagged and how many have been manually edited since turning auto tagging on.</span></span>  
 
  
## <a name="manage-your-tags"></a><span data-ttu-id="a54c6-191">Manage your tags</span><span class="sxs-lookup"><span data-stu-id="a54c6-191">Manage your tags</span></span>  
  
### <a name="delete-tags"></a><span data-ttu-id="a54c6-192">Delete tags</span><span class="sxs-lookup"><span data-stu-id="a54c6-192">Delete tags</span></span>  
  
1.  <span data-ttu-id="a54c6-193">Go to **Settings** > **Global Settings**.</span><span class="sxs-lookup"><span data-stu-id="a54c6-193">Go to **Settings** > **Global Settings**.</span></span>  
  
2.  <span data-ttu-id="a54c6-194">In the **Global Settings** pane, select **Custom Tags**.</span><span class="sxs-lookup"><span data-stu-id="a54c6-194">In the **Global Settings** pane, select **Custom Tags**.</span></span>  
  
3.  <span data-ttu-id="a54c6-195">In the **Custom Tags** pane, next to the tag name, select **Delete** ![Delete button](media/trashbin-icon.png "Delete button"), and then select **Confirm**.</span><span class="sxs-lookup"><span data-stu-id="a54c6-195">In the **Custom Tags** pane, next to the tag name, select **Delete** ![Delete button](media/trashbin-icon.png "Delete button"), and then select **Confirm**.</span></span>  
  
### <a name="rename-tags"></a><span data-ttu-id="a54c6-196">Rename tags</span><span class="sxs-lookup"><span data-stu-id="a54c6-196">Rename tags</span></span>  
  
1.  <span data-ttu-id="a54c6-197">Go to **Settings** > **Global Settings**.</span><span class="sxs-lookup"><span data-stu-id="a54c6-197">Go to **Settings** > **Global Settings**.</span></span>  
  
2.  <span data-ttu-id="a54c6-198">In the **Global Settings** pane, select **Custom Tags**.</span><span class="sxs-lookup"><span data-stu-id="a54c6-198">In the **Global Settings** pane, select **Custom Tags**.</span></span>  
  
3.  <span data-ttu-id="a54c6-199">In the **Custom Tags** pane, select **Edit** ![Edit button](media/edit-icon.png "Edit button") next to the tag name, and then start typing in the edit box.</span><span class="sxs-lookup"><span data-stu-id="a54c6-199">In the **Custom Tags** pane, select **Edit** ![Edit button](media/edit-icon.png "Edit button") next to the tag name, and then start typing in the edit box.</span></span>  
  
4.  <span data-ttu-id="a54c6-200">Select **Confirm** ![Apply button](media/check-icon.png "Apply button")</span><span class="sxs-lookup"><span data-stu-id="a54c6-200">Select **Confirm** ![Apply button](media/check-icon.png "Apply button")</span></span>  
  
## <a name="find-posts-with-tags"></a><span data-ttu-id="a54c6-201">Find posts with tags</span><span class="sxs-lookup"><span data-stu-id="a54c6-201">Find posts with tags</span></span>  
<span data-ttu-id="a54c6-202">To quickly find posts with tags use the **Post Tags and Intentions** [filter to configure a data set](use-filters.md).</span><span class="sxs-lookup"><span data-stu-id="a54c6-202">To quickly find posts with tags use the **Post Tags and Intentions** [filter to configure a data set](use-filters.md).</span></span> 
  
### <a name="see-also"></a><span data-ttu-id="a54c6-203">See Also</span><span class="sxs-lookup"><span data-stu-id="a54c6-203">See Also</span></span>  
<span data-ttu-id="a54c6-204">[Manage global settings](manage-global-settings.md) </span><span class="sxs-lookup"><span data-stu-id="a54c6-204">[Manage global settings](manage-global-settings.md) </span></span>  
[<span data-ttu-id="a54c6-205">Work with posts</span><span class="sxs-lookup"><span data-stu-id="a54c6-205">Work with posts</span></span>](work-with-posts.md)
