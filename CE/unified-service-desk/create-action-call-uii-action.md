---
title: Create an action call for a UII action | MicrosoftDocs
description: Learn about creating an action call for a UII action.
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
ms.assetid: 5b8bac46-075e-4ad7-864f-a3a08ca8c743
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
ms.openlocfilehash: 9ac7b9915c9036b223f2347621b04b0875ced08c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385789"
---
# <a name="create-an-action-call-for-a-uii-action-in-unified-service-desk"></a>Create an action call for a UII action in Unified Service Desk
Có hai cách mà bạn có thể tạo cuộc gọi hành động cho một hành động [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)]:  

-   Tạo một cuộc gọi hành động và sau đó đính kèm nó vào kiểm soát tổ chức và hành động UII tương ứng.  

-   Bắt đầu từ kiểm soát tổ chức chứa hành động UII mà bạn muốn tạo cuộc gọi hành động.  

<a name="StartActionCall"></a>   
## <a name="start-from-the-action-call"></a>Bắt đầu từ cuộc gọi hành động  

1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. Click **Action Calls**.  

4. Trên trang danh sách cuộc gọi hành động, chọn **Thêm Cuộc gọi Hành động Mới** trên thanh lệnh.  

5. Trên trang **Cuộc gọi Hành động Mới**, chỉ định thông tin cho các trường khác nhau theo bảng sau.  

   ![New action call in Unified Service Desk](../unified-service-desk/media/usd-new-action-call.png "New action call in Unified Service Desk")  


   |     Trường      |                                                                                                                                                                                                                                                                         Mô tả                                                                                                                                                                                                                                                                         |
   |----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |      Tên      |                                                                                                                                                                                                                                                           Tên mô tả của cuộc gọi hành động.                                                                                                                                                                                                                                                            |
   | Kiểm soát được lưu trữ |                                                                                                                                                                                                                                                   Kiểm soát tổ chức có hành động UII được gọi.                                                                                                                                                                                                                                                    |
   |     Hành động     |                                                                                                                                                                                   Tên hành động UII để gọi trên kiểm soát tổ chức. To call a UII action for a hosted control, the action must be added to the list of UII actions for a hosted control in Dynamics 365 for Customer Engagement apps.                                                                                                                                                                                   |
   |      Dữ liệu      |                                                                                                                                                                                   Đây là dữ liệu được đăng (chuỗi dữ liệu) được thông qua dưới dạng tham số dữ liệu vào hành động. **Note:**  Some actions interpret multiline input specified here as separate parameters.                                                                                                                                                                                    |
   |   Điều kiện    |              Đây là một biểu thức [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] phải dẫn đến đúng hoặc sai. Ví dụ, "[[account.name]]"=="Tài khoản của tôi"<br /><br /> Nếu điều kiện dẫn đến sai hoặc đặt ra trường hợp ngoại lệ, các hành động sẽ không được thực hiện. Nếu các hành động là trống hoặc kết quả là đúng, những hành động sẽ được thực hiện. **Note:**  If the condition results in false or throws an exception, the action won’t be performed. Nếu các hành động là trống hoặc kết quả là đúng, những hành động sẽ được thực hiện.               |
   |  Phím tắt  | Đây là một phím tắt có thể được sử dụng bởi một tổng đài viên để chạy hành động này trong ứng dụng [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. Có thể sử dụng mọi mục hợp lệ cho chuỗi `KeyBinding.Gesture` tại đây. For more information see: [http://msdn.microsoft.com/en-us/library/system.windows.input.keybinding.gesture.aspx](https://msdn.microsoft.com/library/system.windows.input.keybinding.gesture.aspx).<br /><br /> Ví dụ:<br /><br /> -   CTRL+R<br />-   CTRL+ALT+A<br />-   SHIFT+ALT+A<br />-   CTRL-F12 |

   > [!TIP]
   >  Bạn có thể xem trợ giúp nhúng ở cuối trang **Cuộc gọi hành động mới** để biết mô tả và thông số áp dụng có thể được thông qua sử dụng cuộc gọi hành động.  

6. Chọn **Lưu**.  

<a name="StartHostedControl"></a>   
## <a name="start-from-the-hosted-control"></a>Bắt đầu từ kiểm soát tổ chức  

1. Tạo hoặc chỉnh sửa kiểm soát tổ chức có hành động UII mà bạn muốn tạo cuộc gọi hành động. For more information, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).  

2. Trên trang kiểm soát tổ chức, chọn mũi tên xuống bên cạnh tên kiểm soát tổ chức trên thanh điều hướng, sau đó chọn Hành động UII.  

   ![Navigation to UII Actions for a hosted control](../unified-service-desk/media/usd-uii-actions-hosted-control.png "Navigation to UII Actions for a hosted control")  

3. Từ danh sách hành động UII, chọn tên của hành động UII trong cột **Tên** mà bạn muốn thêm cuộc gọi hành động. Ngoài ra, chọn hồ sơ hành động UII theo yêu cầu, sau đó chọn **Chỉnh sửa** ở thanh lệnh. Thao tác này sẽ mở hồ sơ hành động UII.  

4. Trên trang hành động UII, chọn mũi tên xuống bên cạnh tên hành động UII trên thanh điều hướng, rồi chọn **Cuộc gọi Hành động**.  

   ![Menu navigation to create an action call](../unified-service-desk/media/usd-action-call-uii-action.png "Menu navigation to create an action call")  

5. On the action call list page, choose **Add New Action Call** on the command bar.  

6. Trên trang **Cuộc gọi hành động mới**, làm theo bước 5 và 6 trong phần trước.  

### <a name="see-also"></a>Xem thêm  
 [Quản lý kiểm soát tổ chức, hành động và sự kiện](../unified-service-desk/manage-hosted-controls-actions-events.md)   
 [Unified Service Desk Configuration Walkthroughs](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md)  

