---
title: InputElement in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: The topic describes the elements of <IntputElement>.
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
ms.assetid: 80a0bb8c-e9c1-45d4-9600-fc929654f681
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
ms.openlocfilehash: beb9d1a8ffb531e857d76bf48b3d0b8f87ebcc8d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387724"
---
# <a name="inputelement-in-unified-service-desk"></a><span data-ttu-id="fa068-103">InputElement in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="fa068-103">InputElement in Unified Service Desk</span></span>
<span data-ttu-id="fa068-104">Yếu tố `<InputElement>` liên kết kiểm soát có tên với yếu tố `<input/> HTML` nếu yếu tố này có một trong các giá trị `type=attribute` sau: `check box`, `radio`, `text`, `password`, `submit`, `reset`, `hidden`, `image` hoặc `file`.</span><span class="sxs-lookup"><span data-stu-id="fa068-104">`<InputElement>` element associates a named control with an `<input/> HTML` element if the element has one of the following `type=attribute` values: `check box`, `radio`, `text`, `password`, `submit`, `reset`, `hidden`, `image`, or `file`.</span></span> <span data-ttu-id="fa068-105">Chủ đề này mô tả các yếu tố của `<IntputElement>`.</span><span class="sxs-lookup"><span data-stu-id="fa068-105">This topic describes the elements of `<IntputElement>`.</span></span>  
  
## <a name="inputelement-syntax"></a><span data-ttu-id="fa068-106">\<InputElement> syntax</span><span class="sxs-lookup"><span data-stu-id="fa068-106">\<InputElement> syntax</span></span>  
 <span data-ttu-id="fa068-107">Đoạn mã sau hiển thị cách sử dụng `<InputElement>`:</span><span class="sxs-lookup"><span data-stu-id="fa068-107">The following code snippet shows how `<InputElement>` is used:</span></span>  
  
```xml  
<InputElement name="control name" type="type">  
Search Path Elements  
</InputElement>  
  
```  
  
## <a name="elements-of-inputelement"></a><span data-ttu-id="fa068-108">Elements of \<InputElement></span><span class="sxs-lookup"><span data-stu-id="fa068-108">Elements of \<InputElement></span></span>  
 <span data-ttu-id="fa068-109">Bảng sau mô tả các yếu tố của thẻ `<InputElement>`.</span><span class="sxs-lookup"><span data-stu-id="fa068-109">The following table describes the elements of the `<InputElement>` tag.</span></span>  
  
|<span data-ttu-id="fa068-110">Yếu tố</span><span class="sxs-lookup"><span data-stu-id="fa068-110">Element</span></span>|<span data-ttu-id="fa068-111">Mô tả</span><span class="sxs-lookup"><span data-stu-id="fa068-111">Description</span></span>|  
|-------------|-----------------|  
|`FindControl`|<span data-ttu-id="fa068-112">Trả về `True` nếu kiểm soát có thể được tìm thấy trên giao diện người dùng (UI), nếu không `False`</span><span class="sxs-lookup"><span data-stu-id="fa068-112">Returns `True` if the control can be found on the user interface (UI), otherwise `False`</span></span>|  
|`GetControlValue`|<span data-ttu-id="fa068-113">Trả về `True` hoặc `False` (giá trị chuỗi) khi `type="checkbox"` hoặc `type="radio"`.</span><span class="sxs-lookup"><span data-stu-id="fa068-113">Returns `True` or `False` (string-valued) when `type="checkbox"` or `type="radio"`.</span></span> <span data-ttu-id="fa068-114">Trả về giá trị của yếu tố cho tất cả các loại khác.</span><span class="sxs-lookup"><span data-stu-id="fa068-114">Returns the value of the element for all other types.</span></span>|  
|`SetControlValue`|<span data-ttu-id="fa068-115">Đặt thành `True` hoặc `False` khi `type="checkbox"` hoặc `type="radio"`.</span><span class="sxs-lookup"><span data-stu-id="fa068-115">Sets to `True` or `False` when `type="checkbox"` or `type="radio"`.</span></span> <span data-ttu-id="fa068-116">Thiết lập giá trị của yếu tố khi `type="text"` hoặc `type="password"` hoặc `type="hidden"`.</span><span class="sxs-lookup"><span data-stu-id="fa068-116">Sets the value of the element when `type="text"` or `type="password"` or `type="hidden"`.</span></span> <span data-ttu-id="fa068-117">Áp dụng một ngoại lệ `UnsupportedControlOperation` cho tất cả các loại khác.</span><span class="sxs-lookup"><span data-stu-id="fa068-117">Throws an `UnsupportedControlOperation` exception for all other types.</span></span>|  
|`ExecuteControlAction`|<span data-ttu-id="fa068-118">Đảo ngược `True` hoặc trạng thái `False` hiện có khi `type="checkbox"`.</span><span class="sxs-lookup"><span data-stu-id="fa068-118">Inverts an existing `True` or `False` state when `type="checkbox"`.</span></span> <span data-ttu-id="fa068-119">Đặt trạng thái thành `True` khi `type="radio"`.</span><span class="sxs-lookup"><span data-stu-id="fa068-119">Sets state to `True` when `type="radio"`.</span></span> <span data-ttu-id="fa068-120">Trả về `UnsupportedControlOperation` khi `type="text"` hoặc `type="password"` hoặc `type="hidden"`.</span><span class="sxs-lookup"><span data-stu-id="fa068-120">Returns `UnsupportedControlOperation` when `type="text"` or `type="password"` or `type="hidden"`.</span></span> <span data-ttu-id="fa068-121">Gây ra vấn đề `Click()` cho tất cả các loại khác.</span><span class="sxs-lookup"><span data-stu-id="fa068-121">Issues a `Click()` for all other types.</span></span>|  
  
### <a name="see-also"></a><span data-ttu-id="fa068-122">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="fa068-122">See also</span></span>  
 <span data-ttu-id="fa068-123">[WebDDA](../unified-service-desk/web-dda.md) </span><span class="sxs-lookup"><span data-stu-id="fa068-123">[WebDDA](../unified-service-desk/web-dda.md) </span></span>  
 [<span data-ttu-id="fa068-124">Use Data Driven Adapters (DDAs)</span><span class="sxs-lookup"><span data-stu-id="fa068-124">Use Data Driven Adapters (DDAs)</span></span>](../unified-service-desk/use-data-driven-adapters-ddas.md)
