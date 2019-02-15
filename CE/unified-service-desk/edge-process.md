---
title: Edge Process hosting method for your controls in Unified Service Desk for Dynamics 365 for Customer Engagement apps | MicrosoftDocs
description: Learn about the Edge Process hosting methods for your controls in Unified Service Desk.
ms.custom:
- dyn365-USD
ms.date: 12/19/2018
ms.service: dynamics-365-customerservice
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 (online)
- Dynamics 365 (on-premises)
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: D9E7AED8-1D3A-4E62-BD15-7C5CF153EB4E
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
monikerRange: '>= dynamics-usd-4'
ms.openlocfilehash: 0de3a2bf3b451074fb7fac04821484e909e3cc0c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385517"
---
# <a name="preview-edge-process"></a><span data-ttu-id="c7573-103">Preview: Edge Process</span><span class="sxs-lookup"><span data-stu-id="c7573-103">Preview: Edge Process</span></span>

[!INCLUDE[cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

<span data-ttu-id="c7573-104">The Edge Process browser control hosts your controls in individual Edge process instances and displays them in tabs in the Unified Service Desk client application.</span><span class="sxs-lookup"><span data-stu-id="c7573-104">The Edge Process browser control hosts your controls in individual Edge process instances and displays them in tabs in the Unified Service Desk client application.</span></span> <span data-ttu-id="c7573-105">It facilitates predictable and secure page rendering by making sure that if your web application works in Edge, it will work in Unified Service Desk.</span><span class="sxs-lookup"><span data-stu-id="c7573-105">It facilitates predictable and secure page rendering by making sure that if your web application works in Edge, it will work in Unified Service Desk.</span></span> <span data-ttu-id="c7573-106">You can select **Edge Process** as the hosting method for the **CRM Dialog**, **CRM Page**, **KM Control**, **Unified Interface Page**, **Unified Interface KM Control** and **Standard Web Application** type of hosted controls.</span><span class="sxs-lookup"><span data-stu-id="c7573-106">You can select **Edge Process** as the hosting method for the **CRM Dialog**, **CRM Page**, **KM Control**, **Unified Interface Page**, **Unified Interface KM Control** and **Standard Web Application** type of hosted controls.</span></span>

<span data-ttu-id="c7573-107">![Edge process hosted control setting](media/edge-process-hosted-control-setting.gif "Edge process hosted control setting")</span><span class="sxs-lookup"><span data-stu-id="c7573-107">![Edge process hosted control setting](media/edge-process-hosted-control-setting.gif "Edge process hosted control setting")</span></span>

<span data-ttu-id="c7573-108">The advantages of using the Edge process hosting method are as follows:</span><span class="sxs-lookup"><span data-stu-id="c7573-108">The advantages of using the Edge process hosting method are as follows:</span></span>

<span data-ttu-id="c7573-109">![Advantages of Edge Process](media/advantages-edge-process.PNG "Advantages of Edge Process")</span><span class="sxs-lookup"><span data-stu-id="c7573-109">![Advantages of Edge Process](media/advantages-edge-process.PNG "Advantages of Edge Process")</span></span>

- <span data-ttu-id="c7573-110">Webpages, including Dynamics 365 pages, render faster in Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c7573-110">Webpages, including Dynamics 365 pages, render faster in Microsoft Edge.</span></span>
- <span data-ttu-id="c7573-111">Microsoft Edge is a modern browser with better process and memory management.</span><span class="sxs-lookup"><span data-stu-id="c7573-111">Microsoft Edge is a modern browser with better process and memory management.</span></span>
- <span data-ttu-id="c7573-112">Microsoft Edge is the default browser for the Windows 10 operating system.</span><span class="sxs-lookup"><span data-stu-id="c7573-112">Microsoft Edge is the default browser for the Windows 10 operating system.</span></span>
- <span data-ttu-id="c7573-113">it provides easy configurations to host the applications in Unified Service Desk.</span><span class="sxs-lookup"><span data-stu-id="c7573-113">it provides easy configurations to host the applications in Unified Service Desk.</span></span>
- <span data-ttu-id="c7573-114">It provides improved reliability and supportability for browser-specific issues</span><span class="sxs-lookup"><span data-stu-id="c7573-114">It provides improved reliability and supportability for browser-specific issues</span></span>

> [!NOTE]
> <span data-ttu-id="c7573-115">To use **Edge Process**, you must have the latest Windows 10 operating system (Windows 10 October 2018 release).</span><span class="sxs-lookup"><span data-stu-id="c7573-115">To use **Edge Process**, you must have the latest Windows 10 operating system (Windows 10 October 2018 release).</span></span>

## <a name="edge-process-settings"></a><span data-ttu-id="c7573-116">Edge Process settings</span><span class="sxs-lookup"><span data-stu-id="c7573-116">Edge Process settings</span></span>

<span data-ttu-id="c7573-117">You can set the **Edge Process** on the hosted controls (exisitng hosted controls and new hosted controls) to host applications.</span><span class="sxs-lookup"><span data-stu-id="c7573-117">You can set the **Edge Process** on the hosted controls (exisitng hosted controls and new hosted controls) to host applications.</span></span> <span data-ttu-id="c7573-118">This allows you to choose the hosted controls that uses **Edge Process** based on your requirements.</span><span class="sxs-lookup"><span data-stu-id="c7573-118">This allows you to choose the hosted controls that uses **Edge Process** based on your requirements.</span></span> <span data-ttu-id="c7573-119">More information: [Create a hosted control with hosting type as Edge](edge-process.md#create-a-hosted-control-with-hosting-type-as-edge)</span><span class="sxs-lookup"><span data-stu-id="c7573-119">More information: [Create a hosted control with hosting type as Edge](edge-process.md#create-a-hosted-control-with-hosting-type-as-edge)</span></span>

<span data-ttu-id="c7573-120">If you want to set the **Edge Process** to host the applications for an entire organization, then use the **GlobalBrowserMode** Global UII option and specify the value as **Edge**.</span><span class="sxs-lookup"><span data-stu-id="c7573-120">If you want to set the **Edge Process** to host the applications for an entire organization, then use the **GlobalBrowserMode** Global UII option and specify the value as **Edge**.</span></span> <span data-ttu-id="c7573-121">More information: [Enable Edge for Unified Service Desk on client desktop](edge-process.md#enable-edge-for-unified-service-desk-on-client-desktop)</span><span class="sxs-lookup"><span data-stu-id="c7573-121">More information: [Enable Edge for Unified Service Desk on client desktop](edge-process.md#enable-edge-for-unified-service-desk-on-client-desktop)</span></span>

<span data-ttu-id="c7573-122">If you want to set the **Edge Process** only for some agents in your organization, then in the **UnifiedServiceDesk.exe.config** file, add the **GlobalBrowserMode** key with the value as **Edge**.</span><span class="sxs-lookup"><span data-stu-id="c7573-122">If you want to set the **Edge Process** only for some agents in your organization, then in the **UnifiedServiceDesk.exe.config** file, add the **GlobalBrowserMode** key with the value as **Edge**.</span></span> <span data-ttu-id="c7573-123">More information: [Enables Edge for an entire organization](edge-process.md#enable-edge-for-an-entire-organization)</span><span class="sxs-lookup"><span data-stu-id="c7573-123">More information: [Enables Edge for an entire organization](edge-process.md#enable-edge-for-an-entire-organization)</span></span>

### <a name="order-of-precedence"></a><span data-ttu-id="c7573-124">Order of precedence</span><span class="sxs-lookup"><span data-stu-id="c7573-124">Order of precedence</span></span>

- <span data-ttu-id="c7573-125">Setting the **GlobalBrowserMode** Global UII option value as **Edge**, takes precedence over the individual hosted control settings.</span><span class="sxs-lookup"><span data-stu-id="c7573-125">Setting the **GlobalBrowserMode** Global UII option value as **Edge**, takes precedence over the individual hosted control settings.</span></span> <br><br><span data-ttu-id="c7573-126">For example, some hosted controls have hosting type as **IE Process** and/or **Internal WPF**.</span><span class="sxs-lookup"><span data-stu-id="c7573-126">For example, some hosted controls have hosting type as **IE Process** and/or **Internal WPF**.</span></span> <span data-ttu-id="c7573-127">At the organization level, you set **GlobalBrowserMode** Global UII option value as **Edge**.</span><span class="sxs-lookup"><span data-stu-id="c7573-127">At the organization level, you set **GlobalBrowserMode** Global UII option value as **Edge**.</span></span> <span data-ttu-id="c7573-128">In this scenario, the Global UII option takes precedence and configuration uses the **Edge Process** to host the applications.</span><span class="sxs-lookup"><span data-stu-id="c7573-128">In this scenario, the Global UII option takes precedence and configuration uses the **Edge Process** to host the applications.</span></span> 

- <span data-ttu-id="c7573-129">Setting the **GlobalBrowser** mode key to **Edge** in the **UnifiedServiceDesk.exe.config** file for a particular client desktop, takes precedence over the individual hosted control settings.</span><span class="sxs-lookup"><span data-stu-id="c7573-129">Setting the **GlobalBrowser** mode key to **Edge** in the **UnifiedServiceDesk.exe.config** file for a particular client desktop, takes precedence over the individual hosted control settings.</span></span><br><br><span data-ttu-id="c7573-130">For example, some hosted controls have hosting type as **IE Process** and/or **Internal WPF**.</span><span class="sxs-lookup"><span data-stu-id="c7573-130">For example, some hosted controls have hosting type as **IE Process** and/or **Internal WPF**.</span></span> <span data-ttu-id="c7573-131">For a few agents, in their client desktops, you have set **GlobalBrowser** mode key to **Edge** in the **UnifiedServiceDesk.exe.config** file.</span><span class="sxs-lookup"><span data-stu-id="c7573-131">For a few agents, in their client desktops, you have set **GlobalBrowser** mode key to **Edge** in the **UnifiedServiceDesk.exe.config** file.</span></span> <span data-ttu-id="c7573-132">The value set in the **UnifiedServiceDesk.exe.config** file take precedence and configuration uses the **Edge Process** to host the applications.</span><span class="sxs-lookup"><span data-stu-id="c7573-132">The value set in the **UnifiedServiceDesk.exe.config** file take precedence and configuration uses the **Edge Process** to host the applications.</span></span>

<span data-ttu-id="c7573-133">Setting the **GlobalBrowser** mode key to **Edge** in the **UnifiedServiceDesk.exe.config** file for a particular client desktop, takes the precedence over other settings.</span><span class="sxs-lookup"><span data-stu-id="c7573-133">Setting the **GlobalBrowser** mode key to **Edge** in the **UnifiedServiceDesk.exe.config** file for a particular client desktop, takes the precedence over other settings.</span></span> 

## <a name="enable-edge-process"></a><span data-ttu-id="c7573-134">Enable Edge Process</span><span class="sxs-lookup"><span data-stu-id="c7573-134">Enable Edge Process</span></span>

<span data-ttu-id="c7573-135">Enable the **Edge Process** by doing one of the following ways:</span><span class="sxs-lookup"><span data-stu-id="c7573-135">Enable the **Edge Process** by doing one of the following ways:</span></span>

- <span data-ttu-id="c7573-136">Create a individual hosted control with hosting type as Edge</span><span class="sxs-lookup"><span data-stu-id="c7573-136">Create a individual hosted control with hosting type as Edge</span></span>
- <span data-ttu-id="c7573-137">Enable for individual client desktops</span><span class="sxs-lookup"><span data-stu-id="c7573-137">Enable for individual client desktops</span></span>
- <span data-ttu-id="c7573-138">Enable for entire an organization</span><span class="sxs-lookup"><span data-stu-id="c7573-138">Enable for entire an organization</span></span>

> [!NOTE]
> <span data-ttu-id="c7573-139">Enable the **Edge Process** either for individual client desktops or for entire organization.</span><span class="sxs-lookup"><span data-stu-id="c7573-139">Enable the **Edge Process** either for individual client desktops or for entire organization.</span></span>

### <a name="create-a-hosted-control-with-hosting-type-as-edge"></a><span data-ttu-id="c7573-140">Create a hosted control with hosting type as Edge</span><span class="sxs-lookup"><span data-stu-id="c7573-140">Create a hosted control with hosting type as Edge</span></span>

<span data-ttu-id="c7573-141">When you are creating a new hosted control, you can select **Edge Process** as the **Hosting Type**.</span><span class="sxs-lookup"><span data-stu-id="c7573-141">When you are creating a new hosted control, you can select **Edge Process** as the **Hosting Type**.</span></span>

1. <span data-ttu-id="c7573-142">Sign in to Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="c7573-142">Sign in to Dynamics 365.</span></span>

2. <span data-ttu-id="c7573-143">Go to **Settings** > **Unified Service Desk**.</span><span class="sxs-lookup"><span data-stu-id="c7573-143">Go to **Settings** > **Unified Service Desk**.</span></span>

3. <span data-ttu-id="c7573-144">Select **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="c7573-144">Select **Hosted Controls**.</span></span> <span data-ttu-id="c7573-145">Trang Hiển thị có kiểm soát tổ chức có sẵn.</span><span class="sxs-lookup"><span data-stu-id="c7573-145">The page displays available hosted controls.</span></span>

4. <span data-ttu-id="c7573-146">To create a new hosted control, select **New**.</span><span class="sxs-lookup"><span data-stu-id="c7573-146">To create a new hosted control, select **New**.</span></span>

5. <span data-ttu-id="c7573-147">On the **New Hosted Control** page, specify the details and select **Edge process** from the **Hosting Type** drop-down.</span><span class="sxs-lookup"><span data-stu-id="c7573-147">On the **New Hosted Control** page, specify the details and select **Edge process** from the **Hosting Type** drop-down.</span></span><br>
<span data-ttu-id="c7573-148">![Edge Process hosted control](media/edge-process-hosted-control.PNG "Edge Process hosted control")</span><span class="sxs-lookup"><span data-stu-id="c7573-148">![Edge Process hosted control](media/edge-process-hosted-control.PNG "Edge Process hosted control")</span></span>

6. <span data-ttu-id="c7573-149">Select **Save** to create the hosted control.</span><span class="sxs-lookup"><span data-stu-id="c7573-149">Select **Save** to create the hosted control.</span></span>

### <a name="enable-edge-for-unified-service-desk-on-client-desktop"></a><span data-ttu-id="c7573-150">Enable Edge for Unified Service Desk on client desktop</span><span class="sxs-lookup"><span data-stu-id="c7573-150">Enable Edge for Unified Service Desk on client desktop</span></span>

1. <span data-ttu-id="c7573-151">Go to directory where you have installed Unified Service Desk and double-click to open the **UnifiedServiceDesk.exe.config** file.</span><span class="sxs-lookup"><span data-stu-id="c7573-151">Go to directory where you have installed Unified Service Desk and double-click to open the **UnifiedServiceDesk.exe.config** file.</span></span>
<span data-ttu-id="c7573-152">Example path: `C:\Program Files\Microsoft Dynamics CRM USD\USD`</span><span class="sxs-lookup"><span data-stu-id="c7573-152">Example path: `C:\Program Files\Microsoft Dynamics CRM USD\USD`</span></span>

2. <span data-ttu-id="c7573-153">Under the `<appSettings>` section add the new key.</span><span class="sxs-lookup"><span data-stu-id="c7573-153">Under the `<appSettings>` section add the new key.</span></span><br>
`<add key="GlobalBrowserMode" value="Edge"/>`

  > [!div class="mx-imageBorder"]
  > <span data-ttu-id="c7573-154">![Edge Process configuration setting key](media/edge-process-app-config-file-setting.PNG "Edge Process configuration setting key")</span><span class="sxs-lookup"><span data-stu-id="c7573-154">![Edge Process configuration setting key](media/edge-process-app-config-file-setting.PNG "Edge Process configuration setting key")</span></span>

3. <span data-ttu-id="c7573-155">Save the file.</span><span class="sxs-lookup"><span data-stu-id="c7573-155">Save the file.</span></span>

### <a name="enable-edge-for-an-entire-organization"></a><span data-ttu-id="c7573-156">Enable Edge for an entire organization</span><span class="sxs-lookup"><span data-stu-id="c7573-156">Enable Edge for an entire organization</span></span>

<span data-ttu-id="c7573-157">Add a new Global UII option for your organization named **GlobalBrowserMode**.</span><span class="sxs-lookup"><span data-stu-id="c7573-157">Add a new Global UII option for your organization named **GlobalBrowserMode**.</span></span> <span data-ttu-id="c7573-158">Specify the value as **Edge**.</span><span class="sxs-lookup"><span data-stu-id="c7573-158">Specify the value as **Edge**.</span></span>

<span data-ttu-id="c7573-159">![Edge process global uii option](media/edge-process-global-uii-option.gif "Edge process global uii option")</span><span class="sxs-lookup"><span data-stu-id="c7573-159">![Edge process global uii option](media/edge-process-global-uii-option.gif "Edge process global uii option")</span></span>

1. <span data-ttu-id="c7573-160">Sign in to Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="c7573-160">Sign in to Dynamics 365.</span></span>

2. <span data-ttu-id="c7573-161">Go to **Settings** > **Unified Service Desk** > **Options**.</span><span class="sxs-lookup"><span data-stu-id="c7573-161">Go to **Settings** > **Unified Service Desk** > **Options**.</span></span>

3. <span data-ttu-id="c7573-162">On the **Active UII Options** page, select **New**.</span><span class="sxs-lookup"><span data-stu-id="c7573-162">On the **Active UII Options** page, select **New**.</span></span>

4. <span data-ttu-id="c7573-163">Choose **Others** for the **Global Option** field.</span><span class="sxs-lookup"><span data-stu-id="c7573-163">Choose **Others** for the **Global Option** field.</span></span>

5. <span data-ttu-id="c7573-164">Type **GlobalBrowserMode** for the **Name** field.</span><span class="sxs-lookup"><span data-stu-id="c7573-164">Type **GlobalBrowserMode** for the **Name** field.</span></span>

6. <span data-ttu-id="c7573-165">Type **Edge** for the **Value** field.</span><span class="sxs-lookup"><span data-stu-id="c7573-165">Type **Edge** for the **Value** field.</span></span>

7. <span data-ttu-id="c7573-166">Chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="c7573-166">Select **Save**.</span></span>

## <a name="debug-edge-process-using-microsoft-edge-devtools-preview"></a><span data-ttu-id="c7573-167">Debug Edge Process using Microsoft Edge DevTools Preview</span><span class="sxs-lookup"><span data-stu-id="c7573-167">Debug Edge Process using Microsoft Edge DevTools Preview</span></span>

<span data-ttu-id="c7573-168">With Edge process, you can use the **Microsoft Edge DevTools Preview** tool as a JavaScript debugger.</span><span class="sxs-lookup"><span data-stu-id="c7573-168">With Edge process, you can use the **Microsoft Edge DevTools Preview** tool as a JavaScript debugger.</span></span> <span data-ttu-id="c7573-169">Edge DevTools helps you debug the webpage locally or remotely.</span><span class="sxs-lookup"><span data-stu-id="c7573-169">Edge DevTools helps you debug the webpage locally or remotely.</span></span>

<span data-ttu-id="c7573-170">In the panel, you can see all the active Edge process.</span><span class="sxs-lookup"><span data-stu-id="c7573-170">In the panel, you can see all the active Edge process.</span></span> <span data-ttu-id="c7573-171">Select the desired webpage from the active list to open a new instance.</span><span class="sxs-lookup"><span data-stu-id="c7573-171">Select the desired webpage from the active list to open a new instance.</span></span>

<span data-ttu-id="c7573-172">More information: [Microsoft Edge DevTools Preview](https://docs.microsoft.com/en-us/microsoft-edge/devtools-guide)</span><span class="sxs-lookup"><span data-stu-id="c7573-172">More information: [Microsoft Edge DevTools Preview](https://docs.microsoft.com/en-us/microsoft-edge/devtools-guide)</span></span>

## <a name="runscript-action-is-asynchronous-in-edge-process"></a><span data-ttu-id="c7573-173">RunScript action is asynchronous in Edge Process</span><span class="sxs-lookup"><span data-stu-id="c7573-173">RunScript action is asynchronous in Edge Process</span></span>

<span data-ttu-id="c7573-174">The Edge browser support only the asynchronous operations, and the RunScript action will be asynchronous.</span><span class="sxs-lookup"><span data-stu-id="c7573-174">The Edge browser support only the asynchronous operations, and the RunScript action will be asynchronous.</span></span>
<span data-ttu-id="c7573-175">If your custom code execution is dependent on the return value provided by RunScript action that injects JavaScript into the main frame of the application, then your custom code execution may fail.</span><span class="sxs-lookup"><span data-stu-id="c7573-175">If your custom code execution is dependent on the return value provided by RunScript action that injects JavaScript into the main frame of the application, then your custom code execution may fail.</span></span>

<span data-ttu-id="c7573-176">For example, Your custom code has a RunScript actions that injects the JavaScript into the main frame of the application followed by an operation or another RunScript action.</span><span class="sxs-lookup"><span data-stu-id="c7573-176">For example, Your custom code has a RunScript actions that injects the JavaScript into the main frame of the application followed by an operation or another RunScript action.</span></span> <span data-ttu-id="c7573-177">The RunScript action is invoked and returns a value after the JavaScript injection.</span><span class="sxs-lookup"><span data-stu-id="c7573-177">The RunScript action is invoked and returns a value after the JavaScript injection.</span></span> <span data-ttu-id="c7573-178">If the subsequent operation or another RunScript action executes based on the return value provided by the executed RunScript action, then subsequent operations of your custom code will fail.</span><span class="sxs-lookup"><span data-stu-id="c7573-178">If the subsequent operation or another RunScript action executes based on the return value provided by the executed RunScript action, then subsequent operations of your custom code will fail.</span></span>

### <a name="scenario-example"></a><span data-ttu-id="c7573-179">Scenario example</span><span class="sxs-lookup"><span data-stu-id="c7573-179">Scenario example</span></span> 

<span data-ttu-id="c7573-180">Whenever you open a case, verify whether the case has been open for 10 or more days, then display a message in a dialog.</span><span class="sxs-lookup"><span data-stu-id="c7573-180">Whenever you open a case, verify whether the case has been open for 10 or more days, then display a message in a dialog.</span></span> <span data-ttu-id="c7573-181">When you perform an action on the dialog box, the phone call page is opened for further operations.</span><span class="sxs-lookup"><span data-stu-id="c7573-181">When you perform an action on the dialog box, the phone call page is opened for further operations.</span></span>

<span data-ttu-id="c7573-182">To perform the above-mentioned scenario, you must have an action call that executes a **RunScript** action and returns a value for the next operation.</span><span class="sxs-lookup"><span data-stu-id="c7573-182">To perform the above-mentioned scenario, you must have an action call that executes a **RunScript** action and returns a value for the next operation.</span></span> <span data-ttu-id="c7573-183">The data on the action call calculates the number of days a case is open.</span><span class="sxs-lookup"><span data-stu-id="c7573-183">The data on the action call calculates the number of days a case is open.</span></span> 

<span data-ttu-id="c7573-184">Now, you must create an action call with action as **ExecuteOnDataAvailable**, and the data field must have the return value of the first action call.</span><span class="sxs-lookup"><span data-stu-id="c7573-184">Now, you must create an action call with action as **ExecuteOnDataAvailable**, and the data field must have the return value of the first action call.</span></span> <span data-ttu-id="c7573-185">That is, the return value will have the form `[[$Return.ActionCallName]]`.</span><span class="sxs-lookup"><span data-stu-id="c7573-185">That is, the return value will have the form `[[$Return.ActionCallName]]`.</span></span> <span data-ttu-id="c7573-186">This ensures that after the first action is executed and the return is available, this action call will be executed.</span><span class="sxs-lookup"><span data-stu-id="c7573-186">This ensures that after the first action is executed and the return is available, this action call will be executed.</span></span>

<span data-ttu-id="c7573-187">Next, you must create a sub action call to show the number of days a case is in the open state.</span><span class="sxs-lookup"><span data-stu-id="c7573-187">Next, you must create a sub action call to show the number of days a case is in the open state.</span></span> <span data-ttu-id="c7573-188">The data field will use the return value form the first action call, that is, `[[$Return.ActionCallName]]`.</span><span class="sxs-lookup"><span data-stu-id="c7573-188">The data field will use the return value form the first action call, that is, `[[$Return.ActionCallName]]`.</span></span>

<span data-ttu-id="c7573-189">You must create another sub action call to open the phone call page and perform the next operation.</span><span class="sxs-lookup"><span data-stu-id="c7573-189">You must create another sub action call to open the phone call page and perform the next operation.</span></span> <span data-ttu-id="c7573-190">After seeing the message, you select the **OK** button on the dialog, and this causes the phone call page to opens.</span><span class="sxs-lookup"><span data-stu-id="c7573-190">After seeing the message, you select the **OK** button on the dialog, and this causes the phone call page to opens.</span></span>

<span data-ttu-id="c7573-191">Let us see what configurations you need to do create for the above-mentioned scenario.</span><span class="sxs-lookup"><span data-stu-id="c7573-191">Let us see what configurations you need to do create for the above-mentioned scenario.</span></span>

### <a name="step-1-create-a-hosted-control"></a><span data-ttu-id="c7573-192">Step 1: Create a hosted control</span><span class="sxs-lookup"><span data-stu-id="c7573-192">Step 1: Create a hosted control</span></span>

1. <span data-ttu-id="c7573-193">Go to **Settings** > **Unified Service Desk** > **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="c7573-193">Go to **Settings** > **Unified Service Desk** > **Hosted Controls**.</span></span>

2. <span data-ttu-id="c7573-194">Chọn **+ Mới**.</span><span class="sxs-lookup"><span data-stu-id="c7573-194">Select **+ New**.</span></span>

3. <span data-ttu-id="c7573-195">Add the following details and save the hosted control.</span><span class="sxs-lookup"><span data-stu-id="c7573-195">Add the following details and save the hosted control.</span></span>

| <span data-ttu-id="c7573-196">Trường</span><span class="sxs-lookup"><span data-stu-id="c7573-196">Field</span></span> | <span data-ttu-id="c7573-197">Value</span><span class="sxs-lookup"><span data-stu-id="c7573-197">Value</span></span> |
|--------|---------|
| <span data-ttu-id="c7573-198">Tên</span><span class="sxs-lookup"><span data-stu-id="c7573-198">Name</span></span> | <span data-ttu-id="c7573-199">Sự cố</span><span class="sxs-lookup"><span data-stu-id="c7573-199">Incident</span></span> |
| <span data-ttu-id="c7573-200">Tên Hiển thị</span><span class="sxs-lookup"><span data-stu-id="c7573-200">Display Name</span></span> | `[[incident.title]]` |
| <span data-ttu-id="c7573-201">Unified Service Desk Component Type</span><span class="sxs-lookup"><span data-stu-id="c7573-201">Unified Service Desk Component Type</span></span> | <span data-ttu-id="c7573-202">Unified Interface Page</span><span class="sxs-lookup"><span data-stu-id="c7573-202">Unified Interface Page</span></span> |
| <span data-ttu-id="c7573-203">Loại lưu trữ</span><span class="sxs-lookup"><span data-stu-id="c7573-203">Hosting Type</span></span> | <span data-ttu-id="c7573-204">Edge Process</span><span class="sxs-lookup"><span data-stu-id="c7573-204">Edge Process</span></span> |
| <span data-ttu-id="c7573-205">Nhóm hiển thị</span><span class="sxs-lookup"><span data-stu-id="c7573-205">Display Group</span></span> | <span data-ttu-id="c7573-206">Bảng điều khiển chính</span><span class="sxs-lookup"><span data-stu-id="c7573-206">MainPanel</span></span> |

### <a name="step-2-create-two-action-calls"></a><span data-ttu-id="c7573-207">Step 2: Create two action calls</span><span class="sxs-lookup"><span data-stu-id="c7573-207">Step 2: Create two action calls</span></span>

1. <span data-ttu-id="c7573-208">Go to  **Settings** > **Unified Service Desk** > **Action Calls**.</span><span class="sxs-lookup"><span data-stu-id="c7573-208">Go to  **Settings** > **Unified Service Desk** > **Action Calls**.</span></span>

2. <span data-ttu-id="c7573-209">Select **+ New**.</span><span class="sxs-lookup"><span data-stu-id="c7573-209">Select **+ New**.</span></span>

3. <span data-ttu-id="c7573-210">Add the following details and save the action call.</span><span class="sxs-lookup"><span data-stu-id="c7573-210">Add the following details and save the action call.</span></span>

| <span data-ttu-id="c7573-211">Trường</span><span class="sxs-lookup"><span data-stu-id="c7573-211">Field</span></span> | <span data-ttu-id="c7573-212">Value</span><span class="sxs-lookup"><span data-stu-id="c7573-212">Value</span></span> |
|--------|---------|
| <span data-ttu-id="c7573-213">Tên</span><span class="sxs-lookup"><span data-stu-id="c7573-213">Name</span></span> | <span data-ttu-id="c7573-214">FindNoOfDaysCaseBeingOpened</span><span class="sxs-lookup"><span data-stu-id="c7573-214">FindNoOfDaysCaseBeingOpened</span></span> |
| <span data-ttu-id="c7573-215">Thứ tự</span><span class="sxs-lookup"><span data-stu-id="c7573-215">Order</span></span> | <span data-ttu-id="c7573-216">1</span><span class="sxs-lookup"><span data-stu-id="c7573-216">1</span></span> |
| <span data-ttu-id="c7573-217">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="c7573-217">Hosted Control</span></span> | <span data-ttu-id="c7573-218">Sự cố</span><span class="sxs-lookup"><span data-stu-id="c7573-218">Incident</span></span> |
| <span data-ttu-id="c7573-219">Hành động</span><span class="sxs-lookup"><span data-stu-id="c7573-219">Action</span></span> | <span data-ttu-id="c7573-220">Chạy mã lệnh</span><span class="sxs-lookup"><span data-stu-id="c7573-220">RunScript</span></span> |
| <span data-ttu-id="c7573-221">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="c7573-221">Data</span></span> | <span data-ttu-id="c7573-222">function findAge(dateString)</span><span class="sxs-lookup"><span data-stu-id="c7573-222">function findAge(dateString)</span></span></br><span data-ttu-id="c7573-223">{</span><span class="sxs-lookup"><span data-stu-id="c7573-223">{</span></span></br><span data-ttu-id="c7573-224">if("[[incident.statuscode]]".indexOf("1") > -1){</span><span class="sxs-lookup"><span data-stu-id="c7573-224">if("[[incident.statuscode]]".indexOf("1") > -1){</span></span></br><span data-ttu-id="c7573-225">var date1 =new Date(dateString);</span><span class="sxs-lookup"><span data-stu-id="c7573-225">var date1 =new Date(dateString);</span></span></br><span data-ttu-id="c7573-226">var date2 =new Date();</span><span class="sxs-lookup"><span data-stu-id="c7573-226">var date2 =new Date();</span></span></br><span data-ttu-id="c7573-227">var timeDiff = Math.abs(date2.getTime() - date1.getTime());</span><span class="sxs-lookup"><span data-stu-id="c7573-227">var timeDiff = Math.abs(date2.getTime() - date1.getTime());</span></span></br><span data-ttu-id="c7573-228">var diffDays = Math.ceil(timeDiff / (1000 \* 3600 \* 24));</span><span class="sxs-lookup"><span data-stu-id="c7573-228">var diffDays = Math.ceil(timeDiff / (1000 \* 3600 \* 24));</span></span></br><span data-ttu-id="c7573-229">return diffDays.toString();</span><span class="sxs-lookup"><span data-stu-id="c7573-229">return diffDays.toString();</span></span></br><span data-ttu-id="c7573-230">}</span><span class="sxs-lookup"><span data-stu-id="c7573-230">}</span></span></br><span data-ttu-id="c7573-231">return 0;</span><span class="sxs-lookup"><span data-stu-id="c7573-231">return 0;</span></span></br><span data-ttu-id="c7573-232">}</span><span class="sxs-lookup"><span data-stu-id="c7573-232">}</span></span></br><span data-ttu-id="c7573-233">findAge("[[incident.createdon]]");</span><span class="sxs-lookup"><span data-stu-id="c7573-233">findAge("[[incident.createdon]]");</span></span> |

4. <span data-ttu-id="c7573-234">Repeat steps 2 and 3 to create another action call.</span><span class="sxs-lookup"><span data-stu-id="c7573-234">Repeat steps 2 and 3 to create another action call.</span></span>

| <span data-ttu-id="c7573-235">Trường</span><span class="sxs-lookup"><span data-stu-id="c7573-235">Field</span></span> | <span data-ttu-id="c7573-236">Value</span><span class="sxs-lookup"><span data-stu-id="c7573-236">Value</span></span> |
|--------|---------|
| <span data-ttu-id="c7573-237">Tên</span><span class="sxs-lookup"><span data-stu-id="c7573-237">Name</span></span> | <span data-ttu-id="c7573-238">DaysValue</span><span class="sxs-lookup"><span data-stu-id="c7573-238">DaysValue</span></span>|
| <span data-ttu-id="c7573-239">Thứ tự</span><span class="sxs-lookup"><span data-stu-id="c7573-239">Order</span></span> | <span data-ttu-id="c7573-240">2</span><span class="sxs-lookup"><span data-stu-id="c7573-240">2</span></span> |
| <span data-ttu-id="c7573-241">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="c7573-241">Hosted Control</span></span> | <span data-ttu-id="c7573-242">CRM Global Manager</span><span class="sxs-lookup"><span data-stu-id="c7573-242">CRM Global Manager</span></span> |
| <span data-ttu-id="c7573-243">Hành động</span><span class="sxs-lookup"><span data-stu-id="c7573-243">Action</span></span> | <span data-ttu-id="c7573-244">ExecuteOnDataAvailable</span><span class="sxs-lookup"><span data-stu-id="c7573-244">ExecuteOnDataAvailable</span></span> |
| <span data-ttu-id="c7573-245">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="c7573-245">Data</span></span> | `[[$Return.FindNoOfDaysCaseBeingOpened]]` |

#### <a name="step-3-create-two-action-calls-and-add-them-under-the-daysvalue-action-call"></a><span data-ttu-id="c7573-246">Step 3: Create two action calls, and add them under the DaysValue action call</span><span class="sxs-lookup"><span data-stu-id="c7573-246">Step 3: Create two action calls, and add them under the DaysValue action call</span></span>

1. <span data-ttu-id="c7573-247">Go to **Settings** > **Unified Service Desk** > **Action Calls**.</span><span class="sxs-lookup"><span data-stu-id="c7573-247">Go to **Settings** > **Unified Service Desk** > **Action Calls**.</span></span>

2. <span data-ttu-id="c7573-248">Select **+ New**.</span><span class="sxs-lookup"><span data-stu-id="c7573-248">Select **+ New**.</span></span>

3. <span data-ttu-id="c7573-249">Add the following details and save the action call.</span><span class="sxs-lookup"><span data-stu-id="c7573-249">Add the following details and save the action call.</span></span>

| <span data-ttu-id="c7573-250">Trường</span><span class="sxs-lookup"><span data-stu-id="c7573-250">Field</span></span> | <span data-ttu-id="c7573-251">Value</span><span class="sxs-lookup"><span data-stu-id="c7573-251">Value</span></span> |
|--------|---------|
| <span data-ttu-id="c7573-252">Tên</span><span class="sxs-lookup"><span data-stu-id="c7573-252">Name</span></span> | <span data-ttu-id="c7573-253">DisplayMessageForCaseOpen</span><span class="sxs-lookup"><span data-stu-id="c7573-253">DisplayMessageForCaseOpen</span></span> |
| <span data-ttu-id="c7573-254">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="c7573-254">Hosted Control</span></span> | <span data-ttu-id="c7573-255">CRM Global Manager</span><span class="sxs-lookup"><span data-stu-id="c7573-255">CRM Global Manager</span></span> |
| <span data-ttu-id="c7573-256">Hành động</span><span class="sxs-lookup"><span data-stu-id="c7573-256">Action</span></span> | <span data-ttu-id="c7573-257">DisplayMessage</span><span class="sxs-lookup"><span data-stu-id="c7573-257">DisplayMessage</span></span> |
| <span data-ttu-id="c7573-258">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="c7573-258">Data</span></span> |    <span data-ttu-id="c7573-259">text=No of days case is in open state: [[$Return.FindNoOfDaysCaseBeingOpened]]</span><span class="sxs-lookup"><span data-stu-id="c7573-259">text=No of days case is in open state: [[$Return.FindNoOfDaysCaseBeingOpened]]</span></span><br>
<span data-ttu-id="c7573-260">caption=Case is open</span><span class="sxs-lookup"><span data-stu-id="c7573-260">caption=Case is open</span></span> |

4. <span data-ttu-id="c7573-261">Repeat steps 2 and 3 to create another action call.</span><span class="sxs-lookup"><span data-stu-id="c7573-261">Repeat steps 2 and 3 to create another action call.</span></span>

| <span data-ttu-id="c7573-262">Trường</span><span class="sxs-lookup"><span data-stu-id="c7573-262">Field</span></span> | <span data-ttu-id="c7573-263">Value</span><span class="sxs-lookup"><span data-stu-id="c7573-263">Value</span></span> |
|--------|---------|
| <span data-ttu-id="c7573-264">Tên</span><span class="sxs-lookup"><span data-stu-id="c7573-264">Name</span></span> | <span data-ttu-id="c7573-265">OpenPhoneCallPage</span><span class="sxs-lookup"><span data-stu-id="c7573-265">OpenPhoneCallPage</span></span> |
| <span data-ttu-id="c7573-266">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="c7573-266">Hosted Control</span></span> | <span data-ttu-id="c7573-267">Cuộc gọi Điện thoại </span><span class="sxs-lookup"><span data-stu-id="c7573-267">PhoneCall</span></span> |
| <span data-ttu-id="c7573-268">Hành động</span><span class="sxs-lookup"><span data-stu-id="c7573-268">Action</span></span> | <span data-ttu-id="c7573-269">New_CRM_Page</span><span class="sxs-lookup"><span data-stu-id="c7573-269">New_CRM_Page</span></span> |
| <span data-ttu-id="c7573-270">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="c7573-270">Data</span></span> |        <span data-ttu-id="c7573-271">LogicalName=phonecall</span><span class="sxs-lookup"><span data-stu-id="c7573-271">LogicalName=phonecall</span></span><br><span data-ttu-id="c7573-272">description=Long pending case more than 9 days</span><span class="sxs-lookup"><span data-stu-id="c7573-272">description=Long pending case more than 9 days</span></span> <br> <span data-ttu-id="c7573-273">subject=Long pending case</span><span class="sxs-lookup"><span data-stu-id="c7573-273">subject=Long pending case</span></span> <br> |
| <span data-ttu-id="c7573-274">Điều kiện</span><span class="sxs-lookup"><span data-stu-id="c7573-274">Condition</span></span> | <span data-ttu-id="c7573-275">"[[$Return.FindNoOfDaysCaseBeingOpened]]">9</span><span class="sxs-lookup"><span data-stu-id="c7573-275">"[[$Return.FindNoOfDaysCaseBeingOpened]]">9</span></span> |

5. <span data-ttu-id="c7573-276">From the list of action calls, select the **DaysValue** action call.</span><span class="sxs-lookup"><span data-stu-id="c7573-276">From the list of action calls, select the **DaysValue** action call.</span></span>

6. <span data-ttu-id="c7573-277">In the navigation bar, next to the **DaysValue** action call, select the *>* icon, and select **Sub Action Call**.</span><span class="sxs-lookup"><span data-stu-id="c7573-277">In the navigation bar, next to the **DaysValue** action call, select the *>* icon, and select **Sub Action Call**.</span></span>

7. <span data-ttu-id="c7573-278">Select the **ADD EXISTING ACTION CALL** option.</span><span class="sxs-lookup"><span data-stu-id="c7573-278">Select the **ADD EXISTING ACTION CALL** option.</span></span> <span data-ttu-id="c7573-279">In the search field, type the action **DisplayMessageForCaseOpen**, and select the search icon.</span><span class="sxs-lookup"><span data-stu-id="c7573-279">In the search field, type the action **DisplayMessageForCaseOpen**, and select the search icon.</span></span>

8. <span data-ttu-id="c7573-280">To add the action call, select the action call name that appears.</span><span class="sxs-lookup"><span data-stu-id="c7573-280">To add the action call, select the action call name that appears.</span></span>

9. <span data-ttu-id="c7573-281">Perform the steps 7 and 8 to add the **OpenPhoneCallPage** action call.</span><span class="sxs-lookup"><span data-stu-id="c7573-281">Perform the steps 7 and 8 to add the **OpenPhoneCallPage** action call.</span></span>

10. <span data-ttu-id="c7573-282">Lưu các thay đổi.</span><span class="sxs-lookup"><span data-stu-id="c7573-282">Save the changes.</span></span>

#### <a name="step-4-add-the-action-calls-to-the-pageready-event"></a><span data-ttu-id="c7573-283">Step 4: Add the action calls to the PageReady event</span><span class="sxs-lookup"><span data-stu-id="c7573-283">Step 4: Add the action calls to the PageReady event</span></span>

1. <span data-ttu-id="c7573-284">Go to  **Settings** > **Unified Service Desk** > **Events**.</span><span class="sxs-lookup"><span data-stu-id="c7573-284">Go to  **Settings** > **Unified Service Desk** > **Events**.</span></span>

2. <span data-ttu-id="c7573-285">Select the **PageReady** event for the **Incident** hosted control from the list of events.</span><span class="sxs-lookup"><span data-stu-id="c7573-285">Select the **PageReady** event for the **Incident** hosted control from the list of events.</span></span>

3. <span data-ttu-id="c7573-286">On the event page, under the **Active Actions** area, click **+** to add action calls.</span><span class="sxs-lookup"><span data-stu-id="c7573-286">On the event page, under the **Active Actions** area, click **+** to add action calls.</span></span>

4. <span data-ttu-id="c7573-287">A search box appears, type **FindNoOfDaysCaseBeingOpened** and select the search icon and select the action call.</span><span class="sxs-lookup"><span data-stu-id="c7573-287">A search box appears, type **FindNoOfDaysCaseBeingOpened** and select the search icon and select the action call.</span></span> <span data-ttu-id="c7573-288">The action call appears under the **Active Actions** area.</span><span class="sxs-lookup"><span data-stu-id="c7573-288">The action call appears under the **Active Actions** area.</span></span>

5. <span data-ttu-id="c7573-289">Repeat step 4 to add the **DaysValue** action.</span><span class="sxs-lookup"><span data-stu-id="c7573-289">Repeat step 4 to add the **DaysValue** action.</span></span>

6. <span data-ttu-id="c7573-290">Save the changes.</span><span class="sxs-lookup"><span data-stu-id="c7573-290">Save the changes.</span></span>

## <a name="edgesingleprocess-global-uii-option"></a><span data-ttu-id="c7573-291">EdgeSingleProcess global UII option</span><span class="sxs-lookup"><span data-stu-id="c7573-291">EdgeSingleProcess global UII option</span></span>

<span data-ttu-id="c7573-292">With the Edge WebView control, each domain will have its own process.</span><span class="sxs-lookup"><span data-stu-id="c7573-292">With the Edge WebView control, each domain will have its own process.</span></span> <span data-ttu-id="c7573-293">If your organization requires common authentication modes across different domains, the Edge process might not support the same authentication.</span><span class="sxs-lookup"><span data-stu-id="c7573-293">If your organization requires common authentication modes across different domains, the Edge process might not support the same authentication.</span></span>

<span data-ttu-id="c7573-294">To use common authentication mode across different domains, use the `EdgeSingleProcess` global UII option to ensure all the processes with different domains are created in a single process at the run-time.</span><span class="sxs-lookup"><span data-stu-id="c7573-294">To use common authentication mode across different domains, use the `EdgeSingleProcess` global UII option to ensure all the processes with different domains are created in a single process at the run-time.</span></span> 

<span data-ttu-id="c7573-295">To use the `EdgeSingleProcess`, you must add the UII option and set the value to `True`.</span><span class="sxs-lookup"><span data-stu-id="c7573-295">To use the `EdgeSingleProcess`, you must add the UII option and set the value to `True`.</span></span> <span data-ttu-id="c7573-296">More information: [EdgeSingleProcess](admin/manage-options-unified-service-desk.md)</span><span class="sxs-lookup"><span data-stu-id="c7573-296">More information: [EdgeSingleProcess](admin/manage-options-unified-service-desk.md)</span></span>

### <a name="add-the-uii-option"></a><span data-ttu-id="c7573-297">Add the UII option</span><span class="sxs-lookup"><span data-stu-id="c7573-297">Add the UII option</span></span>

1. <span data-ttu-id="c7573-298">Đăng nhập vào [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].</span><span class="sxs-lookup"><span data-stu-id="c7573-298">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].</span></span>

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]

3. <span data-ttu-id="c7573-299">Select **Options**.</span><span class="sxs-lookup"><span data-stu-id="c7573-299">Select **Options**.</span></span>  

4. <span data-ttu-id="c7573-300">Select **New** on the **Active UII Options** page.</span><span class="sxs-lookup"><span data-stu-id="c7573-300">Select **New** on the **Active UII Options** page.</span></span>

5. <span data-ttu-id="c7573-301">Choose **Others** for the **Global Option** field.</span><span class="sxs-lookup"><span data-stu-id="c7573-301">Choose **Others** for the **Global Option** field.</span></span>

6. <span data-ttu-id="c7573-302">Type **EdgeSingleProcess** for the **Name** field.</span><span class="sxs-lookup"><span data-stu-id="c7573-302">Type **EdgeSingleProcess** for the **Name** field.</span></span>

7. <span data-ttu-id="c7573-303">Type **True** for the **Value** field.</span><span class="sxs-lookup"><span data-stu-id="c7573-303">Type **True** for the **Value** field.</span></span>

8. <span data-ttu-id="c7573-304">Chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="c7573-304">Select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="c7573-305">If you set the value as `False` or leave the field blank, the option will be disabled.</span><span class="sxs-lookup"><span data-stu-id="c7573-305">If you set the value as `False` or leave the field blank, the option will be disabled.</span></span>


## <a name="sign-out-from-sessions-when-using-the-edge-process"></a><span data-ttu-id="c7573-306">Sign out from sessions when using the Edge Process</span><span class="sxs-lookup"><span data-stu-id="c7573-306">Sign out from sessions when using the Edge Process</span></span>

<span data-ttu-id="c7573-307">To sign out from sessions when using the Edge process, you must configure the sign-out URL using the **Navigate** action on the hosted control.</span><span class="sxs-lookup"><span data-stu-id="c7573-307">To sign out from sessions when using the Edge process, you must configure the sign-out URL using the **Navigate** action on the hosted control.</span></span> <span data-ttu-id="c7573-308">For example, the sign-out URL of Dynamics 365 for Customer Engagement apps is `url=/main.aspx?signout=1`.</span><span class="sxs-lookup"><span data-stu-id="c7573-308">For example, the sign-out URL of Dynamics 365 for Customer Engagement apps is `url=/main.aspx?signout=1`.</span></span>

## <a name="limitations"></a><span data-ttu-id="c7573-309">Giới hạn</span><span class="sxs-lookup"><span data-stu-id="c7573-309">Limitations</span></span>

<span data-ttu-id="c7573-310">To learn about the limitations of the Edge process, see [Edge process limitations](release-notes.md)</span><span class="sxs-lookup"><span data-stu-id="c7573-310">To learn about the limitations of the Edge process, see [Edge process limitations](release-notes.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="c7573-311">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="c7573-311">See also</span></span>  
 [<span data-ttu-id="c7573-312">Tạo hoặc chỉnh sửa kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="c7573-312">Create or edit a hosted control</span></span>](../unified-service-desk/create-edit-hosted-control.md)  

 [<span data-ttu-id="c7573-313">Tham chiếu loại kiểm soát tổ chức và hoạt động/sự kiện</span><span class="sxs-lookup"><span data-stu-id="c7573-313">Hosted control types and action/event reference</span></span>](../unified-service-desk/hosted-control-types-action-event-reference.md)   

 [<span data-ttu-id="c7573-314">Quản lý kiểm soát tổ chức, hành động và sự kiện</span><span class="sxs-lookup"><span data-stu-id="c7573-314">Manage hosted controls, actions, and events</span></span>](../unified-service-desk/manage-hosted-controls-actions-events.md)
