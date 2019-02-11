---
title: Manage the quality of your search results in Social Engagement | Microsoft Docs
description: Learn how to increase the quality of your search results.
keywords: block content, block authors
ms.date: 07/11/2018
ms.service: dynamics-365-marketing
ms.topic: article
applies_to:
- Social Engagement
ms.assetid: 302a0005-c7b0-4247-8d2d-663685716b75
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
ms.openlocfilehash: 05dc192ce54d5554f1bdb60badc7f5d7fb254bbb
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "375540"
---
# <a name="manage-the-quality-of-your-search-results"></a><span data-ttu-id="fa167-104">Manage the quality of your search results</span><span class="sxs-lookup"><span data-stu-id="fa167-104">Manage the quality of your search results</span></span>
<span data-ttu-id="fa167-105">You can perform quality management over the entire application by blocking irrelevant posts and sources.</span><span class="sxs-lookup"><span data-stu-id="fa167-105">You can perform quality management over the entire application by blocking irrelevant posts and sources.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="fa167-106">As an Administrator or a Power Analyst, you can add terms to the list of blocked content to delete the matching posts in your analysis, or block entire domains from the data acquisition and delete already-acquired posts from these domains.</span><span class="sxs-lookup"><span data-stu-id="fa167-106">As an Administrator or a Power Analyst, you can add terms to the list of blocked content to delete the matching posts in your analysis, or block entire domains from the data acquisition and delete already-acquired posts from these domains.</span></span> <span data-ttu-id="fa167-107">Deleted posts are deducted from your monthly post quota.</span><span class="sxs-lookup"><span data-stu-id="fa167-107">Deleted posts are deducted from your monthly post quota.</span></span>  
  
> [!TIP]
>  <span data-ttu-id="fa167-108">This topic is part of a walkthrough on how you can set up searches.</span><span class="sxs-lookup"><span data-stu-id="fa167-108">This topic is part of a walkthrough on how you can set up searches.</span></span> <span data-ttu-id="fa167-109">More information: [Set up searches to listen to social media conversations](set-up-searches.md)</span><span class="sxs-lookup"><span data-stu-id="fa167-109">More information: [Set up searches to listen to social media conversations](set-up-searches.md)</span></span>  
  
## <a name="block-domains-from-your-sources"></a><span data-ttu-id="fa167-110">Block domains from your sources</span><span class="sxs-lookup"><span data-stu-id="fa167-110">Block domains from your sources</span></span>  
 <span data-ttu-id="fa167-111">To improve the quality of your organization’s data, you can block URLs that aren’t required.</span><span class="sxs-lookup"><span data-stu-id="fa167-111">To improve the quality of your organization’s data, you can block URLs that aren’t required.</span></span> <span data-ttu-id="fa167-112">You can add URLs and partial URLs to a blocked sources list that will be excluded from data acquisition and analysis.</span><span class="sxs-lookup"><span data-stu-id="fa167-112">You can add URLs and partial URLs to a blocked sources list that will be excluded from data acquisition and analysis.</span></span> <span data-ttu-id="fa167-113">Posts that were already acquired from a source on your blocked list are deleted from the database four hours after you add the domain to the list.</span><span class="sxs-lookup"><span data-stu-id="fa167-113">Posts that were already acquired from a source on your blocked list are deleted from the database four hours after you add the domain to the list.</span></span> <span data-ttu-id="fa167-114">In the meantime, posts from this source are hidden.</span><span class="sxs-lookup"><span data-stu-id="fa167-114">In the meantime, posts from this source are hidden.</span></span>  
  
 <span data-ttu-id="fa167-115">For example, you find multiple posts from a specific blog with irrelevant content or spam.</span><span class="sxs-lookup"><span data-stu-id="fa167-115">For example, you find multiple posts from a specific blog with irrelevant content or spam.</span></span> <span data-ttu-id="fa167-116">Instead of deleting every post manually from your analysis, you can add the blog URL to the blocked sources list.</span><span class="sxs-lookup"><span data-stu-id="fa167-116">Instead of deleting every post manually from your analysis, you can add the blog URL to the blocked sources list.</span></span> <span data-ttu-id="fa167-117">Even if future posts on that blog match your keywords, they won’t show up in your analysis.</span><span class="sxs-lookup"><span data-stu-id="fa167-117">Even if future posts on that blog match your keywords, they won’t show up in your analysis.</span></span>  
  
 <span data-ttu-id="fa167-118">When you're not interested in posts from a specific domain, add the domain to the list of blocked domains.</span><span class="sxs-lookup"><span data-stu-id="fa167-118">When you're not interested in posts from a specific domain, add the domain to the list of blocked domains.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="fa167-119">You must remove a source from the blocked list to restart the data acquisition for that source.</span><span class="sxs-lookup"><span data-stu-id="fa167-119">You must remove a source from the blocked list to restart the data acquisition for that source.</span></span>  
  
### <a name="view-blocked-domains"></a><span data-ttu-id="fa167-120">View blocked domains</span><span class="sxs-lookup"><span data-stu-id="fa167-120">View blocked domains</span></span>  
 <span data-ttu-id="fa167-121">Every user can review the list of blocked domains to find out which URLs are blocked from data acquisition.</span><span class="sxs-lookup"><span data-stu-id="fa167-121">Every user can review the list of blocked domains to find out which URLs are blocked from data acquisition.</span></span>  
  
1.  <span data-ttu-id="fa167-122">Go to **Search Setup** > **Blocked Content**.</span><span class="sxs-lookup"><span data-stu-id="fa167-122">Go to **Search Setup** > **Blocked Content**.</span></span>  
  
2.  <span data-ttu-id="fa167-123">Review the list in the **DOMAINS** pane.</span><span class="sxs-lookup"><span data-stu-id="fa167-123">Review the list in the **DOMAINS** pane.</span></span>  
  
### <a name="block-a-domain-from-your-searches"></a><span data-ttu-id="fa167-124">Block a domain from your searches</span><span class="sxs-lookup"><span data-stu-id="fa167-124">Block a domain from your searches</span></span>  
 <span data-ttu-id="fa167-125">When you’re not interested in posts from a specific domain, add the domain to the list of blocked sources.</span><span class="sxs-lookup"><span data-stu-id="fa167-125">When you’re not interested in posts from a specific domain, add the domain to the list of blocked sources.</span></span>  
  
> [!NOTE]
> [!INCLUDE[proc_permissions_social_listening_admin_power_analyst](../includes/proc-permissions-social-listening-admin-power-analyst.md)]  
> 
> [!IMPORTANT]
>  <span data-ttu-id="fa167-126">When you add a domain to the list of blocked domains, posts from this domain will be hidden in Analytics for four hours and be irreversibly deleted afterward.</span><span class="sxs-lookup"><span data-stu-id="fa167-126">When you add a domain to the list of blocked domains, posts from this domain will be hidden in Analytics for four hours and be irreversibly deleted afterward.</span></span>  
  
1.  <span data-ttu-id="fa167-127">Go to **Search setup** > **Blocked Content**.</span><span class="sxs-lookup"><span data-stu-id="fa167-127">Go to **Search setup** > **Blocked Content**.</span></span>  
  
2.  <span data-ttu-id="fa167-128">In the **DOMAINS** pane, enter the domain or partial domain in the field.</span><span class="sxs-lookup"><span data-stu-id="fa167-128">In the **DOMAINS** pane, enter the domain or partial domain in the field.</span></span>  
  
3.  <span data-ttu-id="fa167-129">Click the **Add** button ![New or Add button](media/plus-icon.png "New or Add button").</span><span class="sxs-lookup"><span data-stu-id="fa167-129">Click the **Add** button ![New or Add button](media/plus-icon.png "New or Add button").</span></span>  
  
> [!WARNING]
>  <span data-ttu-id="fa167-130">Blocking a top-level domain also excludes all of its subdomains.</span><span class="sxs-lookup"><span data-stu-id="fa167-130">Blocking a top-level domain also excludes all of its subdomains.</span></span> <span data-ttu-id="fa167-131">For example, if you exclude `contoso.com`, the subdomain `shop.contoso.com` is also excluded.</span><span class="sxs-lookup"><span data-stu-id="fa167-131">For example, if you exclude `contoso.com`, the subdomain `shop.contoso.com` is also excluded.</span></span>  
>   
>  <span data-ttu-id="fa167-132">Blocking domains can have a severe impact on the data you already acquired.</span><span class="sxs-lookup"><span data-stu-id="fa167-132">Blocking domains can have a severe impact on the data you already acquired.</span></span> <span data-ttu-id="fa167-133">When you add a domain to the list of blocked content, all posts found on the blocked domain, including subdomains, will be removed from your database after a grace period of four hours.</span><span class="sxs-lookup"><span data-stu-id="fa167-133">When you add a domain to the list of blocked content, all posts found on the blocked domain, including subdomains, will be removed from your database after a grace period of four hours.</span></span>  
  
### <a name="remove-a-domain-from-the-list-of-blocked-sources"></a><span data-ttu-id="fa167-134">Remove a domain from the list of blocked sources</span><span class="sxs-lookup"><span data-stu-id="fa167-134">Remove a domain from the list of blocked sources</span></span>  
 <span data-ttu-id="fa167-135">Reactivate the data acquisition from a blocked source by removing the domain from the list.</span><span class="sxs-lookup"><span data-stu-id="fa167-135">Reactivate the data acquisition from a blocked source by removing the domain from the list.</span></span>  
  
> [!NOTE]
> [!INCLUDE[proc_permissions_social_listening_admin_power_analyst](../includes/proc-permissions-social-listening-admin-power-analyst.md)]  
  
1.  <span data-ttu-id="fa167-136">Go to **Search setup** > **Blocked Content**.</span><span class="sxs-lookup"><span data-stu-id="fa167-136">Go to **Search setup** > **Blocked Content**.</span></span>  
  
2.  <span data-ttu-id="fa167-137">Find the source you want to remove from the list and re-enable for data acquisition, and then click the **Delete** button ![Delete button](media/trashbin-icon.png "Delete button").</span><span class="sxs-lookup"><span data-stu-id="fa167-137">Find the source you want to remove from the list and re-enable for data acquisition, and then click the **Delete** button ![Delete button](media/trashbin-icon.png "Delete button").</span></span>  
  
3.  <span data-ttu-id="fa167-138">In the confirmation message, click **CONFIRM**.</span><span class="sxs-lookup"><span data-stu-id="fa167-138">In the confirmation message, click **CONFIRM**.</span></span>  
  
4.  <span data-ttu-id="fa167-139">The data acquisition for the selected domain will restart.</span><span class="sxs-lookup"><span data-stu-id="fa167-139">The data acquisition for the selected domain will restart.</span></span>  
  
## <a name="block-keywords-and-terms-from-your-searches"></a><span data-ttu-id="fa167-140">Block keywords and terms from your searches</span><span class="sxs-lookup"><span data-stu-id="fa167-140">Block keywords and terms from your searches</span></span>  
 <span data-ttu-id="fa167-141">Exclude a specific term (word or phrase) by adding it to the blocked content list.</span><span class="sxs-lookup"><span data-stu-id="fa167-141">Exclude a specific term (word or phrase) by adding it to the blocked content list.</span></span> <span data-ttu-id="fa167-142">Terms on the blocked content list cause matching posts to be deleted from the database.</span><span class="sxs-lookup"><span data-stu-id="fa167-142">Terms on the blocked content list cause matching posts to be deleted from the database.</span></span> <span data-ttu-id="fa167-143">Because terms on the blocked content list act as a global exclusion, it’s a very efficient way to improve the quality of your data.</span><span class="sxs-lookup"><span data-stu-id="fa167-143">Because terms on the blocked content list act as a global exclusion, it’s a very efficient way to improve the quality of your data.</span></span> <span data-ttu-id="fa167-144">However, be cautious of unintentionally deleting relevant posts.</span><span class="sxs-lookup"><span data-stu-id="fa167-144">However, be cautious of unintentionally deleting relevant posts.</span></span>  
  
 <span data-ttu-id="fa167-145">Posts that don't show up in Analytics because of your blocked content settings don't count toward your post quota.</span><span class="sxs-lookup"><span data-stu-id="fa167-145">Posts that don't show up in Analytics because of your blocked content settings don't count toward your post quota.</span></span>  
  
 <span data-ttu-id="fa167-146">For example, if you’re listening to multiple search topics about cars, but don’t want to see any posts that mention the keyword “insurance,” you can add this term to the blocked content list.</span><span class="sxs-lookup"><span data-stu-id="fa167-146">For example, if you’re listening to multiple search topics about cars, but don’t want to see any posts that mention the keyword “insurance,” you can add this term to the blocked content list.</span></span> <span data-ttu-id="fa167-147">This deletes all posts that mention “insurance,” and posts that contain this term are no longer acquired by your search topics.</span><span class="sxs-lookup"><span data-stu-id="fa167-147">This deletes all posts that mention “insurance,” and posts that contain this term are no longer acquired by your search topics.</span></span>  
  
### <a name="view-excluded-keywords"></a><span data-ttu-id="fa167-148">View excluded keywords</span><span class="sxs-lookup"><span data-stu-id="fa167-148">View excluded keywords</span></span>  
 <span data-ttu-id="fa167-149">Every user can review the list of blocked content to find out which words or phrases are blocked from data acquisition.</span><span class="sxs-lookup"><span data-stu-id="fa167-149">Every user can review the list of blocked content to find out which words or phrases are blocked from data acquisition.</span></span>  
  
1.  <span data-ttu-id="fa167-150">Go to **Search setup** > **Blocked Content**.</span><span class="sxs-lookup"><span data-stu-id="fa167-150">Go to **Search setup** > **Blocked Content**.</span></span>  
  
2.  <span data-ttu-id="fa167-151">Review the list of excluded keywords below the text input field.</span><span class="sxs-lookup"><span data-stu-id="fa167-151">Review the list of excluded keywords below the text input field.</span></span>  
  
### <a name="block-keywords-from-your-search-results"></a><span data-ttu-id="fa167-152">Block keywords from your search results</span><span class="sxs-lookup"><span data-stu-id="fa167-152">Block keywords from your search results</span></span>  
 <span data-ttu-id="fa167-153">Acting as global exclusions, keywords and phrases you add to the list of blocked content will be deleted from your analysis, and already-acquired posts  removed from the database.</span><span class="sxs-lookup"><span data-stu-id="fa167-153">Acting as global exclusions, keywords and phrases you add to the list of blocked content will be deleted from your analysis, and already-acquired posts  removed from the database.</span></span>  
  
> [!NOTE]
> [!INCLUDE[proc_permissions_social_listening_admin_power_analyst](../includes/proc-permissions-social-listening-admin-power-analyst.md)]  
> 
> [!IMPORTANT]
>  <span data-ttu-id="fa167-154">When you add a keyword to the list of blocked keywords, posts matching this keyword will be hidden in Analytics for four hours and be irreversibly deleted  afterward.</span><span class="sxs-lookup"><span data-stu-id="fa167-154">When you add a keyword to the list of blocked keywords, posts matching this keyword will be hidden in Analytics for four hours and be irreversibly deleted  afterward.</span></span>  
  
1.  <span data-ttu-id="fa167-155">Go to **Search setup** > **Blocked Content**.</span><span class="sxs-lookup"><span data-stu-id="fa167-155">Go to **Search setup** > **Blocked Content**.</span></span>  
  
2.  <span data-ttu-id="fa167-156">Type the term in the input field.</span><span class="sxs-lookup"><span data-stu-id="fa167-156">Type the term in the input field.</span></span>  
  
3.  <span data-ttu-id="fa167-157">Click the **Add** button ![New or Add button](media/plus-icon.png "New or Add button").</span><span class="sxs-lookup"><span data-stu-id="fa167-157">Click the **Add** button ![New or Add button](media/plus-icon.png "New or Add button").</span></span>  
  
### <a name="remove-a-keyword-from-blocked-content"></a><span data-ttu-id="fa167-158">Remove a keyword from blocked content</span><span class="sxs-lookup"><span data-stu-id="fa167-158">Remove a keyword from blocked content</span></span>  
 <span data-ttu-id="fa167-159">Remove a global exclusion and restart the data acquisition for posts matching this keyword by removing a keyword from the blocked content list.</span><span class="sxs-lookup"><span data-stu-id="fa167-159">Remove a global exclusion and restart the data acquisition for posts matching this keyword by removing a keyword from the blocked content list.</span></span>  
  
> [!NOTE]
> [!INCLUDE[proc_permissions_social_listening_admin_power_analyst](../includes/proc-permissions-social-listening-admin-power-analyst.md)] <span data-ttu-id="fa167-160">Data acquisition restarts after removing a keyword from the list of blocked content.</span><span class="sxs-lookup"><span data-stu-id="fa167-160">Data acquisition restarts after removing a keyword from the list of blocked content.</span></span> <span data-ttu-id="fa167-161">Posts aren’t acquired retroactively.</span><span class="sxs-lookup"><span data-stu-id="fa167-161">Posts aren’t acquired retroactively.</span></span>  
  
1.  <span data-ttu-id="fa167-162">Go to **Search Setup** > **Blocked Content**.</span><span class="sxs-lookup"><span data-stu-id="fa167-162">Go to **Search Setup** > **Blocked Content**.</span></span>  
  
2.  <span data-ttu-id="fa167-163">Identify the list entry you want to remove from the blocked content, and then  click the **Delete** button ![Delete button](media/trashbin-icon.png "Delete button").</span><span class="sxs-lookup"><span data-stu-id="fa167-163">Identify the list entry you want to remove from the blocked content, and then  click the **Delete** button ![Delete button](media/trashbin-icon.png "Delete button").</span></span>  
  
3.  <span data-ttu-id="fa167-164">In the confirmation message, click **CONFIRM**.</span><span class="sxs-lookup"><span data-stu-id="fa167-164">In the confirmation message, click **CONFIRM**.</span></span>  
  
## <a name="manage-the-data-acquisition-volume"></a><span data-ttu-id="fa167-165">Manage the data acquisition volume</span><span class="sxs-lookup"><span data-stu-id="fa167-165">Manage the data acquisition volume</span></span>  
  
- <span data-ttu-id="fa167-166">Optimize your search topics regularly.</span><span class="sxs-lookup"><span data-stu-id="fa167-166">Optimize your search topics regularly.</span></span> <span data-ttu-id="fa167-167">Review the rules to make sure that only relevant data is selected.</span><span class="sxs-lookup"><span data-stu-id="fa167-167">Review the rules to make sure that only relevant data is selected.</span></span> <span data-ttu-id="fa167-168">Validate your rules before saving the search topic to get an idea of how many posts you’re expecting for the configuration you provided.</span><span class="sxs-lookup"><span data-stu-id="fa167-168">Validate your rules before saving the search topic to get an idea of how many posts you’re expecting for the configuration you provided.</span></span>  
  
- <span data-ttu-id="fa167-169">Maintain a list of blocked sources to delete matching posts and avoid any posts appearing in your results from the listed domains.</span><span class="sxs-lookup"><span data-stu-id="fa167-169">Maintain a list of blocked sources to delete matching posts and avoid any posts appearing in your results from the listed domains.</span></span> <span data-ttu-id="fa167-170">When you add a source to the list of blocked sources, posts from this source will be hidden in Analytics for four hours and be irreversibly deleted afterward.</span><span class="sxs-lookup"><span data-stu-id="fa167-170">When you add a source to the list of blocked sources, posts from this source will be hidden in Analytics for four hours and be irreversibly deleted afterward.</span></span>  
  
- <span data-ttu-id="fa167-171">Maintain a list of blocked terms to delete matching posts and avoid any posts appearing in your results that match the listed terms.</span><span class="sxs-lookup"><span data-stu-id="fa167-171">Maintain a list of blocked terms to delete matching posts and avoid any posts appearing in your results that match the listed terms.</span></span> <span data-ttu-id="fa167-172">When you add a term to the list of blocked terms, posts matching this term will be hidden in Analytics for four hours and be irreversibly deleted afterward.</span><span class="sxs-lookup"><span data-stu-id="fa167-172">When you add a term to the list of blocked terms, posts matching this term will be hidden in Analytics for four hours and be irreversibly deleted afterward.</span></span>  
  
- <span data-ttu-id="fa167-173">Exclude authors who publish irrelevant posts that match one of your search topics.</span><span class="sxs-lookup"><span data-stu-id="fa167-173">Exclude authors who publish irrelevant posts that match one of your search topics.</span></span>  
  
-   <span data-ttu-id="fa167-174">[Get additional post quota](manage-post-quota.md).</span><span class="sxs-lookup"><span data-stu-id="fa167-174">[Get additional post quota](manage-post-quota.md).</span></span> <span data-ttu-id="fa167-175">Ask your [!INCLUDE[pn_Office_365](../includes/pn-office-365.md)] admin to add more posts to your solution’s quota in the [Office 365 admin center](https://portal.office.com/).</span><span class="sxs-lookup"><span data-stu-id="fa167-175">Ask your [!INCLUDE[pn_Office_365](../includes/pn-office-365.md)] admin to add more posts to your solution’s quota in the [Office 365 admin center](https://portal.office.com/).</span></span>  
  
### <a name="privacy-notice"></a><span data-ttu-id="fa167-176">Privacy notice</span><span class="sxs-lookup"><span data-stu-id="fa167-176">Privacy notice</span></span>  
 [!INCLUDE[cc_privacy_msl_social_services_content](../includes/cc-privacy-msl-social-services-content.md)]  
  
### <a name="see-also"></a><span data-ttu-id="fa167-177">See Also</span><span class="sxs-lookup"><span data-stu-id="fa167-177">See Also</span></span>  
 <span data-ttu-id="fa167-178">[Set up searches to listen to social media conversations](set-up-searches.md) </span><span class="sxs-lookup"><span data-stu-id="fa167-178">[Set up searches to listen to social media conversations](set-up-searches.md) </span></span>  
 [<span data-ttu-id="fa167-179">Refine your search rules</span><span class="sxs-lookup"><span data-stu-id="fa167-179">Refine your search rules</span></span>](refine-search-rules.md)
 
