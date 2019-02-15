---
title: AccControl Tag | MicrosoftDocs
description: Learn about the AccControl tag that uses the IAccessible interface from Microsoft Active Accessibility (MSAA).
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
ms.assetid: e4d9d212-1709-4983-8d57-9359cda932fd
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
ms.openlocfilehash: ceb972e7f2876882cd2486f0fb1bcf970bda1520
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388441"
---
# <a name="acccontrol-tag"></a><span data-ttu-id="931b9-103">Thẻ AccControl</span><span class="sxs-lookup"><span data-stu-id="931b9-103">AccControl Tag</span></span>
<span data-ttu-id="931b9-104">Thẻ `AccControl` sử dụng giao diện [IAccessible](https://msdn.microsoft.com/library/accessibility.iaccessible\(v=vs.110\).aspx) từ Microsoft Active Accessibility (MSAA).</span><span class="sxs-lookup"><span data-stu-id="931b9-104">The `AccControl` tag uses the [IAccessible](https://msdn.microsoft.com/library/accessibility.iaccessible\(v=vs.110\).aspx) interface from Microsoft Active Accessibility (MSAA).</span></span> <span data-ttu-id="931b9-105">Thẻ AccControl có:</span><span class="sxs-lookup"><span data-stu-id="931b9-105">The AccControl tag has:</span></span>  
  
- <span data-ttu-id="931b9-106">Thuộc tính `Name` để xác định tên thân thiện với người dùng cho một kiểm soát.</span><span class="sxs-lookup"><span data-stu-id="931b9-106">`Name` property to define the user-accessible (friendly) name for a control.</span></span>  
  
- <span data-ttu-id="931b9-107">Thẻ `Path` xác định đường dẫn tìm kiếm cho kiểm soát trong cây `IAccessibility` của ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="931b9-107">`Path` tag to define a search path for the control in the application's `IAccessibility` tree.</span></span> <span data-ttu-id="931b9-108">The `<Path>` tag contains the following: [FindWindow Tag](../unified-service-desk/find-window-tag.md) and [Next Tag](../unified-service-desk/next-tag-windda.md).</span><span class="sxs-lookup"><span data-stu-id="931b9-108">The `<Path>` tag contains the following: [FindWindow Tag](../unified-service-desk/find-window-tag.md) and [Next Tag](../unified-service-desk/next-tag-windda.md).</span></span>  
  
  <span data-ttu-id="931b9-109">The following XML example shows a control definition using the `AccControl` tag.</span><span class="sxs-lookup"><span data-stu-id="931b9-109">The following XML example shows a control definition using the `AccControl` tag.</span></span>  
  
```xml  
<AccControl name="Control Name">  
   <Path>   
      <FindWindow>  
         <CaptionStartsWith>Customer App</CaptionStartsWith>  
      </FindWindow>  
      <Next/>  
      <Next match="2">Customer Name:</Next>  
   </Path>  
</AccControl>  
```  
  
> [!NOTE]
>  <span data-ttu-id="931b9-110">Một số yếu tố trong thẻ `Path` có thuộc tính `<match>` mà bạn có thể sử dụng để thêm bộ đếm vào mô tả tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="931b9-110">Some elements in the `Path` tag have a `<match>` attribute that you can use to add a counter to the search description.</span></span> <span data-ttu-id="931b9-111">Both the following examples return the same search result, but the first example implements the `<match>` tag:</span><span class="sxs-lookup"><span data-stu-id="931b9-111">Both the following examples return the same search result, but the first example implements the `<match>` tag:</span></span>  
> 
> - <span data-ttu-id="931b9-112">**Ví dụ 1**</span><span class="sxs-lookup"><span data-stu-id="931b9-112">**Example 1**</span></span>  
> 
>    ```  
>    <Caption match="2">Test Application</Caption>  
>    ```  
>   - <span data-ttu-id="931b9-113">Ví dụ 2:</span><span class="sxs-lookup"><span data-stu-id="931b9-113">Example 2:</span></span>  
> 
>     ```  
>     <Caption>Test Application</Caption>  
>     <Caption>Test Application</Caption>  
>     ```  
> 
>   <span data-ttu-id="931b9-114">Nếu `<match>` không được chỉ định, giá trị mặc định là 0.</span><span class="sxs-lookup"><span data-stu-id="931b9-114">If `<match>` isn’t specified, the default value is 0.</span></span>  
  
 <span data-ttu-id="931b9-115">The [String)](https://docs.microsoft.com/dotnet/api/microsoft.uii.hostedapplicationtoolkit.datadrivenadapter.datadrivenadapterbase.getcontrolvalue\(system.string,system.string\)) method on an `AccControl` tag is always mapped to the `get_accValue` method on the subject `IAccessible` node, unless the node contains `role="radio button"` or `role="check box"`.</span><span class="sxs-lookup"><span data-stu-id="931b9-115">The [String)](https://docs.microsoft.com/dotnet/api/microsoft.uii.hostedapplicationtoolkit.datadrivenadapter.datadrivenadapterbase.getcontrolvalue\(system.string,system.string\)) method on an `AccControl` tag is always mapped to the `get_accValue` method on the subject `IAccessible` node, unless the node contains `role="radio button"` or `role="check box"`.</span></span> <span data-ttu-id="931b9-116">In these cases, the [String)](https://docs.microsoft.com/dotnet/api/microsoft.uii.hostedapplicationtoolkit.datadrivenadapter.datadrivenadapterbase.getcontrolvalue\(system.string,system.string\)) method returns `True` or `False`, depending on whether the state of the node is selected.</span><span class="sxs-lookup"><span data-stu-id="931b9-116">In these cases, the [String)](https://docs.microsoft.com/dotnet/api/microsoft.uii.hostedapplicationtoolkit.datadrivenadapter.datadrivenadapterbase.getcontrolvalue\(system.string,system.string\)) method returns `True` or `False`, depending on whether the state of the node is selected.</span></span>  
  
 <span data-ttu-id="931b9-117">The [String)](https://docs.microsoft.com/dotnet/api/microsoft.uii.hostedapplicationtoolkit.datadrivenadapter.datadrivenadapterbase.setcontrolvalue\(system.string,system.string,system.string\)) method on an `AccControl` tag is always mapped to the `set_accValue` method on the subject `IAccessible` node, with the exception of nodes that have `role="radio button"` or `role="check box"`.</span><span class="sxs-lookup"><span data-stu-id="931b9-117">The [String)](https://docs.microsoft.com/dotnet/api/microsoft.uii.hostedapplicationtoolkit.datadrivenadapter.datadrivenadapterbase.setcontrolvalue\(system.string,system.string,system.string\)) method on an `AccControl` tag is always mapped to the `set_accValue` method on the subject `IAccessible` node, with the exception of nodes that have `role="radio button"` or `role="check box"`.</span></span> <span data-ttu-id="931b9-118">Trong trường hợp nút radio, ngoại lệ `UnsupportedControlOperation` được đưa ra vì nút radio không thể được gán giá trị `True` hoặc `False`.</span><span class="sxs-lookup"><span data-stu-id="931b9-118">In the case of a radio button, an `UnsupportedControlOperation` exception is raised because a radio button can’t be assigned a `True` or `False` value.</span></span>  
  
 <span data-ttu-id="931b9-119">The following example displays the [RELAX NG](http://relaxng.org/compact-tutorial-20030326.html) XML code for the \<Path> tag.</span><span class="sxs-lookup"><span data-stu-id="931b9-119">The following example displays the [RELAX NG](http://relaxng.org/compact-tutorial-20030326.html) XML code for the \<Path> tag.</span></span>  
  
```xml  
# RELAX NG XML grammar for Path  
# http://relaxng.org/compact-tutorial-20030326.html  
#  
grammar   
{  
   start = Path  
   Path = element Path   
   {   
      FindWindow* & element Next   
      { attribute match { xsd:integer }?  
      ,attribute offset { xsd:integer  }?,text? }*   
   }  
}  
```  
  
### <a name="see-also"></a><span data-ttu-id="931b9-120">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="931b9-120">See also</span></span>  
 <span data-ttu-id="931b9-121">[Win DDA](../unified-service-desk/windda.md) </span><span class="sxs-lookup"><span data-stu-id="931b9-121">[Win DDA](../unified-service-desk/windda.md) </span></span>  
 [<span data-ttu-id="931b9-122">Use Data Driven Adapters (DDAs)</span><span class="sxs-lookup"><span data-stu-id="931b9-122">Use Data Driven Adapters (DDAs)</span></span>](../unified-service-desk/use-data-driven-adapters-ddas.md)
