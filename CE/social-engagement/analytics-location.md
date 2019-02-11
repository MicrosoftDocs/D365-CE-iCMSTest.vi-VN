---
title: Analytics for locations in Social Engagement | Microsoft Docs
description: Learn how to focus your analysis on location data in Social Engagement.
keywords: analytics, locations, maps, location analysis
ms.date: 07/11/2018
ms.service: dynamics-365-marketing
ms.topic: article
applies_to:
- Social Engagement
ms.assetid: 8aec5246-e411-4fb9-9790-2bcd94438038
author: m-hartmann
ms.author: mhart
manager: annbe
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
ms.openlocfilehash: 25639d2f2b3ae8ca70ba42bec36f1fea0ec20166
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "375534"
---
# <a name="focus-your-analysis-on-location-data"></a><span data-ttu-id="7c6db-104">Focus your analysis on location data</span><span class="sxs-lookup"><span data-stu-id="7c6db-104">Focus your analysis on location data</span></span>

<span data-ttu-id="7c6db-105">Get insights from geographical location information contained in posts or in authors’ profiles.</span><span class="sxs-lookup"><span data-stu-id="7c6db-105">Get insights from geographical location information contained in posts or in authors’ profiles.</span></span> <span data-ttu-id="7c6db-106">Using the **Location** page, you can analyze your data set with a strong focus on where posts are coming from.</span><span class="sxs-lookup"><span data-stu-id="7c6db-106">Using the **Location** page, you can analyze your data set with a strong focus on where posts are coming from.</span></span>  

<span data-ttu-id="7c6db-107">In [!INCLUDE[pn-social-engagement-short](../includes/pn-social-engagement-short.md)], go to **Analytics** > **Conversations** to access the conversations page.</span><span class="sxs-lookup"><span data-stu-id="7c6db-107">In [!INCLUDE[pn-social-engagement-short](../includes/pn-social-engagement-short.md)], go to **Analytics** > **Conversations** to access the conversations page.</span></span>  

<span data-ttu-id="7c6db-108">![Screenshot of the location page in the Analytics area of Social Engagement](media/analytics-location.png "Screenshot of the location page in the Analytics area of Social Engagement")</span><span class="sxs-lookup"><span data-stu-id="7c6db-108">![Screenshot of the location page in the Analytics area of Social Engagement](media/analytics-location.png "Screenshot of the location page in the Analytics area of Social Engagement")</span></span>

## <a name="types-of-location-data"></a><span data-ttu-id="7c6db-109">Types of location data</span><span class="sxs-lookup"><span data-stu-id="7c6db-109">Types of location data</span></span>  

<span data-ttu-id="7c6db-110">In [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)], two types of location data are available:</span><span class="sxs-lookup"><span data-stu-id="7c6db-110">In [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)], two types of location data are available:</span></span>  

- <span data-ttu-id="7c6db-111">**Author location:** Location data that is shared by a user through a profile, for example, on a user’s [!INCLUDE[tn_twitter](../includes/tn-twitter.md)] profile page.</span><span class="sxs-lookup"><span data-stu-id="7c6db-111">**Author location:** Location data that is shared by a user through a profile, for example, on a user’s [!INCLUDE[tn_twitter](../includes/tn-twitter.md)] profile page.</span></span> <span data-ttu-id="7c6db-112">It is an approximate value, because the system calculates geographical coordinates.</span><span class="sxs-lookup"><span data-stu-id="7c6db-112">It is an approximate value, because the system calculates geographical coordinates.</span></span> <span data-ttu-id="7c6db-113">If no post location is provided by the user, the author location is considered, where available.</span><span class="sxs-lookup"><span data-stu-id="7c6db-113">If no post location is provided by the user, the author location is considered, where available.</span></span>  

- <span data-ttu-id="7c6db-114">**Post location:** Location data that shows where (latitude/longitude) a post was published.</span><span class="sxs-lookup"><span data-stu-id="7c6db-114">**Post location:** Location data that shows where (latitude/longitude) a post was published.</span></span> <span data-ttu-id="7c6db-115">The location can differ greatly between posts from the same author, depending on the settings that are applied when publishing the post.</span><span class="sxs-lookup"><span data-stu-id="7c6db-115">The location can differ greatly between posts from the same author, depending on the settings that are applied when publishing the post.</span></span> <span data-ttu-id="7c6db-116">It is an exact value because geographical coordinates are provided with the post.</span><span class="sxs-lookup"><span data-stu-id="7c6db-116">It is an exact value because geographical coordinates are provided with the post.</span></span>  

<span data-ttu-id="7c6db-117">Both types of location data are available under the [**Location Type** filter](understand-filters.md#location-type) when defining a data set.</span><span class="sxs-lookup"><span data-stu-id="7c6db-117">Both types of location data are available under the [**Location Type** filter](understand-filters.md#location-type) when defining a data set.</span></span> 

<span data-ttu-id="7c6db-118">For the United States, you can choose between two ways of grouping visualized data.</span><span class="sxs-lookup"><span data-stu-id="7c6db-118">For the United States, you can choose between two ways of grouping visualized data.</span></span> <span data-ttu-id="7c6db-119">To see how many posts with location data are available in each subregion, apply a filter for post location and select **Subregions**.</span><span class="sxs-lookup"><span data-stu-id="7c6db-119">To see how many posts with location data are available in each subregion, apply a filter for post location and select **Subregions**.</span></span> <span data-ttu-id="7c6db-120">To see posts with precise geographical information (post location data) on the map, select **Posts**.</span><span class="sxs-lookup"><span data-stu-id="7c6db-120">To see posts with precise geographical information (post location data) on the map, select **Posts**.</span></span>

> [!NOTE]
>  <span data-ttu-id="7c6db-121">Some posts may have both post and author location.</span><span class="sxs-lookup"><span data-stu-id="7c6db-121">Some posts may have both post and author location.</span></span> <span data-ttu-id="7c6db-122">In these cases, the post location information is considered&mdash;not the author location.</span><span class="sxs-lookup"><span data-stu-id="7c6db-122">In these cases, the post location information is considered&mdash;not the author location.</span></span>  

## <a name="sources-that-provide-location-data"></a><span data-ttu-id="7c6db-123">Sources that provide location data</span><span class="sxs-lookup"><span data-stu-id="7c6db-123">Sources that provide location data</span></span>  

<span data-ttu-id="7c6db-124">A subset of available sources provides location data.</span><span class="sxs-lookup"><span data-stu-id="7c6db-124">A subset of available sources provides location data.</span></span> <span data-ttu-id="7c6db-125">Authors need to share their location information, so it can be processed by [!INCLUDE[pn-social-engagement-short](../includes/pn-social-engagement-short.md)].</span><span class="sxs-lookup"><span data-stu-id="7c6db-125">Authors need to share their location information, so it can be processed by [!INCLUDE[pn-social-engagement-short](../includes/pn-social-engagement-short.md)].</span></span>  
## <a name="authors"></a><span data-ttu-id="7c6db-126">Authors</span><span class="sxs-lookup"><span data-stu-id="7c6db-126">Authors</span></span>

<span data-ttu-id="7c6db-127">The normal view of this widget shows the top five authors and sources, based on the volume of posts and trend indicator.</span><span class="sxs-lookup"><span data-stu-id="7c6db-127">The normal view of this widget shows the top five authors and sources, based on the volume of posts and trend indicator.</span></span> <span data-ttu-id="7c6db-128">Select the **Full view** button ![Full view button](media/open-full-view-icon.png "Full view button") to expand the widget and find more details such as reach, source, and location for the 100 most-active authors and their posts.</span><span class="sxs-lookup"><span data-stu-id="7c6db-128">Select the **Full view** button ![Full view button](media/open-full-view-icon.png "Full view button") to expand the widget and find more details such as reach, source, and location for the 100 most-active authors and their posts.</span></span>    
<span data-ttu-id="7c6db-129">To add a filter for multiple authors at once, select the check boxes on the left side of the list for all authors that you want to include.</span><span class="sxs-lookup"><span data-stu-id="7c6db-129">To add a filter for multiple authors at once, select the check boxes on the left side of the list for all authors that you want to include.</span></span> <span data-ttu-id="7c6db-130">Then select **INCLUDE** in the list header.</span><span class="sxs-lookup"><span data-stu-id="7c6db-130">Then select **INCLUDE** in the list header.</span></span> <span data-ttu-id="7c6db-131">To remove an author from the authors filter, select the check boxes on the left side of the list for all authors that you want to remove from the filter.</span><span class="sxs-lookup"><span data-stu-id="7c6db-131">To remove an author from the authors filter, select the check boxes on the left side of the list for all authors that you want to remove from the filter.</span></span> <span data-ttu-id="7c6db-132">Then select **EXCLUDE** in the list header.</span><span class="sxs-lookup"><span data-stu-id="7c6db-132">Then select **EXCLUDE** in the list header.</span></span>

> [!NOTE]
> <span data-ttu-id="7c6db-133">Full view also has a **Delete** button ![Delete button](media/trashbin-icon.png "Delete button") you can use to [delete a selected author](manage-authors.md) and the author’s posts.</span><span class="sxs-lookup"><span data-stu-id="7c6db-133">Full view also has a **Delete** button ![Delete button](media/trashbin-icon.png "Delete button") you can use to [delete a selected author](manage-authors.md) and the author’s posts.</span></span> <span data-ttu-id="7c6db-134">You must have a **Power Analyst** or **Administrator** user role to delete an author.</span><span class="sxs-lookup"><span data-stu-id="7c6db-134">You must have a **Power Analyst** or **Administrator** user role to delete an author.</span></span>
> <span data-ttu-id="7c6db-135">When you delete an author, none of the author’s previous posts will be available in the solution’s database; they are permanently deleted.</span><span class="sxs-lookup"><span data-stu-id="7c6db-135">When you delete an author, none of the author’s previous posts will be available in the solution’s database; they are permanently deleted.</span></span> <span data-ttu-id="7c6db-136">No new posts from this author will be acquired in the future.</span><span class="sxs-lookup"><span data-stu-id="7c6db-136">No new posts from this author will be acquired in the future.</span></span> 

## <a name="cities"></a><span data-ttu-id="7c6db-137">Cities</span><span class="sxs-lookup"><span data-stu-id="7c6db-137">Cities</span></span>

<span data-ttu-id="7c6db-138">Lists the cities where most posts are coming from and their trend indicator.</span><span class="sxs-lookup"><span data-stu-id="7c6db-138">Lists the cities where most posts are coming from and their trend indicator.</span></span> <span data-ttu-id="7c6db-139">You can't drill down into more details from this list.</span><span class="sxs-lookup"><span data-stu-id="7c6db-139">You can't drill down into more details from this list.</span></span> 

## <a name="languages"></a><span data-ttu-id="7c6db-140">Languages</span><span class="sxs-lookup"><span data-stu-id="7c6db-140">Languages</span></span>

<span data-ttu-id="7c6db-141">Lists the five most-used languages based on the volume of posts and their trend indicator.</span><span class="sxs-lookup"><span data-stu-id="7c6db-141">Lists the five most-used languages based on the volume of posts and their trend indicator.</span></span>

## <a name="locations"></a><span data-ttu-id="7c6db-142">Locations</span><span class="sxs-lookup"><span data-stu-id="7c6db-142">Locations</span></span>

<span data-ttu-id="7c6db-143">Lists the countries/regions where most posts are coming from and their trend indicator.</span><span class="sxs-lookup"><span data-stu-id="7c6db-143">Lists the countries/regions where most posts are coming from and their trend indicator.</span></span>

## <a name="location-coverage"></a><span data-ttu-id="7c6db-144">Location coverage</span><span class="sxs-lookup"><span data-stu-id="7c6db-144">Location coverage</span></span>

<span data-ttu-id="7c6db-145">Shows the percentage of posts and authors based on their location, combined with posts without location information.</span><span class="sxs-lookup"><span data-stu-id="7c6db-145">Shows the percentage of posts and authors based on their location, combined with posts without location information.</span></span>

## <a name="location-groups"></a><span data-ttu-id="7c6db-146">Location groups</span><span class="sxs-lookup"><span data-stu-id="7c6db-146">Location groups</span></span>

<span data-ttu-id="7c6db-147">Lists the location groups where most posts are coming from and their trend indicator.</span><span class="sxs-lookup"><span data-stu-id="7c6db-147">Lists the location groups where most posts are coming from and their trend indicator.</span></span>  

<span data-ttu-id="7c6db-148">Dynamic widget.</span><span class="sxs-lookup"><span data-stu-id="7c6db-148">Dynamic widget.</span></span> <span data-ttu-id="7c6db-149">Shows only if posts from a country/region in the [configured location groups](manage-global-settings.md#create-and-manage-location-groups) are available.</span><span class="sxs-lookup"><span data-stu-id="7c6db-149">Shows only if posts from a country/region in the [configured location groups](manage-global-settings.md#create-and-manage-location-groups) are available.</span></span> 

## <a name="location-insights"></a><span data-ttu-id="7c6db-150">Location insights</span><span class="sxs-lookup"><span data-stu-id="7c6db-150">Location insights</span></span>

<span data-ttu-id="7c6db-151">Visualizes the posts with location information on a map to find out where the posts are coming from.</span><span class="sxs-lookup"><span data-stu-id="7c6db-151">Visualizes the posts with location information on a map to find out where the posts are coming from.</span></span> <span data-ttu-id="7c6db-152">You can also [define an activity map](activity-maps.md) to see new posts in real-time, with additional functionality.</span><span class="sxs-lookup"><span data-stu-id="7c6db-152">You can also [define an activity map](activity-maps.md) to see new posts in real-time, with additional functionality.</span></span> 

 - <span data-ttu-id="7c6db-153">![Single post symbol](media/single-post-marker.png "Single post symbol") Single post in a specific location.</span><span class="sxs-lookup"><span data-stu-id="7c6db-153">![Single post symbol](media/single-post-marker.png "Single post symbol") Single post in a specific location.</span></span>
 - <span data-ttu-id="7c6db-154">![Multiple posts symbol](media/post-cluster-marker.png "Multiple posts symbol") Multiple posts at the same location.</span><span class="sxs-lookup"><span data-stu-id="7c6db-154">![Multiple posts symbol](media/post-cluster-marker.png "Multiple posts symbol") Multiple posts at the same location.</span></span>
 - <span data-ttu-id="7c6db-155">![Cluster symbol](media/map-cluster-marker.png "Cluster symbol") Clusters of posts with location data in the same area.</span><span class="sxs-lookup"><span data-stu-id="7c6db-155">![Cluster symbol](media/map-cluster-marker.png "Cluster symbol") Clusters of posts with location data in the same area.</span></span>

## <a name="phrases-by-countryregion"></a><span data-ttu-id="7c6db-156">Phrases by country/region</span><span class="sxs-lookup"><span data-stu-id="7c6db-156">Phrases by country/region</span></span>

<span data-ttu-id="7c6db-157">Lists the most-mentioned phrases coming from the five countries/regions with the most posts in the current data set.</span><span class="sxs-lookup"><span data-stu-id="7c6db-157">Lists the most-mentioned phrases coming from the five countries/regions with the most posts in the current data set.</span></span>

## <a name="sentiment"></a><span data-ttu-id="7c6db-158">Sentiment</span><span class="sxs-lookup"><span data-stu-id="7c6db-158">Sentiment</span></span>

<span data-ttu-id="7c6db-159">Visualizes the sentiment index across all posts with a sentiment value in the selected data set.</span><span class="sxs-lookup"><span data-stu-id="7c6db-159">Visualizes the sentiment index across all posts with a sentiment value in the selected data set.</span></span> <span data-ttu-id="7c6db-160">It also shows the change in sentiment index compared to the last similar time frame and a trend indicator.</span><span class="sxs-lookup"><span data-stu-id="7c6db-160">It also shows the change in sentiment index compared to the last similar time frame and a trend indicator.</span></span>    
<span data-ttu-id="7c6db-161">You can [manually change the sentiment values](analytics-sentiment.md) if a post's sentiment is analyzed incorrectly.</span><span class="sxs-lookup"><span data-stu-id="7c6db-161">You can [manually change the sentiment values](analytics-sentiment.md) if a post's sentiment is analyzed incorrectly.</span></span> 

<span data-ttu-id="7c6db-162">Dynamic widget.</span><span class="sxs-lookup"><span data-stu-id="7c6db-162">Dynamic widget.</span></span> <span data-ttu-id="7c6db-163">Shows only if the data set contains posts with sentiment value.</span><span class="sxs-lookup"><span data-stu-id="7c6db-163">Shows only if the data set contains posts with sentiment value.</span></span>

### <a name="see-also"></a><span data-ttu-id="7c6db-164">See Also</span><span class="sxs-lookup"><span data-stu-id="7c6db-164">See Also</span></span>

<span data-ttu-id="7c6db-165">[Analyze social data using widgets](analyze-social-data-using-widgets.md) </span><span class="sxs-lookup"><span data-stu-id="7c6db-165">[Analyze social data using widgets](analyze-social-data-using-widgets.md) </span></span>  
<span data-ttu-id="7c6db-166">[Get to know your filters](use-filters.md)  </span><span class="sxs-lookup"><span data-stu-id="7c6db-166">[Get to know your filters](use-filters.md)  </span></span>  
[<span data-ttu-id="7c6db-167">Explore more options with your data set</span><span class="sxs-lookup"><span data-stu-id="7c6db-167">Explore more options with your data set</span></span>](more-options-with-data-set.md)    
