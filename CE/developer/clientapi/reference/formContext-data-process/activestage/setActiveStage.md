---
title: setActiveStage (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/20/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 9c40a770-f4cb-4230-8893-0527f8472825
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ed51f7f759398a8e4d6286d2dbcb942c8d1c1dea
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385660"
---
# <a name="setactivestage-client-api-reference"></a><span data-ttu-id="32f7f-102">setActiveStage (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="32f7f-102">setActiveStage (Client API reference)</span></span>

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/setActiveStage-description.md](./includes/setActiveStage-description.md)]

## <a name="syntax"></a><span data-ttu-id="32f7f-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="32f7f-103">Syntax</span></span>

`formContext.data.process.setActiveStage(stageId, callbackFunction);`

## <a name="parameters"></a><span data-ttu-id="32f7f-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="32f7f-104">Parameters</span></span>

<table style="width:100%">
<tr>
<th><span data-ttu-id="32f7f-105">Tên</span><span class="sxs-lookup"><span data-stu-id="32f7f-105">Name</span></span></th>
<th><span data-ttu-id="32f7f-106">Loại</span><span class="sxs-lookup"><span data-stu-id="32f7f-106">Type</span></span></th>
<th><span data-ttu-id="32f7f-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="32f7f-107">Required</span></span></th>
<th><span data-ttu-id="32f7f-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="32f7f-108">Description</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="32f7f-109">stageId</span><span class="sxs-lookup"><span data-stu-id="32f7f-109">stageId</span></span></td>
<td><span data-ttu-id="32f7f-110">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="32f7f-110">String</span></span></td>
<td><span data-ttu-id="32f7f-111">Có</span><span class="sxs-lookup"><span data-stu-id="32f7f-111">Yes</span></span></td>
<td><span data-ttu-id="32f7f-112">The ID of the completed stage for the entity to make the active stage.</span><span class="sxs-lookup"><span data-stu-id="32f7f-112">The ID of the completed stage for the entity to make the active stage.</span></span> </td>
</tr>
<tr>
<td><span data-ttu-id="32f7f-113">callbackFunction</span><span class="sxs-lookup"><span data-stu-id="32f7f-113">callbackFunction</span></span></td>
<td><span data-ttu-id="32f7f-114">Hàm</span><span class="sxs-lookup"><span data-stu-id="32f7f-114">Function</span></span></td>
<td><span data-ttu-id="32f7f-115">Không</span><span class="sxs-lookup"><span data-stu-id="32f7f-115">No</span></span></td>
<td><span data-ttu-id="32f7f-116">A function to call when the operation is complete.</span><span class="sxs-lookup"><span data-stu-id="32f7f-116">A function to call when the operation is complete.</span></span> <span data-ttu-id="32f7f-117">This callback function is passed one of the following string values to indicate the status of the operation:</span><span class="sxs-lookup"><span data-stu-id="32f7f-117">This callback function is passed one of the following string values to indicate the status of the operation:</span></span>
<table>
<tr>
<th><span data-ttu-id="32f7f-118">Value</span><span class="sxs-lookup"><span data-stu-id="32f7f-118">Value</span></span></th>
<th><span data-ttu-id="32f7f-119">Reason</span><span class="sxs-lookup"><span data-stu-id="32f7f-119">Reason</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="32f7f-120">success</span><span class="sxs-lookup"><span data-stu-id="32f7f-120">success</span></span></td>
<td><span data-ttu-id="32f7f-121">The operation succeeded.</span><span class="sxs-lookup"><span data-stu-id="32f7f-121">The operation succeeded.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32f7f-122">invalid</span><span class="sxs-lookup"><span data-stu-id="32f7f-122">invalid</span></span></td>
<td><span data-ttu-id="32f7f-123">There are three reasons why this value may be returned:</span><span class="sxs-lookup"><span data-stu-id="32f7f-123">There are three reasons why this value may be returned:</span></span>
<ul>
<li><span data-ttu-id="32f7f-124">The <em>stageId</em> parameter is a non-existent stage ID value.</span><span class="sxs-lookup"><span data-stu-id="32f7f-124">The <em>stageId</em> parameter is a non-existent stage ID value.</span></span></li>
<li><span data-ttu-id="32f7f-125">The active stage isn’t the selected stage.</span><span class="sxs-lookup"><span data-stu-id="32f7f-125">The active stage isn’t the selected stage.</span></span></li>
<li><span data-ttu-id="32f7f-126">The record hasn’t been saved yet.</span><span class="sxs-lookup"><span data-stu-id="32f7f-126">The record hasn’t been saved yet.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="32f7f-127">unreachable</span><span class="sxs-lookup"><span data-stu-id="32f7f-127">unreachable</span></span></td>
<td><span data-ttu-id="32f7f-128">The stage exists on a different path.</span><span class="sxs-lookup"><span data-stu-id="32f7f-128">The stage exists on a different path.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32f7f-129">dirtyForm</span><span class="sxs-lookup"><span data-stu-id="32f7f-129">dirtyForm</span></span></td>
<td><span data-ttu-id="32f7f-130">This value will be returned if the data in the page is not saved.</span><span class="sxs-lookup"><span data-stu-id="32f7f-130">This value will be returned if the data in the page is not saved.</span></span></td>
</tr>
</table>
</td>
</tr>
</table>

>[!IMPORTANT]
><span data-ttu-id="32f7f-131">This method can only be used when the selected stage and the active stage are the same.</span><span class="sxs-lookup"><span data-stu-id="32f7f-131">This method can only be used when the selected stage and the active stage are the same.</span></span> <span data-ttu-id="32f7f-132">When your code is initiated from the [OnStageChange](../../events/onstagechange.md) event, the current stage will be selected.</span><span class="sxs-lookup"><span data-stu-id="32f7f-132">When your code is initiated from the [OnStageChange](../../events/onstagechange.md) event, the current stage will be selected.</span></span> <span data-ttu-id="32f7f-133">When your code is initiated from the [OnStageSelected](../../events/onstageselected.md) event, you should use the [getActiveStage](getActiveStage.md) method to verify that the selected stage is also the active stage.</span><span class="sxs-lookup"><span data-stu-id="32f7f-133">When your code is initiated from the [OnStageSelected](../../events/onstageselected.md) event, you should use the [getActiveStage](getActiveStage.md) method to verify that the selected stage is also the active stage.</span></span> <span data-ttu-id="32f7f-134">For any other form event, it isn’t possible to determine which stage is currently selected.</span><span class="sxs-lookup"><span data-stu-id="32f7f-134">For any other form event, it isn’t possible to determine which stage is currently selected.</span></span> <span data-ttu-id="32f7f-135">For best results, this method should only be used in code that is called in functions initiated by the [OnStageChange](../../events/onstagechange.md) and [OnStageSelected](../../events/onstageselected.md) events.</span><span class="sxs-lookup"><span data-stu-id="32f7f-135">For best results, this method should only be used in code that is called in functions initiated by the [OnStageChange](../../events/onstagechange.md) and [OnStageSelected](../../events/onstageselected.md) events.</span></span>

### <a name="related-topics"></a><span data-ttu-id="32f7f-136">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="32f7f-136">Related topics</span></span>

[<span data-ttu-id="32f7f-137">getActiveStage</span><span class="sxs-lookup"><span data-stu-id="32f7f-137">getActiveStage</span></span>](getActiveStage.md)

[<span data-ttu-id="32f7f-138">formContext.data.process</span><span class="sxs-lookup"><span data-stu-id="32f7f-138">formContext.data.process</span></span>](../../formContext-data-process.md)
 


