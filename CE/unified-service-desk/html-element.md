---
title: HtmlElement in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: The <HTMLElement> element associates a named control to the HTML object specified by the search path. Chủ đề này mô tả các yếu tố của <HTMLElement>.
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
ms.assetid: 72a912d3-c16d-4e38-9367-bc2722ac0fa6
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
ms.openlocfilehash: 8e80aa1c6cad4c93dd1a5db12710a7472ea7e3cb
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387780"
---
# <a name="htmlelement-in-unified-service-desk"></a><span data-ttu-id="ec0ec-104">HtmlElement in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="ec0ec-104">HtmlElement in Unified Service Desk</span></span>
<span data-ttu-id="ec0ec-105">The `<HTMLElement>` element associates a named control to the `HTML` object specified by the search path.</span><span class="sxs-lookup"><span data-stu-id="ec0ec-105">The `<HTMLElement>` element associates a named control to the `HTML` object specified by the search path.</span></span> <span data-ttu-id="ec0ec-106">Chủ đề này mô tả các yếu tố của `<HTMLElement>`.</span><span class="sxs-lookup"><span data-stu-id="ec0ec-106">This topic describes the elements of `<HTMLElement>`.</span></span>  
  
## <a name="htmlelement-syntax"></a><span data-ttu-id="ec0ec-107">\<HTMLElement> syntax</span><span class="sxs-lookup"><span data-stu-id="ec0ec-107">\<HTMLElement> syntax</span></span>  
 <span data-ttu-id="ec0ec-108">The following code snippet shows how \<HTMLElement> is used:</span><span class="sxs-lookup"><span data-stu-id="ec0ec-108">The following code snippet shows how \<HTMLElement> is used:</span></span>  
  
```xml  
<HTMLElement name="control name">  
Search Path Elements  
</HTMLElement>  
```  
  
## <a name="elements-of-htmlelement"></a><span data-ttu-id="ec0ec-109">Elements of \<HTMLElement></span><span class="sxs-lookup"><span data-stu-id="ec0ec-109">Elements of \<HTMLElement></span></span>  
 <span data-ttu-id="ec0ec-110">Bảng sau mô tả các yếu tố của thẻ `<HTMLElement>`.</span><span class="sxs-lookup"><span data-stu-id="ec0ec-110">The following table describes the elements of the `<HTMLElement>` tag.</span></span>  
  
|<span data-ttu-id="ec0ec-111">Yếu tố</span><span class="sxs-lookup"><span data-stu-id="ec0ec-111">Element</span></span>|<span data-ttu-id="ec0ec-112">Mô tả</span><span class="sxs-lookup"><span data-stu-id="ec0ec-112">Description</span></span>|  
|-------------|-----------------|  
|`FindControl`|<span data-ttu-id="ec0ec-113">Trả về `True` nếu kiểm soát có thể được tìm thấy trên giao diện người dùng (UI), nếu không `False`.</span><span class="sxs-lookup"><span data-stu-id="ec0ec-113">Returns `True` if the control can be found on the user interface (UI), otherwise `False`.</span></span>|  
|`GetControlValue`|<span data-ttu-id="ec0ec-114">Trả về nội dung của đối tượng `HTML`.</span><span class="sxs-lookup"><span data-stu-id="ec0ec-114">Returns the content of the `HTML` object.</span></span>|  
|`SetControlValue`|<span data-ttu-id="ec0ec-115">Throws an `UnsupportedControlOperation` exception.</span><span class="sxs-lookup"><span data-stu-id="ec0ec-115">Throws an `UnsupportedControlOperation` exception.</span></span>|  
|`ExecuteControlAction`|<span data-ttu-id="ec0ec-116">Executes a `Click()` command on the control.</span><span class="sxs-lookup"><span data-stu-id="ec0ec-116">Executes a `Click()` command on the control.</span></span>|  
  
### <a name="see-also"></a><span data-ttu-id="ec0ec-117">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="ec0ec-117">See also</span></span>  
 <span data-ttu-id="ec0ec-118">[WebDDA](../unified-service-desk/web-dda.md) </span><span class="sxs-lookup"><span data-stu-id="ec0ec-118">[WebDDA](../unified-service-desk/web-dda.md) </span></span>  
 [<span data-ttu-id="ec0ec-119">Use Data Driven Adapters (DDAs)</span><span class="sxs-lookup"><span data-stu-id="ec0ec-119">Use Data Driven Adapters (DDAs)</span></span>](../unified-service-desk/use-data-driven-adapters-ddas.md)
