---
title: Execute scripts using scriptlets in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Scriptlets are snippets of JavaScript that are executed when using a special syntax for your replacement parameter.
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
ms.assetid: 43bc1881-1db2-44ea-b52f-ed79717f5120
caps.latest.revision: 6
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: e4169639e8720fc3fb0e8e9e7413ff0c3539b106
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387834"
---
# <a name="execute-scripts-using-scriptlets-in-unified-service-desk"></a><span data-ttu-id="fa75c-103">Execute scripts using scriptlets in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="fa75c-103">Execute scripts using scriptlets in Unified Service Desk</span></span>
<span data-ttu-id="fa75c-104">Scriptlets are snippets of JavaScript that are executed when using a special syntax for your replacement parameter.</span><span class="sxs-lookup"><span data-stu-id="fa75c-104">Scriptlets are snippets of JavaScript that are executed when using a special syntax for your replacement parameter.</span></span> <span data-ttu-id="fa75c-105">Đôi khi các tham số thay thế được hệ thống tạo ra chứa dữ liệu thích hợp cần thiết cho các chức năng này, nhưng có thể không chứa dữ liệu trong các định dạng mong muốn.</span><span class="sxs-lookup"><span data-stu-id="fa75c-105">Sometimes the system generated replacement parameters contain the proper data needed for these functions, but might not contain the data in the desired format.</span></span> <span data-ttu-id="fa75c-106">Ví dụ, trong Tích hợp điện thoại máy tính (CTI), số điện thoại thường đến từ hệ thống điện thoại dưới dạng chuỗi các chữ số như "3035551212", mà không có bất kỳ định dạng nào.</span><span class="sxs-lookup"><span data-stu-id="fa75c-106">For example, in Computer Telephone Integration (CTI), phone numbers typically arrive from phone system as a string of digits such as “3035551212”, without any formatting.</span></span> <span data-ttu-id="fa75c-107">However, Microsoft Dynamics 365 for Customer Engagement apps stores phone numbers as a string that typically includes formatting characters such as dashes as in (303) 555-1212.</span><span class="sxs-lookup"><span data-stu-id="fa75c-107">However, Microsoft Dynamics 365 for Customer Engagement apps stores phone numbers as a string that typically includes formatting characters such as dashes as in (303) 555-1212.</span></span> <span data-ttu-id="fa75c-108">If you were to search your Dynamics 365 for Customer Engagement apps entity using the data supplied directly by the phone system, changes are slim that a match would ever be found.</span><span class="sxs-lookup"><span data-stu-id="fa75c-108">If you were to search your Dynamics 365 for Customer Engagement apps entity using the data supplied directly by the phone system, changes are slim that a match would ever be found.</span></span> <span data-ttu-id="fa75c-109">Bạn giải quyết điều này bằng cách sử dụng Scriptlet trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="fa75c-109">You address this using scriptlets in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span>  
  
<a name="HowTo"></a>   
## <a name="how-to-use-scriptlets"></a><span data-ttu-id="fa75c-110">Cách sử dụng Scriptlet?</span><span class="sxs-lookup"><span data-stu-id="fa75c-110">How to use scriptlets?</span></span>  
 <span data-ttu-id="fa75c-111">You define a scriptlet in the **Scriptlets** area (**Settings** > **Scriptlets**) in Microsoft Dynamics 365 for Customer Engagement apps.</span><span class="sxs-lookup"><span data-stu-id="fa75c-111">You define a scriptlet in the **Scriptlets** area (**Settings** > **Scriptlets**) in Microsoft Dynamics 365 for Customer Engagement apps.</span></span> <span data-ttu-id="fa75c-112">Sau khi bạn đã xác định scriptlet, bạn sử dụng scriptlet trong các định dạng sau đây như là một tham số thay thế trong các truy vấn hoặc các tham số cho cuộc gọi hành động.</span><span class="sxs-lookup"><span data-stu-id="fa75c-112">After you have defined a scriptlet, you use the scriptlet in the following format as a replacement parameter in your queries or parameters to the action calls.</span></span>  
  
```  
[[script.<Scriptlet_Name>]]  
```  
  
 <span data-ttu-id="fa75c-113">Khi hệ thống thấy tham số thay thế một bắt đầu với **mã lệnh.**, nó sẽ tìm kiếm một mã lệnh với tên phù hợp với văn bản theo sau nó trong danh sách scriptlet.</span><span class="sxs-lookup"><span data-stu-id="fa75c-113">When the system sees such a replacement parameter starting with **script.**, it will look for a script with the name matching the text following it in your scriptlet list.</span></span> <span data-ttu-id="fa75c-114">Nếu nó tìm thấy một scriptlet với tên được chỉ định, nó sẽ lần đầu tiên thay thế các tham số trong kịch bản đó, và sau đó thực hiện mã lệnh dưới dạng biểu thức JavaScript.</span><span class="sxs-lookup"><span data-stu-id="fa75c-114">If it finds a scriptlet with the specified name, it will first replace parameters within that script, and then execute the script as a JavaScript expression.</span></span> <span data-ttu-id="fa75c-115">Giá trị của biểu thức sẽ được sử dụng để thay thế giá trị của tham số thay thế ở trên.</span><span class="sxs-lookup"><span data-stu-id="fa75c-115">The value of the expression will be used to replace the value of the replacement above.</span></span>  
  
> [!WARNING]
>  <span data-ttu-id="fa75c-116">Nếu tham số thay thế của bạn trong scriptlet chứa một scriptlet thay thế khác và cho đến khi nó tạo ra một vòng lặp, nó sẽ làm cho hệ thống liên tục thay thế thông số cho đến khi ngăn xếp tràn.</span><span class="sxs-lookup"><span data-stu-id="fa75c-116">If your replacement parameters in the scriptlet contain another scriptlet replacement, and so on until it creates a loop, it will cause the system to continuously substitute parameters until the stack overflows.</span></span> <span data-ttu-id="fa75c-117">As a result, it is highly recommended that you never use `[[script.ReplacementParameters]]` in your scriptlets.</span><span class="sxs-lookup"><span data-stu-id="fa75c-117">As a result, it is highly recommended that you never use `[[script.ReplacementParameters]]` in your scriptlets.</span></span>  
  
<a name="RferringToGlobalHC"></a>   
## <a name="referring-to-global-hosted-controls-from-your-scriptlets"></a><span data-ttu-id="fa75c-118">Referring to global hosted controls from your scriptlets</span><span class="sxs-lookup"><span data-stu-id="fa75c-118">Referring to global hosted controls from your scriptlets</span></span>  
 <span data-ttu-id="fa75c-119">Scriptlet có thể tham khảo các phương pháp kiểm soát tổ chức chung trong khi thực hiện.</span><span class="sxs-lookup"><span data-stu-id="fa75c-119">Scriptlets can reference global hosted control methods while executing.</span></span> <span data-ttu-id="fa75c-120">Tất cả kiểm soát tổ chức chung (không động) được thêm vào như là các đối tượng cps thể viết mã lệnh vào động cơ scriptlet lúc khởi động.</span><span class="sxs-lookup"><span data-stu-id="fa75c-120">All global (non-dynamic) hosted controls are added as scriptable objects to the scriptlet engine at startup.</span></span> <span data-ttu-id="fa75c-121">Because JavaScript cannot refer to names with spaces in them, the scriptlet engine automatically replaces spaces in the name of your global hosted control with “_” underscores.</span><span class="sxs-lookup"><span data-stu-id="fa75c-121">Because JavaScript cannot refer to names with spaces in them, the scriptlet engine automatically replaces spaces in the name of your global hosted control with “_” underscores.</span></span> <span data-ttu-id="fa75c-122">You can therefore use the following valid JavaScript.</span><span class="sxs-lookup"><span data-stu-id="fa75c-122">You can therefore use the following valid JavaScript.</span></span>  
  
```  
Connection_Manager.ConfigurationReader.ReadAppSettings(“maxNumberOfSessions”);  
```  
  
 <span data-ttu-id="fa75c-123">Có tồn tại một kịch bản trường hợp đặc biệt cho trình quản lý chung.</span><span class="sxs-lookup"><span data-stu-id="fa75c-123">There exists a special case scenario for the Global Manager.</span></span> <span data-ttu-id="fa75c-124">It can also be referred to via `CRMGlobalManager`, regardless of what it is named in the configuration.</span><span class="sxs-lookup"><span data-stu-id="fa75c-124">It can also be referred to via `CRMGlobalManager`, regardless of what it is named in the configuration.</span></span>  
  
 <span data-ttu-id="fa75c-125">Nếu (CRMGlobalManager.SessionCount == 0) / / không có phiên khách hàng nào được tải.</span><span class="sxs-lookup"><span data-stu-id="fa75c-125">If (CRMGlobalManager.SessionCount == 0)  // no customer sessions are loaded.</span></span> <span data-ttu-id="fa75c-126">Chỉ có phiên chung được tải.</span><span class="sxs-lookup"><span data-stu-id="fa75c-126">Only a global session is loaded.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="fa75c-127">Chỉ có chức năng chung có thể truy cập thông qua phương pháp này.</span><span class="sxs-lookup"><span data-stu-id="fa75c-127">Only public functions are accessible via this method.</span></span>  
  
 <span data-ttu-id="fa75c-128">Consider a situation where you want to display session overview information in your Session Lines component but the information actually resides in an external system that is accessible via web services rather than being available in your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps server.</span><span class="sxs-lookup"><span data-stu-id="fa75c-128">Consider a situation where you want to display session overview information in your Session Lines component but the information actually resides in an external system that is accessible via web services rather than being available in your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps server.</span></span> <span data-ttu-id="fa75c-129">Bạn có thể tạo ra kiểm soát tổ chức cho thấy một chức năng chung, mà gọi các Dịch vụ web bên ngoài.</span><span class="sxs-lookup"><span data-stu-id="fa75c-129">You may create a hosted control that exposes a public function, which calls the external web service.</span></span> <span data-ttu-id="fa75c-130">You then configure this hosted control as a global hosted control and place it on the HiddenPanel.</span><span class="sxs-lookup"><span data-stu-id="fa75c-130">You then configure this hosted control as a global hosted control and place it on the HiddenPanel.</span></span> <span data-ttu-id="fa75c-131">Cuộc gọi Dịch vụ web và chức năng này bây giờ là có thể sử dụng từ một scriptlet.</span><span class="sxs-lookup"><span data-stu-id="fa75c-131">This function and web service call is now usable from a scriptlet.</span></span> <span data-ttu-id="fa75c-132">You could then create the following scriptlet to call your new function.</span><span class="sxs-lookup"><span data-stu-id="fa75c-132">You could then create the following scriptlet to call your new function.</span></span>  
  
```  
My_Global_Application.CallExternalWebService(“[[account.accountnumber]$]”);  
```  
  
 <span data-ttu-id="fa75c-133">Mã này đi qua số tài khoản từ tài khoản vào chức năng của bạn như là tham số đầu tiên.</span><span class="sxs-lookup"><span data-stu-id="fa75c-133">This code passes the account number from the account into your function as the first parameter.</span></span> <span data-ttu-id="fa75c-134">Nếu bạn đặt tên **Gọi Dịch vụ web** scriplet của bạn, bạn có thể sử dụng dòng phiên sau đây để hiển thị kết quả của các cuộc gọi Dịch vụ web.</span><span class="sxs-lookup"><span data-stu-id="fa75c-134">If you name your scriptlet **Call Web Service**, you can then use the following Session Line to display the result of the web service call.</span></span>  
  
```  
<Grid Margin="0"  
  xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"  
  xmlns:CCA="clr-namespace:Dynamics;assembly=Dynamics">  
<Grid.RowDefinitions>  
 <RowDefinition Height="auto" />  
</Grid.RowDefinitions>  
<Grid.ColumnDefinitions>  
 <ColumnDefinition Width="100"/>  
 <ColumnDefinition Width="*" />  
 <ColumnDefinition Width="auto" />  
</Grid.ColumnDefinitions>  
<Label Margin="3,0,5,3" Content="Web Service Data" Padding="0" Grid.Row="4" HorizontalAlignment="Right" FontFamily="Tohoma" FontSize="12" FontWeight="Bold" />  
<TextBlock Text="[[script.Call Web Service]]" Margin="0" Grid.Column="1" Grid.Row="4" Padding="3,0,0,3" FontFamily="Tohoma" FontSize="12"/>  
</Grid>  
```  
  
### <a name="see-also"></a><span data-ttu-id="fa75c-135">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="fa75c-135">See also</span></span>  
 <span data-ttu-id="fa75c-136">[Thông số thay thế](../unified-service-desk/replacement-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="fa75c-136">[Replacement parameters](../unified-service-desk/replacement-parameters.md) </span></span>  
 [<span data-ttu-id="fa75c-137">Global and session-based Unified Service Desk hosted controls</span><span class="sxs-lookup"><span data-stu-id="fa75c-137">Global and session-based Unified Service Desk hosted controls</span></span>](../unified-service-desk/unified-service-desk-hosted-controls.md#Global)
