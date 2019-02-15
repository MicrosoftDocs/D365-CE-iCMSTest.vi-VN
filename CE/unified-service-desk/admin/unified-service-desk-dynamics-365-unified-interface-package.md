---
title: Unified Service Desk for Dynamics 365 for Customer Engagement apps Unified Interface package | MicrosoftDocs
description: Overview of the Unified Interface sample application.
keywords: ''
ms.date: 08/17/2018
ms.service:
- crm-online
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
- Dynamics CRM Online
ms.assetid: FA01CA74-AD17-44A1-8AAD-C296B549F8A2
author: kabala123
ms.author: kabala
manager: shujoshi
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 85130adaa3d7cece5f46ee4054bbfa1f4a7b41cb
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382592"
---
# <a name="unified-interface-sample-application-package"></a>Unified Interface sample application package
[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] is a desktop application that helps your customer service agents provide phone, email, and chat support to your customers. [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] provides a configurable framework to quickly build an Agent Desktop application that’s integrated with [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps. With [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] you can quickly make a customized Agent Desktop application by leveraging the User Interface Integration (UII) framework. Gói này được sử dụng hiệu quả nhất trong các trường hợp sau:  
  
- To demonstrate the rich set of customer service capabilities in [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps and simplify the customization of your agent desktop application.  
  
  With the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] Dynamics 365 for Customer Engagement apps Web Client sample application package, the following components are installed:  
  
- Unified Service Desk Administrator App (Public preview feature)
::: moniker-end

- User Interface Integration Solution 
  
- Unified Service Desk Solution

::: moniker range="dynamics-usd-4"

- Customizations for [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps Unified Interface package

::: moniker-end 

- Data required for [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps and customizations
  
- The following sample hosted controls  
  
  -   KPI Custom Control  
  
  -   Hệ thống Thông tin Khách hàng  
  
> [!IMPORTANT]
>  The sample applications aren't supported for production use.  
  
  
 Here’s what you’ll see when you install the Dynamics 365 for Customer Engagement apps Unified Interface package:  
  
1. Left Nav: Opens the left navigation area that you can open or collapse.  
  
2. Bảng thông tin: Mở bảng thông tin dịch vụ khách hàng [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)].  

> [!NOTE]
> During login, if you choose Customer Service Hub, customer service dashboard appears in the Dashboard area. 
  
3. My Work: Shows a list of all active cases assigned to a service rep.  
  
4. search tab: Opens search for navigating through various entities. Đối với gói này, bạn có thể tìm kiếm tài khoản và liên hệ.  
  
5. Thẻ phiên: Khi bạn đang mở nhiều phiên khách hàng, mỗi thẻ sẽ hiển thị một phiên khác nhau. Các tab khiến cho tổng đài viên dễ dàng làm việc trên nhiều trường hợp khách hàng.  
  
6. Mã lệnh gọi: Hiển thị các mã lệnh gọi mà tổng đài viên dịch vụ có thể sử dụng khi họ đang làm việc trong một trường hợp. Các mã lệnh giúp hướng dẫn các tổng đài viên bằng cách hướng dẫn cho họ từng bước cách làm thế nào để xử lý trường hợp.  
  
7. Notes: This is the area to take notes in regarding the case.  
  
8. KB search:  Use this for finding relevant knowledge base (KB) articles to link to.  
  
   Các tính năng Chỉ số Đánh giá Hiệu suất Chính bổ sung được hiển thị ở cuối máy khách [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] bao gồm:  
  
-   Thời gian Giải quyết Trường hợp Trung bình (Giây). Hiển thị khoảng thời gian giải quyết trường hợp trung bình tính bằng giây cho tổng đài viên.  
  
-   Số lượng trường hợp được giải quyết. Hiển thị tổng số trường hợp được giải quyết cho tổng đài viên.  
  
-   Thời gian Phiên: Hiển thị thời gian tích lũy mà thẻ phiên mở.  
  
  
## <a name="view-active-cases"></a>Xem các trường hợp hiện hoạt  
 Từ thanh công cụ, bấm vào **Công việc của tôi** để xem tất cả các trường hợp hiện hoạt rồi chọn một trường hợp để làm việc. When you open a case, a new session opens.  
  
## <a name="create-a-case"></a>Create a case  
  
1.  Look up the contact information by clicking **search** on the toolbar.  
  
2.  In the **search** field, enter the contact or account information. You can also search on other entities such as cases, activities, or queues.  
  
3.  Khi bạn tìm thấy thông tin liên hệ, hãy bấm vào bản ghi để mở một phiên mới.  
  
4.  Trên khu vực điều hướng **Kịch bản cuộc gọi** bên trái, sử dụng danh sách các kịch bản cuộc gọi để hướng dẫn bạn trong suốt trường hợp hỗ trợ.  Khi bạn bấm vào mã lệnh gọi, dấu kiểm xanh lục cho biết hành động đã được thực hiện.  
  
5.  Nhập ghi chú của trường hợp trong khu vực **Ghi chú**. To attach your notes to the case, click **Update** notes from call scripts.  
  
## <a name="search-for-a-resolution"></a>search for a resolution  
 To help resolve the case, use the knowledge base articles search window to find a solution.  
  
1.  From the **KB search** area, enter text to search for published articles that can be used to help resolve the case.  
  
2.  Gửi liên kết qua email, liên kết bài viết với trường hợp hoặc sao chép liên kết bài viết sang bảng tạm để dán vào ứng dụng khác.  
  
## <a name="resolve-a-case"></a>Giải quyết trường hợp  
 To resolve a case, from the **Call Script** area, click the **Resolve Case** call script.  

## <a name="see-also"></a>Xem thêm  
 [Unified Service Desk Overview](../../unified-service-desk/admin/overview-unified-service-desk.md)
