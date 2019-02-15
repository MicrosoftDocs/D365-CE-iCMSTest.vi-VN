---
title: UII Application Integration Framework | MicrosoftDocs
description: Learn information about UII Application Integration Framework that enables the integration and automation of applications.
ms.custom:
- dyn365-USD
ms.date: 11/29/2016
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
ms.assetid: 647d2d06-ca73-4951-8038-374d0ba65a2d
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
ms.openlocfilehash: 787b2edb253a85b2ff6e556373cc2648b4f9fafd
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387301"
---
# <a name="uii-application-integration-framework"></a>UII Application Integration Framework
The [!INCLUDE[pn_application_integration_framework_aif](../includes/pn-application-integration-framework-aif-md.md)] in [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-inteface-integration-uii-md.md)] enables the integration and automation of applications. Thông qua [!INCLUDE[pn_aif_acronym](../includes/pn-aif-acronym-md.md)], ứng dụng có thể được khởi chạy và tự động hóa cho nhiều mục đích, chẳng hạn như giảm bớt sao chép và dán. Nó cũng cung cấp khả năng quản lý phiên, cho phép các ứng dụng được phân lập lẫn nhau trên một phím phiên. Sự phân lập này giúp tăng cường bảo mật dữ liệu và quản lý ứng dụng dễ dàng hơn cho người dùng.  
  
 [!INCLUDE[pn_aif_acronym](../includes/pn-aif-acronym-md.md)] sử dụng các [!INCLUDE[pn_composite_ui_application_block](../includes/pn-composite-ui-application-block-md.md)] công cụ và dịch vụ để nhắn tin, ngăn chặn trực quan, tải ứng dụng và quản lý trạng thái. For more information, and to download the application block, see [MSDN:  HYPERLINK "http://msdn.microsoft.com/en-us/library/aa480450.aspx" Smart Client – Composite UI Application Block](https://msdn.microsoft.com/library/aa480450.aspx).  
  
<a name="AIFComponents"></a>   
## <a name="aif-components"></a>Thành phần AIF  
 Các hình minh họa sau cho thấy các thành phần [!INCLUDE[pn_aif_acronym](../includes/pn-aif-acronym-md.md)].  
  
 ![UII Application Integration Framework components](media/usd-aif-components.png "UII Application Integration Framework components")  
  
 Như được trình bày trong minh họa trước, [!INCLUDE[pn_aif_acronym](../includes/pn-aif-acronym-md.md)] có các thành phần chính sau:  
  
- **Ứng dụng được lưu trữ**: Ứng dụng được lưu trữ là một ứng dụng thành phần được lưu trữ trực tiếp trong vỏ [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym-md.md)]. Ứng dụng có thể là kiểm soát tổ chức, ứng dụng bên ngoài (chẳng hạn như [!INCLUDE[pn_ms_VisualC_long](../includes/pn-ms-visualc-long-md.md)], [!INCLUDE[pn_ms_Visual_Basic_long](../includes/pn-ms-visual-basic-long-md.md)] hoặc [!INCLUDE[pn_Java](../includes/pn-java-md.md)]), ứng dụng web hoặc ứng dụng được lưu trữ [!INCLUDE[pn_citrix](../includes/pn-citrix-md.md)]. Hosted controls are Windows Forms or [!INCLUDE[pn_ms_Windows_Presentation_Foundation](../includes/pn-ms-windows-presentation-foundation-md.md)] user controls that implement additional hooks to integrate into the [!INCLUDE[pn_aif_acronym](../includes/pn-aif-acronym-md.md)]. [!INCLUDE[proc_more_information](../includes/proc-more-information-md.md)] [UII Hosted Applications](uii-hosted-applications.md)  
  
- **Khung Vỏ UI**: Cung cấp khung hợp nhất để phát triển các vỏ ứng dụng máy tính để bàn hợp nhất bằng cách cung cấp các lớp dịch vụ UII cơ bản đơn giản hóa phát triển [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym-md.md)]. [!INCLUDE[proc_more_information](../includes/proc-more-information-md.md)] [UI Shell Framework](ui-shell-framework.md)  
  
- **Thành phần tổng hợp**:[!INCLUDE[pn_aif_acronym](../includes/pn-aif-acronym-md.md)] sử dụng các công cụ và dịch vụ [!INCLUDE[pn_composite_ui_application_block](../includes/pn-composite-ui-application-block-md.md)] để nhắn tin (sự kiện môi giới), ngăn chặn hình ảnh (không gian làm việc), tải ứng dụng (trình tải mô-đun) và quản lý trạng thái. Khung Tích hợp Ứng dụng thúc đẩy Khối Ứng dụng UI Tổng hợp để cung cấp chức năng và hướng dẫn cho việc xây dựng môi trường máy chủ lưu trữ có thể kết hợp và trình bày các giao diện người dùng cho mỗi ứng dụng lưu trữ trên máy. Khung Tích hợp Ứng dụng cũng cho phép các ứng dụng chia sẻ thông tin và sự kiện, do đó, thay đổi trong một ngăn có thể ảnh hưởng đến các ứng dụng được lưu trữ khác.  
  
- **Quản lý tập trung**: Cấu hình của ứng dụng được lưu trữ, hành động, quy trình làm việc và an ninh được quản lý thông qua máy khách web [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm-md.md)].  
  
<a name="AIFObjectModel"></a>   
## <a name="aif-object-model"></a>Mô hình đối tượng AIF  
 [!INCLUDE[pn_aif_acronym](../includes/pn-aif-acronym-md.md)]đưa ra một mô hình đối tượng để kích hoạt một ứng dụng vỏ, chẳng hạn như [!INCLUDE[pn_unified_service_desk_for_crm](../includes/pn-unified-service-desk-for-crm-md.md)], cho ứng dụng dòng kinh doanh. Mô hình đối tượng cũng cho phép bạn sử dụng một ngữ cảnh phiên để thực hiện tương tác giữa các ứng dụng và hành động để chuyển tin nhắn giữa chúng.  
  
 ![Application Integration Framework object model](media/usd-aif-object-model.png "Application Integration Framework object model")  
  
- `ApplicationHost`: `ApplicationHost` hoạt động dưới dạng nhà môi giới giữa ứng dụng để bàn [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym-md.md)] (chẳng hạn như [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk-md.md)]) và ứng dụng được lưu trữ. Nó cũng có thể đóng vai trò của một nhà môi giới giữa nhiều ứng dụng được lưu trữ, cho phép chúng gửi và nhận các hành động hoặc sự kiện. Các đối tượng `ApplicationHost` cho phép các ứng dụng được lưu trữ để đưa ra sự kiện, được gọi là hành động trong [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym-md.md)]. Các ứng dụng được lưu trữ chuyển các hành động đến đối tượng `ApplicationHost`, ngược lại chuyển chúng tới đích (ứng dụng được lưu trữ) của hành động. `ApplicationHost` cũng cung cấp các ứng dụng được lưu trữ với quyền truy cập vào đối tượng ngữ cảnh.  
  
- **Ngữ cảnh**: Ngữ cảnh là một tập hợp các cặp khóa-giá trị được chia sẻ giữa các ứng dụng được lưu trữ. Mỗi phiên của Khung Tích hợp Ứng dụng bao gồm một đối tượng ngữ cảnh chứa dữ liệu được người dùng xác định. Dữ liệu ngữ cảnh được chia sẻ giữa ứng dụng được lưu trữ và bộ chuyển đổi trong phiên. Một ứng dụng được lưu trữ có thể ghi một số dữ liệu (chẳng hạn như ID người dùng) vào ngữ cảnh và dữ liệu này hiển thị với các ứng dụng khác. Ngữ cảnh có thể tiếp tục tồn tại, cho phép phiên được chuyển giao cho tổng đài viên khác hoặc được truy xuất bởi tổng đài viên ban đầu.  
  
- **Phiên**: [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym-md.md)] cung cấp công cụ phiên chứa cả phiên bản ứng dụng được lưu trữ và thông tin ngữ cảnh cho phiên đó. Một phiên được sử dụng như một cấu trúc tổ chức để cho phép việc phân tách các nhóm ứng dụng được lưu trữ và dữ liệu liên kết. Dữ liệu cho một phiên có thể được nhóm thành hai danh mục chính:  
  
  - **Dữ liệu hỗ trợ chính**: Điều này bao gồm thông tin nhận dạng phiên, cấu trúc dữ liệu chính (thường là dữ liệu khách hàng), định danh kết nối [!INCLUDE[pn_computer_telephony_integration_cti](../includes/pn-computer-telephony-integration-cti-md.md)] và bất kỳ ứng dụng nào được lưu trữ trong phiên.  
  
  - **Ngữ cảnh phiên**: Đây là khu vực thông tin được chia sẻ giữa các ứng dụng được lưu trữ.  
  
    A session can be associated with any type of channel (such as a phone call, an email message, an instant messaging [IM] conversation, or another means of communication). [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym-md.md)] can be configured to permit only one session at a time or multiple, concurrent sessions. Quản lý phiên cho phép tổng đài viên xử lý nhiều tương tác đồng thời trên nhiều kênh mà không mất hoặc bị xen vào ngữ cảnh hoặc trạng thái của từng phiên.  
  
### <a name="see-also"></a>Xem thêm  
 [AifServices](https://docs.microsoft.com/dotnet/api/microsoft.uii.aifservices)   
 [IHostedApplication](https://docs.microsoft.com/dotnet/api/microsoft.uii.csr.aifinterfaces.ihostedapplication)   
 [UII Hosted Applications](uii-hosted-applications.md)   
 [Mở rộng Unified Service Desk](extend-unified-service-desk.md)   
 [Quản lý phiên trong Unified Service Desk](session-management-unified-service-desk.md)
