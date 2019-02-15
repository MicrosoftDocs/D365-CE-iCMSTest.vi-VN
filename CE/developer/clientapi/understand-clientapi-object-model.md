---
title: Understand the Client API object model in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: conceptual
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 3335aec5-6b48-4ef6-8d49-2833b177f318
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 3f98aed7483dfbdb3c221b6a3ba48b5f7acd97b7
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387942"
---
# <a name="understand-the-client-api-object-model"></a><span data-ttu-id="40c29-102">Understand the Client API object model</span><span class="sxs-lookup"><span data-stu-id="40c29-102">Understand the Client API object model</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="40c29-103">The Client API object model for Customer Engagement provides you objects and methods that you can use to apply custom business logic in Customer Engagement using JavaScript, such as:</span><span class="sxs-lookup"><span data-stu-id="40c29-103">The Client API object model for Customer Engagement provides you objects and methods that you can use to apply custom business logic in Customer Engagement using JavaScript, such as:</span></span>
- <span data-ttu-id="40c29-104">Get or set attribute values.</span><span class="sxs-lookup"><span data-stu-id="40c29-104">Get or set attribute values.</span></span>
- <span data-ttu-id="40c29-105">Show and hide user interface elements.</span><span class="sxs-lookup"><span data-stu-id="40c29-105">Show and hide user interface elements.</span></span>
- <span data-ttu-id="40c29-106">Reference multiple controls per attribute.</span><span class="sxs-lookup"><span data-stu-id="40c29-106">Reference multiple controls per attribute.</span></span>
- <span data-ttu-id="40c29-107">Access multiple forms per entity.</span><span class="sxs-lookup"><span data-stu-id="40c29-107">Access multiple forms per entity.</span></span>
- <span data-ttu-id="40c29-108">Manipulate form navigation items.</span><span class="sxs-lookup"><span data-stu-id="40c29-108">Manipulate form navigation items.</span></span>
- <span data-ttu-id="40c29-109">Interact with the business process flow control.</span><span class="sxs-lookup"><span data-stu-id="40c29-109">Interact with the business process flow control.</span></span>

<span data-ttu-id="40c29-110">Its important that you understand the Customer Engagement Client API object model to effectively write and use your JavaScript code in Customer Enagagement.</span><span class="sxs-lookup"><span data-stu-id="40c29-110">Its important that you understand the Customer Engagement Client API object model to effectively write and use your JavaScript code in Customer Enagagement.</span></span>

## <a name="root-objects-in-the-client-api-object-model"></a><span data-ttu-id="40c29-111">Root objects in the Client API object model</span><span class="sxs-lookup"><span data-stu-id="40c29-111">Root objects in the Client API object model</span></span>

<span data-ttu-id="40c29-112">At the root of the Client API object model are the following contexts and the Xrm object:</span><span class="sxs-lookup"><span data-stu-id="40c29-112">At the root of the Client API object model are the following contexts and the Xrm object:</span></span>

|<span data-ttu-id="40c29-113">Đối tượng</span><span class="sxs-lookup"><span data-stu-id="40c29-113">Object</span></span>|<span data-ttu-id="40c29-114">Mô tả</span><span class="sxs-lookup"><span data-stu-id="40c29-114">Description</span></span>|
|--|--|
|<span data-ttu-id="40c29-115">**executionContext**</span><span class="sxs-lookup"><span data-stu-id="40c29-115">**executionContext**</span></span>|<span data-ttu-id="40c29-116">Represents the execution context for an event in Customer Engagement forms and grids.</span><span class="sxs-lookup"><span data-stu-id="40c29-116">Represents the execution context for an event in Customer Engagement forms and grids.</span></span><br/><span data-ttu-id="40c29-117">More information: [Client API execution context](clientapi-execution-context.md)</span><span class="sxs-lookup"><span data-stu-id="40c29-117">More information: [Client API execution context](clientapi-execution-context.md)</span></span>|
|<span data-ttu-id="40c29-118">**formContext**</span><span class="sxs-lookup"><span data-stu-id="40c29-118">**formContext**</span></span> |<span data-ttu-id="40c29-119">Provides a reference to a form or an item on the form against which the current code executes.</span><span class="sxs-lookup"><span data-stu-id="40c29-119">Provides a reference to a form or an item on the form against which the current code executes.</span></span> <span data-ttu-id="40c29-120">To get the **formContext** object, use the **executionContext**.[getFormContext](reference/executioncontext/getFormContext.md) method.</span><span class="sxs-lookup"><span data-stu-id="40c29-120">To get the **formContext** object, use the **executionContext**.[getFormContext](reference/executioncontext/getFormContext.md) method.</span></span><br/><span data-ttu-id="40c29-121">Thông tin khác: [Ngữ cảnh biểu mẫu API máy khách](clientapi-form-context.md)</span><span class="sxs-lookup"><span data-stu-id="40c29-121">More information: [Client API form context](clientapi-form-context.md)</span></span>|
|<span data-ttu-id="40c29-122">**gridContext**</span><span class="sxs-lookup"><span data-stu-id="40c29-122">**gridContext**</span></span> |<span data-ttu-id="40c29-123">Provides a reference to a grid or a subgrid on a form against which the current code executes.</span><span class="sxs-lookup"><span data-stu-id="40c29-123">Provides a reference to a grid or a subgrid on a form against which the current code executes.</span></span><br/><span data-ttu-id="40c29-124">More information: [Client API grid context](clientapi-grid-context.md)</span><span class="sxs-lookup"><span data-stu-id="40c29-124">More information: [Client API grid context](clientapi-grid-context.md)</span></span>|
|<span data-ttu-id="40c29-125">**Xrm**</span><span class="sxs-lookup"><span data-stu-id="40c29-125">**Xrm**</span></span>| <span data-ttu-id="40c29-126">Provides a global object for performing operations that do not directly impact the data and UI in forms, grids, subgrids, controls, or attributes.</span><span class="sxs-lookup"><span data-stu-id="40c29-126">Provides a global object for performing operations that do not directly impact the data and UI in forms, grids, subgrids, controls, or attributes.</span></span> <span data-ttu-id="40c29-127">For example, navigate forms, create and manage records using Web API.</span><span class="sxs-lookup"><span data-stu-id="40c29-127">For example, navigate forms, create and manage records using Web API.</span></span><br/><span data-ttu-id="40c29-128">More information: [Client API Xrm object](clientapi-xrm.md)</span><span class="sxs-lookup"><span data-stu-id="40c29-128">More information: [Client API Xrm object](clientapi-xrm.md)</span></span>|

### <a name="related-topics"></a><span data-ttu-id="40c29-129">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="40c29-129">Related topics</span></span>

[<span data-ttu-id="40c29-130">Client API global context</span><span class="sxs-lookup"><span data-stu-id="40c29-130">Client API global context</span></span>](clientapi-xrm.md#client-api-global-context)

[<span data-ttu-id="40c29-131">Client API reference</span><span class="sxs-lookup"><span data-stu-id="40c29-131">Client API reference</span></span>](reference.md)








