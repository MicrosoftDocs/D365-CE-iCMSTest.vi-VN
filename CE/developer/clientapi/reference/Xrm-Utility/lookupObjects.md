---
title: lookupObjects (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 89123cde-7c66-4c7d-94e4-e287285019f8
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 6458207f70426a4a501b002be7b4b0a5f0bfda53
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385783"
---
# <a name="lookupobjects-client-api-reference"></a><span data-ttu-id="e11c9-102">lookupObjects (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="e11c9-102">lookupObjects (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/lookupObjects-description.md](./includes/lookupObjects-description.md)] 

## <a name="syntax"></a><span data-ttu-id="e11c9-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="e11c9-103">Syntax</span></span>

`Xrm.Utility.lookupObjects(lookupOptions).then(successCallback, cancelCallback)`

## <a name="parameters"></a><span data-ttu-id="e11c9-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="e11c9-104">Parameters</span></span>

<span data-ttu-id="e11c9-105">**lookupOptions**: Object.</span><span class="sxs-lookup"><span data-stu-id="e11c9-105">**lookupOptions**: Object.</span></span> <span data-ttu-id="e11c9-106">Defines the options for opening the lookup dialog.</span><span class="sxs-lookup"><span data-stu-id="e11c9-106">Defines the options for opening the lookup dialog.</span></span> <span data-ttu-id="e11c9-107">Has the following properties:</span><span class="sxs-lookup"><span data-stu-id="e11c9-107">Has the following properties:</span></span>

|<span data-ttu-id="e11c9-108">Property Name</span><span class="sxs-lookup"><span data-stu-id="e11c9-108">Property Name</span></span> |<span data-ttu-id="e11c9-109">Loại</span><span class="sxs-lookup"><span data-stu-id="e11c9-109">Type</span></span> |<span data-ttu-id="e11c9-110">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="e11c9-110">Required</span></span> |<span data-ttu-id="e11c9-111">Mô tả</span><span class="sxs-lookup"><span data-stu-id="e11c9-111">Description</span></span> |
|---|---|---|---|
|<span data-ttu-id="e11c9-112">allowMultiSelect</span><span class="sxs-lookup"><span data-stu-id="e11c9-112">allowMultiSelect</span></span>|<span data-ttu-id="e11c9-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="e11c9-113">Boolean</span></span>|<span data-ttu-id="e11c9-114">Không</span><span class="sxs-lookup"><span data-stu-id="e11c9-114">No</span></span>|<span data-ttu-id="e11c9-115">Indicates whether the lookup allows more than one item to be selected.</span><span class="sxs-lookup"><span data-stu-id="e11c9-115">Indicates whether the lookup allows more than one item to be selected.</span></span>|
|<span data-ttu-id="e11c9-116">defaultEntityType</span><span class="sxs-lookup"><span data-stu-id="e11c9-116">defaultEntityType</span></span>|<span data-ttu-id="e11c9-117">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="e11c9-117">String</span></span>|<span data-ttu-id="e11c9-118">Không</span><span class="sxs-lookup"><span data-stu-id="e11c9-118">No</span></span>|<span data-ttu-id="e11c9-119">The default entity type to use.</span><span class="sxs-lookup"><span data-stu-id="e11c9-119">The default entity type to use.</span></span>|
|<span data-ttu-id="e11c9-120">defaultViewId</span><span class="sxs-lookup"><span data-stu-id="e11c9-120">defaultViewId</span></span>|<span data-ttu-id="e11c9-121">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="e11c9-121">String</span></span>|<span data-ttu-id="e11c9-122">Không</span><span class="sxs-lookup"><span data-stu-id="e11c9-122">No</span></span>|<span data-ttu-id="e11c9-123">The default view to use.</span><span class="sxs-lookup"><span data-stu-id="e11c9-123">The default view to use.</span></span>|
|<span data-ttu-id="e11c9-124">entityTypes</span><span class="sxs-lookup"><span data-stu-id="e11c9-124">entityTypes</span></span>|<span data-ttu-id="e11c9-125">Mảng</span><span class="sxs-lookup"><span data-stu-id="e11c9-125">Array</span></span>|<span data-ttu-id="e11c9-126">Không</span><span class="sxs-lookup"><span data-stu-id="e11c9-126">No</span></span>|<span data-ttu-id="e11c9-127">The entity types to display.</span><span class="sxs-lookup"><span data-stu-id="e11c9-127">The entity types to display.</span></span>|
|<span data-ttu-id="e11c9-128">showBarcodeScanner</span><span class="sxs-lookup"><span data-stu-id="e11c9-128">showBarcodeScanner</span></span>|<span data-ttu-id="e11c9-129">Boolean</span><span class="sxs-lookup"><span data-stu-id="e11c9-129">Boolean</span></span>|<span data-ttu-id="e11c9-130">Không</span><span class="sxs-lookup"><span data-stu-id="e11c9-130">No</span></span>|<span data-ttu-id="e11c9-131">Indicates whether the lookup control should show the barcode scanner in mobile clients.</span><span class="sxs-lookup"><span data-stu-id="e11c9-131">Indicates whether the lookup control should show the barcode scanner in mobile clients.</span></span>|
|<span data-ttu-id="e11c9-132">viewIds</span><span class="sxs-lookup"><span data-stu-id="e11c9-132">viewIds</span></span>|<span data-ttu-id="e11c9-133">Mảng</span><span class="sxs-lookup"><span data-stu-id="e11c9-133">Array</span></span>|<span data-ttu-id="e11c9-134">Không</span><span class="sxs-lookup"><span data-stu-id="e11c9-134">No</span></span>|<span data-ttu-id="e11c9-135">The views to be available in the view picker.</span><span class="sxs-lookup"><span data-stu-id="e11c9-135">The views to be available in the view picker.</span></span> <span data-ttu-id="e11c9-136">Only system views are supported.</span><span class="sxs-lookup"><span data-stu-id="e11c9-136">Only system views are supported.</span></span>|
|<span data-ttu-id="e11c9-137">successCallback</span><span class="sxs-lookup"><span data-stu-id="e11c9-137">successCallback</span></span> |<span data-ttu-id="e11c9-138">Hàm</span><span class="sxs-lookup"><span data-stu-id="e11c9-138">Function</span></span> |<span data-ttu-id="e11c9-139">Có</span><span class="sxs-lookup"><span data-stu-id="e11c9-139">Yes</span></span> |<span data-ttu-id="e11c9-140">A function to call when the lookup control is invoked.</span><span class="sxs-lookup"><span data-stu-id="e11c9-140">A function to call when the lookup control is invoked.</span></span> <span data-ttu-id="e11c9-141">An object with the following properties is passed:</span><span class="sxs-lookup"><span data-stu-id="e11c9-141">An object with the following properties is passed:</span></span><br/><span data-ttu-id="e11c9-142">- **entityType**: String.</span><span class="sxs-lookup"><span data-stu-id="e11c9-142">- **entityType**: String.</span></span> <span data-ttu-id="e11c9-143">Entity type of the record selected in the lookup control.</span><span class="sxs-lookup"><span data-stu-id="e11c9-143">Entity type of the record selected in the lookup control.</span></span><br/><span data-ttu-id="e11c9-144">- **id**: String.</span><span class="sxs-lookup"><span data-stu-id="e11c9-144">- **id**: String.</span></span> <span data-ttu-id="e11c9-145">ID of the record selected in the lookup control.</span><span class="sxs-lookup"><span data-stu-id="e11c9-145">ID of the record selected in the lookup control.</span></span><br/><span data-ttu-id="e11c9-146">- **name**: String.</span><span class="sxs-lookup"><span data-stu-id="e11c9-146">- **name**: String.</span></span> <span data-ttu-id="e11c9-147">Name of the record selected in the lookup control.</span><span class="sxs-lookup"><span data-stu-id="e11c9-147">Name of the record selected in the lookup control.</span></span>|
|<span data-ttu-id="e11c9-148">errorCallback</span><span class="sxs-lookup"><span data-stu-id="e11c9-148">errorCallback</span></span> |<span data-ttu-id="e11c9-149">Hàm</span><span class="sxs-lookup"><span data-stu-id="e11c9-149">Function</span></span> |<span data-ttu-id="e11c9-150">Có</span><span class="sxs-lookup"><span data-stu-id="e11c9-150">Yes</span></span> |<span data-ttu-id="e11c9-151">A function to call when you cancel the lookup control or the operation fails.</span><span class="sxs-lookup"><span data-stu-id="e11c9-151">A function to call when you cancel the lookup control or the operation fails.</span></span>  |


### <a name="related-topics"></a><span data-ttu-id="e11c9-152">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="e11c9-152">Related topics</span></span>

[<span data-ttu-id="e11c9-153">Xrm.Utility</span><span class="sxs-lookup"><span data-stu-id="e11c9-153">Xrm.Utility</span></span>](../xrm-utility.md)
