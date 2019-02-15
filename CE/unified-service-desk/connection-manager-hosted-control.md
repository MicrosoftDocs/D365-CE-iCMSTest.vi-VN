---
title: Connection Manager (Hosted Control) | MicrosoftDocs
description: The Connection Manager hosted control type manages connections to the Dynamics 365 for Customer Engagement server, and makes it available to the rest of the agent application.
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
ms.assetid: c1a9b9ef-6243-4d1c-b0fe-726def04b417
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 79be0986f6f5b692ec38b39350a43fff36e666ff
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387568"
---
# <a name="connection-manager-hosted-control"></a>Connection Manager (Hosted Control)
The **Connection Manager** hosted control type manages connections to the Dynamics 365 for Customer Engagement server, and makes it available to the rest of the agent application. Một phiên bản của kiểm soát tổ chức này được yêu cầu bởi [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], và chỉ một phiên bản loại kiểm soát tổ chức đơn này mới tồn tại trong ứng dụng tổng đài viên của bạn.  
  
> [!IMPORTANT]
>  The three sample application packages for [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], `New Environment`, `CRM Web Client`, and `Interactive Service Hub`, come preconfigured with an instance each of the **Connection Manager** hosted control type. For information about the sample applications, see [Deploy sample Unified Service Desk applications to CRM server using Package Deployer](admin/deploy-sample-unified-service-desk-applications-using-package-deployer.md).  
  
## <a name="in-this-section"></a>In This Section  
 [Tạo kiểm soát tổ chức Trình quản lý kết nối](../unified-service-desk/connection-manager-hosted-control.md#create)  
  
 [Thao tác UII được xác định trước](../unified-service-desk/connection-manager-hosted-control.md#UIIactions)  
  
 [Predefined UII actions](../unified-service-desk/connection-manager-hosted-control.md#UIIactions)  
  
<a name="create"></a>   
## <a name="create-a-connection-manager-hosted-control"></a>Tạo kiểm soát tổ chức Trình quản lý kết nối  
 While creating a new hosted control, the fields in the **New Hosted Control** screen vary based on the type of hosted control you want to create. Phần này cung cấp thông tin về các trường cụ thể mà là duy nhất cho loại kiểm soát tổ chức **Trình quản lý kết nối**. For detailed information about creating a hosted control, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).  
  
 ![Connection manager hosted control](../unified-service-desk/media/crm-itpro-usd-connectionmanagerhostedcontrol.PNG "Connection manager hosted control")  
  
 Trong màn hình **Kiểm soát tổ chức mới**, dưới khu vực **Unified Service Desk**, chọn **trình quản lý kết nối** từ danh sách thả xuống **Loại Thành phần USD**. Ngoài ra, đảm bảo rằng bạn đặt giá trị **thứ tự sắp xếp** của kiểm soát tổ chức thành **1** để đảm bảo đây là kiểm soát tổ chức đầu tiên được trích xuất và hiển thị bằng ứng dụng tổng đài viên của bạn khi ứng dụng tổng đài viên được khởi chạy. For information about other **General** fields, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).  
  
<a name="UIIactions"></a>   
## <a name="predefined-uii-actions"></a>Predefined UII actions  
 Loại kiểm soát tổ chức này không có bất kỳ hoạt động UII được xác định trước nào.  
  
<a name="events"></a>   
## <a name="predefined-events"></a>Sự kiện được xác định trước  
 Loại kiểm soát tổ chức này không có bất kỳ sự kiện được xác định trước nào.  
  
### <a name="see-also"></a>Xem thêm  
 [Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)   
 [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md)   
 [Unified Service Desk Hosted Controls](../unified-service-desk/unified-service-desk-hosted-controls.md)   
 [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md)
