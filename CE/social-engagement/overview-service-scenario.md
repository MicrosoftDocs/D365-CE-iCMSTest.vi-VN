---
title: Customer service scenarios for Social Engagement | Microsoft Docs
description: Review service scenarios to get inspiration for how to efficiently leverage Social Engagement in your organization.
keywords: service scenario, overview, customer service, social customer service
ms.date: 03/27/2018
ms.service: dynamics-365-marketing
ms.topic: article
applies_to:
- Social Engagement
ms.assetid: 0c5c29b5-c4f8-43e2-b20e-65408303e53a
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
ms.openlocfilehash: 5d764fe1f95cf77127750274772e248cca936c4d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "375697"
---
# <a name="address-customer-service-scenarios-on-social-media-with-social-engagement"></a><span data-ttu-id="3302d-104">Address customer service scenarios on social media with Social Engagement</span><span class="sxs-lookup"><span data-stu-id="3302d-104">Address customer service scenarios on social media with Social Engagement</span></span>

<span data-ttu-id="3302d-105">Do you want to offer fast, powerful support to your customers on social channels?</span><span class="sxs-lookup"><span data-stu-id="3302d-105">Do you want to offer fast, powerful support to your customers on social channels?</span></span> <span data-ttu-id="3302d-106">This overview suggests ways you and your team can use [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] to address your customers' service requests on social media.</span><span class="sxs-lookup"><span data-stu-id="3302d-106">This overview suggests ways you and your team can use [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] to address your customers' service requests on social media.</span></span> [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] <span data-ttu-id="3302d-107">lets you keep track of requests and adds intelligence on top of this tracking.</span><span class="sxs-lookup"><span data-stu-id="3302d-107">lets you keep track of requests and adds intelligence on top of this tracking.</span></span> <span data-ttu-id="3302d-108">You can answer customers directly in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] or link them to [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps for further tracking.</span><span class="sxs-lookup"><span data-stu-id="3302d-108">You can answer customers directly in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] or link them to [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps for further tracking.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3302d-109">Prerequisites</span><span class="sxs-lookup"><span data-stu-id="3302d-109">Prerequisites</span></span>

- <span data-ttu-id="3302d-110">You (and any user you plan to work with) have a [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] license assigned.</span><span class="sxs-lookup"><span data-stu-id="3302d-110">You (and any user you plan to work with) have a [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] license assigned.</span></span>

- [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] <span data-ttu-id="3302d-111">is [set up](administer-microsoft-social-engagement.md).</span><span class="sxs-lookup"><span data-stu-id="3302d-111">is [set up](administer-microsoft-social-engagement.md).</span></span>

- <span data-ttu-id="3302d-112">[Search topics are configured](set-up-searches.md) and data acquisition is up and running.</span><span class="sxs-lookup"><span data-stu-id="3302d-112">[Search topics are configured](set-up-searches.md) and data acquisition is up and running.</span></span>

- <span data-ttu-id="3302d-113">You have the required [user roles and permissions](user-roles.md) assigned in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span><span class="sxs-lookup"><span data-stu-id="3302d-113">You have the required [user roles and permissions](user-roles.md) assigned in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span></span>

## <a name="social-customer-care-scenario-overview"></a><span data-ttu-id="3302d-114">Social customer care scenario overview</span><span class="sxs-lookup"><span data-stu-id="3302d-114">Social customer care scenario overview</span></span>

<span data-ttu-id="3302d-115">The following steps describe an end-to-end configuration for social customer care.</span><span class="sxs-lookup"><span data-stu-id="3302d-115">The following steps describe an end-to-end configuration for social customer care.</span></span> <span data-ttu-id="3302d-116">Review the steps and decide which are relevant for your customer care scenario.</span><span class="sxs-lookup"><span data-stu-id="3302d-116">Review the steps and decide which are relevant for your customer care scenario.</span></span>

1. <span data-ttu-id="3302d-117">[Enable service reps to engage with customers via social media](#manage-social-profiles-to-participate-in-conversations) by adding and sharing social profiles and streams.</span><span class="sxs-lookup"><span data-stu-id="3302d-117">[Enable service reps to engage with customers via social media](#manage-social-profiles-to-participate-in-conversations) by adding and sharing social profiles and streams.</span></span>

2. <span data-ttu-id="3302d-118">Before you start engaging with customers, you need to [create a search topic](set-up-searches.md) with rules that gather all posts that address your organization's social profiles.</span><span class="sxs-lookup"><span data-stu-id="3302d-118">Before you start engaging with customers, you need to [create a search topic](set-up-searches.md) with rules that gather all posts that address your organization's social profiles.</span></span> <span data-ttu-id="3302d-119">For example, if you added a Twitter or Facebook page profile, make sure you [allow the acquisition of private messages](manage-access-tokens.md#tokens-for-interactions-with-posts) and [create search rules](add-rules-search-topic.md) that gather private messages and all post types for the profile.</span><span class="sxs-lookup"><span data-stu-id="3302d-119">For example, if you added a Twitter or Facebook page profile, make sure you [allow the acquisition of private messages](manage-access-tokens.md#tokens-for-interactions-with-posts) and [create search rules](add-rules-search-topic.md) that gather private messages and all post types for the profile.</span></span>

3. <span data-ttu-id="3302d-120">[Add tags, automatically and manually](#use-intelligence-to-boost-productivity), and learn how automated intention analysis can help triage incoming posts.</span><span class="sxs-lookup"><span data-stu-id="3302d-120">[Add tags, automatically and manually](#use-intelligence-to-boost-productivity), and learn how automated intention analysis can help triage incoming posts.</span></span> <span data-ttu-id="3302d-121">Let [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] do some of your work for you.</span><span class="sxs-lookup"><span data-stu-id="3302d-121">Let [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] do some of your work for you.</span></span>

4. <span data-ttu-id="3302d-122">[Save time on repetitive tasks](#create-support-cases-from-social-posts).</span><span class="sxs-lookup"><span data-stu-id="3302d-122">[Save time on repetitive tasks](#create-support-cases-from-social-posts).</span></span> <span data-ttu-id="3302d-123">Create new case records in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] directly from a post within [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span><span class="sxs-lookup"><span data-stu-id="3302d-123">Create new case records in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] directly from a post within [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span></span>

5. <span data-ttu-id="3302d-124">[Collaborate with your team](#establish-workflows-and-collaborate-with-other-users) and make sure they address the right customer issue with the intended priority.</span><span class="sxs-lookup"><span data-stu-id="3302d-124">[Collaborate with your team](#establish-workflows-and-collaborate-with-other-users) and make sure they address the right customer issue with the intended priority.</span></span>

> [!NOTE]
> <span data-ttu-id="3302d-125">Some of these capabilities can be automated.</span><span class="sxs-lookup"><span data-stu-id="3302d-125">Some of these capabilities can be automated.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="3302d-126">[Route posts using automation rules](automation-rules.md)</span><span class="sxs-lookup"><span data-stu-id="3302d-126">[Route posts using automation rules](automation-rules.md)</span></span>

## <a name="manage-social-profiles-to-participate-in-conversations"></a><span data-ttu-id="3302d-127">Manage social profiles to participate in conversations</span><span class="sxs-lookup"><span data-stu-id="3302d-127">Manage social profiles to participate in conversations</span></span>

 <span data-ttu-id="3302d-128">Learn how to add and share social profiles and streams in Social Center, how to keep them up and running, and how to enable users to post on behalf of your organization.</span><span class="sxs-lookup"><span data-stu-id="3302d-128">Learn how to add and share social profiles and streams in Social Center, how to keep them up and running, and how to enable users to post on behalf of your organization.</span></span>

1. <span data-ttu-id="3302d-129">[Add a new social profile](manage-social-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="3302d-129">[Add a new social profile](manage-social-profiles.md).</span></span>

2. <span data-ttu-id="3302d-130">[Share a social profile](manage-social-profiles.md#share-a-social-profile-with-other-users).</span><span class="sxs-lookup"><span data-stu-id="3302d-130">[Share a social profile](manage-social-profiles.md#share-a-social-profile-with-other-users).</span></span>

3. <span data-ttu-id="3302d-131">[Create](social-center.md#configure-a-stream) and [share a stream](social-center.md#share-a-stream).</span><span class="sxs-lookup"><span data-stu-id="3302d-131">[Create](social-center.md#configure-a-stream) and [share a stream](social-center.md#share-a-stream).</span></span>

4. <span data-ttu-id="3302d-132">[Keep social profiles up and running](social-profiles-health-state.md).</span><span class="sxs-lookup"><span data-stu-id="3302d-132">[Keep social profiles up and running](social-profiles-health-state.md).</span></span>

## <a name="use-intelligence-to-boost-productivity"></a><span data-ttu-id="3302d-133">Use intelligence to boost productivity</span><span class="sxs-lookup"><span data-stu-id="3302d-133">Use intelligence to boost productivity</span></span>

<span data-ttu-id="3302d-134">Let [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] work for you.</span><span class="sxs-lookup"><span data-stu-id="3302d-134">Let [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] work for you.</span></span> <span data-ttu-id="3302d-135">Find out how you can add tags to important posts, automatically or manually, and learn how intention analysis can help triage incoming posts and how to automate this process.</span><span class="sxs-lookup"><span data-stu-id="3302d-135">Find out how you can add tags to important posts, automatically or manually, and learn how intention analysis can help triage incoming posts and how to automate this process.</span></span>

- <span data-ttu-id="3302d-136">[Define a new tag](tags.md#add-custom-tags) so you can add it to posts.</span><span class="sxs-lookup"><span data-stu-id="3302d-136">[Define a new tag](tags.md#add-custom-tags) so you can add it to posts.</span></span>

- <span data-ttu-id="3302d-137">Let the system learn from the tags you added and [automate the tagging of posts](tags.md#promote-custom-tags-to-auto-tags).</span><span class="sxs-lookup"><span data-stu-id="3302d-137">Let the system learn from the tags you added and [automate the tagging of posts](tags.md#promote-custom-tags-to-auto-tags).</span></span>

- <span data-ttu-id="3302d-138">Get [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] to [find the intentions in posts](tags.md#how-intention-analysis-works) to enable quick triage of large number of posts.</span><span class="sxs-lookup"><span data-stu-id="3302d-138">Get [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] to [find the intentions in posts](tags.md#how-intention-analysis-works) to enable quick triage of large number of posts.</span></span> <span data-ttu-id="3302d-139">For example, you can route support requests to your service reps.</span><span class="sxs-lookup"><span data-stu-id="3302d-139">For example, you can route support requests to your service reps.</span></span>  
  <span data-ttu-id="3302d-140">To further increase efficiency, you can automate the routing of posts by using [automation rules](automation-rules.md).</span><span class="sxs-lookup"><span data-stu-id="3302d-140">To further increase efficiency, you can automate the routing of posts by using [automation rules](automation-rules.md).</span></span>

## <a name="create-support-cases-from-social-posts"></a><span data-ttu-id="3302d-141">Create support cases from social posts</span><span class="sxs-lookup"><span data-stu-id="3302d-141">Create support cases from social posts</span></span>

<span data-ttu-id="3302d-142">Save time and minimize repetitive activities.</span><span class="sxs-lookup"><span data-stu-id="3302d-142">Save time and minimize repetitive activities.</span></span> [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] <span data-ttu-id="3302d-143">lets you create new records in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps directly from a post within [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span><span class="sxs-lookup"><span data-stu-id="3302d-143">lets you create new records in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps directly from a post within [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span></span> <span data-ttu-id="3302d-144">For example, you can create a case and assign it so the right service rep so they review and solve the case efficiently.</span><span class="sxs-lookup"><span data-stu-id="3302d-144">For example, you can create a case and assign it so the right service rep so they review and solve the case efficiently.</span></span>

1. <span data-ttu-id="3302d-145">Get an [overview](link-posts-to-dynamics-365.md) of the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] integration.</span><span class="sxs-lookup"><span data-stu-id="3302d-145">Get an [overview](link-posts-to-dynamics-365.md) of the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] integration.</span></span>

2. <span data-ttu-id="3302d-146">[Set up the connection](connect-dynamics-365-social-engagement.md) to [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="3302d-146">[Set up the connection](connect-dynamics-365-social-engagement.md) to [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps.</span></span>

3. <span data-ttu-id="3302d-147">[Set up record details](create-dynamics-365-record-from-social-post.md) for cases.</span><span class="sxs-lookup"><span data-stu-id="3302d-147">[Set up record details](create-dynamics-365-record-from-social-post.md) for cases.</span></span>

4. <span data-ttu-id="3302d-148">[Create a case from a post](create-dynamics-365-record-from-social-post.md) in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span><span class="sxs-lookup"><span data-stu-id="3302d-148">[Create a case from a post](create-dynamics-365-record-from-social-post.md) in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span></span>

## <a name="establish-workflows-and-collaborate-with-other-users"></a><span data-ttu-id="3302d-149">Establish workflows and collaborate with other users</span><span class="sxs-lookup"><span data-stu-id="3302d-149">Establish workflows and collaborate with other users</span></span>

<span data-ttu-id="3302d-150">Collaborate with your team and make sure they prioritize the right issues.</span><span class="sxs-lookup"><span data-stu-id="3302d-150">Collaborate with your team and make sure they prioritize the right issues.</span></span>

1. <span data-ttu-id="3302d-151">[Assign posts](work-with-posts.md#assign-a-post-to-other-users-in-analytics-and-social-center) to other users to distribute work across the team.</span><span class="sxs-lookup"><span data-stu-id="3302d-151">[Assign posts](work-with-posts.md#assign-a-post-to-other-users-in-analytics-and-social-center) to other users to distribute work across the team.</span></span>

2. <span data-ttu-id="3302d-152">[Share streams](social-center.md#share-a-stream) with other users so they can work on posts in near&ndash;real time.</span><span class="sxs-lookup"><span data-stu-id="3302d-152">[Share streams](social-center.md#share-a-stream) with other users so they can work on posts in near&ndash;real time.</span></span>

3. <span data-ttu-id="3302d-153">[Add labels](work-with-posts.md#add-a-label-to-a-post-in-analytics-or-social-center) to posts to route them to specific streams.</span><span class="sxs-lookup"><span data-stu-id="3302d-153">[Add labels](work-with-posts.md#add-a-label-to-a-post-in-analytics-or-social-center) to posts to route them to specific streams.</span></span>

> [!NOTE]
> [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] <span data-ttu-id="3302d-154">leverages Office 365 Groups to enable collaboration with groups of people.</span><span class="sxs-lookup"><span data-stu-id="3302d-154">leverages Office 365 Groups to enable collaboration with groups of people.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="3302d-155">[Work with Office 365 Groups in Social Engagement](office-365-groups-social-engagement.md)</span><span class="sxs-lookup"><span data-stu-id="3302d-155">[Work with Office 365 Groups in Social Engagement](office-365-groups-social-engagement.md)</span></span>

## <a name="customer-stories"></a><span data-ttu-id="3302d-156">Customer stories</span><span class="sxs-lookup"><span data-stu-id="3302d-156">Customer stories</span></span>

- [<span data-ttu-id="3302d-157">UK banking disrupted: Metro Bank reinvents customer service with Microsoft</span><span class="sxs-lookup"><span data-stu-id="3302d-157">UK banking disrupted: Metro Bank reinvents customer service with Microsoft</span></span>](https://customers.microsoft.com/story/uk-banking-disrupted-metro-bank-reinvents-customer-ser)

- [<span data-ttu-id="3302d-158">5 tips to help your business weather changes in the financial services industry</span><span class="sxs-lookup"><span data-stu-id="3302d-158">5 tips to help your business weather changes in the financial services industry</span></span>](https://customers.microsoft.com/story/5-tips-to-help-your-business-weather-changes-in-the-fi)

### <a name="see-also"></a><span data-ttu-id="3302d-159">See also</span><span class="sxs-lookup"><span data-stu-id="3302d-159">See also</span></span>

<span data-ttu-id="3302d-160">[Connect Dynamics 365 for Customer Engagement apps and Social Engagement](connect-dynamics-365-social-engagement.md) </span><span class="sxs-lookup"><span data-stu-id="3302d-160">[Connect Dynamics 365 for Customer Engagement apps and Social Engagement](connect-dynamics-365-social-engagement.md) </span></span>  
<span data-ttu-id="3302d-161">[Link posts from Social Engagement to Dynamics 365 for Customer Engagement apps](link-posts-to-dynamics-365.md) </span><span class="sxs-lookup"><span data-stu-id="3302d-161">[Link posts from Social Engagement to Dynamics 365 for Customer Engagement apps](link-posts-to-dynamics-365.md) </span></span>  
[<span data-ttu-id="3302d-162">Work with posts</span><span class="sxs-lookup"><span data-stu-id="3302d-162">Work with posts</span></span>](work-with-posts.md)
