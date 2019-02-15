---
title: 'Walkthrough: Create a UII Web Application Adapter in Unified Service Desk for Dynamics 365 for Customer Engagement apps | MicrosoftDocs'
description: Demonstrates how to host and interact with an external web application in Unified Service Desk.
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
ms.assetid: 0b4f5456-deef-41e9-ac58-13a2a0ce5de2
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 872fd24a73e15fd089a60c96aa836ee59525b061
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387614"
---
# <a name="walkthrough-create-a-uii-web-application-adapter"></a>Walkthrough: Create a UII Web Application Adapter
You can create a web application adapter if you want to enhance and modify web applications for which you don’t have access to the source code or don’t have permissions to change by using managed code. [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps provides a [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)] template for creating a web application adapter. Mẫu này cung cấp mã cơ bản như nhận xét để giúp bạn bắt đầu với việc tạo bộ chuyển đổi ứng dụng web.  

 Trong cách này, bạn sẽ xây dựng một ứng dụng web bên ngoài được gọi là `QsWebApplication` và lưu trữ nó trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. Sau đó, bạn sẽ tạo và cấu hình bộ chuyển đổi ứng dụng web được gọi là `MyWebApplicationAdapter` cho ứng dụng web bên ngoài để tương tác với [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. Ứng dụng web có bốn nhãn, mỗi nhãn cho tên, họ, địa chỉ và ID của khách hàng và bốn hộp văn bản tương ứng để hiển thị các giá trị [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].  

<a name="Prereq"></a>   
## <a name="prerequisites"></a>Điều kiện tiên quyết  

- [!INCLUDE[pn_Microsoft_.Net_Framework](../includes/pn-microsoft-net-framework.md)] 4.5.2  

- [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application; required for testing the hosted control.  

- [!INCLUDE[pn_microsoft_visual_studio_2012](../includes/pn-microsoft-visual-studio-2012.md)], [!INCLUDE[pn_visual_studio_2013](../includes/pn-visual-studio-2013.md)], or [!INCLUDE[pn_visual_studio_2015](../includes/pn-visual-studio-2015.md)]  

- [!INCLUDE[tn_nuget_package_manager](../includes/tn-nuget-package-manager.md)] for [Visual Studio 2012](http://visualstudiogallery.msdn.microsoft.com/27077b70-9dad-4c64-adcf-c7cf6bc9970c), [Visual Studio 2013](http://visualstudiogallery.msdn.microsoft.com/4ec1526c-4a8c-4a84-b702-b21a8f5293ca), or [Visual Studio 2015](https://visualstudiogallery.msdn.microsoft.com/5d345edc-2e2d-4a9c-b73b-d53956dc458d)  

- **CRM SDK Templates** for [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] that contains the UII hosted control project template. [Download](http://go.microsoft.com/fwlink/p/?LinkId=400925) the **CRM SDK Templates** from the Visual Studio gallery, and double-click the CRMSDKTemplates.vsix file to install the template in [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)].  

<a name="Build"></a>   
## <a name="step-1-build-a-sample-web-application"></a>Bước 1: Xây dựng một ứng dụng web mẫu  

1. [Tải xuống gói UII SDK (.exe)](http://go.microsoft.com/fwlink/p/?LinkId=519179)  

2. Bấm đúp vào tệp gói để giải nén nội dung.  

3. Navigate to the \<ExtractedFolder>\UII\SampleCode\UII\AIF\QsWebApplication folder, and open the Microsoft.Uii.QuickStarts.QsWebApplication.csproj file in [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)].  

4. Press F5 or choose **Debug** > **Start Debugging** to host the sample web application locally on your computer. The application will be hosted at http://localhost:2627/.  

   ![Web app in Visual Studio](../unified-service-desk/media/usd-web-app-local-host.png "Web app in Visual Studio")  

<a name="ConfigureExApp"></a>   
## <a name="step-2-configure-the-web-application-in-dynamics-365-for-customer-engagement-apps"></a>Step 2: Configure the web application in Dynamics 365 for Customer Engagement apps

1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. Chọn **Kiểm soát Tổ chức**.  

4. Chọn **Mới**.  

5. On the **New Hosted Control** page, specify the following values.  


   |           Trường            |                                                 Value                                                 |
   |----------------------------|-------------------------------------------------------------------------------------------------------|
   |          **Tên**          |                                           QsWebApplication                                            |
   |   **Loại thành phần USD**   |                                        CCA Hosted Application                                         |
   |   **Ứng dụng được lưu trữ**   |                                        Ứng dụng web được lưu trữ                                         |
   | **Ứng dụng toàn cầu**  |                                                Đã kiểm tra                                                |
   |     **Nhóm hiển thị**      |                                               Bảng điều khiển chính                                               |
   |        **Bộ điều hợp**         |                                            Không sử dụng bộ điều hợp                                             |
   | **Ứng dụng động** |                                                  No                                                   |
   |  **Lưu trữ ứng dụng**   |                                             Sử dụng SetParent                                             |
   |          **URL**           | Xác định vị trí nơi ứng dụng web của bạn được tổ chức. Trong trường hợp này, đây là http://localhost:2627/ |

   ![Screenshot of Web App Config in Dynamics 365 for Customer Engagement apps](../unified-service-desk/media/usd-web-app-crm-config.png "Screenshot of Web App Config in Dynamics 365 for Customer Engagement apps")  

6. Chọn **Lưu**.  

<a name="TestExApp"></a>   
## <a name="step-3-test-the-web-application"></a>Bước 3: Kiểm tra ứng dụng web  

1. Đảm bảo rằng ứng dụng web mẫu bạn xây dựng trong bước 1 vẫn đang chạy.  

2. Chạy ứng dụng khách [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] để kết nối với máy chủ **Microsoft Dynamics 365 for Customer Engagement** của bạn.  

3. Trên lần đăng nhập thành công, bạn sẽ nhìn thấy **Ứng dụng Web Bên ngoài Mẫu** trên máy tính để bàn của mình.  

4. Bấm vào tab **Ứng dụng Web Bên ngoài Mẫu **để xem ứng dụng web của bạn có được tổ chức trong **Unified Service Desk** hay không.  

   ![Hosting web app in Unified Service Desk](../unified-service-desk/media/usd-web-app-hosting.PNG "Hosting web app in Unified Service Desk")  

> [!NOTE]
>  Tại thời điểm này, các trường này trống vì bạn chỉ đang lưu trữ ứng dụng web bên ngoài trong **Unified Service Desk**. Để đưa vào các giá trị từ **Unified Service Desk**, chúng ta phải tạo ra một bộ chuyển đổi ứng dụng web như minh họa trong bước tiếp theo.  

<a name="createappadapter"></a>   
## <a name="step-4-create-the-web-application-adapter"></a>Bước 4: Tạo các bộ chuyển đổi ứng dụng web  

1. Bắt đầu [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)] và tạo một dự án mới.  

2. Trong hộp thoại **Dự án mới**:  

   1. From the list of installed templates on the left, expand [!INCLUDE[pn_Visual_C#](../includes/pn-visual-csharp.md)], and select **Dynamics 365 for Customer Engagement apps SDK Templates** > **Unified Service Desk** > **UII Web Application Adapter**.  

   2. Specify the name and location of the project, and click **OK** to create a new project.  

   ![Screenshot of Web Adapter in Visual Studio](../unified-service-desk/media/usd-web-app-adapter-vs.PNG "Screenshot of Web Adapter in Visual Studio")  

   3. Choose WebAppAdapter.cs and update the definition of **NotifyContextChange** with the following code to populate the text fields from the context information. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Context)](https://docs.microsoft.com/dotnet/api/microsoft.uii.csr.hostedapplicationadapter.notifycontextchange\(microsoft.uii.csr.context\))  

      ```csharp  
      public override bool NotifyContextChange(Context context)  
              {  
                  // Populating text fields from context information.  

                  HTMLDocument htmlDoc = Browser.Document as HTMLDocument;  
                  if (htmlDoc != null)  
                  {  
                      IHTMLElementCollection htmlElementCollection = htmlDoc.all;  
                      IHTMLElement htmlFirstName = htmlElementCollection.item("txtFirstName", 0) as IHTMLElement;  
                      htmlFirstName.setAttribute("value", context["firstname"], 0);  
                      IHTMLElement htmlLastName = htmlElementCollection.item("txtLastName", 0) as IHTMLElement;  
                      htmlLastName.setAttribute("value", context["lastname"], 0);  
                      IHTMLElement htmlAddress = htmlElementCollection.item("txtAddress", 0) as IHTMLElement;  
                      htmlAddress.setAttribute("value", context["address1_line1"], 0);  
                      IHTMLElement htmlID = htmlElementCollection.item("txtID", 0) as IHTMLElement;  
                      htmlID.setAttribute("value", context["CustomerID"], 0);  
                  }  
                  return base.NotifyContextChange(context);  
              }  

      ```  

   4. Thêm mã sau vào định nghĩa ghi đè của **DoAction** để cập nhật ứng dụng với các giá trị từ [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]  

      ```csharp  
      public override bool DoAction(HostedWebApplication.WebAction action, ref string data)  
              {  
                  Trace.WriteLine(string.Format("{0}>>>>> RECEIVED (WebAction) Action : {1} ", this.Name, action.Name));  

                  // Check to see if the browser is working on something before allowing the system to do 'normal' behavior.  
                  if (Browser.WebBrowser.ReadyState != tagREADYSTATE.READYSTATE_COMPLETE)  
                  {  
                      // Browser is not in a state to process this request,  Queue it for when the browser is ready to handle it.   
                      Trace.WriteLine(string.Format("{0}>>>>> Browser Busy,({2}) Queuing Action : {1} ", this.Name, action.Name, Browser.WebBrowser.ReadyState.ToString()));  
                      qReqActionList.Enqueue(new BrowserActionData(action, data));  
                      return false;  
                  }  
                Trace.WriteLine(string.Format("{0}>>>>>>>>>>> Action:Name={1} Action:Url={2} Action:Query={3} Action:Init={4}", this.Name, action.Name, action.Url, action.QueryString, action.Initialization));  

                  // Get browser DOM and element collection.  
                  // Create an XML Document to load the passed in data to.  
                  HTMLDocument htmlDoc = Browser.Document as HTMLDocument;  
                  IHTMLElementCollection htmlElementCollection = htmlDoc.all;  

                  // Check action name for something we know how to process.  
                  switch (action.Name)  
                  {  
                      case "UpdateFirstName":  
                          IHTMLElement htmlFirstName = htmlElementCollection.item("txtFirstName", 0) as IHTMLElement;  
                          htmlFirstName.setAttribute("value", data, 0);  
                          break;  
                      case "UpdateLastName":  
                          IHTMLElement htmlLastName = htmlElementCollection.item("txtLastName", 0) as IHTMLElement;  
                          htmlLastName.setAttribute("value", data, 0);  
                          break;  
                      case "UpdateAddress":  
                          IHTMLElement htmlAddress = htmlElementCollection.item("txtAddress", 0) as IHTMLElement;  
                          htmlAddress.setAttribute("value", data, 0);  
                          break;  
                      case "UpdateID":  
                          IHTMLElement htmlID = htmlElementCollection.item("txtID", 0) as IHTMLElement;  
                          htmlID.setAttribute("value", data, 0);  
                          break;  
                  }  
                  return false;  
              }  

      ```  

   5. Save your project, and build it (**Build** > **Build Solution**). After the project builds successfully, an assembly (MyWebApplicationAdapter.dll) is generated in the \bin\debug folder of your project folder. Bạn sẽ cần lắp ráp cụm tổ hợp này sau để thử nghiệm và sử dụng bộ chuyển đổi ứng dụng web của bạn.  

<a name="ConfigureWebAdapter"></a>   
## <a name="step-5-configure-the-web-application-adapter-in-dynamics-365-for-customer-engagement-apps"></a>Step 5: Configure the web application adapter in Dynamics 365 for Customer Engagement apps  

1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  

2. On the nav bar, choose **Microsoft Dynamics 365 for Customer Engagement**, and then select **Settings**.  

3. Choose **Settings** > **Unified Service Desk** > **Hosted Controls**.  

4. Từ danh sách kiểm soát tổ chức, chọn kiểm soát được tổ chức **QsWebApplication**.  

   ![Hosted controls list in Dynamics 365 for Customer Engagement apps](../unified-service-desk/media/usd-web-app-hosted-controls-list.PNG "Hosted controls list in Dynamics 365 for Customer Engagement apps")  

5. Trong phần **Cấu hình Bộ chuyển đổi**, chỉ định các giá trị sau.  

   |**Trường**|Value|  
   |---------------|-----------|  
   |**Bộ điều hợp**|Sử dụng bộ điều hợp|  
   |**URI**|MyWebApplicationAdapter|  
   |Loại|MyWebApplicationAdapter.WebAppAdapter|  

   ![Web adapter configuration in Dynamics 365 for Customer Engagement apps](../unified-service-desk/media/usd-web-app-adapter-config.PNG "Web adapter configuration in Dynamics 365 for Customer Engagement apps")  

   > [!NOTE]
   > **URI** là tên của cụm tổ hợp của bạn và **Loại** là tên của cụm tổ hợp của bạn (dll) theo sau bởi dấu chấm (.) sau đó là tên lớp trong dự án [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] của bạn. In this example, the name of the assembly is MyWebApplicationAdapter and name of the class is WebAdapter, which is the default class name when you create a web application adapter.  

6. Chọn **Lưu** để lưu các thay đổi.  

<a name="TestAppAdapter"></a>   
## <a name="step-6-test-the-web-application-adapter"></a>Bước 6: Thử nghiệm bộ chuyển đổi ứng dụng web  

1. Copy the assembly that contains your web application adapter definition from your [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] project output folder (\<ProjectFolder>\bin\debug) to the Unified Service Desk application directory. In this case, you’ll copy the MyWebApplicationAdapter.dll file to the c:\Program Files\Microsoft Dynamics CRM USD\USD directory.  

2. Run the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client to connect to your [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps server.  

3. Trên lần đăng nhập thành công, bạn sẽ nhìn thấy nút ứng dụng web bên ngoài mẫu trên máy tính để bàn của mình.  

4. Chọn **Tìm kiếm** rồi sau đó chọn **Người liên hệ** và chọn một người liên hệ. Trong trường hợp này, chọn **Patrick Sands**.  

   ![Screenshot of contact list](../unified-service-desk/media/usd-web-app-adapter-contacts-list.PNG "Screenshot of contact list")  

5. Bấm vào **Ứng dụng Web Bên Ngoài Mẫu** và bạn sẽ nhìn thấy tên, họ, địa chỉ và ID của khách hàng được điền vào.  

   ![Testing WebApp Adapter screenshot](../unified-service-desk/media/usd-web-app-adapter-test.PNG "Testing WebApp Adapter screenshot")  

> [!NOTE]
>  Cách này cho bạn thấy cách đọc hoặc hiển thị dữ liệu từ [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] trong ứng dụng web bên ngoài. To update the data in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] from the external web application, and vice versa, see [Walkthrough: Create a UII Windows Forms Hosted Control](../unified-service-desk/walkthrough-create-uii-windows-forms-hosted-control.md)  

### <a name="see-also"></a>Xem thêm  
 [Use UII adapters to interact with external and web applications](../unified-service-desk/use-uii-adapters-interact-external-web-applications.md)
