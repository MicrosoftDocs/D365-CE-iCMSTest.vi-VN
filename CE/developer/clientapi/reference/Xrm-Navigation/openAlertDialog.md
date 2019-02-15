---
title: openAlertDialog (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 8615a284-41b4-479c-81bd-577b3b7c79ad
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 338b064b8a046d13a1c84ef6eeff8e0bf2d88083
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385565"
---
# <a name="openalertdialog-client-api-reference"></a><span data-ttu-id="4ffa1-102">openAlertDialog (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="4ffa1-102">openAlertDialog (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/openAlertDialog-description.md](./includes/openAlertDialog-description.md)]

## <a name="syntax"></a><span data-ttu-id="4ffa1-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="4ffa1-103">Syntax</span></span>

`Xrm.Navigation.openAlertDialog(alertStrings,alertOptions).then(closeCallback,errorCallback);`

## <a name="parameters"></a><span data-ttu-id="4ffa1-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="4ffa1-104">Parameters</span></span>

|<span data-ttu-id="4ffa1-105">Tên</span><span class="sxs-lookup"><span data-stu-id="4ffa1-105">Name</span></span> |<span data-ttu-id="4ffa1-106">Loại</span><span class="sxs-lookup"><span data-stu-id="4ffa1-106">Type</span></span> |<span data-ttu-id="4ffa1-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="4ffa1-107">Required</span></span> |<span data-ttu-id="4ffa1-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="4ffa1-108">Description</span></span> |
|---|---|---|---|
|<span data-ttu-id="4ffa1-109">alertStrings</span><span class="sxs-lookup"><span data-stu-id="4ffa1-109">alertStrings</span></span>|<span data-ttu-id="4ffa1-110">Đối tượng</span><span class="sxs-lookup"><span data-stu-id="4ffa1-110">Object</span></span>|<span data-ttu-id="4ffa1-111">Có</span><span class="sxs-lookup"><span data-stu-id="4ffa1-111">Yes</span></span>|<span data-ttu-id="4ffa1-112">The strings to be used in the alert dialog.</span><span class="sxs-lookup"><span data-stu-id="4ffa1-112">The strings to be used in the alert dialog.</span></span> <span data-ttu-id="4ffa1-113">The object contains the following attributes:</span><span class="sxs-lookup"><span data-stu-id="4ffa1-113">The object contains the following attributes:</span></span><br/><span data-ttu-id="4ffa1-114">- **confirmButtonLabel**: (Optional) String.</span><span class="sxs-lookup"><span data-stu-id="4ffa1-114">- **confirmButtonLabel**: (Optional) String.</span></span> <span data-ttu-id="4ffa1-115">The confirm button label.</span><span class="sxs-lookup"><span data-stu-id="4ffa1-115">The confirm button label.</span></span> <span data-ttu-id="4ffa1-116">If you do not specify the button label, **OK** is used as the button label.</span><span class="sxs-lookup"><span data-stu-id="4ffa1-116">If you do not specify the button label, **OK** is used as the button label.</span></span><br/><span data-ttu-id="4ffa1-117">- **text**: String.</span><span class="sxs-lookup"><span data-stu-id="4ffa1-117">- **text**: String.</span></span> <span data-ttu-id="4ffa1-118">The message to be displyed in the alert dialog.</span><span class="sxs-lookup"><span data-stu-id="4ffa1-118">The message to be displyed in the alert dialog.</span></span>|
|<span data-ttu-id="4ffa1-119">alertOptions</span><span class="sxs-lookup"><span data-stu-id="4ffa1-119">alertOptions</span></span>|<span data-ttu-id="4ffa1-120">Đối tượng</span><span class="sxs-lookup"><span data-stu-id="4ffa1-120">Object</span></span>|<span data-ttu-id="4ffa1-121">Không</span><span class="sxs-lookup"><span data-stu-id="4ffa1-121">No</span></span>|<span data-ttu-id="4ffa1-122">The height and width options for alert dialog.</span><span class="sxs-lookup"><span data-stu-id="4ffa1-122">The height and width options for alert dialog.</span></span> <span data-ttu-id="4ffa1-123">The object contains the following attributes:</span><span class="sxs-lookup"><span data-stu-id="4ffa1-123">The object contains the following attributes:</span></span><br/><span data-ttu-id="4ffa1-124">- **height**: (Optional) Number.</span><span class="sxs-lookup"><span data-stu-id="4ffa1-124">- **height**: (Optional) Number.</span></span> <span data-ttu-id="4ffa1-125">Height of the alert dialog in pixels.</span><span class="sxs-lookup"><span data-stu-id="4ffa1-125">Height of the alert dialog in pixels.</span></span><br/><span data-ttu-id="4ffa1-126">- **width**: (Optional) Number.</span><span class="sxs-lookup"><span data-stu-id="4ffa1-126">- **width**: (Optional) Number.</span></span> <span data-ttu-id="4ffa1-127">Width of the alert dialog pixels.</span><span class="sxs-lookup"><span data-stu-id="4ffa1-127">Width of the alert dialog pixels.</span></span>|
|<span data-ttu-id="4ffa1-128">successCallback</span><span class="sxs-lookup"><span data-stu-id="4ffa1-128">successCallback</span></span>|<span data-ttu-id="4ffa1-129">function</span><span class="sxs-lookup"><span data-stu-id="4ffa1-129">function</span></span>|<span data-ttu-id="4ffa1-130">Không</span><span class="sxs-lookup"><span data-stu-id="4ffa1-130">No</span></span>|<span data-ttu-id="4ffa1-131">A function to execute when the alert dialog is closed by either clicking the confirm button or canceled by pressing ESC.</span><span class="sxs-lookup"><span data-stu-id="4ffa1-131">A function to execute when the alert dialog is closed by either clicking the confirm button or canceled by pressing ESC.</span></span>|
|<span data-ttu-id="4ffa1-132">errorCallback</span><span class="sxs-lookup"><span data-stu-id="4ffa1-132">errorCallback</span></span>|<span data-ttu-id="4ffa1-133">function</span><span class="sxs-lookup"><span data-stu-id="4ffa1-133">function</span></span>|<span data-ttu-id="4ffa1-134">Không</span><span class="sxs-lookup"><span data-stu-id="4ffa1-134">No</span></span>|<span data-ttu-id="4ffa1-135">A function to execute when the operation fails.</span><span class="sxs-lookup"><span data-stu-id="4ffa1-135">A function to execute when the operation fails.</span></span>|


## <a name="example"></a><span data-ttu-id="4ffa1-136">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="4ffa1-136">Example</span></span>

<span data-ttu-id="4ffa1-137">The following sample code displays an alert dialog.</span><span class="sxs-lookup"><span data-stu-id="4ffa1-137">The following sample code displays an alert dialog.</span></span> <span data-ttu-id="4ffa1-138">Clicking **Yes** button in the alert dialog or canceling the alert dialog by pressing ESC calls the `close` function::</span><span class="sxs-lookup"><span data-stu-id="4ffa1-138">Clicking **Yes** button in the alert dialog or canceling the alert dialog by pressing ESC calls the `close` function::</span></span>

```JavaScript
var alertStrings = { confirmButtonLabel: "Yes", text: "This is an alert." };
var alertOptions = { height: 120, width: 260 };
Xrm.Navigation.openAlertDialog(alertStrings, alertOptions).then(
    function success(result) {
        console.log("Alert dialog closed");
    },
    function (error) {
        console.log(error.message);
    }
);
```

### <a name="related-topics"></a><span data-ttu-id="4ffa1-139">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="4ffa1-139">Related topics</span></span>

[<span data-ttu-id="4ffa1-140">Xrm.navigation</span><span class="sxs-lookup"><span data-stu-id="4ffa1-140">Xrm.navigation</span></span>](../xrm-navigation.md)

