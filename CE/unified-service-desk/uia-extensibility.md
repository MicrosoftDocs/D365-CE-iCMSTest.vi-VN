---
title: UIA Extensibility in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn about UIA extensibility in Unified Service Desk.
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
ms.assetid: 7a2c950b-36e6-48ef-8990-2725219255ed
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
ms.openlocfilehash: 4a308b370ddba641f3046018d1bb4446b66e0562
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385853"
---
# <a name="uia-extensibility-in-unified-service-desk"></a><span data-ttu-id="a8047-103">UIA Extensibility in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="a8047-103">UIA Extensibility in Unified Service Desk</span></span>
<span data-ttu-id="a8047-104">Bạn có thể thêm đối số `data` vào từng phương pháp DDA khác nhau `OperationHandler` để cho phép khả năng mở rộng UIA.</span><span class="sxs-lookup"><span data-stu-id="a8047-104">A `data` argument can be added to each of the different DDA `OperationHandler` methods to enable UIA extensibility.</span></span> <span data-ttu-id="a8047-105">Bạn có thể sử dụng tham số này để mở rộng DDA khi cần.</span><span class="sxs-lookup"><span data-stu-id="a8047-105">You can use this parameter to extend the DDA as needed.</span></span> <span data-ttu-id="a8047-106">Theo mặc định, nếu tham số này là null, các phương pháp DDA khác nhau sẽ theo dõi hành vi mặc định.</span><span class="sxs-lookup"><span data-stu-id="a8047-106">By default, if this parameter is null, the different methods of the DDA will follow the default behavior.</span></span> <span data-ttu-id="a8047-107">Bạn có thể đặt nội dung của tham số này cho một đối tượng.</span><span class="sxs-lookup"><span data-stu-id="a8047-107">You should be able to set the content of this parameter to an object.</span></span> <span data-ttu-id="a8047-108">Chủ đề này mô tả cách mở rộng UIA bằng tham số `data`.</span><span class="sxs-lookup"><span data-stu-id="a8047-108">This topic describes how to extend UIA using the `data` parameter.</span></span>  
  
 <span data-ttu-id="a8047-109">Đối với mỗi hoạt động sau, phương pháp `Execute` của hoạt động tương ứng sẽ xây dựng đối tượng dữ liệu để được chuyển tới phương pháp `OperationHandler` của DDA.</span><span class="sxs-lookup"><span data-stu-id="a8047-109">For each of the following activities, the `Execute` method of the corresponding activity builds the data object to be passed to the `OperationHandler` method of the DDA.</span></span> <span data-ttu-id="a8047-110">Tham số `Data` được bao gồm trong các hoạt động sau:</span><span class="sxs-lookup"><span data-stu-id="a8047-110">A `Data` parameter is included in the following activities:</span></span>  
  
- <span data-ttu-id="a8047-111">`GetControlValue`: **"Desired Pattern to use/Desired Property name to retrieve"** can be passed to the data parameter to retrieve the specified property.</span><span class="sxs-lookup"><span data-stu-id="a8047-111">`GetControlValue`: **"Desired Pattern to use/Desired Property name to retrieve"** can be passed to the data parameter to retrieve the specified property.</span></span> <span data-ttu-id="a8047-112">The property can be any one from the [UIA property list](../unified-service-desk/uia-property-list.md).</span><span class="sxs-lookup"><span data-stu-id="a8047-112">The property can be any one from the [UIA property list](../unified-service-desk/uia-property-list.md).</span></span>  <span data-ttu-id="a8047-113">`ControlProperty` – Chỉ định thuộc tính mà DDA nên truy xuất.</span><span class="sxs-lookup"><span data-stu-id="a8047-113">`ControlProperty` – Specifies which property the DDA should be retrieving.</span></span>  
  
- <span data-ttu-id="a8047-114">`SetControlValue`: **"Desired pattern Name" (Desired Pattern to use)** shall be passed to the data parameter to perform the pattern selection.</span><span class="sxs-lookup"><span data-stu-id="a8047-114">`SetControlValue`: **"Desired pattern Name" (Desired Pattern to use)** shall be passed to the data parameter to perform the pattern selection.</span></span> <span data-ttu-id="a8047-115">The pattern can be any one from the [UIA Pattern List](../unified-service-desk/uia-pattern-list.md).</span><span class="sxs-lookup"><span data-stu-id="a8047-115">The pattern can be any one from the [UIA Pattern List](../unified-service-desk/uia-pattern-list.md).</span></span>  <span data-ttu-id="a8047-116">`ControlProperty` – Chỉ định thuộc tính mà DDA nên gán.</span><span class="sxs-lookup"><span data-stu-id="a8047-116">`ControlProperty` – Specifies which property the DDA should be assigning.</span></span>  
  
- <span data-ttu-id="a8047-117">`ExecuteControlValue`: **"Desired pattern Name" (Desired Pattern to use)** shall be passed to the data parameter to perform the pattern execution.</span><span class="sxs-lookup"><span data-stu-id="a8047-117">`ExecuteControlValue`: **"Desired pattern Name" (Desired Pattern to use)** shall be passed to the data parameter to perform the pattern execution.</span></span> <span data-ttu-id="a8047-118">The pattern can be any one from the [UIA Pattern List](../unified-service-desk/uia-pattern-list.md) later in this section.</span><span class="sxs-lookup"><span data-stu-id="a8047-118">The pattern can be any one from the [UIA Pattern List](../unified-service-desk/uia-pattern-list.md) later in this section.</span></span>  
  
- <span data-ttu-id="a8047-119">`RegisterActionForEvent`: **"For PropertyChangedEvent"** (data property) can be used to specify the property on which the event will be triggered.</span><span class="sxs-lookup"><span data-stu-id="a8047-119">`RegisterActionForEvent`: **"For PropertyChangedEvent"** (data property) can be used to specify the property on which the event will be triggered.</span></span> <span data-ttu-id="a8047-120">The property can be any one from the [UIA property list](../unified-service-desk/uia-property-list.md) later in this section.</span><span class="sxs-lookup"><span data-stu-id="a8047-120">The property can be any one from the [UIA property list](../unified-service-desk/uia-property-list.md) later in this section.</span></span>  
  
  <span data-ttu-id="a8047-121">Điều này được sử dụng để chuyển bất kỳ dữ liệu nào từ hoạt động của quy trình làm việc đến bộ chuyển đổi.</span><span class="sxs-lookup"><span data-stu-id="a8047-121">This is used to pass any data from workflow activity to the adapter.</span></span> <span data-ttu-id="a8047-122">Dữ liệu này có thể được DDA sử dụng hoặc bằng cách mở rộng DDA.</span><span class="sxs-lookup"><span data-stu-id="a8047-122">This data can be consumed by the DDA or by extending the DDA.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="a8047-123">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="a8047-123">See also</span></span>  
 <span data-ttu-id="a8047-124">[UIADDA](../unified-service-desk/uiadda.md) </span><span class="sxs-lookup"><span data-stu-id="a8047-124">[UIADDA](../unified-service-desk/uiadda.md) </span></span>  
 [<span data-ttu-id="a8047-125">Use Data Driven Adapters (DDAs)</span><span class="sxs-lookup"><span data-stu-id="a8047-125">Use Data Driven Adapters (DDAs)</span></span>](../unified-service-desk/use-data-driven-adapters-ddas.md)
