---
title: Guide customer interactions with agent scripts in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Agent scripting in Unified Service Desk provides guidance to agents about what they should say on calls or what they should type on chat conversations. It includes a script that can use values from any loaded entity on the agent application, hosted control, or the Unified Service Desk context (using replacement parameters).
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
ms.assetid: 2e6af283-c0c9-4cce-92b1-88485748e0a8
caps.latest.revision: 5
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 0fec68eceb08b5a464641fb0d893b4cbeb25480c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385477"
---
# <a name="guide-customer-interactions-with-agent-scripts-in-unified-service-desk"></a>Guide customer interactions with agent scripts in Unified Service Desk
Mã lệnh tổng đài viên trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] cung cấp hướng dẫn cho các tổng đài viên về những gì họ nên nói về các cuộc gọi hoặc những gì họ nên nhập vào cuộc hội thoại trò chuyện. Nó bao gồm mã lệnh mà có thể sử dụng các giá trị từ bất kỳ thực thể được tải nào trên ứng dụng tổng đài viên, kiểm soát tổ chức, hoặc bối cảnh [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] (bằng cách sử dụng tham số thay thế). Mã lệnh tổng đài viên cũng cung cấp một cơ chế để hiển thị hướng dẫn cho tổng đài viên về cách và những gì cần thực hiện tác vụ cần thiết để hoàn thành công việc của họ.  
  
 Các mô-đun mã lệnh hỗ trợ phân nhánh cho luồng công việc tổng đại lý phi tuyến tính. Nó cũng hỗ trợ việc chuyển sang mã lệnh cụ thể dựa trên các biến như nút được xác định trong giao diện người dùng, sự kiện tích hợp điện thoại máy tính (CTI) và thông số chẳng hạn như dịch vụ xác định số được quay (DNIS). Lịch sử của các bước được giữ trong danh sách thả xuống để người dùng có thể quay trở lại bước đã truy cập trước đó. Hành động đã được thực hiện trên quá trình không hoàn tác khi tổng đài viên trở lại bước trước. Nếu câu trả lời đã được truy cập, hộp kiểm sẽ xuất hiện bên cạnh nó.  
  
## <a name="components-of-an-agent-script"></a>Thành phần của mã lệnh tổng đài viên  
 Sau đây là mã lệnh tổng đài viên mẫu trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:  
  
 ![Agent script in Unified Service Desk](../unified-service-desk/media/usd-agent-script.png "Agent script in Unified Service Desk")  
  
- **Lịch sử và bước hiện tại**: Danh sách thả xuống (chào mừng bạn đến với Phiên liên hệ) hiển thị bước hiện tại. Nếu bạn nhấp vào danh sách, bạn sẽ thấy một lịch sử về nơi bạn đã ở. Bạn có thể chọn một bước trước đó từ danh sách này để trở về nó.  
  
    > [!NOTE]
    >  Nếu bạn trở lại một điểm trước đó bằng cách sử dụng danh sách thả-xuống, hành động và đầu vào mà bạn thực hiện trên các ứng dụng trong các bước tiếp theo sẽ không thể quay lại.  
  
- **Văn bản giới thiệu**: Đây là văn bản được sử dụng bằng tổng đài viên để bắt đầu cuộc trò chuyện với khách hàng. Văn bản này hỗ trợ các tham số thay thế từ ngữ cảnh dữ liệu [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. Nếu trường này bị để trống khi bạn tạo mã lệnh tổng đài viên, phần sẽ không được trình bày trong màn hình cho tổng đài viên và tiêu đề mã lệnh sẽ bị xóa.  
  
     Nếu một cuộc hội thoại trò chuyện bắt đầu phiên, nút sẽ hiển thị bên cạnh mã lệnh tổng đài viên. Khi nút này được nhấn vào, các văn bản sẽ được sao chép vào đầu ra tương thích trò chuyện tự động.  
  
- **Hướng dẫn cho tổng đài viên**: văn bản này cung cấp hướng dẫn cho tổng đài viên về hoạt động cần được thực hiện. Nó có thể cung cấp gợi ý hoặc các hướng dẫn khác. Nếu trường này bị để trống khi bạn tạo mã lệnh tổng đài viên, tiêu đề và văn bản sẽ không hiển thị cho ứng dụng khi đang thực hiện tác vụ này. Văn bản hướng dẫn này xuất hiện trong các phông chữ khác nhau từ mã lệnh giới thiệu.  
  
- **Bước/ Câu trả lời kế tiếp**: Ngăn xếp chồng các nút này cho thấy các lựa chọn có thể cho bước tiếp theo. Một hành động có thể được thực hiện để đáp ứng với việc nhấp vào một trong các câu trả lời hoặc một hành động có thể thực hiện khi đạt đến công việc tiếp theo.  
  
  [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Configure and manage agent scripts](../unified-service-desk/configure-manage-agent-scripts.md)  
  
### <a name="see-also"></a>Xem thêm  
 [Mã lệnh tổng đài viên (Kiểm soát tổ chức)](../unified-service-desk/agent-scripting-hosted-control.md)   
 [Thông số thay thế](../unified-service-desk/replacement-parameters.md)   
 [UII Computer Telephony Integration (CTI) framework](../unified-service-desk/uii-computer-telephony-integration-cti-framework.md)   
 [Cách 7: Đặt cấu hình mã lệnh tổng đài viên trong ứng dụng tổng đài viên của bạn](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md)
