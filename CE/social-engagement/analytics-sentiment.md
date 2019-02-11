---
title: Analytics for sentiment in Social Engagement | Microsoft Docs
description: Learn how to focus your analysis on sentiment and tonality in Social Engagement.
keywords: sentiment, natural language processing, tonality, analytics, sentiment analysis
ms.date: 12/14/2018
ms.service: dynamics-365-marketing
ms.topic: article
applies_to:
- Social Engagement
ms.assetid: eafeef08-d2ea-470a-a538-9010b19bb7dd
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
ms.openlocfilehash: 697b1833ba23e0d4bfb6171fb346ecde3251265b
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "375344"
---
# <a name="understand-public-perception-using-sentiment-analysis"></a><span data-ttu-id="e792c-104">Understand public perception using sentiment analysis</span><span class="sxs-lookup"><span data-stu-id="e792c-104">Understand public perception using sentiment analysis</span></span>

<span data-ttu-id="e792c-105">View and understand social sentiment in posts that are found by your search topics.</span><span class="sxs-lookup"><span data-stu-id="e792c-105">View and understand social sentiment in posts that are found by your search topics.</span></span> <span data-ttu-id="e792c-106">Sentiment analysis in [!INCLUDE[pn_netbreeze_long](../includes/pn-social-engagement-long.md)] calculates the sentiment value of social posts using natural-language processing and machine learning techniques.</span><span class="sxs-lookup"><span data-stu-id="e792c-106">Sentiment analysis in [!INCLUDE[pn_netbreeze_long](../includes/pn-social-engagement-long.md)] calculates the sentiment value of social posts using natural-language processing and machine learning techniques.</span></span> 

<span data-ttu-id="e792c-107">In [!INCLUDE[pn-social-engagement-short](../includes/pn-social-engagement-short.md)], go to **Analytics** > **Sentiment** to learn more  about sentiment across posts in your data set.</span><span class="sxs-lookup"><span data-stu-id="e792c-107">In [!INCLUDE[pn-social-engagement-short](../includes/pn-social-engagement-short.md)], go to **Analytics** > **Sentiment** to learn more  about sentiment across posts in your data set.</span></span>  

<span data-ttu-id="e792c-108">![Screenshot of the sentiment page in the Analytics area of Social Engagement](media/analytics-sentiment.png "Screenshot of the sentiment page in the Analytics area of Social Engagement")</span><span class="sxs-lookup"><span data-stu-id="e792c-108">![Screenshot of the sentiment page in the Analytics area of Social Engagement](media/analytics-sentiment.png "Screenshot of the sentiment page in the Analytics area of Social Engagement")</span></span>

## <a name="sentmient-value"></a><span data-ttu-id="e792c-109">Sentmient value</span><span class="sxs-lookup"><span data-stu-id="e792c-109">Sentmient value</span></span>

<span data-ttu-id="e792c-110">**Sentiment value** is the positive, negative, neutral, or unknown sentiment for a post.</span><span class="sxs-lookup"><span data-stu-id="e792c-110">**Sentiment value** is the positive, negative, neutral, or unknown sentiment for a post.</span></span> <span data-ttu-id="e792c-111">Occasionally, the algorithm identifies positive and negative parts of a sentence and rates the post as neutral, because the amount of positive or negative text cancel each other out. You can [edit and confirm sentiment values](work-with-posts.md) for individual posts to benefit from [adaptive learning](adaptive-learning.md) for your organization's sentiment algorithm.</span><span class="sxs-lookup"><span data-stu-id="e792c-111">Occasionally, the algorithm identifies positive and negative parts of a sentence and rates the post as neutral, because the amount of positive or negative text cancel each other out. You can [edit and confirm sentiment values](work-with-posts.md) for individual posts to benefit from [adaptive learning](adaptive-learning.md) for your organization's sentiment algorithm.</span></span> <span data-ttu-id="e792c-112">An unknown sentiment value indicates that the language isn’t supported by the sentiment algorithm.</span><span class="sxs-lookup"><span data-stu-id="e792c-112">An unknown sentiment value indicates that the language isn’t supported by the sentiment algorithm.</span></span> 

## <a name="sentiment-index"></a><span data-ttu-id="e792c-113">Sentiment index</span><span class="sxs-lookup"><span data-stu-id="e792c-113">Sentiment index</span></span>

<span data-ttu-id="e792c-114">The **sentiment index** is calculated from the sentiment value of posts and normalized to a value between -10 and 10.</span><span class="sxs-lookup"><span data-stu-id="e792c-114">The **sentiment index** is calculated from the sentiment value of posts and normalized to a value between -10 and 10.</span></span> <span data-ttu-id="e792c-115">All your active filters and parameters are considered to define the data set that the sentiment index calculates.</span><span class="sxs-lookup"><span data-stu-id="e792c-115">All your active filters and parameters are considered to define the data set that the sentiment index calculates.</span></span>  
  
-   <span data-ttu-id="e792c-116">A sentiment index of 10 means that there are no negative posts in your data set.</span><span class="sxs-lookup"><span data-stu-id="e792c-116">A sentiment index of 10 means that there are no negative posts in your data set.</span></span>  
  
-   <span data-ttu-id="e792c-117">A sentiment index of 0 means that there are equal amounts of positive and negative posts in your data set.</span><span class="sxs-lookup"><span data-stu-id="e792c-117">A sentiment index of 0 means that there are equal amounts of positive and negative posts in your data set.</span></span>  
  
-   <span data-ttu-id="e792c-118">A sentiment index of -10 means that there are no positive posts in your data set.</span><span class="sxs-lookup"><span data-stu-id="e792c-118">A sentiment index of -10 means that there are no positive posts in your data set.</span></span>  
  
<span data-ttu-id="e792c-119">Formula:</span><span class="sxs-lookup"><span data-stu-id="e792c-119">Formula:</span></span>  
  
`Sentiment index = (Positive posts – Negative posts)/(Positive posts + Negative posts) * 10`    

## <a name="authors"></a><span data-ttu-id="e792c-120">Authors</span><span class="sxs-lookup"><span data-stu-id="e792c-120">Authors</span></span>

<span data-ttu-id="e792c-121">The normal view of this widget shows the top five authors and sources, based on the volume of posts and trend indicator.</span><span class="sxs-lookup"><span data-stu-id="e792c-121">The normal view of this widget shows the top five authors and sources, based on the volume of posts and trend indicator.</span></span> <span data-ttu-id="e792c-122">Select the **Full view** button ![Full view button](media/open-full-view-icon.png "Full view button") to expand the widget and find more details such as reach, source, and location about the 100 most-active authors and their posts.</span><span class="sxs-lookup"><span data-stu-id="e792c-122">Select the **Full view** button ![Full view button](media/open-full-view-icon.png "Full view button") to expand the widget and find more details such as reach, source, and location about the 100 most-active authors and their posts.</span></span>    
<span data-ttu-id="e792c-123">To add a filter for multiple authors at once, select the check boxes on the left side of the list for all authors that you want to include.</span><span class="sxs-lookup"><span data-stu-id="e792c-123">To add a filter for multiple authors at once, select the check boxes on the left side of the list for all authors that you want to include.</span></span> <span data-ttu-id="e792c-124">Then select **INCLUDE** in the list header.</span><span class="sxs-lookup"><span data-stu-id="e792c-124">Then select **INCLUDE** in the list header.</span></span> <span data-ttu-id="e792c-125">To remove an author from the authors filter, select the check boxes on the left side of the list for all authors that you want to remove from the filter.</span><span class="sxs-lookup"><span data-stu-id="e792c-125">To remove an author from the authors filter, select the check boxes on the left side of the list for all authors that you want to remove from the filter.</span></span> <span data-ttu-id="e792c-126">Then select **EXCLUDE** in the list header.</span><span class="sxs-lookup"><span data-stu-id="e792c-126">Then select **EXCLUDE** in the list header.</span></span>
> [!NOTE]
> <span data-ttu-id="e792c-127">Full view also has a **Delete** button ![Delete button](media/trashbin-icon.png "Delete button") that you can use to [delete a selected author](manage-authors.md) and the author’s posts.</span><span class="sxs-lookup"><span data-stu-id="e792c-127">Full view also has a **Delete** button ![Delete button](media/trashbin-icon.png "Delete button") that you can use to [delete a selected author](manage-authors.md) and the author’s posts.</span></span> <span data-ttu-id="e792c-128">You must have a **Power Analyst** or **Administrator** user role to delete an author.</span><span class="sxs-lookup"><span data-stu-id="e792c-128">You must have a **Power Analyst** or **Administrator** user role to delete an author.</span></span>
> <span data-ttu-id="e792c-129">When you delete an author, none of the author’s posts will be available in the solution’s database; they are permanently deleted.</span><span class="sxs-lookup"><span data-stu-id="e792c-129">When you delete an author, none of the author’s posts will be available in the solution’s database; they are permanently deleted.</span></span> <span data-ttu-id="e792c-130">No new posts from this author will be acquired in the future.</span><span class="sxs-lookup"><span data-stu-id="e792c-130">No new posts from this author will be acquired in the future.</span></span>  

## <a name="location-insights"></a><span data-ttu-id="e792c-131">Location insights</span><span class="sxs-lookup"><span data-stu-id="e792c-131">Location insights</span></span>

<span data-ttu-id="e792c-132">Posts that include location information display on a map to show where the posts are coming from.</span><span class="sxs-lookup"><span data-stu-id="e792c-132">Posts that include location information display on a map to show where the posts are coming from.</span></span> <span data-ttu-id="e792c-133">You can also [define an activity map](activity-maps.md) to see new posts in real-time, with additional functionality.</span><span class="sxs-lookup"><span data-stu-id="e792c-133">You can also [define an activity map](activity-maps.md) to see new posts in real-time, with additional functionality.</span></span> 

<span data-ttu-id="e792c-134">Dynamic widget.</span><span class="sxs-lookup"><span data-stu-id="e792c-134">Dynamic widget.</span></span> <span data-ttu-id="e792c-135">Shows only if posts with location information are available in the selected data set.</span><span class="sxs-lookup"><span data-stu-id="e792c-135">Shows only if posts with location information are available in the selected data set.</span></span>

## <a name="negative-phrases"></a><span data-ttu-id="e792c-136">Negative phrases</span><span class="sxs-lookup"><span data-stu-id="e792c-136">Negative phrases</span></span>

<span data-ttu-id="e792c-137">Lists often-mentioned negative phrases, based on the posts in your current data set.</span><span class="sxs-lookup"><span data-stu-id="e792c-137">Lists often-mentioned negative phrases, based on the posts in your current data set.</span></span> <span data-ttu-id="e792c-138">The larger that a phrase appears, the more posts contain this phrase.</span><span class="sxs-lookup"><span data-stu-id="e792c-138">The larger that a phrase appears, the more posts contain this phrase.</span></span>

## <a name="positive-phrases"></a><span data-ttu-id="e792c-139">Positive phrases</span><span class="sxs-lookup"><span data-stu-id="e792c-139">Positive phrases</span></span>

<span data-ttu-id="e792c-140">Lists often-mentioned positive phrases, based on the posts in your current data set.</span><span class="sxs-lookup"><span data-stu-id="e792c-140">Lists often-mentioned positive phrases, based on the posts in your current data set.</span></span> <span data-ttu-id="e792c-141">The larger a phrase appears, the more posts contain this phrase.</span><span class="sxs-lookup"><span data-stu-id="e792c-141">The larger a phrase appears, the more posts contain this phrase.</span></span>

## <a name="sentiment"></a><span data-ttu-id="e792c-142">Sentiment</span><span class="sxs-lookup"><span data-stu-id="e792c-142">Sentiment</span></span>

<span data-ttu-id="e792c-143">Visualizes the sentiment index across all posts that have a sentiment value in the selected data set.</span><span class="sxs-lookup"><span data-stu-id="e792c-143">Visualizes the sentiment index across all posts that have a sentiment value in the selected data set.</span></span> <span data-ttu-id="e792c-144">It also shows the change in sentiment index compared to the last similar time frame and trend indicator.</span><span class="sxs-lookup"><span data-stu-id="e792c-144">It also shows the change in sentiment index compared to the last similar time frame and trend indicator.</span></span>    
<span data-ttu-id="e792c-145">You can [manually change the sentiment values](analytics-sentiment.md) if you find that a post's sentiment is analyzed incorrectly.</span><span class="sxs-lookup"><span data-stu-id="e792c-145">You can [manually change the sentiment values](analytics-sentiment.md) if you find that a post's sentiment is analyzed incorrectly.</span></span> 

## <a name="sentiment-coverage"></a><span data-ttu-id="e792c-146">Sentiment coverage</span><span class="sxs-lookup"><span data-stu-id="e792c-146">Sentiment coverage</span></span>

<span data-ttu-id="e792c-147">Shows the relative distribution of system-rated and manually edited sentiment values.</span><span class="sxs-lookup"><span data-stu-id="e792c-147">Shows the relative distribution of system-rated and manually edited sentiment values.</span></span> 

## <a name="sentiment-history"></a><span data-ttu-id="e792c-148">Sentiment history</span><span class="sxs-lookup"><span data-stu-id="e792c-148">Sentiment history</span></span>

<span data-ttu-id="e792c-149">Shows the number of posts with sentiment value, the sentiment index, and the average sentiment value for a selected time frame.</span><span class="sxs-lookup"><span data-stu-id="e792c-149">Shows the number of posts with sentiment value, the sentiment index, and the average sentiment value for a selected time frame.</span></span>

## <a name="sentiment-by-source"></a><span data-ttu-id="e792c-150">Sentiment by source</span><span class="sxs-lookup"><span data-stu-id="e792c-150">Sentiment by source</span></span>

<span data-ttu-id="e792c-151">Lists the sentiment index for the top five sources and trend indicators.</span><span class="sxs-lookup"><span data-stu-id="e792c-151">Lists the sentiment index for the top five sources and trend indicators.</span></span>

## <a name="top-critics"></a><span data-ttu-id="e792c-152">Top critics</span><span class="sxs-lookup"><span data-stu-id="e792c-152">Top critics</span></span>

<span data-ttu-id="e792c-153">Lists the authors who published the most posts with a negative sentiment value.</span><span class="sxs-lookup"><span data-stu-id="e792c-153">Lists the authors who published the most posts with a negative sentiment value.</span></span>

## <a name="top-fans"></a><span data-ttu-id="e792c-154">Top fans</span><span class="sxs-lookup"><span data-stu-id="e792c-154">Top fans</span></span>

<span data-ttu-id="e792c-155">Lists the authors who published the most posts with a positive sentiment value.</span><span class="sxs-lookup"><span data-stu-id="e792c-155">Lists the authors who published the most posts with a positive sentiment value.</span></span>
  
### <a name="see-also"></a><span data-ttu-id="e792c-156">See Also</span><span class="sxs-lookup"><span data-stu-id="e792c-156">See Also</span></span>

<span data-ttu-id="e792c-157">[Analyze social data using widgets](analyze-social-data-using-widgets.md) </span><span class="sxs-lookup"><span data-stu-id="e792c-157">[Analyze social data using widgets](analyze-social-data-using-widgets.md) </span></span>  
<span data-ttu-id="e792c-158">[Get to know your filters](use-filters.md)  </span><span class="sxs-lookup"><span data-stu-id="e792c-158">[Get to know your filters](use-filters.md)  </span></span>  
[<span data-ttu-id="e792c-159">Explore more options with your data set</span><span class="sxs-lookup"><span data-stu-id="e792c-159">Explore more options with your data set</span></span>](more-options-with-data-set.md)    
