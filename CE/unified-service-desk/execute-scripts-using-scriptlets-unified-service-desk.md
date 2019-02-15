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
# <a name="execute-scripts-using-scriptlets-in-unified-service-desk"></a>Execute scripts using scriptlets in Unified Service Desk
Scriptlets are snippets of JavaScript that are executed when using a special syntax for your replacement parameter. Đôi khi các tham số thay thế được hệ thống tạo ra chứa dữ liệu thích hợp cần thiết cho các chức năng này, nhưng có thể không chứa dữ liệu trong các định dạng mong muốn. Ví dụ, trong Tích hợp điện thoại máy tính (CTI), số điện thoại thường đến từ hệ thống điện thoại dưới dạng chuỗi các chữ số như "3035551212", mà không có bất kỳ định dạng nào. However, Microsoft Dynamics 365 for Customer Engagement apps stores phone numbers as a string that typically includes formatting characters such as dashes as in (303) 555-1212. If you were to search your Dynamics 365 for Customer Engagement apps entity using the data supplied directly by the phone system, changes are slim that a match would ever be found. Bạn giải quyết điều này bằng cách sử dụng Scriptlet trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].  
  
<a name="HowTo"></a>   
## <a name="how-to-use-scriptlets"></a>Cách sử dụng Scriptlet?  
 You define a scriptlet in the **Scriptlets** area (**Settings** > **Scriptlets**) in Microsoft Dynamics 365 for Customer Engagement apps. Sau khi bạn đã xác định scriptlet, bạn sử dụng scriptlet trong các định dạng sau đây như là một tham số thay thế trong các truy vấn hoặc các tham số cho cuộc gọi hành động.  
  
```  
[[script.<Scriptlet_Name>]]  
```  
  
 Khi hệ thống thấy tham số thay thế một bắt đầu với **mã lệnh.**, nó sẽ tìm kiếm một mã lệnh với tên phù hợp với văn bản theo sau nó trong danh sách scriptlet. Nếu nó tìm thấy một scriptlet với tên được chỉ định, nó sẽ lần đầu tiên thay thế các tham số trong kịch bản đó, và sau đó thực hiện mã lệnh dưới dạng biểu thức JavaScript. Giá trị của biểu thức sẽ được sử dụng để thay thế giá trị của tham số thay thế ở trên.  
  
> [!WARNING]
>  Nếu tham số thay thế của bạn trong scriptlet chứa một scriptlet thay thế khác và cho đến khi nó tạo ra một vòng lặp, nó sẽ làm cho hệ thống liên tục thay thế thông số cho đến khi ngăn xếp tràn. As a result, it is highly recommended that you never use `[[script.ReplacementParameters]]` in your scriptlets.  
  
<a name="RferringToGlobalHC"></a>   
## <a name="referring-to-global-hosted-controls-from-your-scriptlets"></a>Referring to global hosted controls from your scriptlets  
 Scriptlet có thể tham khảo các phương pháp kiểm soát tổ chức chung trong khi thực hiện. Tất cả kiểm soát tổ chức chung (không động) được thêm vào như là các đối tượng cps thể viết mã lệnh vào động cơ scriptlet lúc khởi động. Because JavaScript cannot refer to names with spaces in them, the scriptlet engine automatically replaces spaces in the name of your global hosted control with “_” underscores. You can therefore use the following valid JavaScript.  
  
```  
Connection_Manager.ConfigurationReader.ReadAppSettings(“maxNumberOfSessions”);  
```  
  
 Có tồn tại một kịch bản trường hợp đặc biệt cho trình quản lý chung. It can also be referred to via `CRMGlobalManager`, regardless of what it is named in the configuration.  
  
 Nếu (CRMGlobalManager.SessionCount == 0) / / không có phiên khách hàng nào được tải. Chỉ có phiên chung được tải.  
  
> [!NOTE]
>  Chỉ có chức năng chung có thể truy cập thông qua phương pháp này.  
  
 Consider a situation where you want to display session overview information in your Session Lines component but the information actually resides in an external system that is accessible via web services rather than being available in your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps server. Bạn có thể tạo ra kiểm soát tổ chức cho thấy một chức năng chung, mà gọi các Dịch vụ web bên ngoài. You then configure this hosted control as a global hosted control and place it on the HiddenPanel. Cuộc gọi Dịch vụ web và chức năng này bây giờ là có thể sử dụng từ một scriptlet. You could then create the following scriptlet to call your new function.  
  
```  
My_Global_Application.CallExternalWebService(“[[account.accountnumber]$]”);  
```  
  
 Mã này đi qua số tài khoản từ tài khoản vào chức năng của bạn như là tham số đầu tiên. Nếu bạn đặt tên **Gọi Dịch vụ web** scriplet của bạn, bạn có thể sử dụng dòng phiên sau đây để hiển thị kết quả của các cuộc gọi Dịch vụ web.  
  
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
  
### <a name="see-also"></a>Xem thêm  
 [Thông số thay thế](../unified-service-desk/replacement-parameters.md)   
 [Global and session-based Unified Service Desk hosted controls](../unified-service-desk/unified-service-desk-hosted-controls.md#Global)
