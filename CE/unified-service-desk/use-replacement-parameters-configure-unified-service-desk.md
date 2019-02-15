---
title: Use replacement parameters to configure Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn how to use replacement parameters in Unified Service Desk to customize amd personalize interactions through actions and window navigation rules.
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
ms.assetid: 8d435068-1fd3-4886-b574-f1001dc21bc8
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
ms.openlocfilehash: 03b285e509a2cc44cd1cb550033ffb108ebb03a8
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388698"
---
# <a name="use-replacement-parameters-to-configure-unified-service-desk"></a><span data-ttu-id="eb9c3-103">Use replacement parameters to configure Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="eb9c3-103">Use replacement parameters to configure Unified Service Desk</span></span>
<span data-ttu-id="eb9c3-104">Thông số thay thế có thể được sử dụng để tuỳ chỉnh tương tác trong một quá trình kinh doanh cụ thể thông qua quy tắc điều hướng cửa sổ và hành động.</span><span class="sxs-lookup"><span data-stu-id="eb9c3-104">Replacement parameters can be used for customizing interactions during a specific business process through actions and window navigation rules.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="eb9c3-105">[Replacement parameters](../unified-service-desk/replacement-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="eb9c3-105">[Replacement parameters](../unified-service-desk/replacement-parameters.md)</span></span>  

 <span data-ttu-id="eb9c3-106">Chủ đề này cung cấp thông tin về các phím thay thế mà bạn có thể sử dụng trong các tham số thay thế để chỉ ra cách xử lý đặc biệt về cách bạn có thể sử dụng các tham số thay thế trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] trong một số điều kiện đặc biệt.</span><span class="sxs-lookup"><span data-stu-id="eb9c3-106">This topic provides information about the replacement keys that you can use in your replacement parameters to indicate special handling how you can use the replacement parameters in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] in some special conditions.</span></span>  

<a name="ReplacementKeys"></a>   
## <a name="replacement-keys"></a><span data-ttu-id="eb9c3-107">Phím thay thế</span><span class="sxs-lookup"><span data-stu-id="eb9c3-107">Replacement keys</span></span>  
 <span data-ttu-id="eb9c3-108">Bảng dưới đây cung cấp các thông tin về các phím thay thế mà bạn có thể sử dụng trong các tham số thay thế.</span><span class="sxs-lookup"><span data-stu-id="eb9c3-108">The following table provides information about the replacement keys that you can use in your replacement parameters.</span></span>  


| <span data-ttu-id="eb9c3-109">Phím thay thế</span><span class="sxs-lookup"><span data-stu-id="eb9c3-109">Replacement key</span></span> |                                                                                                                                                                                                                                          <span data-ttu-id="eb9c3-110">Mô tả</span><span class="sxs-lookup"><span data-stu-id="eb9c3-110">Description</span></span>                                                                                                                                                                                                                                           |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        +        |     <span data-ttu-id="eb9c3-111">Phím này, khi có, sẽ thay thế phím không tồn tại hoặc không có bằng một chuỗi trống.</span><span class="sxs-lookup"><span data-stu-id="eb9c3-111">This key, when present, will replace a null or non-existent key with an empty string.</span></span><br /><br /> <span data-ttu-id="eb9c3-112">For example: In the scenario where `account.name` is undefined, calling `[[account.name]]` would result in a “Not all parameters in action call *\<ActionName>* are available, aborting action call.”</span><span class="sxs-lookup"><span data-stu-id="eb9c3-112">For example: In the scenario where `account.name` is undefined, calling `[[account.name]]` would result in a “Not all parameters in action call *\<ActionName>* are available, aborting action call.”</span></span> <span data-ttu-id="eb9c3-113">error.</span><span class="sxs-lookup"><span data-stu-id="eb9c3-113">error.</span></span> <span data-ttu-id="eb9c3-114">This will stop processing the rule or line item being executed.</span><span class="sxs-lookup"><span data-stu-id="eb9c3-114">This will stop processing the rule or line item being executed.</span></span><br /><br /> <span data-ttu-id="eb9c3-115">However, `[[account.name]+]` will return a blank, and not raise the replacement key error.</span><span class="sxs-lookup"><span data-stu-id="eb9c3-115">However, `[[account.name]+]` will return a blank, and not raise the replacement key error.</span></span>      |
|        $        |                                                                                                                                          <span data-ttu-id="eb9c3-116">Phím này cho phép thoát trong dấu ngoặc kép và xuống dòng.</span><span class="sxs-lookup"><span data-stu-id="eb9c3-116">This key allows escaping of quotes and line breaks.</span></span> <span data-ttu-id="eb9c3-117">Nó thường được sử dụng như là một toán tử khi gọi một scriptlet hoặc trả về chuỗi nhiều dòng.</span><span class="sxs-lookup"><span data-stu-id="eb9c3-117">It is generally used as an operator when invoking a scriptlet or returning a multi-line string.</span></span><br /><br /> <span data-ttu-id="eb9c3-118">Ví dụ: `[[script.MyMultiLineString]$]`</span><span class="sxs-lookup"><span data-stu-id="eb9c3-118">For example: `[[script.MyMultiLineString]$]`</span></span>                                                                                                                                          |
|        ^        |                                                                                                                                                                    <span data-ttu-id="eb9c3-119">Phím này ngăn không cho thoát dấu ngoặc kép và xuống dòng và được sử dụng để làm đồng đều bộ kết quả nhiều dòng.</span><span class="sxs-lookup"><span data-stu-id="eb9c3-119">This key prevents escaping of quotes and line breaks, and is used to flatten multi-line result set.</span></span><br /><br /> <span data-ttu-id="eb9c3-120">Ví dụ: `MyMultiline=[[myvalue]^]`</span><span class="sxs-lookup"><span data-stu-id="eb9c3-120">For example: `MyMultiline=[[myvalue]^]`</span></span>                                                                                                                                                                     |
|        <span data-ttu-id="eb9c3-121">u</span><span class="sxs-lookup"><span data-stu-id="eb9c3-121">u</span></span>        |                                                                                        <span data-ttu-id="eb9c3-122">Khóa này được sử dụng cho tham số thay thế Mã hóa URL (cũng được gọi là Mã hóa tỷ lệ).</span><span class="sxs-lookup"><span data-stu-id="eb9c3-122">This key is used to URL Encode (also called Percent Encode) the replacement parameter.</span></span><br /><br /> <span data-ttu-id="eb9c3-123">For example, consider the replacement parameter in the following URL: http://mysite?something=`[[opportunity.name]u]`.</span><span class="sxs-lookup"><span data-stu-id="eb9c3-123">For example, consider the replacement parameter in the following URL: http://mysite?something=`[[opportunity.name]u]`.</span></span><br /><br /> <span data-ttu-id="eb9c3-124">The following string is returned: http://mysite?something=My%20Opportunity.</span><span class="sxs-lookup"><span data-stu-id="eb9c3-124">The following string is returned: http://mysite?something=My%20Opportunity.</span></span>                                                                                        |
|        <span data-ttu-id="eb9c3-125">x</span><span class="sxs-lookup"><span data-stu-id="eb9c3-125">x</span></span>        |                                                                                                                                                <span data-ttu-id="eb9c3-126">Khóa này được sử dụng cho tham số thay thế Mã hóa XML.</span><span class="sxs-lookup"><span data-stu-id="eb9c3-126">This key is used to XML encode the replacement parameter.</span></span> <span data-ttu-id="eb9c3-127">Cho phép các ký tự XAML, chẳng hạn như <, để thoát và hiển thị đúng trong đầu ra.</span><span class="sxs-lookup"><span data-stu-id="eb9c3-127">The enables the XAML characters, such as <, to be escaped and display properly in the output.</span></span><br /><br /> <span data-ttu-id="eb9c3-128">Ví dụ, `[[myvalue]x]`.</span><span class="sxs-lookup"><span data-stu-id="eb9c3-128">For example, `[[myvalue]x]`.</span></span>                                                                                                                                                |
|        <span data-ttu-id="eb9c3-129">g</span><span class="sxs-lookup"><span data-stu-id="eb9c3-129">g</span></span>        |                                                                                                                                                                    <span data-ttu-id="eb9c3-130">Khóa này được sử dụng để trả về giá trị từ phiên chung.</span><span class="sxs-lookup"><span data-stu-id="eb9c3-130">This key is used to return the value from the global session.</span></span> <span data-ttu-id="eb9c3-131">Nếu không tìm thấy khóa trong phiên chung, nó sẽ dẫn đến lỗi không tìm thấy khóa.</span><span class="sxs-lookup"><span data-stu-id="eb9c3-131">If the key cannot be found in the global session, it will result in a key not found error.</span></span>                                                                                                                                                                    |
|        <span data-ttu-id="eb9c3-132">a</span><span class="sxs-lookup"><span data-stu-id="eb9c3-132">a</span></span>        |                                                                                                                                                         <span data-ttu-id="eb9c3-133">Khóa này được sử dụng để trả về giá trị từ phiên đang hiện hoạt mà được tập trung.</span><span class="sxs-lookup"><span data-stu-id="eb9c3-133">This key is used to return value from the currently active session that is in focus.</span></span> <span data-ttu-id="eb9c3-134">Nếu không tìm thấy khóa trong phiên hiện hoạt nó sẽ dẫn đến lỗi không tìm thấy khóa.</span><span class="sxs-lookup"><span data-stu-id="eb9c3-134">If the key cannot be found in the active session it will result in a key not found error.</span></span>                                                                                                                                                         |
|        <span data-ttu-id="eb9c3-135">v</span><span class="sxs-lookup"><span data-stu-id="eb9c3-135">v</span></span>        | <span data-ttu-id="eb9c3-136">Khóa này được sử dụng để thay thế các khóa trong khóa thay thế.</span><span class="sxs-lookup"><span data-stu-id="eb9c3-136">This key is used to replace keys within a replacement key.</span></span><br /><br /> <span data-ttu-id="eb9c3-137">Ví dụ, hãy xem xét hai giá trị sau đây:</span><span class="sxs-lookup"><span data-stu-id="eb9c3-137">For example, consider the following two values:</span></span><br /><br /> <span data-ttu-id="eb9c3-138">-   account.name = "My Account"</span><span class="sxs-lookup"><span data-stu-id="eb9c3-138">-   account.name = "My Account"</span></span><br /><span data-ttu-id="eb9c3-139">-   mytemplate.value = "My template is `[[account.name]+]`"</span><span class="sxs-lookup"><span data-stu-id="eb9c3-139">-   mytemplate.value = "My template is `[[account.name]+]`"</span></span><br /><br /> <span data-ttu-id="eb9c3-140">When you invoke the `[[mytemplate.value]]`, the following string is returned: “My Template is [[account.name]+]".</span><span class="sxs-lookup"><span data-stu-id="eb9c3-140">When you invoke the `[[mytemplate.value]]`, the following string is returned: “My Template is [[account.name]+]".</span></span><br /><br /> <span data-ttu-id="eb9c3-141">However, when you invoke `[[mytemplate.value]v]`, the following string is returned: "My template is My Account".</span><span class="sxs-lookup"><span data-stu-id="eb9c3-141">However, when you invoke `[[mytemplate.value]v]`, the following string is returned: "My template is My Account".</span></span> |

<a name="SpecializedHandlers"></a>   
## <a name="specialized-handlers"></a><span data-ttu-id="eb9c3-142">Trình xử lý chuyên dụng</span><span class="sxs-lookup"><span data-stu-id="eb9c3-142">Specialized handlers</span></span>  
 <span data-ttu-id="eb9c3-143">Thông thường, chúng ta có nhu cầu thực hiện mọi việc đơn giản, giống như nếu/sau đó/loại khác xây dựng mà không đảm bảo tạo ra scriptlet.</span><span class="sxs-lookup"><span data-stu-id="eb9c3-143">Often times, there is a need to do something simple, like an if/then/else type construct that does not warrant creating a scriptlet.</span></span> <span data-ttu-id="eb9c3-144">Các tình huống này yêu cầu sử dụng một scriptlet bên trong một cuộc gọi hành động.</span><span class="sxs-lookup"><span data-stu-id="eb9c3-144">These situations require using a scriptlet inside an action call.</span></span> <span data-ttu-id="eb9c3-145">There are two specialized handlers to assist when building inline scriptlets in action calls: `$Expression` and `$Multiline`.</span><span class="sxs-lookup"><span data-stu-id="eb9c3-145">There are two specialized handlers to assist when building inline scriptlets in action calls: `$Expression` and `$Multiline`.</span></span>  

### <a name="expression"></a><span data-ttu-id="eb9c3-146">$Biểu thức</span><span class="sxs-lookup"><span data-stu-id="eb9c3-146">$Expression</span></span>  
 <span data-ttu-id="eb9c3-147">Consider a situation where you need to switch display name based on the entity type code (etc) of the current entity.</span><span class="sxs-lookup"><span data-stu-id="eb9c3-147">Consider a situation where you need to switch display name based on the entity type code (etc) of the current entity.</span></span> <span data-ttu-id="eb9c3-148">Bạn đang xây dựng một URL cần thông tin này.</span><span class="sxs-lookup"><span data-stu-id="eb9c3-148">You are building a URL that needs this information.</span></span> <span data-ttu-id="eb9c3-149">Trong tình huống này, chỉ có thể tải tài khoản hoặc liên hệ.</span><span class="sxs-lookup"><span data-stu-id="eb9c3-149">In this situation, there can only be either an account or contact loaded.</span></span>  

 <span data-ttu-id="eb9c3-150">In this scenario, we are calling the **Navigate** action on a **Standard Web Application** hosted control by using the following value in the **Data** field:</span><span class="sxs-lookup"><span data-stu-id="eb9c3-150">In this scenario, we are calling the **Navigate** action on a **Standard Web Application** hosted control by using the following value in the **Data** field:</span></span>  

```  
url= http://mysite/showmessage.aspx?displayname={either the account or contact display name}  
```  

 <span data-ttu-id="eb9c3-151">To achieve this, we will use `$Expression` as follows:</span><span class="sxs-lookup"><span data-stu-id="eb9c3-151">To achieve this, we will use `$Expression` as follows:</span></span>  

```  
url= http://mysite/showmessage.aspx?displayname=$Expression("[[$Context.etc]]" == "1" ? "[[account.name]u+]" : "[[contact.fullname]u+]")  
```  

 <span data-ttu-id="eb9c3-152">Điều này có hiệu quả tạo ra và chạy một scriptlet như các hành động được xử lý.</span><span class="sxs-lookup"><span data-stu-id="eb9c3-152">This effectively creates and runs a scriptlet as the action is processed.</span></span>  

### <a name="multiline"></a><span data-ttu-id="eb9c3-153">$Đa dòng</span><span class="sxs-lookup"><span data-stu-id="eb9c3-153">$Multiline</span></span>  
 <span data-ttu-id="eb9c3-154">Trong phần $Biểu thức, chúng tôi đã nói về cách thực hiện sriptlet nội tuyến bên trong một hành động.</span><span class="sxs-lookup"><span data-stu-id="eb9c3-154">In the $Expression section, we talked about doing an inline scriptlet within an action.</span></span> <span data-ttu-id="eb9c3-155">Trong tình hình có yêu cầu thực hiện một scriptlet phức tạp hơn và bạn vẫn không muốn sử dụng đối tượng scriptlet để lưu trữ scriptlet, lệnh $Đa dòng có thể được sử dụng để lưu trữ Scriptlet phức tạp hơn.</span><span class="sxs-lookup"><span data-stu-id="eb9c3-155">In the situation where there is a need to do a more complex scriptlet, and you still do not want to use a scriptlet object to store the scriptlet, the $Multiline command can be used to store more complex scriptlets.</span></span>  

 <span data-ttu-id="eb9c3-156">For example, using the example we used earlier in the `$Expression` section, it can be broken out as:</span><span class="sxs-lookup"><span data-stu-id="eb9c3-156">For example, using the example we used earlier in the `$Expression` section, it can be broken out as:</span></span>  

```  
url= http://mysite/showmessage.aspx?displayname=$Multiline( $Expression(  
function doWork()  
{  
      If ("[[$Context.etc]]" == "1")  
          return "[[account.name]u+]"   
      else   
          return "[[contact.fullname]u+]"  
}  
doWork();   
))  
```  

### <a name="see-also"></a><span data-ttu-id="eb9c3-157">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="eb9c3-157">See also</span></span>  
 <span data-ttu-id="eb9c3-158">[Thông số thay thế](../unified-service-desk/replacement-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="eb9c3-158">[Replacement parameters](../unified-service-desk/replacement-parameters.md) </span></span>  
 <span data-ttu-id="eb9c3-159">[Execute scripts using scriptlets in Unified Service Desk](../unified-service-desk/execute-scripts-using-scriptlets-unified-service-desk.md) </span><span class="sxs-lookup"><span data-stu-id="eb9c3-159">[Execute scripts using scriptlets in Unified Service Desk](../unified-service-desk/execute-scripts-using-scriptlets-unified-service-desk.md) </span></span>  
 [<span data-ttu-id="eb9c3-160">Unified Service Desk Configuration Walkthroughs</span><span class="sxs-lookup"><span data-stu-id="eb9c3-160">Unified Service Desk Configuration Walkthroughs</span></span>](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md)
