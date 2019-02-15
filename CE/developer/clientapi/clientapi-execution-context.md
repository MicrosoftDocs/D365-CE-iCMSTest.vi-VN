---
title: Client API execution context in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: conceptual
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 1fcbf0fd-4e47-4352-a555-9315f7e57331
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: c2437676fb7b4c61ba4f538309d1282946074865
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388350"
---
# <a name="client-api-execution-context"></a><span data-ttu-id="81603-102">Client API execution context</span><span class="sxs-lookup"><span data-stu-id="81603-102">Client API execution context</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="81603-103">The execution context defines the event context in which your code executes.</span><span class="sxs-lookup"><span data-stu-id="81603-103">The execution context defines the event context in which your code executes.</span></span> <span data-ttu-id="81603-104">The execution context is passed when an event occurs on a form or grid, which you can use it in your event handler to perform various tasks such as determine [formContext](clientapi-form-context.md) or [gridContext](clientapi-grid-context.md), or manage the save event.</span><span class="sxs-lookup"><span data-stu-id="81603-104">The execution context is passed when an event occurs on a form or grid, which you can use it in your event handler to perform various tasks such as determine [formContext](clientapi-form-context.md) or [gridContext](clientapi-grid-context.md), or manage the save event.</span></span> 

<span data-ttu-id="81603-105">The execution context is passed in one of the following ways:</span><span class="sxs-lookup"><span data-stu-id="81603-105">The execution context is passed in one of the following ways:</span></span>

- <span data-ttu-id="81603-106">**Defining event handlers using UI**: The execution context is an *optional* parameter that can be passed to a JavaScript library function through an event handler.</span><span class="sxs-lookup"><span data-stu-id="81603-106">**Defining event handlers using UI**: The execution context is an *optional* parameter that can be passed to a JavaScript library function through an event handler.</span></span> <span data-ttu-id="81603-107">Use the **Pass execution context as first parameter** option in the **Handler Properties** dialog while specify the name of the function to pass the event execution context.</span><span class="sxs-lookup"><span data-stu-id="81603-107">Use the **Pass execution context as first parameter** option in the **Handler Properties** dialog while specify the name of the function to pass the event execution context.</span></span> <span data-ttu-id="81603-108">The execution context is the first parameter passed to a function.</span><span class="sxs-lookup"><span data-stu-id="81603-108">The execution context is the first parameter passed to a function.</span></span><br/><br/>
<span data-ttu-id="81603-109">![Pass execution context](../media/ClientAPI-PassExecutionContext.png)</span><span class="sxs-lookup"><span data-stu-id="81603-109">![Pass execution context](../media/ClientAPI-PassExecutionContext.png)</span></span><br/><br/>

- <span data-ttu-id="81603-110">**Defining event handlers using code**: The execution context is automatically passed as the first parameter to functions set using code.</span><span class="sxs-lookup"><span data-stu-id="81603-110">**Defining event handlers using code**: The execution context is automatically passed as the first parameter to functions set using code.</span></span> <span data-ttu-id="81603-111">For a list of methods that can be used to define event handlers in code, see [Add or remove functions to events using code](events-forms-grids.md#add-or-remove-event-handler-function-to-event-using-code).</span><span class="sxs-lookup"><span data-stu-id="81603-111">For a list of methods that can be used to define event handlers in code, see [Add or remove functions to events using code](events-forms-grids.md#add-or-remove-event-handler-function-to-event-using-code).</span></span> 

<span data-ttu-id="81603-112">The execution context object provides a number of methods to further work with the context.</span><span class="sxs-lookup"><span data-stu-id="81603-112">The execution context object provides a number of methods to further work with the context.</span></span> <span data-ttu-id="81603-113">More information: [Execution context (Client API reference)](reference/execution-context.md)</span><span class="sxs-lookup"><span data-stu-id="81603-113">More information: [Execution context (Client API reference)](reference/execution-context.md)</span></span>


### <a name="related-topics"></a><span data-ttu-id="81603-114">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="81603-114">Related topics</span></span>

 [<span data-ttu-id="81603-115">Client API form context</span><span class="sxs-lookup"><span data-stu-id="81603-115">Client API form context</span></span>](clientapi-form-context.md)<br>
 [<span data-ttu-id="81603-116">Client API grid context</span><span class="sxs-lookup"><span data-stu-id="81603-116">Client API grid context</span></span>](clientapi-grid-context.md)<br>
 [<span data-ttu-id="81603-117">Form and grid context in ribbon actions</span><span class="sxs-lookup"><span data-stu-id="81603-117">Form and grid context in ribbon actions</span></span>](../customize-dev/pass-dynamics-365-data-page-parameter-ribbon-actions.md#form-and-grid-context-in-ribbon-actions)

