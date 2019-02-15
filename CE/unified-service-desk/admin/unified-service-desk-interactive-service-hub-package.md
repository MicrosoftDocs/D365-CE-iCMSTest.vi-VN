---
title: Unified Service Desk for Dynamics 365 for Customer Engagement apps - Interactive service hub package | MicrosoftDocs
description: Overview of the Interactive service hub sample application.
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
ms.assetid: bc2bed7d-daab-4c1f-97c4-fea63d6a230a
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 0b2490ea2c84424156c729591911e240a5f2a896
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382418"
---
# <a name="interactive-service-hub-sample-application-package"></a>Interactive service hub sample application package
[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] là một ứng dụng máy tính để bàn giúp tổng đài viên dịch vụ khách hàng của bạn hỗ trợ cho khách hàng thông qua điện thoại, email và trò chuyện. [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] provides a configurable framework to quickly build an Agent Desktop application that’s integrated with [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps. Với [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] bạn có thể nhanh chóng tạo một ứng dụng Màn hình nền của Tổng đài viên tùy chỉnh bằng cách tận dụng nền tảng User Interface Integration (UII) (Tích hợp Giao diện Người dùng).  
  
 Gói này được sử dụng hiệu quả nhất trong các trường hợp sau:  
  
- [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps environments that want to evaluate  interactive service hub integration with [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [User's guide for the new interactive service hub](https://go.microsoft.com/fwlink/?linkid=857154)  
  
- [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps environments that are already using the interactive service hub.  
  
  Với gói ứng dụng mẫu của trung tâm dịch vụ tương tác Unified Service Desk, các thành phần sau đây được cài đặt:  
  
- Giải pháp User Interface Integration  
  
- Giải pháp Unified Service Desk  
  
- Cấu hình để tích hợp trung tâm dịch vụ tương tác với [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]  
  
- Data required for [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps and customizations  
  
- Các kiểm soát tổ chức mẫu sau  
  
  -   Kiểm soát tùy chỉnh Chỉ số Đánh giá Hiệu suất Chính  
  
  -   Hệ thống Thông tin Khách hàng  
  
> [!IMPORTANT]
>  Ứng dụng mẫu không được hỗ trợ cho sản xuất.  
    
  
 Dưới đây là những gì bạn sẽ nhìn thấy khi cài đặt gói trung tâm dịch vụ tương tác:  
  
- **Dashboard** tab: Opens the Dynamics 365 for Customer Engagement apps customer service dashboard.  
  
- Thẻ **Công việc của tôi**: Hiển thị danh sách tất cả trường hợp hiện hoạt được chỉ định cho đại diện dịch vụ.  
  
- **search** tab: Opens search for navigating through various entities. Đối với gói này, bạn có thể tìm kiếm tài khoản và liên hệ.  
  
- Thẻ **Lời nhắc**: Xem và bỏ qua các lời nhắc hoạt động.  
  
- Có sẵn một số bảng thông tin.  Dưới đây là những gì bạn có thể làm với gói mẫu này.  
  
  - Bấm vào một biểu đồ hoặc một mục trong danh sách để duyệt qua và xem các bản ghi phía sau hiển thị trực quan.  
  
  - Chọn phạm vi ngày phổ biến, như **Hôm nay**, **Hôm qua**, **Tháng trước** hoặc **Quý này** hoặc nhập phạm vi ngày của riêng bạn.  
  
  - Chuyển đổi giữa dạng xem danh sách và biểu đồ bằng cách chọn kiểu xem là kiểu luồng hay kiểu lát ở phía dưới bên phải.  
  
    Chọn trong số các bảng thông tin dịch vụ sau:  
  
  - **Trình quản lý kiến thức**. Hiển thị danh sách hoặc kiểu trực quan của dữ liệu bài viết kiến thức chính, chẳng hạn như bài viết được đề xuất, đánh giá nhu cầu bài viết phác thảo, đánh giá nhu cầu bài viết hết hạn, phổ biến nhất và được xếp hạng cao nhất.  
  
  - **Bảng thông tin kiến thức của tôi**. Hiển thị danh sách hoặc kiểu trực quan cho một số chỉ số đo lường hiệu suất chính của bài viết kiến thức được liên kết với tác nhân, như bài viết hiện hoạt, theo chủ đề, theo chủ sở hữu, xem theo chủ đề, theo lý do dẫn đến trạng thái, cũng như tổng số tác nhân cho bài viết được đăng, bài viết hết hạn và bài viết sắp hết hạn tháng này.  
  
  - **Bảng thông tin Cấp 1**. Hiển thị danh sách hoặc kiểu trực quan của dữ liệu dịch vụ tác nhân chính, như trường hợp hiện hoạt, trường hợp đã giải quyết, email nháp và hoạt động.  
  
  - **Bảng thông tin Cấp 2**.  Hiển thị danh sách hoặc kiểu trực quan cho một số chỉ số đo lường hiệu suất chính cho dịch vụ được liên kết với tác nhân, như trường hợp hiện hoạt, trường hợp theo thứ tự ưu tiên, trường hợp theo sản phẩm, kết hợp trường hợp theo loại sự việc và tổng số tác nhân cho trường hợp hiện hoạt, trường hợp được giải quyết, hoạt động và cuộc gọi điện thoại.  
  
  ![Unified ServiceDesk interactive service hub package](../../unified-service-desk/media/unifiedservicedeskishpackage.PNG "Unified ServiceDesk interactive service hub package")  

  ## <a name="see-also"></a>Xem thêm  
  [Unified Service Desk Overview](../../unified-service-desk/admin/overview-unified-service-desk.md)
