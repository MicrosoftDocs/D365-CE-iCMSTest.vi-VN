---
title: Define activity maps in Social Engagement | Microsoft Docs
description: Learn how to configure activity maps in Social Engagement to view real-time data on a map.
keywords: activiy map, localtion analysis, live map
ms.date: 07/11/2018
ms.service: dynamics-365-marketing
ms.topic: article
applies_to:
- Social Engagement
ms.assetid: 33326ad3-89ea-4a12-803e-b6c98cf1757f
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
ms.openlocfilehash: 62b66758375ab2cb60f6282ebc9383f7ca5981bb
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "375357"
---
# <a name="define-activity-maps-to-view-real-time-data"></a><span data-ttu-id="28b4f-104">Define activity maps to view real-time data</span><span class="sxs-lookup"><span data-stu-id="28b4f-104">Define activity maps to view real-time data</span></span>
<span data-ttu-id="28b4f-105">Using activity maps, you can view real-time posts by geographical location on an easy-to-understand map.</span><span class="sxs-lookup"><span data-stu-id="28b4f-105">Using activity maps, you can view real-time posts by geographical location on an easy-to-understand map.</span></span> <span data-ttu-id="28b4f-106">You can further view these posts in Analytics to understand more details and associated metrics.</span><span class="sxs-lookup"><span data-stu-id="28b4f-106">You can further view these posts in Analytics to understand more details and associated metrics.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="28b4f-107">You can only visualize those posts on an activity map that have location data for posts or authors.</span><span class="sxs-lookup"><span data-stu-id="28b4f-107">You can only visualize those posts on an activity map that have location data for posts or authors.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="28b4f-108">[See the locations for the posts](analytics-location.md), [Analyze the sources for the posts](analytics-sources.md)</span><span class="sxs-lookup"><span data-stu-id="28b4f-108">[See the locations for the posts](analytics-location.md), [Analyze the sources for the posts](analytics-sources.md)</span></span>  
  
## <a name="role-privileges"></a><span data-ttu-id="28b4f-109">Role privileges</span><span class="sxs-lookup"><span data-stu-id="28b4f-109">Role privileges</span></span>  
<span data-ttu-id="28b4f-110">Every user can create activity maps in [!INCLUDE[pn_netbreeze_long](../includes/pn-social-engagement-long.md)], regardless of user role or license type.</span><span class="sxs-lookup"><span data-stu-id="28b4f-110">Every user can create activity maps in [!INCLUDE[pn_netbreeze_long](../includes/pn-social-engagement-long.md)], regardless of user role or license type.</span></span> <span data-ttu-id="28b4f-111">Activity maps are saved and displayed separately for every user.</span><span class="sxs-lookup"><span data-stu-id="28b4f-111">Activity maps are saved and displayed separately for every user.</span></span> <span data-ttu-id="28b4f-112">You can only view the activity maps you create.</span><span class="sxs-lookup"><span data-stu-id="28b4f-112">You can only view the activity maps you create.</span></span>  
  
<a name="createactivitymap"></a>   
## <a name="create-an-activity-map"></a><span data-ttu-id="28b4f-113">Create an activity map</span><span class="sxs-lookup"><span data-stu-id="28b4f-113">Create an activity map</span></span>  
  
1. <span data-ttu-id="28b4f-114">Go to **Activity Maps**.</span><span class="sxs-lookup"><span data-stu-id="28b4f-114">Go to **Activity Maps**.</span></span>  
2. <span data-ttu-id="28b4f-115">On the **Activity Maps** pane, click the **Add** button ![Add button](media/add-icon.png "Add button").</span><span class="sxs-lookup"><span data-stu-id="28b4f-115">On the **Activity Maps** pane, click the **Add** button ![Add button](media/add-icon.png "Add button").</span></span>  
3. <span data-ttu-id="28b4f-116">Enter the details on the **Activity Maps Details** page.</span><span class="sxs-lookup"><span data-stu-id="28b4f-116">Enter the details on the **Activity Maps Details** page.</span></span>  
  
   - <span data-ttu-id="28b4f-117">**Name**: Enter a name for the new activity map.</span><span class="sxs-lookup"><span data-stu-id="28b4f-117">**Name**: Enter a name for the new activity map.</span></span>  
  
   - <span data-ttu-id="28b4f-118">**Default time span**: Select the default time span for which you want to view the posts for this activity map.</span><span class="sxs-lookup"><span data-stu-id="28b4f-118">**Default time span**: Select the default time span for which you want to view the posts for this activity map.</span></span> <span data-ttu-id="28b4f-119">You can change this value at any time, even when you view the map.</span><span class="sxs-lookup"><span data-stu-id="28b4f-119">You can change this value at any time, even when you view the map.</span></span> <span data-ttu-id="28b4f-120">**Options**: Past 30 minutes, Past hour, Past 12 hours, Past 24 hours.</span><span class="sxs-lookup"><span data-stu-id="28b4f-120">**Options**: Past 30 minutes, Past hour, Past 12 hours, Past 24 hours.</span></span>  
  
   - <span data-ttu-id="28b4f-121">**Default map type**: Select the default type of the map that you want to view when you open this activity map.</span><span class="sxs-lookup"><span data-stu-id="28b4f-121">**Default map type**: Select the default type of the map that you want to view when you open this activity map.</span></span>  
  
       - <span data-ttu-id="28b4f-122">**Buzz map**: Displays the volume of posts in various locations.</span><span class="sxs-lookup"><span data-stu-id="28b4f-122">**Buzz map**: Displays the volume of posts in various locations.</span></span>  
  
       - <span data-ttu-id="28b4f-123">**Sentiment map:** Displays the sentiment values for the conversations, based on the location.</span><span class="sxs-lookup"><span data-stu-id="28b4f-123">**Sentiment map:** Displays the sentiment values for the conversations, based on the location.</span></span>  
  
   - <span data-ttu-id="28b4f-124">**Filters**: Select the filters you want to create the activity map from.</span><span class="sxs-lookup"><span data-stu-id="28b4f-124">**Filters**: Select the filters you want to create the activity map from.</span></span> <span data-ttu-id="28b4f-125">You can use **All Search Topics** or choose **Change** ![Edit button](media/edit-icon.png "Edit button") to select filters.</span><span class="sxs-lookup"><span data-stu-id="28b4f-125">You can use **All Search Topics** or choose **Change** ![Edit button](media/edit-icon.png "Edit button") to select filters.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="28b4f-126">[Get relevant data using filters](use-filters.md)</span><span class="sxs-lookup"><span data-stu-id="28b4f-126">[Get relevant data using filters](use-filters.md)</span></span>  
  
       > [!IMPORTANT]
       >  <span data-ttu-id="28b4f-127">Make sure that your data set contains posts that the activity map can display.</span><span class="sxs-lookup"><span data-stu-id="28b4f-127">Make sure that your data set contains posts that the activity map can display.</span></span> <span data-ttu-id="28b4f-128">If you configure an activity map that has a data set that doesn't include location information (for example, if you filter only by Blogs, which don't support location data), the activity map won't display any data.</span><span class="sxs-lookup"><span data-stu-id="28b4f-128">If you configure an activity map that has a data set that doesn't include location information (for example, if you filter only by Blogs, which don't support location data), the activity map won't display any data.</span></span>
  
4. <span data-ttu-id="28b4f-129">When you're done, click **Save**.</span><span class="sxs-lookup"><span data-stu-id="28b4f-129">When you're done, click **Save**.</span></span>  
  
> [!TIP]
>  <span data-ttu-id="28b4f-130">To edit an activity map, open the map details and repeat from step 3.</span><span class="sxs-lookup"><span data-stu-id="28b4f-130">To edit an activity map, open the map details and repeat from step 3.</span></span>  
  
## <a name="view-an-activity-map"></a><span data-ttu-id="28b4f-131">View an activity map</span><span class="sxs-lookup"><span data-stu-id="28b4f-131">View an activity map</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="28b4f-132">If you have not created any activity maps, no maps will be displayed for you.</span><span class="sxs-lookup"><span data-stu-id="28b4f-132">If you have not created any activity maps, no maps will be displayed for you.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="28b4f-133">[Create an activity map](activity-maps.md#createactivitymap)</span><span class="sxs-lookup"><span data-stu-id="28b4f-133">[Create an activity map](activity-maps.md#createactivitymap)</span></span>  
  
1.  <span data-ttu-id="28b4f-134">Go to **Activity Maps**.</span><span class="sxs-lookup"><span data-stu-id="28b4f-134">Go to **Activity Maps**.</span></span>  
  
2.  <span data-ttu-id="28b4f-135">From the list, select the activity map, and then click the globe button ![Globe](media/globe-icon.png "Globe") to see the default view of the selected activity map.</span><span class="sxs-lookup"><span data-stu-id="28b4f-135">From the list, select the activity map, and then click the globe button ![Globe](media/globe-icon.png "Globe") to see the default view of the selected activity map.</span></span>  
  
3.  <span data-ttu-id="28b4f-136">Single posts are repesented in smaller shapes than post clusters.</span><span class="sxs-lookup"><span data-stu-id="28b4f-136">Single posts are repesented in smaller shapes than post clusters.</span></span> 

<span data-ttu-id="28b4f-137">An outline indicates how old a post or cluster is.</span><span class="sxs-lookup"><span data-stu-id="28b4f-137">An outline indicates how old a post or cluster is.</span></span> <span data-ttu-id="28b4f-138">New posts show a circle.</span><span class="sxs-lookup"><span data-stu-id="28b4f-138">New posts show a circle.</span></span> <span data-ttu-id="28b4f-139">The older the post, the smaller the outline.</span><span class="sxs-lookup"><span data-stu-id="28b4f-139">The older the post, the smaller the outline.</span></span> 

<span data-ttu-id="28b4f-140">The Sentiment map additionally shows the colors and shapes for the corresponding sentiment values of the posts.</span><span class="sxs-lookup"><span data-stu-id="28b4f-140">The Sentiment map additionally shows the colors and shapes for the corresponding sentiment values of the posts.</span></span>  
  
4.  <span data-ttu-id="28b4f-141">Click **Posts** on the right side of the map to view the list of posts for the map.</span><span class="sxs-lookup"><span data-stu-id="28b4f-141">Click **Posts** on the right side of the map to view the list of posts for the map.</span></span>  
  
    > [!TIP]
    >  <span data-ttu-id="28b4f-142">Choose any data point on the map to view the posts corresponding to that area.</span><span class="sxs-lookup"><span data-stu-id="28b4f-142">Choose any data point on the map to view the posts corresponding to that area.</span></span>  
  
5.  <span data-ttu-id="28b4f-143">Click **Insights** on the left side of the map to view the phrases for the trending conversations.</span><span class="sxs-lookup"><span data-stu-id="28b4f-143">Click **Insights** on the left side of the map to view the phrases for the trending conversations.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="28b4f-144">Posts deleted or edited from any other area of [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] will have applicable changes reflected in the map you are viewing in real time.</span><span class="sxs-lookup"><span data-stu-id="28b4f-144">Posts deleted or edited from any other area of [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] will have applicable changes reflected in the map you are viewing in real time.</span></span> <span data-ttu-id="28b4f-145">For example, if you are viewing a sentiment map for a location that has a post with neutral sentiment value, and you or any other [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] user edits this post’s sentiment as positive from another application area, say Analytics.</span><span class="sxs-lookup"><span data-stu-id="28b4f-145">For example, if you are viewing a sentiment map for a location that has a post with neutral sentiment value, and you or any other [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] user edits this post’s sentiment as positive from another application area, say Analytics.</span></span> <span data-ttu-id="28b4f-146">Then, the new positive sentiment value will be reflected for this post on the map.</span><span class="sxs-lookup"><span data-stu-id="28b4f-146">Then, the new positive sentiment value will be reflected for this post on the map.</span></span> <span data-ttu-id="28b4f-147">You will no longer see the sentiment value as neutral for this post.</span><span class="sxs-lookup"><span data-stu-id="28b4f-147">You will no longer see the sentiment value as neutral for this post.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="28b4f-148">[Understand the public perception using sentiment analysis](analytics-sentiment.md)</span><span class="sxs-lookup"><span data-stu-id="28b4f-148">[Understand the public perception using sentiment analysis](analytics-sentiment.md)</span></span>  
> 
> [!TIP]
>  <span data-ttu-id="28b4f-149">Use the buttons in the lower-left corner of the map to zoom in or zoom out of the map.</span><span class="sxs-lookup"><span data-stu-id="28b4f-149">Use the buttons in the lower-left corner of the map to zoom in or zoom out of the map.</span></span>  
  
 <span data-ttu-id="28b4f-150">**Sample activity map**</span><span class="sxs-lookup"><span data-stu-id="28b4f-150">**Sample activity map**</span></span>  
  
 <span data-ttu-id="28b4f-151">![Activity map in Social Engagement](media/activity-map.png "Activity map in Social Engagement")</span><span class="sxs-lookup"><span data-stu-id="28b4f-151">![Activity map in Social Engagement](media/activity-map.png "Activity map in Social Engagement")</span></span>  
  
## <a name="view-and-understand-sentiment-values-on-an-activity-map"></a><span data-ttu-id="28b4f-152">View and understand sentiment values on an activity map</span><span class="sxs-lookup"><span data-stu-id="28b4f-152">View and understand sentiment values on an activity map</span></span>  
  
1. <span data-ttu-id="28b4f-153">Go to **Activity Maps**.</span><span class="sxs-lookup"><span data-stu-id="28b4f-153">Go to **Activity Maps**.</span></span>  
  
2. <span data-ttu-id="28b4f-154">From the list, select the activity map, and then click the globe button ![Globe](media/globe-icon.png "Globe").</span><span class="sxs-lookup"><span data-stu-id="28b4f-154">From the list, select the activity map, and then click the globe button ![Globe](media/globe-icon.png "Globe").</span></span>  
  
3. <span data-ttu-id="28b4f-155">In the header area, click **Sentiment map** if sentiment map is not your default view.</span><span class="sxs-lookup"><span data-stu-id="28b4f-155">In the header area, click **Sentiment map** if sentiment map is not your default view.</span></span>  
  
4. <span data-ttu-id="28b4f-156">Read the sentiment values on the activity map: green with upward-facing triangle for positive sentiment, red with downward-facing triangle for negative, and gray with a diamond shape for neutral sentiment.</span><span class="sxs-lookup"><span data-stu-id="28b4f-156">Read the sentiment values on the activity map: green with upward-facing triangle for positive sentiment, red with downward-facing triangle for negative, and gray with a diamond shape for neutral sentiment.</span></span>  
  
   > [!TIP]
   >  <span data-ttu-id="28b4f-157">In the header section, the sentiment map denotes the legend in detail.</span><span class="sxs-lookup"><span data-stu-id="28b4f-157">In the header section, the sentiment map denotes the legend in detail.</span></span> <span data-ttu-id="28b4f-158">Select the appropriate button in the sentiment filter widget (next to the map legend) to filter the activity map for a specific sentiment value and view it.</span><span class="sxs-lookup"><span data-stu-id="28b4f-158">Select the appropriate button in the sentiment filter widget (next to the map legend) to filter the activity map for a specific sentiment value and view it.</span></span>  
   > 
   >  <span data-ttu-id="28b4f-159">Click the green button ![Positive sentiment](media/positive-sentiment-symbol.png "Positive sentiment") to view only positive sentiment, the red button ![Negative sentiment](media/negative-sentiment-symbol.png "Negative sentiment") to view negative sentiment, and the gray button for neutral sentiment ![Neutral sentiment](media/neutral-sentiment-symbol.png "Neutral sentiment").</span><span class="sxs-lookup"><span data-stu-id="28b4f-159">Click the green button ![Positive sentiment](media/positive-sentiment-symbol.png "Positive sentiment") to view only positive sentiment, the red button ![Negative sentiment](media/negative-sentiment-symbol.png "Negative sentiment") to view negative sentiment, and the gray button for neutral sentiment ![Neutral sentiment](media/neutral-sentiment-symbol.png "Neutral sentiment").</span></span> <span data-ttu-id="28b4f-160">You can select more than one value.</span><span class="sxs-lookup"><span data-stu-id="28b4f-160">You can select more than one value.</span></span>  
   > 
   >  <span data-ttu-id="28b4f-161">When you select a specific sentiment value&mdash;for example, Positive&mdash;only posts with positive sentiment will be displayed on the map, and the positive sentiment button on the header shows 100%.</span><span class="sxs-lookup"><span data-stu-id="28b4f-161">When you select a specific sentiment value&mdash;for example, Positive&mdash;only posts with positive sentiment will be displayed on the map, and the positive sentiment button on the header shows 100%.</span></span> <span data-ttu-id="28b4f-162">All KPIs and charts will be filtered by the selection you make on the sentiment filter.</span><span class="sxs-lookup"><span data-stu-id="28b4f-162">All KPIs and charts will be filtered by the selection you make on the sentiment filter.</span></span>  
   > 
   >  <span data-ttu-id="28b4f-163">When you select all three of the sentiment values, respective percentages for all the sentiments will be displayed.</span><span class="sxs-lookup"><span data-stu-id="28b4f-163">When you select all three of the sentiment values, respective percentages for all the sentiments will be displayed.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="28b4f-164">[Understand the public perception using sentiment analysis](analytics-sentiment.md)</span><span class="sxs-lookup"><span data-stu-id="28b4f-164">[Understand the public perception using sentiment analysis](analytics-sentiment.md)</span></span>  
  
## <a name="view-and-edit-posts-on-an-activity-map"></a><span data-ttu-id="28b4f-165">View and edit posts on an activity map</span><span class="sxs-lookup"><span data-stu-id="28b4f-165">View and edit posts on an activity map</span></span>  
  
1. <span data-ttu-id="28b4f-166">Go to **Activity Maps**.</span><span class="sxs-lookup"><span data-stu-id="28b4f-166">Go to **Activity Maps**.</span></span>  
  
2. <span data-ttu-id="28b4f-167">From the list, select the activity map, and then click the globe button ![Globe](media/globe-icon.png "Globe").</span><span class="sxs-lookup"><span data-stu-id="28b4f-167">From the list, select the activity map, and then click the globe button ![Globe](media/globe-icon.png "Globe").</span></span>  
  
3. <span data-ttu-id="28b4f-168">On the right side of the map, click **Posts**.</span><span class="sxs-lookup"><span data-stu-id="28b4f-168">On the right side of the map, click **Posts**.</span></span>  
  
4. <span data-ttu-id="28b4f-169">Select the post from the list, and then perform the required actions.</span><span class="sxs-lookup"><span data-stu-id="28b4f-169">Select the post from the list, and then perform the required actions.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="28b4f-170">[Work with posts](work-with-posts.md)</span><span class="sxs-lookup"><span data-stu-id="28b4f-170">[Work with posts](work-with-posts.md)</span></span>  
  
## <a name="understand-the-posts-peaks-on-an-activity-map"></a><span data-ttu-id="28b4f-171">Understand the posts peaks on an activity map</span><span class="sxs-lookup"><span data-stu-id="28b4f-171">Understand the posts peaks on an activity map</span></span>  
 <span data-ttu-id="28b4f-172">Activity maps display up to 5,000 posts at a time.</span><span class="sxs-lookup"><span data-stu-id="28b4f-172">Activity maps display up to 5,000 posts at a time.</span></span> <span data-ttu-id="28b4f-173">If your data set contains more fresh posts per hour (or for the selected time span), and the total posts cross the peak value of 5,000, older posts automatically disappear from the map’s display and you always see the latest ones.</span><span class="sxs-lookup"><span data-stu-id="28b4f-173">If your data set contains more fresh posts per hour (or for the selected time span), and the total posts cross the peak value of 5,000, older posts automatically disappear from the map’s display and you always see the latest ones.</span></span> <span data-ttu-id="28b4f-174">In this scenario, the header section of the activity map displays a clickable notification ![Exclamation mark](media/exclamation-mark-symbol.png "Exclamation mark") that provides the current visualization details.</span><span class="sxs-lookup"><span data-stu-id="28b4f-174">In this scenario, the header section of the activity map displays a clickable notification ![Exclamation mark](media/exclamation-mark-symbol.png "Exclamation mark") that provides the current visualization details.</span></span>  
  
## <a name="view-conversation-insights-on-an-activity-map"></a><span data-ttu-id="28b4f-175">View conversation insights on an activity map</span><span class="sxs-lookup"><span data-stu-id="28b4f-175">View conversation insights on an activity map</span></span>  
 <span data-ttu-id="28b4f-176">Understand the top and trending phrases of the current conversations that you’re interested in.</span><span class="sxs-lookup"><span data-stu-id="28b4f-176">Understand the top and trending phrases of the current conversations that you’re interested in.</span></span> <span data-ttu-id="28b4f-177">Watch these further or work on these as required for your business.</span><span class="sxs-lookup"><span data-stu-id="28b4f-177">Watch these further or work on these as required for your business.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="28b4f-178">[Set up searches to listen to social media conversations](set-up-searches.md), [Get connected to the social conversation using Microsoft Social Engagement](get-connected-social-conversation.md)</span><span class="sxs-lookup"><span data-stu-id="28b4f-178">[Set up searches to listen to social media conversations](set-up-searches.md), [Get connected to the social conversation using Microsoft Social Engagement](get-connected-social-conversation.md)</span></span>  
  
> [!TIP]
>  <span data-ttu-id="28b4f-179">Phrases are refreshed when you update the data set or add a new filter.</span><span class="sxs-lookup"><span data-stu-id="28b4f-179">Phrases are refreshed when you update the data set or add a new filter.</span></span>  
  
1. <span data-ttu-id="28b4f-180">Go to **Activity Maps**.</span><span class="sxs-lookup"><span data-stu-id="28b4f-180">Go to **Activity Maps**.</span></span>  
  
2. <span data-ttu-id="28b4f-181">From the list, select the activity map, and then click the globe button ![Globe](media/globe-icon.png "Globe").</span><span class="sxs-lookup"><span data-stu-id="28b4f-181">From the list, select the activity map, and then click the globe button ![Globe](media/globe-icon.png "Globe").</span></span>  
  
3. <span data-ttu-id="28b4f-182">On the left side of the map, click **Insights**.</span><span class="sxs-lookup"><span data-stu-id="28b4f-182">On the left side of the map, click **Insights**.</span></span>  
  
4. <span data-ttu-id="28b4f-183">View the trending phrases from the **Phrases** widget.</span><span class="sxs-lookup"><span data-stu-id="28b4f-183">View the trending phrases from the **Phrases** widget.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="28b4f-184">[Find out what people are talking about](analytics-conversations.md)</span><span class="sxs-lookup"><span data-stu-id="28b4f-184">[Find out what people are talking about](analytics-conversations.md)</span></span>  
  
## <a name="filter-a-specific-area-of-an-activity-map"></a><span data-ttu-id="28b4f-185">Filter a specific area of an activity map</span><span class="sxs-lookup"><span data-stu-id="28b4f-185">Filter a specific area of an activity map</span></span>  
 <span data-ttu-id="28b4f-186">Filter a specific area of your activity map to have a focused view and perform any required actions.</span><span class="sxs-lookup"><span data-stu-id="28b4f-186">Filter a specific area of your activity map to have a focused view and perform any required actions.</span></span>  
  
1.  <span data-ttu-id="28b4f-187">Go to **Activity Maps**.</span><span class="sxs-lookup"><span data-stu-id="28b4f-187">Go to **Activity Maps**.</span></span>  
  
2.  <span data-ttu-id="28b4f-188">From the list, select the activity map, and then click the globe button ![Globe](media/globe-icon.png "Globe").</span><span class="sxs-lookup"><span data-stu-id="28b4f-188">From the list, select the activity map, and then click the globe button ![Globe](media/globe-icon.png "Globe").</span></span>  
  
3.  <span data-ttu-id="28b4f-189">In the header area, click the **Area filter** button ![Area filter](media/area-filter-icon.PNG "Area filter").</span><span class="sxs-lookup"><span data-stu-id="28b4f-189">In the header area, click the **Area filter** button ![Area filter](media/area-filter-icon.PNG "Area filter").</span></span>  
  
4.  <span data-ttu-id="28b4f-190">Use the rectangular selector to focus on a specific area of the map.</span><span class="sxs-lookup"><span data-stu-id="28b4f-190">Use the rectangular selector to focus on a specific area of the map.</span></span>  
  
5.  <span data-ttu-id="28b4f-191">View the real-time data for this area, and perform any required actions.</span><span class="sxs-lookup"><span data-stu-id="28b4f-191">View the real-time data for this area, and perform any required actions.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="28b4f-192">You can zoom in on this area by clicking the magnifier button ![Search button](media/magnifier-icon.png "Search button").</span><span class="sxs-lookup"><span data-stu-id="28b4f-192">You can zoom in on this area by clicking the magnifier button ![Search button](media/magnifier-icon.png "Search button").</span></span>  
  
6.  <span data-ttu-id="28b4f-193">When you’re done, click the area filter button again to disable it, or click ![Area filter disable](media/disable-area-filter-icon.png "Area filter disable") at the top of the selector.</span><span class="sxs-lookup"><span data-stu-id="28b4f-193">When you’re done, click the area filter button again to disable it, or click ![Area filter disable](media/disable-area-filter-icon.png "Area filter disable") at the top of the selector.</span></span>  
  
## <a name="view-an-activity-maps-data-in-other-areas-of-includepn-social-engagement-shortincludespn-social-engagement-shortmd"></a><span data-ttu-id="28b4f-194">View an activity map’s data in other areas of [!INCLUDE[pn-social-engagement-short](../includes/pn-social-engagement-short.md)]</span><span class="sxs-lookup"><span data-stu-id="28b4f-194">View an activity map’s data in other areas of [!INCLUDE[pn-social-engagement-short](../includes/pn-social-engagement-short.md)]</span></span>
  
<span data-ttu-id="28b4f-195">View the data set selected for an activity map in other areas of [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] to further understand the details and arrive at any required metrics.</span><span class="sxs-lookup"><span data-stu-id="28b4f-195">View the data set selected for an activity map in other areas of [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] to further understand the details and arrive at any required metrics.</span></span> <span data-ttu-id="28b4f-196">Click the **More options with current filters** button ![More options with current filters](media/more-options-with-current-filters-icon.png "More options with current filters") in the header of an activity map.</span><span class="sxs-lookup"><span data-stu-id="28b4f-196">Click the **More options with current filters** button ![More options with current filters](media/more-options-with-current-filters-icon.png "More options with current filters") in the header of an activity map.</span></span>  
  
[!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="28b4f-197">[Open a data set in other areas of Social Engagement](more-options-with-data-set.md)</span><span class="sxs-lookup"><span data-stu-id="28b4f-197">[Open a data set in other areas of Social Engagement](more-options-with-data-set.md)</span></span>  
  
## <a name="delete-an-activity-map"></a><span data-ttu-id="28b4f-198">Delete an activity map</span><span class="sxs-lookup"><span data-stu-id="28b4f-198">Delete an activity map</span></span>  
 <span data-ttu-id="28b4f-199">If you don't want to use an activity map anymore, you can delete it from your list.</span><span class="sxs-lookup"><span data-stu-id="28b4f-199">If you don't want to use an activity map anymore, you can delete it from your list.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="28b4f-200">Deleting a activity map doesn’t affect your post quota because you only delete the maps/visualization, but not the posts themselves.</span><span class="sxs-lookup"><span data-stu-id="28b4f-200">Deleting a activity map doesn’t affect your post quota because you only delete the maps/visualization, but not the posts themselves.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="28b4f-201">[Work with posts](work-with-posts.md)</span><span class="sxs-lookup"><span data-stu-id="28b4f-201">[Work with posts](work-with-posts.md)</span></span>  
  
1.  <span data-ttu-id="28b4f-202">Go to **Activity Maps**.</span><span class="sxs-lookup"><span data-stu-id="28b4f-202">Go to **Activity Maps**.</span></span>  
  
2.  <span data-ttu-id="28b4f-203">Select the activity map, and then click the **Delete** button ![Delete button](media/trashbin-icon.png "Delete button") .</span><span class="sxs-lookup"><span data-stu-id="28b4f-203">Select the activity map, and then click the **Delete** button ![Delete button](media/trashbin-icon.png "Delete button") .</span></span>  
  
3.  <span data-ttu-id="28b4f-204">Confirm the deletion.</span><span class="sxs-lookup"><span data-stu-id="28b4f-204">Confirm the deletion.</span></span>  
  
## <a name="view-an-activity-map-on-a-large-screen"></a><span data-ttu-id="28b4f-205">View an activity map on a large screen</span><span class="sxs-lookup"><span data-stu-id="28b4f-205">View an activity map on a large screen</span></span>  
 <span data-ttu-id="28b4f-206">View an activity map on a large screen, in full-screen mode.</span><span class="sxs-lookup"><span data-stu-id="28b4f-206">View an activity map on a large screen, in full-screen mode.</span></span> <span data-ttu-id="28b4f-207">You can display this large screen at prominent places as appropriate for your business to demonstrate the trends about your products, brand, or organization.</span><span class="sxs-lookup"><span data-stu-id="28b4f-207">You can display this large screen at prominent places as appropriate for your business to demonstrate the trends about your products, brand, or organization.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="28b4f-208">You can display an activity map on a large screen without a need for any user interaction for 30 days.</span><span class="sxs-lookup"><span data-stu-id="28b4f-208">You can display an activity map on a large screen without a need for any user interaction for 30 days.</span></span> <span data-ttu-id="28b4f-209">After 30 days, you need to [sign in](https://social.dynamics.com/login) again.</span><span class="sxs-lookup"><span data-stu-id="28b4f-209">After 30 days, you need to [sign in](https://social.dynamics.com/login) again.</span></span>  
  
1. <span data-ttu-id="28b4f-210">Go to **Activity Maps**.</span><span class="sxs-lookup"><span data-stu-id="28b4f-210">Go to **Activity Maps**.</span></span>  
  
2. <span data-ttu-id="28b4f-211">From the list, select the activity map to view, and then click the globe button ![Globe](media/globe-icon.png "Globe").</span><span class="sxs-lookup"><span data-stu-id="28b4f-211">From the list, select the activity map to view, and then click the globe button ![Globe](media/globe-icon.png "Globe").</span></span>  
  
3. <span data-ttu-id="28b4f-212">On the lower right side of the map, click the **Open the activity map in full screen** button ![Full screen enable](media/enable-fullscreen-activity-map.png "Full screen enable").</span><span class="sxs-lookup"><span data-stu-id="28b4f-212">On the lower right side of the map, click the **Open the activity map in full screen** button ![Full screen enable](media/enable-fullscreen-activity-map.png "Full screen enable").</span></span>  
  
   > [!NOTE]
   > - <span data-ttu-id="28b4f-213">You can hide the header for a better view of the map.</span><span class="sxs-lookup"><span data-stu-id="28b4f-213">You can hide the header for a better view of the map.</span></span> <span data-ttu-id="28b4f-214">Click the **Collapse header** button ![Header collapse](media/collapse-header-icon.png "Header collapse") to hide.</span><span class="sxs-lookup"><span data-stu-id="28b4f-214">Click the **Collapse header** button ![Header collapse](media/collapse-header-icon.png "Header collapse") to hide.</span></span>  
   >   -   <span data-ttu-id="28b4f-215">To exit full screen, press escape or click the **Exit full screen mode** button ![Full screen disable](media/disable-fullscreen-activity-map.png "Full screen disable").</span><span class="sxs-lookup"><span data-stu-id="28b4f-215">To exit full screen, press escape or click the **Exit full screen mode** button ![Full screen disable](media/disable-fullscreen-activity-map.png "Full screen disable").</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="28b4f-216">See Also</span><span class="sxs-lookup"><span data-stu-id="28b4f-216">See Also</span></span>  
 <span data-ttu-id="28b4f-217">[Get relevant data using filters](use-filters.md) </span><span class="sxs-lookup"><span data-stu-id="28b4f-217">[Get relevant data using filters](use-filters.md) </span></span>  
 <span data-ttu-id="28b4f-218">[Get started with Social Engagement](get-started.md) </span><span class="sxs-lookup"><span data-stu-id="28b4f-218">[Get started with Social Engagement](get-started.md) </span></span>  
 <span data-ttu-id="28b4f-219">[Analyze social data using widgets](analyze-social-data-using-widgets.md) </span><span class="sxs-lookup"><span data-stu-id="28b4f-219">[Analyze social data using widgets](analyze-social-data-using-widgets.md) </span></span>  
 [<span data-ttu-id="28b4f-220">Keep track of live data streams with Social Center</span><span class="sxs-lookup"><span data-stu-id="28b4f-220">Keep track of live data streams with Social Center</span></span>](social-center.md)
 
