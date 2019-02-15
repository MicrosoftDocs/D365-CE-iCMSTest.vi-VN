---
title: WebDDA Events in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn about using Web data-driven adapter (WebDDA) events that can be used in automations in Unified Service Desk.
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
ms.assetid: 2ecac8dc-d423-405b-bc4e-23b1b05e1d0e
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
ms.openlocfilehash: 564773386817c644c0cd54969193ac9adf76fcd2
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385710"
---
# <a name="webdda-events"></a><span data-ttu-id="30301-103">Sự kiện WebDDA</span><span class="sxs-lookup"><span data-stu-id="30301-103">WebDDA Events</span></span>
<span data-ttu-id="30301-104">Bộ chuyển đổi định hướng dữ liệu web (WebDDA) cung cấp một tập hợp sự kiện có thể được sử dụng trong quá trình tự động hóa.</span><span class="sxs-lookup"><span data-stu-id="30301-104">The Web data-driven adapter (WebDDA) provides a set of events that can be used in automations.</span></span> <span data-ttu-id="30301-105">Các sự kiện có thể được chia thành sự kiện trang và sự kiện kiểm soát.</span><span class="sxs-lookup"><span data-stu-id="30301-105">The events can be divided in page events and control events.</span></span> <span data-ttu-id="30301-106">Chúng ánh xạ cho cùng tên sự kiện được sử dụng trong DOM.</span><span class="sxs-lookup"><span data-stu-id="30301-106">They map to the same event names used in the DOM.</span></span> <span data-ttu-id="30301-107">Để biết thêm thông tin về các sự kiện, hãy xem [Sự kiện](https://msdn.microsoft.com/library/aa768400.aspx)</span><span class="sxs-lookup"><span data-stu-id="30301-107">For more information about the events see [Events](https://msdn.microsoft.com/library/aa768400.aspx)</span></span>  
  
 <span data-ttu-id="30301-108">When registering Action for page events the control parameter in the `RegisterActionForEvent`(For more information, see [Automate hosted applications using HAT automation activities](../unified-service-desk/automate-hosted-applications-using-hat-automation-activities.md)) activity is ignored.</span><span class="sxs-lookup"><span data-stu-id="30301-108">When registering Action for page events the control parameter in the `RegisterActionForEvent`(For more information, see [Automate hosted applications using HAT automation activities](../unified-service-desk/automate-hosted-applications-using-hat-automation-activities.md)) activity is ignored.</span></span> <span data-ttu-id="30301-109">Đối với sự kiện kiểm soát, tham số `ControlName` phải chứa tên kiểm soát được chỉ định trong liên kết.</span><span class="sxs-lookup"><span data-stu-id="30301-109">For control events the `ControlName` parameter must contain the control name that is specified in the bindings.</span></span>  
  
 <span data-ttu-id="30301-110">Một số sự kiện cũng cung cấp dữ liệu bổ sung về sự kiện này.</span><span class="sxs-lookup"><span data-stu-id="30301-110">Some of the events also provide additional data about the event.</span></span> <span data-ttu-id="30301-111">Dữ liệu này có thể được truy cập thông qua hoạt động `GetActionData`.</span><span class="sxs-lookup"><span data-stu-id="30301-111">This data can be accessed via the `GetActionData` activity.</span></span> <span data-ttu-id="30301-112">(For more information, see [Automate hosted applications using HAT automation activities](../unified-service-desk/automate-hosted-applications-using-hat-automation-activities.md)) The following example shows the format they’re provided in.</span><span class="sxs-lookup"><span data-stu-id="30301-112">(For more information, see [Automate hosted applications using HAT automation activities](../unified-service-desk/automate-hosted-applications-using-hat-automation-activities.md)) The following example shows the format they’re provided in.</span></span>  
  
```xml  
<EventArgs[flags] [frame] [headers ] [navigationcontext] [postdata] [url] [urlcontext] [cancel] [type] [key][button]>  
  
```  
  
 <span data-ttu-id="30301-113">Các đối số cung cấp tùy chọn bổ sung cho sự kiện:</span><span class="sxs-lookup"><span data-stu-id="30301-113">The arguments provide additional options for the events:</span></span>  
  
|<span data-ttu-id="30301-114">Đối số</span><span class="sxs-lookup"><span data-stu-id="30301-114">Argument</span></span>|<span data-ttu-id="30301-115">Mô tả</span><span class="sxs-lookup"><span data-stu-id="30301-115">Description</span></span>|  
|--------------|-----------------|  
|`flags`|<span data-ttu-id="30301-116">Một hằng số hoặc giá trị chỉ định tổ hợp các giá trị được xác định bởi liệt kê `BrowserNavConstants`.</span><span class="sxs-lookup"><span data-stu-id="30301-116">A constant or a value that specifies a combination of the values defined by the `BrowserNavConstants` enumeration.</span></span>|  
|`frame`|<span data-ttu-id="30301-117">Biểu thức chuỗi phân biệt chữ hoa chữ thường đánh giá tên khung để hiển thị tài nguyên.</span><span class="sxs-lookup"><span data-stu-id="30301-117">A case-sensitive string expression that evaluates to the name of the frame to display the resource.</span></span> <span data-ttu-id="30301-118">Đó là `NULL`, nếu không có khung được đặt tên nhắm mục tiêu cho tài nguyên.</span><span class="sxs-lookup"><span data-stu-id="30301-118">It is `NULL`, if no named frame is targeted for the resource.</span></span>|  
|`headers`|<span data-ttu-id="30301-119">A string that contains additional HTTP headers to send to the server.</span><span class="sxs-lookup"><span data-stu-id="30301-119">A string that contains additional HTTP headers to send to the server.</span></span> <span data-ttu-id="30301-120">Các tiêu đề này được thêm vào trình duyệt web.</span><span class="sxs-lookup"><span data-stu-id="30301-120">These headers are added to the web browser.</span></span> <span data-ttu-id="30301-121">This parameter is ignored if the URL isn’t an HTTP URL.</span><span class="sxs-lookup"><span data-stu-id="30301-121">This parameter is ignored if the URL isn’t an HTTP URL.</span></span>|  
|`navigationcontext`|<span data-ttu-id="30301-122">Cờ được sử dụng khi mở cửa sổ mới.</span><span class="sxs-lookup"><span data-stu-id="30301-122">Flags used when opening a new window.</span></span> <span data-ttu-id="30301-123">Những giá trị này được sử dụng để xác định liệu một cửa sổ bật lên có được hiển thị không.</span><span class="sxs-lookup"><span data-stu-id="30301-123">These values are used to decide if a pop-up window should be displayed.</span></span>|  
|`postdata`|<span data-ttu-id="30301-124">Data that is sent to the server as part of an HTTPPOST transaction.</span><span class="sxs-lookup"><span data-stu-id="30301-124">Data that is sent to the server as part of an HTTPPOST transaction.</span></span> <span data-ttu-id="30301-125">A POST transaction is typically used to send data gathered by an HTML form.</span><span class="sxs-lookup"><span data-stu-id="30301-125">A POST transaction is typically used to send data gathered by an HTML form.</span></span> <span data-ttu-id="30301-126">If this parameter doesn’t specify any post data, this method issues an HTTP`GET` transaction.</span><span class="sxs-lookup"><span data-stu-id="30301-126">If this parameter doesn’t specify any post data, this method issues an HTTP`GET` transaction.</span></span> <span data-ttu-id="30301-127">This parameter is ignored if the URL is not an HTTP URL.</span><span class="sxs-lookup"><span data-stu-id="30301-127">This parameter is ignored if the URL is not an HTTP URL.</span></span>|  
|`url`|<span data-ttu-id="30301-128">Đã điều hướng tới URL của trang tới sự kiện đó.</span><span class="sxs-lookup"><span data-stu-id="30301-128">URL of the page to that the event was navigated to.</span></span>|  
|`urlcontext`|<span data-ttu-id="30301-129">URL of the page that is opening the new window.</span><span class="sxs-lookup"><span data-stu-id="30301-129">URL of the page that is opening the new window.</span></span> <span data-ttu-id="30301-130">Tham số này là một phần của sự kiện `NewWindow` của trình duyệt web.</span><span class="sxs-lookup"><span data-stu-id="30301-130">This parameter is a part of web browser’s `NewWindow` event.</span></span>|  
|`cancel`|<span data-ttu-id="30301-131">Quá trình tạo trang đã bị hủy (`True`) hoặc đã hoàn tất (`False`).</span><span class="sxs-lookup"><span data-stu-id="30301-131">Page creation was canceled (`True`) or was finished (`False`).</span></span>|  
|`type`|<span data-ttu-id="30301-132">Loại sự kiện, thường giống như chính sự kiện.</span><span class="sxs-lookup"><span data-stu-id="30301-132">Event type, is usually the same as the event itself.</span></span>|  
|`key`|<span data-ttu-id="30301-133">Nút chuột đã được bấm vào tại sự kiện (1=trái, 2=phải, v.v).</span><span class="sxs-lookup"><span data-stu-id="30301-133">Mouse button that was clicked at the event (1=left, 2=right, and so on).</span></span>|  
|`button`|<span data-ttu-id="30301-134">Mã của nút đã được nhấn (ví dụ: mã phím Enter là 13).</span><span class="sxs-lookup"><span data-stu-id="30301-134">Code of the button that was pressed (for example, the Enter key code is 13).</span></span>|  
  
<a name="BKMK_Control"></a>   
## <a name="control-events"></a><span data-ttu-id="30301-135">Sự kiện Kiểm soát</span><span class="sxs-lookup"><span data-stu-id="30301-135">Control Events</span></span>  
 <span data-ttu-id="30301-136">Sự kiện kiểm soát là các sự kiện được liên kết với một kiểm soát.</span><span class="sxs-lookup"><span data-stu-id="30301-136">Control events are the events associated with a control.</span></span>  
  
 <span data-ttu-id="30301-137">Bảng sau liệt kê các sự kiện kiểm soát có sẵn với các tham số tương ứng:</span><span class="sxs-lookup"><span data-stu-id="30301-137">The following table lists the control events that are available with the respective parameters:</span></span>  
  
|||  
|-|-|  
|`Element`|`Description`|  
|<span data-ttu-id="30301-138">BeforeNavigate</span><span class="sxs-lookup"><span data-stu-id="30301-138">BeforeNavigate</span></span>|<span data-ttu-id="30301-139">`flags`, `frame`, `headers`, `navigationcontext`, `postdata`, `url`</span><span class="sxs-lookup"><span data-stu-id="30301-139">`flags`, `frame`, `headers`, `navigationcontext`, `postdata`, `url`</span></span>|  
|<span data-ttu-id="30301-140">onBlur</span><span class="sxs-lookup"><span data-stu-id="30301-140">onblur</span></span>|<span data-ttu-id="30301-141">loại</span><span class="sxs-lookup"><span data-stu-id="30301-141">type</span></span>|  
|<span data-ttu-id="30301-142">onchange</span><span class="sxs-lookup"><span data-stu-id="30301-142">onchange</span></span>|<span data-ttu-id="30301-143">loại</span><span class="sxs-lookup"><span data-stu-id="30301-143">type</span></span>|  
|<span data-ttu-id="30301-144">onclick</span><span class="sxs-lookup"><span data-stu-id="30301-144">onclick</span></span>|<span data-ttu-id="30301-145">loại, nút</span><span class="sxs-lookup"><span data-stu-id="30301-145">type, button</span></span>|  
|<span data-ttu-id="30301-146">ondblclick</span><span class="sxs-lookup"><span data-stu-id="30301-146">ondblclick</span></span>|<span data-ttu-id="30301-147">loại, nút</span><span class="sxs-lookup"><span data-stu-id="30301-147">type, button</span></span>|  
|<span data-ttu-id="30301-148">onfocus</span><span class="sxs-lookup"><span data-stu-id="30301-148">onfocus</span></span>|<span data-ttu-id="30301-149">loại</span><span class="sxs-lookup"><span data-stu-id="30301-149">type</span></span>|  
|<span data-ttu-id="30301-150">onkeydown</span><span class="sxs-lookup"><span data-stu-id="30301-150">onkeydown</span></span>|<span data-ttu-id="30301-151">loại, phím</span><span class="sxs-lookup"><span data-stu-id="30301-151">type, key</span></span>|  
|<span data-ttu-id="30301-152">onmousedown</span><span class="sxs-lookup"><span data-stu-id="30301-152">onmousedown</span></span>|<span data-ttu-id="30301-153">loại, nút</span><span class="sxs-lookup"><span data-stu-id="30301-153">type, button</span></span>|  
|<span data-ttu-id="30301-154">onreset</span><span class="sxs-lookup"><span data-stu-id="30301-154">onreset</span></span>|<span data-ttu-id="30301-155">loại</span><span class="sxs-lookup"><span data-stu-id="30301-155">type</span></span>|  
|<span data-ttu-id="30301-156">onsubmit</span><span class="sxs-lookup"><span data-stu-id="30301-156">onsubmit</span></span>|<span data-ttu-id="30301-157">loại</span><span class="sxs-lookup"><span data-stu-id="30301-157">type</span></span>|  
  
<a name="BKMK_pageevents"></a>   
## <a name="page-events"></a><span data-ttu-id="30301-158">Sự kiện Trang</span><span class="sxs-lookup"><span data-stu-id="30301-158">Page Events</span></span>  
 <span data-ttu-id="30301-159">Khi đăng ký hành động cho sự kiện trang, tham số kiểm soát trong hoạt động `RegisterActionForEvent` bị bỏ qua.</span><span class="sxs-lookup"><span data-stu-id="30301-159">When registering actions for page events, the control parameter in the `RegisterActionForEvent` activity is ignored.</span></span> <span data-ttu-id="30301-160">(For more information, see [Automate hosted applications using HAT automation activities](../unified-service-desk/automate-hosted-applications-using-hat-automation-activities.md))</span><span class="sxs-lookup"><span data-stu-id="30301-160">(For more information, see [Automate hosted applications using HAT automation activities](../unified-service-desk/automate-hosted-applications-using-hat-automation-activities.md))</span></span>  
  
 <span data-ttu-id="30301-161">Bảng sau liệt kê các sự kiện trang có sẵn với các tham số tương ứng:</span><span class="sxs-lookup"><span data-stu-id="30301-161">The following table lists the page events that are available with the respective parameters:</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="30301-162">**Yếu tố**</span><span class="sxs-lookup"><span data-stu-id="30301-162">**Element**</span></span>|<span data-ttu-id="30301-163">**Mô tả**</span><span class="sxs-lookup"><span data-stu-id="30301-163">**Description**</span></span>|  
|<span data-ttu-id="30301-164">BeforeNavigate</span><span class="sxs-lookup"><span data-stu-id="30301-164">BeforeNavigate</span></span>|<span data-ttu-id="30301-165">`flags`, `frame`, `headers`, `navigationcontext`, `postdata`, `url`</span><span class="sxs-lookup"><span data-stu-id="30301-165">`flags`, `frame`, `headers`, `navigationcontext`, `postdata`, `url`</span></span>|  
|<span data-ttu-id="30301-166">BeforeNewWindow</span><span class="sxs-lookup"><span data-stu-id="30301-166">BeforeNewWindow</span></span>|<span data-ttu-id="30301-167">`flags`, `url`, `urlcontext`</span><span class="sxs-lookup"><span data-stu-id="30301-167">`flags`, `url`, `urlcontext`</span></span>|  
|<span data-ttu-id="30301-168">DocumentCompleted</span><span class="sxs-lookup"><span data-stu-id="30301-168">DocumentCompleted</span></span>|<span data-ttu-id="30301-169">`Notification`, `flag`, `url`</span><span class="sxs-lookup"><span data-stu-id="30301-169">`Notification`, `flag`, `url`</span></span>|  
|<span data-ttu-id="30301-170">DownloadStarted</span><span class="sxs-lookup"><span data-stu-id="30301-170">DownloadStarted</span></span>|<span data-ttu-id="30301-171">`Notification`, `flag`, `url`</span><span class="sxs-lookup"><span data-stu-id="30301-171">`Notification`, `flag`, `url`</span></span>|  
|<span data-ttu-id="30301-172">DownloadCompleted</span><span class="sxs-lookup"><span data-stu-id="30301-172">DownloadCompleted</span></span>|<span data-ttu-id="30301-173">`Notification`, `flag`, `url`</span><span class="sxs-lookup"><span data-stu-id="30301-173">`Notification`, `flag`, `url`</span></span>|  
|<span data-ttu-id="30301-174">NewWindow2</span><span class="sxs-lookup"><span data-stu-id="30301-174">NewWindow2</span></span>|`Cancel`|  
|<span data-ttu-id="30301-175">NewWindow3</span><span class="sxs-lookup"><span data-stu-id="30301-175">NewWindow3</span></span>|<span data-ttu-id="30301-176">`flags`, `url`, `urlcontext`, `cancel`</span><span class="sxs-lookup"><span data-stu-id="30301-176">`flags`, `url`, `urlcontext`, `cancel`</span></span>|  
  
### <a name="see-also"></a><span data-ttu-id="30301-177">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="30301-177">See also</span></span>  
 <span data-ttu-id="30301-178">[WebDDA](../unified-service-desk/web-dda.md) </span><span class="sxs-lookup"><span data-stu-id="30301-178">[WebDDA](../unified-service-desk/web-dda.md) </span></span>  
 [<span data-ttu-id="30301-179">Use Data Driven Adapters (DDAs)</span><span class="sxs-lookup"><span data-stu-id="30301-179">Use Data Driven Adapters (DDAs)</span></span>](../unified-service-desk/use-data-driven-adapters-ddas.md)
