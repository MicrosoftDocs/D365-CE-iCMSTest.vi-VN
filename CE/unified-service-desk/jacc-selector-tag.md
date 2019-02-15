---
title: JAccSelector Tag in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: The topic describes the elements of <JAccSelector>.
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
ms.assetid: 95bd8843-e924-4709-b4aa-86dbdb985b03
caps.latest.revision: 5
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 65c9788baba17721b2b3bb93468d3fad82106ea6
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386289"
---
# <a name="jaccselector-tag-in-unified-service-desk"></a><span data-ttu-id="40e8b-103">JAccSelector Tag in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="40e8b-103">JAccSelector Tag in Unified Service Desk</span></span>
<span data-ttu-id="40e8b-104">`<JAccSelector>` liên kết kiểm soát có tên với đối tượng khả năng tiếp cận [!INCLUDE[pn_Java](../includes/pn-java.md)] được chỉ định trong đường dẫn tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="40e8b-104">`<JAccSelector>` associates a named control to the [!INCLUDE[pn_Java](../includes/pn-java.md)] accessibility element that is specified in the search path.</span></span> <span data-ttu-id="40e8b-105">Bạn có thể sử dụng loại kiểm soát này cho tất cả yếu tố lựa chọn chẳng hạn như hộp danh sách hoặc danh sách trong hộp kết hợp.</span><span class="sxs-lookup"><span data-stu-id="40e8b-105">You can use this control type for all selection elements such as lists boxes or lists in combo boxes.</span></span> <span data-ttu-id="40e8b-106">Chủ đề này mô tả các yếu tố của `<JAccSelector>`</span><span class="sxs-lookup"><span data-stu-id="40e8b-106">This topic describes the elements of `<JAccSelector>`</span></span>  
  
## <a name="jaccselector-syntax"></a><span data-ttu-id="40e8b-107">\<JAccSelector> syntax</span><span class="sxs-lookup"><span data-stu-id="40e8b-107">\<JAccSelector> syntax</span></span>  
  
```xml  
<JAccSelector name="control name">  
<Path>  
...      
</Path>  
</JAccSelector>  
  
```  
  
## <a name="elements-of-jaccselector"></a><span data-ttu-id="40e8b-108">Elements of \<JAccSelector></span><span class="sxs-lookup"><span data-stu-id="40e8b-108">Elements of \<JAccSelector></span></span>  
 <span data-ttu-id="40e8b-109">Bảng sau mô tả các yếu tố của thẻ `<JAccSelector>`:</span><span class="sxs-lookup"><span data-stu-id="40e8b-109">The following table describes the elements of the `<JAccSelector>` tag:</span></span>  
  
|<span data-ttu-id="40e8b-110">Yếu tố</span><span class="sxs-lookup"><span data-stu-id="40e8b-110">Element</span></span>|<span data-ttu-id="40e8b-111">Mô tả</span><span class="sxs-lookup"><span data-stu-id="40e8b-111">Description</span></span>|  
|-------------|-----------------|  
|`FindControl`|<span data-ttu-id="40e8b-112">Trả về `True` hoặc `False` tùy thuộc vào việc kiểm soát có thể được tìm thấy trên UI hay không.</span><span class="sxs-lookup"><span data-stu-id="40e8b-112">Returns `True` or `False` depending on whether the control is found on the UI.</span></span>|  
|`GetControlValue`|<span data-ttu-id="40e8b-113">Trả về tên của (các) mục đã chọn; nhiều mục được phân cách bằng dấu phẩy.</span><span class="sxs-lookup"><span data-stu-id="40e8b-113">Returns the name of the selected item(s); multiple items are separated by comma.</span></span>|  
|`SetControlValue`|<span data-ttu-id="40e8b-114">Đặt lựa chọn trong danh sách; nhiều mục được phân cách bằng dấu phẩy.</span><span class="sxs-lookup"><span data-stu-id="40e8b-114">Sets the selection in the list; multiple items are separated by comma.</span></span>|  
|`ExecuteControlAction`|<span data-ttu-id="40e8b-115">Bật tắt lựa chọn hiện thời.</span><span class="sxs-lookup"><span data-stu-id="40e8b-115">Toggles the current selection.</span></span>|  
  
> [!NOTE]
>  <span data-ttu-id="40e8b-116">Một số hộp tổ hợp được thiết lập để có thể chỉnh sửa, cho phép người dùng nhập văn bản bất kỳ vào trường đầu vào.</span><span class="sxs-lookup"><span data-stu-id="40e8b-116">Some combo boxes are set to editable, which enables user to enter any text in the input field.</span></span> <span data-ttu-id="40e8b-117">For such combo boxes, you must use the `<JAccControl>` tag in the bindings for the input box to set the value.</span><span class="sxs-lookup"><span data-stu-id="40e8b-117">For such combo boxes, you must use the `<JAccControl>` tag in the bindings for the input box to set the value.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="40e8b-118">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="40e8b-118">See also</span></span>  
 <span data-ttu-id="40e8b-119">[JavaDDA](../unified-service-desk/javadda.md) </span><span class="sxs-lookup"><span data-stu-id="40e8b-119">[JavaDDA](../unified-service-desk/javadda.md) </span></span>  
 [<span data-ttu-id="40e8b-120">Use Data Driven Adapters (DDAs)</span><span class="sxs-lookup"><span data-stu-id="40e8b-120">Use Data Driven Adapters (DDAs)</span></span>](../unified-service-desk/use-data-driven-adapters-ddas.md)
