---
title: Client API Xrm object for Dynamics 365 for Customer Engagement | MicrosoftDocs
description: The topic provides client API reference for Dynamics 365 for Customer Engagement apps.
ms.date: 12/05/2017
ms.service: crm-online
ms.topic: conceptual
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 15272ad9-25d7-499e-9361-a65f789daf20
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 75a08e15ccac6c9a2341fd0c8241560a2d001a5d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387513"
---
# <a name="client-api-xrm-object"></a><span data-ttu-id="c2c02-103">Client API Xrm object</span><span class="sxs-lookup"><span data-stu-id="c2c02-103">Client API Xrm object</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="c2c02-104">The **Xrm** object is globally available to use in your code without having to use the execution context in Client API.</span><span class="sxs-lookup"><span data-stu-id="c2c02-104">The **Xrm** object is globally available to use in your code without having to use the execution context in Client API.</span></span>

## <a name="xrm-object-model"></a><span data-ttu-id="c2c02-105">Xrm object model</span><span class="sxs-lookup"><span data-stu-id="c2c02-105">Xrm object model</span></span> 

<span data-ttu-id="c2c02-106">The following illustration displays the Xrm object model:</span><span class="sxs-lookup"><span data-stu-id="c2c02-106">The following illustration displays the Xrm object model:</span></span>

![Xrm Object Model](../media/ClientAPI-XrmModel.png)

<span data-ttu-id="c2c02-108">Here is the information about each of the namespaces in the Xrm object:</span><span class="sxs-lookup"><span data-stu-id="c2c02-108">Here is the information about each of the namespaces in the Xrm object:</span></span>

|<span data-ttu-id="c2c02-109">Không gian tên</span><span class="sxs-lookup"><span data-stu-id="c2c02-109">Namespace</span></span>  |<span data-ttu-id="c2c02-110">Mô tả</span><span class="sxs-lookup"><span data-stu-id="c2c02-110">Description</span></span>  |
---------|---------------
|[<span data-ttu-id="c2c02-111">Xrm.Device</span><span class="sxs-lookup"><span data-stu-id="c2c02-111">Xrm.Device</span></span>](reference/xrm-device.md)|<span data-ttu-id="c2c02-112">Cung cấp các phương pháp để sử dụng chức năng thiết bị gốc của các thiết bị di động.</span><span class="sxs-lookup"><span data-stu-id="c2c02-112">Provides methods to use native device capabilities of mobile devices.</span></span>|
|[<span data-ttu-id="c2c02-113">Xrm.Encoding</span><span class="sxs-lookup"><span data-stu-id="c2c02-113">Xrm.Encoding</span></span>](reference/xrm-encoding.md)|<span data-ttu-id="c2c02-114">Cung cấp các phương pháp để mã hóa chuỗi.</span><span class="sxs-lookup"><span data-stu-id="c2c02-114">Provides methods to encode strings.</span></span>|
|[<span data-ttu-id="c2c02-115">Xrm.Navigation</span><span class="sxs-lookup"><span data-stu-id="c2c02-115">Xrm.Navigation</span></span>](reference/xrm-navigation.md)|<span data-ttu-id="c2c02-116">Provides methods for navigating forms and items in Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="c2c02-116">Provides methods for navigating forms and items in Customer Engagement.</span></span>|
|[<span data-ttu-id="c2c02-117">Xrm.Panel</span><span class="sxs-lookup"><span data-stu-id="c2c02-117">Xrm.Panel</span></span>](reference/xrm-panel.md)|<span data-ttu-id="c2c02-118">Provides a method to display a web page in the side pane of Customer Engagement form.</span><span class="sxs-lookup"><span data-stu-id="c2c02-118">Provides a method to display a web page in the side pane of Customer Engagement form.</span></span>|
|[<span data-ttu-id="c2c02-119">Xrm.Utility</span><span class="sxs-lookup"><span data-stu-id="c2c02-119">Xrm.Utility</span></span>](reference/xrm-utility.md)|<span data-ttu-id="c2c02-120">Provides a container for useful methods.</span><span class="sxs-lookup"><span data-stu-id="c2c02-120">Provides a container for useful methods.</span></span>|
|[<span data-ttu-id="c2c02-121">Xrm.WebApi</span><span class="sxs-lookup"><span data-stu-id="c2c02-121">Xrm.WebApi</span></span>](reference/xrm-webapi.md)|<span data-ttu-id="c2c02-122">Provides methods to use Web API to create and manage records and execute Web API actions and functions.</span><span class="sxs-lookup"><span data-stu-id="c2c02-122">Provides methods to use Web API to create and manage records and execute Web API actions and functions.</span></span><br/><br/><span data-ttu-id="c2c02-123">[Xrm.WebApi.offline](reference/xrm-webapi/offline.md): Provides methods to create and manage records in the Dynamics 365 for Customer Engagement apps mobile clients while working in the *offline* mode.</span><span class="sxs-lookup"><span data-stu-id="c2c02-123">[Xrm.WebApi.offline](reference/xrm-webapi/offline.md): Provides methods to create and manage records in the Dynamics 365 for Customer Engagement apps mobile clients while working in the *offline* mode.</span></span><br/><br/><span data-ttu-id="c2c02-124">[Xrm.WebApi.online](reference/xrm-webapi/online.md): Provides methods to use Web API to create and manage records and execute Web API actions and functions when connected to the server.</span><span class="sxs-lookup"><span data-stu-id="c2c02-124">[Xrm.WebApi.online](reference/xrm-webapi/online.md): Provides methods to use Web API to create and manage records and execute Web API actions and functions when connected to the server.</span></span>|

## <a name="client-api-global-context"></a><span data-ttu-id="c2c02-125">Client API global context</span><span class="sxs-lookup"><span data-stu-id="c2c02-125">Client API global context</span></span>

<span data-ttu-id="c2c02-126">Use the **Xrm.Utility**.[getGlobalContext](reference/xrm-utility/getGlobalContext.md) method in forms to retrieve information specific to an organization, a user, or the client where script is run without going through the form execution context.</span><span class="sxs-lookup"><span data-stu-id="c2c02-126">Use the **Xrm.Utility**.[getGlobalContext](reference/xrm-utility/getGlobalContext.md) method in forms to retrieve information specific to an organization, a user, or the client where script is run without going through the form execution context.</span></span> <span data-ttu-id="c2c02-127">This is a change from previous versions where you had to use the form context to retrieve global context by using **Xrm.Page.context**.</span><span class="sxs-lookup"><span data-stu-id="c2c02-127">This is a change from previous versions where you had to use the form context to retrieve global context by using **Xrm.Page.context**.</span></span>

> [!NOTE]
> <span data-ttu-id="c2c02-128">**Xrm.Page.context** is [deprecated](/dynamics365/get-started/whats-new/customer-engagement/important-changes-coming#some-client-apis-are-deprecated) in the current release, and you should now use the new **Xrm.Utility.**[getGlobalContext](reference/xrm-utility/getGlobalContext.md) method to get global context in your code targeting version 9.0 or later.</span><span class="sxs-lookup"><span data-stu-id="c2c02-128">**Xrm.Page.context** is [deprecated](/dynamics365/get-started/whats-new/customer-engagement/important-changes-coming#some-client-apis-are-deprecated) in the current release, and you should now use the new **Xrm.Utility.**[getGlobalContext](reference/xrm-utility/getGlobalContext.md) method to get global context in your code targeting version 9.0 or later.</span></span> 

<span data-ttu-id="c2c02-129">To access the global context information in a standalone HTML Web resource, you should include a reference to **ClientGlobalContext.js.aspx** in the web resource, and then use the **GetGlobalContext** function.</span><span class="sxs-lookup"><span data-stu-id="c2c02-129">To access the global context information in a standalone HTML Web resource, you should include a reference to **ClientGlobalContext.js.aspx** in the web resource, and then use the **GetGlobalContext** function.</span></span> <span data-ttu-id="c2c02-130">More information: [GetGlobalContext function and ClientGlobalContext.js.aspx](reference/GetGlobalContext-ClientGlobalContext.js.aspx.md)</span><span class="sxs-lookup"><span data-stu-id="c2c02-130">More information: [GetGlobalContext function and ClientGlobalContext.js.aspx](reference/GetGlobalContext-ClientGlobalContext.js.aspx.md)</span></span>

### <a name="related-topics"></a><span data-ttu-id="c2c02-131">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="c2c02-131">Related topics</span></span>

[<span data-ttu-id="c2c02-132">Understand the Client API object model</span><span class="sxs-lookup"><span data-stu-id="c2c02-132">Understand the Client API object model</span></span>](understand-clientapi-object-model.md)

[<span data-ttu-id="c2c02-133">Các API máy khách không còn dùng</span><span class="sxs-lookup"><span data-stu-id="c2c02-133">Deprecated client APIs</span></span>](/dynamics365/get-started/whats-new/customer-engagement/important-changes-coming#some-client-apis-are-deprecated)
