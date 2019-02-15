---
title: Composite DDA | MicrosoftDocs
description: The composite data-driven adapter is an extension of the DDA architecture introduced with UII. Bộ chuyển đổi được tích hợp để giải quyết vấn đề khi bạn chỉ có thể gán một loại DDA cho một ứng dụng. Trong một số trường hợp, một ứng dụng có thể cần công nghệ khác do DDA khác cung cấp để truy cập chức năng được yêu cầu.
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
ms.assetid: dee27756-e74c-465f-a6b0-383b581e693e
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
ms.openlocfilehash: 4d63924152420f67c023d1d59d76e8031fc23b1b
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388095"
---
# <a name="composite-dda"></a><span data-ttu-id="12915-105">DDA Tổng hợp</span><span class="sxs-lookup"><span data-stu-id="12915-105">Composite DDA</span></span>
<span data-ttu-id="12915-106">Bộ chuyển đổi định hướng dữ liệu tổng hợp là phần mở rộng của kiến trúc DDA được giới thiệu với [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)].</span><span class="sxs-lookup"><span data-stu-id="12915-106">The composite data-driven adapter is an extension of the DDA architecture introduced with [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)].</span></span> <span data-ttu-id="12915-107">Bộ chuyển đổi được tích hợp để giải quyết vấn đề khi bạn chỉ có thể gán một loại DDA cho một ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="12915-107">It was built to address the issue where you can assign only one DDA type to an application.</span></span> <span data-ttu-id="12915-108">Trong một số trường hợp, một ứng dụng có thể cần công nghệ khác do DDA khác cung cấp để truy cập chức năng được yêu cầu.</span><span class="sxs-lookup"><span data-stu-id="12915-108">In some cases, an application might need different technologies provided by different DDAs to access the required functionality.</span></span> <span data-ttu-id="12915-109">Một ví dụ cho điều này có thể là một applet Java trong ứng dụng web.</span><span class="sxs-lookup"><span data-stu-id="12915-109">An example for this could be a Java applet in a web application.</span></span> <span data-ttu-id="12915-110">Bạn có thể sử dụng DDA tổng hợp trong những tình huống.</span><span class="sxs-lookup"><span data-stu-id="12915-110">You can use the composite DDA in these scenarios.</span></span>  
  
## <a name="composite-dda-bindings"></a><span data-ttu-id="12915-111">Liên kết DDA tổng hợp</span><span class="sxs-lookup"><span data-stu-id="12915-111">Composite DDA bindings</span></span>  
 <span data-ttu-id="12915-112">Liên kết DDA tổng hợp tương tự với DDA khác.</span><span class="sxs-lookup"><span data-stu-id="12915-112">The composite DDA bindings are similar to the other DDAs.</span></span> <span data-ttu-id="12915-113">The bindings are simply added to a `<DataDrivenAdapterBindingsCollection>` collection, which supports adding bindings of different types.</span><span class="sxs-lookup"><span data-stu-id="12915-113">The bindings are simply added to a `<DataDrivenAdapterBindingsCollection>` collection, which supports adding bindings of different types.</span></span> <span data-ttu-id="12915-114">Mẫu sau đây hiển thị bộ sưu tập liên kết của ba DDA.</span><span class="sxs-lookup"><span data-stu-id="12915-114">The following sample shows a binding collection of three DDAs.</span></span> <span data-ttu-id="12915-115">Tuy nhiên, bạn chí có thể thêm một bộ sưu tập cho mỗi ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="12915-115">However, you can add only one collection per application.</span></span>  
  
```xml  
<DataDrivenAdapterBindingsCollection>  
   <Type>DDAType1, DDAAssembly</Type>   
   <Controls>  
    …  
   </Controls>  
</DataDrivenAdapterBindings>  
  
<DataDrivenAdapterBindings prefix="dda1">  
   <Type>DDAType2, DDAAssembly</Type>   
   <Controls>  
   …  
   </Controls>  
   </DataDrivenAdapterBindings>  
<DataDrivenAdapterBindings prefix="dda2">  
   <Type>DDAType3, DDAAssembly</Type>   
   <Controls>  
   …  
   </Controls>  
</DataDrivenAdapterBindings>  
</DataDrivenAdapterBindingsCollection>  
  
```  
  
 <span data-ttu-id="12915-116">Mỗi thẻ trong số các thẻ `<DataDrivenAdapterBindings>` có thể có tiền tố tham số tùy chọn.</span><span class="sxs-lookup"><span data-stu-id="12915-116">Each of the `<DataDrivenAdapterBindings>` tags can have an optional parameter prefix.</span></span> <span data-ttu-id="12915-117">Điều này cho phép sử dụng cùng tên kiểm soát tổ chức trong các phần liên kết khác nhau.</span><span class="sxs-lookup"><span data-stu-id="12915-117">This allows using the same control name in different binding sections.</span></span> <span data-ttu-id="12915-118">Nếu tiền tố được xác định, tất cả các kiểm soát trong DDA này sẽ có tiền tố gắn vào tên kiểm soát của chúng.</span><span class="sxs-lookup"><span data-stu-id="12915-118">If prefix is defined, all controls in this DDA will have this prefix attached to their control name.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="12915-119">Mỗi liên kết DDA phải luôn được gọi với tiền tố tương ứng của mình.</span><span class="sxs-lookup"><span data-stu-id="12915-119">Every DDA binding should always be called with its respective prefix.</span></span> <span data-ttu-id="12915-120">Ví dụ: nếu `DDAType2` và `DDAType3` có kiểm soát được chỉ định trong tên `Button1`, kiểm soát tổ chức được sử dụng trong quá trình tự động hóa là `dda1Button1` và `dda2Button1`.</span><span class="sxs-lookup"><span data-stu-id="12915-120">For example, if the `DDAType2` and `DDAType3` have a control defined with the name `Button1`, the control names used in the automation are `dda1Button1` and `dda2Button1`.</span></span>  
> 
> [!NOTE]
>  <span data-ttu-id="12915-121">Nếu trang web chứa kiểm soát [!INCLUDE[pn_ms_ActiveX_short](../includes/pn-ms-activex-short.md)] hoặc Applet [!INCLUDE[pn_Java](../includes/pn-java.md)], hành động mặc định của ứng dụng web không chờ kiểm soát [!INCLUDE[pn_ms_ActiveX_short](../includes/pn-ms-activex-short.md)] hoặc Applet [!INCLUDE[pn_Java](../includes/pn-java.md)] tải.</span><span class="sxs-lookup"><span data-stu-id="12915-121">If the webpage contains a [!INCLUDE[pn_ms_ActiveX_short](../includes/pn-ms-activex-short.md)] control or [!INCLUDE[pn_Java](../includes/pn-java.md)] Applet, the web application default action does not wait for the [!INCLUDE[pn_ms_ActiveX_short](../includes/pn-ms-activex-short.md)] control or [!INCLUDE[pn_Java](../includes/pn-java.md)] Applet to load.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="12915-122">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="12915-122">See also</span></span>  
 [<span data-ttu-id="12915-123">Use Data Driven Adapters</span><span class="sxs-lookup"><span data-stu-id="12915-123">Use Data Driven Adapters</span></span>](../unified-service-desk/use-data-driven-adapters-ddas.md)
