---
title: Events in forms and grids in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 9fb38429-55ef-45ce-a3a3-e649e1be89d0
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 998ad4c1cd5a1a47e88e564feb9e940503c1ae1f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386490"
---
# <a name="events-in-forms-and-grids-in-customer-engagement"></a><span data-ttu-id="efe13-102">Events in forms and grids in Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="efe13-102">Events in forms and grids in Customer Engagement</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="efe13-103">All client-side code is initiated by events.</span><span class="sxs-lookup"><span data-stu-id="efe13-103">All client-side code is initiated by events.</span></span> <span data-ttu-id="efe13-104">In Customer Engagement, you associate a specific function in a JavaScript library ([Script web resource](../script-jscript-web-resources.md)) to be executed when an event occurs.</span><span class="sxs-lookup"><span data-stu-id="efe13-104">In Customer Engagement, you associate a specific function in a JavaScript library ([Script web resource](../script-jscript-web-resources.md)) to be executed when an event occurs.</span></span> <span data-ttu-id="efe13-105">This function is called an *event handler*.</span><span class="sxs-lookup"><span data-stu-id="efe13-105">This function is called an *event handler*.</span></span> <span data-ttu-id="efe13-106">Each event handler specifies a single function within a JavaScript library and any parameters that can be passed to the function.</span><span class="sxs-lookup"><span data-stu-id="efe13-106">Each event handler specifies a single function within a JavaScript library and any parameters that can be passed to the function.</span></span>

<span data-ttu-id="efe13-107">You can associate event handlers to only some events using the UI.</span><span class="sxs-lookup"><span data-stu-id="efe13-107">You can associate event handlers to only some events using the UI.</span></span> <span data-ttu-id="efe13-108">For events that are not available to be associated through UI, Client API provides methods that can be used to attach event handlers to such events.</span><span class="sxs-lookup"><span data-stu-id="efe13-108">For events that are not available to be associated through UI, Client API provides methods that can be used to attach event handlers to such events.</span></span> 

## <a name="add-or-remove-event-handler-function-to-event-using-ui"></a><span data-ttu-id="efe13-109">Add or remove event handler function to event using UI</span><span class="sxs-lookup"><span data-stu-id="efe13-109">Add or remove event handler function to event using UI</span></span>

<span data-ttu-id="efe13-110">Use the **Event Handlers** section of the **Form Properties** dialog box to associate your script with an event for forms and fields.</span><span class="sxs-lookup"><span data-stu-id="efe13-110">Use the **Event Handlers** section of the **Form Properties** dialog box to associate your script with an event for forms and fields.</span></span>

![Event Handler section in Form Properties](../media/Form-EventHandlers.png)

## <a name="add-or-remove-event-handler-function-to-event-using-code"></a><span data-ttu-id="efe13-112">Add or remove event handler function to event using code</span><span class="sxs-lookup"><span data-stu-id="efe13-112">Add or remove event handler function to event using code</span></span>

<span data-ttu-id="efe13-113">Using the following methods to add and remove event handler for events that cannot be associated through UI:</span><span class="sxs-lookup"><span data-stu-id="efe13-113">Using the following methods to add and remove event handler for events that cannot be associated through UI:</span></span>

|<span data-ttu-id="efe13-114">Sự kiện</span><span class="sxs-lookup"><span data-stu-id="efe13-114">Events</span></span> |<span data-ttu-id="efe13-115">Event handler</span><span class="sxs-lookup"><span data-stu-id="efe13-115">Event handler</span></span>|
|-------|-------|
|<span data-ttu-id="efe13-116">Attribute [OnChange](reference/events/attribute-onchange.md)</span><span class="sxs-lookup"><span data-stu-id="efe13-116">Attribute [OnChange](reference/events/attribute-onchange.md)</span></span> | <span data-ttu-id="efe13-117">[addOnChange](reference/attributes/addonchange.md) and [removeOnChange](reference/attributes/removeOnchange.md) methods</span><span class="sxs-lookup"><span data-stu-id="efe13-117">[addOnChange](reference/attributes/addonchange.md) and [removeOnChange](reference/attributes/removeOnchange.md) methods</span></span>|
|<span data-ttu-id="efe13-118">Form [OnLoad](reference/events/form-onload.md)</span><span class="sxs-lookup"><span data-stu-id="efe13-118">Form [OnLoad](reference/events/form-onload.md)</span></span>| <span data-ttu-id="efe13-119">formContext.ui [addOnLoad](reference/formcontext-ui/addonload.md) and [removeOnLoad](reference/formcontext-ui/removeonload.md) methods</span><span class="sxs-lookup"><span data-stu-id="efe13-119">formContext.ui [addOnLoad](reference/formcontext-ui/addonload.md) and [removeOnLoad](reference/formcontext-ui/removeonload.md) methods</span></span>|
|<span data-ttu-id="efe13-120">Form data [OnLoad](reference/events/form-data-onload.md)</span><span class="sxs-lookup"><span data-stu-id="efe13-120">Form data [OnLoad](reference/events/form-data-onload.md)</span></span>| <span data-ttu-id="efe13-121">formContext.data [addOnLoad](reference/formcontext-data/addonload.md) and [removeOnLoad](reference/formcontext-data/removeonload.md) methods</span><span class="sxs-lookup"><span data-stu-id="efe13-121">formContext.data [addOnLoad](reference/formcontext-data/addonload.md) and [removeOnLoad](reference/formcontext-data/removeonload.md) methods</span></span>|
|<span data-ttu-id="efe13-122">Form [OnSave](reference/events/form-onsave.md)</span><span class="sxs-lookup"><span data-stu-id="efe13-122">Form [OnSave](reference/events/form-onsave.md)</span></span>| <span data-ttu-id="efe13-123">[addOnSave](reference/formcontext-data-entity/addonsave.md) and [removeOnSave](reference/formcontext-data-entity/removeonsave.md) methods</span><span class="sxs-lookup"><span data-stu-id="efe13-123">[addOnSave](reference/formcontext-data-entity/addonsave.md) and [removeOnSave](reference/formcontext-data-entity/removeonsave.md) methods</span></span>|
|<span data-ttu-id="efe13-124">Lookup control [PreSearch](reference/events/presearch.md)</span><span class="sxs-lookup"><span data-stu-id="efe13-124">Lookup control [PreSearch](reference/events/presearch.md)</span></span>| <span data-ttu-id="efe13-125">[addPreSearch](reference/controls/addpresearch.md) and [removePreSearch](reference/controls/removepresearch.md) methods</span><span class="sxs-lookup"><span data-stu-id="efe13-125">[addPreSearch](reference/controls/addpresearch.md) and [removePreSearch](reference/controls/removepresearch.md) methods</span></span>|
|<span data-ttu-id="efe13-126">kbsearch control [OnResultOpened](reference/events/onresultopened.md)</span><span class="sxs-lookup"><span data-stu-id="efe13-126">kbsearch control [OnResultOpened](reference/events/onresultopened.md)</span></span>|<span data-ttu-id="efe13-127">[addOnResultOpened](reference/controls/addOnResultOpened.md) and [removeOnResultOpened](reference/controls/removeOnResultOpened.md) methods</span><span class="sxs-lookup"><span data-stu-id="efe13-127">[addOnResultOpened](reference/controls/addOnResultOpened.md) and [removeOnResultOpened](reference/controls/removeOnResultOpened.md) methods</span></span>|
|<span data-ttu-id="efe13-128">kbsearch control [OnSelection](reference/events/onselection.md)</span><span class="sxs-lookup"><span data-stu-id="efe13-128">kbsearch control [OnSelection](reference/events/onselection.md)</span></span>|<span data-ttu-id="efe13-129">[addOnSelection](reference/controls/addOnSelection.md) and [removeOnSelection](reference/controls/removeOnSelection.md) methods</span><span class="sxs-lookup"><span data-stu-id="efe13-129">[addOnSelection](reference/controls/addOnSelection.md) and [removeOnSelection](reference/controls/removeOnSelection.md) methods</span></span>|
|<span data-ttu-id="efe13-130">kbsearch control [PostSearch](reference/events/postsearch.md)</span><span class="sxs-lookup"><span data-stu-id="efe13-130">kbsearch control [PostSearch](reference/events/postsearch.md)</span></span>|<span data-ttu-id="efe13-131">[addOnPostSearch](reference/controls/addOnPostSearch.md) and [removeOnPostSearch](reference/controls/removeOnPostSearch.md) methods</span><span class="sxs-lookup"><span data-stu-id="efe13-131">[addOnPostSearch](reference/controls/addOnPostSearch.md) and [removeOnPostSearch](reference/controls/removeOnPostSearch.md) methods</span></span>|

>[!IMPORTANT]
><span data-ttu-id="efe13-132">The execution context is automatically passed as the first parameter to functions that are set using the code.</span><span class="sxs-lookup"><span data-stu-id="efe13-132">The execution context is automatically passed as the first parameter to functions that are set using the code.</span></span> <span data-ttu-id="efe13-133">More information: [Client API execution context](clientapi-execution-context.md)</span><span class="sxs-lookup"><span data-stu-id="efe13-133">More information: [Client API execution context](clientapi-execution-context.md)</span></span> 

## <a name="form-event-pipeline"></a><span data-ttu-id="efe13-134">Form event pipeline</span><span class="sxs-lookup"><span data-stu-id="efe13-134">Form event pipeline</span></span>
<span data-ttu-id="efe13-135">You can define up to 50 event handlers for each event.</span><span class="sxs-lookup"><span data-stu-id="efe13-135">You can define up to 50 event handlers for each event.</span></span> <span data-ttu-id="efe13-136">Each event handler is executed in the order that it is displayed in the **Event Handlers** section in the **Events** tab of the **Form Properties** dialog box.</span><span class="sxs-lookup"><span data-stu-id="efe13-136">Each event handler is executed in the order that it is displayed in the **Event Handlers** section in the **Events** tab of the **Form Properties** dialog box.</span></span>

<span data-ttu-id="efe13-137">Use the [setSharedVariable](reference/executioncontext/setSharedVariable.md) and [getSharedVariable](reference/executioncontext/getSharedVariable.md) methods to pass a common variable between event handlers (functions).</span><span class="sxs-lookup"><span data-stu-id="efe13-137">Use the [setSharedVariable](reference/executioncontext/setSharedVariable.md) and [getSharedVariable](reference/executioncontext/getSharedVariable.md) methods to pass a common variable between event handlers (functions).</span></span> <span data-ttu-id="efe13-138">Use the execution context [getDepth](reference/executioncontext/getDepth.md) method to know the sequence that an event handler is being executed in relative to other event handlers.</span><span class="sxs-lookup"><span data-stu-id="efe13-138">Use the execution context [getDepth](reference/executioncontext/getDepth.md) method to know the sequence that an event handler is being executed in relative to other event handlers.</span></span> 

### <a name="related-topics"></a><span data-ttu-id="efe13-139">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="efe13-139">Related topics</span></span>

[<span data-ttu-id="efe13-140">Understand the Client API object model</span><span class="sxs-lookup"><span data-stu-id="efe13-140">Understand the Client API object model</span></span>](understand-clientapi-object-model.md)

[<span data-ttu-id="efe13-141">Client API execution context</span><span class="sxs-lookup"><span data-stu-id="efe13-141">Client API execution context</span></span>](clientapi-execution-context.md)

[<span data-ttu-id="efe13-142">Events (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="efe13-142">Events (Client API reference)</span></span>](reference/events.md)

