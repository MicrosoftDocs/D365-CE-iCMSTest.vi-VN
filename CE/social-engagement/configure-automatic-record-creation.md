---
title: Set up record creation for social activity entities from Social Engagement | Microsoft Docs
description: Learn how to configure rules in Dynamics 365 for Customer Engagement apps to automatically turn social activities into records.
keywords: rule framework, update rules, create record, entity mapping
ms.date: 01/30/2018
ms.service: dynamics-365-marketing
ms.topic: article
applies_to:
- Social Engagement
ms.assetid: 74f05ebd-73b9-597f-45a5-6faf66c99967
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
ms.openlocfilehash: 96e595adb9ba3429822e63aaa7534ef5e99ecba1
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "375630"
---
# <a name="configure-automatic-record-creation-and-update-rules-to-process-social-activity-entities"></a><span data-ttu-id="05ee9-104">Configure Automatic Record Creation and Update Rules to process Social Activity entities</span><span class="sxs-lookup"><span data-stu-id="05ee9-104">Configure Automatic Record Creation and Update Rules to process Social Activity entities</span></span>

<span data-ttu-id="05ee9-105">To automatically create an entity record (such as a Case or a Lead) from a Social Activity record in [!include[](../includes/pn-dynamics-crm.md)] apps, an administrator or customizer must configure Automatic Record Creation and Update Rules.</span><span class="sxs-lookup"><span data-stu-id="05ee9-105">To automatically create an entity record (such as a Case or a Lead) from a Social Activity record in [!include[](../includes/pn-dynamics-crm.md)] apps, an administrator or customizer must configure Automatic Record Creation and Update Rules.</span></span>

<span data-ttu-id="05ee9-106">In [!INCLUDE[MSE](../includes/pn-social-engagement-short.md)], when users [link a post to Dynamics 365 for Customer Engagement apps](link-posts-to-dynamics-365.md), a Social Activity record is created in the connected [!include[](../includes/pn-dynamics-crm.md)] instance.</span><span class="sxs-lookup"><span data-stu-id="05ee9-106">In [!INCLUDE[MSE](../includes/pn-social-engagement-short.md)], when users [link a post to Dynamics 365 for Customer Engagement apps](link-posts-to-dynamics-365.md), a Social Activity record is created in the connected [!include[](../includes/pn-dynamics-crm.md)] instance.</span></span> <span data-ttu-id="05ee9-107">The entity type the user creates in [!INCLUDE[MSE](../includes/pn-social-engagement-short.md)] (Case, Lead, and so on) is passed on as part of the [JSON Payload](create-dynamics-365-record-from-social-post.md) to the social activity in [!include[](../includes/pn-dynamics-crm.md)].</span><span class="sxs-lookup"><span data-stu-id="05ee9-107">The entity type the user creates in [!INCLUDE[MSE](../includes/pn-social-engagement-short.md)] (Case, Lead, and so on) is passed on as part of the [JSON Payload](create-dynamics-365-record-from-social-post.md) to the social activity in [!include[](../includes/pn-dynamics-crm.md)].</span></span>


> [!IMPORTANT]
>  <span data-ttu-id="05ee9-108">Without Automatic Record Creation and Update Rules, the Social Activity record does not automatically result in a corresponding [!include[](../includes/pn-dynamics-crm.md)] entity record (such as a Case or Lead record).</span><span class="sxs-lookup"><span data-stu-id="05ee9-108">Without Automatic Record Creation and Update Rules, the Social Activity record does not automatically result in a corresponding [!include[](../includes/pn-dynamics-crm.md)] entity record (such as a Case or Lead record).</span></span>

<span data-ttu-id="05ee9-109">![Open drop-down menu with Case and Lead option for creating a record in Dynamics 365 for Customer Engagement from within Social Engagement.](media/select-entity-mse.png "Open drop-down menu with Case and Lead options for creating a record in Dynamics 365 for Customer Engagement from within Social Engagement")</span><span class="sxs-lookup"><span data-stu-id="05ee9-109">![Open drop-down menu with Case and Lead option for creating a record in Dynamics 365 for Customer Engagement from within Social Engagement.](media/select-entity-mse.png "Open drop-down menu with Case and Lead options for creating a record in Dynamics 365 for Customer Engagement from within Social Engagement")</span></span>

## <a name="create-a-rule-to-automatically-turn-social-activities-into-lead-or-case-records"></a><span data-ttu-id="05ee9-110">Create a rule to automatically turn social activities into Lead or Case records</span><span class="sxs-lookup"><span data-stu-id="05ee9-110">Create a rule to automatically turn social activities into Lead or Case records</span></span>

1. <span data-ttu-id="05ee9-111">Sign in to [!include[](../includes/pn-dynamics-crm.md)] with your system administrator or customizer credentials.</span><span class="sxs-lookup"><span data-stu-id="05ee9-111">Sign in to [!include[](../includes/pn-dynamics-crm.md)] with your system administrator or customizer credentials.</span></span>

2. <span data-ttu-id="05ee9-112">Go to **Settings** > **Business Management** > **Automatic Record Creation and Update Rules**.</span><span class="sxs-lookup"><span data-stu-id="05ee9-112">Go to **Settings** > **Business Management** > **Automatic Record Creation and Update Rules**.</span></span>

   <span data-ttu-id="05ee9-113">![Clickpath to access Automatic record Creation and Update Rules settings.](media/business-management-settings-D365.png "Access Automatic Record Creation and Update Rules settings")</span><span class="sxs-lookup"><span data-stu-id="05ee9-113">![Clickpath to access Automatic record Creation and Update Rules settings.](media/business-management-settings-D365.png "Access Automatic Record Creation and Update Rules settings")</span></span>

3. <span data-ttu-id="05ee9-114">Select **New** to create a new rule.</span><span class="sxs-lookup"><span data-stu-id="05ee9-114">Select **New** to create a new rule.</span></span>

   <span data-ttu-id="05ee9-115">![Position of New control to create new rules.](media/new-record-creation-update-rule.png "Location of the New command to create new rules")</span><span class="sxs-lookup"><span data-stu-id="05ee9-115">![Position of New control to create new rules.](media/new-record-creation-update-rule.png "Location of the New command to create new rules")</span></span>

4. <span data-ttu-id="05ee9-116">Provide a **Name** for the rule.</span><span class="sxs-lookup"><span data-stu-id="05ee9-116">Provide a **Name** for the rule.</span></span>

5. <span data-ttu-id="05ee9-117">Set the **Source Type** to **Social Activity**.</span><span class="sxs-lookup"><span data-stu-id="05ee9-117">Set the **Source Type** to **Social Activity**.</span></span>

6. <span data-ttu-id="05ee9-118">Click **Save** to create the record.</span><span class="sxs-lookup"><span data-stu-id="05ee9-118">Click **Save** to create the record.</span></span>

   <span data-ttu-id="05ee9-119">![Highlighted areas for Name, Source Type, and Save control.](media/create-record-creation-update-rule.png "Location of areas for Name, Source Type, and the Save command")</span><span class="sxs-lookup"><span data-stu-id="05ee9-119">![Highlighted areas for Name, Source Type, and Save control.](media/create-record-creation-update-rule.png "Location of areas for Name, Source Type, and the Save command")</span></span>

7. <span data-ttu-id="05ee9-120">Under **Channel Properties**, select **Additional Properties**.</span><span class="sxs-lookup"><span data-stu-id="05ee9-120">Under **Channel Properties**, select **Additional Properties**.</span></span>

8. <span data-ttu-id="05ee9-121">Select the **Search** button, and then select **New**.</span><span class="sxs-lookup"><span data-stu-id="05ee9-121">Select the **Search** button, and then select **New**.</span></span>

9. <span data-ttu-id="05ee9-122">In the new dialog box, provide a **Name** for the Channel Property Group.</span><span class="sxs-lookup"><span data-stu-id="05ee9-122">In the new dialog box, provide a **Name** for the Channel Property Group.</span></span> <span data-ttu-id="05ee9-123">For **Source Type**, select **Social Activity**.</span><span class="sxs-lookup"><span data-stu-id="05ee9-123">For **Source Type**, select **Social Activity**.</span></span>

10. <span data-ttu-id="05ee9-124">Select **Save**.</span><span class="sxs-lookup"><span data-stu-id="05ee9-124">Select **Save**.</span></span>

11. <span data-ttu-id="05ee9-125">Select **Add Channel Property record** in the newly created Channel Property Group.</span><span class="sxs-lookup"><span data-stu-id="05ee9-125">Select **Add Channel Property record** in the newly created Channel Property Group.</span></span> <span data-ttu-id="05ee9-126">Enter **userPreferredTargetEntity** for the name, and set the **Data Type** to **Single Line of Text**.</span><span class="sxs-lookup"><span data-stu-id="05ee9-126">Enter **userPreferredTargetEntity** for the name, and set the **Data Type** to **Single Line of Text**.</span></span> <span data-ttu-id="05ee9-127">It's important that you match the name as documented in the [JSON payload](create-dynamics-365-record-from-social-post.md).</span><span class="sxs-lookup"><span data-stu-id="05ee9-127">It's important that you match the name as documented in the [JSON payload](create-dynamics-365-record-from-social-post.md).</span></span> <span data-ttu-id="05ee9-128">Now that the Channel Property is in place, you create the actual update rules.</span><span class="sxs-lookup"><span data-stu-id="05ee9-128">Now that the Channel Property is in place, you create the actual update rules.</span></span> 

12. <span data-ttu-id="05ee9-129">Select **Save**, and then close the dialog boxes.</span><span class="sxs-lookup"><span data-stu-id="05ee9-129">Select **Save**, and then close the dialog boxes.</span></span>

    <span data-ttu-id="05ee9-130">![Details of the Channel Property record for the Social Engagement payload](media/channel-property-group-userPreferredTargetEntity.png "Details of the Channel Property record for the Social Engagement payload")</span><span class="sxs-lookup"><span data-stu-id="05ee9-130">![Details of the Channel Property record for the Social Engagement payload](media/channel-property-group-userPreferredTargetEntity.png "Details of the Channel Property record for the Social Engagement payload")</span></span>


13. <span data-ttu-id="05ee9-131">In **Record Creation and Update Rule**, select **Add Record Creation and Update Rule Item record**.</span><span class="sxs-lookup"><span data-stu-id="05ee9-131">In **Record Creation and Update Rule**, select **Add Record Creation and Update Rule Item record**.</span></span>

    <span data-ttu-id="05ee9-132">![Highlighted area of the New rule control.](media/specify-record-creation-and-update-details.png "Location of the New Rule command")</span><span class="sxs-lookup"><span data-stu-id="05ee9-132">![Highlighted area of the New rule control.](media/specify-record-creation-and-update-details.png "Location of the New Rule command")</span></span>

14. <span data-ttu-id="05ee9-133">In the new dialog box that opens, provide a **Name** for the rule and then select **Save** to create the rule.</span><span class="sxs-lookup"><span data-stu-id="05ee9-133">In the new dialog box that opens, provide a **Name** for the rule and then select **Save** to create the rule.</span></span>

15. <span data-ttu-id="05ee9-134">Under **Condition**, choose **Select**, and scroll to the bottom of the drop-down list to find **Channel Properties** under **Local Values**.</span><span class="sxs-lookup"><span data-stu-id="05ee9-134">Under **Condition**, choose **Select**, and scroll to the bottom of the drop-down list to find **Channel Properties** under **Local Values**.</span></span> <span data-ttu-id="05ee9-135">Then, select **userPreferredTargetEntity** **Equals** **lead**.</span><span class="sxs-lookup"><span data-stu-id="05ee9-135">Then, select **userPreferredTargetEntity** **Equals** **lead**.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="05ee9-136">The value for userPreferredEntity must exactly match the value in the JSON payload.</span><span class="sxs-lookup"><span data-stu-id="05ee9-136">The value for userPreferredEntity must exactly match the value in the JSON payload.</span></span> <span data-ttu-id="05ee9-137">This value is the [!include[](../includes/pn-dynamics-crm.md)] entity type name that can be different from the name in the [!include[](../includes/pn-dynamics-crm.md)] user interface.</span><span class="sxs-lookup"><span data-stu-id="05ee9-137">This value is the [!include[](../includes/pn-dynamics-crm.md)] entity type name that can be different from the name in the [!include[](../includes/pn-dynamics-crm.md)] user interface.</span></span> <span data-ttu-id="05ee9-138">For example, the entity type name for Case is *incident*.</span><span class="sxs-lookup"><span data-stu-id="05ee9-138">For example, the entity type name for Case is *incident*.</span></span>

    <span data-ttu-id="05ee9-139">![Highlighted condition for lead field in Social Engagement payload for userPrefrerredTargetEntity.](media/lead-creation-condition.png "Condition for a Lead field in the Social Engagement payload for userPrefrerredTargetEntity")</span><span class="sxs-lookup"><span data-stu-id="05ee9-139">![Highlighted condition for lead field in Social Engagement payload for userPrefrerredTargetEntity.](media/lead-creation-condition.png "Condition for a Lead field in the Social Engagement payload for userPrefrerredTargetEntity")</span></span>

16. <span data-ttu-id="05ee9-140">Under **Action**, select **Add Step**, and then select **Create Record**.</span><span class="sxs-lookup"><span data-stu-id="05ee9-140">Under **Action**, select **Add Step**, and then select **Create Record**.</span></span> <span data-ttu-id="05ee9-141">Set the value to **Lead**.</span><span class="sxs-lookup"><span data-stu-id="05ee9-141">Set the value to **Lead**.</span></span> 

    <span data-ttu-id="05ee9-142">![Actions area with record creation set to Lead record.](media/configure-action-update-rule.png "Actions area with record creation set to Lead")</span><span class="sxs-lookup"><span data-stu-id="05ee9-142">![Actions area with record creation set to Lead record.](media/configure-action-update-rule.png "Actions area with record creation set to Lead")</span></span>

17. <span data-ttu-id="05ee9-143">Click **Save & Close** to finalize the rule.</span><span class="sxs-lookup"><span data-stu-id="05ee9-143">Click **Save & Close** to finalize the rule.</span></span>

18. <span data-ttu-id="05ee9-144">Verify that the rules were created, and then select **Activate** to activate the rule.</span><span class="sxs-lookup"><span data-stu-id="05ee9-144">Verify that the rules were created, and then select **Activate** to activate the rule.</span></span>    
    <span data-ttu-id="05ee9-145">Social Activity entities created from [!INCLUDE[MSE](../includes/pn-social-engagement-short.md)] will now automatically create the configured record type in [!include[](../includes/pn-dynamics-crm.md)].</span><span class="sxs-lookup"><span data-stu-id="05ee9-145">Social Activity entities created from [!INCLUDE[MSE](../includes/pn-social-engagement-short.md)] will now automatically create the configured record type in [!include[](../includes/pn-dynamics-crm.md)].</span></span> 

    <span data-ttu-id="05ee9-146">![Activate the newly created rule to automatically turn social activity entities into other record types.](media/activate-update-rule.png "Activate the newly created rule to automatically turn Social Activity entities into other record types")</span><span class="sxs-lookup"><span data-stu-id="05ee9-146">![Activate the newly created rule to automatically turn social activity entities into other record types.](media/activate-update-rule.png "Activate the newly created rule to automatically turn Social Activity entities into other record types")</span></span>

> [!TIP]
> <span data-ttu-id="05ee9-147">To create a Case record, repeat the steps above but select **userPreferredTargetEntity** **Equals** **incident**, and under **Action**, set the **Create Record** value to **Case**.</span><span class="sxs-lookup"><span data-stu-id="05ee9-147">To create a Case record, repeat the steps above but select **userPreferredTargetEntity** **Equals** **incident**, and under **Action**, set the **Create Record** value to **Case**.</span></span>

### <a name="see-also"></a><span data-ttu-id="05ee9-148">See also</span><span class="sxs-lookup"><span data-stu-id="05ee9-148">See also</span></span>

<span data-ttu-id="05ee9-149">[Set up the connection to link posts from Social Engagement to Dynamics 365 for Customer Engagement apps](link-posts-to-dynamics-365.md)  </span><span class="sxs-lookup"><span data-stu-id="05ee9-149">[Set up the connection to link posts from Social Engagement to Dynamics 365 for Customer Engagement apps](link-posts-to-dynamics-365.md)  </span></span>  
<span data-ttu-id="05ee9-150">[Link posts from Social Engagement to Dynamics 365 for Customer Engagement apps](create-dynamics-365-record-from-social-post.md)  </span><span class="sxs-lookup"><span data-stu-id="05ee9-150">[Link posts from Social Engagement to Dynamics 365 for Customer Engagement apps](create-dynamics-365-record-from-social-post.md)  </span></span>  
[<span data-ttu-id="05ee9-151">Set up rules to automatically create or update records in Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="05ee9-151">Set up rules to automatically create or update records in Dynamics 365 for Customer Engagement apps</span></span>](https://technet.microsoft.com/library/mt812474.aspx)
