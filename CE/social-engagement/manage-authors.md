---
title: Manage authors in Social Engagement | Microsoft Docs
description: Learn how to delete posts and export information about authors.
keywords: author management, delete author, block author, export author information
ms.date: 06/13/2018
ms.service: dynamics-365-marketing
ms.topic: article
applies_to:
- Social Engagement
ms.assetid: 9404a5d0-f5c8-48b4-b1c7-1ea56125fcdc
author: m-hartmann
ms.author: mhart
manager: sakudes
ms.custom:
- dyn365-socialengagement
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365SE
ms.openlocfilehash: d60afbc790d1b4e92d5ea9aadbdf260b968bd8f6
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "375644"
---
# <a name="manage-an-authors-data"></a><span data-ttu-id="834b8-104">Manage an author's data</span><span class="sxs-lookup"><span data-stu-id="834b8-104">Manage an author's data</span></span>

<span data-ttu-id="834b8-105">Most posts in [!INCLUDE[pn-social-engagement-short](../includes/pn-social-engagement-short.md)] are linked to an author on a social network.</span><span class="sxs-lookup"><span data-stu-id="834b8-105">Most posts in [!INCLUDE[pn-social-engagement-short](../includes/pn-social-engagement-short.md)] are linked to an author on a social network.</span></span> <span data-ttu-id="834b8-106">With sufficient permissions, you can remove an author from [!INCLUDE[pn-social-engagement-short](../includes/pn-social-engagement-short.md)] and block all future posts by that author.</span><span class="sxs-lookup"><span data-stu-id="834b8-106">With sufficient permissions, you can remove an author from [!INCLUDE[pn-social-engagement-short](../includes/pn-social-engagement-short.md)] and block all future posts by that author.</span></span> <span data-ttu-id="834b8-107">Whenever [!INCLUDE[pn-social-engagement-short](../includes/pn-social-engagement-short.md)] acquires new posts, it checks if the author was deleted earlier and discards posts from deleted authors.</span><span class="sxs-lookup"><span data-stu-id="834b8-107">Whenever [!INCLUDE[pn-social-engagement-short](../includes/pn-social-engagement-short.md)] acquires new posts, it checks if the author was deleted earlier and discards posts from deleted authors.</span></span> <span data-ttu-id="834b8-108">It's critical to understand the implications of removing an author, because it can't be undone and can have a significant impact on data acquisition for your solution.</span><span class="sxs-lookup"><span data-stu-id="834b8-108">It's critical to understand the implications of removing an author, because it can't be undone and can have a significant impact on data acquisition for your solution.</span></span>

## <a name="delete-an-author"></a><span data-ttu-id="834b8-109">Delete an author</span><span class="sxs-lookup"><span data-stu-id="834b8-109">Delete an author</span></span>

<span data-ttu-id="834b8-110">To remove all available information about an author (for example, if you need to respond to a deletion request, or want to remove posts from a spam account) in [!INCLUDE[pn-social-engagement-short](../includes/pn-social-engagement-short.md)], you can delete them.</span><span class="sxs-lookup"><span data-stu-id="834b8-110">To remove all available information about an author (for example, if you need to respond to a deletion request, or want to remove posts from a spam account) in [!INCLUDE[pn-social-engagement-short](../includes/pn-social-engagement-short.md)], you can delete them.</span></span> <span data-ttu-id="834b8-111">However, once you delete an author, there's no way to undo it.</span><span class="sxs-lookup"><span data-stu-id="834b8-111">However, once you delete an author, there's no way to undo it.</span></span> <span data-ttu-id="834b8-112">Data about and from this author will be lost, including their ability to post in the future.</span><span class="sxs-lookup"><span data-stu-id="834b8-112">Data about and from this author will be lost, including their ability to post in the future.</span></span> <span data-ttu-id="834b8-113">To delete an author in [!INCLUDE[pn-social-engagement-short](../includes/pn-social-engagement-short.md)], you need to have a Power Analyst or Administrator [configuration role](user-roles.md).</span><span class="sxs-lookup"><span data-stu-id="834b8-113">To delete an author in [!INCLUDE[pn-social-engagement-short](../includes/pn-social-engagement-short.md)], you need to have a Power Analyst or Administrator [configuration role](user-roles.md).</span></span> 

<span data-ttu-id="834b8-114">Deleting an author will result in:</span><span class="sxs-lookup"><span data-stu-id="834b8-114">Deleting an author will result in:</span></span>

- <span data-ttu-id="834b8-115">All posts from the author will be removed.</span><span class="sxs-lookup"><span data-stu-id="834b8-115">All posts from the author will be removed.</span></span>

- <span data-ttu-id="834b8-116">No new posts from the author will be acquired in the future.</span><span class="sxs-lookup"><span data-stu-id="834b8-116">No new posts from the author will be acquired in the future.</span></span>

- <span data-ttu-id="834b8-117">Search rules that were configured to gather posts from the author's profile will be deleted.</span><span class="sxs-lookup"><span data-stu-id="834b8-117">Search rules that were configured to gather posts from the author's profile will be deleted.</span></span>

### <a name="find-and-delete-an-author"></a><span data-ttu-id="834b8-118">Find and delete an author</span><span class="sxs-lookup"><span data-stu-id="834b8-118">Find and delete an author</span></span>

1. <span data-ttu-id="834b8-119">In **[!INCLUDE[pn-social-engagement-short](../includes/pn-social-engagement-short.md)]** go to **Analytics** > **Overview**</span><span class="sxs-lookup"><span data-stu-id="834b8-119">In **[!INCLUDE[pn-social-engagement-short](../includes/pn-social-engagement-short.md)]** go to **Analytics** > **Overview**</span></span>

2. <span data-ttu-id="834b8-120">[Define a custom time frame](use-filters.md#edit-the-analysis-time-frame) to include the past 15 months.</span><span class="sxs-lookup"><span data-stu-id="834b8-120">[Define a custom time frame](use-filters.md#edit-the-analysis-time-frame) to include the past 15 months.</span></span>    
   <span data-ttu-id="834b8-121">Since posts are stored for 15 months, this ensures that you review all available data in [!INCLUDE[pn-social-engagement-short](../includes/pn-social-engagement-short.md)] and find the author if they published a post during that time.</span><span class="sxs-lookup"><span data-stu-id="834b8-121">Since posts are stored for 15 months, this ensures that you review all available data in [!INCLUDE[pn-social-engagement-short](../includes/pn-social-engagement-short.md)] and find the author if they published a post during that time.</span></span> 

3. <span data-ttu-id="834b8-122">Select the **Author** filter [using the filter menu](use-filters.md#add-edit-or-remove-a-filter).</span><span class="sxs-lookup"><span data-stu-id="834b8-122">Select the **Author** filter [using the filter menu](use-filters.md#add-edit-or-remove-a-filter).</span></span> 

4. <span data-ttu-id="834b8-123">Search for the author name and apply the filter to see all posts by this author.</span><span class="sxs-lookup"><span data-stu-id="834b8-123">Search for the author name and apply the filter to see all posts by this author.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="834b8-124">If you are asked to remove information about a specific author, we recommend that you confirm the identity of that author first to validate the request.</span><span class="sxs-lookup"><span data-stu-id="834b8-124">If you are asked to remove information about a specific author, we recommend that you confirm the identity of that author first to validate the request.</span></span> <span data-ttu-id="834b8-125">To confirm their identity, you can request a private message from the author.</span><span class="sxs-lookup"><span data-stu-id="834b8-125">To confirm their identity, you can request a private message from the author.</span></span> <span data-ttu-id="834b8-126">If they have access to the social media profile, they are likely to own it.</span><span class="sxs-lookup"><span data-stu-id="834b8-126">If they have access to the social media profile, they are likely to own it.</span></span>

5. <span data-ttu-id="834b8-127">Go to **Analytics > Overview**.</span><span class="sxs-lookup"><span data-stu-id="834b8-127">Go to **Analytics > Overview**.</span></span> <span data-ttu-id="834b8-128">In the **Authors** widget, select **Widget actions** ![Widget actions symbol](media/more-options-icon.png "Widget actions symbol") and select **Expand to full view** ![Expand to full view symbol](media/open-full-view-icon.png "Expand to full view symbol").</span><span class="sxs-lookup"><span data-stu-id="834b8-128">In the **Authors** widget, select **Widget actions** ![Widget actions symbol](media/more-options-icon.png "Widget actions symbol") and select **Expand to full view** ![Expand to full view symbol](media/open-full-view-icon.png "Expand to full view symbol").</span></span>

6. <span data-ttu-id="834b8-129">In the expanded view, select the **Remove Author** ![Remove author symbol](media/trashbin-icon.png "Remove author symbol") symbol and confirm your deletion.</span><span class="sxs-lookup"><span data-stu-id="834b8-129">In the expanded view, select the **Remove Author** ![Remove author symbol](media/trashbin-icon.png "Remove author symbol") symbol and confirm your deletion.</span></span>    
   <span data-ttu-id="834b8-130">![Remove author control in full view of Authors widget](media/remove-author-full-view.png "Remove author control in full view of Authors widget")</span><span class="sxs-lookup"><span data-stu-id="834b8-130">![Remove author control in full view of Authors widget](media/remove-author-full-view.png "Remove author control in full view of Authors widget")</span></span>

## <a name="export-author-information"></a><span data-ttu-id="834b8-131">Export author information</span><span class="sxs-lookup"><span data-stu-id="834b8-131">Export author information</span></span>

<span data-ttu-id="834b8-132">To inform an author about personal social profile data that is stored in [!INCLUDE[pn-social-engagement-short](../includes/pn-social-engagement-short.md)], administrators can export profile data to an [!INCLUDE[pn-excel-short](../includes/pn-excel-short.md)] file.</span><span class="sxs-lookup"><span data-stu-id="834b8-132">To inform an author about personal social profile data that is stored in [!INCLUDE[pn-social-engagement-short](../includes/pn-social-engagement-short.md)], administrators can export profile data to an [!INCLUDE[pn-excel-short](../includes/pn-excel-short.md)] file.</span></span> 

### <a name="export-details-about-an-author"></a><span data-ttu-id="834b8-133">Export details about an author</span><span class="sxs-lookup"><span data-stu-id="834b8-133">Export details about an author</span></span>

1. <span data-ttu-id="834b8-134">In **[!INCLUDE[pn-social-engagement-short](../includes/pn-social-engagement-short.md)]** go to **Analytics** > **Overview**.</span><span class="sxs-lookup"><span data-stu-id="834b8-134">In **[!INCLUDE[pn-social-engagement-short](../includes/pn-social-engagement-short.md)]** go to **Analytics** > **Overview**.</span></span>

2. <span data-ttu-id="834b8-135">[Define a custom time frame](use-filters.md#edit-the-analysis-time-frame) to include the past 15 months.</span><span class="sxs-lookup"><span data-stu-id="834b8-135">[Define a custom time frame](use-filters.md#edit-the-analysis-time-frame) to include the past 15 months.</span></span>   
   <span data-ttu-id="834b8-136">Since posts are stored for 15 months, this ensures that you review all available data in [!INCLUDE[pn-social-engagement-short](../includes/pn-social-engagement-short.md)] and find the author if they published a post during that time.</span><span class="sxs-lookup"><span data-stu-id="834b8-136">Since posts are stored for 15 months, this ensures that you review all available data in [!INCLUDE[pn-social-engagement-short](../includes/pn-social-engagement-short.md)] and find the author if they published a post during that time.</span></span> 

3. <span data-ttu-id="834b8-137">Select the **Author** filter [using the filter menu](use-filters.md#add-edit-or-remove-a-filter).</span><span class="sxs-lookup"><span data-stu-id="834b8-137">Select the **Author** filter [using the filter menu](use-filters.md#add-edit-or-remove-a-filter).</span></span> 

4. <span data-ttu-id="834b8-138">Search for the author name and apply the filter to see all posts by this author.</span><span class="sxs-lookup"><span data-stu-id="834b8-138">Search for the author name and apply the filter to see all posts by this author.</span></span> 

5. <span data-ttu-id="834b8-139">Go to **Analytics** > **Overview**.</span><span class="sxs-lookup"><span data-stu-id="834b8-139">Go to **Analytics** > **Overview**.</span></span> <span data-ttu-id="834b8-140">In the **Authors** widget, select the **View author details** ![View author details symbol](media/author-details-icon.png "View author details symbol") symbol.</span><span class="sxs-lookup"><span data-stu-id="834b8-140">In the **Authors** widget, select the **View author details** ![View author details symbol](media/author-details-icon.png "View author details symbol") symbol.</span></span>

6. <span data-ttu-id="834b8-141">In the author details view, select the **Export personal data for this author** ![Export symbol](media/export-data-icon.png "Export symbol") symbol and download the [!INCLUDE[pn-excel-short](../includes/pn-excel-short.md)] file.</span><span class="sxs-lookup"><span data-stu-id="834b8-141">In the author details view, select the **Export personal data for this author** ![Export symbol](media/export-data-icon.png "Export symbol") symbol and download the [!INCLUDE[pn-excel-short](../includes/pn-excel-short.md)] file.</span></span>    
   <span data-ttu-id="834b8-142">![Control to export personal data for this author](media/export-author-details.png "Control to export personal data for this author")</span><span class="sxs-lookup"><span data-stu-id="834b8-142">![Control to export personal data for this author](media/export-author-details.png "Control to export personal data for this author")</span></span>  

## <a name="stop-processing-specific-authors"></a><span data-ttu-id="834b8-143">Stop processing specific authors</span><span class="sxs-lookup"><span data-stu-id="834b8-143">Stop processing specific authors</span></span>

<span data-ttu-id="834b8-144">To stop processing author data, you need to [delete the author](#delete-an-author).</span><span class="sxs-lookup"><span data-stu-id="834b8-144">To stop processing author data, you need to [delete the author](#delete-an-author).</span></span> <span data-ttu-id="834b8-145">This will remove all search rules that are based on the author's profile and no new posts from this author will be acquired in the future.</span><span class="sxs-lookup"><span data-stu-id="834b8-145">This will remove all search rules that are based on the author's profile and no new posts from this author will be acquired in the future.</span></span> 

## <a name="correcting-author-information"></a><span data-ttu-id="834b8-146">Correcting author information</span><span class="sxs-lookup"><span data-stu-id="834b8-146">Correcting author information</span></span>

<span data-ttu-id="834b8-147">Administrators in [!INCLUDE[pn-social-engagement-short](../includes/pn-social-engagement-short.md)] can't change author names.</span><span class="sxs-lookup"><span data-stu-id="834b8-147">Administrators in [!INCLUDE[pn-social-engagement-short](../includes/pn-social-engagement-short.md)] can't change author names.</span></span>    
<span data-ttu-id="834b8-148">However, if an author decides to change their name on a social network, this change will be reflected in [!INCLUDE[pn-social-engagement-short](../includes/pn-social-engagement-short.md)] when their next post is acquired.</span><span class="sxs-lookup"><span data-stu-id="834b8-148">However, if an author decides to change their name on a social network, this change will be reflected in [!INCLUDE[pn-social-engagement-short](../includes/pn-social-engagement-short.md)] when their next post is acquired.</span></span> 

<span data-ttu-id="834b8-149">If an author decides to remove a public post on Twitter, Tumblr, or WordPress, this deletion is reflected in [!INCLUDE[pn-social-engagement-short](../includes/pn-social-engagement-short.md)] and the post is removed from the user interface, too.</span><span class="sxs-lookup"><span data-stu-id="834b8-149">If an author decides to remove a public post on Twitter, Tumblr, or WordPress, this deletion is reflected in [!INCLUDE[pn-social-engagement-short](../includes/pn-social-engagement-short.md)] and the post is removed from the user interface, too.</span></span>

### <a name="see-also"></a><span data-ttu-id="834b8-150">See also</span><span class="sxs-lookup"><span data-stu-id="834b8-150">See also</span></span>
<span data-ttu-id="834b8-151">[Get an overview about the data](analytics-overview.md)  </span><span class="sxs-lookup"><span data-stu-id="834b8-151">[Get an overview about the data](analytics-overview.md)  </span></span>  
<span data-ttu-id="834b8-152">[Get started with Social Engagement](get-started.md)  </span><span class="sxs-lookup"><span data-stu-id="834b8-152">[Get started with Social Engagement](get-started.md)  </span></span>  
[<span data-ttu-id="834b8-153">Set up searches in Social Engagement</span><span class="sxs-lookup"><span data-stu-id="834b8-153">Set up searches in Social Engagement</span></span>](set-up-searches.md)
