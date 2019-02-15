---
title: save (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 03e970ee-7ed3-4df2-9670-222d76a479fd
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 30d37713624e3d3c8338697650867fb6e34a4016
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386155"
---
# <a name="save-client-api-reference"></a><span data-ttu-id="760da-102">save (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="760da-102">save (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/save-description.md](./includes/save-description.md)]

<span data-ttu-id="760da-103">You can also set an object to control how appointment, recurring appointment, or service activity records are processed.</span><span class="sxs-lookup"><span data-stu-id="760da-103">You can also set an object to control how appointment, recurring appointment, or service activity records are processed.</span></span>

## <a name="syntax"></a><span data-ttu-id="760da-104">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="760da-104">Syntax</span></span>

`formContext.data.save(saveOptions).then(successCallback, errorCallback);`

## <a name="parameters"></a><span data-ttu-id="760da-105">Tham số</span><span class="sxs-lookup"><span data-stu-id="760da-105">Parameters</span></span>

|<span data-ttu-id="760da-106">Tên</span><span class="sxs-lookup"><span data-stu-id="760da-106">Name</span></span>|<span data-ttu-id="760da-107">Loại</span><span class="sxs-lookup"><span data-stu-id="760da-107">Type</span></span>|<span data-ttu-id="760da-108">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="760da-108">Required</span></span>|<span data-ttu-id="760da-109">Mô tả</span><span class="sxs-lookup"><span data-stu-id="760da-109">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="760da-110">saveOptions</span><span class="sxs-lookup"><span data-stu-id="760da-110">saveOptions</span></span>|<span data-ttu-id="760da-111">Đối tượng</span><span class="sxs-lookup"><span data-stu-id="760da-111">Object</span></span>|<span data-ttu-id="760da-112">Không</span><span class="sxs-lookup"><span data-stu-id="760da-112">No</span></span>|<span data-ttu-id="760da-113">An object for specifying options for saving the record.</span><span class="sxs-lookup"><span data-stu-id="760da-113">An object for specifying options for saving the record.</span></span> <span data-ttu-id="760da-114">Đối tượng có các thuộc tính sau đây:</span><span class="sxs-lookup"><span data-stu-id="760da-114">The object has following attributes:</span></span><br/><br/><span data-ttu-id="760da-115">- **saveMode**: (Optional) Number.</span><span class="sxs-lookup"><span data-stu-id="760da-115">- **saveMode**: (Optional) Number.</span></span> <span data-ttu-id="760da-116">Specify a value indicating how the save event was initiated.</span><span class="sxs-lookup"><span data-stu-id="760da-116">Specify a value indicating how the save event was initiated.</span></span> <span data-ttu-id="760da-117">For a list of supported values, see the return value of the [getSaveMode](../save-event-arguments/getsavemode.md) method.</span><span class="sxs-lookup"><span data-stu-id="760da-117">For a list of supported values, see the return value of the [getSaveMode](../save-event-arguments/getsavemode.md) method.</span></span> <span data-ttu-id="760da-118">Note that setting the **saveMode** does not actually take the corresponding action; it is just to provide information to the **OnSave** event handlers about the reason for the save operation.</span><span class="sxs-lookup"><span data-stu-id="760da-118">Note that setting the **saveMode** does not actually take the corresponding action; it is just to provide information to the **OnSave** event handlers about the reason for the save operation.</span></span><br/><br/><span data-ttu-id="760da-119">- **useSchedulingEngine**: (Optional) Boolean.</span><span class="sxs-lookup"><span data-stu-id="760da-119">- **useSchedulingEngine**: (Optional) Boolean.</span></span> <span data-ttu-id="760da-120">Indicate whether to use the **Book** or **Reschedule** messages rather than the **Create** or **Update** messages.</span><span class="sxs-lookup"><span data-stu-id="760da-120">Indicate whether to use the **Book** or **Reschedule** messages rather than the **Create** or **Update** messages.</span></span> <span data-ttu-id="760da-121">This option is only applicable when used with appointment, recurring appointment, or service activity records.</span><span class="sxs-lookup"><span data-stu-id="760da-121">This option is only applicable when used with appointment, recurring appointment, or service activity records.</span></span>|
|<span data-ttu-id="760da-122">successCallback</span><span class="sxs-lookup"><span data-stu-id="760da-122">successCallback</span></span>|<span data-ttu-id="760da-123">Hàm</span><span class="sxs-lookup"><span data-stu-id="760da-123">Function</span></span>|<span data-ttu-id="760da-124">Không</span><span class="sxs-lookup"><span data-stu-id="760da-124">No</span></span>|<span data-ttu-id="760da-125">A function to call when the operation succeeds.</span><span class="sxs-lookup"><span data-stu-id="760da-125">A function to call when the operation succeeds.</span></span>|
|<span data-ttu-id="760da-126">errorCallback</span><span class="sxs-lookup"><span data-stu-id="760da-126">errorCallback</span></span>|<span data-ttu-id="760da-127">Hàm</span><span class="sxs-lookup"><span data-stu-id="760da-127">Function</span></span>|<span data-ttu-id="760da-128">Không</span><span class="sxs-lookup"><span data-stu-id="760da-128">No</span></span>|<span data-ttu-id="760da-129">A function to call when the operation fails.</span><span class="sxs-lookup"><span data-stu-id="760da-129">A function to call when the operation fails.</span></span> <span data-ttu-id="760da-130">An object with the following properties will be passed:</span><span class="sxs-lookup"><span data-stu-id="760da-130">An object with the following properties will be passed:</span></span><br/><br/><span data-ttu-id="760da-131">- **errorCode**: Number.</span><span class="sxs-lookup"><span data-stu-id="760da-131">- **errorCode**: Number.</span></span> <span data-ttu-id="760da-132">The error code.</span><span class="sxs-lookup"><span data-stu-id="760da-132">The error code.</span></span><br/><br/><span data-ttu-id="760da-133">- **message**: String.</span><span class="sxs-lookup"><span data-stu-id="760da-133">- **message**: String.</span></span> <span data-ttu-id="760da-134">A localized error message.</span><span class="sxs-lookup"><span data-stu-id="760da-134">A localized error message.</span></span>|


### <a name="related-topics"></a><span data-ttu-id="760da-135">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="760da-135">Related topics</span></span>

[<span data-ttu-id="760da-136">formContext.data.entity.save</span><span class="sxs-lookup"><span data-stu-id="760da-136">formContext.data.entity.save</span></span>](../formContext-data-entity/save.md)

[<span data-ttu-id="760da-137">formContext</span><span class="sxs-lookup"><span data-stu-id="760da-137">formContext</span></span>](../../clientapi-form-context.md)

