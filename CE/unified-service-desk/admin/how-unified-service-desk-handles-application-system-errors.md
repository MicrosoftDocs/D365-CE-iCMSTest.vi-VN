---
title: How Unified Service Desk for Dynamics 365 for Customer Engagement apps handles application and system errors | MicrosoftDocs
description: Understand how application and system faults are managed in Unifed Service Desk.
ms.custom:
- dyn365-USD, dyn365-admin
ms.date: 08/23/2017
ms.prod: usd2.0
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Unified Service Desk 2.0
ms.assetid: 01878a81-2b67-44ab-a11d-b19adc407177
caps.latest.revision: 5
author: kabala123
ms.author: kabala
ms.service: dynamics-365-customerservice
manager: shujoshi
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
ms.openlocfilehash: b052e5cfa96cda2594d1e28510a35ceac7942450
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382482"
---
# <a name="application-and-system-faults"></a>Application and system faults
Việc thu thập báo cáo và nhật ký chi tiết, toàn diện về lỗi khi bị trục trặc về thành phần, ứng dụng hoặc hệ thống có thể giúp xác định thời điểm và cách thức diễn ra lỗi. Máy khách [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] có thể ghi lại nhật ký chẩn đoán, chi tiết trạng thái hệ thống và ứng dụng cũng như kết xuất bộ nhớ hệ thống trong trường hợp ngoại lệ trong máy khác [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].  
  
> [!NOTE]
> - Các tính năng báo cáo chẩn đoán lỗi được mô tả tại đây lần đầu được giới thiệu trong [!INCLUDE[pn_unified_service_desk_2_2dot2](../../includes/pn-unified-service-desk-2-2dot2.md)].  
>   -   For more information about the error diagnostics reporting files that are mentioned here, see [Error diagnostics reporting](../../unified-service-desk/admin/configure-client-diagnostic-logging-unified-service-desk.md#exceptionlogging).  
  
 
<a name="typesofexceptions"></a>   
## <a name="types-of-exceptions"></a>Các loại ngoại lệ  
 Các ngoại lệ có thể là nghiêm trọng hoặc không nghiêm trọng.  
  
### <a name="fatal-exceptions"></a>Các ngoại lệ nghiêm trọng  
 Đây là những sự cố máy khách [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] không thể giải quyết hoặc bỏ qua và thường khiến ứng dụng thoát hoặc không phản hồi. Ví dụ về ngoại lệ nghiêm trọng được xử lý là trường hợp khi hệ thống hết bộ nhớ. Ví dụ về ngoại lệ nghiêm trọng không được xử lý là tràn ngăn xếp hệ điều hành. Khi ngoại lệ nghiêm trọng diễn ra, máy khách [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] phải khởi động lại để tiếp tục.  
  
 ![Unified Service Desk exception dialog](../../unified-service-desk/media/usd-exception-dialog.jpg "Unified Service Desk exception dialog")  
  
 Việc bấm vào **Có** trên hộp hội thoại lỗi sẽ bắt đầu tập hợp các tệp báo cáo chẩn đoán lỗi và khởi động lại máy khách [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]. Clicking **No** begins the collection of the error diagnostics reporting files but does not restart the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client.  
  
 Tiếp theo, hộp thoại này sẽ xuất hiện trong vài giây để bạn có thể bấm vào **Hủy** nếu không muốn tệp tràn bộ nhớ được tạo. Nếu không bấm vào Hủy, một tệp tràn bộ nhớ đầy đủ của quá trình [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] sẽ được tạo.  
  
 ![Unified Service Desk dump file collection](../../unified-service-desk/media/usd-dump-file-collection.jpg "Unified Service Desk dump file collection")  
  
> [!NOTE]
>  Các tệp tràn bộ nhớ lớn và yêu cầu số lượng lớn tài nguyên bộ xử lý và RAM trên máy tính để hoàn tất.  
  
### <a name="non-fatal-exceptions"></a>Các ngoại lệ không nghiêm trọng  
 Đây là những sự cố được máy khách [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] xử lý và thường không gây mất ổn định đối với ứng dụng. Ví dụ về ngoại lệ không nghiêm trọng là khi kiểm soát tổ chức đưa ra yêu cầu không hợp lệ, chẳng hạn như chia cho 0. Khi ngoại lệ không nghiêm trọng diễn ra, thường thì máy khách [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] có thể tiếp tục chạy. Bấm vào **Có** trên hộp thoại để thu thập nhật ký thoát báo cáo chẩn đoán lỗi (các tệp tràn bộ nhớ không được thu thập) và khởi động lại máy khách [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]. Click **No** to continue working in the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client without collecting any error diagnostics reporting files.  
  
 ![Unified Service Desk non-fatal exception dialog](../../unified-service-desk/media/usd-nonfatal-exception.jpg "Unified Service Desk non-fatal exception dialog")  
  
<a name="ondemandDump"></a>   
## <a name="create-a-memory-dump-on-demand"></a>Tạo tràn bộ nhớ theo yêu cầu  
 Bất kỳ lúc nào, các tác nhân đang chạy [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] có thể thu hồi tràn bộ nhớ đầy đủ theo yêu cầu của ứng dụng máy khách [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]. Theo mặc định, tổ hợp phím tắt để thu hồi việc tạo thủ công tệp tràn là CTRL+ALT+a.  
  
> [!NOTE]
>  Memory dump files are large and require a significant amount of processor and RAM computer resources  to complete.  
  
## <a name="see-also"></a>Xem thêm  
 [Manage Options for Unified Service Desk](../../unified-service-desk/admin/manage-options-unified-service-desk.md)
