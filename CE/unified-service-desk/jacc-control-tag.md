---
title: JAccControl Tag in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: <JAccControl> liên kết kiểm soát tổ chức có tên với yếu tố khả năng kiểm soát Java được chỉ định trong đường dẫn tìm kiếm. Chủ đề này mô tả các yếu tố của thẻ <AccControl>.
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
ms.assetid: e6b76e86-3b62-4e34-9d3e-03abf30bad4f
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
ms.openlocfilehash: 41d58e919853b33c65ad829b5fe3a0a0aad22702
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385756"
---
# <a name="jacccontrol-tag-in-unified-service-desk"></a><span data-ttu-id="00a5c-104">JAccControl Tag in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="00a5c-104">JAccControl Tag in Unified Service Desk</span></span>
<span data-ttu-id="00a5c-105">`<JAccControl>` liên kết kiểm soát tổ chức có tên với yếu tố khả năng kiểm soát Java được chỉ định trong đường dẫn tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="00a5c-105">`<JAccControl>` associates a named control to the Java accessibility element that is specified in the search path.</span></span> <span data-ttu-id="00a5c-106">Chủ đề này mô tả các yếu tố của thẻ `<AccControl>`.</span><span class="sxs-lookup"><span data-stu-id="00a5c-106">This topic describes the elements of `<AccControl>` tag.</span></span>  
  
## <a name="jacccontrol-syntax"></a><span data-ttu-id="00a5c-107">\<JAccControl> syntax</span><span class="sxs-lookup"><span data-stu-id="00a5c-107">\<JAccControl> syntax</span></span>  
 <span data-ttu-id="00a5c-108">Đoạn mã sau hiển thị cách sử dụng thẻ `<JAccControl>`:</span><span class="sxs-lookup"><span data-stu-id="00a5c-108">The following code snippet shows how `<JAccControl>` tag is used:</span></span>  
  
```xml  
<JAccControl name="control name">  
<Path>  
...      
</Path>  
</JAccControl>  
  
```  
  
## <a name="elements-of-jacccontrol"></a><span data-ttu-id="00a5c-109">Elements of \<JAccControl></span><span class="sxs-lookup"><span data-stu-id="00a5c-109">Elements of \<JAccControl></span></span>  
 <span data-ttu-id="00a5c-110">Bảng sau mô tả các yếu tố của thẻ `<JAccControl>`.</span><span class="sxs-lookup"><span data-stu-id="00a5c-110">The following table describes the elements of the `<JAccControl>` tag.</span></span>  
  
|<span data-ttu-id="00a5c-111">Yếu tố</span><span class="sxs-lookup"><span data-stu-id="00a5c-111">Element</span></span>|<span data-ttu-id="00a5c-112">Mô tả</span><span class="sxs-lookup"><span data-stu-id="00a5c-112">Description</span></span>|  
|-------------|-----------------|  
|`FindControl`|<span data-ttu-id="00a5c-113">Trả về `True` nếu kiểm soát được tìm thấy trên UI, nếu không sẽ trả lại **False**.</span><span class="sxs-lookup"><span data-stu-id="00a5c-113">Returns `True` if the control is found on the UI, otherwise **False**.</span></span>|  
|`GetControlValue`|<span data-ttu-id="00a5c-114">Trả về nội dung của kiểm soát.</span><span class="sxs-lookup"><span data-stu-id="00a5c-114">Returns the content of the control.</span></span>|  
|`SetControlValue`|<span data-ttu-id="00a5c-115">Đặt nội dung của kiểm soát, một số kiểm soát không thể thay đổi nội dung của chúng.</span><span class="sxs-lookup"><span data-stu-id="00a5c-115">Sets the content of the control; some controls might not be able to change their content.</span></span>|  
|`ExecuteControlAction`|<span data-ttu-id="00a5c-116">Thực hiện lệnh mặc định cho kiểm soát này, tùy thuộc vào việc tích hợp khả năng tiếp cận Java.</span><span class="sxs-lookup"><span data-stu-id="00a5c-116">Executes the default command for this control, depending on the Java accessibility integration.</span></span>|  
  
> [!NOTE]
>  <span data-ttu-id="00a5c-117">Sử dụng loại kiểm soát này cho tất cả các yếu tố không phải là cây hoặc yếu tố lựa chọn, chẳng hạn danh sách.</span><span class="sxs-lookup"><span data-stu-id="00a5c-117">Use this control type for all elements that are not a tree or a selection element, such as a list.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="00a5c-118">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="00a5c-118">See also</span></span>  
 <span data-ttu-id="00a5c-119">[JavaDDA](../unified-service-desk/javadda.md) </span><span class="sxs-lookup"><span data-stu-id="00a5c-119">[JavaDDA](../unified-service-desk/javadda.md) </span></span>  
 [<span data-ttu-id="00a5c-120">Use Data Driven Adapters (DDAs)</span><span class="sxs-lookup"><span data-stu-id="00a5c-120">Use Data Driven Adapters (DDAs)</span></span>](../unified-service-desk/use-data-driven-adapters-ddas.md)
