---
title: Accessibility in Unified Service Desk for Microsoft Dynamics 365 for Customer Engagement apps | MicrosoftDocs
description: Learn about accessiblity features such as keyboard access and screen reader support.
ms.custom:
- dyn365-a11y
- dyn365-USD, dyn365-admin
ms.date: 08/23/2017
ms.reviewer: ''
ms.service: dynamics-365-customerservice
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Unified Service Desk 3.x
ms.assetid: f43d9d0d-50fa-4ffa-908a-e592b40371b4
author: kabala123
ms.author: kabala
tags:
- MigrationHO
manager: shujoshi
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
ms.openlocfilehash: e8285cd2ea7c4ad6d4bb9c51eb028dcd61380ce9
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382466"
---
# <a name="accessibility-features-in-unified-service-desk"></a>Accessibility features in Unified Service Desk
Microsoft cam kết làm cho các sản phẩm và dịch vụ của mình dễ dàng hơn cho tất cả mọi người. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Khả năng truy cập Microsoft](http://www.microsoft.com/enable/default.aspx)  
  
  
<a name="KeyboardAccess"></a>   
## <a name="keyboard--access-in-the-unified-service-desk-client"></a>Keyboard  access in the Unified Service Desk client  
 [!INCLUDE[pn_unified_service_desk_for_crm](../../includes/pn-unified-service-desk-for-crm.md)] offers keyboard navigation to help address issues faced by people with disabilities. Also, people who don’t use a mouse can use their keyboard to navigate in some areas of the [!INCLUDE[pn_unified_service_desk_for_crm](../../includes/pn-unified-service-desk-for-crm.md)] client.  
  
|Tới|Select|  
|--------|-----------|  
|Move from left to right and top to bottom towards the next control, option, option group, or field.|Thẻ|  
|Move from right to left and bottom to top towards the next control, option, option group, or field.|Shift + Tab|  
|Complete the command for the active, control, option, or button|Phím Enter|  
|Cyclically navigates through all the active panels.|Ctrl + 0|  
|Changes the focus from an IE Process hosted control to the main window.|Alt + 0|  
|Navigates through all active notifications in a cyclical manner.|Alt + 1|  
  
 If the Alt + 0  key combination  is assigned as a shortcut in any other application, you can use the IEProcessKeyboardShortcut option in Unified Service Desk to assign a different key combination for moving out of an IE Process hosted control. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Manage Options for Unified Service Desk](../../unified-service-desk/admin/manage-options-unified-service-desk.md).  
  
 If the Alt + 1  key combination  is assigned as a shortcut in any other application, you can use the PopupCycleShortcut option in Unified Service Desk to assign a different key combination for moving out of an IE Process hosted control. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Manage Options for Unified Service Desk](../../unified-service-desk/admin/manage-options-unified-service-desk.md).  
  
<a name="SplashScreen"></a>   
## <a name="keyboard-access-to-the-splash-screen"></a>Quyền truy cập bàn phím cho màn hình bật lên  
 Use the Tab key to navigate to the Change Credentials link in the [!INCLUDE[pn_unified_service_desk_for_crm](../../includes/pn-unified-service-desk-for-crm.md)] splash screen so you can view the login page.  
  
<a name="HighContrast"></a>   
## <a name="high-contrast-mode-in-the--unified-service-desk-client"></a>High contrast mode in the  Unified Service Desk client  
 Thiết đặt độ tương phản cao trong [!INCLUDE[pn_ms_Windows_long](../../includes/pn-ms-windows-long.md)] sẽ tăng cường độ tương phản màu sắc của một số văn bản và hình ảnh trên màn hình của bạn, làm cho những hình ảnh hoặc văn bản này dễ phân biệt và xác định hơn. Bạn sẽ tìm thấy thiết đặt này trên **trang Trợ năng** ở Bảng Điều khiển trong [!INCLUDE[pn_windows_10](../../includes/pn-windows-10.md)], [!INCLUDE[pn_windows8](../../includes/pn-windows8.md)] và [!INCLUDE[pn_Windows_7](../../includes/pn-windows-7.md)].  If you’re using the high contrast setting in  Windows, high contrast in the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client also becomes enabled. Và nếu bạn thay đổi chế độ tương phản cao trong Windows trong khi máy khách [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] đang chạy, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] cũng sẽ chuyển sang chế độ tương phản cao.  
  
 Note that there are two  themes available in earlier versions of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], Blue and Style, are no longer available because they  do not support high contrast mode.  
  
<a name="ScreenReader"></a>   
## <a name="screen--reader-support"></a>Screen  reader support  
 All out-of-box [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] hosted controls and custom controls that are included in the Dynamics 365 for Customer Engagement apps Web Client sample application package work with JAWS version 18 to provide speech output.  
  
 For information about how developers can extend custom hosted controls or hosted controls in the other [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] sample application packages to support the JAWS screen reader, see [Configure JAWS Screen Reader in Unified Service Desk](../configure-jaws-screen-reader-support.md).  
