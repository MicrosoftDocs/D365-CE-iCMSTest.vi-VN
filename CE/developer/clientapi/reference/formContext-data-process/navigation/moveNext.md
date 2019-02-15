---
title: moveNext (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 97640c6a-816b-4d18-9b0b-e79411787c1a
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: e2114249ea3b291a3990aeae929dee4673b5f4e8
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388389"
---
# <a name="movenext-client-api-reference"></a><span data-ttu-id="98d5f-102">moveNext (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="98d5f-102">moveNext (Client API reference)</span></span>

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/moveNext-description.md](./includes/moveNext-description.md)]

<span data-ttu-id="98d5f-103">You can also move to a next stage in a different entity.</span><span class="sxs-lookup"><span data-stu-id="98d5f-103">You can also move to a next stage in a different entity.</span></span> 

## <a name="syntax"></a><span data-ttu-id="98d5f-104">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="98d5f-104">Syntax</span></span>

`formContext.data.process.moveNext(callbackFunction);`

## <a name="parameters"></a><span data-ttu-id="98d5f-105">Tham số</span><span class="sxs-lookup"><span data-stu-id="98d5f-105">Parameters</span></span>

<table style="width:100%">
<tr>
<th><span data-ttu-id="98d5f-106">Tên</span><span class="sxs-lookup"><span data-stu-id="98d5f-106">Name</span></span></th>
<th><span data-ttu-id="98d5f-107">Loại</span><span class="sxs-lookup"><span data-stu-id="98d5f-107">Type</span></span></th>
<th><span data-ttu-id="98d5f-108">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="98d5f-108">Required</span></span></th>
<th><span data-ttu-id="98d5f-109">Mô tả</span><span class="sxs-lookup"><span data-stu-id="98d5f-109">Description</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="98d5f-110">callbackFunction</span><span class="sxs-lookup"><span data-stu-id="98d5f-110">callbackFunction</span></span></td>
<td><span data-ttu-id="98d5f-111">Hàm</span><span class="sxs-lookup"><span data-stu-id="98d5f-111">Function</span></span></td>
<td><span data-ttu-id="98d5f-112">Không</span><span class="sxs-lookup"><span data-stu-id="98d5f-112">No</span></span></td>
<td><span data-ttu-id="98d5f-113">A function to call when the operation is complete.</span><span class="sxs-lookup"><span data-stu-id="98d5f-113">A function to call when the operation is complete.</span></span> <span data-ttu-id="98d5f-114">This callback function is passed one of the following string values to indicate the status of the operation:</span><span class="sxs-lookup"><span data-stu-id="98d5f-114">This callback function is passed one of the following string values to indicate the status of the operation:</span></span>
<table>
<tr>
<th><span data-ttu-id="98d5f-115">Value</span><span class="sxs-lookup"><span data-stu-id="98d5f-115">Value</span></span></th>
<th><span data-ttu-id="98d5f-116">Reason</span><span class="sxs-lookup"><span data-stu-id="98d5f-116">Reason</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="98d5f-117">success</span><span class="sxs-lookup"><span data-stu-id="98d5f-117">success</span></span></td>
<td><span data-ttu-id="98d5f-118">The operation succeeded.</span><span class="sxs-lookup"><span data-stu-id="98d5f-118">The operation succeeded.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98d5f-119">crossEntity</span><span class="sxs-lookup"><span data-stu-id="98d5f-119">crossEntity</span></span></td>
<td><span data-ttu-id="98d5f-120">The next stage is for a different entity.</span><span class="sxs-lookup"><span data-stu-id="98d5f-120">The next stage is for a different entity.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98d5f-121">end</span><span class="sxs-lookup"><span data-stu-id="98d5f-121">end</span></span></td>
<td><span data-ttu-id="98d5f-122">The active stage is the last stage of the active path.</span><span class="sxs-lookup"><span data-stu-id="98d5f-122">The active stage is the last stage of the active path.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98d5f-123">invalid</span><span class="sxs-lookup"><span data-stu-id="98d5f-123">invalid</span></span></td>
<td><span data-ttu-id="98d5f-124">The operation failed because the selected stage isn’t the same as the active stage.</span><span class="sxs-lookup"><span data-stu-id="98d5f-124">The operation failed because the selected stage isn’t the same as the active stage.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98d5f-125">dirtyForm</span><span class="sxs-lookup"><span data-stu-id="98d5f-125">dirtyForm</span></span></td>
<td><span data-ttu-id="98d5f-126">This value will be returned if the data in the page is not saved.</span><span class="sxs-lookup"><span data-stu-id="98d5f-126">This value will be returned if the data in the page is not saved.</span></span></td>
</tr>
</table>
</td>
</tr>
</table>

>[!IMPORTANT]
><span data-ttu-id="98d5f-127">This method can only be used when the selected stage and the active stage are the same.</span><span class="sxs-lookup"><span data-stu-id="98d5f-127">This method can only be used when the selected stage and the active stage are the same.</span></span> <span data-ttu-id="98d5f-128">When your code is initiated from the [OnStageChange](../../events/onstagechange.md) event, the current stage will be selected.</span><span class="sxs-lookup"><span data-stu-id="98d5f-128">When your code is initiated from the [OnStageChange](../../events/onstagechange.md) event, the current stage will be selected.</span></span> <span data-ttu-id="98d5f-129">When your code is initiated from the [OnStageSelected](../../events/onstageselected.md) event, you should use the [getActiveStage](../activestage/getActiveStage.md) method to verify that the selected stage is also the active stage.</span><span class="sxs-lookup"><span data-stu-id="98d5f-129">When your code is initiated from the [OnStageSelected](../../events/onstageselected.md) event, you should use the [getActiveStage](../activestage/getActiveStage.md) method to verify that the selected stage is also the active stage.</span></span> <span data-ttu-id="98d5f-130">For any other form event, it isn’t possible to determine which stage is currently selected.</span><span class="sxs-lookup"><span data-stu-id="98d5f-130">For any other form event, it isn’t possible to determine which stage is currently selected.</span></span> <span data-ttu-id="98d5f-131">For best results, this method should only be used in code that is called in functions initiated by the [OnStageChange](../../events/onstagechange.md) and [OnStageSelected](../../events/onstageselected.md) events.</span><span class="sxs-lookup"><span data-stu-id="98d5f-131">For best results, this method should only be used in code that is called in functions initiated by the [OnStageChange](../../events/onstagechange.md) and [OnStageSelected](../../events/onstageselected.md) events.</span></span>

## <a name="remarks"></a><span data-ttu-id="98d5f-132">Chú thích</span><span class="sxs-lookup"><span data-stu-id="98d5f-132">Remarks</span></span>

<span data-ttu-id="98d5f-133">This methods will cause the [OnStageChange](../../events/onstagechange.md) event to occur.</span><span class="sxs-lookup"><span data-stu-id="98d5f-133">This methods will cause the [OnStageChange](../../events/onstagechange.md) event to occur.</span></span>

### <a name="related-topics"></a><span data-ttu-id="98d5f-134">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="98d5f-134">Related topics</span></span>

[<span data-ttu-id="98d5f-135">movePrevious</span><span class="sxs-lookup"><span data-stu-id="98d5f-135">movePrevious</span></span>](movePrevious.md)

[<span data-ttu-id="98d5f-136">formContext.data.process</span><span class="sxs-lookup"><span data-stu-id="98d5f-136">formContext.data.process</span></span>](../../formContext-data-process.md)
 


