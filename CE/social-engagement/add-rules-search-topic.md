---
title: Add rules to a Social Engagement search topic | Microsoft Docs
description: Learn how to add more rules to a search topic to gather additional data.
keywords: search topic, search rule, Social Engagement
ms.date: 08/22/2018
ms.service: dynamics-365-marketing
ms.topic: article
applies_to:
- Social Engagement
ms.assetid: 9d65050a-4d34-4d87-8361-1954114da289
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
ms.openlocfilehash: 11a964cf29b79baa0565b91cb46ec0ec37aea0c8
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "375530"
---
# <a name="add-rules-to-a-search-topic"></a><span data-ttu-id="7d293-104">Add rules to a search topic</span><span class="sxs-lookup"><span data-stu-id="7d293-104">Add rules to a search topic</span></span>
<span data-ttu-id="7d293-105">Search topics define the data that's available for your analysis.</span><span class="sxs-lookup"><span data-stu-id="7d293-105">Search topics define the data that's available for your analysis.</span></span> <span data-ttu-id="7d293-106">You can add an unlimited number of search rules to a search topic.</span><span class="sxs-lookup"><span data-stu-id="7d293-106">You can add an unlimited number of search rules to a search topic.</span></span> <span data-ttu-id="7d293-107">Each rule selects posts that will be available for the analysis of the data set.</span><span class="sxs-lookup"><span data-stu-id="7d293-107">Each rule selects posts that will be available for the analysis of the data set.</span></span> <span data-ttu-id="7d293-108">You can update your search topics at any time, and add more rules or change existing ones.</span><span class="sxs-lookup"><span data-stu-id="7d293-108">You can update your search topics at any time, and add more rules or change existing ones.</span></span>

[!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] <span data-ttu-id="7d293-109">supports the following search rules.</span><span class="sxs-lookup"><span data-stu-id="7d293-109">supports the following search rules.</span></span> <span data-ttu-id="7d293-110">You need to be a [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] Administrator or Power Analyst to create or modify search topics.</span><span class="sxs-lookup"><span data-stu-id="7d293-110">You need to be a [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] Administrator or Power Analyst to create or modify search topics.</span></span>

- <span data-ttu-id="7d293-111">**[Keywords rule](#add-a-keywords-rule)** ![Keywords symbol](media/keywords-search-rule-icon.png "Keywords symbol"): Gather posts based on a query that consists of keywords, inclusions, and exclusions.</span><span class="sxs-lookup"><span data-stu-id="7d293-111">**[Keywords rule](#add-a-keywords-rule)** ![Keywords symbol](media/keywords-search-rule-icon.png "Keywords symbol"): Gather posts based on a query that consists of keywords, inclusions, and exclusions.</span></span>

- <span data-ttu-id="7d293-112">**[Facebook pages rule](#add-a-facebook-pages-rule)** ![Facebook symbol](media/facebook-source-icon.png "Facebook symbol"): Gather all public posts and comments from a specific [!INCLUDE[tn_facebook](../includes/tn-facebook.md)] page.</span><span class="sxs-lookup"><span data-stu-id="7d293-112">**[Facebook pages rule](#add-a-facebook-pages-rule)** ![Facebook symbol](media/facebook-source-icon.png "Facebook symbol"): Gather all public posts and comments from a specific [!INCLUDE[tn_facebook](../includes/tn-facebook.md)] page.</span></span>

- <span data-ttu-id="7d293-113">**[Twitter rule](#add-a-twitter-rule)** ![Twitter symbol](media/twitter-icon.png "Twitter symbol"): Capture mentions, replies, tweets, or retweets from a [!INCLUDE[tn_twitter](../includes/tn-twitter.md)] account.</span><span class="sxs-lookup"><span data-stu-id="7d293-113">**[Twitter rule](#add-a-twitter-rule)** ![Twitter symbol](media/twitter-icon.png "Twitter symbol"): Capture mentions, replies, tweets, or retweets from a [!INCLUDE[tn_twitter](../includes/tn-twitter.md)] account.</span></span>

- <span data-ttu-id="7d293-114">**[Private messages rule](#add-a-private-messages-rule)** ![Private messages symbol](media/private-message-icon.png "Private messages symbol"): Get private messages that were sent to a [!INCLUDE[tn_twitter](../includes/tn-twitter.md)] profile or [!INCLUDE[tn_facebook](../includes/tn-facebook.md)] page that has been authenticated in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] and [allows private message acquisition](manage-access-tokens.md#tokens-for-data-acquisition).</span><span class="sxs-lookup"><span data-stu-id="7d293-114">**[Private messages rule](#add-a-private-messages-rule)** ![Private messages symbol](media/private-message-icon.png "Private messages symbol"): Get private messages that were sent to a [!INCLUDE[tn_twitter](../includes/tn-twitter.md)] profile or [!INCLUDE[tn_facebook](../includes/tn-facebook.md)] page that has been authenticated in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] and [allows private message acquisition](manage-access-tokens.md#tokens-for-data-acquisition).</span></span>

- <span data-ttu-id="7d293-115">**[Custom sources rule](#add-a-custom-sources-rule)** ![Custom sources symbol](media/custom-sources-icon.png "Custom sources symbol"): Gather posts from public RSS feeds in your custom source groups.</span><span class="sxs-lookup"><span data-stu-id="7d293-115">**[Custom sources rule](#add-a-custom-sources-rule)** ![Custom sources symbol](media/custom-sources-icon.png "Custom sources symbol"): Gather posts from public RSS feeds in your custom source groups.</span></span>

- <span data-ttu-id="7d293-116">**[YouTube rule](#add-a-includetnyoutubeincludestn-youtubemd-rule)** ![YouTube symbol](media/video-icon.png "YouTube symbol"): Gather video posts and comments from [!INCLUDE[tn_youtube](../includes/tn-youtube.md)] channels.</span><span class="sxs-lookup"><span data-stu-id="7d293-116">**[YouTube rule](#add-a-includetnyoutubeincludestn-youtubemd-rule)** ![YouTube symbol](media/video-icon.png "YouTube symbol"): Gather video posts and comments from [!INCLUDE[tn_youtube](../includes/tn-youtube.md)] channels.</span></span>

- <span data-ttu-id="7d293-117">**[LinkedIn page rule](#linkedin-page-rule)**: Gather posts from [!INCLUDE[pn-linkedin](../includes/pn-linkedin.md)] Organization Pages.</span><span class="sxs-lookup"><span data-stu-id="7d293-117">**[LinkedIn page rule](#linkedin-page-rule)**: Gather posts from [!INCLUDE[pn-linkedin](../includes/pn-linkedin.md)] Organization Pages.</span></span>
  
> [!TIP]
>  <span data-ttu-id="7d293-118">This topic is part of a walkthrough about how to set up searches.</span><span class="sxs-lookup"><span data-stu-id="7d293-118">This topic is part of a walkthrough about how to set up searches.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="7d293-119">[Set up searches to listen to social media conversations](set-up-searches.md)</span><span class="sxs-lookup"><span data-stu-id="7d293-119">[Set up searches to listen to social media conversations](set-up-searches.md)</span></span>  
  
## <a name="add-a-rule-to-a-search-topic"></a><span data-ttu-id="7d293-120">Add a rule to a search topic</span><span class="sxs-lookup"><span data-stu-id="7d293-120">Add a rule to a search topic</span></span>  
<span data-ttu-id="7d293-121">To enable searches and collect posts, add one or more rules to a search topic.</span><span class="sxs-lookup"><span data-stu-id="7d293-121">To enable searches and collect posts, add one or more rules to a search topic.</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="7d293-122">Your keywords, inclusions, and exclusions can each extend up to 128 characters.</span><span class="sxs-lookup"><span data-stu-id="7d293-122">Your keywords, inclusions, and exclusions can each extend up to 128 characters.</span></span> <span data-ttu-id="7d293-123">You can add up to 15 keywords and inclusions per search rule and up to 25 exclusions per search rule.</span><span class="sxs-lookup"><span data-stu-id="7d293-123">You can add up to 15 keywords and inclusions per search rule and up to 25 exclusions per search rule.</span></span>  
> 
>  <span data-ttu-id="7d293-124">Adding a rule usually leads to more posts resulting from your searches.</span><span class="sxs-lookup"><span data-stu-id="7d293-124">Adding a rule usually leads to more posts resulting from your searches.</span></span> <span data-ttu-id="7d293-125">The increased number of posts will count against your post quota.</span><span class="sxs-lookup"><span data-stu-id="7d293-125">The increased number of posts will count against your post quota.</span></span> <span data-ttu-id="7d293-126">You'll need to validate every search topic that you changed before you can save it.</span><span class="sxs-lookup"><span data-stu-id="7d293-126">You'll need to validate every search topic that you changed before you can save it.</span></span> <span data-ttu-id="7d293-127">It's a good idea to frequently review the results of a new or updated search topic to confirm that it collects relevant data and complies with your quota limits.</span><span class="sxs-lookup"><span data-stu-id="7d293-127">It's a good idea to frequently review the results of a new or updated search topic to confirm that it collects relevant data and complies with your quota limits.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="7d293-128">[Manage your post quota](manage-post-quota.md)</span><span class="sxs-lookup"><span data-stu-id="7d293-128">[Manage your post quota](manage-post-quota.md)</span></span>  
  
### <a name="add-a-new-rule"></a><span data-ttu-id="7d293-129">Add a new rule</span><span class="sxs-lookup"><span data-stu-id="7d293-129">Add a new rule</span></span>  
  
1.  <span data-ttu-id="7d293-130">Go to **Search Setup**.</span><span class="sxs-lookup"><span data-stu-id="7d293-130">Go to **Search Setup**.</span></span>  
  
2.  <span data-ttu-id="7d293-131">In the list of search topics, select the search topic to add a rule to.</span><span class="sxs-lookup"><span data-stu-id="7d293-131">In the list of search topics, select the search topic to add a rule to.</span></span>  
  
3.  <span data-ttu-id="7d293-132">Click **Add rule** (![Add button](media/add-icon.png "Add button")) to open the **Add Rule** pane.</span><span class="sxs-lookup"><span data-stu-id="7d293-132">Click **Add rule** (![Add button](media/add-icon.png "Add button")) to open the **Add Rule** pane.</span></span>  
  
4.  <span data-ttu-id="7d293-133">Select the rule type that you want to add.</span><span class="sxs-lookup"><span data-stu-id="7d293-133">Select the rule type that you want to add.</span></span>  
  
5.  <span data-ttu-id="7d293-134">Define the values as required for the new rule.</span><span class="sxs-lookup"><span data-stu-id="7d293-134">Define the values as required for the new rule.</span></span>  
  
6.  <span data-ttu-id="7d293-135">Click **Continue** in the **Add Rule** pane to add the rule to the search topic.</span><span class="sxs-lookup"><span data-stu-id="7d293-135">Click **Continue** in the **Add Rule** pane to add the rule to the search topic.</span></span>  
  
    > [!IMPORTANT]
    >  <span data-ttu-id="7d293-136">The solution checks the quota availability for the new rule and prompts you accordingly.</span><span class="sxs-lookup"><span data-stu-id="7d293-136">The solution checks the quota availability for the new rule and prompts you accordingly.</span></span> <span data-ttu-id="7d293-137">If your quota can't accommodate the new rule, you can't save it.</span><span class="sxs-lookup"><span data-stu-id="7d293-137">If your quota can't accommodate the new rule, you can't save it.</span></span>  
  
7.  <span data-ttu-id="7d293-138">In the search topic pane, click **Save** (![Save button](media/save-icon.png "Save button")) to activate your search topic, or click **Add** to add another rule to your topic.</span><span class="sxs-lookup"><span data-stu-id="7d293-138">In the search topic pane, click **Save** (![Save button](media/save-icon.png "Save button")) to activate your search topic, or click **Add** to add another rule to your topic.</span></span>  


<a name="addKeywordsRule"></a>   
## <a name="add-a-keywords-rule"></a><span data-ttu-id="7d293-139">Add a keywords rule</span><span class="sxs-lookup"><span data-stu-id="7d293-139">Add a keywords rule</span></span>  
 <span data-ttu-id="7d293-140">Create rules from keywords, inclusions, and exclusions and define the sources and languages that you want the rule to search on.</span><span class="sxs-lookup"><span data-stu-id="7d293-140">Create rules from keywords, inclusions, and exclusions and define the sources and languages that you want the rule to search on.</span></span> <span data-ttu-id="7d293-141">This is the most common way to define a rule in a search topic, and it usually results in a large number of posts.</span><span class="sxs-lookup"><span data-stu-id="7d293-141">This is the most common way to define a rule in a search topic, and it usually results in a large number of posts.</span></span>  
  
### <a name="add-a-new-keywords-rule"></a><span data-ttu-id="7d293-142">Add a new keywords rule</span><span class="sxs-lookup"><span data-stu-id="7d293-142">Add a new keywords rule</span></span>  
  
1. <span data-ttu-id="7d293-143">Go to **Search Setup**.</span><span class="sxs-lookup"><span data-stu-id="7d293-143">Go to **Search Setup**.</span></span>  
  
2. <span data-ttu-id="7d293-144">Select the search topic that you want to add the rule to, or create a new search topic.</span><span class="sxs-lookup"><span data-stu-id="7d293-144">Select the search topic that you want to add the rule to, or create a new search topic.</span></span>  
  
3. <span data-ttu-id="7d293-145">Under **Rules**, click **Add new rule** (![Add button](media/add-icon.png "Add button")) to open the **Add Rule** page.</span><span class="sxs-lookup"><span data-stu-id="7d293-145">Under **Rules**, click **Add new rule** (![Add button](media/add-icon.png "Add button")) to open the **Add Rule** page.</span></span>  
  
4. <span data-ttu-id="7d293-146">Click **Keywords rule**.</span><span class="sxs-lookup"><span data-stu-id="7d293-146">Click **Keywords rule**.</span></span>  
  
5. <span data-ttu-id="7d293-147">Enter the keywords; select the inclusions, exclusions, and the filters that you want to use when searching for posts.</span><span class="sxs-lookup"><span data-stu-id="7d293-147">Enter the keywords; select the inclusions, exclusions, and the filters that you want to use when searching for posts.</span></span>  
  
6. <span data-ttu-id="7d293-148">Select **Continue** in the **Add Rule** pane to add the rule to the search topic.</span><span class="sxs-lookup"><span data-stu-id="7d293-148">Select **Continue** in the **Add Rule** pane to add the rule to the search topic.</span></span>  
  
   > [!IMPORTANT]
   >  <span data-ttu-id="7d293-149">The solution checks the quota availability for the new rule and prompts you accordingly.</span><span class="sxs-lookup"><span data-stu-id="7d293-149">The solution checks the quota availability for the new rule and prompts you accordingly.</span></span> <span data-ttu-id="7d293-150">If your quota can't accommodate the new rule, you can't save it.</span><span class="sxs-lookup"><span data-stu-id="7d293-150">If your quota can't accommodate the new rule, you can't save it.</span></span> <span data-ttu-id="7d293-151">Additionally, you'll find a preview of posts on [!INCLUDE[tn-twitter](../includes/tn-twitter.md)] matching your rule.</span><span class="sxs-lookup"><span data-stu-id="7d293-151">Additionally, you'll find a preview of posts on [!INCLUDE[tn-twitter](../includes/tn-twitter.md)] matching your rule.</span></span>   
  
7. <span data-ttu-id="7d293-152">In the search topic pane, click **Save** (![Save button](media/save-icon.png "Save button")) to activate your rule.</span><span class="sxs-lookup"><span data-stu-id="7d293-152">In the search topic pane, click **Save** (![Save button](media/save-icon.png "Save button")) to activate your rule.</span></span>  
  
### <a name="add-keywords-to-search-for"></a><span data-ttu-id="7d293-153">Add keywords to search for</span><span class="sxs-lookup"><span data-stu-id="7d293-153">Add keywords to search for</span></span>  
<span data-ttu-id="7d293-154">Keywords define the terms and phrases to listen for.</span><span class="sxs-lookup"><span data-stu-id="7d293-154">Keywords define the terms and phrases to listen for.</span></span> <span data-ttu-id="7d293-155">Keywords are exact, but not case-sensitive.</span><span class="sxs-lookup"><span data-stu-id="7d293-155">Keywords are exact, but not case-sensitive.</span></span> <span data-ttu-id="7d293-156">We recommend that you include variations of keywords.</span><span class="sxs-lookup"><span data-stu-id="7d293-156">We recommend that you include variations of keywords.</span></span> <span data-ttu-id="7d293-157">For example, if your keyword is **phone** and the term that appears in a post is **phones**, your result won't be selected by the search rule and the result won't show up in your analysis.</span><span class="sxs-lookup"><span data-stu-id="7d293-157">For example, if your keyword is **phone** and the term that appears in a post is **phones**, your result won't be selected by the search rule and the result won't show up in your analysis.</span></span> <span data-ttu-id="7d293-158">For each keyword, the comma serves as an OR.</span><span class="sxs-lookup"><span data-stu-id="7d293-158">For each keyword, the comma serves as an OR.</span></span> <span data-ttu-id="7d293-159">If you add more than one search term, your search rule looks for at least one of the listed terms.</span><span class="sxs-lookup"><span data-stu-id="7d293-159">If you add more than one search term, your search rule looks for at least one of the listed terms.</span></span> <span data-ttu-id="7d293-160">To increase the likelihood of getting the results you want, think about adding acronyms and common contractions.</span><span class="sxs-lookup"><span data-stu-id="7d293-160">To increase the likelihood of getting the results you want, think about adding acronyms and common contractions.</span></span>  
  
<span data-ttu-id="7d293-161">It's important to review keywords regularly.</span><span class="sxs-lookup"><span data-stu-id="7d293-161">It's important to review keywords regularly.</span></span> <span data-ttu-id="7d293-162">If your keywords yield too many results, consider narrowing the search rule by adding inclusions and exclusions, or reducing the number of keywords.</span><span class="sxs-lookup"><span data-stu-id="7d293-162">If your keywords yield too many results, consider narrowing the search rule by adding inclusions and exclusions, or reducing the number of keywords.</span></span>  
  
[!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="7d293-163">[Refine your search rules](refine-search-rules.md)</span><span class="sxs-lookup"><span data-stu-id="7d293-163">[Refine your search rules](refine-search-rules.md)</span></span>  
  
<span data-ttu-id="7d293-164">For example, let's assume that you want to listen to posts about a product that Contoso manufactures.</span><span class="sxs-lookup"><span data-stu-id="7d293-164">For example, let's assume that you want to listen to posts about a product that Contoso manufactures.</span></span> <span data-ttu-id="7d293-165">You could add the keywords to a search rule like this: **Product name, #prodname, Name of the product**.</span><span class="sxs-lookup"><span data-stu-id="7d293-165">You could add the keywords to a search rule like this: **Product name, #prodname, Name of the product**.</span></span> <span data-ttu-id="7d293-166">All posts that mention one of these keywords will result from the search rule.</span><span class="sxs-lookup"><span data-stu-id="7d293-166">All posts that mention one of these keywords will result from the search rule.</span></span>  
  
### <a name="add-inclusions-to-a-keywords-rule"></a><span data-ttu-id="7d293-167">Add inclusions to a keywords rule</span><span class="sxs-lookup"><span data-stu-id="7d293-167">Add inclusions to a keywords rule</span></span>  
<span data-ttu-id="7d293-168">Narrow your search by adding inclusions so that you get a much higher quality selection of posts.</span><span class="sxs-lookup"><span data-stu-id="7d293-168">Narrow your search by adding inclusions so that you get a much higher quality selection of posts.</span></span> <span data-ttu-id="7d293-169">Think of inclusions as the word AND.</span><span class="sxs-lookup"><span data-stu-id="7d293-169">Think of inclusions as the word AND.</span></span> <span data-ttu-id="7d293-170">Your search will be filtered so that posts are selected only if they contain at least one of the keywords *and* at least one of the inclusions.</span><span class="sxs-lookup"><span data-stu-id="7d293-170">Your search will be filtered so that posts are selected only if they contain at least one of the keywords *and* at least one of the inclusions.</span></span> <span data-ttu-id="7d293-171">Inclusions aren't case-sensitive.</span><span class="sxs-lookup"><span data-stu-id="7d293-171">Inclusions aren't case-sensitive.</span></span>  
  
<span data-ttu-id="7d293-172">When listening to posts about a product, you want to make sure that posts relate to a product in the manufacturer's portfolio.</span><span class="sxs-lookup"><span data-stu-id="7d293-172">When listening to posts about a product, you want to make sure that posts relate to a product in the manufacturer's portfolio.</span></span> <span data-ttu-id="7d293-173">Consider adding different spellings of the brand or company name.</span><span class="sxs-lookup"><span data-stu-id="7d293-173">Consider adding different spellings of the brand or company name.</span></span> <span data-ttu-id="7d293-174">For example, to find posts that mention Contoso's product you might add something like this to the inclusions: <strong>#contoso, Contoso, @contoso</strong>.</span><span class="sxs-lookup"><span data-stu-id="7d293-174">For example, to find posts that mention Contoso's product you might add something like this to the inclusions: <strong>#contoso, Contoso, @contoso</strong>.</span></span> <span data-ttu-id="7d293-175">All posts that mention one of the keywords and one of the inclusions will now be found by this search rule.</span><span class="sxs-lookup"><span data-stu-id="7d293-175">All posts that mention one of the keywords and one of the inclusions will now be found by this search rule.</span></span>  
  
<span data-ttu-id="7d293-176">When you set up your search rule, you can choose from the following options to decide how close a keyword and an inclusion must appear in a post:</span><span class="sxs-lookup"><span data-stu-id="7d293-176">When you set up your search rule, you can choose from the following options to decide how close a keyword and an inclusion must appear in a post:</span></span>  
  
- <span data-ttu-id="7d293-177">**Sentence**: Keywords and inclusions must appear in the same sentence.</span><span class="sxs-lookup"><span data-stu-id="7d293-177">**Sentence**: Keywords and inclusions must appear in the same sentence.</span></span>  
  
- <span data-ttu-id="7d293-178">**Paragraph**: Keywords and inclusions must appear in the same paragraph.</span><span class="sxs-lookup"><span data-stu-id="7d293-178">**Paragraph**: Keywords and inclusions must appear in the same paragraph.</span></span>  
  
- <span data-ttu-id="7d293-179">**Post**: Keywords and inclusions must appear in the same post.</span><span class="sxs-lookup"><span data-stu-id="7d293-179">**Post**: Keywords and inclusions must appear in the same post.</span></span>  
  
<span data-ttu-id="7d293-180">It's a good idea to start with the default option (**Paragraph**).</span><span class="sxs-lookup"><span data-stu-id="7d293-180">It's a good idea to start with the default option (**Paragraph**).</span></span> <span data-ttu-id="7d293-181">If your search topic yields too many irrelevant results, narrow it by selecting the **Sentence** option.</span><span class="sxs-lookup"><span data-stu-id="7d293-181">If your search topic yields too many irrelevant results, narrow it by selecting the **Sentence** option.</span></span> <span data-ttu-id="7d293-182">Note that this may also remove relevant posts because all combinations of inclusions and keywords outside of a sentence will no longer be picked up by the keywords rule.</span><span class="sxs-lookup"><span data-stu-id="7d293-182">Note that this may also remove relevant posts because all combinations of inclusions and keywords outside of a sentence will no longer be picked up by the keywords rule.</span></span>  

<span data-ttu-id="7d293-183">Inclusions are a great way to reduce the number of posts resulting from your search and make sure you stay within your quota.</span><span class="sxs-lookup"><span data-stu-id="7d293-183">Inclusions are a great way to reduce the number of posts resulting from your search and make sure you stay within your quota.</span></span>  
  
### <a name="exclude-terms-from-a-keywords-rule"></a><span data-ttu-id="7d293-184">Exclude terms from a keywords rule</span><span class="sxs-lookup"><span data-stu-id="7d293-184">Exclude terms from a keywords rule</span></span>  
<span data-ttu-id="7d293-185">Sometimes a specific word or phrase can overwhelm your results with irrelevant posts.</span><span class="sxs-lookup"><span data-stu-id="7d293-185">Sometimes a specific word or phrase can overwhelm your results with irrelevant posts.</span></span> <span data-ttu-id="7d293-186">With exclusions, you can narrow your searches and improve your results.</span><span class="sxs-lookup"><span data-stu-id="7d293-186">With exclusions, you can narrow your searches and improve your results.</span></span> <span data-ttu-id="7d293-187">Enter the terms you want to exclude and separate them by commas, and your searches will ignore posts that contain those terms.</span><span class="sxs-lookup"><span data-stu-id="7d293-187">Enter the terms you want to exclude and separate them by commas, and your searches will ignore posts that contain those terms.</span></span> <span data-ttu-id="7d293-188">Exclusions aren't case-sensitive.</span><span class="sxs-lookup"><span data-stu-id="7d293-188">Exclusions aren't case-sensitive.</span></span> <span data-ttu-id="7d293-189">For every term that you add to the exclusions, your search will be filtered so that no post will be selected if it matches one of the keywords but contains any of your exclusions.</span><span class="sxs-lookup"><span data-stu-id="7d293-189">For every term that you add to the exclusions, your search will be filtered so that no post will be selected if it matches one of the keywords but contains any of your exclusions.</span></span> <span data-ttu-id="7d293-190">Think of exclusions as the words AND NOT.</span><span class="sxs-lookup"><span data-stu-id="7d293-190">Think of exclusions as the words AND NOT.</span></span>  
  
<span data-ttu-id="7d293-191">For example, let's assume that you're not interested in discounts or offers around Contoso's product.</span><span class="sxs-lookup"><span data-stu-id="7d293-191">For example, let's assume that you're not interested in discounts or offers around Contoso's product.</span></span> <span data-ttu-id="7d293-192">To avoid results that contain either **discounts** or **offers**, add those terms to the search rule's exclusions.</span><span class="sxs-lookup"><span data-stu-id="7d293-192">To avoid results that contain either **discounts** or **offers**, add those terms to the search rule's exclusions.</span></span> <span data-ttu-id="7d293-193">All posts that mention at least one of the exclusions in the same post as a keyword will no longer be included in the results from this rule.</span><span class="sxs-lookup"><span data-stu-id="7d293-193">All posts that mention at least one of the exclusions in the same post as a keyword will no longer be included in the results from this rule.</span></span>  
  
<span data-ttu-id="7d293-194">To exclude multiple terms, the exclusions must be added to the same search rule.</span><span class="sxs-lookup"><span data-stu-id="7d293-194">To exclude multiple terms, the exclusions must be added to the same search rule.</span></span> <span data-ttu-id="7d293-195">If one rule searches for **Contoso** while excluding **discounts** and another rule searches for **Contoso** while excluding **offers**, the search topic will only exclude all posts mentioning **Contoso** that contain both **discounts** and **offers**.</span><span class="sxs-lookup"><span data-stu-id="7d293-195">If one rule searches for **Contoso** while excluding **discounts** and another rule searches for **Contoso** while excluding **offers**, the search topic will only exclude all posts mentioning **Contoso** that contain both **discounts** and **offers**.</span></span> <span data-ttu-id="7d293-196">If the rule searches for **Contoso** while excluding **discounts, offers**, the search topic will exclude all posts mentioning **Contoso** that contain either **discounts** or **offers**, which is what you want.</span><span class="sxs-lookup"><span data-stu-id="7d293-196">If the rule searches for **Contoso** while excluding **discounts, offers**, the search topic will exclude all posts mentioning **Contoso** that contain either **discounts** or **offers**, which is what you want.</span></span>  
  
> [!TIP]
>  <span data-ttu-id="7d293-197">You can exclude terms from all active search rules in one step by adding a term to the list of blocked content.</span><span class="sxs-lookup"><span data-stu-id="7d293-197">You can exclude terms from all active search rules in one step by adding a term to the list of blocked content.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="7d293-198">[Manage the quality of your search results](search-results-quality.md)</span><span class="sxs-lookup"><span data-stu-id="7d293-198">[Manage the quality of your search results](search-results-quality.md)</span></span>  
  
<span data-ttu-id="7d293-199">Exclusions are a great way to reduce the number of posts that result from your search and make sure you stay within your post quota.</span><span class="sxs-lookup"><span data-stu-id="7d293-199">Exclusions are a great way to reduce the number of posts that result from your search and make sure you stay within your post quota.</span></span> <span data-ttu-id="7d293-200">However, you should choose your exclusions carefully to avoid missing relevant posts.</span><span class="sxs-lookup"><span data-stu-id="7d293-200">However, you should choose your exclusions carefully to avoid missing relevant posts.</span></span>  
  
### <a name="handle-special-characters-in-keywords-inclusions-and-exclusions"></a><span data-ttu-id="7d293-201">Handle special characters in keywords, inclusions, and exclusions</span><span class="sxs-lookup"><span data-stu-id="7d293-201">Handle special characters in keywords, inclusions, and exclusions</span></span>  
<span data-ttu-id="7d293-202">Exact searches are critical to successful social listening.</span><span class="sxs-lookup"><span data-stu-id="7d293-202">Exact searches are critical to successful social listening.</span></span> <span data-ttu-id="7d293-203">Special characters are often used in brand or product names in the form of connectors.</span><span class="sxs-lookup"><span data-stu-id="7d293-203">Special characters are often used in brand or product names in the form of connectors.</span></span> [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] <span data-ttu-id="7d293-204">interprets the special characters +, &, /,  and - as separate entities in a search rule.</span><span class="sxs-lookup"><span data-stu-id="7d293-204">interprets the special characters +, &, /,  and - as separate entities in a search rule.</span></span>  
  
<span data-ttu-id="7d293-205">For example, searching for the term **City Power & Light** will result in posts that mention this term with all combinations of white space.</span><span class="sxs-lookup"><span data-stu-id="7d293-205">For example, searching for the term **City Power & Light** will result in posts that mention this term with all combinations of white space.</span></span> <span data-ttu-id="7d293-206">Posts that contain any of the following terms (not case-sensitive) will be picked up by the search:</span><span class="sxs-lookup"><span data-stu-id="7d293-206">Posts that contain any of the following terms (not case-sensitive) will be picked up by the search:</span></span>  
  
-   <span data-ttu-id="7d293-207">City Power & Light (white space before and after the special character)</span><span class="sxs-lookup"><span data-stu-id="7d293-207">City Power & Light (white space before and after the special character)</span></span>  
  
-   <span data-ttu-id="7d293-208">City Power& Light (white space after the special character)</span><span class="sxs-lookup"><span data-stu-id="7d293-208">City Power& Light (white space after the special character)</span></span>  
  
-   <span data-ttu-id="7d293-209">City Power &Light (white space before the special character)</span><span class="sxs-lookup"><span data-stu-id="7d293-209">City Power &Light (white space before the special character)</span></span>  
  
-   <span data-ttu-id="7d293-210">City Power&Light (no white space before or after the special character)</span><span class="sxs-lookup"><span data-stu-id="7d293-210">City Power&Light (no white space before or after the special character)</span></span>  
  
#### <a name="additional-special-characters"></a><span data-ttu-id="7d293-211">Additional special characters</span><span class="sxs-lookup"><span data-stu-id="7d293-211">Additional special characters</span></span>  
<span data-ttu-id="7d293-212">Authors on [!INCLUDE[tn_twitter](../includes/tn-twitter.md)] and [!INCLUDE[tn_instagram](../includes/tn-instagram.md)] regularly use #hashtags and \@mentions.</span><span class="sxs-lookup"><span data-stu-id="7d293-212">Authors on [!INCLUDE[tn_twitter](../includes/tn-twitter.md)] and [!INCLUDE[tn_instagram](../includes/tn-instagram.md)] regularly use #hashtags and \@mentions.</span></span> [!INCLUDE[tn_twitter](../includes/tn-twitter.md)] <span data-ttu-id="7d293-213">authors also will use $stocktweets.</span><span class="sxs-lookup"><span data-stu-id="7d293-213">authors also will use $stocktweets.</span></span> <span data-ttu-id="7d293-214">Use those special characters if you want to search explicitly for #hashtags, $stocktweets, or \@mentions.</span><span class="sxs-lookup"><span data-stu-id="7d293-214">Use those special characters if you want to search explicitly for #hashtags, $stocktweets, or \@mentions.</span></span> [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] <span data-ttu-id="7d293-215">interprets those terms as unique entities when they're added to a search rule.</span><span class="sxs-lookup"><span data-stu-id="7d293-215">interprets those terms as unique entities when they're added to a search rule.</span></span>  
  
<span data-ttu-id="7d293-216">For example, searching for the term **#contoso** will only find results that contain the exact match of the hashtag.</span><span class="sxs-lookup"><span data-stu-id="7d293-216">For example, searching for the term **#contoso** will only find results that contain the exact match of the hashtag.</span></span>  
  
### <a name="limitations-on-topic-names-keywords-inclusions-and-exclusions"></a><span data-ttu-id="7d293-217">Limitations on topic names, keywords, inclusions, and exclusions</span><span class="sxs-lookup"><span data-stu-id="7d293-217">Limitations on topic names, keywords, inclusions, and exclusions</span></span>  
<span data-ttu-id="7d293-218">Although you can create an unlimited number of search rules per search topic, there are limits on the length and number of terms:</span><span class="sxs-lookup"><span data-stu-id="7d293-218">Although you can create an unlimited number of search rules per search topic, there are limits on the length and number of terms:</span></span>  
  
-   <span data-ttu-id="7d293-219">Maximum length, in characters, of search topic names: 35</span><span class="sxs-lookup"><span data-stu-id="7d293-219">Maximum length, in characters, of search topic names: 35</span></span>  
  
-   <span data-ttu-id="7d293-220">Maximum length, in characters, per keyword, inclusion, or exclusion: 128</span><span class="sxs-lookup"><span data-stu-id="7d293-220">Maximum length, in characters, per keyword, inclusion, or exclusion: 128</span></span>  
  
-   <span data-ttu-id="7d293-221">Maximum number of keywords per search rule: 15</span><span class="sxs-lookup"><span data-stu-id="7d293-221">Maximum number of keywords per search rule: 15</span></span>  
  
-   <span data-ttu-id="7d293-222">Maximum number of inclusions per search rule: 15</span><span class="sxs-lookup"><span data-stu-id="7d293-222">Maximum number of inclusions per search rule: 15</span></span>  
  
-   <span data-ttu-id="7d293-223">Maximum number of exclusions per search rule: 25</span><span class="sxs-lookup"><span data-stu-id="7d293-223">Maximum number of exclusions per search rule: 25</span></span>  
  
<a name="addFacebookRule"></a>   
## <a name="add-a-facebook-pages-rule"></a><span data-ttu-id="7d293-224">Add a Facebook pages rule</span><span class="sxs-lookup"><span data-stu-id="7d293-224">Add a Facebook pages rule</span></span>  
<span data-ttu-id="7d293-225">Keep track of all conversations that happen on a [!INCLUDE[tn_facebook](../includes/tn-facebook.md)] page.</span><span class="sxs-lookup"><span data-stu-id="7d293-225">Keep track of all conversations that happen on a [!INCLUDE[tn_facebook](../includes/tn-facebook.md)] page.</span></span> <span data-ttu-id="7d293-226">Usually, you follow conversations on a [!INCLUDE[tn_facebook](../includes/tn-facebook.md)] page in full context and don't look only at specific posts.</span><span class="sxs-lookup"><span data-stu-id="7d293-226">Usually, you follow conversations on a [!INCLUDE[tn_facebook](../includes/tn-facebook.md)] page in full context and don't look only at specific posts.</span></span> <span data-ttu-id="7d293-227">If you add a [!INCLUDE[tn_facebook](../includes/tn-facebook.md)] page to a search topic, you can make sure that all posts on the [!INCLUDE[tn_facebook](../includes/tn-facebook.md)] page (such as posts from the audience and the page, or comments from the page and the audience) are captured for further processing in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span><span class="sxs-lookup"><span data-stu-id="7d293-227">If you add a [!INCLUDE[tn_facebook](../includes/tn-facebook.md)] page to a search topic, you can make sure that all posts on the [!INCLUDE[tn_facebook](../includes/tn-facebook.md)] page (such as posts from the audience and the page, or comments from the page and the audience) are captured for further processing in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span></span>  
  
### <a name="add-a-new-facebook-pages-rule"></a><span data-ttu-id="7d293-228">Add a new Facebook pages rule</span><span class="sxs-lookup"><span data-stu-id="7d293-228">Add a new Facebook pages rule</span></span>  
  
1. <span data-ttu-id="7d293-229">Go to **Search Setup**.</span><span class="sxs-lookup"><span data-stu-id="7d293-229">Go to **Search Setup**.</span></span>  
  
2. <span data-ttu-id="7d293-230">Select the search topic that you want to add the rule to, or create a new search topic.</span><span class="sxs-lookup"><span data-stu-id="7d293-230">Select the search topic that you want to add the rule to, or create a new search topic.</span></span>  
  
3. <span data-ttu-id="7d293-231">Under **Rules**, click **Add new rule** (![Add button](media/add-icon.png "Add button")) to open the **Add Rule** page.</span><span class="sxs-lookup"><span data-stu-id="7d293-231">Under **Rules**, click **Add new rule** (![Add button](media/add-icon.png "Add button")) to open the **Add Rule** page.</span></span>  
  
4. <span data-ttu-id="7d293-232">Click **Facebook pages rule**.</span><span class="sxs-lookup"><span data-stu-id="7d293-232">Click **Facebook pages rule**.</span></span>  
  
5. <span data-ttu-id="7d293-233">In the input field, enter a [!INCLUDE[tn_facebook](../includes/tn-facebook.md)] page URL.</span><span class="sxs-lookup"><span data-stu-id="7d293-233">In the input field, enter a [!INCLUDE[tn_facebook](../includes/tn-facebook.md)] page URL.</span></span>  
  
6. <span data-ttu-id="7d293-234">From the result, select the [!INCLUDE[tn_facebook](../includes/tn-facebook.md)] page to add.</span><span class="sxs-lookup"><span data-stu-id="7d293-234">From the result, select the [!INCLUDE[tn_facebook](../includes/tn-facebook.md)] page to add.</span></span>  
  
    <span data-ttu-id="7d293-235">or</span><span class="sxs-lookup"><span data-stu-id="7d293-235">or</span></span>  
  
    <span data-ttu-id="7d293-236">Select a [!INCLUDE[tn_facebook](../includes/tn-facebook.md)] page from the social profiles that you added.</span><span class="sxs-lookup"><span data-stu-id="7d293-236">Select a [!INCLUDE[tn_facebook](../includes/tn-facebook.md)] page from the social profiles that you added.</span></span>  
  
   > [!NOTE]
   >  <span data-ttu-id="7d293-237">You can also add multiple [!INCLUDE[tn_facebook](../includes/tn-facebook.md)] profiles or pages to a rule in one step by clicking **Add** (![Add button](media/add-icon.png "Add button")) next to each page.</span><span class="sxs-lookup"><span data-stu-id="7d293-237">You can also add multiple [!INCLUDE[tn_facebook](../includes/tn-facebook.md)] profiles or pages to a rule in one step by clicking **Add** (![Add button](media/add-icon.png "Add button")) next to each page.</span></span>  
  
7. <span data-ttu-id="7d293-238">Click **Continue** in the **Add Rule** pane to add the rule to the search topic.</span><span class="sxs-lookup"><span data-stu-id="7d293-238">Click **Continue** in the **Add Rule** pane to add the rule to the search topic.</span></span>  
  
8. <span data-ttu-id="7d293-239">In the search topic pane, click **Save** (![Save button](media/save-icon.png "Save button")) to activate your rule.</span><span class="sxs-lookup"><span data-stu-id="7d293-239">In the search topic pane, click **Save** (![Save button](media/save-icon.png "Save button")) to activate your rule.</span></span>  
  
<a name="addTwitterRule"></a>   
## <a name="add-a-twitter-rule"></a><span data-ttu-id="7d293-240">Add a Twitter rule</span><span class="sxs-lookup"><span data-stu-id="7d293-240">Add a Twitter rule</span></span>  
<span data-ttu-id="7d293-241">Follow conversations on [!INCLUDE[tn_twitter](../includes/tn-twitter.md)] and add a [!INCLUDE[tn_twitter](../includes/tn-twitter.md)] rule to see tweets, mentions, replies, or retweets in a search topic.</span><span class="sxs-lookup"><span data-stu-id="7d293-241">Follow conversations on [!INCLUDE[tn_twitter](../includes/tn-twitter.md)] and add a [!INCLUDE[tn_twitter](../includes/tn-twitter.md)] rule to see tweets, mentions, replies, or retweets in a search topic.</span></span>  
  
### <a name="add-a-new-twitter-rule"></a><span data-ttu-id="7d293-242">Add a new Twitter rule</span><span class="sxs-lookup"><span data-stu-id="7d293-242">Add a new Twitter rule</span></span>  
  
1. <span data-ttu-id="7d293-243">Go to **Search Setup**.</span><span class="sxs-lookup"><span data-stu-id="7d293-243">Go to **Search Setup**.</span></span>  
  
2. <span data-ttu-id="7d293-244">Select the search topic you want to add the rule to, or create a new search topic.</span><span class="sxs-lookup"><span data-stu-id="7d293-244">Select the search topic you want to add the rule to, or create a new search topic.</span></span>  
  
3. <span data-ttu-id="7d293-245">Under **Rules**, click **Add new rule** (![Add button](media/add-icon.png "Add button")) to open the **Add Rule** page.</span><span class="sxs-lookup"><span data-stu-id="7d293-245">Under **Rules**, click **Add new rule** (![Add button](media/add-icon.png "Add button")) to open the **Add Rule** page.</span></span>  
  
4. <span data-ttu-id="7d293-246">Click **Twitter rule**.</span><span class="sxs-lookup"><span data-stu-id="7d293-246">Click **Twitter rule**.</span></span>  
  
5. <span data-ttu-id="7d293-247">In the search field, enter the [!INCLUDE[tn_twitter](../includes/tn-twitter.md)] \@username that you want to track.</span><span class="sxs-lookup"><span data-stu-id="7d293-247">In the search field, enter the [!INCLUDE[tn_twitter](../includes/tn-twitter.md)] \@username that you want to track.</span></span>  
  
   <span data-ttu-id="7d293-248">If you don't have a [!INCLUDE[tn_twitter](../includes/tn-twitter.md)] profile added to your social profiles, you need to sign in to [!INCLUDE[tn_twitter](../includes/tn-twitter.md)] first to perform searches on [!INCLUDE[tn_twitter](../includes/tn-twitter.md)].</span><span class="sxs-lookup"><span data-stu-id="7d293-248">If you don't have a [!INCLUDE[tn_twitter](../includes/tn-twitter.md)] profile added to your social profiles, you need to sign in to [!INCLUDE[tn_twitter](../includes/tn-twitter.md)] first to perform searches on [!INCLUDE[tn_twitter](../includes/tn-twitter.md)].</span></span>  
  
6. <span data-ttu-id="7d293-249">In the list of results, select the [!INCLUDE[tn_twitter](../includes/tn-twitter.md)] profile to add.</span><span class="sxs-lookup"><span data-stu-id="7d293-249">In the list of results, select the [!INCLUDE[tn_twitter](../includes/tn-twitter.md)] profile to add.</span></span>  
  
    <span data-ttu-id="7d293-250">or</span><span class="sxs-lookup"><span data-stu-id="7d293-250">or</span></span> 
  
    <span data-ttu-id="7d293-251">Select a [!INCLUDE[tn_twitter](../includes/tn-twitter.md)] profile from social profiles that have already been added.</span><span class="sxs-lookup"><span data-stu-id="7d293-251">Select a [!INCLUDE[tn_twitter](../includes/tn-twitter.md)] profile from social profiles that have already been added.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="7d293-252">[Manage social profiles](manage-social-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="7d293-252">[Manage social profiles](manage-social-profiles.md)</span></span>  
  
   > [!NOTE]
   >  <span data-ttu-id="7d293-253">You can also add multiple [!INCLUDE[tn_twitter](../includes/tn-twitter.md)] profiles to a rule in one step by clicking **Add** (![Add button](media/add-icon.png "Add button")) next to each profile.</span><span class="sxs-lookup"><span data-stu-id="7d293-253">You can also add multiple [!INCLUDE[tn_twitter](../includes/tn-twitter.md)] profiles to a rule in one step by clicking **Add** (![Add button](media/add-icon.png "Add button")) next to each profile.</span></span>  
  
7. <span data-ttu-id="7d293-254">Select the message types that you want to add to this rule.</span><span class="sxs-lookup"><span data-stu-id="7d293-254">Select the message types that you want to add to this rule.</span></span>  
  
8. <span data-ttu-id="7d293-255">Click **Continue** in the **Add Rule** pane to add the rule to the search topic.</span><span class="sxs-lookup"><span data-stu-id="7d293-255">Click **Continue** in the **Add Rule** pane to add the rule to the search topic.</span></span>  
  
9. <span data-ttu-id="7d293-256">In the search topic pane, click **Save** (![Save button](media/save-icon.png "Save button")) to activate your rule.</span><span class="sxs-lookup"><span data-stu-id="7d293-256">In the search topic pane, click **Save** (![Save button](media/save-icon.png "Save button")) to activate your rule.</span></span>  
  
<a name="privateMessagesRule"></a>   
## <a name="add-a-private-messages-rule"></a><span data-ttu-id="7d293-257">Add a private messages rule</span><span class="sxs-lookup"><span data-stu-id="7d293-257">Add a private messages rule</span></span>  
<span data-ttu-id="7d293-258">To see the details of private messages that [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] users send or receive on an added social profile, create a private messages rule in a search topic.</span><span class="sxs-lookup"><span data-stu-id="7d293-258">To see the details of private messages that [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] users send or receive on an added social profile, create a private messages rule in a search topic.</span></span> <span data-ttu-id="7d293-259">You can create a private messages rule for every social profile if the owner of the social profile allows the data acquisition of private messages.</span><span class="sxs-lookup"><span data-stu-id="7d293-259">You can create a private messages rule for every social profile if the owner of the social profile allows the data acquisition of private messages.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="7d293-260">If you add a private messages rule, all private messages (except where the message is an image only) that were sent to the selected profile are visible in your organization's [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] solution.</span><span class="sxs-lookup"><span data-stu-id="7d293-260">If you add a private messages rule, all private messages (except where the message is an image only) that were sent to the selected profile are visible in your organization's [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] solution.</span></span> <span data-ttu-id="7d293-261">All users of the solution will be able to see the private messages and their replies if they are sent through [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span><span class="sxs-lookup"><span data-stu-id="7d293-261">All users of the solution will be able to see the private messages and their replies if they are sent through [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span></span>  
> <span data-ttu-id="7d293-262">When you add a new private messages rule, posts from the past days get acquired once by [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] and thus count toward your monthly post quota.</span><span class="sxs-lookup"><span data-stu-id="7d293-262">When you add a new private messages rule, posts from the past days get acquired once by [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] and thus count toward your monthly post quota.</span></span> 
> - [!INCLUDE[tn-facebook](../includes/tn-facebook.md)]<span data-ttu-id="7d293-263">: Private messages from the past 3 days.</span><span class="sxs-lookup"><span data-stu-id="7d293-263">: Private messages from the past 3 days.</span></span>
> - [!INCLUDE[tn-twitter](../includes/tn-twitter.md)]<span data-ttu-id="7d293-264">: Up to 600 direct messages from the past 12 days.</span><span class="sxs-lookup"><span data-stu-id="7d293-264">: Up to 600 direct messages from the past 12 days.</span></span>

### <a name="add-a-new-private-messages-rule"></a><span data-ttu-id="7d293-265">Add a new private messages rule</span><span class="sxs-lookup"><span data-stu-id="7d293-265">Add a new private messages rule</span></span>  
  
1. <span data-ttu-id="7d293-266">Go to **Search Setup**.</span><span class="sxs-lookup"><span data-stu-id="7d293-266">Go to **Search Setup**.</span></span>  
  
2. <span data-ttu-id="7d293-267">Select the search topic you want to add the rule to, or create a new search topic.</span><span class="sxs-lookup"><span data-stu-id="7d293-267">Select the search topic you want to add the rule to, or create a new search topic.</span></span>  
  
3. <span data-ttu-id="7d293-268">Under **Rules**, click **Add new rule** (![Add button](media/add-icon.png "Add button")) to open the **Add Rule** page.</span><span class="sxs-lookup"><span data-stu-id="7d293-268">Under **Rules**, click **Add new rule** (![Add button](media/add-icon.png "Add button")) to open the **Add Rule** page.</span></span>  
  
4. <span data-ttu-id="7d293-269">Click **Private messages rule**.</span><span class="sxs-lookup"><span data-stu-id="7d293-269">Click **Private messages rule**.</span></span>  
  
5. <span data-ttu-id="7d293-270">Select the social profile for which you want the private messages to be available in Analytics.</span><span class="sxs-lookup"><span data-stu-id="7d293-270">Select the social profile for which you want the private messages to be available in Analytics.</span></span> <span data-ttu-id="7d293-271">Keep in mind that you can only choose from social profiles whose owners explicitly allowed data acquisition for private messages.</span><span class="sxs-lookup"><span data-stu-id="7d293-271">Keep in mind that you can only choose from social profiles whose owners explicitly allowed data acquisition for private messages.</span></span> <span data-ttu-id="7d293-272">You can also add multiple social profiles to a private messages rule in one step by clicking **Add** (![Add button](media/add-icon.png "Add button")) next to each profile.</span><span class="sxs-lookup"><span data-stu-id="7d293-272">You can also add multiple social profiles to a private messages rule in one step by clicking **Add** (![Add button](media/add-icon.png "Add button")) next to each profile.</span></span>  
  
   > [!NOTE]
   > <span data-ttu-id="7d293-273">If the system can't identify a language in a private message, or if an identified language isn't supported by [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)], these private messages will be mapped to the first selected search language in **Global Settings** > **Search Languages**.</span><span class="sxs-lookup"><span data-stu-id="7d293-273">If the system can't identify a language in a private message, or if an identified language isn't supported by [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)], these private messages will be mapped to the first selected search language in **Global Settings** > **Search Languages**.</span></span> <span data-ttu-id="7d293-274">You can't change the identified language of a post.</span><span class="sxs-lookup"><span data-stu-id="7d293-274">You can't change the identified language of a post.</span></span> <span data-ttu-id="7d293-275">Text content is critical for language recognition.</span><span class="sxs-lookup"><span data-stu-id="7d293-275">Text content is critical for language recognition.</span></span> <span data-ttu-id="7d293-276">Private messages that contain an image only don't get acquired by [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span><span class="sxs-lookup"><span data-stu-id="7d293-276">Private messages that contain an image only don't get acquired by [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span></span>

  
6. <span data-ttu-id="7d293-277">Click **Continue** in the **Add Rule** pane to add the rule to the search topic.</span><span class="sxs-lookup"><span data-stu-id="7d293-277">Click **Continue** in the **Add Rule** pane to add the rule to the search topic.</span></span>  
  
7. <span data-ttu-id="7d293-278">In the search topic pane, click **Save** (![Save button](media/save-icon.png "Save button")) to activate your rule.</span><span class="sxs-lookup"><span data-stu-id="7d293-278">In the search topic pane, click **Save** (![Save button](media/save-icon.png "Save button")) to activate your rule.</span></span>  
  
<a name="customSourceRule"></a>   
## <a name="add-a-custom-sources-rule"></a><span data-ttu-id="7d293-279">Add a custom sources rule</span><span class="sxs-lookup"><span data-stu-id="7d293-279">Add a custom sources rule</span></span> 

<span data-ttu-id="7d293-280">Create rules to gather posts from custom sources.</span><span class="sxs-lookup"><span data-stu-id="7d293-280">Create rules to gather posts from custom sources.</span></span> <span data-ttu-id="7d293-281">You can also create keyword rules that match keywords in custom source posts.</span><span class="sxs-lookup"><span data-stu-id="7d293-281">You can also create keyword rules that match keywords in custom source posts.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="7d293-282">[Add a keywords rule](add-rules-search-topic.md#addKeywordsRule)</span><span class="sxs-lookup"><span data-stu-id="7d293-282">[Add a keywords rule](add-rules-search-topic.md#addKeywordsRule)</span></span>  
  
### <a name="add-a-new-custom-sources-rule"></a><span data-ttu-id="7d293-283">Add a new custom sources rule</span><span class="sxs-lookup"><span data-stu-id="7d293-283">Add a new custom sources rule</span></span>  
  
1.  <span data-ttu-id="7d293-284">Go to **Search Setup**.</span><span class="sxs-lookup"><span data-stu-id="7d293-284">Go to **Search Setup**.</span></span>  
  
2.  <span data-ttu-id="7d293-285">Select the search topic you want to add the rule to, or create a new search topic.</span><span class="sxs-lookup"><span data-stu-id="7d293-285">Select the search topic you want to add the rule to, or create a new search topic.</span></span>  
  
3.  <span data-ttu-id="7d293-286">Under **Rules**, click **Add new rule** (![Add button](media/add-icon.png "Add button")) to open the **Add Rule** page.</span><span class="sxs-lookup"><span data-stu-id="7d293-286">Under **Rules**, click **Add new rule** (![Add button](media/add-icon.png "Add button")) to open the **Add Rule** page.</span></span>  
  
4.  <span data-ttu-id="7d293-287">Click **Custom sources rule** in the **Add Rule** pane to add the rule to the search topic.</span><span class="sxs-lookup"><span data-stu-id="7d293-287">Click **Custom sources rule** in the **Add Rule** pane to add the rule to the search topic.</span></span>  
  
5.  <span data-ttu-id="7d293-288">In the list of results, select a custom source group, and then click **Continue**.</span><span class="sxs-lookup"><span data-stu-id="7d293-288">In the list of results, select a custom source group, and then click **Continue**.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="7d293-289">You can also add multiple custom sources to a custom sources rule in one step by clicking **Add** (![Add button](media/add-icon.png "Add button")) next to each profile.</span><span class="sxs-lookup"><span data-stu-id="7d293-289">You can also add multiple custom sources to a custom sources rule in one step by clicking **Add** (![Add button](media/add-icon.png "Add button")) next to each profile.</span></span>  
  
6.  <span data-ttu-id="7d293-290">In the search topic pane, click **Save** (![Save button](media/save-icon.png "Save button")) to activate your rule.</span><span class="sxs-lookup"><span data-stu-id="7d293-290">In the search topic pane, click **Save** (![Save button](media/save-icon.png "Save button")) to activate your rule.</span></span> 

## <a name="add-a-includetnyoutubeincludestn-youtubemd-rule"></a><span data-ttu-id="7d293-291">Add a [!INCLUDE[tn_youtube](../includes/tn-youtube.md)] rule</span><span class="sxs-lookup"><span data-stu-id="7d293-291">Add a [!INCLUDE[tn_youtube](../includes/tn-youtube.md)] rule</span></span>

<span data-ttu-id="7d293-292">Gather video posts and comments from [!INCLUDE[tn_youtube](../includes/tn-youtube.md)] channels.</span><span class="sxs-lookup"><span data-stu-id="7d293-292">Gather video posts and comments from [!INCLUDE[tn_youtube](../includes/tn-youtube.md)] channels.</span></span>

> [!NOTE]
> <span data-ttu-id="7d293-293">After adding a new [!INCLUDE[tn_youtube](../includes/tn-youtube.md)] rule, it might take several hours until the first videos and comments are acquired.</span><span class="sxs-lookup"><span data-stu-id="7d293-293">After adding a new [!INCLUDE[tn_youtube](../includes/tn-youtube.md)] rule, it might take several hours until the first videos and comments are acquired.</span></span> <span data-ttu-id="7d293-294">The data acquisition of comments is focused on videos that have had user activity in the last month.</span><span class="sxs-lookup"><span data-stu-id="7d293-294">The data acquisition of comments is focused on videos that have had user activity in the last month.</span></span>

1. <span data-ttu-id="7d293-295">Go to **Search Setup**.</span><span class="sxs-lookup"><span data-stu-id="7d293-295">Go to **Search Setup**.</span></span>  
  
2. <span data-ttu-id="7d293-296">Select the search topic you want to add the rule to, or create a new search topic.</span><span class="sxs-lookup"><span data-stu-id="7d293-296">Select the search topic you want to add the rule to, or create a new search topic.</span></span>  
  
3. <span data-ttu-id="7d293-297">Under **Rules**, click **Add new rule** (![Add button](media/add-icon.png "Add button")) to open the **Add Rule** page.</span><span class="sxs-lookup"><span data-stu-id="7d293-297">Under **Rules**, click **Add new rule** (![Add button](media/add-icon.png "Add button")) to open the **Add Rule** page.</span></span>  
  
4. <span data-ttu-id="7d293-298">Click **YouTube rule**.</span><span class="sxs-lookup"><span data-stu-id="7d293-298">Click **YouTube rule**.</span></span>  
  
5. <span data-ttu-id="7d293-299">In the search field, enter the [!INCLUDE[tn_youtube](../includes/tn-youtube.md)] channel name that you want to track or select a [!INCLUDE[tn_youtube](../includes/tn-youtube.md)] profile from the list.</span><span class="sxs-lookup"><span data-stu-id="7d293-299">In the search field, enter the [!INCLUDE[tn_youtube](../includes/tn-youtube.md)] channel name that you want to track or select a [!INCLUDE[tn_youtube](../includes/tn-youtube.md)] profile from the list.</span></span>
  
   > [!NOTE]
   >  <span data-ttu-id="7d293-300">You can also add multiple [!INCLUDE[tn_youtube](../includes/tn-youtube.md)] channels to a rule in one step by clicking **Add** (![Add button](media/add-icon.png "Add button")) next to each channel.</span><span class="sxs-lookup"><span data-stu-id="7d293-300">You can also add multiple [!INCLUDE[tn_youtube](../includes/tn-youtube.md)] channels to a rule in one step by clicking **Add** (![Add button](media/add-icon.png "Add button")) next to each channel.</span></span>  
  
6. <span data-ttu-id="7d293-301">Click **Continue** in the **Add Rule** pane to add the rule to the search topic.</span><span class="sxs-lookup"><span data-stu-id="7d293-301">Click **Continue** in the **Add Rule** pane to add the rule to the search topic.</span></span>  

<a name="linkedin-page-rule"></a> 
## <a name="add-a-includepn-linkedinincludespn-linkedinmd-page-rule"></a><span data-ttu-id="7d293-302">Add a [!INCLUDE[pn-linkedin](../includes/pn-linkedin.md)] page rule</span><span class="sxs-lookup"><span data-stu-id="7d293-302">Add a [!INCLUDE[pn-linkedin](../includes/pn-linkedin.md)] page rule</span></span>

<span data-ttu-id="7d293-303">Gather posts and comments from [!INCLUDE[pn-linkedin](../includes/pn-linkedin.md)] Organization Pages that you administer.</span><span class="sxs-lookup"><span data-stu-id="7d293-303">Gather posts and comments from [!INCLUDE[pn-linkedin](../includes/pn-linkedin.md)] Organization Pages that you administer.</span></span>

1. <span data-ttu-id="7d293-304">Go to **Search Setup**.</span><span class="sxs-lookup"><span data-stu-id="7d293-304">Go to **Search Setup**.</span></span>  
  
2. <span data-ttu-id="7d293-305">Select the search topic you want to add the rule to, or create a new search topic.</span><span class="sxs-lookup"><span data-stu-id="7d293-305">Select the search topic you want to add the rule to, or create a new search topic.</span></span>  
  
3. <span data-ttu-id="7d293-306">Under **Rules**, select **Add new rule** (![Add button](media/add-icon.png "Add button")) to open the **Add Rule** page.</span><span class="sxs-lookup"><span data-stu-id="7d293-306">Under **Rules**, select **Add new rule** (![Add button](media/add-icon.png "Add button")) to open the **Add Rule** page.</span></span>  
  
4. <span data-ttu-id="7d293-307">Select **[!INCLUDE[pn-linkedin](../includes/pn-linkedin.md)] page rule**.</span><span class="sxs-lookup"><span data-stu-id="7d293-307">Select **[!INCLUDE[pn-linkedin](../includes/pn-linkedin.md)] page rule**.</span></span>  
  
5. <span data-ttu-id="7d293-308">Select the [!INCLUDE[pn-linkedin](../includes/pn-linkedin.md)] Organization Pages you want to keep track of, and then select **Add** to add them to the search rule.</span><span class="sxs-lookup"><span data-stu-id="7d293-308">Select the [!INCLUDE[pn-linkedin](../includes/pn-linkedin.md)] Organization Pages you want to keep track of, and then select **Add** to add them to the search rule.</span></span>    
  
   > [!NOTE]
   > <span data-ttu-id="7d293-309">You need to have [organization pages added to your social profiles](./manage-social-profiles.md) to add them to a rule.</span><span class="sxs-lookup"><span data-stu-id="7d293-309">You need to have [organization pages added to your social profiles](./manage-social-profiles.md) to add them to a rule.</span></span>  
  
6. <span data-ttu-id="7d293-310">Select **Continue** in the **Add Rule** pane to add the rule to the search topic.</span><span class="sxs-lookup"><span data-stu-id="7d293-310">Select **Continue** in the **Add Rule** pane to add the rule to the search topic.</span></span>

7. <span data-ttu-id="7d293-311">In the **Search Topic** pane, select **Save** to apply the changes and start data acquisition.</span><span class="sxs-lookup"><span data-stu-id="7d293-311">In the **Search Topic** pane, select **Save** to apply the changes and start data acquisition.</span></span>
  
## <a name="privacy-notices"></a><span data-ttu-id="7d293-312">Privacy notices</span><span class="sxs-lookup"><span data-stu-id="7d293-312">Privacy notices</span></span>  
[!INCLUDE[cc_privacy_msl_social_services_content](../includes/cc-privacy-msl-social-services-content.md)]  
  
[!INCLUDE[cc_privacy_msl_index_cached_data](../includes/cc-privacy-msl-index-cached-data.md)]  
  
[!INCLUDE[cc_privacy_mse_bing_social_check](../includes/cc-privacy-mse-bing-social-check.md)]  

[!include[cognitive services privacy token](../includes/cc-privacy-mse-ms-cognitive-services.md)]

### <a name="see-also"></a><span data-ttu-id="7d293-313">See also</span><span class="sxs-lookup"><span data-stu-id="7d293-313">See also</span></span>  
<span data-ttu-id="7d293-314">[Set up searches to listen to social media conversations](set-up-searches.md) </span><span class="sxs-lookup"><span data-stu-id="7d293-314">[Set up searches to listen to social media conversations](set-up-searches.md) </span></span>  
<span data-ttu-id="7d293-315">[Create or delete a search topic](create-delete-search-topic.md) </span><span class="sxs-lookup"><span data-stu-id="7d293-315">[Create or delete a search topic](create-delete-search-topic.md) </span></span>  
<span data-ttu-id="7d293-316">[Manage your post quota](manage-post-quota.md) </span><span class="sxs-lookup"><span data-stu-id="7d293-316">[Manage your post quota](manage-post-quota.md) </span></span>  
[<span data-ttu-id="7d293-317">Get started with Social Engagement</span><span class="sxs-lookup"><span data-stu-id="7d293-317">Get started with Social Engagement</span></span>](get-started.md)
