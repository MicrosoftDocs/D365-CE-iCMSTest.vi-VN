---
title: Help improve Unified Service Desk for Dynamics 365 for Customer Engagement apps | MicrosoftDocs
description: Learn how you can make our app better by sending system and application information to Microsoft.
ms.custom:
- dyn365-USD, dyn365-admin
ms.date: 04/24/2018
ms.service: dynamics-365-customerservice
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: 4ca41e5e-d266-4060-8f26-dac57ca2bb29
author: kabala123
ms.author: kabala
manager: shujoshi
tags:
- MigrationHO
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 2712637ca099a9659f9ecc3d1dfe1a31de229b26
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382516"
---
# <a name="improve-unified-service-desk"></a><span data-ttu-id="00e85-103">Improve Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="00e85-103">Improve Unified Service Desk</span></span>
<span data-ttu-id="00e85-104">Improvement program data lets [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] send  application-specific information like product usage, health, and performance data to [!INCLUDE[cc_Microsoft](../../includes/cc-microsoft.md)].</span><span class="sxs-lookup"><span data-stu-id="00e85-104">Improvement program data lets [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] send  application-specific information like product usage, health, and performance data to [!INCLUDE[cc_Microsoft](../../includes/cc-microsoft.md)].</span></span> <span data-ttu-id="00e85-105">We use the information that we collect from the program to analyze and improve the service and product experience for our customers.</span><span class="sxs-lookup"><span data-stu-id="00e85-105">We use the information that we collect from the program to analyze and improve the service and product experience for our customers.</span></span>
  
 <span data-ttu-id="00e85-106">The kinds of information that [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] sends anonymously includes:</span><span class="sxs-lookup"><span data-stu-id="00e85-106">The kinds of information that [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] sends anonymously includes:</span></span>  
  
- <span data-ttu-id="00e85-107">Operating system version and bit type.</span><span class="sxs-lookup"><span data-stu-id="00e85-107">Operating system version and bit type.</span></span>  
  
- <span data-ttu-id="00e85-108">Web browser application and version.</span><span class="sxs-lookup"><span data-stu-id="00e85-108">Web browser application and version.</span></span>  
  
- [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="00e85-109">version.</span><span class="sxs-lookup"><span data-stu-id="00e85-109">version.</span></span>  
  
- <span data-ttu-id="00e85-110">Number of monitors used and screen resolution of the primary monitor.</span><span class="sxs-lookup"><span data-stu-id="00e85-110">Number of monitors used and screen resolution of the primary monitor.</span></span>  
  
- <span data-ttu-id="00e85-111">Device processor class and random-access memory (RAM) details.</span><span class="sxs-lookup"><span data-stu-id="00e85-111">Device processor class and random-access memory (RAM) details.</span></span>

- [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="00e85-112">application-specific information.</span><span class="sxs-lookup"><span data-stu-id="00e85-112">application-specific information.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="00e85-113">[Telemetry data](../admin/comply-unified-service-desk-data-gdpr.md#telemetry-data)</span><span class="sxs-lookup"><span data-stu-id="00e85-113">[Telemetry data](../admin/comply-unified-service-desk-data-gdpr.md#telemetry-data)</span></span>

## <a name="help-improve-unified-service-desk-enabled-by-default"></a><span data-ttu-id="00e85-114">Help Improve Unified Service Desk enabled by default</span><span class="sxs-lookup"><span data-stu-id="00e85-114">Help Improve Unified Service Desk enabled by default</span></span>

<span data-ttu-id="00e85-115">With the release of [!INCLUDE[pn-unified-service-desk-3-3](../../includes/pn-unified-service-desk-3-3.md)], by default, the Help Improve [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] feature is enabled for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] instance and [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] sends information to [!INCLUDE[cc_Microsoft](../../includes/cc-microsoft.md)].</span><span class="sxs-lookup"><span data-stu-id="00e85-115">With the release of [!INCLUDE[pn-unified-service-desk-3-3](../../includes/pn-unified-service-desk-3-3.md)], by default, the Help Improve [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] feature is enabled for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] instance and [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] sends information to [!INCLUDE[cc_Microsoft](../../includes/cc-microsoft.md)].</span></span>

> [!Note]
> <span data-ttu-id="00e85-116">If you are using [!INCLUDE[pn-unified-service-desk-3-2](../../includes/pn-unified-service-desk-3-2.md)] and lower with [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] instance, you must enable the Help improve [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] by configuring the **HelpImproveUSD** global option and setting the option to **True**.</span><span class="sxs-lookup"><span data-stu-id="00e85-116">If you are using [!INCLUDE[pn-unified-service-desk-3-2](../../includes/pn-unified-service-desk-3-2.md)] and lower with [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] instance, you must enable the Help improve [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] by configuring the **HelpImproveUSD** global option and setting the option to **True**.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="00e85-117">[Enable sending improvement program information to Microsoft anonymously](#enable-sending-improvement-program-information-to-microsoft-anonymously)</span><span class="sxs-lookup"><span data-stu-id="00e85-117">[Enable sending improvement program information to Microsoft anonymously](#enable-sending-improvement-program-information-to-microsoft-anonymously)</span></span>

<span data-ttu-id="00e85-118">During new installation or upgrade scenario, the information about the transmitting the product usage and performance information to [!INCLUDE[cc_Microsoft](../../includes/cc-microsoft.md)] appears as shown in the below image.</span><span class="sxs-lookup"><span data-stu-id="00e85-118">During new installation or upgrade scenario, the information about the transmitting the product usage and performance information to [!INCLUDE[cc_Microsoft](../../includes/cc-microsoft.md)] appears as shown in the below image.</span></span> <span data-ttu-id="00e85-119">This informaiton helps us to improve the product experience.</span><span class="sxs-lookup"><span data-stu-id="00e85-119">This informaiton helps us to improve the product experience.</span></span>

<span data-ttu-id="00e85-120">![Transmitting usage and performance information](../media/helpimprove-usd-install.PNG "Transmitting usage and performance information")</span><span class="sxs-lookup"><span data-stu-id="00e85-120">![Transmitting usage and performance information](../media/helpimprove-usd-install.PNG "Transmitting usage and performance information")</span></span>

<span data-ttu-id="00e85-121">![Transmitting usage and performance information](../media/helpimprove-usd-upgrade.PNG "Transmitting usage and performance information")</span><span class="sxs-lookup"><span data-stu-id="00e85-121">![Transmitting usage and performance information](../media/helpimprove-usd-upgrade.PNG "Transmitting usage and performance information")</span></span>

<span data-ttu-id="00e85-122">Configuring and setting the value of the Global Option: `HelpImproveUSD` to `FALSE` disables data collection and [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] does not send information to [!INCLUDE[cc_Microsoft](../../includes/cc-microsoft.md)].</span><span class="sxs-lookup"><span data-stu-id="00e85-122">Configuring and setting the value of the Global Option: `HelpImproveUSD` to `FALSE` disables data collection and [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] does not send information to [!INCLUDE[cc_Microsoft](../../includes/cc-microsoft.md)].</span></span>

> [!Note]
>  <span data-ttu-id="00e85-123">The checkbox in the Help Improve [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] section on **About** page reflects whether or not [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] sends data to [!INCLUDE[cc_Microsoft](../../includes/cc-microsoft.md)], and agent cannot select or clear the checkbox.</span><span class="sxs-lookup"><span data-stu-id="00e85-123">The checkbox in the Help Improve [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] section on **About** page reflects whether or not [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] sends data to [!INCLUDE[cc_Microsoft](../../includes/cc-microsoft.md)], and agent cannot select or clear the checkbox.</span></span> <span data-ttu-id="00e85-124">However, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] Administrators can control whether or not send data to [!INCLUDE[cc_Microsoft](../../includes/cc-microsoft.md)].</span><span class="sxs-lookup"><span data-stu-id="00e85-124">However, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] Administrators can control whether or not send data to [!INCLUDE[cc_Microsoft](../../includes/cc-microsoft.md)].</span></span>

<a name="Disable_ImproveUSD"></a>   
## <a name="disable-sending-improvement-program-information-to-includeccmicrosoftincludescc-microsoftmd-anonymously"></a><span data-ttu-id="00e85-125">Disable sending improvement program information to [!INCLUDE[cc_Microsoft](../../includes/cc-microsoft.md)] anonymously</span><span class="sxs-lookup"><span data-stu-id="00e85-125">Disable sending improvement program information to [!INCLUDE[cc_Microsoft](../../includes/cc-microsoft.md)] anonymously</span></span>
  
1. <span data-ttu-id="00e85-126">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps as a user with the System Administrator or [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] Administrator security role.</span><span class="sxs-lookup"><span data-stu-id="00e85-126">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps as a user with the System Administrator or [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] Administrator security role.</span></span>  
  
2. <span data-ttu-id="00e85-127">Go to **Settings** > **Unified Service Desk.**</span><span class="sxs-lookup"><span data-stu-id="00e85-127">Go to **Settings** > **Unified Service Desk.**</span></span>
  
3. <span data-ttu-id="00e85-128">Bấm vào **Tùy chọn**.</span><span class="sxs-lookup"><span data-stu-id="00e85-128">Click **Options**.</span></span>  
  
4. <span data-ttu-id="00e85-129">On the Active UII Options page, click **New**.</span><span class="sxs-lookup"><span data-stu-id="00e85-129">On the Active UII Options page, click **New**.</span></span>  
  
5. <span data-ttu-id="00e85-130">On the New Option page, select **HelpImproveUSD** in the **Global Options** list.</span><span class="sxs-lookup"><span data-stu-id="00e85-130">On the New Option page, select **HelpImproveUSD** in the **Global Options** list.</span></span>  
  
6. <span data-ttu-id="00e85-131">In the Value box, type `FALSE`.</span><span class="sxs-lookup"><span data-stu-id="00e85-131">In the Value box, type `FALSE`.</span></span>
  
7. <span data-ttu-id="00e85-132">Click **SAVE & CLOSE**.</span><span class="sxs-lookup"><span data-stu-id="00e85-132">Click **SAVE & CLOSE**.</span></span>
  
<a name="Enable_ImproveUSD"></a>   
## <a name="enable-sending-improvement-program-information-to-microsoft-anonymously"></a><span data-ttu-id="00e85-133">Enable sending improvement program information to Microsoft anonymously</span><span class="sxs-lookup"><span data-stu-id="00e85-133">Enable sending improvement program information to Microsoft anonymously</span></span>  

1. <span data-ttu-id="00e85-134">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps as a user with the System Administrator or [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] Administrator security role.</span><span class="sxs-lookup"><span data-stu-id="00e85-134">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps as a user with the System Administrator or [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] Administrator security role.</span></span>  
  
2. <span data-ttu-id="00e85-135">Chuyển tới **Thiết đặt** > **Unified Service Desk**.</span><span class="sxs-lookup"><span data-stu-id="00e85-135">Go to **Settings** > **Unified Service Desk**.</span></span>
  
3. <span data-ttu-id="00e85-136">Bấm vào **Tùy chọn**.</span><span class="sxs-lookup"><span data-stu-id="00e85-136">Click **Options**.</span></span>
  
4. <span data-ttu-id="00e85-137">On the Active UII Options page,  select **HelpImproveUSD** from the **Global Options** list.</span><span class="sxs-lookup"><span data-stu-id="00e85-137">On the Active UII Options page,  select **HelpImproveUSD** from the **Global Options** list.</span></span>
  
5. <span data-ttu-id="00e85-138">In the Value box, type `TRUE`.</span><span class="sxs-lookup"><span data-stu-id="00e85-138">In the Value box, type `TRUE`.</span></span>
  
6. <span data-ttu-id="00e85-139">Click **SAVE & CLOSE**.</span><span class="sxs-lookup"><span data-stu-id="00e85-139">Click **SAVE & CLOSE**.</span></span>

> [!NOTE]
> <span data-ttu-id="00e85-140">Alternatively, you can enable the global option for sending improvement program information to [!INCLUDE[cc_Microsoft](../../includes/cc-microsoft.md)] by performing the following.</span><span class="sxs-lookup"><span data-stu-id="00e85-140">Alternatively, you can enable the global option for sending improvement program information to [!INCLUDE[cc_Microsoft](../../includes/cc-microsoft.md)] by performing the following.</span></span>
> 1. <span data-ttu-id="00e85-141">Go to **Settings** > **[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]** > **Options**.</span><span class="sxs-lookup"><span data-stu-id="00e85-141">Go to **Settings** > **[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]** > **Options**.</span></span>
> 2. <span data-ttu-id="00e85-142">Select **HelpImproveUSD** checkbox.</span><span class="sxs-lookup"><span data-stu-id="00e85-142">Select **HelpImproveUSD** checkbox.</span></span>
> 3. <span data-ttu-id="00e85-143">Click **Deactivate** in the toolbar.</span><span class="sxs-lookup"><span data-stu-id="00e85-143">Click **Deactivate** in the toolbar.</span></span>
> 
> [!Note]
> <span data-ttu-id="00e85-144">If you delete the **HelpImproveUSD** global option from the UII options page, the data collection is enabled and [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] sends information to [!INCLUDE[cc_Microsoft](../../includes/cc-microsoft.md)]</span><span class="sxs-lookup"><span data-stu-id="00e85-144">If you delete the **HelpImproveUSD** global option from the UII options page, the data collection is enabled and [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] sends information to [!INCLUDE[cc_Microsoft](../../includes/cc-microsoft.md)]</span></span>
  
## <a name="privacy-notice"></a><span data-ttu-id="00e85-145">Thông báo bảo mật</span><span class="sxs-lookup"><span data-stu-id="00e85-145">Privacy notice</span></span>  
[!INCLUDE[cc_privacy_usd_telemetry](../../includes/cc-privacy-usd-telemetry.md)]
  
## <a name="see-also"></a><span data-ttu-id="00e85-146">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="00e85-146">See also</span></span>
[<span data-ttu-id="00e85-147">Manage Options for Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="00e85-147">Manage Options for Unified Service Desk</span></span>](../../unified-service-desk/admin/manage-options-unified-service-desk.md)

[<span data-ttu-id="00e85-148">Provide feedback about Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="00e85-148">Provide feedback about Unified Service Desk</span></span>](../admin/provide-feedback.md)
