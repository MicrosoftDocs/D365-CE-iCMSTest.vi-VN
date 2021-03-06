---
title: Popup Notification (Hosted Control) in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn about using the Popup Notification hosted control type to display notifications in Unified Service Desk. The notification layout and content is defined as XAML in a Unified Service Desk form instance, and the Popup Notification hosted control is used to display and hide the form instance as required
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
ms.assetid: 0271073c-d9b1-4f40-8d9a-c2398ae7df8d
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
ms.openlocfilehash: 3b600c46e2518ee2542bf22160c3fabca74d7e08
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388589"
---
# <a name="popup-notification-hosted-control"></a>Popup Notification (Hosted Control)
Use the **Popup Notification** hosted control type to display notifications in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. The notification layout and content is defined as XAML  in a [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] form instance, and the **Popup Notification** hosted control is used to display and hide the form instance as required. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Configure notifications in Unified Service Desk](../unified-service-desk/configure-notifications-unified-service-desk.md)  

> [!NOTE]
>  This hosted control type was introduced in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] 2.2 release.  

<a name="Create"></a>   
## <a name="create-a-popup-notification-hosted-control"></a>Create a Popup Notification hosted control  
 While creating a new hosted control, the fields in the **New Hosted Control** screen vary based on the type of hosted control you want to create. This section provides information about the specific fields that are unique to the **Popup Notification** hosted control type. For detailed information about creating a hosted control, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).  

 ![Notification Hosted Control](../unified-service-desk/media/usd-notification-hosted-control.png "Notification Hosted Control")

 In the **New Hosted Control** screen:  

- Under **Unified Service Desk** area, select **Popup Notification** from the **Unified Service Desk Component Type** drop-down list.  

- Select the **Application is Global** check box to set the hosted control as global, which can be displayed outside of a customer session. Kiểm soát tổ chức chung không có trạng thái phiên dành riêng cho phiên để khi bạn thay đổi phiên, các kiểm soát tổ chức chung tương tự vẫn được duy trì. Nếu hộp kiểm không được chọn, kiểm soát tổ chức trở thành kiểu dựa trên phiên. Kiểm soát dựa trên phiên tồn tại trong ngữ cảnh của phiên khách hàng. If the user changes to another session, all the notifications and other hosted controls   from the previous session are hidden.  

- You cannot change the value of the **Application is Dynamic** field. By default, the control is a dynamic hosted control, which allows an agent to start or close a hosted control on demand, either by using the UI or programmatically through code. More information: [Dynamic Unified Service Desk hosted controls](../unified-service-desk/unified-service-desk-hosted-controls.md#Dynamic)  

  For information about other **General** fields, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).  

<a name="Actions"></a>   
## <a name="predefined-uii-actions"></a>Predefined UII Actions  
 These are the predefined events for this hosted control.  

<a name="Show"></a>   
### <a name="show"></a>Show  
 Displays a notification.  

::: moniker range="=dynamics-usd-3"

|   Tham số   | Mô tả  |
|---------------|--------------|
|   formname    | Name of the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] form to display. |
| placementmode | Specifies whether or not to display the notification relative to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] window. Valid values are `absolute` or `relative`.<br /><br /> -   `absolute`: Specifies that the notification will be displayed based on your screen coordinates. The values that you specify in the `left` and `top` parameters for the notification location are absolute percentage values for your computer screen.</br><br/>-   `relative`:  Specifies that the notification will be displayed based on [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client window coordinates. The values that you specify in the `left` and `top` parameters for the notification location are  percentage values relative to the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client window. |
|     trái      | Specifies the position, in percentage, from the left of either your screen or the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client window where the notification should be displayed. Nếu bạn không chỉ định tham số này, giá trị 0 sẽ được dùng theo mặc định. |
|      trên cùng      | Specifies the position, in percentage, from the top of either your screen or the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client window where the notification should be displayed. If you don’t specify this parameter, 0 is passed by default. |
|    timeout    | Duration in seconds for the notification to be available without any interaction. If you do not specify a valid value for this parameter, the notification will continue to appear, and won't hide/close automatically. If you want a notification to be explicitly closed, you might leave out this value but should add a cancel/close button to close the notification if the user wants to close the notification. |

::: moniker-end

::: moniker range=">=dynamics-usd-4"

|   Tham số   | Mô tả  |
|---------------|--------------|
|   formname    | Name of the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] form to display. |
| placementmode | Specifies whether or not to display the notification relative to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] window. Valid values are `absolute` or `relative`.<br /><br /> -   `absolute`: Specifies that the notification will be displayed based on your screen coordinates. The values that you specify in the `left` and `top` parameters for the notification location are absolute percentage values for your computer screen.</br><br/>-   `relative`:  Specifies that the notification will be displayed based on [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client window coordinates. The values that you specify in the `left` and `top` parameters for the notification location are  percentage values relative to the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client window. |
|     trái      | Specifies the position, in percentage, from the left of either your screen or the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client window where the notification should be displayed. If you don’t specify this parameter, 0 is passed by default. |
|      trên cùng      | Specifies the position, in percentage, from the top of either your screen or the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client window where the notification should be displayed. If you don’t specify this parameter, 0 is passed by default. |
|    timeout    | Duration in seconds for the notification to be available without any interaction. If you do not specify a valid value for this parameter, the notification will continue to appear, and won't hide/close automatically. If you want a notification to be explicitly closed, you might leave out this value but should add a cancel/close button to close the notification if the user wants to close the notification. |
|    stack    | Specifies whether Unified Service Desk shows the notifications as a stack.<br> Set **true** to show the notification in stack.<br>Set **false** to not to show the notifications in stack. |
|    stackHeight    | Height the notification in pixels in the collapsed state.<br> The range of the value is between 1 - 100. Mặc định là 50. If you do not specify any value, the default value (50) is passed. Also, if you specify 0 or specify more than 100, default value (50) is passed.|

::: moniker-end


<a name="Hide"></a>   
### <a name="hide"></a>Hide  
 Hides the notification.  

<a name="Close"></a>   
### <a name="close"></a>Đóng  
 Closes the notification, and disposes the associated UI elements.  

<a name="events"></a>   
## <a name="predefined-events"></a>Predefined Events  
 These are the predefined events for this hosted control.  

> [!NOTE]
>  Developers can define custom (user-defined) events for the hosted control, and fire them from the XAML. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Command binding to fire events for the Popup Notification control](../unified-service-desk/configure-notifications-unified-service-desk.md#CommandBinding). In case of user-defined events, you will have to explicitly invoke the `Hide` action to hide the notification as opposed to the predefined events that automatically hide the notification when they occur.  

### <a name="ok"></a>Ok  
 This event is fired from the form XAML that defines the notification layout. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Command binding to fire events for the Popup Notification control](../unified-service-desk/configure-notifications-unified-service-desk.md#CommandBinding). When this event occurs, the notification control will automatically hide.  

### <a name="cancel"></a>Hủy  
 This event is fired from the form XAML that defines the notification layout. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Command binding to fire events for the Popup Notification control](../unified-service-desk/configure-notifications-unified-service-desk.md#CommandBinding). When this event occurs, the notification control will automatically hide.  

### <a name="timedout"></a>TimedOut  
 This event occurs when the timeout value specified for the control in the `Show` action has elapsed without any interaction on the notification message. When this event occurs, the notification control will automatically hide.  

### <a name="see-also"></a>Xem thêm  
 [How to configure notifications in Unified Service Desk](../unified-service-desk/configure-notifications-unified-service-desk.md)   
 [Create a user-defined event](../unified-service-desk/create-user-defined-event.md)
