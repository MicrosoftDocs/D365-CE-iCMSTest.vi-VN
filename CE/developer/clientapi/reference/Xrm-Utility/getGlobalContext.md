---
title: getGlobalContext (Client API reference) in Dynamics 365 for Customer Engagement apps | MicrosoftDocs
ms.date: 01/23/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: d87e0614-f365-4ed1-992a-741575bb2b7e
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 58f59b22e7b3d3e54fa62c6381dfe749c3bce4cf
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386782"
---
# <a name="getglobalcontext-client-api-reference"></a><span data-ttu-id="b6fc1-102">getGlobalContext (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="b6fc1-102">getGlobalContext (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getGlobalContext-description.md](./includes/getGlobalContext-description.md)]
<span data-ttu-id="b6fc1-103">The method provides access to the global context without going through the form context.</span><span class="sxs-lookup"><span data-stu-id="b6fc1-103">The method provides access to the global context without going through the form context.</span></span> <span data-ttu-id="b6fc1-104">It contains an equivalent of all the methods available for the **Xrm.Page.context** object (now deprecated) to retrieve information specific to the client, organization or user.</span><span class="sxs-lookup"><span data-stu-id="b6fc1-104">It contains an equivalent of all the methods available for the **Xrm.Page.context** object (now deprecated) to retrieve information specific to the client, organization or user.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b6fc1-105">To access the global context information in a standalone HTML Web resource, you should include a reference to **ClientGlobalContext.js.aspx** in the web resource, and then use the **GetGlobalContext** function.</span><span class="sxs-lookup"><span data-stu-id="b6fc1-105">To access the global context information in a standalone HTML Web resource, you should include a reference to **ClientGlobalContext.js.aspx** in the web resource, and then use the **GetGlobalContext** function.</span></span> <span data-ttu-id="b6fc1-106">More information: [GetGlobalContext function and ClientGlobalContext.js.aspx](../GetGlobalContext-ClientGlobalContext.js.aspx.md)</span><span class="sxs-lookup"><span data-stu-id="b6fc1-106">More information: [GetGlobalContext function and ClientGlobalContext.js.aspx](../GetGlobalContext-ClientGlobalContext.js.aspx.md)</span></span> 

## <a name="properties-of-global-context-getglobalcontext"></a><span data-ttu-id="b6fc1-107">Properties of Global Context (getGlobalContext)</span><span class="sxs-lookup"><span data-stu-id="b6fc1-107">Properties of Global Context (getGlobalContext)</span></span>

<span data-ttu-id="b6fc1-108">Use the following properties of global context to return information about the client, organization settings, or user settings:</span><span class="sxs-lookup"><span data-stu-id="b6fc1-108">Use the following properties of global context to return information about the client, organization settings, or user settings:</span></span>

|<span data-ttu-id="b6fc1-109">Thuộc tính</span><span class="sxs-lookup"><span data-stu-id="b6fc1-109">Property</span></span> |<span data-ttu-id="b6fc1-110">Mô tả</span><span class="sxs-lookup"><span data-stu-id="b6fc1-110">Description</span></span> | 
|---|---|
|[<span data-ttu-id="b6fc1-111">client</span><span class="sxs-lookup"><span data-stu-id="b6fc1-111">client</span></span>](getGlobalContext/client.md) | <span data-ttu-id="b6fc1-112">Returns information about the client.</span><span class="sxs-lookup"><span data-stu-id="b6fc1-112">Returns information about the client.</span></span>|
|[<span data-ttu-id="b6fc1-113">organizationSettings</span><span class="sxs-lookup"><span data-stu-id="b6fc1-113">organizationSettings</span></span>](getGlobalContext/organizationSettings.md) | <span data-ttu-id="b6fc1-114">Returns information about the current organization settings.</span><span class="sxs-lookup"><span data-stu-id="b6fc1-114">Returns information about the current organization settings.</span></span>|
|[<span data-ttu-id="b6fc1-115">userSettings</span><span class="sxs-lookup"><span data-stu-id="b6fc1-115">userSettings</span></span>](getGlobalContext/userSettings.md) | <span data-ttu-id="b6fc1-116">Returns information about the current user settings.</span><span class="sxs-lookup"><span data-stu-id="b6fc1-116">Returns information about the current user settings.</span></span>|


## <a name="methods-of-global-context-getglobalcontext"></a><span data-ttu-id="b6fc1-117">Methods of Global Context (getGlobalContext)</span><span class="sxs-lookup"><span data-stu-id="b6fc1-117">Methods of Global Context (getGlobalContext)</span></span>

|<span data-ttu-id="b6fc1-118">Phương pháp</span><span class="sxs-lookup"><span data-stu-id="b6fc1-118">Method</span></span> |<span data-ttu-id="b6fc1-119">Mô tả</span><span class="sxs-lookup"><span data-stu-id="b6fc1-119">Description</span></span> |
|---|---|
|[<span data-ttu-id="b6fc1-120">getAdvancedConfigSetting</span><span class="sxs-lookup"><span data-stu-id="b6fc1-120">getAdvancedConfigSetting</span></span>](getGlobalContext/getAdvancedConfigSetting.md) |<span data-ttu-id="b6fc1-121">Returns information about the advanced configuration settings for the organization.</span><span class="sxs-lookup"><span data-stu-id="b6fc1-121">Returns information about the advanced configuration settings for the organization.</span></span>|
|[<span data-ttu-id="b6fc1-122">getClientUrl</span><span class="sxs-lookup"><span data-stu-id="b6fc1-122">getClientUrl</span></span>](getGlobalContext/getClientUrl.md) |<span data-ttu-id="b6fc1-123">Returns the base URL that was used to access the application.</span><span class="sxs-lookup"><span data-stu-id="b6fc1-123">Returns the base URL that was used to access the application.</span></span>|
|[<span data-ttu-id="b6fc1-124">getCurrentAppName</span><span class="sxs-lookup"><span data-stu-id="b6fc1-124">getCurrentAppName</span></span>](getGlobalContext/getCurrentAppName.md) |<span data-ttu-id="b6fc1-125">Returns the name of the current business app in Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="b6fc1-125">Returns the name of the current business app in Customer Engagement.</span></span>|
|[<span data-ttu-id="b6fc1-126">getCurrentAppProperties</span><span class="sxs-lookup"><span data-stu-id="b6fc1-126">getCurrentAppProperties</span></span>](getGlobalContext/getCurrentAppProperties.md) |<span data-ttu-id="b6fc1-127">Returns the properties of the current business app in Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="b6fc1-127">Returns the properties of the current business app in Customer Engagement.</span></span>|
|[<span data-ttu-id="b6fc1-128">getCurrentAppUrl</span><span class="sxs-lookup"><span data-stu-id="b6fc1-128">getCurrentAppUrl</span></span>](getGlobalContext/getCurrentAppUrl.md) |<span data-ttu-id="b6fc1-129">Returns the URL of the current business app in Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="b6fc1-129">Returns the URL of the current business app in Customer Engagement.</span></span>|
|[<span data-ttu-id="b6fc1-130">getVersion</span><span class="sxs-lookup"><span data-stu-id="b6fc1-130">getVersion</span></span>](getGlobalContext/getVersion.md) |<span data-ttu-id="b6fc1-131">Returns the version number of the Dynamics 365 for Customer Engagement apps instance.</span><span class="sxs-lookup"><span data-stu-id="b6fc1-131">Returns the version number of the Dynamics 365 for Customer Engagement apps instance.</span></span>|
|[<span data-ttu-id="b6fc1-132">isOnPremises</span><span class="sxs-lookup"><span data-stu-id="b6fc1-132">isOnPremises</span></span>](getGlobalContext/isOnPremises.md) |<span data-ttu-id="b6fc1-133">Returns a boolean value indicating if the Customer Engagement instance is hosted on-premises or online.</span><span class="sxs-lookup"><span data-stu-id="b6fc1-133">Returns a boolean value indicating if the Customer Engagement instance is hosted on-premises or online.</span></span>|
|[<span data-ttu-id="b6fc1-134">prependOrgName</span><span class="sxs-lookup"><span data-stu-id="b6fc1-134">prependOrgName</span></span>](getGlobalContext/prependOrgName.md) |<span data-ttu-id="b6fc1-135">Prefixes the current organization's unique name to a string, typically a URL path.</span><span class="sxs-lookup"><span data-stu-id="b6fc1-135">Prefixes the current organization's unique name to a string, typically a URL path.</span></span>|




 



