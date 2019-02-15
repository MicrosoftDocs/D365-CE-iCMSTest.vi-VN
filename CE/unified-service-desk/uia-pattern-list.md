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
# <a name="uia-pattern-list-in-unified-service-desk"></a><span data-ttu-id="ede8f-103">UIA Pattern List in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="ede8f-103">UIA Pattern List in Unified Service Desk</span></span>
<span data-ttu-id="ede8f-104">Chủ đề này liệt kê các mẫu UIA.</span><span class="sxs-lookup"><span data-stu-id="ede8f-104">This topic lists the UIA patterns.</span></span>  
  
1. [<span data-ttu-id="ede8f-105">InvokePatternIdentifiers.Pattern</span><span class="sxs-lookup"><span data-stu-id="ede8f-105">InvokePatternIdentifiers.Pattern</span></span>](https://msdn.microsoft.com/library/vstudio/system.windows.automation.invokepatternidentifiers.pattern.aspx)  
  
2. [<span data-ttu-id="ede8f-106">TogglePatternIdentifiers.Pattern</span><span class="sxs-lookup"><span data-stu-id="ede8f-106">TogglePatternIdentifiers.Pattern</span></span>](https://msdn.microsoft.com/library/vstudio/system.windows.automation.transformpatternidentifiers.pattern.aspx)  
  
3. [<span data-ttu-id="ede8f-107">ExpandCollapsePatternIdentifiers.Pattern</span><span class="sxs-lookup"><span data-stu-id="ede8f-107">ExpandCollapsePatternIdentifiers.Pattern</span></span>](https://msdn.microsoft.com/library/vstudio/system.windows.automation.expandcollapsepatternidentifiers.pattern.aspx)  
  
4. [<span data-ttu-id="ede8f-108">SelectionItemPatternIdentifiers.Pattern</span><span class="sxs-lookup"><span data-stu-id="ede8f-108">SelectionItemPatternIdentifiers.Pattern</span></span>](https://msdn.microsoft.com/library/vstudio/system.windows.automation.selectionitempatternidentifiers.pattern.aspx)  
  
5. [<span data-ttu-id="ede8f-109">TextPatternIdentifiers.Pattern</span><span class="sxs-lookup"><span data-stu-id="ede8f-109">TextPatternIdentifiers.Pattern</span></span>](https://msdn.microsoft.com/library/vstudio/system.windows.automation.tablepatternidentifiers.pattern.aspx)  
  
6. [<span data-ttu-id="ede8f-110">ScrollPatternIdentifiers.Pattern</span><span class="sxs-lookup"><span data-stu-id="ede8f-110">ScrollPatternIdentifiers.Pattern</span></span>](https://msdn.microsoft.com/library/vstudio/system.windows.automation.scrollpatternidentifiers.pattern.aspx)  
  
7. [<span data-ttu-id="ede8f-111">RangeValuePatternIdentifiers.Pattern</span><span class="sxs-lookup"><span data-stu-id="ede8f-111">RangeValuePatternIdentifiers.Pattern</span></span>](https://msdn.microsoft.com/library/vstudio/system.windows.automation.rangevaluepatternidentifiers.pattern.aspx)  
  
8. [<span data-ttu-id="ede8f-112">TogglePatternIdentifiers.Pattern</span><span class="sxs-lookup"><span data-stu-id="ede8f-112">TogglePatternIdentifiers.Pattern</span></span>](https://msdn.microsoft.com/library/vstudio/system.windows.automation.transformpatternidentifiers.pattern.aspx)  
  
9. [<span data-ttu-id="ede8f-113">ValuePatternIdentifiers.Pattern</span><span class="sxs-lookup"><span data-stu-id="ede8f-113">ValuePatternIdentifiers.Pattern</span></span>](https://msdn.microsoft.com/library/vstudio/system.windows.automation.valuepatternidentifiers.pattern.aspx)  
  
   <span data-ttu-id="ede8f-114">DDA có thể được mở rộng để thêm mẫu mới.</span><span class="sxs-lookup"><span data-stu-id="ede8f-114">DDA can be extended to add a new pattern.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="ede8f-115">Khi UIADDA được sử dụng với ứng dụng bất kỳ, UIA yêu cầu ứng dụng phải được tập trung trước khi xảy ra bất kỳ tương tác nào với ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="ede8f-115">When UIADDA is used with any application, UIA requires that the application be in focus before any interaction can occur with the application.</span></span> <span data-ttu-id="ede8f-116">Điều này nghĩa là quá trình tự động hóa bất kỳ sẽ yêu cầu hoạt động Tiêu điểm xuất hiện trước khi diễn ra bất kỳ tương tác nào với các kiểm soát, bao gồm đăng ký một sự kiện.</span><span class="sxs-lookup"><span data-stu-id="ede8f-116">This means that any automation will require that a Focus activity occur before any interaction with controls can take place, including registering for an event.</span></span> <span data-ttu-id="ede8f-117">Nếu có tương tác kế tiếp với các kiểm soát trên ứng dụng khác, ứng dụng đó phải được đưa vào tiêu điểm.</span><span class="sxs-lookup"><span data-stu-id="ede8f-117">If there is subsequent interaction with controls on another application, that application must be brought into focus.</span></span>  <span data-ttu-id="ede8f-118">`Dynamic positioning` phải được sử dụng thay vì `set parent` khi sử dụng UIADDA với các ứng dụng không phải là WPF.</span><span class="sxs-lookup"><span data-stu-id="ede8f-118">`Dynamic positioning` must be used instead of `set parent` when using the UIADDA with non-WPF applications.</span></span>  <span data-ttu-id="ede8f-119">Nếu một ứng dụng được lưu trữ bên ngoài, sẽ không cần tiêu điểm.</span><span class="sxs-lookup"><span data-stu-id="ede8f-119">If an application is hosted outside, focus is not required.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="ede8f-120">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="ede8f-120">See also</span></span>  
 <span data-ttu-id="ede8f-121">[UIADDA](../unified-service-desk/uiadda.md) </span><span class="sxs-lookup"><span data-stu-id="ede8f-121">[UIADDA](../unified-service-desk/uiadda.md) </span></span>  
 [<span data-ttu-id="ede8f-122">Use Data Driven Adapters (DDAs)</span><span class="sxs-lookup"><span data-stu-id="ede8f-122">Use Data Driven Adapters (DDAs)</span></span>](../unified-service-desk/use-data-driven-adapters-ddas.md)
