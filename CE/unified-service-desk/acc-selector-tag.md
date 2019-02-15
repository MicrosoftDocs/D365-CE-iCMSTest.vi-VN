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
# <a name="accselector-tag"></a>Thẻ ACCSelector
Thẻ `AccSelector` sử dụng giao diện [IAccessible](https://msdn.microsoft.com/library/accessibility.iaccessible\(v=vs.110\).aspx) từ Microsoft Active Accessibility (MSAA) để truy cập các kiểm soát cho phép nhiều lựa chọn, chẳng hạn như hộp danh sách hoặc hộp combo. Thẻ này có một thuộc tính tên xác định tên (thân thiện) mà người dùng có thể truy cập cho một kiểm soát. The [GetControlValue](https://docs.microsoft.com/dotnet/api/microsoft.uii.hostedapplicationtoolkit.datadrivenadapter.operationtype.getcontrolvalue) on an `AccSelector` returns the value of the selected item.  
  
### <a name="see-also"></a>Xem thêm  
 [Win DDA](../unified-service-desk/windda.md)   
 [Use Data Driven Adapters (DDAs)](../unified-service-desk/use-data-driven-adapters-ddas.md)
