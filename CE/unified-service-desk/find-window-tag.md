---
title: FindWindow Tag in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Thẻ <FindWindow> bao gồm danh sách các yếu tố phụ thể hiện một chuỗi toán thử phù hợp, tất cả chúng cần thành công cho cửa sổ mục tiêu để được xem xét tìm thấy.
ms.custom:
- dyn365-USD
ms.date: 08/23/2017
ms.reviewer: ''
ms.service: dynamics-365-customerservice
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: 1e3efa2f-e888-4a92-a32a-1990735fd936
caps.latest.revision: 7
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 02db1269d611580cbd6d2fd5de9036a83f6ce8fd
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387182"
---
# <a name="findwindow-tag-in-unified-service-desk"></a><span data-ttu-id="1d65b-103">FindWindow Tag in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="1d65b-103">FindWindow Tag in Unified Service Desk</span></span>
<span data-ttu-id="1d65b-104">Thẻ `<FindWindow>` bao gồm danh sách các yếu tố phụ thể hiện một chuỗi toán thử phù hợp, tất cả chúng cần thành công cho cửa sổ mục tiêu để được xem xét tìm thấy.</span><span class="sxs-lookup"><span data-stu-id="1d65b-104">The `<FindWindow>` tag consists of a list of child elements that represent a sequence of match operations, all of which need to succeed for the target window to be considered found.</span></span>  
  
 <span data-ttu-id="1d65b-105">Đoạn mã sau đây cho thấy cách sử dụng các yếu tố `<FindWindow>` khác nhau để tìm cửa sổ mục tiêu:</span><span class="sxs-lookup"><span data-stu-id="1d65b-105">The following code snippet shows how the various `<FindWindow>` elements are used to find the target window:</span></span>  
  
```xml  
# RELAX NG XML grammar for FindWindow  
# http://relaxng.org/compact-tutorial-20030326.html  
#  
grammar {  
   start      = FindWindow  
   FindWindow = element FindWindow {  
element ControlId { attribute match { xsd:integer }?, text }*  
& element Caption { attribute match { xsd:integer }?, text }*  
& element CaptionStartsWith { same as Caption }*  
& element CaptionEndsWith { same as Caption }*  
& element CaptionContains { same as Caption }*  
& element Class { attribute match { xsd:integer }?, text }*  
& element ClassStartsWith { same as Class }*  
& element ClassEndsWith { same as Class }*  
& element ClassContains { same as Class }*  
& element Find { Caption & Class }*  
& element Desktop { empty }*  
& element Application { empty }*  
& element Owner { empty }*  
& element RelaxProcessIdRestriction { empty }*  
& element RelaxThreadIdRestriction  { empty }*  
}  
}  
  
```  
  
### <a name="findwindow-tag-elements"></a><span data-ttu-id="1d65b-106">\<FindWindow> tag elements</span><span class="sxs-lookup"><span data-stu-id="1d65b-106">\<FindWindow> tag elements</span></span>  
 <span data-ttu-id="1d65b-107">Bảng sau mô tả các yếu tố khác nhau của thẻ `<FindWindow>`:</span><span class="sxs-lookup"><span data-stu-id="1d65b-107">The following table describes the various elements of the `<FindWindow>` tag:</span></span>  
  
|<span data-ttu-id="1d65b-108">Yếu tố</span><span class="sxs-lookup"><span data-stu-id="1d65b-108">Element</span></span>|<span data-ttu-id="1d65b-109">Mô tả</span><span class="sxs-lookup"><span data-stu-id="1d65b-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="1d65b-110">ControlId</span><span class="sxs-lookup"><span data-stu-id="1d65b-110">ControlId</span></span>|<span data-ttu-id="1d65b-111">Cửa sổ với ID.</span><span class="sxs-lookup"><span data-stu-id="1d65b-111">Window with ID.</span></span>|  
|<span data-ttu-id="1d65b-112">Caption</span><span class="sxs-lookup"><span data-stu-id="1d65b-112">Caption</span></span>|<span data-ttu-id="1d65b-113">Văn bản chú thích cửa sổ.</span><span class="sxs-lookup"><span data-stu-id="1d65b-113">Window caption text.</span></span>|  
|<span data-ttu-id="1d65b-114">CaptionStartsWith</span><span class="sxs-lookup"><span data-stu-id="1d65b-114">CaptionStartsWith</span></span>|<span data-ttu-id="1d65b-115">Chú thích bắt đầu bằng văn bản.</span><span class="sxs-lookup"><span data-stu-id="1d65b-115">Caption starts with text.</span></span>|  
|<span data-ttu-id="1d65b-116">CaptionEndsWith</span><span class="sxs-lookup"><span data-stu-id="1d65b-116">CaptionEndsWith</span></span>|<span data-ttu-id="1d65b-117">Chú thích kết thúc bằng văn bản.</span><span class="sxs-lookup"><span data-stu-id="1d65b-117">Caption ends with text.</span></span>|  
|<span data-ttu-id="1d65b-118">CaptionContains</span><span class="sxs-lookup"><span data-stu-id="1d65b-118">CaptionContains</span></span>|<span data-ttu-id="1d65b-119">Chú thích có chứa văn bản.</span><span class="sxs-lookup"><span data-stu-id="1d65b-119">Caption contains text.</span></span>|  
|<span data-ttu-id="1d65b-120">Lớp</span><span class="sxs-lookup"><span data-stu-id="1d65b-120">Class</span></span>|<span data-ttu-id="1d65b-121">Cửa sổ với tên lớp.</span><span class="sxs-lookup"><span data-stu-id="1d65b-121">Window with class name.</span></span>|  
|<span data-ttu-id="1d65b-122">ClassStartsWith</span><span class="sxs-lookup"><span data-stu-id="1d65b-122">ClassStartsWith</span></span>|<span data-ttu-id="1d65b-123">Tên lớp bắt đầu bằng văn bản.</span><span class="sxs-lookup"><span data-stu-id="1d65b-123">Class name stats with text.</span></span>|  
|<span data-ttu-id="1d65b-124">ClassEndsWith</span><span class="sxs-lookup"><span data-stu-id="1d65b-124">ClassEndsWith</span></span>|<span data-ttu-id="1d65b-125">Tên lớp kết thúc bằng văn bản.</span><span class="sxs-lookup"><span data-stu-id="1d65b-125">Class name ends with text.</span></span>|  
|<span data-ttu-id="1d65b-126">ClassContains</span><span class="sxs-lookup"><span data-stu-id="1d65b-126">ClassContains</span></span>|<span data-ttu-id="1d65b-127">Lớp có chứa văn bản.</span><span class="sxs-lookup"><span data-stu-id="1d65b-127">Class contains text.</span></span>|  
|<span data-ttu-id="1d65b-128">Find</span><span class="sxs-lookup"><span data-stu-id="1d65b-128">Find</span></span>|<span data-ttu-id="1d65b-129">Tìm kiếm cho cửa sổ như được chỉ định qua yếu tố `Class` hoặc `Caption`.</span><span class="sxs-lookup"><span data-stu-id="1d65b-129">Searches for window as specified via `Class` or `Caption` element.</span></span>|  
|<span data-ttu-id="1d65b-130">Desktop</span><span class="sxs-lookup"><span data-stu-id="1d65b-130">Desktop</span></span>|<span data-ttu-id="1d65b-131">Đặt điểm tìm cho máy tính để bàn.</span><span class="sxs-lookup"><span data-stu-id="1d65b-131">Sets the search point to the desktop.</span></span>|  
|<span data-ttu-id="1d65b-132">Application</span><span class="sxs-lookup"><span data-stu-id="1d65b-132">Application</span></span>|<span data-ttu-id="1d65b-133">Đặt điểm tìm cho cửa sổ ứng dụng cấp cao nhất.</span><span class="sxs-lookup"><span data-stu-id="1d65b-133">Sets the search point to the applications top-level window.</span></span>|  
|<span data-ttu-id="1d65b-134">Chủ sở hữu</span><span class="sxs-lookup"><span data-stu-id="1d65b-134">Owner</span></span>|<span data-ttu-id="1d65b-135">Cửa sổ với chủ sở hữu được chỉ định.</span><span class="sxs-lookup"><span data-stu-id="1d65b-135">Window with specified owner.</span></span>|  
|<span data-ttu-id="1d65b-136">RelaxProcessIdRestriction</span><span class="sxs-lookup"><span data-stu-id="1d65b-136">RelaxProcessIdRestriction</span></span>|<span data-ttu-id="1d65b-137">Bao gồm các cửa sổ với các ID quá trình khác nhau trong tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="1d65b-137">Includes windows with different process IDs in search.</span></span> <span data-ttu-id="1d65b-138">Theo mặc định, tất cả cửa sổ thuộc về cùng ID quá trình.</span><span class="sxs-lookup"><span data-stu-id="1d65b-138">By default, all windows belong to the same process ID.</span></span>|  
|<span data-ttu-id="1d65b-139">RelaxThreadIdRestriction</span><span class="sxs-lookup"><span data-stu-id="1d65b-139">RelaxThreadIdRestriction</span></span>|<span data-ttu-id="1d65b-140">Bao gồm các cửa sổ với ID chuỗi chủ đề khác nhau trong quá trình tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="1d65b-140">Includes windows with different thread ID in search process.</span></span> <span data-ttu-id="1d65b-141">Theo mặc định, tất cả cửa sổ thuộc về cùng ID chuỗi chủ đề.</span><span class="sxs-lookup"><span data-stu-id="1d65b-141">By default all windows belong to the same thread ID.</span></span>|  
  
 <span data-ttu-id="1d65b-142">The following XML shows control definition using the **\<FindWindow>** tag.</span><span class="sxs-lookup"><span data-stu-id="1d65b-142">The following XML shows control definition using the **\<FindWindow>** tag.</span></span>  
  
```xml  
<FindWindow>  
<Desktop/>  
<Caption match="1">Font</Caption>  
<Class>#32770</Class>  
<Caption>OK</Caption>  
</FindWindow>  
<FindWindow>  
<Application/>  
<ControlId>7d</ControlId>  
</FindWindow>  
<FindWindow>  
<Desktop/>  
<Class>Notepad</Class>  
</FindWindow>  
  
```  
  
 <span data-ttu-id="1d65b-143">Trong ví dụ `XML` trước, các yếu tố có các định nghĩa sau:</span><span class="sxs-lookup"><span data-stu-id="1d65b-143">In the preceding `XML` example, the elements have the following definitions:</span></span>  
  
- <span data-ttu-id="1d65b-144">`<Application/>` – Đặt cửa sổ ngữ cảnh thành cửa sổ ứng dụng cấp cao nhất.</span><span class="sxs-lookup"><span data-stu-id="1d65b-144">`<Application/>` – Sets the context window to the top-level window of the application.</span></span> <span data-ttu-id="1d65b-145">By default, the context is initialized to the top-level window before the first child node in \<FindWindow/>.</span><span class="sxs-lookup"><span data-stu-id="1d65b-145">By default, the context is initialized to the top-level window before the first child node in \<FindWindow/>.</span></span>  
  
- <span data-ttu-id="1d65b-146">`<Desktop/>` – Đặt cửa sổ bối cảnh ở cửa sổ máy tính để bàn cấp gốc.</span><span class="sxs-lookup"><span data-stu-id="1d65b-146">`<Desktop/>` – Sets the context window to the root-level desktop window.</span></span>  
  
- <span data-ttu-id="1d65b-147">\<Caption match="1">Font\</Caption> – Searches the window hierarchy, starting at the current context window and working down the hierarchy, for the first window with caption text that matches the text provided.</span><span class="sxs-lookup"><span data-stu-id="1d65b-147">\<Caption match="1">Font\</Caption> – Searches the window hierarchy, starting at the current context window and working down the hierarchy, for the first window with caption text that matches the text provided.</span></span> <span data-ttu-id="1d65b-148">Nếu `match="2"`, nó tìm kiếm cửa sổ thứ hai với văn bản chú thích phù hợp với văn bản đã cung cấp.</span><span class="sxs-lookup"><span data-stu-id="1d65b-148">If `match="2"`, it searches for the second window with caption text that matches the provided text.</span></span> <span data-ttu-id="1d65b-149">Nếu không có thuộc tính `match` được cung cấp,  `match="1"` là mặc định.</span><span class="sxs-lookup"><span data-stu-id="1d65b-149">If no `match` attribute is provided,  `match="1"` is the default.</span></span> <span data-ttu-id="1d65b-150">So sánh văn bản là kết quả phù hợp chuỗi con so với văn bản chú thích.</span><span class="sxs-lookup"><span data-stu-id="1d65b-150">The text comparison is a substring match against the caption text.</span></span> <span data-ttu-id="1d65b-151">Nếu văn bản được cung cấp có thể được tìm thấy là chuỗi con trong chú thích của cửa sổ chủ đề, đó được coi là một kết quả phù hợp.</span><span class="sxs-lookup"><span data-stu-id="1d65b-151">If the provided text can be found as a substring in the subject window's caption, it is considered a match.</span></span> <span data-ttu-id="1d65b-152">Cửa sổ ghép đôi phù hợp sẽ trở thành cửa sổ ngữ cảnh mới.</span><span class="sxs-lookup"><span data-stu-id="1d65b-152">The successful matching window becomes the new context window.</span></span> <span data-ttu-id="1d65b-153">Nếu không tìm thấy kết quả phù hợp, tìm kiếm thất bại.</span><span class="sxs-lookup"><span data-stu-id="1d65b-153">If no match is found, the search fails.</span></span> <span data-ttu-id="1d65b-154">Theo mặc định, chỉ có cửa sổ thuộc cùng `ProcessId` và `ThreadId` mới được coi là kết quả phù hợp.</span><span class="sxs-lookup"><span data-stu-id="1d65b-154">By default, only windows that belong to the same `ProcessId` and `ThreadId` are considered a match.</span></span>  
  
- <span data-ttu-id="1d65b-155">`<Class>#32770</Class>` – Tìm kiếm hệ thống cấp bậc cửa sổ, cho cửa sổ đầu tiên với văn bản lớp phù hợp với văn bản đã chọn.</span><span class="sxs-lookup"><span data-stu-id="1d65b-155">`<Class>#32770</Class>` – Searches the window hierarchy, for the first window with class text that matches the provided text.</span></span> <span data-ttu-id="1d65b-156">Tất cả các chi tiết hành vi khác giống nhau để `<Caption/>.`</span><span class="sxs-lookup"><span data-stu-id="1d65b-156">All other behavioral details are identical to `<Caption/>.`</span></span>  
  
- <span data-ttu-id="1d65b-157">`<ControlId>7d</ControlId>` – Tìm kiếm hệ thống cấp bậc cửa sổ, cho cửa sổ đầu tiên với ID kiểm soát phù hợp với giá trị đã cung cấp.</span><span class="sxs-lookup"><span data-stu-id="1d65b-157">`<ControlId>7d</ControlId>` – Searches the window hierarchy, for the first window with a control ID that matches the provided value.</span></span> <span data-ttu-id="1d65b-158">Đây phải là kết quả phù hợp chính xác.</span><span class="sxs-lookup"><span data-stu-id="1d65b-158">This must be an exact match.</span></span> <span data-ttu-id="1d65b-159">Tất cả các chi tiết hành vi khác giống nhau để `<Caption/>`.</span><span class="sxs-lookup"><span data-stu-id="1d65b-159">All other behavioral details are identical to `<Caption/>`.</span></span>  
  
  <span data-ttu-id="1d65b-160">The following XML searches for the window with the caption **OK** in the first window with the caption **Font** and the class ID 32770, starting at the desktop.</span><span class="sxs-lookup"><span data-stu-id="1d65b-160">The following XML searches for the window with the caption **OK** in the first window with the caption **Font** and the class ID 32770, starting at the desktop.</span></span>  
  
```xml  
<FindWindow>  
<Desktop/>  
<Caption match="1">Font</Caption>  
<Class>#32770</Class>  
<Caption>OK</Caption>  
</FindWindow>  
  
```  
  
 <span data-ttu-id="1d65b-161">`XML` sau tìm kiếm cửa sổ với ID Kiểm soát 7D, bắt đầu ở cửa sổ cấp cao nhất của ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="1d65b-161">The following `XML` looks for the window with Control ID 7D, starting at the application's top-level window.</span></span>  
  
```xml  
<FindWindow>  
<Application/>  
<ControlId>7d</ControlId>  
</FindWindow>  
  
```  
  
 <span data-ttu-id="1d65b-162">`XML` sau tìm kiếm cửa sổ (đầu tiên) với tên lớp **Notepad**, bắt đầu tại màn hình.</span><span class="sxs-lookup"><span data-stu-id="1d65b-162">The following `XML` searches for the (first) window with the class name **Notepad**, starting at the desktop.</span></span>  
  
```xml  
<FindWindow>  
<Desktop/>  
<Class>Notepad</Class>  
</FindWindow>  
  
```  
  
### <a name="see-also"></a><span data-ttu-id="1d65b-163">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="1d65b-163">See also</span></span>  
 <span data-ttu-id="1d65b-164">[Win DDA](../unified-service-desk/windda.md) </span><span class="sxs-lookup"><span data-stu-id="1d65b-164">[Win DDA](../unified-service-desk/windda.md) </span></span>  
 [<span data-ttu-id="1d65b-165">Use Data Driven Adapters (DDAs)</span><span class="sxs-lookup"><span data-stu-id="1d65b-165">Use Data Driven Adapters (DDAs)</span></span>](../unified-service-desk/use-data-driven-adapters-ddas.md)
