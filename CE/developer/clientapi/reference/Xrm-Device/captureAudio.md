---
title: captureAudio| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: fa39d18e-4b82-423a-84a0-e54450b7964e
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: b709b90159c7108946f788c54bf5bb0dfee10a3f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388193"
---
# <a name="captureaudio-client-api-reference"></a><span data-ttu-id="14007-102">captureAudio (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="14007-102">captureAudio (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/captureAudio-description.md](./includes/captureAudio-description.md)]


## <a name="syntax"></a><span data-ttu-id="14007-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="14007-103">Syntax</span></span>

`Xrm.Device.captureAudio().then(successCallback, errorCallback)`

## <a name="parameters"></a><span data-ttu-id="14007-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="14007-104">Parameters</span></span>

| <span data-ttu-id="14007-105">Parameter Name</span><span class="sxs-lookup"><span data-stu-id="14007-105">Parameter Name</span></span>        | <span data-ttu-id="14007-106">Loại</span><span class="sxs-lookup"><span data-stu-id="14007-106">Type</span></span>           | <span data-ttu-id="14007-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="14007-107">Required</span></span>  |<span data-ttu-id="14007-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="14007-108">Description</span></span>  |
| ------------- |-------------| -----|-----|
|<span data-ttu-id="14007-109">successCallback</span><span class="sxs-lookup"><span data-stu-id="14007-109">successCallback</span></span> |<span data-ttu-id="14007-110">Hàm</span><span class="sxs-lookup"><span data-stu-id="14007-110">Function</span></span> | <span data-ttu-id="14007-111">Có</span><span class="sxs-lookup"><span data-stu-id="14007-111">Yes</span></span>|<span data-ttu-id="14007-112">A function to call when audio is returned.</span><span class="sxs-lookup"><span data-stu-id="14007-112">A function to call when audio is returned.</span></span> <span data-ttu-id="14007-113">A base64 encoded audio object with the following attributes is passed to the function:</span><span class="sxs-lookup"><span data-stu-id="14007-113">A base64 encoded audio object with the following attributes is passed to the function:</span></span><br/><span data-ttu-id="14007-114">- **fileContent**: Contents of the audio file.</span><span class="sxs-lookup"><span data-stu-id="14007-114">- **fileContent**: Contents of the audio file.</span></span> <span data-ttu-id="14007-115">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="14007-115">String</span></span> <br/><span data-ttu-id="14007-116">- **fileName**: Name of the audio file.</span><span class="sxs-lookup"><span data-stu-id="14007-116">- **fileName**: Name of the audio file.</span></span> <span data-ttu-id="14007-117">String.</span><span class="sxs-lookup"><span data-stu-id="14007-117">String.</span></span><br/><span data-ttu-id="14007-118">- **fileSize**: Size of the audio file in KB.</span><span class="sxs-lookup"><span data-stu-id="14007-118">- **fileSize**: Size of the audio file in KB.</span></span> <span data-ttu-id="14007-119">Số.</span><span class="sxs-lookup"><span data-stu-id="14007-119">Number.</span></span><br/><span data-ttu-id="14007-120">- **mimeType**: Audio file MIME type.</span><span class="sxs-lookup"><span data-stu-id="14007-120">- **mimeType**: Audio file MIME type.</span></span> <span data-ttu-id="14007-121">String.</span><span class="sxs-lookup"><span data-stu-id="14007-121">String.</span></span>|
|<span data-ttu-id="14007-122">errorCallback</span><span class="sxs-lookup"><span data-stu-id="14007-122">errorCallback</span></span> |<span data-ttu-id="14007-123">Hàm</span><span class="sxs-lookup"><span data-stu-id="14007-123">Function</span></span> | <span data-ttu-id="14007-124">Có</span><span class="sxs-lookup"><span data-stu-id="14007-124">Yes</span></span>|<span data-ttu-id="14007-125">A function to call when the operation fails.</span><span class="sxs-lookup"><span data-stu-id="14007-125">A function to call when the operation fails.</span></span> |
 

## <a name="return-value"></a><span data-ttu-id="14007-126">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="14007-126">Return Value</span></span>
<span data-ttu-id="14007-127">On success, returns a base64 encoded audio object with the attributes specified earlier.</span><span class="sxs-lookup"><span data-stu-id="14007-127">On success, returns a base64 encoded audio object with the attributes specified earlier.</span></span>

## <a name="remarks"></a><span data-ttu-id="14007-128">Chú thích</span><span class="sxs-lookup"><span data-stu-id="14007-128">Remarks</span></span>
<span data-ttu-id="14007-129">This method is supported only for the mobile clients.</span><span class="sxs-lookup"><span data-stu-id="14007-129">This method is supported only for the mobile clients.</span></span>

### <a name="related-topics"></a><span data-ttu-id="14007-130">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="14007-130">Related topics</span></span>
[<span data-ttu-id="14007-131">Xrm.Device</span><span class="sxs-lookup"><span data-stu-id="14007-131">Xrm.Device</span></span>](../xrm-device.md)

