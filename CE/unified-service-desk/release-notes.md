---
title: Unified Service Desk Release Notes | MicrosoftDocs
description: Learn about the known issues and limitations in Unified Service Desk.
keywords: ''
ms.date: 12/17/2018
ms.service:
- usd
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: B0070DA6-803C-4F92-92E7-9524EDD7C1A2
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 1a7c2083d8dde4030a3dd8a62eeaa86b46244d0c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386384"
---
# <a name="unified-service-desk-known-issues-and-limitations"></a><span data-ttu-id="d75de-103">Unified Service Desk known issues and limitations</span><span class="sxs-lookup"><span data-stu-id="d75de-103">Unified Service Desk known issues and limitations</span></span>

::: moniker range="dynamics-usd-4"

## <a name="public-preview-unified-service-desk-41-known-issues-and-limitations"></a><span data-ttu-id="d75de-104">Public Preview: Unified Service Desk 4.1 known issues and limitations</span><span class="sxs-lookup"><span data-stu-id="d75de-104">Public Preview: Unified Service Desk 4.1 known issues and limitations</span></span>

### <a name="preview-edge-process"></a><span data-ttu-id="d75de-105">Preview: Edge process</span><span class="sxs-lookup"><span data-stu-id="d75de-105">Preview: Edge process</span></span>

#### <a name="support-for-closeandprompt-action-in-edge-process"></a><span data-ttu-id="d75de-106">Support for CloseAndPrompt action in Edge process</span><span class="sxs-lookup"><span data-stu-id="d75de-106">Support for CloseAndPrompt action in Edge process</span></span>

<span data-ttu-id="d75de-107">The Edge process does not support the **CloseAndPrompt** action for Dynamics 365 for Customer Engagement web client.</span><span class="sxs-lookup"><span data-stu-id="d75de-107">The Edge process does not support the **CloseAndPrompt** action for Dynamics 365 for Customer Engagement web client.</span></span> <span data-ttu-id="d75de-108">When you make changes in a webpage or a form on a web client, the process does not perform a dirty data check by prompting a dialog.</span><span class="sxs-lookup"><span data-stu-id="d75de-108">When you make changes in a webpage or a form on a web client, the process does not perform a dirty data check by prompting a dialog.</span></span> <span data-ttu-id="d75de-109">Instead, when you close the webpage or the form, Unified Service Desk closes the webpage or the form.</span><span class="sxs-lookup"><span data-stu-id="d75de-109">Instead, when you close the webpage or the form, Unified Service Desk closes the webpage or the form.</span></span>

#### <a name="support-for-alert-dialog-with-webview-control"></a><span data-ttu-id="d75de-110">Support for alert dialog with WebView control</span><span class="sxs-lookup"><span data-stu-id="d75de-110">Support for alert dialog with WebView control</span></span>

<span data-ttu-id="d75de-111">The Edge process doesn't support the native JavaScript alert dialog in the WebView control.</span><span class="sxs-lookup"><span data-stu-id="d75de-111">The Edge process doesn't support the native JavaScript alert dialog in the WebView control.</span></span> <span data-ttu-id="d75de-112">When you use the Microsoft Edge WebView control, the alert dialog (WPF message) shows the information.</span><span class="sxs-lookup"><span data-stu-id="d75de-112">When you use the Microsoft Edge WebView control, the alert dialog (WPF message) shows the information.</span></span> <span data-ttu-id="d75de-113">However, the alert does not stop the JavaScript execution.</span><span class="sxs-lookup"><span data-stu-id="d75de-113">However, the alert does not stop the JavaScript execution.</span></span> <span data-ttu-id="d75de-114">That is, even though you do not perform an action on the alert dialog, the JavaScript execution continues.</span><span class="sxs-lookup"><span data-stu-id="d75de-114">That is, even though you do not perform an action on the alert dialog, the JavaScript execution continues.</span></span>

#### <a name="support-for-confirm-dialog"></a><span data-ttu-id="d75de-115">Support for confirm dialog</span><span class="sxs-lookup"><span data-stu-id="d75de-115">Support for confirm dialog</span></span>

<span data-ttu-id="d75de-116">The Edge process doesn't support the confirm dialog in the WebView control.</span><span class="sxs-lookup"><span data-stu-id="d75de-116">The Edge process doesn't support the confirm dialog in the WebView control.</span></span> <span data-ttu-id="d75de-117">If your custom code uses the confirm dialog, the Edge process in the WebView control does not support the execution, and your code may fail.</span><span class="sxs-lookup"><span data-stu-id="d75de-117">If your custom code uses the confirm dialog, the Edge process in the WebView control does not support the execution, and your code may fail.</span></span>

#### <a name="support-for-multiple-page-navigation-in-edge-process"></a><span data-ttu-id="d75de-118">Support for multiple page navigation in Edge process</span><span class="sxs-lookup"><span data-stu-id="d75de-118">Support for multiple page navigation in Edge process</span></span>

<span data-ttu-id="d75de-119">The Edge process WebView control doesn't support multiple-page navigation for the hosted control.</span><span class="sxs-lookup"><span data-stu-id="d75de-119">The Edge process WebView control doesn't support multiple-page navigation for the hosted control.</span></span> <span data-ttu-id="d75de-120">During the hosted control creation, setting the option **Allow Multiple Pages** to **True** with more than one URL does not perform the navigation in the Unified Service Desk client application at run-time.</span><span class="sxs-lookup"><span data-stu-id="d75de-120">During the hosted control creation, setting the option **Allow Multiple Pages** to **True** with more than one URL does not perform the navigation in the Unified Service Desk client application at run-time.</span></span> <span data-ttu-id="d75de-121">That is, the navigation to first URL will happen and the page renders.</span><span class="sxs-lookup"><span data-stu-id="d75de-121">That is, the navigation to first URL will happen and the page renders.</span></span> <span data-ttu-id="d75de-122">However, the navigation to the second URL will not be executed and the webpage will not render the second URL.</span><span class="sxs-lookup"><span data-stu-id="d75de-122">However, the navigation to the second URL will not be executed and the webpage will not render the second URL.</span></span>

#### <a name="use-windowtopnotifyusd-to-open-event-in-a-new-browser"></a><span data-ttu-id="d75de-123">Use window.top.notifyUSD to open event in a new browser</span><span class="sxs-lookup"><span data-stu-id="d75de-123">Use window.top.notifyUSD to open event in a new browser</span></span>

<span data-ttu-id="d75de-124">The Edge process WebView control supports using `window.top.notifyUSD` to open the event in a new browser instead of `window.open`.</span><span class="sxs-lookup"><span data-stu-id="d75de-124">The Edge process WebView control supports using `window.top.notifyUSD` to open the event in a new browser instead of `window.open`.</span></span>

#### <a name="using-a-long-running-script-with-edge-process-freezes-unified-service-desk"></a><span data-ttu-id="d75de-125">Using a long-running script with Edge process freezes Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="d75de-125">Using a long-running script with Edge process freezes Unified Service Desk</span></span>

<span data-ttu-id="d75de-126">When you execute a long-running script with edge process, the Unified Service Desk client application freezes, and you must restart the client application.</span><span class="sxs-lookup"><span data-stu-id="d75de-126">When you execute a long-running script with edge process, the Unified Service Desk client application freezes, and you must restart the client application.</span></span> <span data-ttu-id="d75de-127">We recommend that you review the script that caused the freeze, and then restart the Unified Service Desk client application.</span><span class="sxs-lookup"><span data-stu-id="d75de-127">We recommend that you review the script that caused the freeze, and then restart the Unified Service Desk client application.</span></span>

#### <a name="support-for-downloading-files-with-edge-process"></a><span data-ttu-id="d75de-128">Support for downloading files with Edge process</span><span class="sxs-lookup"><span data-stu-id="d75de-128">Support for downloading files with Edge process</span></span>

<span data-ttu-id="d75de-129">When you host your web pages in a Unified Service Desk client application using Edge process, downloading files from the web application is not supported with Edge process.</span><span class="sxs-lookup"><span data-stu-id="d75de-129">When you host your web pages in a Unified Service Desk client application using Edge process, downloading files from the web application is not supported with Edge process.</span></span>

<span data-ttu-id="d75de-130">A workaround is to open the Microsoft Edge browser separately, navigate to the website URL and download the file.</span><span class="sxs-lookup"><span data-stu-id="d75de-130">A workaround is to open the Microsoft Edge browser separately, navigate to the website URL and download the file.</span></span>

#### <a name="support-for-launching-application-for-a-uri-with-edge-webview-control"></a><span data-ttu-id="d75de-131">Support for launching application for a URI with Edge WebView control</span><span class="sxs-lookup"><span data-stu-id="d75de-131">Support for launching application for a URI with Edge WebView control</span></span>

<span data-ttu-id="d75de-132">When you host your web application in Unified Service Desk client application using Edge process, launching application for a URI is not supported with Edge process.</span><span class="sxs-lookup"><span data-stu-id="d75de-132">When you host your web application in Unified Service Desk client application using Edge process, launching application for a URI is not supported with Edge process.</span></span>

<span data-ttu-id="d75de-133">Some of the URI schemes and applications are as follows:</span><span class="sxs-lookup"><span data-stu-id="d75de-133">Some of the URI schemes and applications are as follows:</span></span>

| <span data-ttu-id="d75de-134">URI Scheme</span><span class="sxs-lookup"><span data-stu-id="d75de-134">URI Scheme</span></span> | <span data-ttu-id="d75de-135">Launches</span><span class="sxs-lookup"><span data-stu-id="d75de-135">Launches</span></span> |
| ----------:|----------|
|<span data-ttu-id="d75de-136">bingmaps</span><span class="sxs-lookup"><span data-stu-id="d75de-136">bingmaps</span></span> | <span data-ttu-id="d75de-137">Maps app</span><span class="sxs-lookup"><span data-stu-id="d75de-137">Maps app</span></span> |
|<span data-ttu-id="d75de-138">mailto:</span><span class="sxs-lookup"><span data-stu-id="d75de-138">mailto:</span></span> | <span data-ttu-id="d75de-139">Default email app</span><span class="sxs-lookup"><span data-stu-id="d75de-139">Default email app</span></span> |
|<span data-ttu-id="d75de-140">ms-call:</span><span class="sxs-lookup"><span data-stu-id="d75de-140">ms-call:</span></span>|  <span data-ttu-id="d75de-141">Call app</span><span class="sxs-lookup"><span data-stu-id="d75de-141">Call app</span></span> |
|<span data-ttu-id="d75de-142">ms-chat:</span><span class="sxs-lookup"><span data-stu-id="d75de-142">ms-chat:</span></span> | <span data-ttu-id="d75de-143">Messaging app</span><span class="sxs-lookup"><span data-stu-id="d75de-143">Messaging app</span></span> |

<span data-ttu-id="d75de-144">A workaround is to open the Edge browser separately, navigate to the website URL and select the URI scheme to launch the application.</span><span class="sxs-lookup"><span data-stu-id="d75de-144">A workaround is to open the Edge browser separately, navigate to the website URL and select the URI scheme to launch the application.</span></span>

#### <a name="kb-article-support-with-edge-process"></a><span data-ttu-id="d75de-145">KB article support with Edge process</span><span class="sxs-lookup"><span data-stu-id="d75de-145">KB article support with Edge process</span></span>

<span data-ttu-id="d75de-146">In Dynamics 365 Customer Engagement apps web client, when you host the KB article in Unified Service Desk client application using Edge Process, the KB articles does not render.</span><span class="sxs-lookup"><span data-stu-id="d75de-146">In Dynamics 365 Customer Engagement apps web client, when you host the KB article in Unified Service Desk client application using Edge Process, the KB articles does not render.</span></span> 

<span data-ttu-id="d75de-147">A workaround is to change the **Unified Service Desk Component Type** of the **KB Article** hosted control from **CRM Page** to **Unified Interface Page**.</span><span class="sxs-lookup"><span data-stu-id="d75de-147">A workaround is to change the **Unified Service Desk Component Type** of the **KB Article** hosted control from **CRM Page** to **Unified Interface Page**.</span></span>

<span data-ttu-id="d75de-148">After chaning the component type, go to the action call for opening the KM, and in the **Data** field you can see the parameters like **url**, **postdata**, and **header**.</span><span class="sxs-lookup"><span data-stu-id="d75de-148">After chaning the component type, go to the action call for opening the KM, and in the **Data** field you can see the parameters like **url**, **postdata**, and **header**.</span></span>

<span data-ttu-id="d75de-149">![Action call with the postdata and header parameter](media/manual-update-unified-interface-km-control-action-call-data.PNG "Action call with the postdata and header parameter")</span><span class="sxs-lookup"><span data-stu-id="d75de-149">![Action call with the postdata and header parameter](media/manual-update-unified-interface-km-control-action-call-data.PNG "Action call with the postdata and header parameter")</span></span>

<span data-ttu-id="d75de-150">Remove the following values from the data field:</span><span class="sxs-lookup"><span data-stu-id="d75de-150">Remove the following values from the data field:</span></span>

`postdata=[[postdata]]`

`header=[[header]+]` 

<span data-ttu-id="d75de-151">To open an KB article, only the article url is sufficient.</span><span class="sxs-lookup"><span data-stu-id="d75de-151">To open an KB article, only the article url is sufficient.</span></span> <span data-ttu-id="d75de-152">Ví dụ: `url=[[KB Search.articleurl]g]`</span><span class="sxs-lookup"><span data-stu-id="d75de-152">For example: `url=[[KB Search.articleurl]g]`</span></span>

<span data-ttu-id="d75de-153">Now, save the configuration.</span><span class="sxs-lookup"><span data-stu-id="d75de-153">Now, save the configuration.</span></span> <span data-ttu-id="d75de-154">Login to Unified Service Desk and open any article to see the article contents.</span><span class="sxs-lookup"><span data-stu-id="d75de-154">Login to Unified Service Desk and open any article to see the article contents.</span></span>

## <a name="unified-service-desk-40-known-issues-and-limitations"></a><span data-ttu-id="d75de-155">Unified Service Desk 4.0 known issues and limitations</span><span class="sxs-lookup"><span data-stu-id="d75de-155">Unified Service Desk 4.0 known issues and limitations</span></span>

### <a name="select-articles-from-the-unified-interface-kb-control-in-the-unified-service-desk-displays-error"></a><span data-ttu-id="d75de-156">Select articles from the Unified Interface KB Control in the Unified Service Desk displays error</span><span class="sxs-lookup"><span data-stu-id="d75de-156">Select articles from the Unified Interface KB Control in the Unified Service Desk displays error</span></span>

<span data-ttu-id="d75de-157">If you are using **Web client - Unified Interface Migration Assistant** to migrate your Unified Service Desk Configurations from Dynamics 365 for Customer Engagement apps Web Client to Dynamics 365 for Customer Engagement apps Unified Interface, the KM Control is changed to Unified Interface KM Control.</span><span class="sxs-lookup"><span data-stu-id="d75de-157">If you are using **Web client - Unified Interface Migration Assistant** to migrate your Unified Service Desk Configurations from Dynamics 365 for Customer Engagement apps Web Client to Dynamics 365 for Customer Engagement apps Unified Interface, the KM Control is changed to Unified Interface KM Control.</span></span>

<span data-ttu-id="d75de-158">With the Unified Interface KM Control hosted control, if you login to Unified Service Desk and open any KB article, you can see server error.</span><span class="sxs-lookup"><span data-stu-id="d75de-158">With the Unified Interface KM Control hosted control, if you login to Unified Service Desk and open any KB article, you can see server error.</span></span>

<span data-ttu-id="d75de-159">![Opening article displays server error](media/kb-search-server-error.PNG "Opening article displays server error")</span><span class="sxs-lookup"><span data-stu-id="d75de-159">![Opening article displays server error](media/kb-search-server-error.PNG "Opening article displays server error")</span></span>

#### <a name="workaround"></a><span data-ttu-id="d75de-160">Giải pháp thay thế</span><span class="sxs-lookup"><span data-stu-id="d75de-160">Workaround</span></span>

<span data-ttu-id="d75de-161">To fix the issue, you must manually update the data parameter for the Unified Interface KM Control action call.</span><span class="sxs-lookup"><span data-stu-id="d75de-161">To fix the issue, you must manually update the data parameter for the Unified Interface KM Control action call.</span></span>

<span data-ttu-id="d75de-162">In the Dynamics 365 Web Client configurations, go to the action call for opening the KM, and in the **Data** field you can see the parameters like **url**, **postdata**, and **header**.</span><span class="sxs-lookup"><span data-stu-id="d75de-162">In the Dynamics 365 Web Client configurations, go to the action call for opening the KM, and in the **Data** field you can see the parameters like **url**, **postdata**, and **header**.</span></span>

<span data-ttu-id="d75de-163">![Action call with the postdata and header parameter](media/manual-update-unified-interface-km-control-action-call-data.PNG "Action call with the postdata and header parameter")</span><span class="sxs-lookup"><span data-stu-id="d75de-163">![Action call with the postdata and header parameter](media/manual-update-unified-interface-km-control-action-call-data.PNG "Action call with the postdata and header parameter")</span></span>

<span data-ttu-id="d75de-164">Remove the following values from the data field:</span><span class="sxs-lookup"><span data-stu-id="d75de-164">Remove the following values from the data field:</span></span>

`postdata=[[postdata]]`

`header=[[header]+]` 

<span data-ttu-id="d75de-165">To open an KB article, only the article url is sufficient.</span><span class="sxs-lookup"><span data-stu-id="d75de-165">To open an KB article, only the article url is sufficient.</span></span> <span data-ttu-id="d75de-166">Ví dụ: `url=[[KB Search.articleurl]g]`</span><span class="sxs-lookup"><span data-stu-id="d75de-166">For example: `url=[[KB Search.articleurl]g]`</span></span>

<span data-ttu-id="d75de-167">Now, save the configuration.</span><span class="sxs-lookup"><span data-stu-id="d75de-167">Now, save the configuration.</span></span> <span data-ttu-id="d75de-168">Login to Unified Service Desk and open any article to see the article contents.</span><span class="sxs-lookup"><span data-stu-id="d75de-168">Login to Unified Service Desk and open any article to see the article contents.</span></span>

<span data-ttu-id="d75de-169">![Remove the header and postdata parameter to see the article contents](media/kb-search-fix.PNG "Remove the header and postdata parameter to see the article contents")</span><span class="sxs-lookup"><span data-stu-id="d75de-169">![Remove the header and postdata parameter to see the article contents](media/kb-search-fix.PNG "Remove the header and postdata parameter to see the article contents")</span></span>


### <a name="toolbar-shows-unified-blue-theme-instead-air-theme"></a><span data-ttu-id="d75de-170">Toolbar shows Unified Blue theme instead Air theme</span><span class="sxs-lookup"><span data-stu-id="d75de-170">Toolbar shows Unified Blue theme instead Air theme</span></span>

<span data-ttu-id="d75de-171">In the **Unified Interface Settings** record, select **Air** theme instead **Unified Blue** theme, and select an Unified Interface App.</span><span class="sxs-lookup"><span data-stu-id="d75de-171">In the **Unified Interface Settings** record, select **Air** theme instead **Unified Blue** theme, and select an Unified Interface App.</span></span> 

<span data-ttu-id="d75de-172">![Air theme is set in the Unified Interface Settings record](media/usd-crm-unified-interface-air-theme.png "Air theme is set in the Unified Interface Settings record")</span><span class="sxs-lookup"><span data-stu-id="d75de-172">![Air theme is set in the Unified Interface Settings record](media/usd-crm-unified-interface-air-theme.png "Air theme is set in the Unified Interface Settings record")</span></span>

<span data-ttu-id="d75de-173">Now, if you login to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], the **About Tool Bar** and **Main** toolbar chooses to show **Unified Blue** theme colors instead **Air** theme.</span><span class="sxs-lookup"><span data-stu-id="d75de-173">Now, if you login to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], the **About Tool Bar** and **Main** toolbar chooses to show **Unified Blue** theme colors instead **Air** theme.</span></span>

<span data-ttu-id="d75de-174">![The main and about toolbar shows Unified Interface theme colors instead Air theme colors](media/about-toolbar-main-toolbar-known-issue.png "The main and about toolbar shows Unified Interface theme colors instead Air theme colors")</span><span class="sxs-lookup"><span data-stu-id="d75de-174">![The main and about toolbar shows Unified Interface theme colors instead Air theme colors](media/about-toolbar-main-toolbar-known-issue.png "The main and about toolbar shows Unified Interface theme colors instead Air theme colors")</span></span>

#### <a name="workaround"></a><span data-ttu-id="d75de-175">Giải pháp thay thế</span><span class="sxs-lookup"><span data-stu-id="d75de-175">Workaround</span></span>

<span data-ttu-id="d75de-176">Remove the **Custom Styles** XAML from the **About Tool Bar** and **Main** toolbar so that toolbar picks the **Air** theme colors.</span><span class="sxs-lookup"><span data-stu-id="d75de-176">Remove the **Custom Styles** XAML from the **About Tool Bar** and **Main** toolbar so that toolbar picks the **Air** theme colors.</span></span>

1. <span data-ttu-id="d75de-177">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="d75de-177">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>

2. <span data-ttu-id="d75de-178">Go to **Settings** > **My Apps** > **Unified Service Desk Administrator** app.</span><span class="sxs-lookup"><span data-stu-id="d75de-178">Go to **Settings** > **My Apps** > **Unified Service Desk Administrator** app.</span></span><br>

3. <span data-ttu-id="d75de-179">Select **Site Map**.</span><span class="sxs-lookup"><span data-stu-id="d75de-179">Select **Site Map**.</span></span></br>
<span data-ttu-id="d75de-180">![Select Site Map to go to Unified Interface Settings](media/usd-crm-site-map-unified-interface-setting.PNG "Select Site Map to go to Unified Interface Settings")</span><span class="sxs-lookup"><span data-stu-id="d75de-180">![Select Site Map to go to Unified Interface Settings](media/usd-crm-site-map-unified-interface-setting.PNG "Select Site Map to go to Unified Interface Settings")</span></span>

4. <span data-ttu-id="d75de-181">Choose **Toolbars** under the **Basic Settings**.</span><span class="sxs-lookup"><span data-stu-id="d75de-181">Choose **Toolbars** under the **Basic Settings**.</span></span>

5. <span data-ttu-id="d75de-182">Select **About Tool Bar** from the list.</span><span class="sxs-lookup"><span data-stu-id="d75de-182">Select **About Tool Bar** from the list.</span></span>

6. <span data-ttu-id="d75de-183">Choose the **Styles** tab.</span><span class="sxs-lookup"><span data-stu-id="d75de-183">Choose the **Styles** tab.</span></span>

7. <span data-ttu-id="d75de-184">Remove the content in the **Custom Styles** field.</span><span class="sxs-lookup"><span data-stu-id="d75de-184">Remove the content in the **Custom Styles** field.</span></span>

8. <span data-ttu-id="d75de-185">Select **Save** to save the settings.</span><span class="sxs-lookup"><span data-stu-id="d75de-185">Select **Save** to save the settings.</span></span> 

<span data-ttu-id="d75de-186">Repeat the steps 5-8 for the **Main** toolbar.</span><span class="sxs-lookup"><span data-stu-id="d75de-186">Repeat the steps 5-8 for the **Main** toolbar.</span></span>

<span data-ttu-id="d75de-187">Login to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] and toolbar chooses **Air** theme colors.</span><span class="sxs-lookup"><span data-stu-id="d75de-187">Login to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] and toolbar chooses **Air** theme colors.</span></span>

<span data-ttu-id="d75de-188">![The main and about toolbar shows Air theme colors](media/about-toolbar-main-toolbar-known-issue-fixed-toolbar.png "The main and about toolbar shows Air theme colors")</span><span class="sxs-lookup"><span data-stu-id="d75de-188">![The main and about toolbar shows Air theme colors](media/about-toolbar-main-toolbar-known-issue-fixed-toolbar.png "The main and about toolbar shows Air theme colors")</span></span>

### <a name="unified-interface-form-does-not-close-the-tab-and-navigates-to-dashboard"></a><span data-ttu-id="d75de-189">Unified Interface form does not close the tab and navigates to Dashboard</span><span class="sxs-lookup"><span data-stu-id="d75de-189">Unified Interface form does not close the tab and navigates to Dashboard</span></span>

<span data-ttu-id="d75de-190">Go to **Settings** > **Administration** > **System Settings** and set the **Enable auto save on all forms** to **No** in Dynamics 365 for Customer Engagement apps Unified Interface.</span><span class="sxs-lookup"><span data-stu-id="d75de-190">Go to **Settings** > **Administration** > **System Settings** and set the **Enable auto save on all forms** to **No** in Dynamics 365 for Customer Engagement apps Unified Interface.</span></span> 

<span data-ttu-id="d75de-191">![Disable autosave in Unified Interface forms](media/crm-unified-interface-disable-autosave.png "Disable autosave in Unified Interface forms")</span><span class="sxs-lookup"><span data-stu-id="d75de-191">![Disable autosave in Unified Interface forms](media/crm-unified-interface-disable-autosave.png "Disable autosave in Unified Interface forms")</span></span>

<span data-ttu-id="d75de-192">Now, login to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], and open any Unified Interface page.</span><span class="sxs-lookup"><span data-stu-id="d75de-192">Now, login to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], and open any Unified Interface page.</span></span> <span data-ttu-id="d75de-193">For example, open a case.</span><span class="sxs-lookup"><span data-stu-id="d75de-193">For example, open a case.</span></span> <span data-ttu-id="d75de-194">After completing your work on the case, if you select **Save & Close** on the Unified Interface page (form), the form saves and closes.</span><span class="sxs-lookup"><span data-stu-id="d75de-194">After completing your work on the case, if you select **Save & Close** on the Unified Interface page (form), the form saves and closes.</span></span>

<span data-ttu-id="d75de-195">![Select Save & Close on Unified Interface forms](media/usd-crm-saveclose.png "Select Save & Close on Unified Interface forms")</span><span class="sxs-lookup"><span data-stu-id="d75de-195">![Select Save & Close on Unified Interface forms](media/usd-crm-saveclose.png "Select Save & Close on Unified Interface forms")</span></span>

<span data-ttu-id="d75de-196">However, the tab does not close, and the Unified Interface page (form) navigates to **Dashboard** page.</span><span class="sxs-lookup"><span data-stu-id="d75de-196">However, the tab does not close, and the Unified Interface page (form) navigates to **Dashboard** page.</span></span>

<span data-ttu-id="d75de-197">![Unified Interface page navigates to Dashboard page](media/usd-crm-page-navigates-dashboard.png "Unified Interface page navigates to Dashboard page")</span><span class="sxs-lookup"><span data-stu-id="d75de-197">![Unified Interface page navigates to Dashboard page](media/usd-crm-page-navigates-dashboard.png "Unified Interface page navigates to Dashboard page")</span></span>

#### <a name="workaround"></a><span data-ttu-id="d75de-198">Giải pháp thay thế</span><span class="sxs-lookup"><span data-stu-id="d75de-198">Workaround</span></span>

<span data-ttu-id="d75de-199">To close the tab, you need to select **User Can Close** in the hosted control so that you see **X** button the tab in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="d75de-199">To close the tab, you need to select **User Can Close** in the hosted control so that you see **X** button the tab in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> 

<span data-ttu-id="d75de-200">![Set user can close option in the hosted control](media/usd-crm-usercanclose-option.png "Set user can close option in the hosted control")</span><span class="sxs-lookup"><span data-stu-id="d75de-200">![Set user can close option in the hosted control](media/usd-crm-usercanclose-option.png "Set user can close option in the hosted control")</span></span>

<span data-ttu-id="d75de-201">Now, login to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], and open the case.</span><span class="sxs-lookup"><span data-stu-id="d75de-201">Now, login to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], and open the case.</span></span> <span data-ttu-id="d75de-202">Now, select **Save & Close** on the Unified Interface page (form), the form saves and closes.</span><span class="sxs-lookup"><span data-stu-id="d75de-202">Now, select **Save & Close** on the Unified Interface page (form), the form saves and closes.</span></span> <span data-ttu-id="d75de-203">The page navigates to the **Dashboard** page.</span><span class="sxs-lookup"><span data-stu-id="d75de-203">The page navigates to the **Dashboard** page.</span></span> <span data-ttu-id="d75de-204">To close the tab, you can select the **X** button.</span><span class="sxs-lookup"><span data-stu-id="d75de-204">To close the tab, you can select the **X** button.</span></span>

<span data-ttu-id="d75de-205">![Select close button to close the tab](media/usd-crm-close-button-saveclose.png "Select close button to close the tab")</span><span class="sxs-lookup"><span data-stu-id="d75de-205">![Select close button to close the tab](media/usd-crm-close-button-saveclose.png "Select close button to close the tab")</span></span>

### <a name="sub-actions-calls-is-not-available-in-unified-service-desk-administrator-app"></a><span data-ttu-id="d75de-206">Sub Actions Calls is not available in Unified Service Desk Administrator app</span><span class="sxs-lookup"><span data-stu-id="d75de-206">Sub Actions Calls is not available in Unified Service Desk Administrator app</span></span>

<span data-ttu-id="d75de-207">You cannot view and attach an action call to another call (sub-action call) in Unified Service Desk Administrator app as the **Action Calls** in Unified Service Desk Administrator app does not display the **Sub Action Calls** option in the related tab. .</span><span class="sxs-lookup"><span data-stu-id="d75de-207">You cannot view and attach an action call to another call (sub-action call) in Unified Service Desk Administrator app as the **Action Calls** in Unified Service Desk Administrator app does not display the **Sub Action Calls** option in the related tab. .</span></span>

#### <a name="workaround"></a><span data-ttu-id="d75de-208">Giải pháp thay thế</span><span class="sxs-lookup"><span data-stu-id="d75de-208">Workaround</span></span>

<span data-ttu-id="d75de-209">You can add an action call to another call using the Unified Service Desk configurations in Dynamics 365 for Customer Engagement apps Web Client.</span><span class="sxs-lookup"><span data-stu-id="d75de-209">You can add an action call to another call using the Unified Service Desk configurations in Dynamics 365 for Customer Engagement apps Web Client.</span></span> 

### <a name="support-for-relevance-search-search-technique-in-unified-interface-km-control"></a><span data-ttu-id="d75de-210">Support for Relevance Search (search technique) in Unified Interface KM Control</span><span class="sxs-lookup"><span data-stu-id="d75de-210">Support for Relevance Search (search technique) in Unified Interface KM Control</span></span>

<span data-ttu-id="d75de-211">The Unified Interface KM Control supports [Full-Text search](https://docs.microsoft.com/en-us/sql/relational-databases/search/full-text-search?view=sql-server-2017) technique in Dynamics 365 for Customer Engagement apps and does not support the **Relevance Search**.</span><span class="sxs-lookup"><span data-stu-id="d75de-211">The Unified Interface KM Control supports [Full-Text search](https://docs.microsoft.com/en-us/sql/relational-databases/search/full-text-search?view=sql-server-2017) technique in Dynamics 365 for Customer Engagement apps and does not support the **Relevance Search**.</span></span> <span data-ttu-id="d75de-212">For more information about the availability of the Relevance Search, see [Relevance search for knowledge management](https://docs.microsoft.com/en-us/business-applications-release-notes/October18/service/customer-service-core-release-notes/relevance-search-for-knowledge-management).</span><span class="sxs-lookup"><span data-stu-id="d75de-212">For more information about the availability of the Relevance Search, see [Relevance search for knowledge management](https://docs.microsoft.com/en-us/business-applications-release-notes/October18/service/customer-service-core-release-notes/relevance-search-for-knowledge-management).</span></span>

### <a name="quick-create-in-unified-service-administrator-app"></a><span data-ttu-id="d75de-213">Quick create in Unified Service Administrator app</span><span class="sxs-lookup"><span data-stu-id="d75de-213">Quick create in Unified Service Administrator app</span></span>

<span data-ttu-id="d75de-214">Selecting the **New** button (quick create)  in the **Navigation** toolbar of the Unified Service Desk Administraor app does not display any option to create.</span><span class="sxs-lookup"><span data-stu-id="d75de-214">Selecting the **New** button (quick create)  in the **Navigation** toolbar of the Unified Service Desk Administraor app does not display any option to create.</span></span>

<span data-ttu-id="d75de-215">![Quick create option in the Navigation toolbar](media/usd-crm-quick-create-button.PNG "Quick create option in the Navigation toolbar")</span><span class="sxs-lookup"><span data-stu-id="d75de-215">![Quick create option in the Navigation toolbar](media/usd-crm-quick-create-button.PNG "Quick create option in the Navigation toolbar")</span></span>

### <a name="navigation-and-command-bar-configuration-does-not-execute-when-internet-explorer-pooling-is-enabled"></a><span data-ttu-id="d75de-216">Navigation and command bar configuration does not execute when Internet Explorer pooling is enabled</span><span class="sxs-lookup"><span data-stu-id="d75de-216">Navigation and command bar configuration does not execute when Internet Explorer pooling is enabled</span></span>

<span data-ttu-id="d75de-217">By default, when you a open Dynamics 365 for Customer Engagement apps page in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, the navigation bar is hidden and command bar is displayed.</span><span class="sxs-lookup"><span data-stu-id="d75de-217">By default, when you a open Dynamics 365 for Customer Engagement apps page in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, the navigation bar is hidden and command bar is displayed.</span></span> 

<span data-ttu-id="d75de-218">However, when you enable Internet Explorer pooling and change the configurations in Dynamics 365 for Customer Engagement apps to hide the command bar and display the navigation bar, the Dynamics 365 for Customer Engagement apps page in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application does hide the command bar and display the navigation bar.</span><span class="sxs-lookup"><span data-stu-id="d75de-218">However, when you enable Internet Explorer pooling and change the configurations in Dynamics 365 for Customer Engagement apps to hide the command bar and display the navigation bar, the Dynamics 365 for Customer Engagement apps page in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application does hide the command bar and display the navigation bar.</span></span>

<span data-ttu-id="d75de-219">To execute the configuration, disable the Internet Explorer pooling.</span><span class="sxs-lookup"><span data-stu-id="d75de-219">To execute the configuration, disable the Internet Explorer pooling.</span></span>

## <a name="see-also"></a><span data-ttu-id="d75de-220">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="d75de-220">See Also</span></span>

[<span data-ttu-id="d75de-221">Unified Interface KM Control (hosted control)</span><span class="sxs-lookup"><span data-stu-id="d75de-221">Unified Interface KM Control (hosted control)</span></span>](unified-interface-km-control-hosted-control.md)

::: moniker-end

::: moniker range="dynamics-usd-3"

## <a name="unified-service-desk-33-known-issues-and-limitations"></a><span data-ttu-id="d75de-222">Unified Service Desk 3.3 known issues and limitations</span><span class="sxs-lookup"><span data-stu-id="d75de-222">Unified Service Desk 3.3 known issues and limitations</span></span>

<span data-ttu-id="d75de-223">This section describes the known issues and limitations in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]</span><span class="sxs-lookup"><span data-stu-id="d75de-223">This section describes the known issues and limitations in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]</span></span>

### <a name="best-practices-analyzer"></a><span data-ttu-id="d75de-224">Best Practices Analyzer</span><span class="sxs-lookup"><span data-stu-id="d75de-224">Best Practices Analyzer</span></span>

- <span data-ttu-id="d75de-225">**Warning for HelpImproveUSD parameter in Dynamics 365 for Customer Engagement (on-premises) apps**</span><span class="sxs-lookup"><span data-stu-id="d75de-225">**Warning for HelpImproveUSD parameter in Dynamics 365 for Customer Engagement (on-premises) apps**</span></span>

  <span data-ttu-id="d75de-226">Help Improve [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] is enabled/disabled only for [!INCLUDE[pn-crm-online](../includes/pn-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="d75de-226">Help Improve [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] is enabled/disabled only for [!INCLUDE[pn-crm-online](../includes/pn-crm-online.md)].</span></span> <span data-ttu-id="d75de-227">If you are using [!INCLUDE[pn-crm-onprem](../includes/pn-crm-onprem.md)] apps, you can see a warning for the Help Improve [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] (HelpImproveUSD) parameter in the report.</span><span class="sxs-lookup"><span data-stu-id="d75de-227">If you are using [!INCLUDE[pn-crm-onprem](../includes/pn-crm-onprem.md)] apps, you can see a warning for the Help Improve [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] (HelpImproveUSD) parameter in the report.</span></span>

- <span data-ttu-id="d75de-228">**Error for Enable Enhanced Protected mode in Windows 7 operating system**</span><span class="sxs-lookup"><span data-stu-id="d75de-228">**Error for Enable Enhanced Protected mode in Windows 7 operating system**</span></span>

  <span data-ttu-id="d75de-229">If you are using [!include[pn-windows-7](../includes/pn-windows-7.md)] operating system, the **Enable Enhanced Protected Mode** option is not available in Internet Explorer options.</span><span class="sxs-lookup"><span data-stu-id="d75de-229">If you are using [!include[pn-windows-7](../includes/pn-windows-7.md)] operating system, the **Enable Enhanced Protected Mode** option is not available in Internet Explorer options.</span></span> <span data-ttu-id="d75de-230">Hence, you can see an error message for the **Enable Enhanced Protected Mode** parameter in the report.</span><span class="sxs-lookup"><span data-stu-id="d75de-230">Hence, you can see an error message for the **Enable Enhanced Protected Mode** parameter in the report.</span></span>

### <a name="provide-feedback"></a><span data-ttu-id="d75de-231">Provide Feedback</span><span class="sxs-lookup"><span data-stu-id="d75de-231">Provide Feedback</span></span>

- <span data-ttu-id="d75de-232">**Insufficient permissions to provide feedback**</span><span class="sxs-lookup"><span data-stu-id="d75de-232">**Insufficient permissions to provide feedback**</span></span>

  <span data-ttu-id="d75de-233">The **Provide Feedback** feature is available only if you have a [!INCLUDE[pn-crm-online](../includes/pn-crm-online.md)] apps instance.</span><span class="sxs-lookup"><span data-stu-id="d75de-233">The **Provide Feedback** feature is available only if you have a [!INCLUDE[pn-crm-online](../includes/pn-crm-online.md)] apps instance.</span></span>

  <span data-ttu-id="d75de-234">If you log in using administrator credentials and select **Provide Feedback** to provide your feedback/comments, you can see an **Insufficient Permissions** message.</span><span class="sxs-lookup"><span data-stu-id="d75de-234">If you log in using administrator credentials and select **Provide Feedback** to provide your feedback/comments, you can see an **Insufficient Permissions** message.</span></span> 

  <span data-ttu-id="d75de-235">![Insufficient Permissions](media/insufficient-permissions-provide-feedback-window.PNG "Insufficient Permissions")</span><span class="sxs-lookup"><span data-stu-id="d75de-235">![Insufficient Permissions](media/insufficient-permissions-provide-feedback-window.PNG "Insufficient Permissions")</span></span>

  <span data-ttu-id="d75de-236">The message says to contact the administrator even though you log in as an administrator.</span><span class="sxs-lookup"><span data-stu-id="d75de-236">The message says to contact the administrator even though you log in as an administrator.</span></span> <span data-ttu-id="d75de-237">The reason for this message is that you did not enable the **HelpImproveUsd** option in the UII global options.</span><span class="sxs-lookup"><span data-stu-id="d75de-237">The reason for this message is that you did not enable the **HelpImproveUsd** option in the UII global options.</span></span>

  <span data-ttu-id="d75de-238">If you enable **HelpImproveUsd**, the data collection is enabled, and in turn, you (agent and administrator) can provide feedback to improve the product.</span><span class="sxs-lookup"><span data-stu-id="d75de-238">If you enable **HelpImproveUsd**, the data collection is enabled, and in turn, you (agent and administrator) can provide feedback to improve the product.</span></span>

  <span data-ttu-id="d75de-239">To enable **HelpImproveUsd**, view [Help improve Unified Service Desk](admin/help-improve-unified-service-desk.md).</span><span class="sxs-lookup"><span data-stu-id="d75de-239">To enable **HelpImproveUsd**, view [Help improve Unified Service Desk](admin/help-improve-unified-service-desk.md).</span></span>

<span data-ttu-id="d75de-240">This section describes the limitations in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]</span><span class="sxs-lookup"><span data-stu-id="d75de-240">This section describes the limitations in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]</span></span>

### <a name="runscript"></a><span data-ttu-id="d75de-241">Chạy mã lệnh</span><span class="sxs-lookup"><span data-stu-id="d75de-241">RunScript</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d75de-242">This also applies to:</span><span class="sxs-lookup"><span data-stu-id="d75de-242">This also applies to:</span></span>
> - [!INCLUDE[pn-unified-service-desk-3-2](../includes/pn-unified-service-desk-3-2.md)]
> - [!INCLUDE[pn-unified-service-desk-3-1](../includes/pn-unified-service-desk-3-1.md)]
> - [!INCLUDE[pn-unified-service-desk-3-0](../includes/pn-unified-service-desk-3-0.md)]
> - [!INCLUDE[pn-unified-service-desk-2-2](../includes/pn-unified-service-desk-2-2.md)]

<span data-ttu-id="d75de-243">**RunScript action does not execute if the tab or page is not in focus**</span><span class="sxs-lookup"><span data-stu-id="d75de-243">**RunScript action does not execute if the tab or page is not in focus**</span></span>

<span data-ttu-id="d75de-244">If you execute a RunScript action on a tab or a page that is not in focus, the execution of RunScript action does not execute the script.</span><span class="sxs-lookup"><span data-stu-id="d75de-244">If you execute a RunScript action on a tab or a page that is not in focus, the execution of RunScript action does not execute the script.</span></span>

<span data-ttu-id="d75de-245">**Ví dụ:**</span><span class="sxs-lookup"><span data-stu-id="d75de-245">**Example:**</span></span>

<span data-ttu-id="d75de-246">Accounts and Contacts tabs are open and focus is on Accounts tab. You execute `window.close()` RunScript command to close the Contacts tab. Since, the focus is on Accounts tab the RunScript execution does not execute and the Contacts tab does not close.</span><span class="sxs-lookup"><span data-stu-id="d75de-246">Accounts and Contacts tabs are open and focus is on Accounts tab. You execute `window.close()` RunScript command to close the Contacts tab. Since, the focus is on Accounts tab the RunScript execution does not execute and the Contacts tab does not close.</span></span>

<span data-ttu-id="d75de-247">**Workaround:**</span><span class="sxs-lookup"><span data-stu-id="d75de-247">**Workaround:**</span></span>

<span data-ttu-id="d75de-248">If you open several tabs and want to execute a RunScript action on a tab that is not in focus, set the focus on the tab you want to work and then execute the RunScript action.</span><span class="sxs-lookup"><span data-stu-id="d75de-248">If you open several tabs and want to execute a RunScript action on a tab that is not in focus, set the focus on the tab you want to work and then execute the RunScript action.</span></span>

### <a name="performance-enhancement-for-crm-entity-page-loads"></a><span data-ttu-id="d75de-249">Performance enhancement for CRM entity page loads</span><span class="sxs-lookup"><span data-stu-id="d75de-249">Performance enhancement for CRM entity page loads</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d75de-250">This also applies to:</span><span class="sxs-lookup"><span data-stu-id="d75de-250">This also applies to:</span></span>
> - [!INCLUDE[pn-unified-service-desk-3-2](../includes/pn-unified-service-desk-3-2.md)]

<span data-ttu-id="d75de-251">**Closing CRM entity page starts loading but never completes loading**</span><span class="sxs-lookup"><span data-stu-id="d75de-251">**Closing CRM entity page starts loading but never completes loading**</span></span>

<span data-ttu-id="d75de-252">When **InternetExplorerPooling** is enabled, and if you close a CRM entity page hosted in Unified Service Desk using the close (**x**) button (_see Image 1_), the CRM entity page to starts loading but never completes loading (_see Image 2_).</span><span class="sxs-lookup"><span data-stu-id="d75de-252">When **InternetExplorerPooling** is enabled, and if you close a CRM entity page hosted in Unified Service Desk using the close (**x**) button (_see Image 1_), the CRM entity page to starts loading but never completes loading (_see Image 2_).</span></span>

  <span data-ttu-id="d75de-253">![Closing CRM entity page hosted in Unified Service Desk using close button](../unified-service-desk/media/usd-crm-page-hosted-close-button.PNG "Closing CRM entity page hosted in Unified Service Desk using close button")</span><span class="sxs-lookup"><span data-stu-id="d75de-253">![Closing CRM entity page hosted in Unified Service Desk using close button](../unified-service-desk/media/usd-crm-page-hosted-close-button.PNG "Closing CRM entity page hosted in Unified Service Desk using close button")</span></span>
    
  <span data-ttu-id="d75de-254">_Image 1: Closing CRM entity page hosted in Unified Service Desk using close (x) button_</span><span class="sxs-lookup"><span data-stu-id="d75de-254">_Image 1: Closing CRM entity page hosted in Unified Service Desk using close (x) button_</span></span>
  
  <span data-ttu-id="d75de-255">![CRM entity page start loading but never completes loading](../unified-service-desk/media/usd-crm-page-hosted-never-completes-loading.PNG "CRM entity page start loading but never completes loading")</span><span class="sxs-lookup"><span data-stu-id="d75de-255">![CRM entity page start loading but never completes loading](../unified-service-desk/media/usd-crm-page-hosted-never-completes-loading.PNG "CRM entity page start loading but never completes loading")</span></span>
  
  <span data-ttu-id="d75de-256">_Image 2: CRM entity page start loading but never completes loading_</span><span class="sxs-lookup"><span data-stu-id="d75de-256">_Image 2: CRM entity page start loading but never completes loading_</span></span>

<span data-ttu-id="d75de-257">**Giải pháp thay thế**</span><span class="sxs-lookup"><span data-stu-id="d75de-257">**Workaround**</span></span>

<span data-ttu-id="d75de-258">If you close the CRM entity page, the page starts loading but never completes the loading.</span><span class="sxs-lookup"><span data-stu-id="d75de-258">If you close the CRM entity page, the page starts loading but never completes the loading.</span></span> <span data-ttu-id="d75de-259">In this case, to restore the CRM entity page, right-click on CRM entity page and select **Forward** from the context menu (_see Image 1_).</span><span class="sxs-lookup"><span data-stu-id="d75de-259">In this case, to restore the CRM entity page, right-click on CRM entity page and select **Forward** from the context menu (_see Image 1_).</span></span>

<span data-ttu-id="d75de-260">![Right-click on the CRM entity page and select Forward from the context menu](../unified-service-desk/media/usd-crm-page-right-click-CRM-entity-page-select-forward.PNG "Right-click on the CRM entity page and select Forward from the context menu")</span><span class="sxs-lookup"><span data-stu-id="d75de-260">![Right-click on the CRM entity page and select Forward from the context menu](../unified-service-desk/media/usd-crm-page-right-click-CRM-entity-page-select-forward.PNG "Right-click on the CRM entity page and select Forward from the context menu")</span></span>

<span data-ttu-id="d75de-261">_Image 1: Right-click on the CRM entity page and select Forward from the context menu_</span><span class="sxs-lookup"><span data-stu-id="d75de-261">_Image 1: Right-click on the CRM entity page and select Forward from the context menu_</span></span>

> [!Note]
> <span data-ttu-id="d75de-262">The session that you are working is fine and there is no data loss.</span><span class="sxs-lookup"><span data-stu-id="d75de-262">The session that you are working is fine and there is no data loss.</span></span>

### <a name="clicking-back-button-in-a-session-does-not-perform-navigation-to-original-url"></a><span data-ttu-id="d75de-263">Clicking back button in a session does not perform navigation to original URL</span><span class="sxs-lookup"><span data-stu-id="d75de-263">Clicking back button in a session does not perform navigation to original URL</span></span>

<span data-ttu-id="d75de-264">If you open any webpage in the browser with hosted controls using IE Process hosting method, the webpage opens in a new window within the same-hosted control overlaying the existing page/window.</span><span class="sxs-lookup"><span data-stu-id="d75de-264">If you open any webpage in the browser with hosted controls using IE Process hosting method, the webpage opens in a new window within the same-hosted control overlaying the existing page/window.</span></span> 

<span data-ttu-id="d75de-265">Since the webpage is opened in the new window within the same hosted control overlaying the existing page or window, clicking the back button in the webpage does not perform the navigation back to the original page.</span><span class="sxs-lookup"><span data-stu-id="d75de-265">Since the webpage is opened in the new window within the same hosted control overlaying the existing page or window, clicking the back button in the webpage does not perform the navigation back to the original page.</span></span> <span data-ttu-id="d75de-266">This behavior is that the new window does not have any history to navigate back to the original page.</span><span class="sxs-lookup"><span data-stu-id="d75de-266">This behavior is that the new window does not have any history to navigate back to the original page.</span></span>

<span data-ttu-id="d75de-267">**Giải pháp thay thế**</span><span class="sxs-lookup"><span data-stu-id="d75de-267">**Workaround**</span></span>

<span data-ttu-id="d75de-268">Configure **Show Outside** action call to show the webpage in an **IE process** outside of the hosted control space in the popup window.</span><span class="sxs-lookup"><span data-stu-id="d75de-268">Configure **Show Outside** action call to show the webpage in an **IE process** outside of the hosted control space in the popup window.</span></span>

#### <a name="step-1-configure-showoutside-action-call"></a><span data-ttu-id="d75de-269">Step 1: Configure ShowOutside action call</span><span class="sxs-lookup"><span data-stu-id="d75de-269">Step 1: Configure ShowOutside action call</span></span>

<span data-ttu-id="d75de-270">In this step, you will create an action call to show the webpage.</span><span class="sxs-lookup"><span data-stu-id="d75de-270">In this step, you will create an action call to show the webpage.</span></span>

1. <span data-ttu-id="d75de-271">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="d75de-271">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>
2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]
3. <span data-ttu-id="d75de-272">Clikc **Action Calls**.</span><span class="sxs-lookup"><span data-stu-id="d75de-272">Clikc **Action Calls**.</span></span>
4. <span data-ttu-id="d75de-273">Bấm vào **+Mới**.</span><span class="sxs-lookup"><span data-stu-id="d75de-273">Click **+ New**.</span></span>
5. <span data-ttu-id="d75de-274">On the **New Action Call** page, specify the following values.</span><span class="sxs-lookup"><span data-stu-id="d75de-274">On the **New Action Call** page, specify the following values.</span></span>
  
   | <span data-ttu-id="d75de-275">Trường</span><span class="sxs-lookup"><span data-stu-id="d75de-275">Field</span></span> | <span data-ttu-id="d75de-276">Value</span><span class="sxs-lookup"><span data-stu-id="d75de-276">Value</span></span> |
   |----------|-----------|
   |<span data-ttu-id="d75de-277">Tên</span><span class="sxs-lookup"><span data-stu-id="d75de-277">Name</span></span> | <span data-ttu-id="d75de-278">Show Outside</span><span class="sxs-lookup"><span data-stu-id="d75de-278">Show Outside</span></span> |
   |<span data-ttu-id="d75de-279">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="d75de-279">Hosted Control</span></span> | <span data-ttu-id="d75de-280">CRM Global Manager</span><span class="sxs-lookup"><span data-stu-id="d75de-280">CRM Global Manager</span></span>|
   |<span data-ttu-id="d75de-281">Hành động</span><span class="sxs-lookup"><span data-stu-id="d75de-281">Action</span></span>| <span data-ttu-id="d75de-282">LaunchURL</span><span class="sxs-lookup"><span data-stu-id="d75de-282">LaunchURL</span></span>|
   |<span data-ttu-id="d75de-283">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="d75de-283">Data</span></span>| <span data-ttu-id="d75de-284">[[SUBJECTURL]]</span><span class="sxs-lookup"><span data-stu-id="d75de-284">[[SUBJECTURL]]</span></span>|

   <span data-ttu-id="d75de-285">![Show outside Action Call](media/show-outside-action-call.PNG "Show outside Action Call")</span><span class="sxs-lookup"><span data-stu-id="d75de-285">![Show outside Action Call](media/show-outside-action-call.PNG "Show outside Action Call")</span></span>
6. <span data-ttu-id="d75de-286">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="d75de-286">Click **Save**.</span></span>

#### <a name="step-2-configure-window-navigation-rules-and-add-the-action-call"></a><span data-ttu-id="d75de-287">Step 2: Configure Window Navigation Rules and add the Action Call</span><span class="sxs-lookup"><span data-stu-id="d75de-287">Step 2: Configure Window Navigation Rules and add the Action Call</span></span>

<span data-ttu-id="d75de-288">In this step you will create a navigation rule and set the order before other default rules.</span><span class="sxs-lookup"><span data-stu-id="d75de-288">In this step you will create a navigation rule and set the order before other default rules.</span></span> <span data-ttu-id="d75de-289">After creating the navigation rule, add the **ShowOutside** action call that you created in Step 1 to the **Show Outside Rule** window navigation rule.</span><span class="sxs-lookup"><span data-stu-id="d75de-289">After creating the navigation rule, add the **ShowOutside** action call that you created in Step 1 to the **Show Outside Rule** window navigation rule.</span></span>

1. <span data-ttu-id="d75de-290">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="d75de-290">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>
2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]
3. <span data-ttu-id="d75de-291">Click **Window Navigation Rules**.</span><span class="sxs-lookup"><span data-stu-id="d75de-291">Click **Window Navigation Rules**.</span></span>
4. <span data-ttu-id="d75de-292">Click **+ New**.</span><span class="sxs-lookup"><span data-stu-id="d75de-292">Click **+ New**.</span></span>
5. <span data-ttu-id="d75de-293">On the **New Window Navigation Rules** page, specify the following values.</span><span class="sxs-lookup"><span data-stu-id="d75de-293">On the **New Window Navigation Rules** page, specify the following values.</span></span>

   | <span data-ttu-id="d75de-294">Trường</span><span class="sxs-lookup"><span data-stu-id="d75de-294">Field</span></span> | <span data-ttu-id="d75de-295">Value</span><span class="sxs-lookup"><span data-stu-id="d75de-295">Value</span></span> |
   |-------------|----------------|
   |<span data-ttu-id="d75de-296">Tên</span><span class="sxs-lookup"><span data-stu-id="d75de-296">Name</span></span>| <span data-ttu-id="d75de-297">Show Outside Rule</span><span class="sxs-lookup"><span data-stu-id="d75de-297">Show Outside Rule</span></span>|
   |<span data-ttu-id="d75de-298">Thứ tự</span><span class="sxs-lookup"><span data-stu-id="d75de-298">Order</span></span> | <span data-ttu-id="d75de-299">1</span><span class="sxs-lookup"><span data-stu-id="d75de-299">1</span></span> <br> <span data-ttu-id="d75de-300">**Note:** You can specify any order that is lesser than the default list of Window Navigation Rules.</span><span class="sxs-lookup"><span data-stu-id="d75de-300">**Note:** You can specify any order that is lesser than the default list of Window Navigation Rules.</span></span> |
   | <span data-ttu-id="d75de-301">Url</span><span class="sxs-lookup"><span data-stu-id="d75de-301">Url</span></span> | <span data-ttu-id="d75de-302">https://www.bing.com</span><span class="sxs-lookup"><span data-stu-id="d75de-302">https://www.bing.com</span></span> <br> <span data-ttu-id="d75de-303">**Note:** You must to specify a URL to which you want to navigate.</span><span class="sxs-lookup"><span data-stu-id="d75de-303">**Note:** You must to specify a URL to which you want to navigate.</span></span>|
   |<span data-ttu-id="d75de-304">Loại định tuyến</span><span class="sxs-lookup"><span data-stu-id="d75de-304">Route Type</span></span> | <span data-ttu-id="d75de-305">Cửa sổ bật lên</span><span class="sxs-lookup"><span data-stu-id="d75de-305">Popup</span></span> |
   | <span data-ttu-id="d75de-306">Điểm đến</span><span class="sxs-lookup"><span data-stu-id="d75de-306">Destination</span></span> | <span data-ttu-id="d75de-307">Thẻ</span><span class="sxs-lookup"><span data-stu-id="d75de-307">Tab</span></span> |
   |<span data-ttu-id="d75de-308">Hành động</span><span class="sxs-lookup"><span data-stu-id="d75de-308">Action</span></span> | <span data-ttu-id="d75de-309">Không có</span><span class="sxs-lookup"><span data-stu-id="d75de-309">None</span></span> |

   <span data-ttu-id="d75de-310">![Show outside Window Navigation Rule](media/show-outside-navigation-rule.PNG "Show outside Window Navigation Rule")</span><span class="sxs-lookup"><span data-stu-id="d75de-310">![Show outside Window Navigation Rule](media/show-outside-navigation-rule.PNG "Show outside Window Navigation Rule")</span></span>

6. <span data-ttu-id="d75de-311">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="d75de-311">Click **Save**.</span></span>
7. <span data-ttu-id="d75de-312">On the nav bar, click the down arrow next to **Show Outside Rule**, and click **Actions**.</span><span class="sxs-lookup"><span data-stu-id="d75de-312">On the nav bar, click the down arrow next to **Show Outside Rule**, and click **Actions**.</span></span>
8. <span data-ttu-id="d75de-313">On the next page, click **ADD EXISTING ACTION CALL**, type **Show Outside** in the search bar, and then press **ENTER** or click the search icon.</span><span class="sxs-lookup"><span data-stu-id="d75de-313">On the next page, click **ADD EXISTING ACTION CALL**, type **Show Outside** in the search bar, and then press **ENTER** or click the search icon.</span></span>
9. <span data-ttu-id="d75de-314">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="d75de-314">Click **Save**.</span></span>

<span data-ttu-id="d75de-315">The configuration of action call and window navigation rule is completed.</span><span class="sxs-lookup"><span data-stu-id="d75de-315">The configuration of action call and window navigation rule is completed.</span></span> <span data-ttu-id="d75de-316">If you now open a webpage, the webpage opens as a popup in a new window.</span><span class="sxs-lookup"><span data-stu-id="d75de-316">If you now open a webpage, the webpage opens as a popup in a new window.</span></span>

<span data-ttu-id="d75de-317">For more information related to this limitation, refer the [Unified Service Desk Blogs](https://blogs.msdn.microsoft.com/usd/2017/09/27/unified-service-desk-best-practices-part-5-open-pdf-files-in-an-ie-process-hosted-control/)</span><span class="sxs-lookup"><span data-stu-id="d75de-317">For more information related to this limitation, refer the [Unified Service Desk Blogs](https://blogs.msdn.microsoft.com/usd/2017/09/27/unified-service-desk-best-practices-part-5-open-pdf-files-in-an-ie-process-hosted-control/)</span></span>

## <a name="see-also"></a><span data-ttu-id="d75de-318">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="d75de-318">See also</span></span>

[<span data-ttu-id="d75de-319">Analyze best practices in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="d75de-319">Analyze best practices in Unified Service Desk</span></span>](admin/analyze-best-practices-unified-service-desk.md)

[<span data-ttu-id="d75de-320">Performance enhancement for CRM entity page loads</span><span class="sxs-lookup"><span data-stu-id="d75de-320">Performance enhancement for CRM entity page loads</span></span>](admin/performance-enhancement-CRM-entity-page-loads.md)

[<span data-ttu-id="d75de-321">Help improve Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="d75de-321">Help improve Unified Service Desk</span></span>](admin/help-improve-unified-service-desk.md)

::: moniker-end