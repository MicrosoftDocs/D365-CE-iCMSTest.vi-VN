---
title: AnchorElement | MicrosoftDocs
description: The topic explains about <AnchorElement> element which is one of the binding elements of the WebDDA.
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
ms.assetid: 2332b53a-92e6-419f-aace-af6dfda0dcb7
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
ms.openlocfilehash: 8a86b56f35c2113d688cace91316e66f707d3cc4
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388519"
---
# <a name="anchorelement"></a><span data-ttu-id="10da0-103">AnchorElement</span><span class="sxs-lookup"><span data-stu-id="10da0-103">AnchorElement</span></span>
<span data-ttu-id="10da0-104">Yếu tố `<AnchorElement>` là một trong các yếu tố liên kết của WebDDA.</span><span class="sxs-lookup"><span data-stu-id="10da0-104">`<AnchorElement>` element is one of the binding elements of the WebDDA.</span></span>  
  
## <a name="anchorelement-syntax"></a><span data-ttu-id="10da0-105">\<AnchorElement> syntax</span><span class="sxs-lookup"><span data-stu-id="10da0-105">\<AnchorElement> syntax</span></span>  
 <span data-ttu-id="10da0-106">`<AnchorElement>` associates a named control to an `<a/> HTML`  element.</span><span class="sxs-lookup"><span data-stu-id="10da0-106">`<AnchorElement>` associates a named control to an `<a/> HTML`  element.</span></span> <span data-ttu-id="10da0-107">Đoạn mã sau hiển thị cách sử dụng `<AnchorElement>`.</span><span class="sxs-lookup"><span data-stu-id="10da0-107">The following code snippet shows how `<AnchorElement>` is used.</span></span>  
  
```xml  
<AnchorElement name="control name">  
Search Path Elements  
</AnchorElement>  
  
```  
  
## <a name="anchorelement-elements"></a><span data-ttu-id="10da0-108">\<AnchorElement> elements</span><span class="sxs-lookup"><span data-stu-id="10da0-108">\<AnchorElement> elements</span></span>  
 <span data-ttu-id="10da0-109">Bảng sau mô tả các yếu tố khác nhau của `<AnchorElement>`:</span><span class="sxs-lookup"><span data-stu-id="10da0-109">The following table describes the various elements of `<AnchorElement>`:</span></span>  
  
|<span data-ttu-id="10da0-110">Yếu tố</span><span class="sxs-lookup"><span data-stu-id="10da0-110">Element</span></span>|<span data-ttu-id="10da0-111">Mô tả</span><span class="sxs-lookup"><span data-stu-id="10da0-111">Descripton</span></span>|  
|-------------|----------------|  
|`FindControl`|<span data-ttu-id="10da0-112">Trả về **True** hoặc **False** tùy theo có thể tìm thấy kiểm soát trên giao diện người dùng (UI) hay không.</span><span class="sxs-lookup"><span data-stu-id="10da0-112">Returns **True** or **False** depending on whether the control can be found on the user interface (UI).</span></span>|  
|`GetControlValue`|<span data-ttu-id="10da0-113">Returns the URL text.</span><span class="sxs-lookup"><span data-stu-id="10da0-113">Returns the URL text.</span></span>|  
|`SetControlValue`|<span data-ttu-id="10da0-114">Throws an `UnsupportedControlOperation` exception.</span><span class="sxs-lookup"><span data-stu-id="10da0-114">Throws an `UnsupportedControlOperation` exception.</span></span>|  
|`ExecuteControlAction`|<span data-ttu-id="10da0-115">Navigates to the specified URL.</span><span class="sxs-lookup"><span data-stu-id="10da0-115">Navigates to the specified URL.</span></span>|  
  
### <a name="see-also"></a><span data-ttu-id="10da0-116">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="10da0-116">See also</span></span>  
 <span data-ttu-id="10da0-117">[WebDDA](../unified-service-desk/web-dda.md) </span><span class="sxs-lookup"><span data-stu-id="10da0-117">[WebDDA](../unified-service-desk/web-dda.md) </span></span>  
 [<span data-ttu-id="10da0-118">Use Data Driven Adapters (DDAs)</span><span class="sxs-lookup"><span data-stu-id="10da0-118">Use Data Driven Adapters (DDAs)</span></span>](../unified-service-desk/use-data-driven-adapters-ddas.md)
