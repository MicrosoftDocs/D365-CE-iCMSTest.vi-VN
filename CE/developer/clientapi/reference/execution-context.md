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
ms.openlocfilehash: d4df59501df501cab84a0e7cbe749df7dbf695a5
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385465"
---
# <a name="execution-context-client-api-reference"></a><span data-ttu-id="a2642-102">Execution context (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="a2642-102">Execution context (Client API reference)</span></span>

[!INCLUDE[](../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="a2642-103">The execution context defines the event context in which your code executes.</span><span class="sxs-lookup"><span data-stu-id="a2642-103">The execution context defines the event context in which your code executes.</span></span> <span data-ttu-id="a2642-104">More information: [Client API execution context](../clientapi-execution-context.md).</span><span class="sxs-lookup"><span data-stu-id="a2642-104">More information: [Client API execution context](../clientapi-execution-context.md).</span></span>

<span data-ttu-id="a2642-105">The execution context object provides the following methods.</span><span class="sxs-lookup"><span data-stu-id="a2642-105">The execution context object provides the following methods.</span></span>

|<span data-ttu-id="a2642-106">Phương pháp</span><span class="sxs-lookup"><span data-stu-id="a2642-106">Method</span></span> |<span data-ttu-id="a2642-107">Mô tả</span><span class="sxs-lookup"><span data-stu-id="a2642-107">Description</span></span> |
|---|---|
|[<span data-ttu-id="a2642-108">getDepth</span><span class="sxs-lookup"><span data-stu-id="a2642-108">getDepth</span></span>](executioncontext/getDepth.md)|<span data-ttu-id="a2642-109">Returns a value that indicates the order in which this handler is executed.</span><span class="sxs-lookup"><span data-stu-id="a2642-109">Returns a value that indicates the order in which this handler is executed.</span></span>|
|[<span data-ttu-id="a2642-110">getEventArgs</span><span class="sxs-lookup"><span data-stu-id="a2642-110">getEventArgs</span></span>](executioncontext/getEventArgs.md)|<span data-ttu-id="a2642-111">Returns an object with methods to manage the **OnSave** event.</span><span class="sxs-lookup"><span data-stu-id="a2642-111">Returns an object with methods to manage the **OnSave** event.</span></span>|
|[<span data-ttu-id="a2642-112">getEventSource</span><span class="sxs-lookup"><span data-stu-id="a2642-112">getEventSource</span></span>](executioncontext/getEventSource.md)|<span data-ttu-id="a2642-113">Returns a reference to the object that the event occurred on.</span><span class="sxs-lookup"><span data-stu-id="a2642-113">Returns a reference to the object that the event occurred on.</span></span>|
|[<span data-ttu-id="a2642-114">getFormContext</span><span class="sxs-lookup"><span data-stu-id="a2642-114">getFormContext</span></span>](executioncontext/getFormContext.md)|<span data-ttu-id="a2642-115">Returns a reference to the form or an item on the form depending on where the method was called.</span><span class="sxs-lookup"><span data-stu-id="a2642-115">Returns a reference to the form or an item on the form depending on where the method was called.</span></span>|
|[<span data-ttu-id="a2642-116">getSharedVariable</span><span class="sxs-lookup"><span data-stu-id="a2642-116">getSharedVariable</span></span>](executioncontext/getSharedVariable.md)|<span data-ttu-id="a2642-117">Retrieves a variable set using the [setSharedVariable](executioncontext/setSharedVariable.md) method.</span><span class="sxs-lookup"><span data-stu-id="a2642-117">Retrieves a variable set using the [setSharedVariable](executioncontext/setSharedVariable.md) method.</span></span>|
|[<span data-ttu-id="a2642-118">setSharedVariable</span><span class="sxs-lookup"><span data-stu-id="a2642-118">setSharedVariable</span></span>](executioncontext/setSharedVariable.md)|<span data-ttu-id="a2642-119">Sets the value of a variable to be used by a handler after the current handler completes.</span><span class="sxs-lookup"><span data-stu-id="a2642-119">Sets the value of a variable to be used by a handler after the current handler completes.</span></span>|

### <a name="related-topics"></a><span data-ttu-id="a2642-120">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="a2642-120">Related topics</span></span>

[<span data-ttu-id="a2642-121">Client API execution context</span><span class="sxs-lookup"><span data-stu-id="a2642-121">Client API execution context</span></span>](../clientapi-execution-context.md)

[<span data-ttu-id="a2642-122">Save event arguments</span><span class="sxs-lookup"><span data-stu-id="a2642-122">Save event arguments</span></span>](save-event-arguments.md)

[<span data-ttu-id="a2642-123">Understand Client API object model</span><span class="sxs-lookup"><span data-stu-id="a2642-123">Understand Client API object model</span></span>](../understand-clientapi-object-model.md) 

