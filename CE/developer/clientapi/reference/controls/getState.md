---
title: getState (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 199d1344-351a-44ee-8c43-f6b00b85a793
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 31f19c192efddd8d164783a0147f52494f9a2051
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387467"
---
# <a name="getstate-client-api-reference"></a><span data-ttu-id="fdc97-102">getState (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="fdc97-102">getState (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="fdc97-103">Returns the state of the timer control.</span><span class="sxs-lookup"><span data-stu-id="fdc97-103">Returns the state of the timer control.</span></span>

<span data-ttu-id="fdc97-104">This method is only supported for [Unified Interface](/dynamics365/get-started/whats-new/customer-engagement/new-in-july-2017-update#unified-interface-framework-for-new-apps).</span><span class="sxs-lookup"><span data-stu-id="fdc97-104">This method is only supported for [Unified Interface](/dynamics365/get-started/whats-new/customer-engagement/new-in-july-2017-update#unified-interface-framework-for-new-apps).</span></span> 

## <a name="control-types-supported"></a><span data-ttu-id="fdc97-105">Control types supported</span><span class="sxs-lookup"><span data-stu-id="fdc97-105">Control types supported</span></span>

<span data-ttu-id="fdc97-106">Đồng hồ hẹn giờ</span><span class="sxs-lookup"><span data-stu-id="fdc97-106">Timer</span></span>

## <a name="syntax"></a><span data-ttu-id="fdc97-107">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="fdc97-107">Syntax</span></span>

`formContext.getControl(arg).getState();`

## <a name="return-value"></a><span data-ttu-id="fdc97-108">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="fdc97-108">Return Value</span></span>

<span data-ttu-id="fdc97-109">**Type**: Number</span><span class="sxs-lookup"><span data-stu-id="fdc97-109">**Type**: Number</span></span>

<span data-ttu-id="fdc97-110">**Description**: Returns one of the following values:</span><span class="sxs-lookup"><span data-stu-id="fdc97-110">**Description**: Returns one of the following values:</span></span>

|<span data-ttu-id="fdc97-111">Value</span><span class="sxs-lookup"><span data-stu-id="fdc97-111">Value</span></span> | <span data-ttu-id="fdc97-112">Tiểu bang</span><span class="sxs-lookup"><span data-stu-id="fdc97-112">State</span></span> |
|--|--|
|<span data-ttu-id="fdc97-113">1</span><span class="sxs-lookup"><span data-stu-id="fdc97-113">1</span></span> | <span data-ttu-id="fdc97-114">Not Set</span><span class="sxs-lookup"><span data-stu-id="fdc97-114">Not Set</span></span>|
|<span data-ttu-id="fdc97-115">2</span><span class="sxs-lookup"><span data-stu-id="fdc97-115">2</span></span> | <span data-ttu-id="fdc97-116">In progress</span><span class="sxs-lookup"><span data-stu-id="fdc97-116">In progress</span></span>|
|<span data-ttu-id="fdc97-117">3</span><span class="sxs-lookup"><span data-stu-id="fdc97-117">3</span></span> | <span data-ttu-id="fdc97-118">Cảnh báo</span><span class="sxs-lookup"><span data-stu-id="fdc97-118">Warning</span></span>|
|<span data-ttu-id="fdc97-119">4</span><span class="sxs-lookup"><span data-stu-id="fdc97-119">4</span></span> | <span data-ttu-id="fdc97-120">Violated</span><span class="sxs-lookup"><span data-stu-id="fdc97-120">Violated</span></span>|
|<span data-ttu-id="fdc97-121">5</span><span class="sxs-lookup"><span data-stu-id="fdc97-121">5</span></span> | <span data-ttu-id="fdc97-122">Success</span><span class="sxs-lookup"><span data-stu-id="fdc97-122">Success</span></span>|
|<span data-ttu-id="fdc97-123">6</span><span class="sxs-lookup"><span data-stu-id="fdc97-123">6</span></span> | <span data-ttu-id="fdc97-124">Expired</span><span class="sxs-lookup"><span data-stu-id="fdc97-124">Expired</span></span>|
|<span data-ttu-id="fdc97-125">7</span><span class="sxs-lookup"><span data-stu-id="fdc97-125">7</span></span> | <span data-ttu-id="fdc97-126">Đã hủy</span><span class="sxs-lookup"><span data-stu-id="fdc97-126">Canceled</span></span>|
|<span data-ttu-id="fdc97-127">8</span><span class="sxs-lookup"><span data-stu-id="fdc97-127">8</span></span> | <span data-ttu-id="fdc97-128">Paused</span><span class="sxs-lookup"><span data-stu-id="fdc97-128">Paused</span></span>|

### <a name="related-topics"></a><span data-ttu-id="fdc97-129">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="fdc97-129">Related topics</span></span>

[<span data-ttu-id="fdc97-130">Kiểm soát</span><span class="sxs-lookup"><span data-stu-id="fdc97-130">Controls</span></span>](../controls.md)
