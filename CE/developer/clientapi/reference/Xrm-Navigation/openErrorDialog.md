---
title: openErrorDialog (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 9749143d-c159-4833-aff9-d8bc2c3395f3
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: c3805c757495ecb0b3bf187a29fb2f9259920dc2
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386220"
---
# <a name="openerrordialog-client-api-reference"></a><span data-ttu-id="d2287-102">openErrorDialog (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="d2287-102">openErrorDialog (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/openErrorDialog-description.md](./includes/openErrorDialog-description.md)]

## <a name="syntax"></a><span data-ttu-id="d2287-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="d2287-103">Syntax</span></span>

`Xrm.Navigation.openErrorDialog(errorOptions).then(successCallback,errorCallback);`

## <a name="parameters"></a><span data-ttu-id="d2287-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="d2287-104">Parameters</span></span>

|<span data-ttu-id="d2287-105">Tên</span><span class="sxs-lookup"><span data-stu-id="d2287-105">Name</span></span> |<span data-ttu-id="d2287-106">Loại</span><span class="sxs-lookup"><span data-stu-id="d2287-106">Type</span></span> |<span data-ttu-id="d2287-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="d2287-107">Required</span></span> |<span data-ttu-id="d2287-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="d2287-108">Description</span></span> |
|---|---|---|---|
|<span data-ttu-id="d2287-109">errorOptions</span><span class="sxs-lookup"><span data-stu-id="d2287-109">errorOptions</span></span>|<span data-ttu-id="d2287-110">Đối tượng</span><span class="sxs-lookup"><span data-stu-id="d2287-110">Object</span></span>|<span data-ttu-id="d2287-111">Có</span><span class="sxs-lookup"><span data-stu-id="d2287-111">Yes</span></span>|<span data-ttu-id="d2287-112">An object to specify the options for error dialog.</span><span class="sxs-lookup"><span data-stu-id="d2287-112">An object to specify the options for error dialog.</span></span> <span data-ttu-id="d2287-113">The object contains the following attributes:</span><span class="sxs-lookup"><span data-stu-id="d2287-113">The object contains the following attributes:</span></span><br/><span data-ttu-id="d2287-114">- **details**: (Optional) String.</span><span class="sxs-lookup"><span data-stu-id="d2287-114">- **details**: (Optional) String.</span></span> <span data-ttu-id="d2287-115">Details about the error.</span><span class="sxs-lookup"><span data-stu-id="d2287-115">Details about the error.</span></span> <span data-ttu-id="d2287-116">When you specify this, the **Download Log File** button is available in the error message, and clicking it will let users download a text file with the content specified in this attribute.</span><span class="sxs-lookup"><span data-stu-id="d2287-116">When you specify this, the **Download Log File** button is available in the error message, and clicking it will let users download a text file with the content specified in this attribute.</span></span><br/><span data-ttu-id="d2287-117">- **errorCode**: (Optional) Number.</span><span class="sxs-lookup"><span data-stu-id="d2287-117">- **errorCode**: (Optional) Number.</span></span> <span data-ttu-id="d2287-118">The error code.</span><span class="sxs-lookup"><span data-stu-id="d2287-118">The error code.</span></span> <span data-ttu-id="d2287-119">If you just set **errorCode**, the message for the error code is automatically retrieved from the server and displayed in the error dialog.</span><span class="sxs-lookup"><span data-stu-id="d2287-119">If you just set **errorCode**, the message for the error code is automatically retrieved from the server and displayed in the error dialog.</span></span> <span data-ttu-id="d2287-120">If you specify an invalid **errorCode** value, an error dialog with a default error message is displyed.</span><span class="sxs-lookup"><span data-stu-id="d2287-120">If you specify an invalid **errorCode** value, an error dialog with a default error message is displyed.</span></span><br/><span data-ttu-id="d2287-121">- **message**: (Optional) String.</span><span class="sxs-lookup"><span data-stu-id="d2287-121">- **message**: (Optional) String.</span></span> <span data-ttu-id="d2287-122">The message to be displayed in the error dialog.</span><span class="sxs-lookup"><span data-stu-id="d2287-122">The message to be displayed in the error dialog.</span></span><br/><br/><span data-ttu-id="d2287-123">You must set either the **errorCode** or **message** attribute.</span><span class="sxs-lookup"><span data-stu-id="d2287-123">You must set either the **errorCode** or **message** attribute.</span></span> |
|<span data-ttu-id="d2287-124">successCallback</span><span class="sxs-lookup"><span data-stu-id="d2287-124">successCallback</span></span>|<span data-ttu-id="d2287-125">function</span><span class="sxs-lookup"><span data-stu-id="d2287-125">function</span></span>|<span data-ttu-id="d2287-126">Không</span><span class="sxs-lookup"><span data-stu-id="d2287-126">No</span></span>|<span data-ttu-id="d2287-127">A function to execute when the error dialog is closed.</span><span class="sxs-lookup"><span data-stu-id="d2287-127">A function to execute when the error dialog is closed.</span></span>|
|<span data-ttu-id="d2287-128">errorCallback</span><span class="sxs-lookup"><span data-stu-id="d2287-128">errorCallback</span></span>|<span data-ttu-id="d2287-129">function</span><span class="sxs-lookup"><span data-stu-id="d2287-129">function</span></span>|<span data-ttu-id="d2287-130">Không</span><span class="sxs-lookup"><span data-stu-id="d2287-130">No</span></span>|<span data-ttu-id="d2287-131">A function to execute when the operation fails.</span><span class="sxs-lookup"><span data-stu-id="d2287-131">A function to execute when the operation fails.</span></span>|

## <a name="example"></a><span data-ttu-id="d2287-132">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="d2287-132">Example</span></span>

<span data-ttu-id="d2287-133">The following code sample passes an incorrect errorCode (1234) to display an error dialog with default message:</span><span class="sxs-lookup"><span data-stu-id="d2287-133">The following code sample passes an incorrect errorCode (1234) to display an error dialog with default message:</span></span>

```JavaScript
Xrm.Navigation.openErrorDialog({ errorCode:1234 }).then(
    function (success) {
        console.log(success);        
    },
    function (error) {
        console.log(error);
    });
```

<span data-ttu-id="d2287-134">This displays an error dialog with the default message:</span><span class="sxs-lookup"><span data-stu-id="d2287-134">This displays an error dialog with the default message:</span></span>

![Error dialog with default message](../../../media//clientapi_sampleerrordialog.png)

### <a name="related-topics"></a><span data-ttu-id="d2287-136">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="d2287-136">Related topics</span></span>

[<span data-ttu-id="d2287-137">Xrm.Navigation</span><span class="sxs-lookup"><span data-stu-id="d2287-137">Xrm.Navigation</span></span>](../xrm-navigation.md)

