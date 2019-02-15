---
title: Unified Service Desk for Dynamics 365 for Customer Engagement apps Base package | MicrosoftDocs
description: Overview of the base sample application.
ms.custom:
- dyn365-USD, dyn365-admin
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
- Dynamics CRM Online
ms.assetid: 5ee40b52-6c52-48ec-b3f1-7c2a839e7285
caps.latest.revision: 19
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
ms.openlocfilehash: f2b1685405aa4487686c496d90e757a630731002
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382552"
---
# <a name="base-sample-application-package"></a>Base sample application package
[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] is a desktop application that helps your customer service agents provide phone, email, and chat support to your customers. [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] provides a configurable framework to quickly build an Agent Desktop application that’s integrated with [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps. With [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] you can quickly make a customized Agent Desktop application by leveraging the User Interface Integration (UII) framework.  
  
 Với gói ứng dụng mẫu Cơ sở Unified Service Desk, các thành phần sau đây sẽ được cài đặt:  
  
- User Interface Integration Solution  
  
- Unified Service Desk Solution  
  
- Data required for [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps and customizations  
  
> [!IMPORTANT]
>  The sample applications are not supported for production use.  

  
 Dưới đây là những gì bạn sẽ nhìn thấy khi bạn cài đặt gói phần mềm cơ sở:  
  
1. **Điều hướng bên trái**: Mở vùng điều hướng bên trái mà bạn có thể mở hoặc thu gọn.  
  
2. **Bảng thông tin**: Mở bảng thông tin dịch vụ khách hàng [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)].  
  
3. **Công việc của tôi**: Hiển thị danh sách tất cả trường hợp hiện hoạt được gán cho một đại diện dịch vụ.  
  
4. **search**: Opens search for navigating through various entities. Đối với gói này, bạn có thể tìm kiếm tài khoản và liên hệ.  
  
5. **Thẻ phiên**: Khi bạn đang mở nhiều phiên khách hàng, mỗi thẻ sẽ hiển thị một phiên khác nhau. Các tab khiến cho tổng đài viên dễ dàng làm việc trên nhiều trường hợp khách hàng.  
  
6. **Tổng quan về Phiên**: Hiển thị các thông tin có liên quan về khách hàng.  
  
7. **Mã lệnh gọi**: Hiển thị các mã lệnh gọi mà tổng đài viên dịch vụ có thể sử dụng khi họ đang làm việc trong một trường hợp. Các mã lệnh giúp hướng dẫn các tổng đài viên bằng cách hướng dẫn cho họ từng bước cách làm thế nào để xử lý trường hợp.  
  
8. **Ghi chú**: Đây là khu vực để viết ghi chú liên quan đến trường hợp.  
  
   ![Unified Service Desk Base package components](../../unified-service-desk/media/unifiedservicedeskbasepackage.png "Unified Service Desk Base package components")  
  
## <a name="view-active-cases"></a>Xem các trường hợp hiện hoạt  
 Từ thanh công cụ, bấm vào **Công việc của tôi** để xem tất cả các trường hợp hiện hoạt rồi chọn một trường hợp để làm việc. Khi bạn mở một trường hợp, một phiên mới sẽ mở ra.  
  
## <a name="create-a-case"></a>Create a case  
  
1.  Look up the contact information by clicking **search** on the toolbar.  
  
2.  In the **search** field, enter the contact information.  
  
3.  Khi bạn tìm thấy thông tin liên hệ, hãy bấm vào bản ghi để mở một phiên mới.  
  
4.  Trên khu vực điều hướng **Kịch bản cuộc gọi** bên trái, sử dụng danh sách các kịch bản cuộc gọi để hướng dẫn bạn trong suốt trường hợp hỗ trợ.  Khi bạn bấm vào mã lệnh gọi, dấu kiểm xanh lục cho biết hành động đã được thực hiện.  
  
5.  Nhập ghi chú của trường hợp trong khu vực **Ghi chú**. Để gắn ghi chú của bạn với trường hợp, bấm vào **Cập nhật ghi chú** từ mã lệnh gọi.  
  
## <a name="search-for-solutions"></a>Tìm kiếm giải pháp  
 Để giúp giải quyết một trường hợp, bạn có thể sử dụng các bài viết cơ sở kiến thức hoặc tìm kiếm trên Bing để tìm ra giải pháp.  
  
1.  From the **Call script** area, click the **search for solutions** call script.  
  
2.  Sau đó, bấm vào một trong những giải pháp sau:  
  
    - **Bài viết KB**: Sử dụng công cụ tìm kiếm để tìm bài viết có thể giúp bạn giải quyết trường hợp này.  
  
    - **Tìm kiếm trên Bing**: Chủ đề tự động nạp vào hộp tìm kiếm Bing.  
  
## <a name="send-an-email"></a>Gửi một email  
 Từ danh sách mã lệnh gọi, bấm vào mã lệnh gọi **Gửi email** rồi chọn một mẫu tự động chuyển đến phần thân của email.  
  
## <a name="resolve-a-case"></a>Giải quyết trường hợp  
 Để giải quyết một trường hợp, từ khu vực **Mã lệnh gọi**, hãy bấm vào mã lệnh gọi **Giải quyết trường hợp**.  
  
## <a name="see-also"></a>Xem thêm  
 [Unified Service Desk Overview](../../unified-service-desk/admin/overview-unified-service-desk.md)
