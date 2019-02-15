---
title: Create a user-defined event | MicrosoftDocs
description: Unified Service Desk provides you with predefined events for hosted controls based on the type of the hosted control. Apart from these predefined events, you can also create your own events in Unified Service Desk, which are called user-defined events. You can use the FireEvent action or the event moniker to run user-defined events.
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
ms.assetid: d9bc82cb-4d6c-4f3b-9aa5-2bb757de116b
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
ms.openlocfilehash: 947ddeaa1a6724dd91f24532e8e9c31d808f5ec9
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386784"
---
# <a name="create-a-user-defined-event"></a>Create a user-defined event
[!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]cung cấp cho bạn sự kiện được xác định trước cho kiểm soát tổ chức dựa trên loại kiểm soát tổ chức. Ngoài những sự kiện được xác định trước này, bạn cũng có thể tạo sự kiện của riêng bạn trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], mà được gọi là sự kiện do người dùng xác định. You can use the **FireEvent** action or the event moniker to run user-defined events.  

<a name="FireEvent"></a>   
## <a name="use-the-fireevent-action"></a>Use the FireEvent action  
 Tất cả loại kiểm soát tổ chức [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] được xác định trước và tùy chỉnh, ngoại trừ **Ứng dụng tổ chức CCA** có một hành động UII đặc biệt được gọi là **FireEvent**. Bạn có thể gọi hành động này để bắt đầu một sự kiện do người dùng xác định từ kiểm soát đó. Đây là một cách thuận tiện để nhóm nhiều cuộc gọi hành động thành một cuộc gọi duy nhất, tạo hàm trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] có hiệu quả. Nó cũng là một cách hợp lý để kiểm tra sự kiện và trình tự hành động trước khi triển khai.  

 Các tham số đầu tiên vào **FireEvent** là tên của sự kiện này:  

```  
name=MyEvent  
```  

 Tất cả các cặp tên/giá trị tiếp theo trở thành các tham số cho sự kiện này và do đó có thể được sử dụng như thay thế thông số trong các hành động được gọi như kết quả. Ví dụ, nếu bạn vượt qua danh sách tham số sau đây:  

```  
name=MyEvent  
var1=[[account.name]]  
```  

 This will fire the custom event **MyEvent** event enabling the ability to create an action call that uses the `var1` parameter as follows:  

```  
Hosted Control=Some Hosted Control  
UII Action=Some action on the Hosted Control  
Data=[[var1]]  
```  

 Điều này đi qua tham số sự kiện như là một tham số dữ liệu cho hành động của kiểm soát tổ chức. Trong ví dụ này, đó có nghĩa là các tham số dữ liệu cho kiểm soát tổ chức sẽ là già trí tên tài khoản từ phiên.  

<a name="EventMoniker"></a>   
## <a name="use-the-event-moniker"></a>Use the event moniker  
 You can create a custom event on a hosted control, and then call it using the following event moniker syntax:  

```  
http://event/?EventName=<EVENT_NAME>&key=value&key=value&…  
```  

 In the syntax, you specify the `key=value` pair to pass parameter list to be used when the event is triggered.  

 Consider an example where you want to raise a user-defined event whenever the title of the case on the case form changes in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps. To do this:  

1. Create a new event, called `TitleChanged`, for the **Incident** hosted control in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  

2. Create an action call, called `Action Call for Title Change`, with the following values:  


   |     Trường      |                                                                                                                         Value                                                                                                                         |
   |----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |      Tên      |                                                                                                             Action Call for Title Change                                                                                                              |
   | Kiểm soát được lưu trữ |                                                                                                                       Sự cố                                                                                                                        |
   |     Hành động     |                                                                                                                     Chạy lệnh Xrm                                                                                                                     |
   |      Dữ liệu      | function titleChangeReaction()  {<br /> window.open("<http://event/?EventName=TitleChanged&NewTitle="+encodeURIComponent(Xrm.Page.getAttribute("title").getValue(>)));<br /> }<br /> Xrm.Page.getAttribute("title").addOnChange(titleChangeReaction); |


3. Add the new action call that you created to the **BrowserDocumentComplete** event of the **Incident** hosted control. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Add action calls to an event](../unified-service-desk/add-action-calls-event.md)  

    When the `TitleChanged` event is triggered, the following request is raised: `http://event/?EventName=TitleChanged&NewTitle=<NEW_TITLE>`  

    This will cause the `TitleChanged` event to be triggered with the following data parameter: `NewTitle=<NEW_TITLE>`  

   If you use [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps to invoke an event in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] using the event moniker (`http://event/?EventName=<EVENT_NAME>&key=value&key=value&…`), you can use the `window.IsUSD` property to determine whether the [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] code is running under [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] when the event is invoked. The following code sample can be included in your [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] code to ensure that the event is invoked only when the calling [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] is running within [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].  

```  
if ((window.IsUSD != null) && (window.IsUSD == true))  
{  
   window.open(http://event/?EventName=<EVENT_NAME>&key=value&key=value&…);  
}  
```  

### <a name="see-also"></a>Xem thêm  
 [Sự kiện](../unified-service-desk/events.md)   
 [Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)   
 [Manage hosted controls, actions, and events](../unified-service-desk/manage-hosted-controls-actions-events.md)   
 [MSDN: Use JavaScript with Microsoft Dynamics CRM](https://msdn.microsoft.com/library/hh771584.aspx)
