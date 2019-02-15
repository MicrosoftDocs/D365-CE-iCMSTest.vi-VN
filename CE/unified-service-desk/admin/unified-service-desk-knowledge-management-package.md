---
title: Unified Service Desk for Dynamics 365 for Customer Engagement apps – Knowledge Management package | MicrosoftDocs
description: Overview of the Knowledge Management sample application.
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
ms.assetid: 5937df93-dcbc-4024-a46c-6afbe61f4359
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 98cc3d812f94e6bdbe39905b37fab4686a888746
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382509"
---
# <a name="knowledge-management-sample-application-package"></a>Knowledge Management sample application package 
[!INCLUDE[pn_unified_service_desk_for_crm](../../includes/pn-unified-service-desk-for-crm.md)] provides a configurable framework for quickly building applications for call centers so the customer service reps get a unified view of the customer data stored in [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps or any other application.  
  
 Nếu bạn là đại diện dịch vụ, bạn có thể sử dụng [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] để cung cấp cho khách hàng của bạn trải nghiệm đáng tin cậy và nhất quán trong giữa nhiều kênh khác nhau bao gồm điện thoại, email và trò chuyện và bạn cũng có thể phục vụ đồng thời nhiều khách hàng thông qua phiên. Một quản trị viên hệ thống trong tổ chức của bạn có thể tích hợp với Unified Service Desk nhiều ứng dụng khác mà bạn sử dụng hàng ngày để bạn có thể hoàn thành công việc c từ máy tính của bạn mà không cần chuyển sang các ứng dụng khác nhau.  
  
 The [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] Knowledge Management sample application package provides a configuration for integrating [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps with the [!INCLUDE[pn_parature](../../includes/pn-parature.md)] knowledge base that lets you easily search for articles from your desktop and share them with customers right away, reducing call handling times and improving customer satisfaction.  
  
> [!IMPORTANT]
>  Ứng dụng mẫu không được hỗ trợ cho sản xuất.  
> 
>  This sample application is useful only if you have set up knowledge management for [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Set up knowledge management with a knowledge base](https://technet.microsoft.com/library/dn946909.aspx)  
  
 Với gói [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] Quản lý Kiến thức, các thành phần sau đây được cài đặt:  
  
- User Interface Integration Solution  
  
- [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] Giải pháp  
  
- Data required for [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps and customizations  
  
- Cấu hình để tích hợp [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] với quản lý kiến thức  
   
  
 Dưới đây là những gì bạn sẽ nhìn thấy khi bạn cài đặt [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]:  
  
1. **Bảng thông tin**: Mở bảng thông tin dịch vụ khách hàng [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)].  
  
2. **Công việc của tôi**: Hiển thị danh sách tất cả trường hợp hiện hoạt được gán cho một đại diện dịch vụ.  
  
3. **search**: Opens search for navigating through various entities. Với gói này bạn có thể tìm kiếm khách hàng, người liên hệ, trường hợp, hoạt động và hàng.  
  
4. **Thẻ phiên**: Mỗi thẻ hiển thị một phiên làm việc khác nhau khi bạn có nhiều phiên khách hàng cùng ở chế độ mở. Các thẻ khiến cho đại diện dễ dàng làm việc trên nhiều trường hợp khách hàng.  
  
5. **Ngăn trái**: Khi bạn mở phiên họp bất kỳ, vùng ngăn trái tự động mở ra và cho thấy kịch bản cuộc gọi cho phiên. Bạn có thể mở hoặc thu hẹp cửa sổ này.  
  
6. **Cửa sổ bên phải**: khi bạn mở phiên bất kỳ, cửa sổ bên phải tự động mở và cho phép bạn tìm kiếm các bài viết cơ sở kiến thức.  
  
7. **Mã lệnh gọi**: Hiển thị các mã lệnh gọi mà đại diện dịch vụ có thể sử dụng khi họ đang làm việc trong một trường hợp. Các mã lệnh giúp hướng dẫn các đại diện bằng cách hướng dẫn cho họ từng bước cách làm thế nào để xử lý trường hợp.  
  
8. **Ghi chú**: Thể hiện khu vực để viết ghi chú liên quan đến trường hợp.  
  
9. **Bộ đếm thời gian phiên**: Hiển thị thời gian đại diện dịch vụ đã ở phiên đó bao lâu.  
  
   ![Account session in Unified Service Desk](../../unified-service-desk/media/account-session-unified-service-desk.png "Account session in Unified Service Desk")  
  
## <a name="view-your-cases"></a>Xem trường hợp của bạn  
  
-   Từ thanh công cụ, bấm vào **Công việc của Tôi** để xem tất cả các trường hợp của bạn.  
  
## <a name="create-a-case"></a>Tạo trường hợp  
 Tra cứu thông tin người liên hệ.  
  
1.  From the toolbar, click **search**.  
  
     Một tab ứng dụng sẽ mở ra với một danh sách các hồ sơ.  
  
2.  In the **search for records** box, enter the account or contact information.  
  
3.  Khi bạn tìm thấy thông tin, bấm vào hồ sơ để mở phiên mới.  
  
4.  Trên khu vực điều hướng **Kịch bản cuộc gọi** bên trái, sử dụng danh sách các kịch bản cuộc gọi để hướng dẫn bạn trong suốt trường hợp hỗ trợ.   
  
     Khi bạn mở mã lệnh gọi, dấu kiểm xanh lục hiển thị để cho biết hành động đã được thực hiện.  
  
5.  Nhập ghi chú của trường hợp trong khu vực **Ghi chú**. Để gắn ghi chú của bạn với trường hợp, bấm vào **Cập nhật ghi chú** từ mã lệnh gọi.  
  
## <a name="search-for-solutions"></a>Tìm kiếm giải pháp  
 Để giúp bạn giải quyết một trường hợp, sử dụng bài viết cơ sở kiến thức để tìm giải pháp.  
  
1.  From the **Call script** area, click **search for a solution**.  
  
     Ngăn **Bản ghi KB** hiển thị quả tìm kiếm dựa trên tiêu đề của trường hợp. Theo mặc định, các cửa sổ được cấu hình để mở trong bảng bên phải, nhưng bạn có thể nói chuyện với người quản trị để mở cửa sổ này trong bảng điều khiển bên trái hoặc chính.  
  
2.  To do a different search, use the **search** box to type a keyword and search for other articles.  
  
3.  Trong kết quả tìm kiếm, chọn bài viết bằng cách chọn blurb bài viết và thực hiện một trong những điều sau đây:  
  
    -   To copy the URL of the article, click the **Copy Link** button ![Copy knowledge article link button Dynamics 365 for Customer Engagement apps](../../unified-service-desk/media/copy-link-button.png "Copy knowledge article link button Dynamics 365 for Customer Engagement apps"). Sau đó, bạn có thể dán vào phiên trò chuyện với khách hàng hoặc trong phần thân email.  
  
        > [!NOTE]
        >  Nếu bạn không nhìn thấy URL khi bạn dán, nguyên nhân có thể do bài viết vẫn đang ở trạng thái không chính thức hoặc hết hạn.  
  
    -   To send the link of the article to a customer, click the **Send Email**  button ![Case origin button for email](../../unified-service-desk/media/case-origin-email-button.png "Case origin button for email").  
  
         Một mẫu email mở ra có dữ liệu được điền sẵn.  
  
    -   To link the article with the case, click the **Link Article** button ![Link knowledge article to current case button in Dynamics 365 for Customer Engagement apps](../../unified-service-desk/media/link-article-current-record.png "Link knowledge article to current case button in Dynamics 365 for Customer Engagement apps").  
  
         Liên kết các bài viết tới trường hợp giúp xác định bài viết nào hiệu quả khi giải quyết trường hợp. You can also dissociate the article from the case by clicking the **Remove Link** button ![Unlink knowledge article from current record button in Dynamics 365 for Customer Engagement apps](../../unified-service-desk/media/unlink-article.png "Unlink knowledge article from current record button in Dynamics 365 for Customer Engagement apps").  
  
    -   Để mở bài viết trong một tab mới trong bảng điều khiển chính và đọc nội dung, bấm vào tiêu đề bài viết.  
  
         Tất cả hành động như **Sao chép Liên kết** hoặc **Gửi Email** đều có sẵn trên tab mới này.  
  
    -   Additionally, to open the article in a new browser window, click the **Pop Out** button ![Pop out knowledge article in a new window button in Dynamics 365 for Customer Engagement apps](../../unified-service-desk/media/pop-out-article.png "Pop out knowledge article in a new window button in Dynamics 365 for Customer Engagement apps"). Nút này chỉ có sẵn trong bảng điều khiển chính và đặc biệt hữu ích khi bạn đang sử dụng nhiều màn hình. Bạn có thể bật ra một bài viết và xem bài viết trên một màn hình thứ hai để bạn có thể tiếp tục sử dụng màn hình đầu tiên để làm việc về vụ án hoặc ghi chú. While going through the article, you can click a link to go to a different page, and use the **Back** button ![Back button in Unified Service Desk](../../unified-service-desk/media/back-arrow-button.png "Back button in Unified Service Desk") to go back to the original article.  
  
    > [!TIP]
    >  Your system administrator can also set up the search control to search automatically based on certain criteria as soon as you open a session. Để biết thêm chi tiết về việc này, hãy nói chuyện với người quản trị hệ thống của bạn.  
  
## <a name="send-an-email"></a>Gửi một email  
  
-   Từ danh sách mã lệnh gọi, chọn mã lệnh gọi **Gửi email** và chọn một mẫu tự động chuyển đến phần nội dung của email.  
  
## <a name="update-the-notes"></a>Cập nhật ghi chú  
  
- Nhập ghi chú của trường hợp trong khu vực **Ghi chú**.  
  
- Từ danh sách các tập lệnh gọi, chọn các tập lệnh gọi **Cập nhật các ghi chú**. This will attach the notes you’ve taken during your conversation with the customer to the **Notes** tab of the case record in [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.  
  
## <a name="close-the-session"></a>Đóng phiên  
 Từ danh sách các tập lệnh gọi, chọn các tập lệnh gọi **Đóng phiên**. Điều này sẽ đóng phiên mở và thu gọn ngăn bên trái cho thấy các tập lệnh gọi và bảng bên phải cho phép bạn tìm kiếm các bài viết KB.  
  
## <a name="see-also"></a>Xem thêm  
 [Unified Service Desk Overview](../../unified-service-desk/admin/overview-unified-service-desk.md)
