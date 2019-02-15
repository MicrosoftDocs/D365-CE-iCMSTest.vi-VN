---
title: GetGlobalContext function and ClientGlobalContext.js.aspx in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 06/05/2018
ms.service: crm-online
ms.topic: conceptual
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: b58e6173-e3cd-4a3b-b39a-334c295503ec
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 5fb84aac769682c7338f21e557714ed31b99412a
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386023"
---
# <a name="getglobalcontext-function-and-clientglobalcontextjsaspx-client-api-reference"></a><span data-ttu-id="bda2c-102">GetGlobalContext function and ClientGlobalContext.js.aspx (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="bda2c-102">GetGlobalContext function and ClientGlobalContext.js.aspx (Client API reference)</span></span>

[!INCLUDE[](../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="bda2c-103">Use the **GetGlobalContext** function when programming with [web resources](../../web-resources.md) to gain access to the global context information such as the information specific to the client, organization or user for your Customer Engagement instance.</span><span class="sxs-lookup"><span data-stu-id="bda2c-103">Use the **GetGlobalContext** function when programming with [web resources](../../web-resources.md) to gain access to the global context information such as the information specific to the client, organization or user for your Customer Engagement instance.</span></span> 

<span data-ttu-id="bda2c-104">To get access to the **GetGlobalContext** function in your HTML web resource, include a reference to **ClientGlobalContext.js.aspx**.</span><span class="sxs-lookup"><span data-stu-id="bda2c-104">To get access to the **GetGlobalContext** function in your HTML web resource, include a reference to **ClientGlobalContext.js.aspx**.</span></span>

> [!NOTE]
> <span data-ttu-id="bda2c-105">Including a reference to **ClientGlobalContext.js.aspx** does not make the **Xrm** object available in HTML web resources.</span><span class="sxs-lookup"><span data-stu-id="bda2c-105">Including a reference to **ClientGlobalContext.js.aspx** does not make the **Xrm** object available in HTML web resources.</span></span> <span data-ttu-id="bda2c-106">Therefore, scripts containing `Xrm.*` methods aren’t supported in HTML web resources.</span><span class="sxs-lookup"><span data-stu-id="bda2c-106">Therefore, scripts containing `Xrm.*` methods aren’t supported in HTML web resources.</span></span> <span data-ttu-id="bda2c-107">`parent.Xrm.*` will work if the HTML web resource is loaded in a form container.</span><span class="sxs-lookup"><span data-stu-id="bda2c-107">`parent.Xrm.*` will work if the HTML web resource is loaded in a form container.</span></span> <span data-ttu-id="bda2c-108">However, for other places, such as loading an HTML web resource as part of the SiteMap, `parent.Xrm.*` also won’t work.</span><span class="sxs-lookup"><span data-stu-id="bda2c-108">However, for other places, such as loading an HTML web resource as part of the SiteMap, `parent.Xrm.*` also won’t work.</span></span>

## <a name="getglobalcontext-function"></a><span data-ttu-id="bda2c-109">GetGlobalContext function</span><span class="sxs-lookup"><span data-stu-id="bda2c-109">GetGlobalContext function</span></span>

<span data-ttu-id="bda2c-110">The **GetGlobalContext** function returns the same context object as returned by the **Xrm.Utility.getGlobalContext** method, which implies that the context object will have the same properties and methods as available for **Xrm.Utility.getGlobalContext**.</span><span class="sxs-lookup"><span data-stu-id="bda2c-110">The **GetGlobalContext** function returns the same context object as returned by the **Xrm.Utility.getGlobalContext** method, which implies that the context object will have the same properties and methods as available for **Xrm.Utility.getGlobalContext**.</span></span> <span data-ttu-id="bda2c-111">More information: Xrm.Utility.[getGlobalContext](Xrm-Utility/getGlobalContext.md)</span><span class="sxs-lookup"><span data-stu-id="bda2c-111">More information: Xrm.Utility.[getGlobalContext](Xrm-Utility/getGlobalContext.md)</span></span>

## <a name="clientglobalcontextjsaspx"></a><span data-ttu-id="bda2c-112">ClientGlobalContext.js.aspx</span><span class="sxs-lookup"><span data-stu-id="bda2c-112">ClientGlobalContext.js.aspx</span></span>

<span data-ttu-id="bda2c-113">You must include a reference to the **ClientGlobalContext.js.aspx** page located at the root of the web resources directory to be able to use the **GetGlobalContext** function.</span><span class="sxs-lookup"><span data-stu-id="bda2c-113">You must include a reference to the **ClientGlobalContext.js.aspx** page located at the root of the web resources directory to be able to use the **GetGlobalContext** function.</span></span>

- <span data-ttu-id="bda2c-114">If you are not using backslash characters in HTML web resource names to simulate a folder structure, you can include this script by directly referring to it.</span><span class="sxs-lookup"><span data-stu-id="bda2c-114">If you are not using backslash characters in HTML web resource names to simulate a folder structure, you can include this script by directly referring to it.</span></span> <span data-ttu-id="bda2c-115">Ví dụ:</span><span class="sxs-lookup"><span data-stu-id="bda2c-115">For example:</span></span>

    ```HTML
    <head>
      <title>HTML Web Resource</title>
      <script src="ClientGlobalContext.js.aspx" type="text/javascript" ></script>
      
    </head>
    ```
- <span data-ttu-id="bda2c-116">If you are using backslash characters in HTML web resource names to simulate a directory structure, you must reflect this in your script element.</span><span class="sxs-lookup"><span data-stu-id="bda2c-116">If you are using backslash characters in HTML web resource names to simulate a directory structure, you must reflect this in your script element.</span></span> <span data-ttu-id="bda2c-117">The following example is for an HTML web resource named **sdk_/Contoso.htm** and a JavaScript web resource named **sdk_/Scripts/ContosoScript.js** with a CSS web resource named **sdk_/Styles/ContosoStyles.css**.</span><span class="sxs-lookup"><span data-stu-id="bda2c-117">The following example is for an HTML web resource named **sdk_/Contoso.htm** and a JavaScript web resource named **sdk_/Scripts/ContosoScript.js** with a CSS web resource named **sdk_/Styles/ContosoStyles.css**.</span></span>

    ```HTML
    <head>
      <title>HTML Web Resource</title>
      <script src="../ClientGlobalContext.js.aspx" type="text/javascript" ></script>

      <script src="Scripts/ContosoScript.js" type="text/javascript"></script>
      <link href="Styles/ContosoStyles.css" rel="stylesheet" type="text/css" />
    </head>

    ```

> [!NOTE]
> <span data-ttu-id="bda2c-118">Using a relative path including the root WebResources folder, for example, /WebResources/ClientGlobalContext.js.aspx, is not recommended because it can cause the page to lose organization context in a multi-tenant environment.</span><span class="sxs-lookup"><span data-stu-id="bda2c-118">Using a relative path including the root WebResources folder, for example, /WebResources/ClientGlobalContext.js.aspx, is not recommended because it can cause the page to lose organization context in a multi-tenant environment.</span></span>

<span data-ttu-id="bda2c-119">The **ClientGlobalContext.js.aspx** page will include some global event handlers.</span><span class="sxs-lookup"><span data-stu-id="bda2c-119">The **ClientGlobalContext.js.aspx** page will include some global event handlers.</span></span> <span data-ttu-id="bda2c-120">These event handlers will cancel the [onselectstart](https://developer.mozilla.org/en-US/docs/Web/Events/selectstart), [contextmenu](https://developer.mozilla.org/en-US/docs/Web/Events/contextmenu), and [ondragstart](https://developer.mozilla.org/en-US/docs/Web/Events/dragstart) events.</span><span class="sxs-lookup"><span data-stu-id="bda2c-120">These event handlers will cancel the [onselectstart](https://developer.mozilla.org/en-US/docs/Web/Events/selectstart), [contextmenu](https://developer.mozilla.org/en-US/docs/Web/Events/contextmenu), and [ondragstart](https://developer.mozilla.org/en-US/docs/Web/Events/dragstart) events.</span></span> 

### <a name="related-topics"></a><span data-ttu-id="bda2c-121">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="bda2c-121">Related topics</span></span>

[<span data-ttu-id="bda2c-122">Xrm.Utility.getGlobalContext</span><span class="sxs-lookup"><span data-stu-id="bda2c-122">Xrm.Utility.getGlobalContext</span></span>](Xrm-Utility/getGlobalContext.md)

[<span data-ttu-id="bda2c-123">Understand Client API object model</span><span class="sxs-lookup"><span data-stu-id="bda2c-123">Understand Client API object model</span></span>](../understand-clientapi-object-model.md) 

[<span data-ttu-id="bda2c-124">Web resources for Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="bda2c-124">Web resources for Customer Engagement</span></span>](../../web-resources.md)

