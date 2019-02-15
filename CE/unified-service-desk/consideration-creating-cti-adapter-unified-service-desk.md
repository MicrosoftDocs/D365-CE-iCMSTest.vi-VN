---
title: Considerations for creating a CTI adapter for Unified Service Desk | MicrosoftDocs
description: 'The topic provides information on things to consider while creating a computer telephony integration (CTI) adapter to make it work with Unified Service Desk. '
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
ms.assetid: 6b59cb93-8e3b-4224-b6fe-c9964fcefbfb
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
ms.openlocfilehash: 4c4c6fb76c972e8c42497a966dbd8770f18e67a9
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385830"
---
# <a name="considerations-for-creating-a-cti-adapter-for-unified-service-desk"></a>Considerations for creating a CTI adapter for Unified Service Desk
This topic provides information on things to consider while creating a computer telephony integration (CTI) adapter to make it work with [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].  

<a name="UISpec"></a>   
## <a name="cti-control-softphone-user-interface-specification"></a>CTI Control (softphone user interface) specification  
 To ensure that softphone and [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] user interface components will interoperate with [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], make sure of the following:  

- Controls are created using [!INCLUDE[pn_ms_Windows_Presentation_Foundation](../includes/pn-ms-windows-presentation-foundation.md)], and are derived from the [DynamicsBaseHostedControl](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.dynamicsbasehostedcontrol) class.  

- [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] controls are placed on `CtiPanel`  panel in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. The height of the control should be 23 to fit in `CtiPanel`. Larger controls may be used.  

- Multiple [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] control or user interface components can exist on `CtiPanel`. This is a horizontal stack panel so if you have multiple controls on this panel, they will appear next to each other.  

<a name="Actions"></a>   
## <a name="actions-supported-for-telephony-functions"></a>Hành động được hỗ trợ cho các chức năng điện thoại  
 Tính năng của [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] là khả năng cấu hình thiết kế ứng dụng nâng cao mà không cần lập trình. Loại chức năng tiếp xúc thông qua các khái niệm về các hành động trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. To support the idea of extending telephony control functions to buttons, agent scripts, and links in hosted applications, the system relies on actions being defined for capabilities exposed by the [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] adapter. This is done by exposing UII Actions in the [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] Desktop Manager hosted control of your [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] component. Mỗi hành động trong số những hành động này cung cấp cho các quản trị viên quyền kiểm soát nhiều hơn hành vi của ứng dụng.  

 It is recommended that the following actions be defined and implemented in the **CTI Desktop Manager** hosted control.  

|Hành động|Mô tả|  
|------------|-----------------|  
|Quay số|Số để gọi. Nếu tham số này không được cung cấp, một bảng quay số sẽ được hiển thị cho người dùng để nhập chữ số.<br /><br /> Nếu cuộc gọi là cuộc gọi đang hoạt động, hành động này sẽ quay số như cho IVR.|  
|Chuyển|Điều này sẽ bắt đầu hoặc hoàn tất việc chuyển giao. Nếu việc chuyển giao đã được bắt đầu nhưng chưa hoàn tất, điều này sẽ chuyển cuộc gọi và bỏ qua các tham số. Nếu cuộc gọi hiện hoạt là hiện tại, nó sẽ đặt giữ cuộc gọi và thực hiện cuộc gọi mới đi qua các dữ liệu ngữ cảnh.|  
|Hội nghị|Điều này sẽ bắt đầu hoặc hoàn tất hội nghị. Nếu hội nghị đã được bắt đầu nhưng chưa hoàn tất, điều này sẽ chuyển hội nghị và bỏ qua các tham số. Nếu cuộc gọi hiện hoạt là hiện tại, nó sẽ đặt giữ cuộc gọi và thực hiện cuộc gọi mới đi qua các dữ liệu ngữ cảnh.|  
|Gác máy|Điều này kết thúc cuộc gọi hiện tại.|  

> [!NOTE]
>  If these actions are supported by the **CTI Desktop Manager** hosted control, users will be able to trigger this functionality from a wide variety of locations within the application, thus providing a tightly integrated agent experience.  

<a name="CTIScreenPop"></a>   
## <a name="cti-screen-pop"></a>CTI screen pop  
 You must ensure the following while designing [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] screen pops in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].  

- The following values must be populated in the `CallInfo` parameter of the [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)]request.  


  | Tham số |                                                                                               Mô tả                                                                                               |
  |-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
  | hướng | Specify “inbound” for incoming calls and “outbound” for outgoing calls.<br /><br /> Điều này được sử dụng bởi hệ thống để cho phép các quản trị viên xác định các hành vi khác nhau tùy thuộc vào sự hướng dẫn của các cuộc gọi. |
  | Loại cuộc gọi  |                                                                    Specify “phonecall” for voicecalls and “chat” for chat sessions..                                                                    |


- [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] adapters should not automatically create activities in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps because this is not always the desired behavior. Do đó, điều này nên được để lại cho các quản trị viên hệ thống định cấu hình.  

    ```csharp  
    try  
    {  
      FireRequestAction(new RequestActionEventArgs("*", CtiLookuprequest.CTILOOKUPACTIONNAME,GeneralFunctions.Serialize<CtiLookupRequest>(data)));  
    }  
    ```  

  > [!NOTE]
  >  It is assumed that the `CTILOOKUPACTIONNAME` be used for calling the [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] action, and that the application name will be "*", as shown in the example code.  

> [!IMPORTANT]
>  It is possible to create [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] adapters for [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] that don’t follow the [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)][!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] framework.  

<a name="CTISearch"></a>   
## <a name="cti-search"></a>Tìm kiếm CTI  
 [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] searches are done using FetchXML in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps. You can search using any data passed in any parameter from [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] against any field in your entity of choice in Dynamics 365 for Customer Engagement apps. Tìm kiếm được thực hiện một quy tắc tại một thời điểm tìm thấy kết quả khớp. Khi khớp với quy tắc điều hướng cửa sổ trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] được tìm thấy, nó sẽ làm theo sự hướng dẫn cấu hình trong quy tắc chuyển hướng cho bước tiếp theo. Typically, a rule is set up to open a session around the activity, and optionally display the activity in a tab. For more information about how to configure a window navigation rule to perform a [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)]search, see [Walkthrough: Use generic listener adapter for CTI events](../unified-service-desk/walkthrough-use-the-generic-listener-adapter-for-cti-event-routing.md).  

 Chúng ta hãy đặt cấu hình quy tắc tìm CTI mẫu bằng cách sử dụng quy tắc chuyển hướng cửa sổ trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. For more information about the window navigation rule, see [Use window navigation rules in Unified Service Desk](../unified-service-desk/use-window-navigation-rules-unified-service-desk.md).  

1. Trên thanh điều hướng, chọn **Microsoft Dynamics 365 for Customer Engagement** và chọn **Thiết đặt**.  

2. On the nav bar, choose **Settings**, and then select **Window Navigation Rules**.  

3. Chọn **Mới**.  

4. Nhập tên và thứ tự cho quy tắc điều hướng cửa sổ. In the **From** box, select your [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] Desktop Manager hosted control.  

5. After you have selected your [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] Desktop Manager, the [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] options will be displayed starting with an initiating activity. The initiating activity field should contain the entity type passed from the [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] adapter. For example, it can be phonecall, chat, email, and so on. Một quy tắc chỉ xử lý một loại hoạt động từ các máy chủ CTI.  

   ![New window navigation rule for routing CTI event](../unified-service-desk/media/usd-cti-route-rule.png "New window navigation rule for routing CTI event")  

6. Bấm vào **Lưu** ở góc dưới bên phải để lưu hồ sơ và cho phép các trường cần thiết cho các bước tiếp theo.  

7. Trong **Tìm kiếm CTI**, nhấp vào biểu tượng tìm kiếm, và sau đó nhấp vào **Mới** trong hộp tìm kiếm để xác định một tiêu chí tìm kiếm mới bằng cách sử dụng các truy vấn FetchXML.  

8. Trong màn hình **Tìm kiếm CTI mới**, chỉ định tên và trình tự cho truy vấn tìm kiếm của CTI. The direction field is Inbound or Outbound and is used to search against only a specific direction of CTI event. This direction is passed from the [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] adapter.  

    Enter the required FetchXML query for the [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] search. Use the advanced find feature in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps to create your initial search, and then download the FetchXML. The key field is often not available in the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps Advanced Find search, so you may find that you need to add that condition manually to the XML after you have exported it. You should also select the attributes that you’re interested to show up in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] context. Các thuộc tính này hiển thị ngay lập tức thay vì được xác định sau khi tải trang trong màn hình như các loại dữ liệu thông số khác. Once you have the FetchXML you want, paste the text into the **FetchXML** box, and save the [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] search rule.  

   ![New CTI search in Unified Service Desk](../unified-service-desk/media/usd-cti-search-rule-2.PNG "New CTI search in Unified Service Desk")  

9. The system will search each of your [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] search items for the rule. Điều này có thể được dùng như một thực thể qua tìm kiếm. The conditions relate to the final result set and may, in the case of multiple results handling, indicate that one or more records were found from more than one entity type.  

     Below the search list are three conditions and selections used to indicate what is to be done in each case.  

    |Điều kiện|Mô tả|  
    |---------------|-----------------|  
    |Không có kết quả phù hợp|What should the system do if no matches were found across all the searches specified in the rule.|  
    |Một kết quả phù hợp|Hệ thống sẽ làm gì khi chỉ tìm thấy một hồ sơ cho kết quả tìm kiếm kết hợp.|  
    |Nhiều kết quả phù hợp|Hệ thống sẽ làm gì nếu có nhiều hơn một kết quả được tìm thấy trên tất cả các tìm kiếm.|  

     Đối với mỗi điều kiện, cần đưa ra một quyết định liên quan đến việc phải làm gì.  


   |                 Quyết định                  |                                                                                                                                                                           Mô tả                                                                                                                                                                            |
   |-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |       Tạo phiên sau đó Thực hiện hành động       |                                                                                                                    Creates a new session before firing a configured action. Hành động này sẽ được bắt đầu trong ngữ cảnh của phiên mới này.                                                                                                                    |
   | Tạo phiên, tải kết quả phù hợp sau đó Thực hiện hành động |                                                 Creates a session, then loads the match into a tab or Entity Search based upon the selection in the Result Tab of the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps form. Finally, it calls an action. Tùy chọn này chỉ có hiệu lực cho một kết quả phù hợp.                                                 |
   |                 Thực hiện Hành động                 | Tells the system to do nothing with the result, but optionally call a configured action specific to this condition. You can call the `FireEvent` action on Global Manager hosted control, if you want to call multiple actions in sequence as a result of this. Hành động này sẽ được bắt đầu trong ngữ cảnh của phiên hiện tại. Không có phiên làm việc mới được tạo ra. |
   |                 Nguyên tắc tiếp theo                 |                                                                                              Cho hệ thống biết bỏ qua phần còn lại của việc xử lý quy tắc này và để tìm kiếm các quy tắc có thể phù hợp khác. Tìm kiếm mới sẽ được thực hiện chống lại quy tắc tiếp theo.                                                                                              |

    > [!IMPORTANT]
    >  Bất kỳ thời điểm nào hệ thống không có tùy chọn "Quy tắc Tiếp theo" được cấu hình trong các quy tắc chuyển hướng của bạn, nó cũng sẽ thực hiện các hành động được cấu hình trên quy tắc chuyển hướng của chính nó. Nếu bạn muốn chỉ thực hiện quy tắc trong trường hợp cụ thể, bạn nên sử dụng các hành động trong phần đó. Vì hành động có mục đích chung mà nên thực hiện cho dù có đưa ra sự lựa chọn nào, bạn có thể nhập chúng vào danh sách hoạt động cho quy tắc điều hướng.  

<a name="chat"></a>   
## <a name="special-features-of-chat-events"></a>Các tính năng đặc biệt của sự kiện trò chuyện  
 Khi đáp ứng với sự kiện trò chuyện, một số điều đặc biệt diễn ra trong hệ thống. It is assumed that the [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] event data parameter “`CTIDESKTOPMANAGERCONTROL`” value is populated with the [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] Desktop Manager hosted control name and it supports the `SendIM` action. If the [CALLTYPE](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.lookuprequestkeys.calltype) passed into the [CtiLookupRequest](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.ctilookuprequest) is “Chat”, [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] will show an extra button on the agent scripting user interface. If the agent clicks this button, it will attempt to invoke the `SendIM` action on the [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] Desktop Manager hosted control specified in the `CTIDESKTOPMANAGERCONTROL` control. It will pass the text of the agent script to this action, and it is assumed that the [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] Desktop Manager hosted control will write this text to the chat output.  

### <a name="see-also"></a>Xem thêm  
 [UII Computer Telephony Integration (CTI) framework](../unified-service-desk/uii-computer-telephony-integration-cti-framework.md)   
 [CTIDESKTOPMANAGERCONTROL](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.lookuprequestkeys.ctidesktopmanagercontrol)   
 [Create a CTI Desktop Manager](../unified-service-desk/create-cti-desktop-manager.md)   
 [Sử dụng quy tắc điều hướng cửa sổ trong Unified Service Desk](../unified-service-desk/use-window-navigation-rules-unified-service-desk.md)   
 [Walkthrough: Use generic listener adapter for CTI events](../unified-service-desk/walkthrough-use-the-generic-listener-adapter-for-cti-event-routing.md)
