---
title: captureImage | MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 1b24e8b2-20af-4e75-8c00-1aa393c07aef
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 98596bf2bd62820b45b7f005a3ab230c04eaff07
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388276"
---
# <a name="captureimage-client-api-reference"></a><span data-ttu-id="56ae0-102">captureImage (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="56ae0-102">captureImage (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/captureImage-description.md](./includes/captureImage-description.md)]


## <a name="syntax"></a><span data-ttu-id="56ae0-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="56ae0-103">Syntax</span></span>

`Xrm.Device.captureImage(imageOptions).then(successCallback, errorCallback)`

## <a name="parameters"></a><span data-ttu-id="56ae0-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="56ae0-104">Parameters</span></span>

| <span data-ttu-id="56ae0-105">Parameter Name</span><span class="sxs-lookup"><span data-stu-id="56ae0-105">Parameter Name</span></span>        | <span data-ttu-id="56ae0-106">Loại</span><span class="sxs-lookup"><span data-stu-id="56ae0-106">Type</span></span>           | <span data-ttu-id="56ae0-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="56ae0-107">Required</span></span>  |<span data-ttu-id="56ae0-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="56ae0-108">Description</span></span>  |
| ------------- |-------------| -----|-----|
|<span data-ttu-id="56ae0-109">imageOptions</span><span class="sxs-lookup"><span data-stu-id="56ae0-109">imageOptions</span></span> |<span data-ttu-id="56ae0-110">Đối tượng</span><span class="sxs-lookup"><span data-stu-id="56ae0-110">Object</span></span> | <span data-ttu-id="56ae0-111">Không</span><span class="sxs-lookup"><span data-stu-id="56ae0-111">No</span></span>|<span data-ttu-id="56ae0-112">An object with the following attributes:</span><span class="sxs-lookup"><span data-stu-id="56ae0-112">An object with the following attributes:</span></span><br/><span data-ttu-id="56ae0-113">- **allowEdit**: Indicates whether to edit the image before saving.</span><span class="sxs-lookup"><span data-stu-id="56ae0-113">- **allowEdit**: Indicates whether to edit the image before saving.</span></span> <span data-ttu-id="56ae0-114">Boolean.</span><span class="sxs-lookup"><span data-stu-id="56ae0-114">Boolean.</span></span><br/><span data-ttu-id="56ae0-115">- **height**: Height of the image to capture.</span><span class="sxs-lookup"><span data-stu-id="56ae0-115">- **height**: Height of the image to capture.</span></span> <span data-ttu-id="56ae0-116">Số.</span><span class="sxs-lookup"><span data-stu-id="56ae0-116">Number.</span></span><br/><span data-ttu-id="56ae0-117">- **preferFrontCamera**: Indicates whether to capture image using the front camera of the device.</span><span class="sxs-lookup"><span data-stu-id="56ae0-117">- **preferFrontCamera**: Indicates whether to capture image using the front camera of the device.</span></span> <span data-ttu-id="56ae0-118">Boolean.</span><span class="sxs-lookup"><span data-stu-id="56ae0-118">Boolean.</span></span><br/><span data-ttu-id="56ae0-119">- **quality**: Quality of the image file in percentage.</span><span class="sxs-lookup"><span data-stu-id="56ae0-119">- **quality**: Quality of the image file in percentage.</span></span> <span data-ttu-id="56ae0-120">Số.</span><span class="sxs-lookup"><span data-stu-id="56ae0-120">Number.</span></span><br/><span data-ttu-id="56ae0-121">- **width**: Width of the image to capture.</span><span class="sxs-lookup"><span data-stu-id="56ae0-121">- **width**: Width of the image to capture.</span></span> <span data-ttu-id="56ae0-122">Number..</span><span class="sxs-lookup"><span data-stu-id="56ae0-122">Number..</span></span>|
|<span data-ttu-id="56ae0-123">successCallback</span><span class="sxs-lookup"><span data-stu-id="56ae0-123">successCallback</span></span> |<span data-ttu-id="56ae0-124">Hàm</span><span class="sxs-lookup"><span data-stu-id="56ae0-124">Function</span></span> | <span data-ttu-id="56ae0-125">Có</span><span class="sxs-lookup"><span data-stu-id="56ae0-125">Yes</span></span>|<span data-ttu-id="56ae0-126">A function to call when image is returned.</span><span class="sxs-lookup"><span data-stu-id="56ae0-126">A function to call when image is returned.</span></span> <span data-ttu-id="56ae0-127">A base64 encoded image object with the following attributes is passed to the function:</span><span class="sxs-lookup"><span data-stu-id="56ae0-127">A base64 encoded image object with the following attributes is passed to the function:</span></span><br/><span data-ttu-id="56ae0-128">- **fileContent**: Contents of the image file.</span><span class="sxs-lookup"><span data-stu-id="56ae0-128">- **fileContent**: Contents of the image file.</span></span> <span data-ttu-id="56ae0-129">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="56ae0-129">String</span></span> <br/><span data-ttu-id="56ae0-130">- **fileName**: Name of the image file.</span><span class="sxs-lookup"><span data-stu-id="56ae0-130">- **fileName**: Name of the image file.</span></span> <span data-ttu-id="56ae0-131">String.</span><span class="sxs-lookup"><span data-stu-id="56ae0-131">String.</span></span><br/><span data-ttu-id="56ae0-132">- **fileSize**: Size of the image file in KB.</span><span class="sxs-lookup"><span data-stu-id="56ae0-132">- **fileSize**: Size of the image file in KB.</span></span> <span data-ttu-id="56ae0-133">Số.</span><span class="sxs-lookup"><span data-stu-id="56ae0-133">Number.</span></span><br/><span data-ttu-id="56ae0-134">- **mimeType**: Image file MIME type.</span><span class="sxs-lookup"><span data-stu-id="56ae0-134">- **mimeType**: Image file MIME type.</span></span> <span data-ttu-id="56ae0-135">String.</span><span class="sxs-lookup"><span data-stu-id="56ae0-135">String.</span></span>|
|<span data-ttu-id="56ae0-136">errorCallback</span><span class="sxs-lookup"><span data-stu-id="56ae0-136">errorCallback</span></span> |<span data-ttu-id="56ae0-137">Hàm</span><span class="sxs-lookup"><span data-stu-id="56ae0-137">Function</span></span> | <span data-ttu-id="56ae0-138">Có</span><span class="sxs-lookup"><span data-stu-id="56ae0-138">Yes</span></span>|<span data-ttu-id="56ae0-139">A function to call when the operation fails.</span><span class="sxs-lookup"><span data-stu-id="56ae0-139">A function to call when the operation fails.</span></span> |
 

## <a name="return-value"></a><span data-ttu-id="56ae0-140">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="56ae0-140">Return Value</span></span>
<span data-ttu-id="56ae0-141">On success, returns a base64 encoded image object with the attributes specified earlier.</span><span class="sxs-lookup"><span data-stu-id="56ae0-141">On success, returns a base64 encoded image object with the attributes specified earlier.</span></span>

## <a name="remarks"></a><span data-ttu-id="56ae0-142">Chú thích</span><span class="sxs-lookup"><span data-stu-id="56ae0-142">Remarks</span></span>
<span data-ttu-id="56ae0-143">This method is supported only for the mobile clients.</span><span class="sxs-lookup"><span data-stu-id="56ae0-143">This method is supported only for the mobile clients.</span></span>

### <a name="related-topics"></a><span data-ttu-id="56ae0-144">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="56ae0-144">Related topics</span></span>
[<span data-ttu-id="56ae0-145">Xrm.Device</span><span class="sxs-lookup"><span data-stu-id="56ae0-145">Xrm.Device</span></span>](../xrm-device.md)

