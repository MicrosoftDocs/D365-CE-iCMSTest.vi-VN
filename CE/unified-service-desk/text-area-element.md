---
title: TextAreaElement in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn about using TextAreaElement in Unified Service Desk used to associate a named control with a text area element on the HTML page.
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
ms.assetid: eccf015f-836a-4f4d-8fe7-01ff2405d6c5
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
ms.openlocfilehash: 165c8db78df28c85a9ff6771fa44f5b130543540
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388081"
---
# <a name="textareaelement-in-unified-service-desk"></a><span data-ttu-id="94aa1-103">TextAreaElement in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="94aa1-103">TextAreaElement in Unified Service Desk</span></span>
<span data-ttu-id="94aa1-104">Yếu tố `<TextAreaElement>` liên kết một kiểm soát có tên với yếu tố khu vực văn bản trên trang `HTML`.</span><span class="sxs-lookup"><span data-stu-id="94aa1-104">`<TextAreaElement>` element associates a named control with a text area element on the `HTML` page.</span></span> <span data-ttu-id="94aa1-105">Chủ đề này mô tả các yếu tố của `<TextAreaElement>`.</span><span class="sxs-lookup"><span data-stu-id="94aa1-105">This topic describes the elements of `<TextAreaElement>`.</span></span>  
  
## <a name="textareaelement-syntax"></a><span data-ttu-id="94aa1-106">\<TextAreaElement> syntax</span><span class="sxs-lookup"><span data-stu-id="94aa1-106">\<TextAreaElement> syntax</span></span>  
 <span data-ttu-id="94aa1-107">Đoạn mã sau hiển thị cách sử dụng `<TextAreaElement>`.</span><span class="sxs-lookup"><span data-stu-id="94aa1-107">The following code snippet shows how `<TextAreaElement>` is used.</span></span>  
  
```xml  
<TextAreaElement name="name goes here">  
Search Path Elements  
</TextAreaElement>  
  
```  
  
## <a name="elements-of-textareaelement"></a><span data-ttu-id="94aa1-108">Elements of \<TextAreaElement></span><span class="sxs-lookup"><span data-stu-id="94aa1-108">Elements of \<TextAreaElement></span></span>  
 <span data-ttu-id="94aa1-109">Bảng sau mô tả các yếu tố của thẻ `<TextAreaElement>`:</span><span class="sxs-lookup"><span data-stu-id="94aa1-109">The following table describes the elements of the `<TextAreaElement>` tag:</span></span>  
  
|<span data-ttu-id="94aa1-110">Yếu tố</span><span class="sxs-lookup"><span data-stu-id="94aa1-110">Element</span></span>|<span data-ttu-id="94aa1-111">Mô tả</span><span class="sxs-lookup"><span data-stu-id="94aa1-111">Description</span></span>|  
|-------------|-----------------|  
|`FindControl`|<span data-ttu-id="94aa1-112">Trả về `True` nếu kiểm soát có thể được tìm thấy trên giao diện người dùng (UI), nếu không `False`.</span><span class="sxs-lookup"><span data-stu-id="94aa1-112">Returns `True` if the control can be found on the user interface (UI), otherwise `False`.</span></span>|  
|`GetControlValue`|<span data-ttu-id="94aa1-113">Trả về giá trị của yếu tố khu vực văn bản.</span><span class="sxs-lookup"><span data-stu-id="94aa1-113">Returns the value of the text area element.</span></span>|  
|`SetControlValue`|<span data-ttu-id="94aa1-114">Đặt giá trị của yếu tố khu vực văn bản.</span><span class="sxs-lookup"><span data-stu-id="94aa1-114">Sets the value of a text area element.</span></span>|  
|`ExecuteControlAction`|<span data-ttu-id="94aa1-115">Throws an `UnsupportedControlOperation` exception.</span><span class="sxs-lookup"><span data-stu-id="94aa1-115">Throws an `UnsupportedControlOperation` exception.</span></span>|  
  
### <a name="see-also"></a><span data-ttu-id="94aa1-116">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="94aa1-116">See also</span></span>  
 <span data-ttu-id="94aa1-117">[WebDDA](../unified-service-desk/web-dda.md) </span><span class="sxs-lookup"><span data-stu-id="94aa1-117">[WebDDA](../unified-service-desk/web-dda.md) </span></span>  
 [<span data-ttu-id="94aa1-118">Use Data Driven Adapters (DDAs)</span><span class="sxs-lookup"><span data-stu-id="94aa1-118">Use Data Driven Adapters (DDAs)</span></span>](../unified-service-desk/use-data-driven-adapters-ddas.md)
