---
title: Delete data in bulk (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Helps maintain data quality and manage the consumption of system storage by deleting data that is no longer needed.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: get-started-article
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- bulk delete
- deleting data in bulk in Microsoft Dynamics CRM, about the bulk deletion feature
- deleting data in bulk in Microsoft Dynamics CRM, how the bulk deletion feature helps you delete multiple topics
- bulk deletion feature, about
- deleting data in bulk in Microsoft Dynamics CRM, data cleanup (periodic and scheduled)
- deleting data in bulk in Microsoft Dynamics CRM, tasks for using bulk deletion
- deleting data in bulk in Microsoft Dynamics CRM, failure log
- bulk deletion
- deleting data in bulk in Microsoft Dynamics CRM, email notifications
ms.assetid: 67a3a031-4edf-49de-983b-ba9902223278
caps.latest.revision: 25
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ed981b3778447984bea2400a1bc67c7553f58415
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388438"
---
# <a name="delete-data-in-bulk"></a>Delete data in bulk

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

Tính năng *xóa hàng loạt* giúp bạn duy trì chất lượng dữ liệu và quản lý việc tiêu thụ lưu trữ hệ thống trong [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] bằng cách xoá dữ liệu mà bạn không còn cần.  
  
 Ví dụ, bạn có thể xoá dữ liệu sau với số lượng lớn:  
  
- Dữ liệu cũ.  
  
- Dữ liệu mà không liên quan đến kinh doanh.  
  
- Thử nghiệm không cần thiết hoặc dữ liệu mẫu.  
  
- Dữ liệu không được nhập chính xác từ các hệ thống khác.  
  
  Với xóa hàng loạt, bạn có thể thực hiện thao tác sau:  
  
- Xóa dữ liệu trên nhiều thực thể.  
  
- Xoá hồ sơ cho một thực thể được chỉ định.  
  
- Nhận thông báo email khi xóa hàng loạt kết thúc.  
  
- Xoá dữ liệu định kỳ.  
  
- Lên lịch thời gian bắt đầu cho xóa hàng loạt định kỳ.  
  
- Truy xuất thông tin về những thất bại xảy ra trong xóa hàng loạt.  
  
## <a name="in-this-section"></a>In This Section  
 [Running Bulk Delete](run-bulk-delete.md)  
  
 [BulkDeleteOperation Entity](entities/bulkdeleteoperation.md)  
  
 [BulkDeleteFailure Entity](entities/bulkdeletefailure.md)  
  
## <a name="related-sections"></a>Các phần liên quan  

 [Data Management](manage-data.md)  
  
 [Nhập dữ liệu](import-data.md)
