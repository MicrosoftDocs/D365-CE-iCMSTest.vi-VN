---
title: movePrevious (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 649fe7b0-016d-409f-ba3c-b14e0f1953e0
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 536fc17d8e4970726651a6bf910c2d14bc80f488
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386332"
---
# <a name="moveprevious-client-api-reference"></a><span data-ttu-id="9b412-102">movePrevious (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="9b412-102">movePrevious (Client API reference)</span></span>

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/movePrevious-description.md](./includes/movePrevious-description.md)]

<span data-ttu-id="9b412-103">You can also move to a previous stage in a different entity.</span><span class="sxs-lookup"><span data-stu-id="9b412-103">You can also move to a previous stage in a different entity.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b412-104">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="9b412-104">Syntax</span></span>

`formContext.data.process.movePrevious(callbackFunction);`

## <a name="parameters"></a><span data-ttu-id="9b412-105">Tham số</span><span class="sxs-lookup"><span data-stu-id="9b412-105">Parameters</span></span>

<table style="width:100%">
<tr>
<th><span data-ttu-id="9b412-106">Tên</span><span class="sxs-lookup"><span data-stu-id="9b412-106">Name</span></span></th>
<th><span data-ttu-id="9b412-107">Loại</span><span class="sxs-lookup"><span data-stu-id="9b412-107">Type</span></span></th>
<th><span data-ttu-id="9b412-108">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="9b412-108">Required</span></span></th>
<th><span data-ttu-id="9b412-109">Mô tả</span><span class="sxs-lookup"><span data-stu-id="9b412-109">Description</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="9b412-110">callbackFunction</span><span class="sxs-lookup"><span data-stu-id="9b412-110">callbackFunction</span></span></td>
<td><span data-ttu-id="9b412-111">Hàm</span><span class="sxs-lookup"><span data-stu-id="9b412-111">Function</span></span></td>
<td><span data-ttu-id="9b412-112">Không</span><span class="sxs-lookup"><span data-stu-id="9b412-112">No</span></span></td>
<td><span data-ttu-id="9b412-113">A function to call when the operation is complete.</span><span class="sxs-lookup"><span data-stu-id="9b412-113">A function to call when the operation is complete.</span></span> <span data-ttu-id="9b412-114">This callback function is passed one of the following string values to indicate the status of the operation:</span><span class="sxs-lookup"><span data-stu-id="9b412-114">This callback function is passed one of the following string values to indicate the status of the operation:</span></span>
<table>
<tr>
<th><span data-ttu-id="9b412-115">Value</span><span class="sxs-lookup"><span data-stu-id="9b412-115">Value</span></span></th>
<th><span data-ttu-id="9b412-116">Reason</span><span class="sxs-lookup"><span data-stu-id="9b412-116">Reason</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="9b412-117">success</span><span class="sxs-lookup"><span data-stu-id="9b412-117">success</span></span></td>
<td><span data-ttu-id="9b412-118">The operation succeeded.</span><span class="sxs-lookup"><span data-stu-id="9b412-118">The operation succeeded.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9b412-119">crossEntity</span><span class="sxs-lookup"><span data-stu-id="9b412-119">crossEntity</span></span></td>
<td><span data-ttu-id="9b412-120">The previous stage is for a different entity.</span><span class="sxs-lookup"><span data-stu-id="9b412-120">The previous stage is for a different entity.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9b412-121">beginning</span><span class="sxs-lookup"><span data-stu-id="9b412-121">beginning</span></span></td>
<td><span data-ttu-id="9b412-122">The active stage is the first stage of the active path.</span><span class="sxs-lookup"><span data-stu-id="9b412-122">The active stage is the first stage of the active path.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9b412-123">invalid</span><span class="sxs-lookup"><span data-stu-id="9b412-123">invalid</span></span></td>
<td><span data-ttu-id="9b412-124">The operation failed because the selected stage isn’t the same as the active stage.</span><span class="sxs-lookup"><span data-stu-id="9b412-124">The operation failed because the selected stage isn’t the same as the active stage.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9b412-125">dirtyForm</span><span class="sxs-lookup"><span data-stu-id="9b412-125">dirtyForm</span></span></td>
<td><span data-ttu-id="9b412-126">This value will be returned if the data in the page is not saved.</span><span class="sxs-lookup"><span data-stu-id="9b412-126">This value will be returned if the data in the page is not saved.</span></span></td>
</tr>
</table>
</td>
</tr>
</table>

>[!IMPORTANT]
><span data-ttu-id="9b412-127">This method can only be used when the selected stage and the active stage are the same.</span><span class="sxs-lookup"><span data-stu-id="9b412-127">This method can only be used when the selected stage and the active stage are the same.</span></span> <span data-ttu-id="9b412-128">When your code is initiated from the [OnStageChange](../../events/onstagechange.md) event, the current stage will be selected.</span><span class="sxs-lookup"><span data-stu-id="9b412-128">When your code is initiated from the [OnStageChange](../../events/onstagechange.md) event, the current stage will be selected.</span></span> <span data-ttu-id="9b412-129">When your code is initiated from the [OnStageSelected](../../events/onstageselected.md) event, you should use the [getActiveStage](../activestage/getActiveStage.md) method to verify that the selected stage is also the active stage.</span><span class="sxs-lookup"><span data-stu-id="9b412-129">When your code is initiated from the [OnStageSelected](../../events/onstageselected.md) event, you should use the [getActiveStage](../activestage/getActiveStage.md) method to verify that the selected stage is also the active stage.</span></span> <span data-ttu-id="9b412-130">For any other form event, it isn’t possible to determine which stage is currently selected.</span><span class="sxs-lookup"><span data-stu-id="9b412-130">For any other form event, it isn’t possible to determine which stage is currently selected.</span></span> <span data-ttu-id="9b412-131">For best results, this method should only be used in code that is called in functions initiated by the [OnStageChange](../../events/onstagechange.md) and [OnStageSelected](../../events/onstageselected.md) events.</span><span class="sxs-lookup"><span data-stu-id="9b412-131">For best results, this method should only be used in code that is called in functions initiated by the [OnStageChange](../../events/onstagechange.md) and [OnStageSelected](../../events/onstageselected.md) events.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b412-132">Chú thích</span><span class="sxs-lookup"><span data-stu-id="9b412-132">Remarks</span></span>

<span data-ttu-id="9b412-133">This methods will cause the [OnStageChange](../../events/onstagechange.md) event to occur.</span><span class="sxs-lookup"><span data-stu-id="9b412-133">This methods will cause the [OnStageChange](../../events/onstagechange.md) event to occur.</span></span>

### <a name="related-topics"></a><span data-ttu-id="9b412-134">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="9b412-134">Related topics</span></span>

[<span data-ttu-id="9b412-135">moveNext</span><span class="sxs-lookup"><span data-stu-id="9b412-135">moveNext</span></span>](moveNext.md)

[<span data-ttu-id="9b412-136">formContext.data.process</span><span class="sxs-lookup"><span data-stu-id="9b412-136">formContext.data.process</span></span>](../../formContext-data-process.md)
 


