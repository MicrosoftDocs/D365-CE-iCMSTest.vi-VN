---
title: 'Walkthrough: Create custom hosted control for Unified Service Desk | MicrosoftDocs'
description: Learn about how to create a custom hosted control for Unified Service Desk.
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
ms.assetid: 7d184ce7-ba95-46ea-9219-67fd6821eba5
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 42b01a41f2d57225af64779f844459c2952e6fc5
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385845"
---
# <a name="walkthrough-create-custom-hosted-control-for-unified-service-desk"></a>Walkthrough: Create custom hosted control for Unified Service Desk
Trong chủ đề này, bạn sẽ tìm hiểu cách tạo kiểm soát tổ chức tùy chỉnh được gọi là `My Custom Control` với hành động tùy chỉnh. The custom hosted control has two [!INCLUDE[pn_ms_Windows_Presentation_Foundation](../includes/pn-ms-windows-presentation-foundation.md)] controls: a button that calls the Debugger hosted control and a text label that displays the user name when a custom action, `MyCustomAction`, is called.  
  
## <a name="in-this-section"></a>In This Section  
 [Điều kiện tiên quyết](../unified-service-desk/walkthrough-create-custom-hosted-control-for-unified-service-desk.md#Prereq)  
  
 [Tạo kiểm soát tổ chức tùy chỉnh](../unified-service-desk/walkthrough-create-custom-hosted-control-for-unified-service-desk.md#HowTo)  
  
 [Kiểm tra kiểm soát tổ chức tùy chỉnh của bạn](../unified-service-desk/walkthrough-create-custom-hosted-control-for-unified-service-desk.md#Test)  
  
<a name="Prereq"></a>   
## <a name="prerequisites"></a>Điều kiện tiên quyết  
  
- [!INCLUDE[pn_Microsoft_.Net_Framework](../includes/pn-microsoft-net-framework.md)] 4.5.2  
  
- Ứng dụng khách [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]; ứng dụng khách là bắt buộc để thử nghiệm kiểm soát tổ chức  
  
- [!INCLUDE[pn_microsoft_visual_studio_2012](../includes/pn-microsoft-visual-studio-2012.md)], [!INCLUDE[pn_visual_studio_2013](../includes/pn-visual-studio-2013.md)], hoặc [!INCLUDE[pn_visual_studio_2015](../includes/pn-visual-studio-2015.md)]  
  
- [!INCLUDE[tn_nuget](../includes/tn-nuget.md)] Package Manager for [Visual Studio 2012](http://visualstudiogallery.msdn.microsoft.com/27077b70-9dad-4c64-adcf-c7cf6bc9970c), [Visual Studio 2013](http://visualstudiogallery.msdn.microsoft.com/4ec1526c-4a8c-4a84-b702-b21a8f5293ca), or [Visual Studio 2015](https://visualstudiogallery.msdn.microsoft.com/5d345edc-2e2d-4a9c-b73b-d53956dc458d)  
  
- **CRM SDK Templates** for [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] that contains the custom hosted control project template. [Download](http://go.microsoft.com/fwlink/p/?LinkId=400925) the **CRM SDK Templates** from the Visual Studio gallery, and double-click the CRMSDKTemplates.vsix file to install the template in [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)].
  
<a name="HowTo"></a>   
## <a name="create-a-custom-hosted-control"></a>Tạo kiểm soát tổ chức tùy chỉnh  
  
<a name="Step1"></a>   
1. Bắt đầu [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] và tạo một dự án mới.  
  
2. Trong hộp thoại **Dự án mới**:  
  
   1. From the list of installed templates, expand **Visual C#**, and select **CRM SDK Templates** > **Unified Service Desk** > **USD Custom Hosted Control**.  
  
   2. Đảm bảo rằng **[!INCLUDE[pn_NET_Framework](../includes/pn-net-framework.md)] 4.5.2** được chọn.  
  
   3. Chỉ định tên và vị trí của dự án, và bấm vào **OK** để tạo ra một dự án mới.  
  
   ![Template for creating a custom hosted control](../unified-service-desk/media/crm-itpro-usd-customhostedcontrol01.png "Template for creating a custom hosted control")  
  
3. In **Solution Explorer**, double-click the USDControl.xaml file to bring up the XAML designer.  
  
4. Trong trình thiết kế, thêm kiểm soát sau từ **Hộp công cụ**:  
  
   - **Label**: In the **Properties** pane, set the name of the control to “myLabel.”  
  
   - **Button**: In the **Properties** pane, set the name of the control to “myButton,” and the content to “**Start Debugger**.”  
  
     This is how the controls look in the XAML designer.  
  
   ![XAML designer with custom controls](../unified-service-desk/media/crm-itpro-usd-customhostedcontrol02.png "XAML designer with custom controls")  
  
5. Bấm đúp vào nút này để thêm mã sau XAML. Điều này sẽ đưa bạn đến định nghĩa sự kiện nhấp chuột của Nút của tôi trong tệp USDControl.xaml.cs. Thêm lệnh sau.  
  
   ```csharp  
   private void myButton_Click(object sender, RoutedEventArgs e)  
   {  
       if (!this.desktopAccess.AppExistsInUI("Debugger"))  
       {  
           this.desktopAccess.CreateDynamicApplication("Debugger");  
       }  
       this.FireRequestAction(new Microsoft.Uii.Csr.RequestActionEventArgs("Debugger", "default", null));  
   }  
   ```  
  
6. Xác định hành động tùy chỉnh cho kiểm soát tổ chức. In the USDControl.xaml.cs file, browse to the override definition of `DoAction`.  
  
   ```csharp  
   protected override void DoAction(Microsoft.Uii.Csr.RequestActionEventArgs args)  
   ```  
  
7. Thêm mã sau bên trong định nghĩa thay thế của `DoAction` để xác định hành động tùy chỉnh gọi là `MyCustomAction`, chấp nhận tham số có tên `username`.  
  
   ```csharp  
   if (args.Action.Equals("MyCustomAction", StringComparison.OrdinalIgnoreCase))  
   {  
       List<KeyValuePair<string, string>> actionDataList = Utility.SplitLines(args.Data, CurrentContext, localSession);  
       string valueIwant = Utility.GetAndRemoveParameter(actionDataList, "username"); // assume there is a myKey=<value> in the data.  
  
       if (!string.IsNullOrEmpty(valueIwant))  
       {  
           this.Dispatcher.Invoke(() => { this.myLabel.Content = valueIwant; });  
       }  
   }  
   ```  
  
   > [!TIP]
   >  Mẫu này cung cấp hầu hết các mã như nhận xét bên trong định nghĩa thay thế của `DoAction` để giúp bạn nhanh chóng bắt đầu phát triển. Bạn cần phải bỏ ghi chú dòng mã yêu cầu và thay thế giá trị trình giữ chỗ bằng giá trị của mình.  
  
8. Save your project, and build it (**Build** > **Build Solution**) to verify that it builds successfully.  
  
<a name="Test"></a>   
## <a name="test-your-custom-hosted-control"></a>Kiểm tra kiểm soát tổ chức tùy chỉnh của bạn  
 Sau khi dự án của bạn được tạo dựng thành công, hãy kiểm tra kiểm soát tổ chức tùy chỉnh. Thử nghiệm bao gồm hai phần: xác định kiểm soát tổ chức tùy chỉnh trên máy chủ rồi sau đó kết nối với [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] trên máy chủ bằng cách sử dụng ứng dụng khách của bạn.  
  
### <a name="define-the-custom-hosted-control-and-action-on-the-dynamics-365-for-customer-engagement-server"></a>Define the custom hosted control and action on the Dynamics 365 for Customer Engagement server  
  
1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  
  
2. Trên thanh điều hướng, chọn **Microsoft Dynamics 365 for Customer Engagement** và chọn **Thiết đặt**.  
  
3. Choose **Settings** > **Unified Service Desk** > **Hosted Controls**.  
  
4. Chọn **MỚI** rồi chỉ định các giá trị trong màn hình **Kiểm soát Tổ chức Mới** như được hiển thị tại đây.  
  
   ![New custom hosted control](../unified-service-desk/media/crm-itpro-usd-customhostedcontrol03.png "New custom hosted control")  
  
   > [!NOTE]
   > **URI Cụm** là tên của cụm của bạn và **Loại cụm** là tên của cụm (dll) theo sau là một dấu chấm (.) và sau đó tên lớp trong dự án [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] của bạn. Trong ví dụ này, tên của cụm là **Kiểm soát tùy chỉnh của tôi** và tên của các lớp là **Kiểm soát USD**, chính là tên lớp mặc định khi bạn tạo kiểm soát tổ chức tùy chỉnh.  
  
5. Chọn **Lưu** để tạo kiểm soát tổ chức.  
  
6. Create the action for the hosted control that you defined in Visual Studio. Trên thanh điều hướng, chọn mũi tên xuống bên cạnh tên kiểm soát tổ chức của bạn và chọn **Hành động UII**.  
  
7. Chọn **Thêm Hành động UII Mới**.  
  
8. Nhập **MyCustomAction** vào trường **tên** và chọn **Lưu**.  
  
   You have now configured your custom hosted control and custom action on your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps server.  
  
<a name="Run"></a>   
### <a name="run-the-unified-service-desk-client-to-work-with-custom-hosted-control"></a>Chạy ứng dụng Unified Service Desk để hoạt động với kiểm soát tổ chức tùy chỉnh  
  
1. Copy the assembly that contains your custom hosted control definition from your [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] project output folder (\<*ProjectFolder*>\bin\debug) to the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] application directory. In this case, you’ll copy the MyCustomControl.dll file to the c:\Program Files\Microsoft Dynamics CRM USD\USD directory.  
  
2. Run [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client to connect to your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps server.  
  
3. Khi đăng nhập thành công, bạn sẽ thấy kiểm soát tổ chức tùy chỉnh, **Kiểm soát tổ chức tùy chỉnh của tôi**, trong máy tính của bạn.  
  
   ![Custom hosted control](../unified-service-desk/media/crm-itpro-usd-customhostedcontrol04.png "Custom hosted control")  
  
4. Bấm vào **bắt đầu trình gỡ lỗi** để khởi động kiểm soát tổ chức trình gỡ lỗi.  
  
5. Để kiểm tra hành động tùy chỉnh, chọn tab **Trình gỡ lỗi** rồi bấm vào mũi tên xuống phía trên tab **Cuộc gọi Hành động** để hiển thị khu vực nơi bạn có thể kiểm tra cuộc gọi hành động và hành động [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)].  
  
   ![Expanded testing area in debugger](../unified-service-desk/media/crm-itpro-usd-customhostedcontroldebugger.png "Expanded testing area in debugger")  
  
6. Chọn tab **Hành động Trực tiếp**.  
  
7. Từ danh sách **Kiểm soát tổ chức**, chọn **Kiểm soát tổ chức tùy chỉnh của tôi**, và từ danh sách **hành động**, chọn **Hành động tùy chỉnh của tôi**.  
  
8. Theo định nghĩa hành động tùy chỉnh, cuộc gọi hành động này giả sử tham số có tên `username`, do đó hãy thêm giá trị sau vào trường **Dữ liệu**: **username=Tracie Hamilton**.  
  
   ![Test your custom hosted control](../unified-service-desk/media/crm-itpro-usd-custhostedcontrol01.png "Test your custom hosted control")  
  
9. Click the **Run Direct Action** icon (![Unified Service Desk debugger Run Action Call button](../unified-service-desk/media/usd-run-action-call-icon.png "Unified Service Desk debugger Run Action Call button")), and then click the **My Custom Hosted Control** tab. The specified user name is displayed in the label field.  
  
   ![My Custom Host Control tab shows username](../unified-service-desk/media/crm-itpro-usd-custhostedcontrol02.png "My Custom Host Control tab shows username")
  
### <a name="see-also"></a>Xem thêm  
 [Kiểm soát tổ chức USD (Kiểm soát tổ chức)](../unified-service-desk/usd-hosted-control-hosted-control.md)  
 [Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)   
 [Unified Service Desk Configuration Walkthroughs](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md)   
 [Use custom hosted control in Unified Service Desk](../unified-service-desk/use-custom-hosted-control-unified-service-desk.md)
