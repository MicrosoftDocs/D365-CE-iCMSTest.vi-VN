---
title: Customize themes in Unified Service Desk | MicrosoftDocs
description: Themes in Unified Service Desk define the look and feel of the agent application. A theme in Unified Service Desk consists of a XAML resource library, and can be placed on any web server and referenced via URL or can be compile into .NET assemblies (dll), and distributed with the agent applications.
keywords: ''
ms.date: 08/17/2018
ms.service:
- dynamics-365-customerservice
ms.custom:
- dyn365-USD
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: 27b60bcc-787e-451d-b795-be9b0efbc57d
author: kabala123
ms.author: kabala
manager: shujoshi
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: a806ae95a2a23c14934d798e104ad7d5a1dcb4b8
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385846"
---
# <a name="customize-themes-in-unified-service-desk"></a>Customize themes in Unified Service Desk
Các chủ đề trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] xác định giao diện của ứng dụng tổng đài viên. Một chủ đề trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] bao gồm một thư viện tài nguyên XAML và có thể được đặt trên bất kỳ máy chủ web nào và được tham chiếu thông qua URL hoặc có thể được tạo thành cụm .NET (dll) và phân phối với các ứng dụng tổng đài viên.  
  
  The predefined [Air Theme](../unified-service-desk/customize-themes-in-unified-service-desk.md#AirTheme) supports the high-contrast mode. The high-contrast mode in [!INCLUDE[pn_ms_Windows_short](../includes/pn-ms-windows-short.md)] helps you read the text on screen clearly by increasing the color contrast. When you turn on high-contrast mode on your computer and are using the  `Air Theme`, the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client will automatically switch to the high-contrast mode. Similarly, disabling the high-contrast mode on your computer will cause the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client to automatically switch to the normal display mode.  
  
> [!NOTE]
>  The automatic switching between normal and high-contrast modes in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client is supported only for the  predefined [Air Theme](../unified-service-desk/customize-themes-in-unified-service-desk.md#AirTheme). If you are using custom themes or custom hosted controls that supports high-contrast mode, the switching happens only after you restart the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client after switching to normal or high-contrast mode on your computer. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [High-contrast mode support  for custom themes](#HighContrast)  
  
<a name="PredefinedThemes"></a>   
## <a name="predefined-themes-available-in-unified-service-desk"></a>Chủ đề xác định trước có sẵn trong Unified Service Desk  
 [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]đi kèm với ba chủ đề được xác định trước.  

::: moniker range=">=dynamics-usd-4"

<a name="UnifiedBlueTheme"></a>   
### <a name="unified-blue-theme"></a>Unified Blue Theme

This is Unified Blue theme, which is the predefined theme for Unified Service Desk when you are using Unified Interface App.

![Unified Blue in Unified Service Desk](media/unified-blue-theme.png "Unified Blue in Unified Service Desk") 

::: moniker-end

<a name="AirTheme"></a>   
### <a name="air-theme"></a>Chủ đề về không khí  
 Đây là chủ đề về không khí. This theme supports high-contrast mode.  
  
 ![Air theme in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-themeair.png "Air theme in Unified Service Desk")  
  
### <a name="blue-theme"></a>Chủ đề màu xanh  
 Đây là chủ đề màu xanh. This theme doesn't support high-contrast setting, and is deprecated in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] 2.2 release. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Blog: Deprecating some predefined Unified Service Desk themes](https://blogs.msdn.microsoft.com/usd/2016/08/24/deprecating-some-predefined-unified-service-desk-themes/)  
  
 ![Blue theme in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-themeblue.png "Blue theme in Unified Service Desk")  
  
### <a name="style-theme"></a>Style Theme  
 This is the Style theme. This theme doesn't support high-contrast setting, and is deprecated in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] 2.2 release. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Blog: Deprecating some predefined Unified Service Desk themes](https://blogs.msdn.microsoft.com/usd/2016/08/24/deprecating-some-predefined-unified-service-desk-themes/)  
  
 ![Style theme in Unified Service Desk](../unified-service-desk/media/crmusd-theme-style.png "Style theme in Unified Service Desk")  
  
<a name="SetPredefinedTheme"></a>   
## <a name="set-a-predefined-theme"></a>Đặt chủ đề được xác định trước  
 Thao tác **SetTheme** cho kiểm soát tổ chức trình quản lý chung cho phép bạn thiết lập một chủ đề trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. You can create an action call to the **SetTheme** action, and pass the predefined theme call in the **Data** field using the following syntax to set one of the predefined themes:  
  
```  
/UnifiedServiceDesk;component/Styles/<Theme_Style>.xaml  
```  
  
 Bảng dưới đây cung cấp các cú pháp cho trường **dữ liệu** trong cuộc gọi hành động của bạn để thiết lập một chủ đề được xác định trước:  
  
|Chủ đề|Cú pháp cho trường dữ liệu|  
|-----------|-------------------------------|  
|Không khí|/UnifiedServiceDesk;component/Styles/AirStyle.XAML|  
|Màu xanh|/UnifiedServiceDesk;component/Styles/BlueStyle.xaml|  
|Kiểu|/UnifiedServiceDesk;component/Styles/Style.xaml|  
  
 Trong mẫu [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] ứng dụng khách, tổng đài viên có thể thiết lập chủ đề bằng cách nhấp vào mũi tên xuống bên cạnh biểu tượng cài đặt ở góc trên cùng bên phải, sau đó lựa chọn một chủ đề được xác định trước từ menu phụ **đặt chủ đề**.  
  
 Nhấn vào một chủ đề trong menu phụ **đặt chủ đề** sẽ thực hiện cuộc gọi hành động đến thao tác **SetTheme** với cú pháp thích hợp trong trường **dữ liệu** như đã đề cập trước đó. Ví dụ, đây là định nghĩa cuộc gọi hành động cho kiểu chủ đề về không khí:  
  
 ![Action call definition for Air theme](../unified-service-desk/media/crm-itpro-usd-actioncallforairstyle.png "Action call definition for Air theme")  
  
<a name="Customize"></a>   
## <a name="customize-themes-in-unified-service-desk"></a>Customize themes in Unified Service Desk  
 Ngoài việc có thể để lựa chọn từ nhiều chủ đề khác nhau được xác định trước, bạn có thể tùy chỉnh chủ đề trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. This is done by updating selective controls and then merging it with the existing theme in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] to customize the appearance. [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] provides a default style (XAML file) and a bunch of XAML brush resources that you can use to understand the various WPF controls and layout that define the appearance of your agent application. You can find the default style for [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] application, **DefaultStyle.xaml**, along with other XAML brush resources in the [!INCLUDE[pn_user_interface_integration](../includes/pn-user-interface-integration.md)] SDK download package. [Download](http://go.microsoft.com/fwlink/p/?LinkId=395257) the package, and extract it to view the file and its contents under the "UII\USD Developer Assets\USD Layout and Style Sheet" directory.  
  
> [!NOTE]
>  Ghi mã lệnh WPF và XAML là kỹ năng cần thiết cần thiết để tuỳ chỉnh hiển thị các ứng dụng tác nhân của bạn bằng cách thực hiện thao tác điều khiển trong tệp XAML.  
  
 Use the **SetTheme** action for the Global Manager hosted application to customize the default style of the agent application. [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] supports merging of your customizations with the existing theme or display style of the agent application. Điều này có hiệu quả có nghĩa là bạn chỉ cần xác định các điều khiển hoặc các khu vực mà bạn muốn thay đổi cùng với khối tham khảo ResourceDictionary để tùy chỉnh kiểu hiển thị sẵn có. For general information about ResourceDictionary, click [ResourceDictionary and XAML resource references](https://msdn.microsoft.com/library/windows/apps/Hh968442.aspx).  
  
 Hãy để chúng tôi tạo ra cuộc gọi thao tác để thay đổi văn bản trong tiêu đề và màu nền của ứng dụng tác nhân thành màu vàng. Đảm bảo rằng bạn có sẵn tệp DefaultStyle.xaml vì chúng tôi sẽ cần đến tệp đó.  
  
1. Đăng nhập vào ứng dụng Microsoft Dynamics 365 for Customer Engagement.  
  
2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  
  
3. Click **Action Calls**.  
  
4. Bấm vào **MỚI** để tạo cuộc gọi thao tác.  
  
5. Trên trang **Cuộc gọi thao tác mới**, đặt các thuộc tính chung:  
  
   1.  Trong trường **tên**, nhập **Cuộc gọi thao tác cho hiển thị tùy chỉnh**.  
  
   2.  In the **Hosted Control** field, select **Dynamics 365 for Customer Engagement apps Global Manager**. Nếu có một tên khác nhau cho loại kiểm soát tổ chức của trình quản lý chung của bạn, hãy chỉ định tên đó để thay thế.  
  
   3.  Trong trường **Thao tác**, chọn **SetTheme**.  
  
6. Bây giờ, chúng tôi sẽ đặt các tham số để tuỳ chỉnh màn hình. Trong trường **dữ liệu**, sao chép tài liệu tham khảo ResourceDictionary sau đây:  
  
   ```  
  
   <ResourceDictionary xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"  
        xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"  
        xmlns:Microsoft_Windows_Themes="clr-namespace:Microsoft.Windows.Themes;assembly=PresentationFramework.Classic"  
        xmlns:themes="clr-namespace:Microsoft.Windows.Themes;assembly=PresentationFramework.Luna"  
        xmlns:ribbon="clr-namespace:Microsoft.Windows.Controls.Ribbon;assembly=RibbonControlsLibrary"  
        xmlns:classic="clr-namespace:Microsoft.Windows.Themes;assembly=PresentationFramework.Classic"  
        xmlns:shell="clr-namespace:Microsoft.Windows.Shell;assembly=Microsoft.Windows.Shell"  
        xmlns:system="clr-namespace:System;assembly=mscorlib">  
   ```  
  
   > [!IMPORTANT]
   >  This `ResourceDictionary` reference must be included in every action call that you use to customize the default style.  
  
7. Sao chép các lệnh sau đây trong trường **dữ liệu** sau khi tài liệu tham khảo ResourceDictionary mà bạn đã sao chép trước đó.  
  
   ```  
   <SolidColorBrush x:Key="WindowBackgroundStyle" Color="Yellow"/>  
   ```  
  
    Điều này sẽ thay đổi màu nền của ứng dụng tác nhân sang màu vàng. You will find this command to set the background color in the `<!-- Region General -->` section in the `DefaultStyle.xaml` file.  
  
8. Sao chép lệnh sau đây sau lệnh mà bạn sao chép ở bước trước:  
  
   ```  
   <Style x:Key="MainWindow" TargetType="{x:Type Window}" BasedOn="{StaticResource {x:Type Window}}">  
       <Setter Property="Title" Value="CUSTOM TITLE: Agent Application for CONTOSO INC."/>  
       <Setter Property="Icon" Value="/UnifiedServiceDesk;component/imageResources/dynamics16-32-48-256.ico"/>  
       <Setter Property="FontFamily" Value="Segoe UI" />  
   </Style>  
   ```  
  
    Điều này sẽ thay đổi văn bản trong thanh tiêu đề "TÙY CHỈNH TIÊU ĐỀ: Ứng dụng tác nhân cho CONTOSO Inc". Bạn sẽ tìm thấy lệnh này để đặt tiêu đề cửa sổ trong `<!-- Region Window --> section in the DefaultStyle.xaml file.`  
  
9. Đóng thẻ ResourceDictionary bằng cách thêm mục sau vào cuối trường **dữ liệu**:  
  
    ```  
    </ResourceDictionary>  
    ```  
  
     Đây là cách xác định định nghĩa cuộc gọi thao tác:  
  
   ![Define action call for customizing display](../unified-service-desk/media/crm-itpro-usd-customizedisplay01.png "Define action call for customizing display")  
  
10. Bấm vào **Lưu**.  
  
    Bạn đã hoàn tất và bây giờ hãy sẵn sàng để thử nghiệm cuộc gọi thao tác trong ứng dụng tác nhân.  
  
<a name="Test"></a>   
## <a name="test-the-action-call-for-customizing-your-display"></a>Kiểm tra cuộc gọi hành động để tuỳ chỉnh màn hình của bạn  
 Bạn có thể gọi thao tác này bằng cách tạo nút thanh công cụ, sau đó gắn cuộc gọi hành động vào nút đó. Để đảm bảo ngắn gọn, chúng tôi sẽ sử dụng ứng dụng tổ chức trình gỡ lỗi để kiểm tra cuộc gọi hành động.  
  
1. Start [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to your Dynamics 365 for Customer Engagement server.  
  
2. Trong ứng dụng khách, bắt đầu trình gỡ lỗi bằng cách nhấp vào mũi tên xuống bên cạnh trình đơn cài đặt ở góc trên cùng bên phải, bấm vào **gỡ lỗi**.  
  
3. Trong trình gỡ lỗi, hãy nhấp vào mũi tên xuống trên tab **cuộc gọi hành động** để hiển thị các khu vực nơi bạn có thể kiểm tra cuộc gọi hành động và thao tác UII.  
  
   ![Test action calls & UII actions in debugger](../unified-service-desk/media/usd-customize-display-2.png "Test action calls & UII actions in debugger")  
  
4. From the **Action Calls** drop-down list, select **Action Call for Custom Theme**, and click the **Run Action Call** icon (![USD debugger Run Action Call button](../unified-service-desk/media/usd-run-action-call-icon.png "USD debugger Run Action Call button")). Thay đổi văn bản trong thanh tiêu đề và màu nền của ứng dụng tác nhân.  
  
   ![Customized display of the client application](../unified-service-desk/media/crm-itpro-usd-customizedisplay03.PNG "Customized display of the client application")  
  
   Để hoàn tác những thay đổi, chọn một trong các chủ đề được xác định trước trong các ứng dụng khách.  
  
<a name="HighContrast"></a>   
## <a name="high-contrast-mode-support--for-custom-themes"></a>High-contrast mode support  for custom themes  
 [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] internally uses normal and high-contrast mode XAML brush resources to display its UI elements depending on the high-contrast mode setting on your computer. You can find the XAML brush resources in the [!INCLUDE[pn_user_interface_integration](../includes/pn-user-interface-integration.md)] SDK download package. [Download](http://go.microsoft.com/fwlink/p/?LinkId=395257) the package, and extract it to view the file and its contents under the "UII\USD Developer Assets\USD Layout and Style Sheet" directory.  
  
 To support high-contrast mode in your custom themes, consider the following:  
  
-   Create two action calls for setting a custom theme: one for the *normal* mode and the other for the *high-contrast* mode. For example, while defining the color property of a XAML brush, use:  
  
    -   One of the predefined colors as defined in the [Colors](https://msdn.microsoft.com/en-us/library/system.windows.media.colors\(v=vs.110\).aspx) class for the *normal* mode:  
  
        ```  
        <SolidColorBrush x:Key="WindowBackgroundStyle" Color="Yellow"/>  
        ```  
  
    -   One of the system colors as defined in the [SystemColors](https://msdn.microsoft.com/en-us/library/system.windows.systemcolors.windowcolor\(v=vs.110\).aspx) class for the *high-contrast* mode:  
  
        ```  
        <SolidColorBrush x:Key="WindowBackgroundStyle" Color="{x:Static SystemColors.WindowColor}"/>  
        ```  
  
-   Use the new  `$SystemParameters.HighContrast` replacement parameter in each of your action call definition as a condition to ensure that a action call is fired appropriately. For example, in the action call definition for setting custom theme for:  
  
    -   The *normal* mode, use the following in the **Condition** field to check that the high-contrast mode is not set on your computer:  
  
        ```  
        "[[$SystemParameters.HighContrast]g]"=="False"  
        ```  
  
    -   The *high-contrast* mode, use the following in the **Condition** field to check that the high-contrast mode is set on your computer:  
  
        ```  
        "[[$SystemParameters.HighContrast]g]"=="True"  
        ```  
  
### <a name="see-also"></a>Xem thêm  
 [Customize themes for High Contrast settings](../unified-service-desk/customize-themes-in-unified-service-desk.md )   
 [Unified Service Desk Configuration Walkthroughs](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md)   
 [Sử dụng chủ đề để tùy chỉnh giao diện ứng dụng của bạn](../unified-service-desk/customize-appearance-application.md)   
 [Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)   
