---
title: Stay up to date with alerts in Social Engagement | Microsoft Docs
description: Learn how to set up post alerts and trend alerts to stay on top of what's happening in social media.
keywords: alerts, notification, emails
ms.date: 09/26/2018
ms.service: dynamics-365-marketing
ms.topic: article
applies_to:
- Social Engagement
ms.assetid: f2b7a251-39bf-4bb9-b963-0a98020e7f23
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
ms.openlocfilehash: cba763d4596ac53c6eca595fe477a9c711861d07
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "375629"
---
# <a name="stay-up-to-date-with-alerts"></a><span data-ttu-id="727f9-104">Stay up to date with alerts</span><span class="sxs-lookup"><span data-stu-id="727f9-104">Stay up to date with alerts</span></span>

<span data-ttu-id="727f9-105">You can create email notifications to automatically send to a group of recipients when triggered.</span><span class="sxs-lookup"><span data-stu-id="727f9-105">You can create email notifications to automatically send to a group of recipients when triggered.</span></span> <span data-ttu-id="727f9-106">Alerts are user-specific, and every user role can create them.</span><span class="sxs-lookup"><span data-stu-id="727f9-106">Alerts are user-specific, and every user role can create them.</span></span> <span data-ttu-id="727f9-107">There are two types of alerts, which are based on filters and search topics:</span><span class="sxs-lookup"><span data-stu-id="727f9-107">There are two types of alerts, which are based on filters and search topics:</span></span>

- <span data-ttu-id="727f9-108">**Post alert:** An email notification is delivered to all specified email addresses within a few hours if any new posts match the selected filters.</span><span class="sxs-lookup"><span data-stu-id="727f9-108">**Post alert:** An email notification is delivered to all specified email addresses within a few hours if any new posts match the selected filters.</span></span> <span data-ttu-id="727f9-109">A summary email is delivered to your email account.</span><span class="sxs-lookup"><span data-stu-id="727f9-109">A summary email is delivered to your email account.</span></span> 

- <span data-ttu-id="727f9-110">**Trend alert:** An email notification is delivered to all specified email addresses within a few hours if the volume of posts for any source exceeds the statistical expectation.</span><span class="sxs-lookup"><span data-stu-id="727f9-110">**Trend alert:** An email notification is delivered to all specified email addresses within a few hours if the volume of posts for any source exceeds the statistical expectation.</span></span> <span data-ttu-id="727f9-111">A trend alert notifies you only if there are significant changes in post volumes that match the filters that you defined for an alert.</span><span class="sxs-lookup"><span data-stu-id="727f9-111">A trend alert notifies you only if there are significant changes in post volumes that match the filters that you defined for an alert.</span></span>

<span data-ttu-id="727f9-112">Configure and manage your alerts in the **Alerts** area.</span><span class="sxs-lookup"><span data-stu-id="727f9-112">Configure and manage your alerts in the **Alerts** area.</span></span> <span data-ttu-id="727f9-113">Your alerts configuration is visible only to you.</span><span class="sxs-lookup"><span data-stu-id="727f9-113">Your alerts configuration is visible only to you.</span></span> <span data-ttu-id="727f9-114">Recipients of the alert won't be able to see or edit your alert configuration.</span><span class="sxs-lookup"><span data-stu-id="727f9-114">Recipients of the alert won't be able to see or edit your alert configuration.</span></span> <span data-ttu-id="727f9-115">However, an admin can remove email addresses from all alerts they are mapped to.</span><span class="sxs-lookup"><span data-stu-id="727f9-115">However, an admin can remove email addresses from all alerts they are mapped to.</span></span> 

<span data-ttu-id="727f9-116">Alert emails contain a link to the data set that matches the posts that triggered the alert.</span><span class="sxs-lookup"><span data-stu-id="727f9-116">Alert emails contain a link to the data set that matches the posts that triggered the alert.</span></span> <span data-ttu-id="727f9-117">Choose this link to open and review the content in [!include[](../includes/pn-social-engagement-short.md)].</span><span class="sxs-lookup"><span data-stu-id="727f9-117">Choose this link to open and review the content in [!include[](../includes/pn-social-engagement-short.md)].</span></span>

## <a name="view-your-alerts-list"></a><span data-ttu-id="727f9-118">View your alerts list</span><span class="sxs-lookup"><span data-stu-id="727f9-118">View your alerts list</span></span>

<span data-ttu-id="727f9-119">To review your alerts, go to **Alerts** > **Alert Configuration**.</span><span class="sxs-lookup"><span data-stu-id="727f9-119">To review your alerts, go to **Alerts** > **Alert Configuration**.</span></span>  <span data-ttu-id="727f9-120">The information that you'll see about each alert is explained in the following table.</span><span class="sxs-lookup"><span data-stu-id="727f9-120">The information that you'll see about each alert is explained in the following table.</span></span>

|<span data-ttu-id="727f9-121">List entry / symbol</span><span class="sxs-lookup"><span data-stu-id="727f9-121">List entry / symbol</span></span>|<span data-ttu-id="727f9-122">What it means</span><span class="sxs-lookup"><span data-stu-id="727f9-122">What it means</span></span>|
|--------------------------|-------------------|
|<span data-ttu-id="727f9-123">Alert symbol</span><span class="sxs-lookup"><span data-stu-id="727f9-123">Alert symbol</span></span>|<span data-ttu-id="727f9-124">Indicates whether the alert is enabled or paused.</span><span class="sxs-lookup"><span data-stu-id="727f9-124">Indicates whether the alert is enabled or paused.</span></span> <span data-ttu-id="727f9-125">A gray symbol means that the alert is inactive.</span><span class="sxs-lookup"><span data-stu-id="727f9-125">A gray symbol means that the alert is inactive.</span></span> <span data-ttu-id="727f9-126">An orange symbol means that the alert is active.</span><span class="sxs-lookup"><span data-stu-id="727f9-126">An orange symbol means that the alert is active.</span></span>|
|<span data-ttu-id="727f9-127">Alert name</span><span class="sxs-lookup"><span data-stu-id="727f9-127">Alert name</span></span>|<span data-ttu-id="727f9-128">Name you provided while setting up the alert.</span><span class="sxs-lookup"><span data-stu-id="727f9-128">Name you provided while setting up the alert.</span></span>|
|<span data-ttu-id="727f9-129">Alert type</span><span class="sxs-lookup"><span data-stu-id="727f9-129">Alert type</span></span>|<span data-ttu-id="727f9-130">Type of alert you set up.</span><span class="sxs-lookup"><span data-stu-id="727f9-130">Type of alert you set up.</span></span>|
|<span data-ttu-id="727f9-131">Delete button ![Delete button](media/trashbin-icon.png "Delete button")</span><span class="sxs-lookup"><span data-stu-id="727f9-131">Delete button ![Delete button](media/trashbin-icon.png "Delete button")</span></span>|<span data-ttu-id="727f9-132">Delete an existing alert from the list if you no longer need it.</span><span class="sxs-lookup"><span data-stu-id="727f9-132">Delete an existing alert from the list if you no longer need it.</span></span>|

## <a name="create-an-alert"></a><span data-ttu-id="727f9-133">Create an alert</span><span class="sxs-lookup"><span data-stu-id="727f9-133">Create an alert</span></span>

<span data-ttu-id="727f9-134">A simple way to create an alert is directly from your analysis.</span><span class="sxs-lookup"><span data-stu-id="727f9-134">A simple way to create an alert is directly from your analysis.</span></span> <span data-ttu-id="727f9-135">Filters and parameters that you defined for the current view will be filled in for you.</span><span class="sxs-lookup"><span data-stu-id="727f9-135">Filters and parameters that you defined for the current view will be filled in for you.</span></span> <span data-ttu-id="727f9-136">You can create an alert from every section in Analytics.</span><span class="sxs-lookup"><span data-stu-id="727f9-136">You can create an alert from every section in Analytics.</span></span> <span data-ttu-id="727f9-137">You can also go to the **Alerts** area to create an alert.</span><span class="sxs-lookup"><span data-stu-id="727f9-137">You can also go to the **Alerts** area to create an alert.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="727f9-138">[Explore more options with your data set](more-options-with-data-set.md)</span><span class="sxs-lookup"><span data-stu-id="727f9-138">[Explore more options with your data set](more-options-with-data-set.md)</span></span>

1.  <span data-ttu-id="727f9-139">Go to **Alerts** > **Alert Configuration**.</span><span class="sxs-lookup"><span data-stu-id="727f9-139">Go to **Alerts** > **Alert Configuration**.</span></span>

2.  <span data-ttu-id="727f9-140">In the **Alerts** pane, click the **Add** button ![Add button](media/add-icon.png "Add button").</span><span class="sxs-lookup"><span data-stu-id="727f9-140">In the **Alerts** pane, click the **Add** button ![Add button](media/add-icon.png "Add button").</span></span>

3.  <span data-ttu-id="727f9-141">In the alert configuration dialog box, enter a name (up to 128 characters) for your alert.</span><span class="sxs-lookup"><span data-stu-id="727f9-141">In the alert configuration dialog box, enter a name (up to 128 characters) for your alert.</span></span>

4.  <span data-ttu-id="727f9-142">Select the status of your alert.</span><span class="sxs-lookup"><span data-stu-id="727f9-142">Select the status of your alert.</span></span> <span data-ttu-id="727f9-143">If you want to be notified right away, select **Active**.</span><span class="sxs-lookup"><span data-stu-id="727f9-143">If you want to be notified right away, select **Active**.</span></span> <span data-ttu-id="727f9-144">If you prepare the alert for a specific event in the future and plan to activate it later, select **Inactive**.</span><span class="sxs-lookup"><span data-stu-id="727f9-144">If you prepare the alert for a specific event in the future and plan to activate it later, select **Inactive**.</span></span>

5.  <span data-ttu-id="727f9-145">Select the alert type to create:</span><span class="sxs-lookup"><span data-stu-id="727f9-145">Select the alert type to create:</span></span>

    - <span data-ttu-id="727f9-146">**Post Alert** to receive an alert if a post matches your filters.</span><span class="sxs-lookup"><span data-stu-id="727f9-146">**Post Alert** to receive an alert if a post matches your filters.</span></span> <span data-ttu-id="727f9-147">For post alerts, select the **No duplicates** check box if you don't want to be informed when the same content appears in multiple sources.</span><span class="sxs-lookup"><span data-stu-id="727f9-147">For post alerts, select the **No duplicates** check box if you don't want to be informed when the same content appears in multiple sources.</span></span>

    - <span data-ttu-id="727f9-148">**Trend Alert** to receive an alert if the post volume exceeds the statistical expectation for your filters.</span><span class="sxs-lookup"><span data-stu-id="727f9-148">**Trend Alert** to receive an alert if the post volume exceeds the statistical expectation for your filters.</span></span> <span data-ttu-id="727f9-149">For [trend alerts](#set-a-trend-alerts-sensitivity), select the **sensitivity** of your alert by selecting from the options.</span><span class="sxs-lookup"><span data-stu-id="727f9-149">For [trend alerts](#set-a-trend-alerts-sensitivity), select the **sensitivity** of your alert by selecting from the options.</span></span>

6.  <span data-ttu-id="727f9-150">Or, edit the data set or add more recipients for your alert.</span><span class="sxs-lookup"><span data-stu-id="727f9-150">Or, edit the data set or add more recipients for your alert.</span></span>

7.  <span data-ttu-id="727f9-151">Click **Save**.</span><span class="sxs-lookup"><span data-stu-id="727f9-151">Click **Save**.</span></span>

## <a name="change-or-delete-an-alert"></a><span data-ttu-id="727f9-152">Change or delete an alert</span><span class="sxs-lookup"><span data-stu-id="727f9-152">Change or delete an alert</span></span>

<span data-ttu-id="727f9-153">You can [edit](#change-an-alert) or [delete](#delete-an-alert) any alerts that you created in the **Alerts** area.</span><span class="sxs-lookup"><span data-stu-id="727f9-153">You can [edit](#change-an-alert) or [delete](#delete-an-alert) any alerts that you created in the **Alerts** area.</span></span> <span data-ttu-id="727f9-154">Any changes in the alert configuration are applied immediately.</span><span class="sxs-lookup"><span data-stu-id="727f9-154">Any changes in the alert configuration are applied immediately.</span></span>

> [!TIP]
> <span data-ttu-id="727f9-155">You can't change the alert type after you create a new alert.</span><span class="sxs-lookup"><span data-stu-id="727f9-155">You can't change the alert type after you create a new alert.</span></span> <span data-ttu-id="727f9-156">However, you can always edit and update the data set, recipients, and name for an existing alert.</span><span class="sxs-lookup"><span data-stu-id="727f9-156">However, you can always edit and update the data set, recipients, and name for an existing alert.</span></span>
>
> <span data-ttu-id="727f9-157">You can set an alert status to **inactive**, or you can **reactivate** an inactive alert at any time.</span><span class="sxs-lookup"><span data-stu-id="727f9-157">You can set an alert status to **inactive**, or you can **reactivate** an inactive alert at any time.</span></span> <span data-ttu-id="727f9-158">Recipients of an inactive or deleted alert will no longer receive the notification from this alert.</span><span class="sxs-lookup"><span data-stu-id="727f9-158">Recipients of an inactive or deleted alert will no longer receive the notification from this alert.</span></span>
> 
> <span data-ttu-id="727f9-159">If the alert configuration gets updated after an alert email was sent, all links in the alert email will match the updated configuration.</span><span class="sxs-lookup"><span data-stu-id="727f9-159">If the alert configuration gets updated after an alert email was sent, all links in the alert email will match the updated configuration.</span></span>

### <a name="change-an-alert"></a><span data-ttu-id="727f9-160">Change an alert</span><span class="sxs-lookup"><span data-stu-id="727f9-160">Change an alert</span></span>

1.  <span data-ttu-id="727f9-161">Go to **Alerts** > **Alert Configuration**.</span><span class="sxs-lookup"><span data-stu-id="727f9-161">Go to **Alerts** > **Alert Configuration**.</span></span>

2.  <span data-ttu-id="727f9-162">Select the alert that you want to edit.</span><span class="sxs-lookup"><span data-stu-id="727f9-162">Select the alert that you want to edit.</span></span>

3.  <span data-ttu-id="727f9-163">In the **Alert Details** pane, edit the values that you want to change.</span><span class="sxs-lookup"><span data-stu-id="727f9-163">In the **Alert Details** pane, edit the values that you want to change.</span></span>

4.  <span data-ttu-id="727f9-164">To save your changes, click **Save**.</span><span class="sxs-lookup"><span data-stu-id="727f9-164">To save your changes, click **Save**.</span></span>


### <a name="delete-an-alert"></a><span data-ttu-id="727f9-165">Delete an alert</span><span class="sxs-lookup"><span data-stu-id="727f9-165">Delete an alert</span></span>

1.  <span data-ttu-id="727f9-166">Go to **Alerts** > **Alert Configuration**.</span><span class="sxs-lookup"><span data-stu-id="727f9-166">Go to **Alerts** > **Alert Configuration**.</span></span>

2.  <span data-ttu-id="727f9-167">In the **Alerts** pane, find the alert that you want to delete, and then click the **Delete** button ![Delete button](media/trashbin-icon.png "Delete button").</span><span class="sxs-lookup"><span data-stu-id="727f9-167">In the **Alerts** pane, find the alert that you want to delete, and then click the **Delete** button ![Delete button](media/trashbin-icon.png "Delete button").</span></span>

3.  <span data-ttu-id="727f9-168">Confirm the deletion.</span><span class="sxs-lookup"><span data-stu-id="727f9-168">Confirm the deletion.</span></span>

> [!NOTE]
> <span data-ttu-id="727f9-169">If an alert has been deleted, links in the alert email will redirect to **Analytics** > **Overview** with your default time frame selected.</span><span class="sxs-lookup"><span data-stu-id="727f9-169">If an alert has been deleted, links in the alert email will redirect to **Analytics** > **Overview** with your default time frame selected.</span></span> 

## <a name="manage-alert-recipients-as-administrator"></a><span data-ttu-id="727f9-170">Manage alert recipients as administrator</span><span class="sxs-lookup"><span data-stu-id="727f9-170">Manage alert recipients as administrator</span></span>

<span data-ttu-id="727f9-171">In an administrator role, you can look up email addresses and remove them from alerts that were configured by other users in your organization.</span><span class="sxs-lookup"><span data-stu-id="727f9-171">In an administrator role, you can look up email addresses and remove them from alerts that were configured by other users in your organization.</span></span> <span data-ttu-id="727f9-172">You can also export the list of alerts that go to a specific email address.</span><span class="sxs-lookup"><span data-stu-id="727f9-172">You can also export the list of alerts that go to a specific email address.</span></span> 

1. <span data-ttu-id="727f9-173">Go to **Alerts** > **Manage Recipients**.</span><span class="sxs-lookup"><span data-stu-id="727f9-173">Go to **Alerts** > **Manage Recipients**.</span></span>

2. <span data-ttu-id="727f9-174">Enter the email address you want to search for.</span><span class="sxs-lookup"><span data-stu-id="727f9-174">Enter the email address you want to search for.</span></span>

3. <span data-ttu-id="727f9-175">Select **Remove recipient** to remove the email address from the matching alerts.</span><span class="sxs-lookup"><span data-stu-id="727f9-175">Select **Remove recipient** to remove the email address from the matching alerts.</span></span> <span data-ttu-id="727f9-176">If you remove the last recipient from an alert, the alert state is set to inactive and the owner of the alert receives an email notification.</span><span class="sxs-lookup"><span data-stu-id="727f9-176">If you remove the last recipient from an alert, the alert state is set to inactive and the owner of the alert receives an email notification.</span></span>    
<span data-ttu-id="727f9-177">Optionally, you can select **Export** to download a list of the alerts that contain this recipient.</span><span class="sxs-lookup"><span data-stu-id="727f9-177">Optionally, you can select **Export** to download a list of the alerts that contain this recipient.</span></span>


## <a name="set-a-trend-alerts-sensitivity"></a><span data-ttu-id="727f9-178">Set a trend alert's sensitivity</span><span class="sxs-lookup"><span data-stu-id="727f9-178">Set a trend alert's sensitivity</span></span>

<span data-ttu-id="727f9-179">After you create a trend alert, you may find that you receive too many (or too few) notifications.</span><span class="sxs-lookup"><span data-stu-id="727f9-179">After you create a trend alert, you may find that you receive too many (or too few) notifications.</span></span> <span data-ttu-id="727f9-180">You can adjust the sensitivity to trigger the level of alerts more precisely.</span><span class="sxs-lookup"><span data-stu-id="727f9-180">You can adjust the sensitivity to trigger the level of alerts more precisely.</span></span>

<span data-ttu-id="727f9-181">Trend alert triggers are based on the number of posts and the average number of posts from the past five similar time frames.</span><span class="sxs-lookup"><span data-stu-id="727f9-181">Trend alert triggers are based on the number of posts and the average number of posts from the past five similar time frames.</span></span> <span data-ttu-id="727f9-182">The average number of posts has a standard deviation.</span><span class="sxs-lookup"><span data-stu-id="727f9-182">The average number of posts has a standard deviation.</span></span> <span data-ttu-id="727f9-183">Sensitivity defines how many times the standard deviation is stacked on top of the average number of posts to trigger an alert.</span><span class="sxs-lookup"><span data-stu-id="727f9-183">Sensitivity defines how many times the standard deviation is stacked on top of the average number of posts to trigger an alert.</span></span>

<span data-ttu-id="727f9-184">When you work with a trend alert, you can select from five sensitivity settings:</span><span class="sxs-lookup"><span data-stu-id="727f9-184">When you work with a trend alert, you can select from five sensitivity settings:</span></span>


| <span data-ttu-id="727f9-185">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="727f9-185">Sensitivity</span></span> |                             <span data-ttu-id="727f9-186">Condition to trigger a trend alert</span><span class="sxs-lookup"><span data-stu-id="727f9-186">Condition to trigger a trend alert</span></span>                             |
|-------------|--------------------------------------------------------------------------------------------|
|  <span data-ttu-id="727f9-187">Very low</span><span class="sxs-lookup"><span data-stu-id="727f9-187">Very low</span></span>   |  <span data-ttu-id="727f9-188">Post volume &gt; (**4** &times; the standard deviation) &plus; average number of posts.</span><span class="sxs-lookup"><span data-stu-id="727f9-188">Post volume &gt; (**4** &times; the standard deviation) &plus; average number of posts.</span></span>   |
|     <span data-ttu-id="727f9-189">Low</span><span class="sxs-lookup"><span data-stu-id="727f9-189">Low</span></span>     | <span data-ttu-id="727f9-190">Post volume &gt; (**2.5** &times; the standard deviation) &plus; average number of posts.</span><span class="sxs-lookup"><span data-stu-id="727f9-190">Post volume &gt; (**2.5** &times; the standard deviation) &plus; average number of posts.</span></span>  |
|  <span data-ttu-id="727f9-191">Balanced</span><span class="sxs-lookup"><span data-stu-id="727f9-191">Balanced</span></span>   | <span data-ttu-id="727f9-192">Post volume &gt; (**1.66** &times; the standard deviation) &plus; average number of posts.</span><span class="sxs-lookup"><span data-stu-id="727f9-192">Post volume &gt; (**1.66** &times; the standard deviation) &plus; average number of posts.</span></span> |
|    <span data-ttu-id="727f9-193">High</span><span class="sxs-lookup"><span data-stu-id="727f9-193">High</span></span>     | <span data-ttu-id="727f9-194">Post volume &gt; (**1.25** &times; the standard deviation) &plus; average number of posts.</span><span class="sxs-lookup"><span data-stu-id="727f9-194">Post volume &gt; (**1.25** &times; the standard deviation) &plus; average number of posts.</span></span> |
|  <span data-ttu-id="727f9-195">Very high</span><span class="sxs-lookup"><span data-stu-id="727f9-195">Very high</span></span>  |            <span data-ttu-id="727f9-196">Post volume &gt; standard deviation &plus; average number of posts.</span><span class="sxs-lookup"><span data-stu-id="727f9-196">Post volume &gt; standard deviation &plus; average number of posts.</span></span>             |

### <a name="see-also"></a><span data-ttu-id="727f9-197">See also</span><span class="sxs-lookup"><span data-stu-id="727f9-197">See also</span></span>

 <span data-ttu-id="727f9-198">[Get started with Social Engagement](get-started.md) </span><span class="sxs-lookup"><span data-stu-id="727f9-198">[Get started with Social Engagement](get-started.md) </span></span>  
 <span data-ttu-id="727f9-199">[Use filters to see relevant data](use-filters.md) </span><span class="sxs-lookup"><span data-stu-id="727f9-199">[Use filters to see relevant data](use-filters.md) </span></span>  
 [<span data-ttu-id="727f9-200">Explore more options with your data set</span><span class="sxs-lookup"><span data-stu-id="727f9-200">Explore more options with your data set</span></span>](more-options-with-data-set.md)
