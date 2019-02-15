---
title: Client API Reference for Dynamics 365 for Customer Engagement apps | MicrosoftDocs
description: The topic provides client API reference for Dynamics 365 for Customer Engagement apps.
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: conceptual
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: ''
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: b4127636434969d4c34262f88b741b3ff1ba40bd
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388820"
---
# <a name="client-api-reference-for-customer-engagement"></a><span data-ttu-id="6c628-103">Client API Reference for Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="6c628-103">Client API Reference for Customer Engagement</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="6c628-104">This section contains reference documentation for client API object model that can be used with JavaScript libraries.</span><span class="sxs-lookup"><span data-stu-id="6c628-104">This section contains reference documentation for client API object model that can be used with JavaScript libraries.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6c628-105">The Client API object model also contains the **Xrm.Internal** namespace, and use of the objects/methods in this namespace isn’t supported.</span><span class="sxs-lookup"><span data-stu-id="6c628-105">The Client API object model also contains the **Xrm.Internal** namespace, and use of the objects/methods in this namespace isn’t supported.</span></span> <span data-ttu-id="6c628-106">These objects, and any parts of the HTML Document Object Model (DOM), are subject to change without notice.</span><span class="sxs-lookup"><span data-stu-id="6c628-106">These objects, and any parts of the HTML Document Object Model (DOM), are subject to change without notice.</span></span> <span data-ttu-id="6c628-107">We recommend that you don’t use these functions or any script that depends on the DOM.</span><span class="sxs-lookup"><span data-stu-id="6c628-107">We recommend that you don’t use these functions or any script that depends on the DOM.</span></span><br/><br/>
<span data-ttu-id="6c628-108">Also, while debugging, you may find methods and objects in the Client API object model that aren’t documented.</span><span class="sxs-lookup"><span data-stu-id="6c628-108">Also, while debugging, you may find methods and objects in the Client API object model that aren’t documented.</span></span> <span data-ttu-id="6c628-109">Only documented objects and methods are supported.</span><span class="sxs-lookup"><span data-stu-id="6c628-109">Only documented objects and methods are supported.</span></span>

<span data-ttu-id="6c628-110">The topics under this section are organized as follows:</span><span class="sxs-lookup"><span data-stu-id="6c628-110">The topics under this section are organized as follows:</span></span>
- <span data-ttu-id="6c628-111">Starts with reference for all the events, collections, and the execution context object.</span><span class="sxs-lookup"><span data-stu-id="6c628-111">Starts with reference for all the events, collections, and the execution context object.</span></span>
- <span data-ttu-id="6c628-112">Continues on to provide information about methods for **attributes** and **controls** in Customer Enagagement that are actually collections that appear under different objects in the Client API object model.</span><span class="sxs-lookup"><span data-stu-id="6c628-112">Continues on to provide information about methods for **attributes** and **controls** in Customer Enagagement that are actually collections that appear under different objects in the Client API object model.</span></span>
- <span data-ttu-id="6c628-113">Provides reference for properties and methods for the **formContext** and **gridContext** objects.</span><span class="sxs-lookup"><span data-stu-id="6c628-113">Provides reference for properties and methods for the **formContext** and **gridContext** objects.</span></span>
- <span data-ttu-id="6c628-114">Finally provides reference for namespaces in the **Xrm** object model.</span><span class="sxs-lookup"><span data-stu-id="6c628-114">Finally provides reference for namespaces in the **Xrm** object model.</span></span> 

### <a name="related-topics"></a><span data-ttu-id="6c628-115">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="6c628-115">Related topics</span></span>

[<span data-ttu-id="6c628-116">Client scripting in Customer Engagement using JavaScript</span><span class="sxs-lookup"><span data-stu-id="6c628-116">Client scripting in Customer Engagement using JavaScript</span></span>](client-scripting.md)

[<span data-ttu-id="6c628-117">Understand the Client API object model</span><span class="sxs-lookup"><span data-stu-id="6c628-117">Understand the Client API object model</span></span>](understand-clientapi-object-model.md)

[<span data-ttu-id="6c628-118">Developer Guide for Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="6c628-118">Developer Guide for Dynamics 365 for Customer Engagement apps</span></span>](../developer-guide.md)
