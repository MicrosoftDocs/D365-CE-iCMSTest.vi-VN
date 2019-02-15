---
title: addOnLoad (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/10/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 24f34ac9-2a15-478e-980c-588a79d84e8d
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7a3fe61b251d5f75d15c1924cee4c16fb439fa83
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385467"
---
# <a name="addonload-client-api-reference"></a><span data-ttu-id="e3feb-102">addOnLoad (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="e3feb-102">addOnLoad (Client API reference)</span></span>

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/addOnLoad-description.md](./includes/addOnLoad-description.md)]

## <a name="grid-types-supported"></a><span data-ttu-id="e3feb-103">Grid types supported</span><span class="sxs-lookup"><span data-stu-id="e3feb-103">Grid types supported</span></span>

<span data-ttu-id="e3feb-104">Read-only grids</span><span class="sxs-lookup"><span data-stu-id="e3feb-104">Read-only grids</span></span>

## <a name="syntax"></a><span data-ttu-id="e3feb-105">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="e3feb-105">Syntax</span></span>

`gridContext.addOnLoad(myFunction);`

## <a name="parameter"></a><span data-ttu-id="e3feb-106">Tham số</span><span class="sxs-lookup"><span data-stu-id="e3feb-106">Parameter</span></span>

|<span data-ttu-id="e3feb-107">Tên</span><span class="sxs-lookup"><span data-stu-id="e3feb-107">Name</span></span>|<span data-ttu-id="e3feb-108">Loại</span><span class="sxs-lookup"><span data-stu-id="e3feb-108">Type</span></span>|<span data-ttu-id="e3feb-109">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="e3feb-109">Required</span></span>|<span data-ttu-id="e3feb-110">Mô tả</span><span class="sxs-lookup"><span data-stu-id="e3feb-110">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="e3feb-111">myFunction</span><span class="sxs-lookup"><span data-stu-id="e3feb-111">myFunction</span></span>|<span data-ttu-id="e3feb-112">function reference</span><span class="sxs-lookup"><span data-stu-id="e3feb-112">function reference</span></span>|<span data-ttu-id="e3feb-113">Có</span><span class="sxs-lookup"><span data-stu-id="e3feb-113">Yes</span></span>|<span data-ttu-id="e3feb-114">The function to be executed when the subgrid loads.</span><span class="sxs-lookup"><span data-stu-id="e3feb-114">The function to be executed when the subgrid loads.</span></span> <span data-ttu-id="e3feb-115">The function will be added to the bottom of the event handler pipeline.</span><span class="sxs-lookup"><span data-stu-id="e3feb-115">The function will be added to the bottom of the event handler pipeline.</span></span> <span data-ttu-id="e3feb-116">The execution context is automatically passed as the first parameter to the function.</span><span class="sxs-lookup"><span data-stu-id="e3feb-116">The execution context is automatically passed as the first parameter to the function.</span></span> <span data-ttu-id="e3feb-117">See [execution context](../../../clientapi-execution-context.md) for more information.</span><span class="sxs-lookup"><span data-stu-id="e3feb-117">See [execution context](../../../clientapi-execution-context.md) for more information.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3feb-118">Chú thích</span><span class="sxs-lookup"><span data-stu-id="e3feb-118">Remarks</span></span>

<span data-ttu-id="e3feb-119">To get the `gridContext`, see [Getting the grid context](../../grids.md#bkmk_gridcontext).</span><span class="sxs-lookup"><span data-stu-id="e3feb-119">To get the `gridContext`, see [Getting the grid context](../../grids.md#bkmk_gridcontext).</span></span>

## <a name="example"></a><span data-ttu-id="e3feb-120">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="e3feb-120">Example</span></span>

<span data-ttu-id="e3feb-121">Add the myContactsGridOnloadFunction function to the Contacts subgrid **OnLoad** event.</span><span class="sxs-lookup"><span data-stu-id="e3feb-121">Add the myContactsGridOnloadFunction function to the Contacts subgrid **OnLoad** event.</span></span>

```JavaScript
function myFunction(executionContext) {
    var formContext = executionContext.getFormContext(); // get the form context
    var gridContext = formContext.getControl("Contacts");// get the grid context
    var myContactsGridOnloadFunction = function () { console.log("Contacts Subgrid OnLoad event occurred") };
    gridContext.addOnLoad(myContactsGridOnloadFunction);
}
```

### <a name="related-topics"></a><span data-ttu-id="e3feb-122">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="e3feb-122">Related topics</span></span>

[<span data-ttu-id="e3feb-123">removeOnLoad</span><span class="sxs-lookup"><span data-stu-id="e3feb-123">removeOnLoad</span></span>](removeOnLoad.md)



