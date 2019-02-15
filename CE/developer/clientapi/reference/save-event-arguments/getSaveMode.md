---
title: getSaveMode (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
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
ms.openlocfilehash: 7a4a46d1257d42803801412ee832b4faa40d0867
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387365"
---
# <a name="getsavemode-client-api-reference"></a><span data-ttu-id="1a69b-102">getSaveMode (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="1a69b-102">getSaveMode (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getSaveMode-description.md](./includes/getSaveMode-description.md)]

## <a name="syntax"></a><span data-ttu-id="1a69b-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="1a69b-103">Syntax</span></span>

`executionContext.getEventArgs().getSaveMode()`

## <a name="return-value"></a><span data-ttu-id="1a69b-104">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="1a69b-104">Return Value</span></span>

<span data-ttu-id="1a69b-105">**Type**: Number</span><span class="sxs-lookup"><span data-stu-id="1a69b-105">**Type**: Number</span></span>

<span data-ttu-id="1a69b-106">**Description**: The following table describes the supported values returned to detect different ways entity records may be saved by the user.</span><span class="sxs-lookup"><span data-stu-id="1a69b-106">**Description**: The following table describes the supported values returned to detect different ways entity records may be saved by the user.</span></span>

|<span data-ttu-id="1a69b-107">Value</span><span class="sxs-lookup"><span data-stu-id="1a69b-107">Value</span></span> |<span data-ttu-id="1a69b-108">Save mode</span><span class="sxs-lookup"><span data-stu-id="1a69b-108">Save mode</span></span> |<span data-ttu-id="1a69b-109">Thực thể</span><span class="sxs-lookup"><span data-stu-id="1a69b-109">Entity</span></span>|
|---|---|---|
|<span data-ttu-id="1a69b-110">1</span><span class="sxs-lookup"><span data-stu-id="1a69b-110">1</span></span>|<span data-ttu-id="1a69b-111">Lưu</span><span class="sxs-lookup"><span data-stu-id="1a69b-111">Save</span></span>|<span data-ttu-id="1a69b-112">Tất cả</span><span class="sxs-lookup"><span data-stu-id="1a69b-112">All</span></span>|
|<span data-ttu-id="1a69b-113">2</span><span class="sxs-lookup"><span data-stu-id="1a69b-113">2</span></span>|<span data-ttu-id="1a69b-114">Lưu và Đóng</span><span class="sxs-lookup"><span data-stu-id="1a69b-114">Save and Close</span></span>|<span data-ttu-id="1a69b-115">Tất cả</span><span class="sxs-lookup"><span data-stu-id="1a69b-115">All</span></span>|
|<span data-ttu-id="1a69b-116">5</span><span class="sxs-lookup"><span data-stu-id="1a69b-116">5</span></span>|<span data-ttu-id="1a69b-117">Dừng kích hoạt</span><span class="sxs-lookup"><span data-stu-id="1a69b-117">Deactivate</span></span>|<span data-ttu-id="1a69b-118">Tất cả</span><span class="sxs-lookup"><span data-stu-id="1a69b-118">All</span></span>|
|<span data-ttu-id="1a69b-119">6</span><span class="sxs-lookup"><span data-stu-id="1a69b-119">6</span></span>|<span data-ttu-id="1a69b-120">Reactivate</span><span class="sxs-lookup"><span data-stu-id="1a69b-120">Reactivate</span></span>|<span data-ttu-id="1a69b-121">Tất cả</span><span class="sxs-lookup"><span data-stu-id="1a69b-121">All</span></span>|
|<span data-ttu-id="1a69b-122">7</span><span class="sxs-lookup"><span data-stu-id="1a69b-122">7</span></span>|<span data-ttu-id="1a69b-123">Gửi</span><span class="sxs-lookup"><span data-stu-id="1a69b-123">Send</span></span>|<span data-ttu-id="1a69b-124">Email</span><span class="sxs-lookup"><span data-stu-id="1a69b-124">Email</span></span>|
|<span data-ttu-id="1a69b-125">15</span><span class="sxs-lookup"><span data-stu-id="1a69b-125">15</span></span>|<span data-ttu-id="1a69b-126">Disqualify</span><span class="sxs-lookup"><span data-stu-id="1a69b-126">Disqualify</span></span>|<span data-ttu-id="1a69b-127">Khách hàng tiềm năng</span><span class="sxs-lookup"><span data-stu-id="1a69b-127">Lead</span></span>|
|<span data-ttu-id="1a69b-128">16</span><span class="sxs-lookup"><span data-stu-id="1a69b-128">16</span></span>|<span data-ttu-id="1a69b-129">Bao gồm</span><span class="sxs-lookup"><span data-stu-id="1a69b-129">Qualify</span></span>|<span data-ttu-id="1a69b-130">Khách hàng tiềm năng</span><span class="sxs-lookup"><span data-stu-id="1a69b-130">Lead</span></span>|
|<span data-ttu-id="1a69b-131">47</span><span class="sxs-lookup"><span data-stu-id="1a69b-131">47</span></span>|<span data-ttu-id="1a69b-132">Chỉ định</span><span class="sxs-lookup"><span data-stu-id="1a69b-132">Assign</span></span>|<span data-ttu-id="1a69b-133">User or Team owned entities</span><span class="sxs-lookup"><span data-stu-id="1a69b-133">User or Team owned entities</span></span>|
|<span data-ttu-id="1a69b-134">58</span><span class="sxs-lookup"><span data-stu-id="1a69b-134">58</span></span>|<span data-ttu-id="1a69b-135">Save as Completed</span><span class="sxs-lookup"><span data-stu-id="1a69b-135">Save as Completed</span></span>|<span data-ttu-id="1a69b-136">Hoạt động</span><span class="sxs-lookup"><span data-stu-id="1a69b-136">Activities</span></span>|
|<span data-ttu-id="1a69b-137">59</span><span class="sxs-lookup"><span data-stu-id="1a69b-137">59</span></span>|<span data-ttu-id="1a69b-138">Save and New</span><span class="sxs-lookup"><span data-stu-id="1a69b-138">Save and New</span></span>|<span data-ttu-id="1a69b-139">Tất cả</span><span class="sxs-lookup"><span data-stu-id="1a69b-139">All</span></span>|
|<span data-ttu-id="1a69b-140">70</span><span class="sxs-lookup"><span data-stu-id="1a69b-140">70</span></span>|<span data-ttu-id="1a69b-141">Auto Save</span><span class="sxs-lookup"><span data-stu-id="1a69b-141">Auto Save</span></span>|<span data-ttu-id="1a69b-142">Tất cả</span><span class="sxs-lookup"><span data-stu-id="1a69b-142">All</span></span>|

## <a name="remarks"></a><span data-ttu-id="1a69b-143">Chú thích</span><span class="sxs-lookup"><span data-stu-id="1a69b-143">Remarks</span></span>

<span data-ttu-id="1a69b-144">This method is essential if you want to enable auto-save for most forms in an organization but disable it for specific forms.</span><span class="sxs-lookup"><span data-stu-id="1a69b-144">This method is essential if you want to enable auto-save for most forms in an organization but disable it for specific forms.</span></span>  

## <a name="example"></a><span data-ttu-id="1a69b-145">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="1a69b-145">Example</span></span>

<span data-ttu-id="1a69b-146">The following code registered for the **OnSave** event with the execution context passed to it will prevent any saves that initiate from an auto-save but allow all others.</span><span class="sxs-lookup"><span data-stu-id="1a69b-146">The following code registered for the **OnSave** event with the execution context passed to it will prevent any saves that initiate from an auto-save but allow all others.</span></span> <span data-ttu-id="1a69b-147">With auto-save enabled, navigating away is equivalent to **Save and Close**.</span><span class="sxs-lookup"><span data-stu-id="1a69b-147">With auto-save enabled, navigating away is equivalent to **Save and Close**.</span></span> <span data-ttu-id="1a69b-148">This code will prevent any saves that are initiated by the 30 second timer or when people navigate away from a form with unsaved data.</span><span class="sxs-lookup"><span data-stu-id="1a69b-148">This code will prevent any saves that are initiated by the 30 second timer or when people navigate away from a form with unsaved data.</span></span>

```JavaScript
function preventAutoSave(executionContext) {
    var eventArgs = executionContext.getEventArgs();
    if (eventArgs.getSaveMode() == 70 || eventArgs.getSaveMode() == 2) {
        eventArgs.preventDefault();
    }
}
```

<span data-ttu-id="1a69b-149">To save a record the user must click the **Save** icon at the bottom of the form or a custom **Save** command needs to be added to the command bar.</span><span class="sxs-lookup"><span data-stu-id="1a69b-149">To save a record the user must click the **Save** icon at the bottom of the form or a custom **Save** command needs to be added to the command bar.</span></span>

### <a name="related-topics"></a><span data-ttu-id="1a69b-150">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="1a69b-150">Related topics</span></span>

[<span data-ttu-id="1a69b-151">isDefaultPrevented</span><span class="sxs-lookup"><span data-stu-id="1a69b-151">isDefaultPrevented</span></span>](isDefaultPrevented.md)

[<span data-ttu-id="1a69b-152">preventDefault</span><span class="sxs-lookup"><span data-stu-id="1a69b-152">preventDefault</span></span>](preventDefault.md)

