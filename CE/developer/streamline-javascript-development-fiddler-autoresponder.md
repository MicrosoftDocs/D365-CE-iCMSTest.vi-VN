---
title: Streamline JavaScript web resource development using Fiddler AutoResponder (Developer Guide for Dynamics 365 for Customer Engagement apps)| MicrosoftDocs
description: Learn about how to setup and use AutoResponder in Fiddler for local debugging of JavaScript web resources.
ms.custom: ''
ms.date: 09/18/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: E197DEB3-7461-48D4-80D4-C0BFC8AC80A1
author: SushantSikka
ms.author: susikka
manager: sakudes
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7163e0fb328fca3e02cf78db030e262f0fdf17cc
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388501"
---
# <a name="streamline-javascript-web-resource-development-using-fiddler-autoresponder"></a><span data-ttu-id="d56ed-103">Streamline JavaScript web resource development using Fiddler AutoResponder</span><span class="sxs-lookup"><span data-stu-id="d56ed-103">Streamline JavaScript web resource development using Fiddler AutoResponder</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="d56ed-104">While developing and debugging JavaScript web resources, you can use AutoResponder in [Telerik Fiddler](https://www.telerik.com/fiddler) to replace the content of a web resource with content from a local file rather than uploading it in your Dynamics 365 for Customer Engagement instance and publishing each time.</span><span class="sxs-lookup"><span data-stu-id="d56ed-104">While developing and debugging JavaScript web resources, you can use AutoResponder in [Telerik Fiddler](https://www.telerik.com/fiddler) to replace the content of a web resource with content from a local file rather than uploading it in your Dynamics 365 for Customer Engagement instance and publishing each time.</span></span> <span data-ttu-id="d56ed-105">Use the following steps below to setup AutoResponder in Fiddler.</span><span class="sxs-lookup"><span data-stu-id="d56ed-105">Use the following steps below to setup AutoResponder in Fiddler.</span></span>

## <a name="install-and-configure-fiddler"></a><span data-ttu-id="d56ed-106">Install and configure Fiddler</span><span class="sxs-lookup"><span data-stu-id="d56ed-106">Install and configure Fiddler</span></span>

1. <span data-ttu-id="d56ed-107">[Download](https://www.telerik.com/download/fiddler) and install Fiddler.</span><span class="sxs-lookup"><span data-stu-id="d56ed-107">[Download](https://www.telerik.com/download/fiddler) and install Fiddler.</span></span>
1. <span data-ttu-id="d56ed-108">Open Fiddler and from the menu bar, go to **Tools**, and then select **Options**.</span><span class="sxs-lookup"><span data-stu-id="d56ed-108">Open Fiddler and from the menu bar, go to **Tools**, and then select **Options**.</span></span>
2. <span data-ttu-id="d56ed-109">Select the **HTTPS** tab in the dialog box and check the **Capture HTTPS CONNECTS** and **Decrypt HTTPS traffic** checkboxes so that the HTTPS traffic is captured and then decrypted.</span><span class="sxs-lookup"><span data-stu-id="d56ed-109">Select the **HTTPS** tab in the dialog box and check the **Capture HTTPS CONNECTS** and **Decrypt HTTPS traffic** checkboxes so that the HTTPS traffic is captured and then decrypted.</span></span><br />
 <span data-ttu-id="d56ed-110">![Select the marked checkboxes in the HTTP tab](media/fiddler-https-options.png "Select the marked checkboxes in the HTTP tab")</span><span class="sxs-lookup"><span data-stu-id="d56ed-110">![Select the marked checkboxes in the HTTP tab](media/fiddler-https-options.png "Select the marked checkboxes in the HTTP tab")</span></span></br>
3. <span data-ttu-id="d56ed-111">Click **OK** to close the dialog box.</span><span class="sxs-lookup"><span data-stu-id="d56ed-111">Click **OK** to close the dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="d56ed-112">If it is the first time you are enabling this setting, Fiddler will prompt you to install a certificate.</span><span class="sxs-lookup"><span data-stu-id="d56ed-112">If it is the first time you are enabling this setting, Fiddler will prompt you to install a certificate.</span></span> <span data-ttu-id="d56ed-113">Install the certificate and restart Fiddler so that the new settings take effect.</span><span class="sxs-lookup"><span data-stu-id="d56ed-113">Install the certificate and restart Fiddler so that the new settings take effect.</span></span><br />
> <span data-ttu-id="d56ed-114">If you have run Fiddler in the past and get a `NET::ERR_CERT_AUTHORITY_INVALID` error, in the **HTTPS** tab, click the **Actions** button and choose **Reset All Certificates**.</span><span class="sxs-lookup"><span data-stu-id="d56ed-114">If you have run Fiddler in the past and get a `NET::ERR_CERT_AUTHORITY_INVALID` error, in the **HTTPS** tab, click the **Actions** button and choose **Reset All Certificates**.</span></span> <span data-ttu-id="d56ed-115">This will also present a number of prompts for the new certificates to be installed.</span><span class="sxs-lookup"><span data-stu-id="d56ed-115">This will also present a number of prompts for the new certificates to be installed.</span></span>

## <a name="configure-autoresponder"></a><span data-ttu-id="d56ed-116">Configure AutoResponder</span><span class="sxs-lookup"><span data-stu-id="d56ed-116">Configure AutoResponder</span></span>

1. <span data-ttu-id="d56ed-117">Open the page in your Dynamics 365 for Customer Engagement apps instance that you want to debug.</span><span class="sxs-lookup"><span data-stu-id="d56ed-117">Open the page in your Dynamics 365 for Customer Engagement apps instance that you want to debug.</span></span>
2. <span data-ttu-id="d56ed-118">Start the Fiddler trace capture by clicking the **Capturing** button in the bottom left corner.</span><span class="sxs-lookup"><span data-stu-id="d56ed-118">Start the Fiddler trace capture by clicking the **Capturing** button in the bottom left corner.</span></span>
   <span data-ttu-id="d56ed-119">![Click on Capturing button to start capturing HTTPS traffic](media/fiddler-start-capturing.png "Click on Capturing button to start capturing HTTPS traffic")</span><span class="sxs-lookup"><span data-stu-id="d56ed-119">![Click on Capturing button to start capturing HTTPS traffic](media/fiddler-start-capturing.png "Click on Capturing button to start capturing HTTPS traffic")</span></span></br>

   > [!NOTE]
   > <span data-ttu-id="d56ed-120">If you want to capture HTTPS traffic only from a particular host, on the **Filters** tab, in the **Hosts** area, in the **-No Host Filter-** drop-down select **Show only the following Hosts** from the menu and enter the list of domains from which you wish to see traffic, separated by semi-colon.</span><span class="sxs-lookup"><span data-stu-id="d56ed-120">If you want to capture HTTPS traffic only from a particular host, on the **Filters** tab, in the **Hosts** area, in the **-No Host Filter-** drop-down select **Show only the following Hosts** from the menu and enter the list of domains from which you wish to see traffic, separated by semi-colon.</span></span> <span data-ttu-id="d56ed-121">More information: [Filters reference](http://docs.telerik.com/fiddler/KnowledgeBase/Filters).</span><span class="sxs-lookup"><span data-stu-id="d56ed-121">More information: [Filters reference](http://docs.telerik.com/fiddler/KnowledgeBase/Filters).</span></span>
   > <span data-ttu-id="d56ed-122">![Filter traffic displayed in Fiddler UI](media/fiddler-filter-traffic.png "Filter traffic displayed in Fiddler UI")</span><span class="sxs-lookup"><span data-stu-id="d56ed-122">![Filter traffic displayed in Fiddler UI](media/fiddler-filter-traffic.png "Filter traffic displayed in Fiddler UI")</span></span>

3. <span data-ttu-id="d56ed-123">Perform any operation necessary to load the script you are testing.</span><span class="sxs-lookup"><span data-stu-id="d56ed-123">Perform any operation necessary to load the script you are testing.</span></span> <span data-ttu-id="d56ed-124">You can stop the capture by clicking the same **Capturing** button again.</span><span class="sxs-lookup"><span data-stu-id="d56ed-124">You can stop the capture by clicking the same **Capturing** button again.</span></span>
4. <span data-ttu-id="d56ed-125">Select the trace log sessions from the left pane and search for the file you want to setup the AutoResponder for.</span><span class="sxs-lookup"><span data-stu-id="d56ed-125">Select the trace log sessions from the left pane and search for the file you want to setup the AutoResponder for.</span></span><br /> <span data-ttu-id="d56ed-126">For example, if the code you want to debug is in a JavaScript web resource named `new_testscript.js`, use the **Find** button to open the  **Find Sessions** dialog box and search for the name of the webresource.</span><span class="sxs-lookup"><span data-stu-id="d56ed-126">For example, if the code you want to debug is in a JavaScript web resource named `new_testscript.js`, use the **Find** button to open the  **Find Sessions** dialog box and search for the name of the webresource.</span></span> <br /><span data-ttu-id="d56ed-127">![Find a session in fiddler](media/fiddler-find-sessions.PNG)</span><span class="sxs-lookup"><span data-stu-id="d56ed-127">![Find a session in fiddler](media/fiddler-find-sessions.PNG)</span></span><br /><span data-ttu-id="d56ed-128">You will see the rows that match with your search criteria highlighted in the left pane.</span><span class="sxs-lookup"><span data-stu-id="d56ed-128">You will see the rows that match with your search criteria highlighted in the left pane.</span></span>
5. <span data-ttu-id="d56ed-129">Select that row.</span><span class="sxs-lookup"><span data-stu-id="d56ed-129">Select that row.</span></span> <span data-ttu-id="d56ed-130">In the right pane, select the **AutoResponder** tab.</span><span class="sxs-lookup"><span data-stu-id="d56ed-130">In the right pane, select the **AutoResponder** tab.</span></span> <br /> <span data-ttu-id="d56ed-131">![Select the AutoResponder tab](media/fiddler-auto-responder.png)</span><span class="sxs-lookup"><span data-stu-id="d56ed-131">![Select the AutoResponder tab](media/fiddler-auto-responder.png)</span></span>
6. <span data-ttu-id="d56ed-132">In the **AutoResponder** tab, select the **Enable rules** and **Unmatched requests passthrough** check boxes.</span><span class="sxs-lookup"><span data-stu-id="d56ed-132">In the **AutoResponder** tab, select the **Enable rules** and **Unmatched requests passthrough** check boxes.</span></span><br />
   <span data-ttu-id="d56ed-133">![Select the two highlighted checkboxes](media/fiddler-select-checkbox.png "Select the two highlighted checkboxes")</span><span class="sxs-lookup"><span data-stu-id="d56ed-133">![Select the two highlighted checkboxes](media/fiddler-select-checkbox.png "Select the two highlighted checkboxes")</span></span><br />
7. <span data-ttu-id="d56ed-134">Ensure that you still have the session related to your target file selected and then click on the **Add Rule** button in the **AutoResponder** section.</span><span class="sxs-lookup"><span data-stu-id="d56ed-134">Ensure that you still have the session related to your target file selected and then click on the **Add Rule** button in the **AutoResponder** section.</span></span> <span data-ttu-id="d56ed-135">This adds a new entry into the rules table.</span><span class="sxs-lookup"><span data-stu-id="d56ed-135">This adds a new entry into the rules table.</span></span><br />
   <span data-ttu-id="d56ed-136">![Add new rule](media/fiddler-add-rule.png "Add new rule")</span><span class="sxs-lookup"><span data-stu-id="d56ed-136">![Add new rule](media/fiddler-add-rule.png "Add new rule")</span></span>
8. <span data-ttu-id="d56ed-137">When the rule is selected, the **Rule Editor** at the bottom has the top row populated with the Session URL related to your file and prefixed with a string like `EXACT:`.</span><span class="sxs-lookup"><span data-stu-id="d56ed-137">When the rule is selected, the **Rule Editor** at the bottom has the top row populated with the Session URL related to your file and prefixed with a string like `EXACT:`.</span></span><br />
   <span data-ttu-id="d56ed-138">You can then edit the string to match to simplify it.</span><span class="sxs-lookup"><span data-stu-id="d56ed-138">You can then edit the string to match to simplify it.</span></span> <span data-ttu-id="d56ed-139">With web resources, the URL will contain generated values in the URL or in a query string to make sure that the latest published version is included in the response.</span><span class="sxs-lookup"><span data-stu-id="d56ed-139">With web resources, the URL will contain generated values in the URL or in a query string to make sure that the latest published version is included in the response.</span></span> <span data-ttu-id="d56ed-140">You will probably see the `EXACT` value will look something like this:</span><span class="sxs-lookup"><span data-stu-id="d56ed-140">You will probably see the `EXACT` value will look something like this:</span></span><br />
    ```
    EXACT:https://<org URL>/%7B636556138760000160%7D/WebResources/new_testscript.js?    ver=-1229805553
    ```
  
    <span data-ttu-id="d56ed-141">You can simplify this to remove the generated values and use this instead:</span><span class="sxs-lookup"><span data-stu-id="d56ed-141">You can simplify this to remove the generated values and use this instead:</span></span><br />

    ```
    /WebResources/new_testscript.js
    ```

   <span data-ttu-id="d56ed-142">The bottom row is left blank.</span><span class="sxs-lookup"><span data-stu-id="d56ed-142">The bottom row is left blank.</span></span> <span data-ttu-id="d56ed-143">Type the path to your local file on your disk on this bottom row and <strong>Save</strong>.</span><span class="sxs-lookup"><span data-stu-id="d56ed-143">Type the path to your local file on your disk on this bottom row and <strong>Save</strong>.</span></span><br />

   <span data-ttu-id="d56ed-144">![Add path to your local file in Rule editor](media/fiddler-save-rule.png "Add path to your local file in Rule editor")</span><span class="sxs-lookup"><span data-stu-id="d56ed-144">![Add path to your local file in Rule editor](media/fiddler-save-rule.png "Add path to your local file in Rule editor")</span></span><br />

<span data-ttu-id="d56ed-145">By following the above steps, Fiddler is configured to listen to the requests and responds with the local file instead of passing the request over the network.</span><span class="sxs-lookup"><span data-stu-id="d56ed-145">By following the above steps, Fiddler is configured to listen to the requests and responds with the local file instead of passing the request over the network.</span></span>

## <a name="update-and-test-your-code"></a><span data-ttu-id="d56ed-146">Update and test your code</span><span class="sxs-lookup"><span data-stu-id="d56ed-146">Update and test your code</span></span>

1. <span data-ttu-id="d56ed-147">Apply changes to your local file.</span><span class="sxs-lookup"><span data-stu-id="d56ed-147">Apply changes to your local file.</span></span>
2. <span data-ttu-id="d56ed-148">Start Fiddler trace capture again and go back to your browser and hard reload the page with empty cache.</span><span class="sxs-lookup"><span data-stu-id="d56ed-148">Start Fiddler trace capture again and go back to your browser and hard reload the page with empty cache.</span></span>
3. <span data-ttu-id="d56ed-149">In the browser developer tools you can see that the file that is now received will be the local one.</span><span class="sxs-lookup"><span data-stu-id="d56ed-149">In the browser developer tools you can see that the file that is now received will be the local one.</span></span>
4. <span data-ttu-id="d56ed-150">Continue repeating this process while updating your code until you get the results you require.</span><span class="sxs-lookup"><span data-stu-id="d56ed-150">Continue repeating this process while updating your code until you get the results you require.</span></span>


## <a name="see-also"></a><span data-ttu-id="d56ed-151">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="d56ed-151">See Also</span></span>

[<span data-ttu-id="d56ed-152">Web resources for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="d56ed-152">Web resources for Customer Engagement apps</span></span>](web-resources.md)<br />
[<span data-ttu-id="d56ed-153">Use JavaScript with Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="d56ed-153">Use JavaScript with Customer Engagement apps</span></span>](use-javascript.md)<br />
[<span data-ttu-id="d56ed-154">Client scripting in Customer Engagement apps using JavaScript</span><span class="sxs-lookup"><span data-stu-id="d56ed-154">Client scripting in Customer Engagement apps using JavaScript</span></span>](clientapi/client-scripting.md)
