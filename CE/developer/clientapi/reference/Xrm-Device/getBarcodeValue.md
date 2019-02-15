---
title: getBarcodeValue| MicrosoftDocs
ms.date: 11/10/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 0218b96c-2809-4f2d-9f9f-d8ee8f8e3b7b
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 17ec172e7aa3ba3ac5ef897c49375581d3dbcefa
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386218"
---
# <a name="getbarcodevalue-client-api-reference"></a><span data-ttu-id="0943c-102">getBarcodeValue (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="0943c-102">getBarcodeValue (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getBarcodeValue-description.md](./includes/getBarcodeValue-description.md)]


## <a name="syntax"></a><span data-ttu-id="0943c-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="0943c-103">Syntax</span></span>

`Xrm.Device.getBarcodeValue().then(successCallback, errorCallback)`

## <a name="parameters"></a><span data-ttu-id="0943c-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="0943c-104">Parameters</span></span>

| <span data-ttu-id="0943c-105">Parameter Name</span><span class="sxs-lookup"><span data-stu-id="0943c-105">Parameter Name</span></span>        | <span data-ttu-id="0943c-106">Loại</span><span class="sxs-lookup"><span data-stu-id="0943c-106">Type</span></span>           | <span data-ttu-id="0943c-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="0943c-107">Required</span></span>  |<span data-ttu-id="0943c-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="0943c-108">Description</span></span>  |
| ------------- |-------------| -----|-----|
|<span data-ttu-id="0943c-109">successCallback</span><span class="sxs-lookup"><span data-stu-id="0943c-109">successCallback</span></span> |<span data-ttu-id="0943c-110">Hàm</span><span class="sxs-lookup"><span data-stu-id="0943c-110">Function</span></span> | <span data-ttu-id="0943c-111">Có</span><span class="sxs-lookup"><span data-stu-id="0943c-111">Yes</span></span>|<span data-ttu-id="0943c-112">A function to call when the barcode value is returned as a String.</span><span class="sxs-lookup"><span data-stu-id="0943c-112">A function to call when the barcode value is returned as a String.</span></span>|
|<span data-ttu-id="0943c-113">errorCallback</span><span class="sxs-lookup"><span data-stu-id="0943c-113">errorCallback</span></span> |<span data-ttu-id="0943c-114">Hàm</span><span class="sxs-lookup"><span data-stu-id="0943c-114">Function</span></span> | <span data-ttu-id="0943c-115">Có</span><span class="sxs-lookup"><span data-stu-id="0943c-115">Yes</span></span>|<span data-ttu-id="0943c-116">A function to call when the operation fails.</span><span class="sxs-lookup"><span data-stu-id="0943c-116">A function to call when the operation fails.</span></span> <span data-ttu-id="0943c-117">An error object with the **message** property (String) will be passed that describes the error details.</span><span class="sxs-lookup"><span data-stu-id="0943c-117">An error object with the **message** property (String) will be passed that describes the error details.</span></span>|
 

## <a name="return-value"></a><span data-ttu-id="0943c-118">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="0943c-118">Return Value</span></span>
<span data-ttu-id="0943c-119">On success, returns a string containing the scanned barcode value.</span><span class="sxs-lookup"><span data-stu-id="0943c-119">On success, returns a string containing the scanned barcode value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0943c-120">Chú thích</span><span class="sxs-lookup"><span data-stu-id="0943c-120">Remarks</span></span>
<span data-ttu-id="0943c-121">This method is supported only for the mobile clients.</span><span class="sxs-lookup"><span data-stu-id="0943c-121">This method is supported only for the mobile clients.</span></span>

## <a name="example"></a><span data-ttu-id="0943c-122">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="0943c-122">Example</span></span>

```JavaScript
Xrm.Device.getBarcodeValue().then(
    function success(result) {
        Xrm.Navigation.openAlertDialog({ text: "Barcode value: " + result });
    },
    function (error) {
        Xrm.Navigation.openAlertDialog( {text: error.message} );
    }
);
``` 

### <a name="related-topics"></a><span data-ttu-id="0943c-123">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="0943c-123">Related topics</span></span>
[<span data-ttu-id="0943c-124">Xrm.Device</span><span class="sxs-lookup"><span data-stu-id="0943c-124">Xrm.Device</span></span>](../xrm-device.md)

