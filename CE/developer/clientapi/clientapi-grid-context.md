---
title: Client API grid context in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 08/29/2018
ms.service: crm-online
ms.topic: conceptual
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: f884d7d4-31e6-4080-acd9-493e81e6b278
author: KumarVivek
ms.author: kvivek
manager: annbe
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 91d7bb9617398aa5d5973ca0b81e12545b7d08dd
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388204"
---
# <a name="client-api-grid-context"></a><span data-ttu-id="41197-102">Client API grid context</span><span class="sxs-lookup"><span data-stu-id="41197-102">Client API grid context</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="41197-103">Grids present data in a tabular format.</span><span class="sxs-lookup"><span data-stu-id="41197-103">Grids present data in a tabular format.</span></span> <span data-ttu-id="41197-104">Grids can span the entire form or can be one of the items on a form; the latter are called **subgrids**.</span><span class="sxs-lookup"><span data-stu-id="41197-104">Grids can span the entire form or can be one of the items on a form; the latter are called **subgrids**.</span></span>

<span data-ttu-id="41197-105">The Client API grid context object provides reference to a subgrid on a form against which the current code is executed.</span><span class="sxs-lookup"><span data-stu-id="41197-105">The Client API grid context object provides reference to a subgrid on a form against which the current code is executed.</span></span> 

> [!NOTE]
> <span data-ttu-id="41197-106">Getting the context of a grid (spanning the entire form) is only supported in ribbon commands.</span><span class="sxs-lookup"><span data-stu-id="41197-106">Getting the context of a grid (spanning the entire form) is only supported in ribbon commands.</span></span> <span data-ttu-id="41197-107">More information: [Form and grid context in ribbon actions](../customize-dev/pass-dynamics-365-data-page-parameter-ribbon-actions.md#form-and-grid-context-in-ribbon-actions)</span><span class="sxs-lookup"><span data-stu-id="41197-107">More information: [Form and grid context in ribbon actions](../customize-dev/pass-dynamics-365-data-page-parameter-ribbon-actions.md#form-and-grid-context-in-ribbon-actions)</span></span>

<span data-ttu-id="41197-108">Use the [formContext](clientapi-form-context.md) object to get an instance of the form where the code is executed, and then retrieve the subgrid control on the form.</span><span class="sxs-lookup"><span data-stu-id="41197-108">Use the [formContext](clientapi-form-context.md) object to get an instance of the form where the code is executed, and then retrieve the subgrid control on the form.</span></span> <span data-ttu-id="41197-109">For example, when you know the name of a subgrid control (say **Contacts** subgrid in the default account form), you can access it using the following code:</span><span class="sxs-lookup"><span data-stu-id="41197-109">For example, when you know the name of a subgrid control (say **Contacts** subgrid in the default account form), you can access it using the following code:</span></span>

```JavaScript
function doSomething(executionContext) {
   var formContext = executionContext.getFormContext(); // get the form Context
   var gridContext = formContext.getControl("Contacts"); // get the grid context

   // Perform operations on the subgrid
}
```

## <a name="related-topics"></a><span data-ttu-id="41197-110">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="41197-110">Related topics</span></span>

[<span data-ttu-id="41197-111">Client API form context</span><span class="sxs-lookup"><span data-stu-id="41197-111">Client API form context</span></span>](clientapi-form-context.md)

[<span data-ttu-id="41197-112">Client API execution context</span><span class="sxs-lookup"><span data-stu-id="41197-112">Client API execution context</span></span>](clientapi-execution-context.md)

[<span data-ttu-id="41197-113">Understand the Client API object model</span><span class="sxs-lookup"><span data-stu-id="41197-113">Understand the Client API object model</span></span>](understand-clientapi-object-model.md)

[<span data-ttu-id="41197-114">Grids and subgrids</span><span class="sxs-lookup"><span data-stu-id="41197-114">Grids and subgrids</span></span>](reference/grids.md)

 

