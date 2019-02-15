---
title: Session Timer (Custom Hosted Control) in Unified Service Desk for Dynamics 365 for Customer Engagement apps | MicrosoftDocs
description: Learn about Session Timer type of hosted control in Unified Service Desk.
ms.custom:
- dyn365-USD
ms.date: 08/23/2017
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
ms.assetid: 044cd615-691e-454d-9877-31095940b226
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: c8c8e99b7894196bae0a318ec501b806bfc74d37
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388752"
---
# <a name="session-timer-custom-hosted-control"></a><span data-ttu-id="7ce96-103">Session Timer (Custom Hosted Control)</span><span class="sxs-lookup"><span data-stu-id="7ce96-103">Session Timer (Custom Hosted Control)</span></span>
<span data-ttu-id="7ce96-104">In [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], the session timer (`Timer`) hosted control displays the elapsed time in seconds since a session was started, and uses different colors to specify the threshold time limits.</span><span class="sxs-lookup"><span data-stu-id="7ce96-104">In [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], the session timer (`Timer`) hosted control displays the elapsed time in seconds since a session was started, and uses different colors to specify the threshold time limits.</span></span>  
  
 <span data-ttu-id="7ce96-105">The `Timer` hosted control isn’t one of the predefined hosted controls; it’s a custom control that is available when you deploy one of the sample [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] applications on your [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps instance.</span><span class="sxs-lookup"><span data-stu-id="7ce96-105">The `Timer` hosted control isn’t one of the predefined hosted controls; it’s a custom control that is available when you deploy one of the sample [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] applications on your [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps instance.</span></span> <span data-ttu-id="7ce96-106">The `Timer` hosted control is displayed in the status panel of your client application whenever a session is started.</span><span class="sxs-lookup"><span data-stu-id="7ce96-106">The `Timer` hosted control is displayed in the status panel of your client application whenever a session is started.</span></span>  
  
<a name="Actions"></a>   
## <a name="actions-for-the-timer-hosted-control"></a><span data-ttu-id="7ce96-107">Actions for the Timer hosted control</span><span class="sxs-lookup"><span data-stu-id="7ce96-107">Actions for the Timer hosted control</span></span>  
 <span data-ttu-id="7ce96-108">The following actions are supported by the `Timer` control:</span><span class="sxs-lookup"><span data-stu-id="7ce96-108">The following actions are supported by the `Timer` control:</span></span>  
  
- <span data-ttu-id="7ce96-109">`GetSessionSeconds`: Returns the total time, in seconds, that the session lasted.</span><span class="sxs-lookup"><span data-stu-id="7ce96-109">`GetSessionSeconds`: Returns the total time, in seconds, that the session lasted.</span></span>  
  
- <span data-ttu-id="7ce96-110">`GetSessionUsageInSeconds`: Returns the total time, in seconds, when the customer service rep was active in the current session.</span><span class="sxs-lookup"><span data-stu-id="7ce96-110">`GetSessionUsageInSeconds`: Returns the total time, in seconds, when the customer service rep was active in the current session.</span></span>  
  
  <span data-ttu-id="7ce96-111">You can use these two actions in your action calls to return session timer values.</span><span class="sxs-lookup"><span data-stu-id="7ce96-111">You can use these two actions in your action calls to return session timer values.</span></span> <span data-ttu-id="7ce96-112">However, before you can use these actions in your action calls, you’ll have to manually add these UII actions to the `Timer` hosted control instance.</span><span class="sxs-lookup"><span data-stu-id="7ce96-112">However, before you can use these actions in your action calls, you’ll have to manually add these UII actions to the `Timer` hosted control instance.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="7ce96-113">[Add a UII action to a hosted control](../unified-service-desk/add-uii-action-hosted-control.md)</span><span class="sxs-lookup"><span data-stu-id="7ce96-113">[Add a UII action to a hosted control](../unified-service-desk/add-uii-action-hosted-control.md)</span></span>  
  
  <span data-ttu-id="7ce96-114">The values are returned and displayed under the `$Return` replacement parameter.</span><span class="sxs-lookup"><span data-stu-id="7ce96-114">The values are returned and displayed under the `$Return` replacement parameter.</span></span> <span data-ttu-id="7ce96-115">To test the values returned by these two actions:</span><span class="sxs-lookup"><span data-stu-id="7ce96-115">To test the values returned by these two actions:</span></span>  
  
1. <span data-ttu-id="7ce96-116">Start [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client and connect to your Dynamics 365 for Customer Engagement apps instance.</span><span class="sxs-lookup"><span data-stu-id="7ce96-116">Start [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client and connect to your Dynamics 365 for Customer Engagement apps instance.</span></span>  
  
2. <span data-ttu-id="7ce96-117">Click the **My Work** menu, and then click a case record to open a session.</span><span class="sxs-lookup"><span data-stu-id="7ce96-117">Click the **My Work** menu, and then click a case record to open a session.</span></span>  
  
3. <span data-ttu-id="7ce96-118">Click **Settings** (![User settings button](../unified-service-desk/media/mp-ua-r17-usersettingsicon.png "User settings button")) at the top-right corner to display the `Debugger` control.</span><span class="sxs-lookup"><span data-stu-id="7ce96-118">Click **Settings** (![User settings button](../unified-service-desk/media/mp-ua-r17-usersettingsicon.png "User settings button")) at the top-right corner to display the `Debugger` control.</span></span>  
  
4. <span data-ttu-id="7ce96-119">On the **Direct Action** tab, select `Timer` from the **Hosted Control** list, the action name from the **Action** list, and click **Run Direct Action** (![USD debugger Run Action Call button](../unified-service-desk/media/usd-run-action-call-icon.png "USD debugger Run Action Call button")).</span><span class="sxs-lookup"><span data-stu-id="7ce96-119">On the **Direct Action** tab, select `Timer` from the **Hosted Control** list, the action name from the **Action** list, and click **Run Direct Action** (![USD debugger Run Action Call button](../unified-service-desk/media/usd-run-action-call-icon.png "USD debugger Run Action Call button")).</span></span> <span data-ttu-id="7ce96-120">Repeat this step for the other action.</span><span class="sxs-lookup"><span data-stu-id="7ce96-120">Repeat this step for the other action.</span></span>  
  
5. <span data-ttu-id="7ce96-121">Click **Refresh** (![refresh_grid](../unified-service-desk/media/crm-ua-refresh-grid.gif "refresh_grid")) to refresh the replacement parameter grid.</span><span class="sxs-lookup"><span data-stu-id="7ce96-121">Click **Refresh** (![refresh_grid](../unified-service-desk/media/crm-ua-refresh-grid.gif "refresh_grid")) to refresh the replacement parameter grid.</span></span> <span data-ttu-id="7ce96-122">Expand the `$Return` parameter to view the value (time in seconds) returned by the `GetSessionUsageInSeconds` and `GetSessionSeconds` actions.</span><span class="sxs-lookup"><span data-stu-id="7ce96-122">Expand the `$Return` parameter to view the value (time in seconds) returned by the `GetSessionUsageInSeconds` and `GetSessionSeconds` actions.</span></span>  
  
   <span data-ttu-id="7ce96-123">![Unified Service Desk session timer values](../unified-service-desk/media/usd-sessionvalueparameters.png "Unified Service Desk session timer values")</span><span class="sxs-lookup"><span data-stu-id="7ce96-123">![Unified Service Desk session timer values](../unified-service-desk/media/usd-sessionvalueparameters.png "Unified Service Desk session timer values")</span></span>  
  
<a name="ConfigureThreshold"></a>   
## <a name="configure-threshold-limits-and-colors-for-the-timer-hosted-control"></a><span data-ttu-id="7ce96-124">Configure threshold limits and colors for the Timer hosted control</span><span class="sxs-lookup"><span data-stu-id="7ce96-124">Configure threshold limits and colors for the Timer hosted control</span></span>  
 <span data-ttu-id="7ce96-125">You can configure the threshold time limits and colors for the `Timer` hosted control by specifying the values in an `XML` format in the `Extensions XML` field of the hosted control definition.</span><span class="sxs-lookup"><span data-stu-id="7ce96-125">You can configure the threshold time limits and colors for the `Timer` hosted control by specifying the values in an `XML` format in the `Extensions XML` field of the hosted control definition.</span></span> <span data-ttu-id="7ce96-126">The threshold color defines the color that the session timer is displayed in after the specified threshold time values have elapsed since the session started.</span><span class="sxs-lookup"><span data-stu-id="7ce96-126">The threshold color defines the color that the session timer is displayed in after the specified threshold time values have elapsed since the session started.</span></span> <span data-ttu-id="7ce96-127">Use hexadecimal color codes to specify the threshold color.</span><span class="sxs-lookup"><span data-stu-id="7ce96-127">Use hexadecimal color codes to specify the threshold color.</span></span>  
  
 <span data-ttu-id="7ce96-128">For example, the following XML defines the background color of the time string to be gray, the time string to change to orange when 60 seconds have elapsed, and then finally change to red when 90 seconds have elapsed since the current session started.</span><span class="sxs-lookup"><span data-stu-id="7ce96-128">For example, the following XML defines the background color of the time string to be gray, the time string to change to orange when 60 seconds have elapsed, and then finally change to red when 90 seconds have elapsed since the current session started.</span></span>  
  
```xml  
<thresholds>  
   <threshold backgroundcolor="#E4E4E4" />  
   <threshold foregroundcolor="#FF9900" seconds="60"/>  
   <threshold foregroundcolor="#FF0000" seconds="90"/>  
</thresholds>  
```  
  
 <span data-ttu-id="7ce96-129">To configure threshold limits and colors for the `Timer` hosted control:</span><span class="sxs-lookup"><span data-stu-id="7ce96-129">To configure threshold limits and colors for the `Timer` hosted control:</span></span>  
  
1. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  
  
2. <span data-ttu-id="7ce96-130">Click **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="7ce96-130">Click **Hosted Controls**.</span></span>  
  
3. <span data-ttu-id="7ce96-131">Search for the `Timer` hosted control, and click the hosted control name to open its definition.</span><span class="sxs-lookup"><span data-stu-id="7ce96-131">Search for the `Timer` hosted control, and click the hosted control name to open its definition.</span></span>  
  
4. <span data-ttu-id="7ce96-132">In the `Timer` hosted control definition form, update the XML in the **Extensions XML** field to specify the threshold limit and corresponding colors.</span><span class="sxs-lookup"><span data-stu-id="7ce96-132">In the `Timer` hosted control definition form, update the XML in the **Extensions XML** field to specify the threshold limit and corresponding colors.</span></span>  
  
5. <span data-ttu-id="7ce96-133">Save the hosted control definition.</span><span class="sxs-lookup"><span data-stu-id="7ce96-133">Save the hosted control definition.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="7ce96-134">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="7ce96-134">See also</span></span>  
 <span data-ttu-id="7ce96-135">[Kiểm soát tổ chức USD (Kiểm soát tổ chức)](../unified-service-desk/usd-hosted-control-hosted-control.md) </span><span class="sxs-lookup"><span data-stu-id="7ce96-135">[USD Hosted Control (Hosted Control)](../unified-service-desk/usd-hosted-control-hosted-control.md) </span></span>  
 [<span data-ttu-id="7ce96-136">Hosted control types and action/event reference</span><span class="sxs-lookup"><span data-stu-id="7ce96-136">Hosted control types and action/event reference</span></span>](../unified-service-desk/hosted-control-types-action-event-reference.md)
