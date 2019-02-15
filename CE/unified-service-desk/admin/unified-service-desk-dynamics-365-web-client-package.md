---
title: Unified Service Desk for Dynamics 365 for Customer Engagement apps Web Client package | MicrosoftDocs
description: Overview of the Web Client sample application.
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
ms.assetid: 1a69d545-24d2-4009-814d-0f9837732bea
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 22ec915f83d15d58bd0fe0b01a69ad2394bec872
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382562"
---
# <a name="web-client-sample-application-package"></a>Web Client sample application package
[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] is a desktop application that helps your customer service agents provide phone, email, and chat support to your customers. [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] provides a configurable framework to quickly build an Agent Desktop application that’s integrated with [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps. With [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] you can quickly make a customized Agent Desktop application by leveraging the User Interface Integration (UII) framework.  
  
 Gói này được sử dụng hiệu quả nhất trong các trường hợp sau:  
  
- To demonstrate the rich set of customer service capabilities in [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps and simplify the customization of your agent desktop application.  
  
  With the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] Dynamics 365 for Customer Engagement apps Web Client sample application package, the following components are installed:  
  
- User Interface Integration Solution  
  
- Unified Service Desk Solution  
  
- Data required for [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps and customizations  
  
- The following sample hosted controls  
  
  -   KPI Custom Control  
  
  -   Hệ thống Thông tin Khách hàng  
  
> [!IMPORTANT]
>  Ứng dụng mẫu không được hỗ trợ cho sản xuất.  
  
  
 Here’s what you’ll see when you install the Dynamics 365 for Customer Engagement apps Web Client package:  
  
1. Điều hướng bên trái: Mở vùng điều hướng bên trái mà bạn có thể mở hoặc thu gọn.  
  
2. Bảng thông tin: Mở bảng thông tin dịch vụ khách hàng [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)].  
  
3. Công việc của tôi: Hiển thị danh sách tất cả trường hợp hiện hoạt được gán cho một đại diện dịch vụ.  
  
4. search tab: Opens search for navigating through various entities. Đối với gói này, bạn có thể tìm kiếm tài khoản và liên hệ.  
  
5. Thẻ phiên: Khi bạn đang mở nhiều phiên khách hàng, mỗi thẻ sẽ hiển thị một phiên khác nhau. Các tab khiến cho tổng đài viên dễ dàng làm việc trên nhiều trường hợp khách hàng.  
  
6. Mã lệnh gọi: Hiển thị các mã lệnh gọi mà tổng đài viên dịch vụ có thể sử dụng khi họ đang làm việc trong một trường hợp. Các mã lệnh giúp hướng dẫn các tổng đài viên bằng cách hướng dẫn cho họ từng bước cách làm thế nào để xử lý trường hợp.  
  
7. Ghi chú: Đây là khu vực để viết ghi chú liên quan đến trường hợp.  
  
8. KB search:  Use this for finding relevant knowledge base (KB) articles to link to.  
  
   Các tính năng Chỉ số Đánh giá Hiệu suất Chính bổ sung được hiển thị ở cuối máy khách [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] bao gồm:  
  
- Thời gian Giải quyết Trường hợp Trung bình (Giây). Hiển thị khoảng thời gian giải quyết trường hợp trung bình tính bằng giây cho tổng đài viên.  
  
- Số lượng trường hợp được giải quyết. Hiển thị tổng số trường hợp được giải quyết cho tổng đài viên.  
  
- Thời gian Phiên: Hiển thị thời gian tích lũy mà thẻ phiên mở.  
  
  ![unifiedservicedeskcrmwebclientpackage](../../unified-service-desk/media/unifiedservicedeskcrmwebclientpackage.png "unifiedservicedeskcrmwebclientpackage")  
  
## <a name="view-active-cases"></a>View active cases  
 From the toolbar, click **My Work** to see all of your active cases, and then select a case to work on. When you open a case, a new session opens.  
  
## <a name="create-a-case"></a>Create a case  
  
1.  Look up the contact information by clicking **search** on the toolbar.  
  
2.  In the **search** field, enter the contact or account information. Bạn cũng có thể tìm kiếm trên các thực thể khác như trường hợp, hoạt động hoặc hàng đợi.  
  
3.  Khi bạn tìm thấy thông tin liên hệ, hãy bấm vào bản ghi để mở một phiên mới.  
  
4.  Trên khu vực điều hướng **Kịch bản cuộc gọi** bên trái, sử dụng danh sách các kịch bản cuộc gọi để hướng dẫn bạn trong suốt trường hợp hỗ trợ.  Khi bạn bấm vào mã lệnh gọi, dấu kiểm xanh lục cho biết hành động đã được thực hiện.  
  
5.  Nhập ghi chú của trường hợp trong khu vực **Ghi chú**. Để đính kèm ghi chú của bạn vào trường hợp, bấm vào **Cập nhật** ghi chú từ mã lệnh gọi.  
  
## <a name="search-for-a-resolution"></a>search for a resolution  
 Để giúp giải quyết trường hợp, hãy sử dụng cửa sổ tìm kiếm bài viết trong cơ sở kiến thức để tìm ra giải pháp.  
  
1.  From the **KB search** area, enter text to search for published articles that can be used to help resolve the case.  
  
2.  Gửi liên kết qua email, liên kết bài viết với trường hợp hoặc sao chép liên kết bài viết sang bảng tạm để dán vào ứng dụng khác.  
  
## <a name="resolve-a-case"></a>Giải quyết trường hợp  
 To resolve a case, from the **Call Script** area, click the **Resolve Case** call script.  

## <a name="see-also"></a>Xem thêm  
 [Unified Service Desk Overview](../../unified-service-desk/admin/overview-unified-service-desk.md)
