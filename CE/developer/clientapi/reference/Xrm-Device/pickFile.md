---
title: pickFile| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: c777a0b8-2b07-458b-8a4f-8938f7a2e696
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7fec32127ec14b1ba2e74122ac252627e9b9f025
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385925"
---
# <a name="pickfile-client-api-reference"></a><span data-ttu-id="fa326-102">pickFile (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="fa326-102">pickFile (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/pickFile-description.md](./includes/pickFile-description.md)]


## <a name="syntax"></a><span data-ttu-id="fa326-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="fa326-103">Syntax</span></span>

`Xrm.Device.pickFile(pickFileOptions).then(successCallback, errorCallback)`

## <a name="parameters"></a><span data-ttu-id="fa326-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="fa326-104">Parameters</span></span>

| <span data-ttu-id="fa326-105">Parameter Name</span><span class="sxs-lookup"><span data-stu-id="fa326-105">Parameter Name</span></span>        | <span data-ttu-id="fa326-106">Loại</span><span class="sxs-lookup"><span data-stu-id="fa326-106">Type</span></span>           | <span data-ttu-id="fa326-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="fa326-107">Required</span></span>  |<span data-ttu-id="fa326-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="fa326-108">Description</span></span>  |
| ------------- |-------------| -----|-----|
|<span data-ttu-id="fa326-109">pickFileOptions</span><span class="sxs-lookup"><span data-stu-id="fa326-109">pickFileOptions</span></span> |<span data-ttu-id="fa326-110">Đối tượng</span><span class="sxs-lookup"><span data-stu-id="fa326-110">Object</span></span> | <span data-ttu-id="fa326-111">Không</span><span class="sxs-lookup"><span data-stu-id="fa326-111">No</span></span>|<span data-ttu-id="fa326-112">An object with the following attributes:</span><span class="sxs-lookup"><span data-stu-id="fa326-112">An object with the following attributes:</span></span><br/><span data-ttu-id="fa326-113">- **accept**: Image file types to select.</span><span class="sxs-lookup"><span data-stu-id="fa326-113">- **accept**: Image file types to select.</span></span> <span data-ttu-id="fa326-114">Valid values are "audio", "video", or "image".</span><span class="sxs-lookup"><span data-stu-id="fa326-114">Valid values are "audio", "video", or "image".</span></span> <span data-ttu-id="fa326-115">String.</span><span class="sxs-lookup"><span data-stu-id="fa326-115">String.</span></span><br/><span data-ttu-id="fa326-116">- **allowMultipleFiles**: Indicates whether to allow selecting multiple files.</span><span class="sxs-lookup"><span data-stu-id="fa326-116">- **allowMultipleFiles**: Indicates whether to allow selecting multiple files.</span></span> <span data-ttu-id="fa326-117">Boolean.</span><span class="sxs-lookup"><span data-stu-id="fa326-117">Boolean.</span></span><br/><span data-ttu-id="fa326-118">- **maximumAllowedFileSize**: Maximum size of the files(s) to be selected.</span><span class="sxs-lookup"><span data-stu-id="fa326-118">- **maximumAllowedFileSize**: Maximum size of the files(s) to be selected.</span></span> <span data-ttu-id="fa326-119">Số.</span><span class="sxs-lookup"><span data-stu-id="fa326-119">Number.</span></span>|
|<span data-ttu-id="fa326-120">successCallback</span><span class="sxs-lookup"><span data-stu-id="fa326-120">successCallback</span></span> |<span data-ttu-id="fa326-121">Hàm</span><span class="sxs-lookup"><span data-stu-id="fa326-121">Function</span></span> | <span data-ttu-id="fa326-122">Có</span><span class="sxs-lookup"><span data-stu-id="fa326-122">Yes</span></span>|<span data-ttu-id="fa326-123">A function to call when selected files are returned.</span><span class="sxs-lookup"><span data-stu-id="fa326-123">A function to call when selected files are returned.</span></span> <span data-ttu-id="fa326-124">An array of objects with *each* object having the following attributes is passed to the function:</span><span class="sxs-lookup"><span data-stu-id="fa326-124">An array of objects with *each* object having the following attributes is passed to the function:</span></span><br/><span data-ttu-id="fa326-125">- **fileContent**: Contents of the file.</span><span class="sxs-lookup"><span data-stu-id="fa326-125">- **fileContent**: Contents of the file.</span></span> <span data-ttu-id="fa326-126">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="fa326-126">String</span></span> <br/><span data-ttu-id="fa326-127">- **fileName**: Name of the file.</span><span class="sxs-lookup"><span data-stu-id="fa326-127">- **fileName**: Name of the file.</span></span> <span data-ttu-id="fa326-128">String.</span><span class="sxs-lookup"><span data-stu-id="fa326-128">String.</span></span><br/><span data-ttu-id="fa326-129">- **fileSize**: Size of the file in KB.</span><span class="sxs-lookup"><span data-stu-id="fa326-129">- **fileSize**: Size of the file in KB.</span></span> <span data-ttu-id="fa326-130">Số.</span><span class="sxs-lookup"><span data-stu-id="fa326-130">Number.</span></span><br/><span data-ttu-id="fa326-131">- **mimeType**: File MIME type.</span><span class="sxs-lookup"><span data-stu-id="fa326-131">- **mimeType**: File MIME type.</span></span> <span data-ttu-id="fa326-132">String.</span><span class="sxs-lookup"><span data-stu-id="fa326-132">String.</span></span>|
|<span data-ttu-id="fa326-133">errorCallback</span><span class="sxs-lookup"><span data-stu-id="fa326-133">errorCallback</span></span> |<span data-ttu-id="fa326-134">Hàm</span><span class="sxs-lookup"><span data-stu-id="fa326-134">Function</span></span> | <span data-ttu-id="fa326-135">Có</span><span class="sxs-lookup"><span data-stu-id="fa326-135">Yes</span></span>|<span data-ttu-id="fa326-136">A function to call when the operation fails.</span><span class="sxs-lookup"><span data-stu-id="fa326-136">A function to call when the operation fails.</span></span> |
 

## <a name="return-value"></a><span data-ttu-id="fa326-137">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="fa326-137">Return Value</span></span>
<span data-ttu-id="fa326-138">On success, returns a promise with array of objects as specified earlier for the **successCallback** function.</span><span class="sxs-lookup"><span data-stu-id="fa326-138">On success, returns a promise with array of objects as specified earlier for the **successCallback** function.</span></span>

### <a name="related-topics"></a><span data-ttu-id="fa326-139">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="fa326-139">Related topics</span></span>
[<span data-ttu-id="fa326-140">Xrm.Device</span><span class="sxs-lookup"><span data-stu-id="fa326-140">Xrm.Device</span></span>](../xrm-device.md)

