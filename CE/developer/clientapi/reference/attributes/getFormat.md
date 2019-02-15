---
title: getFormat (Client API reference)| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: e5f97552-4a48-4bf9-b460-6105442e2e6b
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: e32b057e9812a2b55104e8811adaaf2fee515efd
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387299"
---
# <a name="getformat-client-api-reference"></a><span data-ttu-id="fd033-102">getFormat (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="fd033-102">getFormat (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="fd033-103">Returns a string value that represents formatting options for the attribute.</span><span class="sxs-lookup"><span data-stu-id="fd033-103">Returns a string value that represents formatting options for the attribute.</span></span> 

## <a name="attribute-types-supported"></a><span data-ttu-id="fd033-104">Attribute types supported</span><span class="sxs-lookup"><span data-stu-id="fd033-104">Attribute types supported</span></span>

<span data-ttu-id="fd033-105">Tất cả</span><span class="sxs-lookup"><span data-stu-id="fd033-105">All</span></span>

## <a name="syntax"></a><span data-ttu-id="fd033-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="fd033-106">Syntax</span></span>

`formContext.getAttribute(arg).getFormat()`

## <a name="return-value"></a><span data-ttu-id="fd033-107">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="fd033-107">Return Value</span></span>

<span data-ttu-id="fd033-108">This method will return one of the following **string** values or "null":</span><span class="sxs-lookup"><span data-stu-id="fd033-108">This method will return one of the following **string** values or "null":</span></span>

- <span data-ttu-id="fd033-109">ngày</span><span class="sxs-lookup"><span data-stu-id="fd033-109">date</span></span>
- <span data-ttu-id="fd033-110">ngày giờ</span><span class="sxs-lookup"><span data-stu-id="fd033-110">datetime</span></span>
- <span data-ttu-id="fd033-111">duration</span><span class="sxs-lookup"><span data-stu-id="fd033-111">duration</span></span>
- <span data-ttu-id="fd033-112">email</span><span class="sxs-lookup"><span data-stu-id="fd033-112">email</span></span>
- <span data-ttu-id="fd033-113">language</span><span class="sxs-lookup"><span data-stu-id="fd033-113">language</span></span>
- <span data-ttu-id="fd033-114">không</span><span class="sxs-lookup"><span data-stu-id="fd033-114">none</span></span>
- <span data-ttu-id="fd033-115">Điện thoại </span><span class="sxs-lookup"><span data-stu-id="fd033-115">phone</span></span>
- <span data-ttu-id="fd033-116">văn bản</span><span class="sxs-lookup"><span data-stu-id="fd033-116">text</span></span>
- <span data-ttu-id="fd033-117">textarea</span><span class="sxs-lookup"><span data-stu-id="fd033-117">textarea</span></span>
- <span data-ttu-id="fd033-118">tickersymbol</span><span class="sxs-lookup"><span data-stu-id="fd033-118">tickersymbol</span></span>
- <span data-ttu-id="fd033-119">timezone</span><span class="sxs-lookup"><span data-stu-id="fd033-119">timezone</span></span>
- <span data-ttu-id="fd033-120">url</span><span class="sxs-lookup"><span data-stu-id="fd033-120">url</span></span>

> [!NOTE]
> <span data-ttu-id="fd033-121">This format information generally represents the format options of the application field.</span><span class="sxs-lookup"><span data-stu-id="fd033-121">This format information generally represents the format options of the application field.</span></span> <span data-ttu-id="fd033-122">Format options for Boolean fields are not provided.</span><span class="sxs-lookup"><span data-stu-id="fd033-122">Format options for Boolean fields are not provided.</span></span>

<span data-ttu-id="fd033-123">The following table lists the format string values to expect for each type of attribute schema type and format option.</span><span class="sxs-lookup"><span data-stu-id="fd033-123">The following table lists the format string values to expect for each type of attribute schema type and format option.</span></span>

| <span data-ttu-id="fd033-124">Application Field Type</span><span class="sxs-lookup"><span data-stu-id="fd033-124">Application Field Type</span></span> | <span data-ttu-id="fd033-125">Tùy chọn định dạng</span><span class="sxs-lookup"><span data-stu-id="fd033-125">Format Option</span></span> | <span data-ttu-id="fd033-126">Attribute Type</span><span class="sxs-lookup"><span data-stu-id="fd033-126">Attribute Type</span></span> | <span data-ttu-id="fd033-127">Format Value</span><span class="sxs-lookup"><span data-stu-id="fd033-127">Format Value</span></span>|
|----------------------------|-------------------|--------------------|------------------|
| <span data-ttu-id="fd033-128">Date and Time</span><span class="sxs-lookup"><span data-stu-id="fd033-128">Date and Time</span></span>              | <span data-ttu-id="fd033-129">Chỉ Ngày</span><span class="sxs-lookup"><span data-stu-id="fd033-129">Date Only</span></span>         | <span data-ttu-id="fd033-130">ngày giờ</span><span class="sxs-lookup"><span data-stu-id="fd033-130">datetime</span></span>           | <span data-ttu-id="fd033-131">ngày</span><span class="sxs-lookup"><span data-stu-id="fd033-131">date</span></span>             |
| <span data-ttu-id="fd033-132">Date and Time</span><span class="sxs-lookup"><span data-stu-id="fd033-132">Date and Time</span></span>              | <span data-ttu-id="fd033-133">Date and Time</span><span class="sxs-lookup"><span data-stu-id="fd033-133">Date and Time</span></span>     | <span data-ttu-id="fd033-134">ngày giờ</span><span class="sxs-lookup"><span data-stu-id="fd033-134">datetime</span></span>           | <span data-ttu-id="fd033-135">ngày giờ</span><span class="sxs-lookup"><span data-stu-id="fd033-135">datetime</span></span>         |
| <span data-ttu-id="fd033-136">Số Nguyên</span><span class="sxs-lookup"><span data-stu-id="fd033-136">Whole Number</span></span>               | <span data-ttu-id="fd033-137">Khoảng thời gian</span><span class="sxs-lookup"><span data-stu-id="fd033-137">Duration</span></span>          | <span data-ttu-id="fd033-138">số nguyên</span><span class="sxs-lookup"><span data-stu-id="fd033-138">integer</span></span>            | <span data-ttu-id="fd033-139">duration</span><span class="sxs-lookup"><span data-stu-id="fd033-139">duration</span></span>         |
| <span data-ttu-id="fd033-140">Single Line of Text</span><span class="sxs-lookup"><span data-stu-id="fd033-140">Single Line of Text</span></span>        | <span data-ttu-id="fd033-141">Email</span><span class="sxs-lookup"><span data-stu-id="fd033-141">E-mail</span></span>            | <span data-ttu-id="fd033-142">chuỗi</span><span class="sxs-lookup"><span data-stu-id="fd033-142">string</span></span>             | <span data-ttu-id="fd033-143">email</span><span class="sxs-lookup"><span data-stu-id="fd033-143">email</span></span>            |
| <span data-ttu-id="fd033-144">Số Nguyên</span><span class="sxs-lookup"><span data-stu-id="fd033-144">Whole Number</span></span>               | <span data-ttu-id="fd033-145">Language</span><span class="sxs-lookup"><span data-stu-id="fd033-145">Language</span></span>          | <span data-ttu-id="fd033-146">optionset</span><span class="sxs-lookup"><span data-stu-id="fd033-146">optionset</span></span>          | <span data-ttu-id="fd033-147">language</span><span class="sxs-lookup"><span data-stu-id="fd033-147">language</span></span>         |
| <span data-ttu-id="fd033-148">Số Nguyên</span><span class="sxs-lookup"><span data-stu-id="fd033-148">Whole Number</span></span>               | <span data-ttu-id="fd033-149">Không có</span><span class="sxs-lookup"><span data-stu-id="fd033-149">None</span></span>              | <span data-ttu-id="fd033-150">số nguyên</span><span class="sxs-lookup"><span data-stu-id="fd033-150">integer</span></span>            | <span data-ttu-id="fd033-151">không</span><span class="sxs-lookup"><span data-stu-id="fd033-151">none</span></span>             |
| <span data-ttu-id="fd033-152">Single Line of Text</span><span class="sxs-lookup"><span data-stu-id="fd033-152">Single Line of Text</span></span>        | <span data-ttu-id="fd033-153">Khu vực văn bản</span><span class="sxs-lookup"><span data-stu-id="fd033-153">Text Area</span></span>         | <span data-ttu-id="fd033-154">chuỗi</span><span class="sxs-lookup"><span data-stu-id="fd033-154">string</span></span>             | <span data-ttu-id="fd033-155">textarea</span><span class="sxs-lookup"><span data-stu-id="fd033-155">textarea</span></span>         |
| <span data-ttu-id="fd033-156">Single Line of Text</span><span class="sxs-lookup"><span data-stu-id="fd033-156">Single Line of Text</span></span>        | <span data-ttu-id="fd033-157">Text</span><span class="sxs-lookup"><span data-stu-id="fd033-157">Text</span></span>              | <span data-ttu-id="fd033-158">chuỗi</span><span class="sxs-lookup"><span data-stu-id="fd033-158">string</span></span>             | <span data-ttu-id="fd033-159">văn bản</span><span class="sxs-lookup"><span data-stu-id="fd033-159">text</span></span>             |
| <span data-ttu-id="fd033-160">Single Line of Text</span><span class="sxs-lookup"><span data-stu-id="fd033-160">Single Line of Text</span></span>        | <span data-ttu-id="fd033-161">Ký hiệu Chứng khoán</span><span class="sxs-lookup"><span data-stu-id="fd033-161">Ticker Symbol</span></span>     | <span data-ttu-id="fd033-162">chuỗi</span><span class="sxs-lookup"><span data-stu-id="fd033-162">string</span></span>             | <span data-ttu-id="fd033-163">tickersymbol</span><span class="sxs-lookup"><span data-stu-id="fd033-163">tickersymbol</span></span>     |
| <span data-ttu-id="fd033-164">Single Line of Text</span><span class="sxs-lookup"><span data-stu-id="fd033-164">Single Line of Text</span></span>        | <span data-ttu-id="fd033-165">Số điện thoại</span><span class="sxs-lookup"><span data-stu-id="fd033-165">Phone</span></span>             | <span data-ttu-id="fd033-166">chuỗi</span><span class="sxs-lookup"><span data-stu-id="fd033-166">string</span></span>             | <span data-ttu-id="fd033-167">Điện thoại </span><span class="sxs-lookup"><span data-stu-id="fd033-167">phone</span></span>            |
| <span data-ttu-id="fd033-168">Số Nguyên</span><span class="sxs-lookup"><span data-stu-id="fd033-168">Whole Number</span></span>               | <span data-ttu-id="fd033-169">Múi giờ</span><span class="sxs-lookup"><span data-stu-id="fd033-169">Time Zone</span></span>         | <span data-ttu-id="fd033-170">optionset</span><span class="sxs-lookup"><span data-stu-id="fd033-170">optionset</span></span>          | <span data-ttu-id="fd033-171">timezone</span><span class="sxs-lookup"><span data-stu-id="fd033-171">timezone</span></span>         |
| <span data-ttu-id="fd033-172">Single Line of Text</span><span class="sxs-lookup"><span data-stu-id="fd033-172">Single Line of Text</span></span>        | <span data-ttu-id="fd033-173">Url</span><span class="sxs-lookup"><span data-stu-id="fd033-173">Url</span></span>               | <span data-ttu-id="fd033-174">chuỗi</span><span class="sxs-lookup"><span data-stu-id="fd033-174">string</span></span>             | <span data-ttu-id="fd033-175">url</span><span class="sxs-lookup"><span data-stu-id="fd033-175">url</span></span> 
