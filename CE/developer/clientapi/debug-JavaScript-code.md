---
title: Debug your JavaScript code for Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: conceptual
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 3edad039-4397-4984-a29b-9307a7a2aaee
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: d8a6be0a7b936377cd031f8e2c75683c632b7718
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387540"
---
# <a name="debug-your-javascript-code-for-customer-engagement"></a><span data-ttu-id="14f3a-102">Debug your JavaScript code for Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="14f3a-102">Debug your JavaScript code for Customer Engagement</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="14f3a-103">Each browser provides some kind of debugging extension.</span><span class="sxs-lookup"><span data-stu-id="14f3a-103">Each browser provides some kind of debugging extension.</span></span> <span data-ttu-id="14f3a-104">Microsoft Edge and Internet Explorer provide F12 Developer Tools you can use to debug scripts in Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="14f3a-104">Microsoft Edge and Internet Explorer provide F12 Developer Tools you can use to debug scripts in Customer Engagement.</span></span> <span data-ttu-id="14f3a-105">The F12 Developer Tools can be opened by pressing F12 when viewing a page using Microsoft Edge or Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="14f3a-105">The F12 Developer Tools can be opened by pressing F12 when viewing a page using Microsoft Edge or Internet Explorer.</span></span> <span data-ttu-id="14f3a-106">For more information, see Using the [F12 developer tools guide](https://docs.microsoft.com/microsoft-edge/f12-devtools-guide).</span><span class="sxs-lookup"><span data-stu-id="14f3a-106">For more information, see Using the [F12 developer tools guide](https://docs.microsoft.com/microsoft-edge/f12-devtools-guide).</span></span>

<span data-ttu-id="14f3a-107">For Google Chrome, press F12 to open developer tools.</span><span class="sxs-lookup"><span data-stu-id="14f3a-107">For Google Chrome, press F12 to open developer tools.</span></span> <span data-ttu-id="14f3a-108">Firebug is a popular browser extension for web development using Mozilla Firefox.</span><span class="sxs-lookup"><span data-stu-id="14f3a-108">Firebug is a popular browser extension for web development using Mozilla Firefox.</span></span> <span data-ttu-id="14f3a-109">For Apple Safari, you must first select the **Show Develop** menu in menu bar in **Advanced Preferences**.</span><span class="sxs-lookup"><span data-stu-id="14f3a-109">For Apple Safari, you must first select the **Show Develop** menu in menu bar in **Advanced Preferences**.</span></span> <span data-ttu-id="14f3a-110">Then you can select **Show Web Inspector** from the **Develop** menu.</span><span class="sxs-lookup"><span data-stu-id="14f3a-110">Then you can select **Show Web Inspector** from the **Develop** menu.</span></span>

<span data-ttu-id="14f3a-111">When you use JavaScript libraries in Customer Engagement, your libraries are loaded with the web page.</span><span class="sxs-lookup"><span data-stu-id="14f3a-111">When you use JavaScript libraries in Customer Engagement, your libraries are loaded with the web page.</span></span> <span data-ttu-id="14f3a-112">It can sometimes be difficult to isolate your specific library in the debugging environment.</span><span class="sxs-lookup"><span data-stu-id="14f3a-112">It can sometimes be difficult to isolate your specific library in the debugging environment.</span></span> <span data-ttu-id="14f3a-113">When using debugging tools in Microsoft Edge, on the **Debugger** tab, click on the folder icon at the top-left corner, and expand the available scripts and find the one with the name that corresponds to the name of your JavaScript web resource, such as the **new_myCustomJavaScript.js** web resource shown below.</span><span class="sxs-lookup"><span data-stu-id="14f3a-113">When using debugging tools in Microsoft Edge, on the **Debugger** tab, click on the folder icon at the top-left corner, and expand the available scripts and find the one with the name that corresponds to the name of your JavaScript web resource, such as the **new_myCustomJavaScript.js** web resource shown below.</span></span> <span data-ttu-id="14f3a-114">You can also search for your JavaScript library by typing the file name in the search box.</span><span class="sxs-lookup"><span data-stu-id="14f3a-114">You can also search for your JavaScript library by typing the file name in the search box.</span></span>

![Debugging JavaScript](../media/form-script-debugging.png)

<span data-ttu-id="14f3a-116">Debugging tools for different browsers have similar capabilities.</span><span class="sxs-lookup"><span data-stu-id="14f3a-116">Debugging tools for different browsers have similar capabilities.</span></span> <span data-ttu-id="14f3a-117">Once you have found your library, you can set a break point and recreate the event that should cause your code to run.</span><span class="sxs-lookup"><span data-stu-id="14f3a-117">Once you have found your library, you can set a break point and recreate the event that should cause your code to run.</span></span>

<span data-ttu-id="14f3a-118">Also look at the following blog post on our team blog site for more ideas on debugging your JavaScript code: [Blog: Debugging custom JavaScript code in CRM using browser developer tools](https://blogs.msdn.microsoft.com/crm/2015/11/29/debugging-custom-javascript-code-in-crm-using-browser-developer-tools/).</span><span class="sxs-lookup"><span data-stu-id="14f3a-118">Also look at the following blog post on our team blog site for more ideas on debugging your JavaScript code: [Blog: Debugging custom JavaScript code in CRM using browser developer tools](https://blogs.msdn.microsoft.com/crm/2015/11/29/debugging-custom-javascript-code-in-crm-using-browser-developer-tools/).</span></span>

## <a name="select-appropriate-frame-to-debug-your-code"></a><span data-ttu-id="14f3a-119">Select appropriate frame to debug your code</span><span class="sxs-lookup"><span data-stu-id="14f3a-119">Select appropriate frame to debug your code</span></span>

<span data-ttu-id="14f3a-120">Customer Engagement forms are composed of several frames.</span><span class="sxs-lookup"><span data-stu-id="14f3a-120">Customer Engagement forms are composed of several frames.</span></span> <span data-ttu-id="14f3a-121">For the code to work in the **Console** of the browser developer tools, you must select the appropriate frame.</span><span class="sxs-lookup"><span data-stu-id="14f3a-121">For the code to work in the **Console** of the browser developer tools, you must select the appropriate frame.</span></span> 
- <span data-ttu-id="14f3a-122">For the web client forms, select the frame named **ClientApiWrapper**.</span><span class="sxs-lookup"><span data-stu-id="14f3a-122">For the web client forms, select the frame named **ClientApiWrapper**.</span></span> 
- <span data-ttu-id="14f3a-123">For the new Unified Interface forms, select the frame named **ClientApiFrame_[n]** where n is the internal page ID.</span><span class="sxs-lookup"><span data-stu-id="14f3a-123">For the new Unified Interface forms, select the frame named **ClientApiFrame_[n]** where n is the internal page ID.</span></span> <span data-ttu-id="14f3a-124">You should select the frame with the highest value for [n].</span><span class="sxs-lookup"><span data-stu-id="14f3a-124">You should select the frame with the highest value for [n].</span></span>

## <a name="write-messages-to-the-console"></a><span data-ttu-id="14f3a-125">Write messages to the console</span><span class="sxs-lookup"><span data-stu-id="14f3a-125">Write messages to the console</span></span>

<span data-ttu-id="14f3a-126">Using the [window.alert](https://msdn.microsoft.com/library/ms535933(v=vs.85).aspx) method when debugging JavaScript is still a common way to troubleshoot code in the application.</span><span class="sxs-lookup"><span data-stu-id="14f3a-126">Using the [window.alert](https://msdn.microsoft.com/library/ms535933(v=vs.85).aspx) method when debugging JavaScript is still a common way to troubleshoot code in the application.</span></span> <span data-ttu-id="14f3a-127">But now that all modern browsers provide easy access to debugging tools, it is not a best practice, especially when others might be using the application you are debugging.</span><span class="sxs-lookup"><span data-stu-id="14f3a-127">But now that all modern browsers provide easy access to debugging tools, it is not a best practice, especially when others might be using the application you are debugging.</span></span>

<span data-ttu-id="14f3a-128">Consider writing your messages to the console instead.</span><span class="sxs-lookup"><span data-stu-id="14f3a-128">Consider writing your messages to the console instead.</span></span> <span data-ttu-id="14f3a-129">The following is a small function you can add to your libraries that you can use to send any messages you want to view to the console when it is open.</span><span class="sxs-lookup"><span data-stu-id="14f3a-129">The following is a small function you can add to your libraries that you can use to send any messages you want to view to the console when it is open.</span></span>

```JavaScript
function writeToConsole(message)
{
 if (typeof console != 'undefined') {
  console.log(message);
 }
}
```

<span data-ttu-id="14f3a-130">Unlike using the alert method, if you forget to remove any code that uses this function, people using the application will not see your messages.</span><span class="sxs-lookup"><span data-stu-id="14f3a-130">Unlike using the alert method, if you forget to remove any code that uses this function, people using the application will not see your messages.</span></span>
