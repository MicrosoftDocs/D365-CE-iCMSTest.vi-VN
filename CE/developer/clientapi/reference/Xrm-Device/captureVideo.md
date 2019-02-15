---
title: captureVideo| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 9580d05a-a91f-4126-b94b-4d1068da35fa
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 184db5b218492ad8a80b68e1abae5685f4eae3a2
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387021"
---
# <a name="capturevideo-client-api-reference"></a><span data-ttu-id="25af0-102">captureVideo (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="25af0-102">captureVideo (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/captureVideo-description.md](./includes/captureVideo-description.md)]


## <a name="syntax"></a><span data-ttu-id="25af0-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="25af0-103">Syntax</span></span>

`Xrm.Device.captureVideo().then(successCallback, errorCallback)`

## <a name="parameters"></a><span data-ttu-id="25af0-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="25af0-104">Parameters</span></span>

| <span data-ttu-id="25af0-105">Parameter Name</span><span class="sxs-lookup"><span data-stu-id="25af0-105">Parameter Name</span></span>        | <span data-ttu-id="25af0-106">Loại</span><span class="sxs-lookup"><span data-stu-id="25af0-106">Type</span></span>           | <span data-ttu-id="25af0-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="25af0-107">Required</span></span>  |<span data-ttu-id="25af0-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="25af0-108">Description</span></span>  |
| ------------- |-------------| -----|-----|
|<span data-ttu-id="25af0-109">successCallback</span><span class="sxs-lookup"><span data-stu-id="25af0-109">successCallback</span></span> |<span data-ttu-id="25af0-110">Hàm</span><span class="sxs-lookup"><span data-stu-id="25af0-110">Function</span></span> | <span data-ttu-id="25af0-111">Có</span><span class="sxs-lookup"><span data-stu-id="25af0-111">Yes</span></span>|<span data-ttu-id="25af0-112">A function to call when Video is returned.</span><span class="sxs-lookup"><span data-stu-id="25af0-112">A function to call when Video is returned.</span></span> <span data-ttu-id="25af0-113">A base64 encoded Video object with the following attributes is passed to the function:</span><span class="sxs-lookup"><span data-stu-id="25af0-113">A base64 encoded Video object with the following attributes is passed to the function:</span></span><br/><span data-ttu-id="25af0-114">- **fileContent**: Contents of the Video file.</span><span class="sxs-lookup"><span data-stu-id="25af0-114">- **fileContent**: Contents of the Video file.</span></span> <span data-ttu-id="25af0-115">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="25af0-115">String</span></span> <br/><span data-ttu-id="25af0-116">- **fileName**: Name of the Video file.</span><span class="sxs-lookup"><span data-stu-id="25af0-116">- **fileName**: Name of the Video file.</span></span> <span data-ttu-id="25af0-117">String.</span><span class="sxs-lookup"><span data-stu-id="25af0-117">String.</span></span><br/><span data-ttu-id="25af0-118">- **fileSize**: Size of the Video file in KB.</span><span class="sxs-lookup"><span data-stu-id="25af0-118">- **fileSize**: Size of the Video file in KB.</span></span> <span data-ttu-id="25af0-119">Số.</span><span class="sxs-lookup"><span data-stu-id="25af0-119">Number.</span></span><br/><span data-ttu-id="25af0-120">- **mimeType**: Video file MIME type.</span><span class="sxs-lookup"><span data-stu-id="25af0-120">- **mimeType**: Video file MIME type.</span></span> <span data-ttu-id="25af0-121">String.</span><span class="sxs-lookup"><span data-stu-id="25af0-121">String.</span></span>|
|<span data-ttu-id="25af0-122">errorCallback</span><span class="sxs-lookup"><span data-stu-id="25af0-122">errorCallback</span></span> |<span data-ttu-id="25af0-123">Hàm</span><span class="sxs-lookup"><span data-stu-id="25af0-123">Function</span></span> | <span data-ttu-id="25af0-124">Có</span><span class="sxs-lookup"><span data-stu-id="25af0-124">Yes</span></span>|<span data-ttu-id="25af0-125">A function to call when the operation fails.</span><span class="sxs-lookup"><span data-stu-id="25af0-125">A function to call when the operation fails.</span></span> |
 

## <a name="return-value"></a><span data-ttu-id="25af0-126">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="25af0-126">Return Value</span></span>
<span data-ttu-id="25af0-127">On success, returns a base64 encoded Video object with the attributes specified earlier.</span><span class="sxs-lookup"><span data-stu-id="25af0-127">On success, returns a base64 encoded Video object with the attributes specified earlier.</span></span>

## <a name="remarks"></a><span data-ttu-id="25af0-128">Chú thích</span><span class="sxs-lookup"><span data-stu-id="25af0-128">Remarks</span></span>
<span data-ttu-id="25af0-129">This method is supported only for the mobile clients.</span><span class="sxs-lookup"><span data-stu-id="25af0-129">This method is supported only for the mobile clients.</span></span>

### <a name="related-topics"></a><span data-ttu-id="25af0-130">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="25af0-130">Related topics</span></span>
[<span data-ttu-id="25af0-131">Xrm.Device</span><span class="sxs-lookup"><span data-stu-id="25af0-131">Xrm.Device</span></span>](../xrm-device.md)

