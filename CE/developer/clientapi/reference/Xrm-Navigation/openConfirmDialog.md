---
title: openConfirmDialog (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 05/02/2018
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 9c82028d-cbc9-4d40-9987-6ce1ea01fde2
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 0b92d65f0c3fe6e79622dac886ce146efd9c7eb4
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387880"
---
# <a name="openconfirmdialog-client-api-reference"></a><span data-ttu-id="c71fb-102">openConfirmDialog (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="c71fb-102">openConfirmDialog (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/openConfirmDialog-description.md](./includes/openConfirmDialog-description.md)]

## <a name="syntax"></a><span data-ttu-id="c71fb-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="c71fb-103">Syntax</span></span>

`Xrm.Navigation.openConfirmDialog(confirmStrings,confirmOptions).then(successCallback,errorCallback);`

## <a name="parameters"></a><span data-ttu-id="c71fb-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="c71fb-104">Parameters</span></span>

|<span data-ttu-id="c71fb-105">Tên</span><span class="sxs-lookup"><span data-stu-id="c71fb-105">Name</span></span> |<span data-ttu-id="c71fb-106">Loại</span><span class="sxs-lookup"><span data-stu-id="c71fb-106">Type</span></span> |<span data-ttu-id="c71fb-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="c71fb-107">Required</span></span> |<span data-ttu-id="c71fb-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="c71fb-108">Description</span></span> |
|---|---|---|---|
|<span data-ttu-id="c71fb-109">confirmStrings</span><span class="sxs-lookup"><span data-stu-id="c71fb-109">confirmStrings</span></span>|<span data-ttu-id="c71fb-110">Đối tượng</span><span class="sxs-lookup"><span data-stu-id="c71fb-110">Object</span></span>|<span data-ttu-id="c71fb-111">Có</span><span class="sxs-lookup"><span data-stu-id="c71fb-111">Yes</span></span>|<span data-ttu-id="c71fb-112">The strings to be used in the confirmation dialog.</span><span class="sxs-lookup"><span data-stu-id="c71fb-112">The strings to be used in the confirmation dialog.</span></span> <span data-ttu-id="c71fb-113">The object contains the following attributes:</span><span class="sxs-lookup"><span data-stu-id="c71fb-113">The object contains the following attributes:</span></span><br/><span data-ttu-id="c71fb-114">- **cancelButtonLabel**: (Optional) String.</span><span class="sxs-lookup"><span data-stu-id="c71fb-114">- **cancelButtonLabel**: (Optional) String.</span></span> <span data-ttu-id="c71fb-115">The cancel button label.</span><span class="sxs-lookup"><span data-stu-id="c71fb-115">The cancel button label.</span></span> <span data-ttu-id="c71fb-116">If you do not specify the cancel button label, **Cancel** is used as the button label.</span><span class="sxs-lookup"><span data-stu-id="c71fb-116">If you do not specify the cancel button label, **Cancel** is used as the button label.</span></span><br/><span data-ttu-id="c71fb-117">- **confirmButtonLabel**: (Optional) String.</span><span class="sxs-lookup"><span data-stu-id="c71fb-117">- **confirmButtonLabel**: (Optional) String.</span></span> <span data-ttu-id="c71fb-118">The confirm button label.</span><span class="sxs-lookup"><span data-stu-id="c71fb-118">The confirm button label.</span></span> <span data-ttu-id="c71fb-119">If you do not specify the confirm button label, **OK** is used as the button label.</span><span class="sxs-lookup"><span data-stu-id="c71fb-119">If you do not specify the confirm button label, **OK** is used as the button label.</span></span><br/><span data-ttu-id="c71fb-120">- **subtitle**: (Optional) String.</span><span class="sxs-lookup"><span data-stu-id="c71fb-120">- **subtitle**: (Optional) String.</span></span> <span data-ttu-id="c71fb-121">The subtitle to be displayed in the confirmation dialog.</span><span class="sxs-lookup"><span data-stu-id="c71fb-121">The subtitle to be displayed in the confirmation dialog.</span></span><br/><span data-ttu-id="c71fb-122">- **text**: String.</span><span class="sxs-lookup"><span data-stu-id="c71fb-122">- **text**: String.</span></span> <span data-ttu-id="c71fb-123">The message to be displayed in the confirmation dialog.</span><span class="sxs-lookup"><span data-stu-id="c71fb-123">The message to be displayed in the confirmation dialog.</span></span><br/><span data-ttu-id="c71fb-124">- **title**: (Optional) String.</span><span class="sxs-lookup"><span data-stu-id="c71fb-124">- **title**: (Optional) String.</span></span> <span data-ttu-id="c71fb-125">The title to be displayed in the confirmation dialog.</span><span class="sxs-lookup"><span data-stu-id="c71fb-125">The title to be displayed in the confirmation dialog.</span></span>|
|<span data-ttu-id="c71fb-126">confirmOptions</span><span class="sxs-lookup"><span data-stu-id="c71fb-126">confirmOptions</span></span>|<span data-ttu-id="c71fb-127">Đối tượng</span><span class="sxs-lookup"><span data-stu-id="c71fb-127">Object</span></span>|<span data-ttu-id="c71fb-128">Không</span><span class="sxs-lookup"><span data-stu-id="c71fb-128">No</span></span>|<span data-ttu-id="c71fb-129">The height and width options for confirmation dialog.</span><span class="sxs-lookup"><span data-stu-id="c71fb-129">The height and width options for confirmation dialog.</span></span> <span data-ttu-id="c71fb-130">The object contains the following attributes:</span><span class="sxs-lookup"><span data-stu-id="c71fb-130">The object contains the following attributes:</span></span><br/><span data-ttu-id="c71fb-131">- **height**: (Optional) Number.</span><span class="sxs-lookup"><span data-stu-id="c71fb-131">- **height**: (Optional) Number.</span></span> <span data-ttu-id="c71fb-132">Height of the confirmation dialog in pixels.</span><span class="sxs-lookup"><span data-stu-id="c71fb-132">Height of the confirmation dialog in pixels.</span></span><br/><span data-ttu-id="c71fb-133">- **width**: (Optional) Number.</span><span class="sxs-lookup"><span data-stu-id="c71fb-133">- **width**: (Optional) Number.</span></span> <span data-ttu-id="c71fb-134">Width of the confirmation dialog in pixels.</span><span class="sxs-lookup"><span data-stu-id="c71fb-134">Width of the confirmation dialog in pixels.</span></span>|
|<span data-ttu-id="c71fb-135">successCallback</span><span class="sxs-lookup"><span data-stu-id="c71fb-135">successCallback</span></span>|<span data-ttu-id="c71fb-136">function</span><span class="sxs-lookup"><span data-stu-id="c71fb-136">function</span></span>|<span data-ttu-id="c71fb-137">Không</span><span class="sxs-lookup"><span data-stu-id="c71fb-137">No</span></span>|<span data-ttu-id="c71fb-138">A function to execute when the confirmation dialog is closed by clicking the confirm, cancel, or **X** in the top-right corner of the dialog.</span><span class="sxs-lookup"><span data-stu-id="c71fb-138">A function to execute when the confirmation dialog is closed by clicking the confirm, cancel, or **X** in the top-right corner of the dialog.</span></span> <span data-ttu-id="c71fb-139">An object with the **confirmed** (Boolean) attribute is passed that indicates whether the confirm button was clicked to close the dialog.</span><span class="sxs-lookup"><span data-stu-id="c71fb-139">An object with the **confirmed** (Boolean) attribute is passed that indicates whether the confirm button was clicked to close the dialog.</span></span>|
|<span data-ttu-id="c71fb-140">errorCallback</span><span class="sxs-lookup"><span data-stu-id="c71fb-140">errorCallback</span></span>|<span data-ttu-id="c71fb-141">function</span><span class="sxs-lookup"><span data-stu-id="c71fb-141">function</span></span>|<span data-ttu-id="c71fb-142">Không</span><span class="sxs-lookup"><span data-stu-id="c71fb-142">No</span></span>|<span data-ttu-id="c71fb-143">A function to execute when the operation fails.</span><span class="sxs-lookup"><span data-stu-id="c71fb-143">A function to execute when the operation fails.</span></span>|

## <a name="example"></a><span data-ttu-id="c71fb-144">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="c71fb-144">Example</span></span>

<span data-ttu-id="c71fb-145">The following code sample displays a confirmation dialog box.</span><span class="sxs-lookup"><span data-stu-id="c71fb-145">The following code sample displays a confirmation dialog box.</span></span> <span data-ttu-id="c71fb-146">Appropriate message is logged in the console depending on whether confirm or cancel/**X** was clicked to close the dialog.</span><span class="sxs-lookup"><span data-stu-id="c71fb-146">Appropriate message is logged in the console depending on whether confirm or cancel/**X** was clicked to close the dialog.</span></span>

```JavaScript
var confirmStrings = { text:"This is a confirmation.", title:"Confirmation Dialog" };
var confirmOptions = { height: 200, width: 450 };
Xrm.Navigation.openConfirmDialog(confirmStrings, confirmOptions).then(
function (success) {    
    if (success.confirmed)
        console.log("Dialog closed using OK button.");
    else
        console.log("Dialog closed using Cancel button or X.");
});
```

### <a name="related-topics"></a><span data-ttu-id="c71fb-147">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="c71fb-147">Related topics</span></span>

[<span data-ttu-id="c71fb-148">Xrm.Navigation</span><span class="sxs-lookup"><span data-stu-id="c71fb-148">Xrm.Navigation</span></span>](../xrm-navigation.md)

