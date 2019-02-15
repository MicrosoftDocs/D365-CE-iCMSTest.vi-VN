---
title: getCurrentPosition | MicrosoftDocs
ms.date: 11/10/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 062a52d8-170c-4e98-b48a-ac99ec759f83
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 512823952503699089c81c428cdea9c1adae0df1
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388632"
---
# <a name="getcurrentposition-client-api-reference"></a><span data-ttu-id="80a26-102">getCurrentPosition (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="80a26-102">getCurrentPosition (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getCurrentPosition-description.md](./includes/getCurrentPosition-description.md)]


## <a name="syntax"></a><span data-ttu-id="80a26-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="80a26-103">Syntax</span></span>

`Xrm.Device.getCurrentPosition().then(successCallback, errorCallback)`

## <a name="parameters"></a><span data-ttu-id="80a26-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="80a26-104">Parameters</span></span>

| <span data-ttu-id="80a26-105">Parameter Name</span><span class="sxs-lookup"><span data-stu-id="80a26-105">Parameter Name</span></span>        | <span data-ttu-id="80a26-106">Loại</span><span class="sxs-lookup"><span data-stu-id="80a26-106">Type</span></span>           | <span data-ttu-id="80a26-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="80a26-107">Required</span></span>  |<span data-ttu-id="80a26-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="80a26-108">Description</span></span>  |
| ------------- |-------------| -----|-----|
|<span data-ttu-id="80a26-109">successCallback</span><span class="sxs-lookup"><span data-stu-id="80a26-109">successCallback</span></span> |<span data-ttu-id="80a26-110">Hàm</span><span class="sxs-lookup"><span data-stu-id="80a26-110">Function</span></span> | <span data-ttu-id="80a26-111">Có</span><span class="sxs-lookup"><span data-stu-id="80a26-111">Yes</span></span>|<span data-ttu-id="80a26-112">A function to call when the current geolocation information is returned.</span><span class="sxs-lookup"><span data-stu-id="80a26-112">A function to call when the current geolocation information is returned.</span></span> <span data-ttu-id="80a26-113">A geolocation object with the following attributes is passed to the function.:</span><span class="sxs-lookup"><span data-stu-id="80a26-113">A geolocation object with the following attributes is passed to the function.:</span></span><br/><span data-ttu-id="80a26-114">- **coords**: Contains a set of geographic coordinates along with associated accuracy as well as a set of other optional attributes such as altitude and speed.</span><span class="sxs-lookup"><span data-stu-id="80a26-114">- **coords**: Contains a set of geographic coordinates along with associated accuracy as well as a set of other optional attributes such as altitude and speed.</span></span> <br/><span data-ttu-id="80a26-115">- **timestamp**: Represents the time when the object was acquired and is represented as DOMTimeStamp.</span><span class="sxs-lookup"><span data-stu-id="80a26-115">- **timestamp**: Represents the time when the object was acquired and is represented as DOMTimeStamp.</span></span>|
|<span data-ttu-id="80a26-116">errorCallback</span><span class="sxs-lookup"><span data-stu-id="80a26-116">errorCallback</span></span> |<span data-ttu-id="80a26-117">Hàm</span><span class="sxs-lookup"><span data-stu-id="80a26-117">Function</span></span> | <span data-ttu-id="80a26-118">Có</span><span class="sxs-lookup"><span data-stu-id="80a26-118">Yes</span></span>|<span data-ttu-id="80a26-119">A function to call when the operation fails.</span><span class="sxs-lookup"><span data-stu-id="80a26-119">A function to call when the operation fails.</span></span> <span data-ttu-id="80a26-120">An object with the following properties will be passed:</span><span class="sxs-lookup"><span data-stu-id="80a26-120">An object with the following properties will be passed:</span></span> <br/><span data-ttu-id="80a26-121">- **code**: The error code.</span><span class="sxs-lookup"><span data-stu-id="80a26-121">- **code**: The error code.</span></span> <span data-ttu-id="80a26-122">Số.</span><span class="sxs-lookup"><span data-stu-id="80a26-122">Number.</span></span> <br/><span data-ttu-id="80a26-123">- **message**: RLocalized message describing the error details.</span><span class="sxs-lookup"><span data-stu-id="80a26-123">- **message**: RLocalized message describing the error details.</span></span> <span data-ttu-id="80a26-124">String.</span><span class="sxs-lookup"><span data-stu-id="80a26-124">String.</span></span><br/><br/><span data-ttu-id="80a26-125">If the user location setting is not enabled on your mobile device, the error message indicates the same.</span><span class="sxs-lookup"><span data-stu-id="80a26-125">If the user location setting is not enabled on your mobile device, the error message indicates the same.</span></span> <span data-ttu-id="80a26-126">If you are using an earlier version of the Dynamics 365 for Customer Engagement mobile client or if geolocation capability is not available on your mobile device, null is passed to the error callback.</span><span class="sxs-lookup"><span data-stu-id="80a26-126">If you are using an earlier version of the Dynamics 365 for Customer Engagement mobile client or if geolocation capability is not available on your mobile device, null is passed to the error callback.</span></span>|
 

## <a name="return-value"></a><span data-ttu-id="80a26-127">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="80a26-127">Return Value</span></span>
<span data-ttu-id="80a26-128">On success, returns a geolocation object with the attributes specified earlier in the **successCallback** function.</span><span class="sxs-lookup"><span data-stu-id="80a26-128">On success, returns a geolocation object with the attributes specified earlier in the **successCallback** function.</span></span>

## <a name="remarks"></a><span data-ttu-id="80a26-129">Chú thích</span><span class="sxs-lookup"><span data-stu-id="80a26-129">Remarks</span></span>
<span data-ttu-id="80a26-130">For the **getCurrentPosition** method to work, the geolocation capability must be enabled on your mobile device, and the Dynamics 365 for Customer Engagement mobile clients must have permissions to access the device location, which isn't enabled by default.</span><span class="sxs-lookup"><span data-stu-id="80a26-130">For the **getCurrentPosition** method to work, the geolocation capability must be enabled on your mobile device, and the Dynamics 365 for Customer Engagement mobile clients must have permissions to access the device location, which isn't enabled by default.</span></span>

<span data-ttu-id="80a26-131">This method is supported only for the mobile clients.</span><span class="sxs-lookup"><span data-stu-id="80a26-131">This method is supported only for the mobile clients.</span></span>

## <a name="example"></a><span data-ttu-id="80a26-132">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="80a26-132">Example</span></span>

```JavaScript
Xrm.Device.getCurrentPosition().then(
    function success(location) {
        Xrm.Navigation.openAlertDialog({
            text: "Latitude: " + location.coords.latitude +
            ", Longitude: " + location.coords.longitude
        });
    },
    function (error) {
        Xrm.Navigation.openAlertDialog({ text: error.message });
    }
);
```

### <a name="related-topics"></a><span data-ttu-id="80a26-133">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="80a26-133">Related topics</span></span>
[<span data-ttu-id="80a26-134">Xrm.Device</span><span class="sxs-lookup"><span data-stu-id="80a26-134">Xrm.Device</span></span>](../xrm-device.md)