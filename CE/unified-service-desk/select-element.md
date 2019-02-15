---
title: SelectElement in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn about SelectElement in Unified Service Desk to search for a named control on the HTML page.
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
ms.assetid: 6a5148e9-871e-41d1-8f70-b11175b1c42c
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
ms.openlocfilehash: f23443cd311594e095fa3a5988e5501ad5bc2566
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385938"
---
# <a name="selectelement-in-unified-service-desk"></a><span data-ttu-id="593ed-103">SelectElement in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="593ed-103">SelectElement in Unified Service Desk</span></span>
<span data-ttu-id="593ed-104">Yếu tố `<SelectElement>` tìm kiếm một kiểm soát được đặt tên trên trang `HTML` và trả lại hoặc đảo ngược giá trị của nó.</span><span class="sxs-lookup"><span data-stu-id="593ed-104">`<SelectElement>` element searches for a named control on an `HTML` page, and returns or reverses its value.</span></span> <span data-ttu-id="593ed-105">Chủ đề này mô tả các yếu tố của `<SelectElement>`</span><span class="sxs-lookup"><span data-stu-id="593ed-105">This topic describes the elements of `<SelectElement>`</span></span>  
  
## <a name="selectelement-syntax"></a><span data-ttu-id="593ed-106">\<SelectElement> syntax</span><span class="sxs-lookup"><span data-stu-id="593ed-106">\<SelectElement> syntax</span></span>  
 <span data-ttu-id="593ed-107">Đoạn mã sau hiển thị cách sử dụng `<SelectElement>`:</span><span class="sxs-lookup"><span data-stu-id="593ed-107">The following code snippet shows how `<SelectElement>` is used:</span></span>  
  
```xml  
<SelectElement name="control name">  
Search Path Elements  
</SelectElement>  
  
```  
  
## <a name="elements-of-selectelement"></a><span data-ttu-id="593ed-108">Elements of \<SelectElement></span><span class="sxs-lookup"><span data-stu-id="593ed-108">Elements of \<SelectElement></span></span>  
 <span data-ttu-id="593ed-109">Bảng sau mô tả các yếu tố của thẻ `<SelectElement>`.</span><span class="sxs-lookup"><span data-stu-id="593ed-109">The following table describes the elements of the `<SelectElement>` tag.</span></span>  
  
|<span data-ttu-id="593ed-110">Yếu tố</span><span class="sxs-lookup"><span data-stu-id="593ed-110">Element</span></span>|<span data-ttu-id="593ed-111">Mô tả</span><span class="sxs-lookup"><span data-stu-id="593ed-111">Description</span></span>|  
|-------------|-----------------|  
|`FindControl`|<span data-ttu-id="593ed-112">Trả về `True` hoặc `False` tùy thuộc vào việc kiểm soát có thể được tìm thấy trên giao diện người dùng (UI) hay không.</span><span class="sxs-lookup"><span data-stu-id="593ed-112">Returns `True` or `False` depending on whether the control can be found on the user interface (UI).</span></span>|  
|`GetControlValue`|<span data-ttu-id="593ed-113">Trả về (các) mục đã chọn dưới dạng danh sách được phân tách bằng dấu phẩy.</span><span class="sxs-lookup"><span data-stu-id="593ed-113">Returns the selected item(s), as a comma-separated list.</span></span>|  
|`SetControlValue`|<span data-ttu-id="593ed-114">Đảo ngược trạng thái lựa chọn của mục phù hợp đầu tiên trong danh sách.</span><span class="sxs-lookup"><span data-stu-id="593ed-114">Inverts the selection status of the first matching item in the list.</span></span> <span data-ttu-id="593ed-115">Điều này xóa toàn bộ lựa chọn khi văn bản thiết lập được cung cấp trống.</span><span class="sxs-lookup"><span data-stu-id="593ed-115">This clears the entire selection when the provided set text is empty.</span></span>|  
|`ExecuteControlAction`|<span data-ttu-id="593ed-116">Đối với chế độ một lựa chọn, điều này đảo ngược trạng thái lựa chọn của lựa chọn hiện tại.</span><span class="sxs-lookup"><span data-stu-id="593ed-116">For single-selection modes, this inverts the selection status of the current selection.</span></span> <span data-ttu-id="593ed-117">Đối với chế độ đa lựa chọn, điều này thêm mục chưa chọn tiếp theo vào lựa chọn hiện tại</span><span class="sxs-lookup"><span data-stu-id="593ed-117">For multi-selection modes, it adds the next unselected item to the current selection</span></span>|  
  
### <a name="see-also"></a><span data-ttu-id="593ed-118">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="593ed-118">See also</span></span>  
 <span data-ttu-id="593ed-119">[WebDDA](../unified-service-desk/web-dda.md) </span><span class="sxs-lookup"><span data-stu-id="593ed-119">[WebDDA](../unified-service-desk/web-dda.md) </span></span>  
 [<span data-ttu-id="593ed-120">Use Data Driven Adapters (DDAs)</span><span class="sxs-lookup"><span data-stu-id="593ed-120">Use Data Driven Adapters (DDAs)</span></span>](../unified-service-desk/use-data-driven-adapters-ddas.md)
