---
title: Manage licenses for Social Engagement | Microsoft Docs
description: Learn how to manage user licenses for users of Social Engagement.
keywords: licenses, Social Engagement, Office 365, user license, assign, remove
ms.date: 12/14/2018
ms.service: dynamics-365-marketing
ms.topic: article
applies_to:
- Social Engagement
ms.assetid: 893c7cd6-80fe-61d1-93b6-93ecf3993291
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
ms.openlocfilehash: 5e21d96430d7594437e3e7a0e9dcbf78ce388232
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "375652"
---
# <a name="manage-licenses-for-includepnnetbreezeshortincludespn-social-engagement-shortmd"></a><span data-ttu-id="460e3-104">Manage licenses for [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)]</span><span class="sxs-lookup"><span data-stu-id="460e3-104">Manage licenses for [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)]</span></span>

<span data-ttu-id="460e3-105">Using the [!INCLUDE[pn_MS_Office_365](../includes/pn-ms-office-365.md)] admin center, you can manage [!INCLUDE[pn_netbreeze_long](../includes/pn-social-engagement-long.md)] user licenses and other services.</span><span class="sxs-lookup"><span data-stu-id="460e3-105">Using the [!INCLUDE[pn_MS_Office_365](../includes/pn-ms-office-365.md)] admin center, you can manage [!INCLUDE[pn_netbreeze_long](../includes/pn-social-engagement-long.md)] user licenses and other services.</span></span> <span data-ttu-id="460e3-106">This topic provides information about the steps to give users access to [!INCLUDE[pn_netbreeze_long](../includes/pn-social-engagement-long.md)].</span><span class="sxs-lookup"><span data-stu-id="460e3-106">This topic provides information about the steps to give users access to [!INCLUDE[pn_netbreeze_long](../includes/pn-social-engagement-long.md)].</span></span>  
<span data-ttu-id="460e3-107">You must be your organization's [!INCLUDE[pn_Office_365](../includes/pn-office-365.md)] administrator to perform the following tasks.</span><span class="sxs-lookup"><span data-stu-id="460e3-107">You must be your organization's [!INCLUDE[pn_Office_365](../includes/pn-office-365.md)] administrator to perform the following tasks.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="460e3-108">If your organization is eligible for Social Engagement and you've signed up for the Dynamics 365 AI for Market Insights Preview, all your existing data will be available in both applications.</span><span class="sxs-lookup"><span data-stu-id="460e3-108">If your organization is eligible for Social Engagement and you've signed up for the Dynamics 365 AI for Market Insights Preview, all your existing data will be available in both applications.</span></span> <span data-ttu-id="460e3-109">If you want to go back to using Social Engagement, a global admin can [remove your license](#remove-a-license-from-a-user) for **Dynamics 365 AI for Market Insights (Preview)** in the Office 365 admin center and ensure a Social Engagement [license is assigned](#assign-a-license-to-a-user) to you.</span><span class="sxs-lookup"><span data-stu-id="460e3-109">If you want to go back to using Social Engagement, a global admin can [remove your license](#remove-a-license-from-a-user) for **Dynamics 365 AI for Market Insights (Preview)** in the Office 365 admin center and ensure a Social Engagement [license is assigned](#assign-a-license-to-a-user) to you.</span></span> <span data-ttu-id="460e3-110">This will roll back to the experience with Social Engagement branding while persisting your data.</span><span class="sxs-lookup"><span data-stu-id="460e3-110">This will roll back to the experience with Social Engagement branding while persisting your data.</span></span> 

## <a name="prepare-your-organization"></a><span data-ttu-id="460e3-111">Prepare your organization</span><span class="sxs-lookup"><span data-stu-id="460e3-111">Prepare your organization</span></span>

<span data-ttu-id="460e3-112">For step-by-step instructions on adding a service to an existing [!INCLUDE[pn_Office_365](../includes/pn-office-365.md)] subscription, see [Office help: Manage a subscription](http://go.microsoft.com/fwlink/p/?LinkId=392376).</span><span class="sxs-lookup"><span data-stu-id="460e3-112">For step-by-step instructions on adding a service to an existing [!INCLUDE[pn_Office_365](../includes/pn-office-365.md)] subscription, see [Office help: Manage a subscription](http://go.microsoft.com/fwlink/p/?LinkId=392376).</span></span>

<span data-ttu-id="460e3-113">As a [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] customer, review [Microsoft Dynamics 365 for Customer Engagement pricing and licensing](http://go.microsoft.com/fwlink/p/?LinkID=401462) if the organization is eligible for [!INCLUDE[pn_netbreeze_long](../includes/pn-social-engagement-long.md)] user licenses.</span><span class="sxs-lookup"><span data-stu-id="460e3-113">As a [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] customer, review [Microsoft Dynamics 365 for Customer Engagement pricing and licensing](http://go.microsoft.com/fwlink/p/?LinkID=401462) if the organization is eligible for [!INCLUDE[pn_netbreeze_long](../includes/pn-social-engagement-long.md)] user licenses.</span></span>

<span data-ttu-id="460e3-114">If your school or work organization doesn't have an [!INCLUDE[pn_Office_365](../includes/pn-office-365.md)] subscription yet, you need to create an [!INCLUDE[pn_Office_365](../includes/pn-office-365.md)] tenant for your organization.</span><span class="sxs-lookup"><span data-stu-id="460e3-114">If your school or work organization doesn't have an [!INCLUDE[pn_Office_365](../includes/pn-office-365.md)] subscription yet, you need to create an [!INCLUDE[pn_Office_365](../includes/pn-office-365.md)] tenant for your organization.</span></span>

### <a name="sign-up-for-a-new-organization-on-office-365"></a><span data-ttu-id="460e3-115">Sign up for a new organization on Office 365</span><span class="sxs-lookup"><span data-stu-id="460e3-115">Sign up for a new organization on Office 365</span></span>

1. <span data-ttu-id="460e3-116">Sign up on [Office 365](https://portal.office.com/).</span><span class="sxs-lookup"><span data-stu-id="460e3-116">Sign up on [Office 365](https://portal.office.com/).</span></span>

2. <span data-ttu-id="460e3-117">Follow the wizard to create your organization and your administrator account.</span><span class="sxs-lookup"><span data-stu-id="460e3-117">Follow the wizard to create your organization and your administrator account.</span></span>

3. <span data-ttu-id="460e3-118">Optionally, select the number of users that you plan to provide access for.</span><span class="sxs-lookup"><span data-stu-id="460e3-118">Optionally, select the number of users that you plan to provide access for.</span></span>

4. <span data-ttu-id="460e3-119">Optionally, select add-ins to enhance your post quota.</span><span class="sxs-lookup"><span data-stu-id="460e3-119">Optionally, select add-ins to enhance your post quota.</span></span>

5. <span data-ttu-id="460e3-120">Complete the purchase process to start provisioning [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span><span class="sxs-lookup"><span data-stu-id="460e3-120">Complete the purchase process to start provisioning [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span></span>

<span data-ttu-id="460e3-121">It takes a few minutes to complete the provisioning process before you can start using [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span><span class="sxs-lookup"><span data-stu-id="460e3-121">It takes a few minutes to complete the provisioning process before you can start using [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span></span> <span data-ttu-id="460e3-122">You'll receive an email with the details to access your [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] instance when it's set up.</span><span class="sxs-lookup"><span data-stu-id="460e3-122">You'll receive an email with the details to access your [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] instance when it's set up.</span></span> <span data-ttu-id="460e3-123">You are now ready to [sign in](sign-in.md) and [set up](administer-microsoft-social-engagement.md) [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span><span class="sxs-lookup"><span data-stu-id="460e3-123">You are now ready to [sign in](sign-in.md) and [set up](administer-microsoft-social-engagement.md) [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span></span>

## <a name="assign-a-license-to-a-user"></a><span data-ttu-id="460e3-124">Assign a license to a user</span><span class="sxs-lookup"><span data-stu-id="460e3-124">Assign a license to a user</span></span>

<span data-ttu-id="460e3-125">Enable users to work with [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] by assigning [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] licenses to them.</span><span class="sxs-lookup"><span data-stu-id="460e3-125">Enable users to work with [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] by assigning [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] licenses to them.</span></span> <span data-ttu-id="460e3-126">As an administrator you can always [modify the user's permissions](assign-user-roles.md) to use certain features.</span><span class="sxs-lookup"><span data-stu-id="460e3-126">As an administrator you can always [modify the user's permissions](assign-user-roles.md) to use certain features.</span></span>  

1. <span data-ttu-id="460e3-127">In the [Office 365 admin center](https://portal.office.com/), select **Users** > **Active Users**, and then select the user.</span><span class="sxs-lookup"><span data-stu-id="460e3-127">In the [Office 365 admin center](https://portal.office.com/), select **Users** > **Active Users**, and then select the user.</span></span>

2. <span data-ttu-id="460e3-128">In the **Product licenses** tab, select **Edit**.</span><span class="sxs-lookup"><span data-stu-id="460e3-128">In the **Product licenses** tab, select **Edit**.</span></span>

3. <span data-ttu-id="460e3-129">Set the toggle for **Dynamics 365 for Customer Engagement Plan** or **[!INCLUDE[pn_netbreeze_long](../includes/pn-social-engagement-long.md)]** to **On**.</span><span class="sxs-lookup"><span data-stu-id="460e3-129">Set the toggle for **Dynamics 365 for Customer Engagement Plan** or **[!INCLUDE[pn_netbreeze_long](../includes/pn-social-engagement-long.md)]** to **On**.</span></span>

4. <span data-ttu-id="460e3-130">Select **Save** to confirm your change and update the user's product licenses.</span><span class="sxs-lookup"><span data-stu-id="460e3-130">Select **Save** to confirm your change and update the user's product licenses.</span></span>  

## <a name="remove-a-license-from-a-user"></a><span data-ttu-id="460e3-131">Remove a license from a user</span><span class="sxs-lookup"><span data-stu-id="460e3-131">Remove a license from a user</span></span>

<span data-ttu-id="460e3-132">When you [create an Office 365 user account](http://go.microsoft.com/fwlink/p/?LinkId=526143), you normally [assign a license](http://go.microsoft.com/fwlink/p/?LinkId=390651) to users so that they can use certain features.</span><span class="sxs-lookup"><span data-stu-id="460e3-132">When you [create an Office 365 user account](http://go.microsoft.com/fwlink/p/?LinkId=526143), you normally [assign a license](http://go.microsoft.com/fwlink/p/?LinkId=390651) to users so that they can use certain features.</span></span> 

<span data-ttu-id="460e3-133">When you [remove the assigned license](http://go.microsoft.com/fwlink/p/?LinkId=526144) from a user in your subscription, the license assigned to that user automatically becomes available for assignment to a different user.</span><span class="sxs-lookup"><span data-stu-id="460e3-133">When you [remove the assigned license](http://go.microsoft.com/fwlink/p/?LinkId=526144) from a user in your subscription, the license assigned to that user automatically becomes available for assignment to a different user.</span></span> <span data-ttu-id="460e3-134">If you want the user to still have access to other applications that you manage through [!INCLUDE[pn_Office_365](../includes/pn-office-365.md)], for example [!INCLUDE[pn_Microsoft_Exchange_Online](../includes/pn-microsoft-exchange-online.md)] or [!INCLUDE[pn_ms_SharePoint_long](../includes/pn-ms-sharepoint-long.md)], don't delete the user.</span><span class="sxs-lookup"><span data-stu-id="460e3-134">If you want the user to still have access to other applications that you manage through [!INCLUDE[pn_Office_365](../includes/pn-office-365.md)], for example [!INCLUDE[pn_Microsoft_Exchange_Online](../includes/pn-microsoft-exchange-online.md)] or [!INCLUDE[pn_ms_SharePoint_long](../includes/pn-ms-sharepoint-long.md)], don't delete the user.</span></span> <span data-ttu-id="460e3-135">Instead, remove the [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] license you've assigned to the user.</span><span class="sxs-lookup"><span data-stu-id="460e3-135">Instead, remove the [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] license you've assigned to the user.</span></span> 

<span data-ttu-id="460e3-136">Removing a user's license  from [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] deletes all related custom settings, alerts, and any owned or shared streams.</span><span class="sxs-lookup"><span data-stu-id="460e3-136">Removing a user's license  from [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] deletes all related custom settings, alerts, and any owned or shared streams.</span></span> <span data-ttu-id="460e3-137">Deleted custom settings can't be restored.</span><span class="sxs-lookup"><span data-stu-id="460e3-137">Deleted custom settings can't be restored.</span></span> <span data-ttu-id="460e3-138">Search topics owned by a removed user will remain.</span><span class="sxs-lookup"><span data-stu-id="460e3-138">Search topics owned by a removed user will remain.</span></span> <span data-ttu-id="460e3-139">It takes up to 30 days to reflect the removal of a license in the list of users in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span><span class="sxs-lookup"><span data-stu-id="460e3-139">It takes up to 30 days to reflect the removal of a license in the list of users in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span></span>

1. <span data-ttu-id="460e3-140">In the [Office 365 admin center](https://portal.office.com/), select **Users** > **Active Users**, and then select the user.</span><span class="sxs-lookup"><span data-stu-id="460e3-140">In the [Office 365 admin center](https://portal.office.com/), select **Users** > **Active Users**, and then select the user.</span></span>

2. <span data-ttu-id="460e3-141">In the **Product licenses** tab, select **Edit**.</span><span class="sxs-lookup"><span data-stu-id="460e3-141">In the **Product licenses** tab, select **Edit**.</span></span>

3. <span data-ttu-id="460e3-142">Set the toggle for **Dynamics 365 for Customer Engagement Plan** or **[!INCLUDE[pn_netbreeze_long](../includes/pn-social-engagement-long.md)]** to **Off**.</span><span class="sxs-lookup"><span data-stu-id="460e3-142">Set the toggle for **Dynamics 365 for Customer Engagement Plan** or **[!INCLUDE[pn_netbreeze_long](../includes/pn-social-engagement-long.md)]** to **Off**.</span></span>

4. <span data-ttu-id="460e3-143">Select **Save** to confirm your change and update the user's product licenses.</span><span class="sxs-lookup"><span data-stu-id="460e3-143">Select **Save** to confirm your change and update the user's product licenses.</span></span>

## <a name="purchase-licenses-or-add-other-office-365-plans"></a><span data-ttu-id="460e3-144">Purchase licenses or add other Office 365 plans</span><span class="sxs-lookup"><span data-stu-id="460e3-144">Purchase licenses or add other Office 365 plans</span></span>

<span data-ttu-id="460e3-145">You can purchase and add licenses and other plans to your subscription any time.</span><span class="sxs-lookup"><span data-stu-id="460e3-145">You can purchase and add licenses and other plans to your subscription any time.</span></span> <span data-ttu-id="460e3-146">You must be a global or billing administrator for your company's account to purchase licenses or add other [!INCLUDE[pn_Office_365](../includes/pn-office-365.md)] plans to your subscription.</span><span class="sxs-lookup"><span data-stu-id="460e3-146">You must be a global or billing administrator for your company's account to purchase licenses or add other [!INCLUDE[pn_Office_365](../includes/pn-office-365.md)] plans to your subscription.</span></span>  
[!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="460e3-147">[Microsoft Dynamics 365 for Customer Engagement pricing and licensing](http://go.microsoft.com/fwlink/p/?LinkID=401462)</span><span class="sxs-lookup"><span data-stu-id="460e3-147">[Microsoft Dynamics 365 for Customer Engagement pricing and licensing](http://go.microsoft.com/fwlink/p/?LinkID=401462)</span></span>

### <a name="purchase-additional-licenses"></a><span data-ttu-id="460e3-148">Purchase additional licenses</span><span class="sxs-lookup"><span data-stu-id="460e3-148">Purchase additional licenses</span></span>

1. <span data-ttu-id="460e3-149">In the [!INCLUDE[pn_office_365_admin_center](../includes/pn-office-365-admin-center.md)], select **Billing** > **Purchase Services**.</span><span class="sxs-lookup"><span data-stu-id="460e3-149">In the [!INCLUDE[pn_office_365_admin_center](../includes/pn-office-365-admin-center.md)], select **Billing** > **Purchase Services**.</span></span>

2. <span data-ttu-id="460e3-150">Select the [!INCLUDE[pn_netbreeze_long](../includes/pn-social-engagement-long.md)] add-in or user licenses you want to purchase, and then select **Change license quantity**.</span><span class="sxs-lookup"><span data-stu-id="460e3-150">Select the [!INCLUDE[pn_netbreeze_long](../includes/pn-social-engagement-long.md)] add-in or user licenses you want to purchase, and then select **Change license quantity**.</span></span> <span data-ttu-id="460e3-151">Customize your order by choosing the number of licenses you'd like to order.</span><span class="sxs-lookup"><span data-stu-id="460e3-151">Customize your order by choosing the number of licenses you'd like to order.</span></span>

3. <span data-ttu-id="460e3-152">Follow the checkout procedure to confirm your purchase.</span><span class="sxs-lookup"><span data-stu-id="460e3-152">Follow the checkout procedure to confirm your purchase.</span></span>

### <a name="privacy-notices"></a><span data-ttu-id="460e3-153">Privacy notices</span><span class="sxs-lookup"><span data-stu-id="460e3-153">Privacy notices</span></span>

[!INCLUDE[cc_privacy_msl_cookies](../includes/cc-privacy-msl-cookies.md)]  

[!INCLUDE[cc_privacy_msl_partners](../includes/cc-privacy-msl-partners.md)]  

[!INCLUDE[cc_privacy_mse_azure_event_hubs](../includes/cc-privacy-mse-azure-event-hubs.md)]  

### <a name="see-also"></a><span data-ttu-id="460e3-154">See also</span><span class="sxs-lookup"><span data-stu-id="460e3-154">See also</span></span>

<span data-ttu-id="460e3-155">[Get started with Social Engagement](get-started.md) </span><span class="sxs-lookup"><span data-stu-id="460e3-155">[Get started with Social Engagement](get-started.md) </span></span>  
<span data-ttu-id="460e3-156">[Assign permissions and user roles](assign-user-roles.md) </span><span class="sxs-lookup"><span data-stu-id="460e3-156">[Assign permissions and user roles](assign-user-roles.md) </span></span>  
<span data-ttu-id="460e3-157">[Integrate Social Engagement with Dynamics 365 for Customer Engagement apps](integrate-social-engagement-dynamics-365.md) </span><span class="sxs-lookup"><span data-stu-id="460e3-157">[Integrate Social Engagement with Dynamics 365 for Customer Engagement apps](integrate-social-engagement-dynamics-365.md) </span></span>  
[<span data-ttu-id="460e3-158">Connect Social Engagement to other domains</span><span class="sxs-lookup"><span data-stu-id="460e3-158">Connect Social Engagement to other domains</span></span>](connect-other-domains.md)
 
