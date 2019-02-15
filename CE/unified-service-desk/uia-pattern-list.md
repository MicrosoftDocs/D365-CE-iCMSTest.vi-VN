---
title: UIA Pattern List in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn about UIA patterns in Unified Service Desk.
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
ms.assetid: a07d78ff-f017-4538-bede-fe722975f434
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
ms.openlocfilehash: e100ae7bf23e161016b38ecab21422f5d6c8c796
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387083"
---
# <a name="uia-pattern-list-in-unified-service-desk"></a>UIA Pattern List in Unified Service Desk
Chủ đề này liệt kê các mẫu UIA.  
  
1. [InvokePatternIdentifiers.Pattern](https://msdn.microsoft.com/library/vstudio/system.windows.automation.invokepatternidentifiers.pattern.aspx)  
  
2. [TogglePatternIdentifiers.Pattern](https://msdn.microsoft.com/library/vstudio/system.windows.automation.transformpatternidentifiers.pattern.aspx)  
  
3. [ExpandCollapsePatternIdentifiers.Pattern](https://msdn.microsoft.com/library/vstudio/system.windows.automation.expandcollapsepatternidentifiers.pattern.aspx)  
  
4. [SelectionItemPatternIdentifiers.Pattern](https://msdn.microsoft.com/library/vstudio/system.windows.automation.selectionitempatternidentifiers.pattern.aspx)  
  
5. [TextPatternIdentifiers.Pattern](https://msdn.microsoft.com/library/vstudio/system.windows.automation.tablepatternidentifiers.pattern.aspx)  
  
6. [ScrollPatternIdentifiers.Pattern](https://msdn.microsoft.com/library/vstudio/system.windows.automation.scrollpatternidentifiers.pattern.aspx)  
  
7. [RangeValuePatternIdentifiers.Pattern](https://msdn.microsoft.com/library/vstudio/system.windows.automation.rangevaluepatternidentifiers.pattern.aspx)  
  
8. [TogglePatternIdentifiers.Pattern](https://msdn.microsoft.com/library/vstudio/system.windows.automation.transformpatternidentifiers.pattern.aspx)  
  
9. [ValuePatternIdentifiers.Pattern](https://msdn.microsoft.com/library/vstudio/system.windows.automation.valuepatternidentifiers.pattern.aspx)  
  
   DDA có thể được mở rộng để thêm mẫu mới.  
  
> [!NOTE]
>  Khi UIADDA được sử dụng với ứng dụng bất kỳ, UIA yêu cầu ứng dụng phải được tập trung trước khi xảy ra bất kỳ tương tác nào với ứng dụng. Điều này nghĩa là quá trình tự động hóa bất kỳ sẽ yêu cầu hoạt động Tiêu điểm xuất hiện trước khi diễn ra bất kỳ tương tác nào với các kiểm soát, bao gồm đăng ký một sự kiện. Nếu có tương tác kế tiếp với các kiểm soát trên ứng dụng khác, ứng dụng đó phải được đưa vào tiêu điểm.  `Dynamic positioning` phải được sử dụng thay vì `set parent` khi sử dụng UIADDA với các ứng dụng không phải là WPF.  Nếu một ứng dụng được lưu trữ bên ngoài, sẽ không cần tiêu điểm.  
  
### <a name="see-also"></a>Xem thêm  
 [UIADDA](../unified-service-desk/uiadda.md)   
 [Use Data Driven Adapters (DDAs)](../unified-service-desk/use-data-driven-adapters-ddas.md)
