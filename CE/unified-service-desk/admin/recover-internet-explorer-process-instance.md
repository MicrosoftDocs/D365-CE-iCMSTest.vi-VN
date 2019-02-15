---
title: Recovering an Internet Explorer process instance in Unified Service Desk | MicrosoftDocs
description: Learn about recovering an Internet Explorer process instance
ms.custom:
- dyn365-USD, dyn365-admin
ms.date: 02/06/2018
ms.reviewer: ''
ms.service: dynamics-365-customerservice
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: 1AEA6B45-3646-400D-B0C1-08B503897E8D
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
ms.openlocfilehash: be432adb231373e001db09f110e528c186f00d82
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382528"
---
# <a name="recover-an-internet-explorer-process-instance"></a><span data-ttu-id="8bd5a-103">Recover an Internet Explorer process instance</span><span class="sxs-lookup"><span data-stu-id="8bd5a-103">Recover an Internet Explorer process instance</span></span>
<span data-ttu-id="8bd5a-104">Starting with [!INCLUDE[pn-unified-service-desk-3-2](../../includes/pn-unified-service-desk-3-2.md)], [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] can help agents to recover the terminated (crashed) webpages hosted in Internet Explorer process in [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="8bd5a-104">Starting with [!INCLUDE[pn-unified-service-desk-3-2](../../includes/pn-unified-service-desk-3-2.md)], [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] can help agents to recover the terminated (crashed) webpages hosted in Internet Explorer process in [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span></span>

<span data-ttu-id="8bd5a-105">By default, Internet Explorer process instance recovery is enabled.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-105">By default, Internet Explorer process instance recovery is enabled.</span></span> <span data-ttu-id="8bd5a-106">To disable the feature, a system administrator must configure the `IEWebPageRecovery` option on the **Active UII Options** page, and set it to **false**.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-106">To disable the feature, a system administrator must configure the `IEWebPageRecovery` option on the **Active UII Options** page, and set it to **false**.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="8bd5a-107">[Manage a Unified Service Desk option](../admin/manage-options-unified-service-desk.md)</span><span class="sxs-lookup"><span data-stu-id="8bd5a-107">[Manage a Unified Service Desk option](../admin/manage-options-unified-service-desk.md)</span></span>

### <a name="disable-iewebpagerecovery-option"></a><span data-ttu-id="8bd5a-108">Disable IEWebPageRecovery option</span><span class="sxs-lookup"><span data-stu-id="8bd5a-108">Disable IEWebPageRecovery option</span></span>

1. <span data-ttu-id="8bd5a-109">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-109">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span></span>

2. [!INCLUDE[proc_settings_usd](../../includes/proc-settings-usd.md)]

3. <span data-ttu-id="8bd5a-110">Chọn **Tùy chọn**.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-110">Choose **Options**.</span></span>  

4. <span data-ttu-id="8bd5a-111">click **New** on the **Active UII Options** page.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-111">click **New** on the **Active UII Options** page.</span></span>

5. <span data-ttu-id="8bd5a-112">Choose **Others** for the **Global Option** field.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-112">Choose **Others** for the **Global Option** field.</span></span>

6. <span data-ttu-id="8bd5a-113">Type **IEWebPageRecovery** for the **Name** field.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-113">Type **IEWebPageRecovery** for the **Name** field.</span></span>

7. <span data-ttu-id="8bd5a-114">Type **false** for the **Value** field.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-114">Type **false** for the **Value** field.</span></span>

8. <span data-ttu-id="8bd5a-115">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-115">Click **Save**.</span></span>

<a name="BKMK_When_Unified_Service_Desk_can_help_recover_the_Internet_Explorer_process_instances"></a>
## <a name="when-includepnunifiedservicedeskincludespn-unified-service-deskmd-can-help-recover-internet-explorer-process-instances"></a><span data-ttu-id="8bd5a-116">When [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] can help recover Internet Explorer process instances</span><span class="sxs-lookup"><span data-stu-id="8bd5a-116">When [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] can help recover Internet Explorer process instances</span></span>

[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="8bd5a-117">can help agents to recover an Internet Explorer process instance in the following scenarios:</span><span class="sxs-lookup"><span data-stu-id="8bd5a-117">can help agents to recover an Internet Explorer process instance in the following scenarios:</span></span>

- <span data-ttu-id="8bd5a-118">When Internet Explorer closes abruptly.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-118">When Internet Explorer closes abruptly.</span></span>
- <span data-ttu-id="8bd5a-119">When you manually end an unresponsive Internet Explorer process instance from Task Manager.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-119">When you manually end an unresponsive Internet Explorer process instance from Task Manager.</span></span>
- <span data-ttu-id="8bd5a-120">When a script on the hosted control that uses `IE process` browser control takes time more than the timeout period ([IEWebPageInactivityTimeOut](#change-iewebpageinactivitytimeout-option)) for page navigation.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-120">When a script on the hosted control that uses `IE process` browser control takes time more than the timeout period ([IEWebPageInactivityTimeOut](#change-iewebpageinactivitytimeout-option)) for page navigation.</span></span>

<a name="BKMK_recover_unresponsive_Internet_Explorer_process_instance"></a>
## <a name="recover-an-unresponsive-internet-explorer-process-instance"></a><span data-ttu-id="8bd5a-121">Recover an unresponsive Internet Explorer process instance</span><span class="sxs-lookup"><span data-stu-id="8bd5a-121">Recover an unresponsive Internet Explorer process instance</span></span>

<span data-ttu-id="8bd5a-122">When a hosted control that uses an Internet Explorer process browser control closes abruptly, the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application displays the message **Internet Explorer closed abruptly**.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-122">When a hosted control that uses an Internet Explorer process browser control closes abruptly, the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application displays the message **Internet Explorer closed abruptly**.</span></span>

<span data-ttu-id="8bd5a-123">![Internet Explorer closed abruptly](../../unified-service-desk/media/usd-ie-closed-abruptly-33update.PNG "Internet Explorer closed abruptly")</span><span class="sxs-lookup"><span data-stu-id="8bd5a-123">![Internet Explorer closed abruptly](../../unified-service-desk/media/usd-ie-closed-abruptly-33update.PNG "Internet Explorer closed abruptly")</span></span>

<span data-ttu-id="8bd5a-124">To recover the closed instance (which may contain more than one webpage), select **Reload**.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-124">To recover the closed instance (which may contain more than one webpage), select **Reload**.</span></span> <span data-ttu-id="8bd5a-125">After you select **Reload**, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] reloads the webpage to the last known URL.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-125">After you select **Reload**, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] reloads the webpage to the last known URL.</span></span> <span data-ttu-id="8bd5a-126">That is, when you open an **Account** Internet Explorer webpage and navigate inline to a **Case** Internet Explorer webpage.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-126">That is, when you open an **Account** Internet Explorer webpage and navigate inline to a **Case** Internet Explorer webpage.</span></span> <span data-ttu-id="8bd5a-127">If the **Case** webpage becomes unresponsive, the recovery feature reloads only the **Account** webpage.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-127">If the **Case** webpage becomes unresponsive, the recovery feature reloads only the **Account** webpage.</span></span>

<span data-ttu-id="8bd5a-128">If you do not want to recover, select **Cancel**.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-128">If you do not want to recover, select **Cancel**.</span></span> <span data-ttu-id="8bd5a-129">If you cancel, the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application skips recovery of the Internet Explorer process instance and displays a message, **The webpage stopped responding. If you frequently experience unexpected closing of Internet Explorer webpage, contact your system administrator**.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-129">If you cancel, the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application skips recovery of the Internet Explorer process instance and displays a message, **The webpage stopped responding. If you frequently experience unexpected closing of Internet Explorer webpage, contact your system administrator**.</span></span>

<span data-ttu-id="8bd5a-130">![Cancel to skip the recovery of Internet Explorer webpage](../../unified-service-desk/media/usd-ie-closed-abruptly-cancel.PNG "Cancel to skip the recovery of Internet Explorer webpage")</span><span class="sxs-lookup"><span data-stu-id="8bd5a-130">![Cancel to skip the recovery of Internet Explorer webpage](../../unified-service-desk/media/usd-ie-closed-abruptly-cancel.PNG "Cancel to skip the recovery of Internet Explorer webpage")</span></span>

<a name="BKMK_recover_when_using_RunScript_on_a_hosted_control"></a>
## <a name="recover-when-script-executed-on-the-webpage-causes-the-webpage-to-run-slowly"></a><span data-ttu-id="8bd5a-131">Recover when script executed on the webpage causes the webpage to run slowly</span><span class="sxs-lookup"><span data-stu-id="8bd5a-131">Recover when script executed on the webpage causes the webpage to run slowly</span></span>

<span data-ttu-id="8bd5a-132">If a script running on a Internet Explorer causes the Internet Explorer webpage to run slowly, then [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] waits until the timeout period ([IEWebPageInactivityTimeOut](../admin/recover-internet-explorer-process-instance.md#change-iewebpageinactivitytimeout-option)) to display the message - **A script on \<Hosted Control Name> is causing the Internet Explorer webpage to run slowly**.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-132">If a script running on a Internet Explorer causes the Internet Explorer webpage to run slowly, then [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] waits until the timeout period ([IEWebPageInactivityTimeOut](../admin/recover-internet-explorer-process-instance.md#change-iewebpageinactivitytimeout-option)) to display the message - **A script on \<Hosted Control Name> is causing the Internet Explorer webpage to run slowly**.</span></span>

<span data-ttu-id="8bd5a-133">To recover the webpage, select **Reload**.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-133">To recover the webpage, select **Reload**.</span></span> <span data-ttu-id="8bd5a-134">After you select **Reload**, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] reloads the webpage to the last known URL.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-134">After you select **Reload**, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] reloads the webpage to the last known URL.</span></span>

<span data-ttu-id="8bd5a-135">Select **Stop** if you want to terminate and do not want to recover the webpage on which the script is executed.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-135">Select **Stop** if you want to terminate and do not want to recover the webpage on which the script is executed.</span></span> 

<span data-ttu-id="8bd5a-136">If you want to wait for the Internet Explorer webpage to respond, select **Continue**, and wait for the Internet Explorer webpage to respond.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-136">If you want to wait for the Internet Explorer webpage to respond, select **Continue**, and wait for the Internet Explorer webpage to respond.</span></span> <span data-ttu-id="8bd5a-137">If the webpage does not respond, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] displays the window again after the timeout period.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-137">If the webpage does not respond, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] displays the window again after the timeout period.</span></span>

<span data-ttu-id="8bd5a-138">The following list shows the options and descriptions to select when you see the message window.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-138">The following list shows the options and descriptions to select when you see the message window.</span></span> 

| <span data-ttu-id="8bd5a-139">Tùy chọn</span><span class="sxs-lookup"><span data-stu-id="8bd5a-139">Option</span></span>   | <span data-ttu-id="8bd5a-140">Mô tả</span><span class="sxs-lookup"><span data-stu-id="8bd5a-140">Description</span></span>                                                                                                                                                                                                               |
|:---------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bd5a-141">Tải lại</span><span class="sxs-lookup"><span data-stu-id="8bd5a-141">Reload</span></span>   | <span data-ttu-id="8bd5a-142">Recovers the Internet Explorer webpage.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-142">Recovers the Internet Explorer webpage.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="8bd5a-143">Stop</span><span class="sxs-lookup"><span data-stu-id="8bd5a-143">Stop</span></span>     | <span data-ttu-id="8bd5a-144">Terminates and does not to recover the Internet Explorer webpage.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-144">Terminates and does not to recover the Internet Explorer webpage.</span></span>                                                                                                                                                         |
| <span data-ttu-id="8bd5a-145">Tiếp tục</span><span class="sxs-lookup"><span data-stu-id="8bd5a-145">Continue</span></span> | <span data-ttu-id="8bd5a-146">Waits until the Internet Explorer webpage to respond.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-146">Waits until the Internet Explorer webpage to respond.</span></span> <span data-ttu-id="8bd5a-147">If the webpage does not respond, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] displays the window again after the timeout period.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-147">If the webpage does not respond, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] displays the window again after the timeout period.</span></span> |

<span data-ttu-id="8bd5a-148">![Script causing Internet Explorer webpage to run slowly](../../unified-service-desk/media/usd-ie-runscript.PNG "Script causing Internet Explorer webpage to run slowly")</span><span class="sxs-lookup"><span data-stu-id="8bd5a-148">![Script causing Internet Explorer webpage to run slowly](../../unified-service-desk/media/usd-ie-runscript.PNG "Script causing Internet Explorer webpage to run slowly")</span></span>

> [!Note]
> <span data-ttu-id="8bd5a-149">If there are other webpages that are unresponsive, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] displays the message - **Internet Explorer closed abruptly.**</span><span class="sxs-lookup"><span data-stu-id="8bd5a-149">If there are other webpages that are unresponsive, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] displays the message - **Internet Explorer closed abruptly.**</span></span> <br><br>
> <span data-ttu-id="8bd5a-150">Select **Reload** to recover the webpage to the last known URL.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-150">Select **Reload** to recover the webpage to the last known URL.</span></span> <span data-ttu-id="8bd5a-151">Or, select **Cancel** to not to recover the webpage.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-151">Or, select **Cancel** to not to recover the webpage.</span></span></br>
> <span data-ttu-id="8bd5a-152">![Internet Explorer closed abruptly](../../unified-service-desk/media/usd-ie-closed-abruptly-33update.PNG "Internet Explorer closed abruptly")</span><span class="sxs-lookup"><span data-stu-id="8bd5a-152">![Internet Explorer closed abruptly](../../unified-service-desk/media/usd-ie-closed-abruptly-33update.PNG "Internet Explorer closed abruptly")</span></span>

### <a name="change-iewebpageinactivitytimeout-option"></a><span data-ttu-id="8bd5a-153">Change IEWebPageInactivityTimeOut option</span><span class="sxs-lookup"><span data-stu-id="8bd5a-153">Change IEWebPageInactivityTimeOut option</span></span>

<span data-ttu-id="8bd5a-154">**IEWebPageInactivityTimeOut** Indicates the timeout period for the duration (in milliseconds) that the Unified Service Desk waits before displaying a message - **A script on \<Hosted Control Name> is causing the Internet Explorer webpage to run slowly**.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-154">**IEWebPageInactivityTimeOut** Indicates the timeout period for the duration (in milliseconds) that the Unified Service Desk waits before displaying a message - **A script on \<Hosted Control Name> is causing the Internet Explorer webpage to run slowly**.</span></span>

<span data-ttu-id="8bd5a-155">By default, the **IEWebPageInactivityTimeOut** is enabled and timeout period is 15000 milliseconds (15 seconds).</span><span class="sxs-lookup"><span data-stu-id="8bd5a-155">By default, the **IEWebPageInactivityTimeOut** is enabled and timeout period is 15000 milliseconds (15 seconds).</span></span>
<span data-ttu-id="8bd5a-156">To change the default timeout period, a System Administrator must configure the **IEWebPageInactivityTimeOut** on the **Active UII Options** page and type the value in milliseconds.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-156">To change the default timeout period, a System Administrator must configure the **IEWebPageInactivityTimeOut** on the **Active UII Options** page and type the value in milliseconds.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="8bd5a-157">[Manage Options for Unified Service Desk](../../unified-service-desk/admin/manage-options-unified-service-desk.md).</span><span class="sxs-lookup"><span data-stu-id="8bd5a-157">[Manage Options for Unified Service Desk](../../unified-service-desk/admin/manage-options-unified-service-desk.md).</span></span>
<span data-ttu-id="8bd5a-158">If you set the value as 0 milliseconds, then the **IEWebPageInactivityTimeOut** is disabled.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-158">If you set the value as 0 milliseconds, then the **IEWebPageInactivityTimeOut** is disabled.</span></span>

<span data-ttu-id="8bd5a-159">To change the **IEWebPageInactivityTimeOut** timeout value:</span><span class="sxs-lookup"><span data-stu-id="8bd5a-159">To change the **IEWebPageInactivityTimeOut** timeout value:</span></span>

1. <span data-ttu-id="8bd5a-160">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-160">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span></span>

2. [!INCLUDE[proc_settings_usd](../../includes/proc-settings-usd.md)]

3. <span data-ttu-id="8bd5a-161">Chọn **Tùy chọn**.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-161">Choose **Options**.</span></span>  

4. <span data-ttu-id="8bd5a-162">click **New** on the **Active UII Options** page.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-162">click **New** on the **Active UII Options** page.</span></span>

5. <span data-ttu-id="8bd5a-163">Choose **Others** for the **Global Option** field.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-163">Choose **Others** for the **Global Option** field.</span></span>

6. <span data-ttu-id="8bd5a-164">Type **IEWebPageInactivityTimeOut** for the **Name** field.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-164">Type **IEWebPageInactivityTimeOut** for the **Name** field.</span></span>

7. <span data-ttu-id="8bd5a-165">Type the value in milliseconds for the **Value** field.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-165">Type the value in milliseconds for the **Value** field.</span></span>

8. <span data-ttu-id="8bd5a-166">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-166">Click **Save**.</span></span>

<a name="Terminate_recover_unresponsive_Internet_Explorer_process_instance using_keyboard_shortcut"></a>
## <a name="terminate-and-recover-unresponsive-internet-explorer-process-instances-using-a-keyboard-shortcut"></a><span data-ttu-id="8bd5a-167">Terminate and recover unresponsive Internet Explorer process instances using a keyboard shortcut</span><span class="sxs-lookup"><span data-stu-id="8bd5a-167">Terminate and recover unresponsive Internet Explorer process instances using a keyboard shortcut</span></span>

<span data-ttu-id="8bd5a-168">When the Internet Explorer webpage is unresponsive and causes the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] to freeze, hover the cursor on the unresponsive tab and use the keyboard shortcut **Ctrl+Alt+K** to terminate.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-168">When the Internet Explorer webpage is unresponsive and causes the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] to freeze, hover the cursor on the unresponsive tab and use the keyboard shortcut **Ctrl+Alt+K** to terminate.</span></span> 

<span data-ttu-id="8bd5a-169">The [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] displays a dialog box: **You have chosen to end the Internet Explorer process that is active in Unified Service Desk by pressing Ctrl+Alt+K. Do you want to continue?**.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-169">The [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] displays a dialog box: **You have chosen to end the Internet Explorer process that is active in Unified Service Desk by pressing Ctrl+Alt+K. Do you want to continue?**.</span></span> 

<span data-ttu-id="8bd5a-170">![Keyboard shortcut to terminate and not to recover Internet Explorer webpage](../../unified-service-desk/media/usd-ie-terminate-shortcutkey.PNG "Keyboard shortcut to terminate and not to recover Internet Explorer webpage")</span><span class="sxs-lookup"><span data-stu-id="8bd5a-170">![Keyboard shortcut to terminate and not to recover Internet Explorer webpage](../../unified-service-desk/media/usd-ie-terminate-shortcutkey.PNG "Keyboard shortcut to terminate and not to recover Internet Explorer webpage")</span></span>

<span data-ttu-id="8bd5a-171">Select **Yes** to terminate the Internet Explorer process instance.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-171">Select **Yes** to terminate the Internet Explorer process instance.</span></span> <span data-ttu-id="8bd5a-172">Select **No** to cancel the operation.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-172">Select **No** to cancel the operation.</span></span>

<span data-ttu-id="8bd5a-173">After you end the Internet Explorer process instance, the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application displays a message, **Internet Explorer closed abruptly**.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-173">After you end the Internet Explorer process instance, the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application displays a message, **Internet Explorer closed abruptly**.</span></span> <span data-ttu-id="8bd5a-174">Select **Reload** to recover the closed Internet Explorer process instance.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-174">Select **Reload** to recover the closed Internet Explorer process instance.</span></span> <span data-ttu-id="8bd5a-175">If you do not want to recover, select **Cancel**.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-175">If you do not want to recover, select **Cancel**.</span></span>

<span data-ttu-id="8bd5a-176">![Internet Explorer closed abruptly](../../unified-service-desk/media/usd-ie-closed-abruptly-33update.PNG "Internet Explorer closed abruptly")</span><span class="sxs-lookup"><span data-stu-id="8bd5a-176">![Internet Explorer closed abruptly](../../unified-service-desk/media/usd-ie-closed-abruptly-33update.PNG "Internet Explorer closed abruptly")</span></span>

> [!Note]
> - <span data-ttu-id="8bd5a-177">An agent must wait for the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] monitoring process (usdmp.exe) to detect and terminate the unresponsive Internet Explorer process instance.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-177">An agent must wait for the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] monitoring process (usdmp.exe) to detect and terminate the unresponsive Internet Explorer process instance.</span></span></br>
> - <span data-ttu-id="8bd5a-178">The agent must use the keyboard shortcut as last option when the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] monitoring process fails to detect the unresponsive Internet Explorer process instance.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-178">The agent must use the keyboard shortcut as last option when the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] monitoring process fails to detect the unresponsive Internet Explorer process instance.</span></span></br>
> - <span data-ttu-id="8bd5a-179">Using the keyboard shortcut may terminate any Internet Explorer webpage, causing you to lose any unsaved work.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-179">Using the keyboard shortcut may terminate any Internet Explorer webpage, causing you to lose any unsaved work.</span></span>

### <a name="change-keyboard-shortcut"></a><span data-ttu-id="8bd5a-180">Change keyboard shortcut</span><span class="sxs-lookup"><span data-stu-id="8bd5a-180">Change keyboard shortcut</span></span>

<span data-ttu-id="8bd5a-181">To change the keyboard shortcut:</span><span class="sxs-lookup"><span data-stu-id="8bd5a-181">To change the keyboard shortcut:</span></span>

1. <span data-ttu-id="8bd5a-182">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-182">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span></span>

2. [!INCLUDE[proc_settings_usd](../../includes/proc-settings-usd.md)]

3. <span data-ttu-id="8bd5a-183">Chọn **Tùy chọn**.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-183">Choose **Options**.</span></span>  

4. <span data-ttu-id="8bd5a-184">click **New** on the **Active UII Options** page.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-184">click **New** on the **Active UII Options** page.</span></span>

5. <span data-ttu-id="8bd5a-185">Choose **Others** for the **Global Option** field.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-185">Choose **Others** for the **Global Option** field.</span></span>

6. <span data-ttu-id="8bd5a-186">Type **On-DemandIETerminationShortcut** for the **Name** field.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-186">Type **On-DemandIETerminationShortcut** for the **Name** field.</span></span>

7. <span data-ttu-id="8bd5a-187">Type the keyboard shortcut in the format _key1+key2+key3_ for the **Value** field.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-187">Type the keyboard shortcut in the format _key1+key2+key3_ for the **Value** field.</span></span>

8. <span data-ttu-id="8bd5a-188">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-188">Click **Save**.</span></span>

<span data-ttu-id="8bd5a-189">![Change On-DemandIETerminationShortcut](../../unified-service-desk/media/crm-usd-options-on-demand-ie-termination-shortcut.PNG "Change On-DemandIETerminationShortcut")</span><span class="sxs-lookup"><span data-stu-id="8bd5a-189">![Change On-DemandIETerminationShortcut](../../unified-service-desk/media/crm-usd-options-on-demand-ie-termination-shortcut.PNG "Change On-DemandIETerminationShortcut")</span></span>

<a name="BKMK_Limitations"></a>
## <a name="limitations"></a><span data-ttu-id="8bd5a-190">Giới hạn</span><span class="sxs-lookup"><span data-stu-id="8bd5a-190">Limitations</span></span> 

- <span data-ttu-id="8bd5a-191">When you recover an Internet Explorer webpage, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] triggers again all the events that associate with the webpage.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-191">When you recover an Internet Explorer webpage, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] triggers again all the events that associate with the webpage.</span></span> </br>
  <span data-ttu-id="8bd5a-192">Ví dụ:</span><span class="sxs-lookup"><span data-stu-id="8bd5a-192">For example:</span></span> </br> <span data-ttu-id="8bd5a-193">**TaskUpdated** is a event configured for the **Agent Scripting** hosted control (webpage) and has **Action Call for Reminder** and **Action Call for Resolve Case** as Action Calls.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-193">**TaskUpdated** is a event configured for the **Agent Scripting** hosted control (webpage) and has **Action Call for Reminder** and **Action Call for Resolve Case** as Action Calls.</span></span> <span data-ttu-id="8bd5a-194">If you recover **Agent Scripting** webpage, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] triggers again the **TaskUpdated** event and the **Action Calls**.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-194">If you recover **Agent Scripting** webpage, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] triggers again the **TaskUpdated** event and the **Action Calls**.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="8bd5a-195">[Events](../events.md)</span><span class="sxs-lookup"><span data-stu-id="8bd5a-195">[Events](../events.md)</span></span>

- [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="8bd5a-196">does not recover inline navigation of an Internet Explorer webpage.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-196">does not recover inline navigation of an Internet Explorer webpage.</span></span></br>
  <span data-ttu-id="8bd5a-197">Ví dụ:</span><span class="sxs-lookup"><span data-stu-id="8bd5a-197">For example:</span></span> </br>
  <span data-ttu-id="8bd5a-198">You open an **Account** Internet Explorer webpage and navigate inline to a **Case** Internet Explorer webpage.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-198">You open an **Account** Internet Explorer webpage and navigate inline to a **Case** Internet Explorer webpage.</span></span> <span data-ttu-id="8bd5a-199">If the **Case** webpage becomes unresponsive, the recovery feature reloads only the **Account** webpage and not the **Case** webpage.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-199">If the **Case** webpage becomes unresponsive, the recovery feature reloads only the **Account** webpage and not the **Case** webpage.</span></span>

- [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="8bd5a-200">does not recover unsaved work.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-200">does not recover unsaved work.</span></span> </br>
  <span data-ttu-id="8bd5a-201">Ví dụ:</span><span class="sxs-lookup"><span data-stu-id="8bd5a-201">For example:</span></span> </br>
  <span data-ttu-id="8bd5a-202">You open an **Account** Internet Explorer webpage and navigate inline to a **Case** Internet Explorer webpage, and enter details on the **case** webpage.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-202">You open an **Account** Internet Explorer webpage and navigate inline to a **Case** Internet Explorer webpage, and enter details on the **case** webpage.</span></span> <span data-ttu-id="8bd5a-203">If the **Case** webpage becomes unresponsive, the recovery feature reloads only the **Account** webpage and not the **Case** webpage.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-203">If the **Case** webpage becomes unresponsive, the recovery feature reloads only the **Account** webpage and not the **Case** webpage.</span></span> <span data-ttu-id="8bd5a-204">You may lose any unsaved data that you had entered in the **Case** webpage.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-204">You may lose any unsaved data that you had entered in the **Case** webpage.</span></span>

- <span data-ttu-id="8bd5a-205">If the web browser runs slowly while executing a script, and you choose **Stop** to terminate and not to recover the Internet Explorer webpage, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] may terminate other Internet Explorer webpages.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-205">If the web browser runs slowly while executing a script, and you choose **Stop** to terminate and not to recover the Internet Explorer webpage, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] may terminate other Internet Explorer webpages.</span></span>

- <span data-ttu-id="8bd5a-206">Using **Ctrl+Alt+K** keyboard shortcut may terminate other Internet Explorer webpage, causing you to lose any unsaved work.</span><span class="sxs-lookup"><span data-stu-id="8bd5a-206">Using **Ctrl+Alt+K** keyboard shortcut may terminate other Internet Explorer webpage, causing you to lose any unsaved work.</span></span>

## <a name="see-also"></a><span data-ttu-id="8bd5a-207">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="8bd5a-207">See also</span></span>

[<span data-ttu-id="8bd5a-208">Manage Options for Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="8bd5a-208">Manage Options for Unified Service Desk</span></span>](../../unified-service-desk/admin/manage-options-unified-service-desk.md)
