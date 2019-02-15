---
title: JAccTree Tag in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: The topic describes the elements of <JAccTree>.
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
ms.assetid: f1a3a64c-b154-4ccb-82f0-5399745d9a6e
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
ms.openlocfilehash: 91d7c69bf38c22a83f509d7e06cb75d793da96c6
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387404"
---
# <a name="jacctree-tag-in-unified-service-desk"></a><span data-ttu-id="573ea-103">JAccTree Tag in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="573ea-103">JAccTree Tag in Unified Service Desk</span></span>
<span data-ttu-id="573ea-104">`JAccTree` liên kết kiểm soát tổ chức có tên với yếu tố cây khả năng tiếp cận Java được chỉ định trong đường dẫn tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="573ea-104">The `JAccTree` associates a named control to the Java accessibility tree element that is specified in the search path.</span></span> <span data-ttu-id="573ea-105">Chủ đề này mô tả các yếu tố của `<JAccTree>`</span><span class="sxs-lookup"><span data-stu-id="573ea-105">This topic describes the elements of `<JAccTree>`</span></span>  
  
## <a name="jacctree-syntax"></a><span data-ttu-id="573ea-106">\<JAccTree> syntax</span><span class="sxs-lookup"><span data-stu-id="573ea-106">\<JAccTree> syntax</span></span>  
 <span data-ttu-id="573ea-107">Đoạn mã sau hiển thị cú pháp của `<JAccTree>`</span><span class="sxs-lookup"><span data-stu-id="573ea-107">The following code snippet shows the syntax of `<JAccTree>`</span></span>  
  
```xml  
<JAccTree name="control name">  
<Path>  
       ...      
</Path>  
</JAccTree>  
  
```  
  
## <a name="elements-of-jacctree"></a><span data-ttu-id="573ea-108">Elements of \<JAccTree></span><span class="sxs-lookup"><span data-stu-id="573ea-108">Elements of \<JAccTree></span></span>  
 <span data-ttu-id="573ea-109">Bảng sau mô tả các yếu tố của thẻ `<JAccTree>`.</span><span class="sxs-lookup"><span data-stu-id="573ea-109">The following table describes the elements of the `<JAccTree>` tag.</span></span>  
  
|<span data-ttu-id="573ea-110">Yếu tố</span><span class="sxs-lookup"><span data-stu-id="573ea-110">Element</span></span>|<span data-ttu-id="573ea-111">Mô tả</span><span class="sxs-lookup"><span data-stu-id="573ea-111">Description</span></span>|  
|-------------|-----------------|  
|`FindControl`|<span data-ttu-id="573ea-112">Trả về `True` hoặc `False` tùy thuộc vào việc kiểm soát có thể được tìm thấy trên UI hay không.</span><span class="sxs-lookup"><span data-stu-id="573ea-112">Returns `True` or `False` depending on whether the control is found on the UI.</span></span>|  
|`GetControlValue`|<span data-ttu-id="573ea-113">Trả về nội dung của kiểm soát.</span><span class="sxs-lookup"><span data-stu-id="573ea-113">Returns the content of the control.</span></span>|  
|`SetControlValue`|<span data-ttu-id="573ea-114">Đặt nội dung của kiểm soát.</span><span class="sxs-lookup"><span data-stu-id="573ea-114">Sets the content of the control.</span></span>|  
|`ExecuteControlAction`|<span data-ttu-id="573ea-115">Bật tắt trạng thái nút cây – mở rộng hoặc thu hẹp.</span><span class="sxs-lookup"><span data-stu-id="573ea-115">Toggles the tree node state – expands or collapses it.</span></span>|  
  
### <a name="see-also"></a><span data-ttu-id="573ea-116">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="573ea-116">See also</span></span>  
 <span data-ttu-id="573ea-117">[JavaDDA](../unified-service-desk/javadda.md) </span><span class="sxs-lookup"><span data-stu-id="573ea-117">[JavaDDA](../unified-service-desk/javadda.md) </span></span>  
 [<span data-ttu-id="573ea-118">Use Data Driven Adapters (DDAs)</span><span class="sxs-lookup"><span data-stu-id="573ea-118">Use Data Driven Adapters (DDAs)</span></span>](../unified-service-desk/use-data-driven-adapters-ddas.md)
