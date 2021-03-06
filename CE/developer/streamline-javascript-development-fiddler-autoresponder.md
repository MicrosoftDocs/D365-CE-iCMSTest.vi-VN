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
# <a name="streamline-javascript-web-resource-development-using-fiddler-autoresponder"></a>Streamline JavaScript web resource development using Fiddler AutoResponder

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

While developing and debugging JavaScript web resources, you can use AutoResponder in [Telerik Fiddler](https://www.telerik.com/fiddler) to replace the content of a web resource with content from a local file rather than uploading it in your Dynamics 365 for Customer Engagement instance and publishing each time. Use the following steps below to setup AutoResponder in Fiddler.

## <a name="install-and-configure-fiddler"></a>Install and configure Fiddler

1. [Download](https://www.telerik.com/download/fiddler) and install Fiddler.
1. Open Fiddler and from the menu bar, go to **Tools**, and then select **Options**.
2. Select the **HTTPS** tab in the dialog box and check the **Capture HTTPS CONNECTS** and **Decrypt HTTPS traffic** checkboxes so that the HTTPS traffic is captured and then decrypted.<br />
 ![Select the marked checkboxes in the HTTP tab](media/fiddler-https-options.png "Select the marked checkboxes in the HTTP tab")</br>
3. Click **OK** to close the dialog box.

> [!NOTE]
> If it is the first time you are enabling this setting, Fiddler will prompt you to install a certificate. Install the certificate and restart Fiddler so that the new settings take effect.<br />
> If you have run Fiddler in the past and get a `NET::ERR_CERT_AUTHORITY_INVALID` error, in the **HTTPS** tab, click the **Actions** button and choose **Reset All Certificates**. This will also present a number of prompts for the new certificates to be installed.

## <a name="configure-autoresponder"></a>Configure AutoResponder

1. Open the page in your Dynamics 365 for Customer Engagement apps instance that you want to debug.
2. Start the Fiddler trace capture by clicking the **Capturing** button in the bottom left corner.
   ![Click on Capturing button to start capturing HTTPS traffic](media/fiddler-start-capturing.png "Click on Capturing button to start capturing HTTPS traffic")</br>

   > [!NOTE]
   > If you want to capture HTTPS traffic only from a particular host, on the **Filters** tab, in the **Hosts** area, in the **-No Host Filter-** drop-down select **Show only the following Hosts** from the menu and enter the list of domains from which you wish to see traffic, separated by semi-colon. More information: [Filters reference](http://docs.telerik.com/fiddler/KnowledgeBase/Filters).
   > ![Filter traffic displayed in Fiddler UI](media/fiddler-filter-traffic.png "Filter traffic displayed in Fiddler UI")

3. Perform any operation necessary to load the script you are testing. You can stop the capture by clicking the same **Capturing** button again.
4. Select the trace log sessions from the left pane and search for the file you want to setup the AutoResponder for.<br /> For example, if the code you want to debug is in a JavaScript web resource named `new_testscript.js`, use the **Find** button to open the  **Find Sessions** dialog box and search for the name of the webresource. <br />![Find a session in fiddler](media/fiddler-find-sessions.PNG)<br />You will see the rows that match with your search criteria highlighted in the left pane.
5. Select that row. In the right pane, select the **AutoResponder** tab. <br /> ![Select the AutoResponder tab](media/fiddler-auto-responder.png)
6. In the **AutoResponder** tab, select the **Enable rules** and **Unmatched requests passthrough** check boxes.<br />
   ![Select the two highlighted checkboxes](media/fiddler-select-checkbox.png "Select the two highlighted checkboxes")<br />
7. Ensure that you still have the session related to your target file selected and then click on the **Add Rule** button in the **AutoResponder** section. This adds a new entry into the rules table.<br />
   ![Add new rule](media/fiddler-add-rule.png "Add new rule")
8. When the rule is selected, the **Rule Editor** at the bottom has the top row populated with the Session URL related to your file and prefixed with a string like `EXACT:`.<br />
   You can then edit the string to match to simplify it. With web resources, the URL will contain generated values in the URL or in a query string to make sure that the latest published version is included in the response. You will probably see the `EXACT` value will look something like this:<br />
    ```
    EXACT:https://<org URL>/%7B636556138760000160%7D/WebResources/new_testscript.js?    ver=-1229805553
    ```
  
    You can simplify this to remove the generated values and use this instead:<br />

    ```
    /WebResources/new_testscript.js
    ```

   The bottom row is left blank. Type the path to your local file on your disk on this bottom row and <strong>Save</strong>.<br />

   ![Add path to your local file in Rule editor](media/fiddler-save-rule.png "Add path to your local file in Rule editor")<br />

By following the above steps, Fiddler is configured to listen to the requests and responds with the local file instead of passing the request over the network.

## <a name="update-and-test-your-code"></a>Update and test your code

1. Apply changes to your local file.
2. Start Fiddler trace capture again and go back to your browser and hard reload the page with empty cache.
3. In the browser developer tools you can see that the file that is now received will be the local one.
4. Continue repeating this process while updating your code until you get the results you require.


## <a name="see-also"></a>Xem thêm

[Web resources for Customer Engagement apps](web-resources.md)<br />
[Use JavaScript with Customer Engagement apps](use-javascript.md)<br />
[Client scripting in Customer Engagement apps using JavaScript](clientapi/client-scripting.md)
