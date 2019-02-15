---
title: Replacement parameters in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Replacement parameters can be used throughout the application to pull data from data elements (called data parameters) captured during the execution of the application that augment and include the Unified Service Desk context.
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
ms.assetid: fbef0bd3-e118-4a5b-8568-897538972066
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
ms.openlocfilehash: 5e77062ab91601d9d2a637c4b788ebe07d0fe702
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388292"
---
# <a name="replacement-parameters-in-unified-service-desk"></a>Replacement parameters in Unified Service Desk

Tham số thay thế có thể được sử dụng trong ứng dụng để kéo dữ liệu từ phần tử dữ liệu (được gọi là tham số dữ liệu) nắm bắt được trong quá trình thực hiện ứng dụng bổ sung và bao gồm ngữ cảnh [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. Bối cảnh bao gồm cặp chuỗi tên/giá trị mà thay đổi thường xuyên như dữ liệu được khám phá từ nhiều cách khác nhau trong khi sử dụng ứng dụng. Tham số thay thế được sử dụng cho một loạt các nhiệm vụ như xác định chuỗi truy vấn URL, tạo đầu ra mã lệnh trong Scriptlet, chỉ định giá trị tìm kiếm cho tìm kiếm thực thể, Tích hợp điện thoại máy tính (CTI) và xác định đầu vào cho hành động được gọi trên kiểm soát tổ chức khác. Tham số thay thế là những yếu tố chính mà cho phép một mức độ cao của cấu hình hoặc tuỳ chỉnh trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] mà không cần phải sử dụng mã.  
  
 For information on how you can use replacement parameters to configure your agent application, see [Use replacement parameters to configure Unified Service Desk](../unified-service-desk/use-replacement-parameters-configure-unified-service-desk.md).  
  
> [!NOTE]
>  Đôi khi tham số thay thế được sử dụng thay thế cho nhau với dữ liệu tham số vì tham số thay thế về cơ bản là đại diện của một tham số dữ liệu.  
  
<a name="ViewReplacementParameters"></a>   
## <a name="view-the-replacement-parameters-in-unified-service-desk"></a>Xem tham số thay thế trong Unified Service Desk  
 Kiểm soát trình gỡ lỗi trong ứng dụng khách có thể được sử dụng để xem danh sách các tham số thay thế có sẵn tại bất kỳ thời gian nhất định.  
  
1. Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client, and log on to Microsoft Dynamics 365 for Customer Engagement apps where you have installed the sample packages.  
  
2. Trong màn hình chính của ứng dụng [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], nhấp vào mũi tên xuống bên cạnh các bánh răng ở góc trên bên phải, và chọn **gỡ lỗi**. Trình gỡ lỗi xuất hiện.  
  
   ![Debug option to open Debugger](../unified-service-desk/media/usd-view-debugger.png "Debug option to open Debugger")  
  
3. Trong trình gỡ lỗi, bấm vào **Tham số dữ liệu** để xem các thông số thay thế.  
  
   ![Replacement parameters on Data Parameters tab](../unified-service-desk/media/usd-replacement-parameters.PNG "Replacement parameters on Data Parameters tab")  
  
   Chế độ xem dạng cây được sử dụng để đại diện cho các biến có sẵn. Khi xác định các biến, chỉ định tên ở cấp độ gốc, theo sau là dấu chấm (.), và sau đó là tên trong danh sách. Dưới đây là một số ví dụ:  
  
- `[[$Session.IsGlobal]]`  
  
- `[[$User.fullname]]`  
  
  These values will change as the user interacts in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client. Cuộc gọi hành động sẽ chọn giá trị hiện tại và sử dụng trong danh sách tham số của nó, hoặc bất cứ nơi nào khác nó có thể được sử dụng. Bất cứ lúc nào các biến được cập Nhật, sự kiện **NotifyContextChange** sẽ được hiển thị trong kiểm soát cơ sở ngay cả khi ngữ cảnh [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] không không thay đổi chính nó. Điều này cho phép các tính năng giống như dòng phiên kiểm tra lại các giá trị của tham số thay thế để xem nếu nó cần phải cập nhật màn hình của nó không.  
  
<a name="SystemReplacementParameters"></a>   
## <a name="system-replacement-parameters"></a>Thông số thay thế hệ thống  
 Thông số thay thế hệ thống là các tham số thay thế được xác định và lưu trữ tại hệ thống, và tên bắt đầu với $ để giữ cho chúng riêng biệt với các tham số thay thế do người dùng xác định. Ví dụ, `$Global`. [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] has following replacement parameters:  
  
-   [$Context](../unified-service-desk/replacement-parameters.md#Context)  
  
-   [$Debug](../unified-service-desk/replacement-parameters.md#Debug)  
  
-   [$Global](../unified-service-desk/replacement-parameters.md#Global)  
  
-   [$Panel](../unified-service-desk/replacement-parameters.md#Panel)  
  
-   [$Resources](../unified-service-desk/replacement-parameters.md#Resources)  
  
-   [$Return](../unified-service-desk/replacement-parameters.md#Return)  
  
-   [$Session](../unified-service-desk/replacement-parameters.md#Session)  
  
-   [$Settings](../unified-service-desk/replacement-parameters.md#Settings)  
  
-   [$Subject](../unified-service-desk/replacement-parameters.md#Subject)  
  
-   [$SystemParameters](#SystemParameters)  
  
-   [$User](../unified-service-desk/replacement-parameters.md#User)  
  
<a name="Context"></a>   
### <a name="context"></a>$Context  
 This section contains the contents of the [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] session context, and provides a convenient way to use [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] session context variables throughout the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]application.  
  
> [!NOTE]
>  The Global Manager hosted control provides an action that allows you to copy values from other replacement parameters into the context. Điều này có thể là hữu ích khi chuyển cuộc gọi hoặc lưu phiên cho quá trình phục hồi sau đó. Bối cảnh có thể được lưu vào máy chủ trong các phiên bản này sử dụng cơ cấu UII tiêu chuẩn.  
  
<a name="Debug"></a>   
### <a name="debug"></a>$Debug  
 Đây là một giá trị thay thế đặc biệt chỉ được sử dụng trong Scriptlet để xác định xem nó có được gọi bởi cửa sổ gỡ lỗi không. Đặc biệt là khi Scriptlet đang làm cho hành động được thực hiện trên hệ thống, chúng tôi kiểm tra tham số này để xác định xem chúng ta có nên bỏ qua việc chặn mã để tránh tác dụng phụ khi gỡ lỗi. Scriptlet sau đây sẽ khởi động kiểm soát tổ chức tài khoản và hiển thị tab khi cửa sổ gỡ lỗi được mở ra.  
  
```  
CRMGlobalManager.GetApp(“Account”);  
```  
  
 This is because the scripts are run in the current context to determine their values in the current state of the system. To avoid this side effect from occurring, do the following.  
  
```  
If ([[$Debug]]!= true) CRMGlobalManager.GetApp(“Account”);  
```  
  
 Điều này sẽ tránh các tác dụng phụ và tiếp tục cung cấp thông tin hữu ích cho trình gỡ lỗi.  
  
<a name="Global"></a>   
### <a name="global"></a>$Global  
 This section is automatically added to show all options configured in Dynamics 365 for Customer Engagement apps Options and their values. Điều này làm cho tùy chọn có thể được truy cập dễ dàng vì chúng có thể được sử dụng để kiểm soát thực hiện hoặc để kiểm soát hành vi đã được tạo trong quy trình công việc hoặc cuộc gọi hành động. Tất cả cờ kiểm tra tự động hiển thị từ phần này.  
  
<a name="Panel"></a>   
### <a name="panel"></a>$Panel  
 The `$Panel` replacement parameter contains all the hosted controls and their current panel names as key-value pairs that have moved to another panel after you last started the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client. The replacement parameter becomes available only if at least one hosted control has changed panels after you last started the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client. All other hosted controls and their existing panels currently loaded in the agent desktop aren’t available in this replacement parameter.  
  
<a name="Resources"></a>   
### <a name="resources"></a>$Resources  
 Bộ sưu tập các thông số thay thế được Trình quản lý chung xác định với bộ định danh ngôn ngữ. In the configuration of the Global Manager hosted control, you can specify various language resources. These resources take the form of .resx files but are uploaded into web resources as XML files. Upon loading of the application, [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] will read the current language setting from Dynamics 365 for Customer Engagement apps and then look for this language in the Global Manager language list. Nếu mục được liệt kê, các nguồn của bộ định danh ngôn ngữ sẽ được tải vào bộ sưu tập $Resources này.  
  
 Wherever you intended to provide language neutral text on the output, you can instead use the replacement parameters from the `$Resources` collection. Ví dụ, bạn có thể sử dụng sau đây cho các văn bản nút.  
  
```  
[[$Resources.MyButtonName]+]  
```  
  
 Depending on the selected language for the user, appropriate localized text will be used.  
  
 It is also important to note here that these replacement parameters, and therefore the .resx files that are loaded, may contain replacement parameter syntax itself. After `$Resources` values are replaced, they are rechecked for additional replacement parameters. Bằng cách này, ngay cả khi bạn đang cung cấp chuỗi dành riêng ngôn ngữ, bạn cũng có thể thay thế các dữ liệu từ phần còn lại của các ứng dụng vào chuỗi này.  
  
 For information about adding localized resources to configure [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Add multilanguage support for your agent applications](../unified-service-desk/add-multilanguage-support-agent-applications.md).  
  
<a name="Return"></a>   
### <a name="return"></a>$Return  
 Một số hành động trả về một giá trị chuỗi. This string value is placed into the $Return replacement parameter using the name of the action call. Nó sẽ tuân theo mô hình này:  
  
```  
[[$Return.ActionCallName]]  
```  
  
 Một ví dụ về điều này sẽ gọi CreateEntity trên trình quản lý chung. This will create a record in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps, and return the GUID of the new record. This new GUID will be in the `$Return` replacement parameter list and can be used as input to the next action.  
  
<a name="Session"></a>   
### <a name="session"></a>$Session  
 The `$Session` section exposes useful variables needed by action calls such as the session count, whether the active session is global, currently active session ID. The `StartTime` value can be used for writing the start time to an activity. This section is populated automatically.  
  
<a name="Settings"></a>   
### <a name="settings"></a>$Settings  
 This section provides user settings that only apply to the current user. These settings are automatically loaded at startup, and may be read using an action call at runtime. These often include settings for the theme selection of the user but may provide access to any user specific settings that the configurator wants to make available.  
  
 These user settings are defined in the **User Settings** area (**Settings** > **User Settings**) in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps while configuring [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].  
  
 Các thiết đặt này có thể được sử dụng như bất kỳ tham số thay thế khác trong hệ thống. The Global Manager hosted control provides an action, [SaveSetting](../unified-service-desk/global-manager-hosted-control.md#SaveSetting), which will write user settings to the server, assuming the user has write access. This can be used to store user specific preferences such as theme selection and layouts.  
  
> [!NOTE]
>  The user settings can be saved to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps server if the user has write access.  
  
<a name="Subject"></a>   
### <a name="subject"></a>$Subject  
 Một khả năng hữu ích trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] là để tự động xác định cây chủ đề trong trường hợp mới mà được tạo trên danh nghĩa của người sử dụng. Đôi khi bạn sẽ muốn tự động xác định trường chủ đề nhưng bạn cần phải biết các giá trị chính xác để sử dụng, mà có thể thay đổi từ hệ thống đến hệ thống.  
  
 Với mục nhập này, bạn có thể tham chiếu đến chủ đề cụ thể khi bạn đang tạo trường hợp, bằng cách sử dụng các tham số thay thế sau đây.  
  
```  
[[$Subject.Default Subject.Id]][[$Subject.Default Subject.LogicalName]]  
```  
  
<a name="SystemParameters"></a>   
### <a name="systemparameters"></a>$SystemParameters  
 This section contains a variable called `HighContrast` that displays whether high-contrast mode in Windows is enabled or not (true/false). You could use this variable to decide whether to enable normal custom colors or system colors (compliant with high-contrast setting) when you customize your theme in the client. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Customize themes in Unified Service Desk](../unified-service-desk/customize-themes-in-unified-service-desk.md )  
  
<a name="User"></a>   
### <a name="user"></a>$User  
 This replacement parameter group is automatically populated with the contents of the current user’s record in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps. For example, if the administrator extends the system user entity in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps to include an agent id, the agent id will appear in this list. This can be used to configure special user settings.  
  
### <a name="see-also"></a>Xem thêm  
 [Use replacement parameters to configure Unified Service Desk](../unified-service-desk/use-replacement-parameters-configure-unified-service-desk.md)   
 
 [Execute scripts using scriptlets in Unified Service Desk](../unified-service-desk/execute-scripts-using-scriptlets-unified-service-desk.md)   
 
 [Search data using entity searches in Unified Service Desk](../unified-service-desk/search-data-entity-searches.md) 
 
 [Learn to use Unified Service Desk](../unified-service-desk/learn-to-use-unified-service-desk.md)   
 
 [Global Manager (Hosted Control)](../unified-service-desk/global-manager-hosted-control.md)
