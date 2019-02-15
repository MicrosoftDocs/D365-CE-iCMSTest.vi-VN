---
title: ACCSelector Tag | MicrosoftDocs
description: Learn about the AccSelector tag uses the IAccessible interface from Microsoft Active Accessibility (MSAA) to access controls that allow multiple selections, such as in a list box or combo box.
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
ms.assetid: 1dad1353-6b70-42b9-95b6-3893bb022bad
caps.latest.revision: 8
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 6420730e2266d6a868229a20b716406491528ec3
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387791"
---
# <a name="accselector-tag"></a><span data-ttu-id="0e68c-103">Thẻ ACCSelector</span><span class="sxs-lookup"><span data-stu-id="0e68c-103">ACCSelector Tag</span></span>
<span data-ttu-id="0e68c-104">Thẻ `AccSelector` sử dụng giao diện [IAccessible](https://msdn.microsoft.com/library/accessibility.iaccessible\(v=vs.110\).aspx) từ Microsoft Active Accessibility (MSAA) để truy cập các kiểm soát cho phép nhiều lựa chọn, chẳng hạn như hộp danh sách hoặc hộp combo.</span><span class="sxs-lookup"><span data-stu-id="0e68c-104">The `AccSelector` tag uses the [IAccessible](https://msdn.microsoft.com/library/accessibility.iaccessible\(v=vs.110\).aspx) interface from Microsoft Active Accessibility (MSAA) to access controls that allow multiple selections, such as in a list box or combo box.</span></span> <span data-ttu-id="0e68c-105">Thẻ này có một thuộc tính tên xác định tên (thân thiện) mà người dùng có thể truy cập cho một kiểm soát.</span><span class="sxs-lookup"><span data-stu-id="0e68c-105">The tag has a name property to define the user-accessible (friendly) name for a control.</span></span> <span data-ttu-id="0e68c-106">The [GetControlValue](https://docs.microsoft.com/dotnet/api/microsoft.uii.hostedapplicationtoolkit.datadrivenadapter.operationtype.getcontrolvalue) on an `AccSelector` returns the value of the selected item.</span><span class="sxs-lookup"><span data-stu-id="0e68c-106">The [GetControlValue](https://docs.microsoft.com/dotnet/api/microsoft.uii.hostedapplicationtoolkit.datadrivenadapter.operationtype.getcontrolvalue) on an `AccSelector` returns the value of the selected item.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="0e68c-107">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="0e68c-107">See also</span></span>  
 <span data-ttu-id="0e68c-108">[Win DDA](../unified-service-desk/windda.md) </span><span class="sxs-lookup"><span data-stu-id="0e68c-108">[Win DDA](../unified-service-desk/windda.md) </span></span>  
 [<span data-ttu-id="0e68c-109">Use Data Driven Adapters (DDAs)</span><span class="sxs-lookup"><span data-stu-id="0e68c-109">Use Data Driven Adapters (DDAs)</span></span>](../unified-service-desk/use-data-driven-adapters-ddas.md)
