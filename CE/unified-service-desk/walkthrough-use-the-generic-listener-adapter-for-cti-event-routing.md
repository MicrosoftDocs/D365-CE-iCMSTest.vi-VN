---
title: 'Walkthrough: Use the generic listener adapter for CTI event routing | MicrosoftDocs'
description: Learn about using the CTI Desktop Manager and generic listener in to expose the CTI events as screen pops in Unified Service Desk.
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
ms.assetid: d6013727-b00e-4671-97c6-f0c0600da980
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 23cc3e9743188e5ddfd014e639524c7481a1bdc7
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386189"
---
# <a name="walkthrough-use-the-generic-listener-adapter-for-cti-event-routing"></a>Walkthrough: Use the generic listener adapter for CTI event routing
Cách này trình bày cách bạn có thể sử dụng Trình quản lý Màn hình nền CTI và trình nghe chung trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] để hiển thị các sự kiện CTI dưới dạng mục bật lên trên màn hình trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. Đối với cách này, chúng ta sẽ sử dụng ứng dụng Trình mô phỏng CTI mẫu gửi yêu cầu CTI tới [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].  
  
 In this walkthrough, you’ll:  
  
- Search for a contact record in the sample [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps data based on an email address specified in the sample CTI Call Tester application.  
  
- Tạo quy tắc điều hướng cửa sổ để hiển thị bản ghi phù hợp trong phiên trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].  
  
<a name="Prereq"></a>   
## <a name="prerequisites"></a>Điều kiện tiên quyết  
  
- [!INCLUDE[pn_Microsoft_.Net_Framework](../includes/pn-microsoft-net-framework.md)] 4.5.2  
  
- [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] ứng dụng khách, được yêu cầu để thử nghiệm kiểm soát tổ chức.  
  
- [!INCLUDE[pn_microsoft_visual_studio_2012](../includes/pn-microsoft-visual-studio-2012.md)] hoặc [!INCLUDE[pn_visual_studio_2013](../includes/pn-visual-studio-2013.md)]  
  
- [Download the sample CTI Simulator Application Visual Studio project to your computer](http://go.microsoft.com/fwlink/p/?LinkId=519007). Build the project, and run the application (.exe file) from the bin\debug folder of the sample application project. Bạn phải chạy ứng dụng Trình mô phỏng USD CTI trên cùng một máy tính nơi ứng dụng khách [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] đang chạy để kiểm tra các ứng dụng.  
  
<a name="step1"></a>   
## <a name="step-1-configure-a-cti-desktop-manager-hosted-control-in-unified-service-desk"></a>Bước 1: Đặt cấu hình kiểm soát tổ chức Trình quản lý Màn hình nền CTI trong Unified Service Desk  
  
1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  
  
2. On the nav bar, choose **Microsoft Dynamics 365 for Customer Engagement** > **Settings** > **Unified Service Desk**.  
  
3. On the **Unified Service Desk** page, choose **Hosted Controls**.  
  
4. Trên trang **Kiểm soát Tổ chức**, chọn **Mới**.  
  
5. On the **New Hosted Control** page, specify the following values.  
  
   |Trường|Value|  
   |-----------|-----------|  
   |Tên|CTITest|  
   |USD Component Type|Trình quản lý Màn hình nền CTI|  
   |Nhóm hiển thị|Bảng điều khiển bị ẩn|  
   |URI cụm tổ hợp|Microsoft.Crm.UnifiedServiceDesk.GenericListener|  
   |Loại cụm tổ hợp|Microsoft.Crm.UnifiedServiceDesk.GenericListener.DesktopManager|  
  
   > [!NOTE]
   >  Các giá trị được chỉ định trong các trường **URI Cụm tổ hợp** và **Loại Cụm tổ hợp** là các giá trị trình nghe chung cho loại kiểm soát tổ chức **Trình quản lý Màn hình nền CTI**.  
  
   ![Configure CTI Dekstop Manager hosted control](../unified-service-desk/media/usd-cti-desktop-manager.png "Configure CTI Dekstop Manager hosted control")  
  
6. Bấm vào **Lưu** để tạo kiểm soát tổ chức.  
  
<a name="step2"></a>   
## <a name="step-2-test-if-the-cti-events-are-raised-in-unified-service-desk"></a>Bước 2: Kiểm tra xem các sự kiện CTI có được nêu trong Unified Service Desk không  
  
1. Start [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client, and connect to your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance. After the client is up, choose **Settings**![Gear button](../unified-service-desk/media/crm-ua-selection-rule-gear.gif "Gear button") in the top-right corner to display the debugger control, and then choose **Clear Debug Output**![Delete button](../unified-service-desk/media/crm-ua-delete.gif "Delete button") to clear the desktop.  
  
   ![Unified Service Desk client](../unified-service-desk/media/usd-usdclientwithdebugger.png "Unified Service Desk client")  
  
2. Bắt đầu ứng dụng Trình mô phỏng USD CTI, nhập **Email** vào cột **Phím** và chỉ định một giá trị ngẫu nhiên trong cột **Giá trị**. Bấm **Gửi tới USD**.  
  
   ![Unified Service Desk CTI Simulator](../unified-service-desk/media/usd-ctistimulator.png "Unified Service Desk CTI Simulator")  
  
3. Màn hình cửa sổ bật lên xuất hiện trong ứng dụng khách để hiển thị sự kiện CTI. Trong trường hợp này, `CTILookUpRequest` được khởi tạo với giá trị được chỉ định trong ứng dụng Trình mô phỏng USD CTI. Bởi vì bạn chưa ghép với một quy tắc điều hướng cửa sổ, sẽ không có gì khác xảy ra.  
  
   ![Screen pop in for the CTI event](../unified-service-desk/media/usd-usdclientwithctievent.png "Screen pop in for the CTI event")  
  
<a name="step3"></a>   
## <a name="step-3-define-a-window-navigation-rule-to-route-the-ctilookuprequest"></a>Bước 3: Xác định một quy tắc điều hướng cửa sổ để định tuyến CtiLookUpRequest  
 Tạo một quy tắc điều hướng cửa sổ để tạo phiên nếu tìm thấy giá trị phù hợp, sau đó hiển thị bản ghi liên hệ phù hợp trong một phiên trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]  
  
1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  
  
2. Navigate to the advanced find for contacts, and create a query where you search for active contacts where the email, email address 2, or email address 3 field equals a certain value, for example, someone_c@example.com.  
  
   ![Query for contacts based on email address](../unified-service-desk/media/usd-contactsadvancedfind.png "Query for contacts based on email address")  
  
3. Bấm **Tải xuống Fetch XML** để lưu truy vấn làm `FetchXML`.  
  
4. On the nav bar, choose **Microsoft Dynamics 365 for Customer Engagement** > **Settings** > **Unified Service Desk** > **Window Navigation Rules**.  
  
5. Bấm **Mới** và trên cửa sổ **Quy tắc Điều hướng Cửa sổ Mới**, hãy chỉ định các giá trị sau.  
  
   |Trường|Value|  
   |-----------|-----------|  
   |Tên|CTITestRoute|  
   |Thứ tự|50|  
   |Từ|CTITest<br /><br /> Đây là tên của kiểm soát tổ chức Trình quản lý Màn hình nền CTI.|  
   |Hướng|Cả hai|  
  
   ![New window navigation rule for routing CTI event](../unified-service-desk/media/usd-cti-route-rule.png "New window navigation rule for routing CTI event")  
  
6. Lưu quy tắc. Điều này cho phép phần còn lại trên trang này.  
  
7. Bây giờ, thêm truy vấn `FetchXML` đã được lưu trước đây vào quy tắc này. Under the **CTI Searches** area, choose Add ![Add a record button](../unified-service-desk/media/crm-ua-add-record.gif "Add a record button").  
  
8. In the **New CTI Search** window, specify the following values:  
  
   - **Name**: CTIContactSearch  
  
   - **Order**: 1  
  
   - **FetchXML**:  
  
       ```xml  
  
       <fetch version="1.0" output-format="xml-platform" mapping="logical" distinct="false">  
         <entity name="contact">  
           <attribute name="fullname" />  
           <attribute name="parentcustomerid" />  
           <attribute name="telephone1" />  
           <attribute name="emailaddress1" />  
           <attribute name="contactid" />  
           <order attribute="fullname" descending="false" />  
           <filter type="and">  
             <condition attribute="statecode" operator="eq" value="0" />  
             <filter type="or">  
               <condition attribute="emailaddress1" operator="eq" value="[[cti.Email]]" />  
               <condition attribute="emailaddress2" operator="eq" value="[[cti.Email]]" />  
               <condition attribute="emailaddress3" operator="eq" value="[[cti.Email]]" />  
             </filter>  
           </filter>  
         </entity>  
       </fetch>  
       ```  
  
     > [!NOTE]
     >  The address someone_c@example.com was replaced with `[[cti.Email]]` so that the search is run based on the value specified for the **Email** key in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] CTI Simulator application.  
  
   ![Define a CTI search for contacts](../unified-service-desk/media/usd-contactctisearch.png "Define a CTI search for contacts")  
  
9. Lưu quy tắc tìm kiếm CTI và trả lại quy tắc điều hướng cửa sổ.  
  
10. Trong **Một Kết quả phù hợp**, trong trường **Quyết định**, chọn **Tạo Phiên, Tải Kết quả phù hợp rồi Hành động**.  
  
11. Trong **Một Kết quả phù hợp**, trong trường **Hành động**, bấm vào biểu tượng tìm kiếm để chọn một giá trị rồi bấm vào **Mới**.  
  
12. Trên trang **Cuộc gọi Hành động Mới**, tạo cuộc gọi hành động để mở bản ghi liên hệ bằng cách chỉ định các giá trị sau.  
  
    |Trường|Value|  
    |-----------|-----------|  
    |Tên|CTIOpenContact|  
    |Kiểm soát được lưu trữ|Dynamics 365 for Customer Engagement apps Global Manager|  
    |Hành động|Open_CRM_Page|  
    |Dữ liệu|Id=[[$Context.Id]]<br />LogicalName=[[$Context.LogicalName]]|  
  
    ![Configure an action to display contact](../unified-service-desk/media/usd-ctiopencontact.png "Configure an action to display contact")  
  
13. Lưu cuộc gọi hành động, rồi sau đó đóng trang cuộc gọi hành động để trở về trang định nghĩa quy tắc điều hướng cửa sổ.  
  
14. Trong khu vực **Kết quả**:  
  
    1. Trong trường **Đích**, chọn **Tab** để hiển thị bản ghi liên hệ phù hợp trong tab.  
  
    2. Trong trường **Tab Đích**, chọn kiểm soát tổ chức **Liên hệ**. The **Contact** hosted control was created when you deployed a sample [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] application on your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps server using the [!INCLUDE[pn_package_deployer_tool](../includes/pn-package-deployer-tool.md)]. For more information, see [Deploy sample Unified Service Desk applications to CRM server using Package Deployer](admin/deploy-sample-unified-service-desk-applications-using-package-deployer.md).  
  
    3. Trong trường **Hiển thị Tab**, chọn kiểm soát tổ chức **Liên hệ**  
  
    ![Specify appropriate values for the rule definition](../unified-service-desk/media/usd-windownavruledefinition.png "Specify appropriate values for the rule definition")  
  
15. Lưu quy tắc điều hướng cửa sổ.  
  
<a name="test"></a>   
## <a name="test-your-cti-adapter"></a>Kiểm tra bộ chuyển đổi CTI của bạn  
  
1. Start [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client, and connect to your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance. After the client is up, choose **Settings**![Gear button](../unified-service-desk/media/crm-ua-selection-rule-gear.gif "Gear button") in the top-right corner to display the debugger control, and then choose **Clear Debug Output**![Delete button](../unified-service-desk/media/crm-ua-delete.gif "Delete button") to clear the desktop.  
  
   ![Unified Service Desk client](../unified-service-desk/media/usd-usdclientwithdebugger.png "Unified Service Desk client")  
  
2. Khởi động ứng dụng Trình mô phỏng USD CTI, nhập **Email** vào cột **Phím** và chỉ định ID email hợp lệ từ liên hệ mà bạn muốn tìm kiếm. In this case, type someone_d@example.com in the **Value** column. Bấm **Gửi tới USD**.  
  
   ![Specify the email to search for a contact](../unified-service-desk/media/usd-testctiadapter01.png "Specify the email to search for a contact")  
  
3. Bản ghi liên hệ phù hợp được hiển thị trong một phiên trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].  
  
   ![Matching Dynamics 365 for Customer Engagement apps contact record displayed in a session](../unified-service-desk/media/usd-testctiadapter02.png "Matching Dynamics 365 for Customer Engagement apps contact record displayed in a session")  
  
4. Kiểm tra kiểm soát tổ chức Trình gỡ lỗi để xem các sự kiện đã được nêu là kết quả của tìm kiếm CTI. Ngoài ra, kiểm tra tab **Tham số Dữ liệu** để xem thông tin ngữ cảnh trong biến `$Context` và thông tin CTI trong biến `CTI`.  
  
### <a name="see-also"></a>Xem thêm  
 [Integrate with CTI systems](../unified-service-desk/integrate-cti-systems-cti-adapters.md)   
 [UII Computer Telephony Integration (CTI) framework](../unified-service-desk/uii-computer-telephony-integration-cti-framework.md)
