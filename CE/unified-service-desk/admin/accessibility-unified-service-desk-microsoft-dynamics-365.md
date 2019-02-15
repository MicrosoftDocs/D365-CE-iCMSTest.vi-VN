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
# <a name="accessibility-features-in-unified-service-desk"></a><span data-ttu-id="f36ae-103">Accessibility features in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="f36ae-103">Accessibility features in Unified Service Desk</span></span>
<span data-ttu-id="f36ae-104">Microsoft cam kết làm cho các sản phẩm và dịch vụ của mình dễ dàng hơn cho tất cả mọi người.</span><span class="sxs-lookup"><span data-stu-id="f36ae-104">Microsoft is committed to making its products and services easier for everyone.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="f36ae-105">[Khả năng truy cập Microsoft](http://www.microsoft.com/enable/default.aspx)</span><span class="sxs-lookup"><span data-stu-id="f36ae-105">[Microsoft accessibility](http://www.microsoft.com/enable/default.aspx)</span></span>  
  
  
<a name="KeyboardAccess"></a>   
## <a name="keyboard--access-in-the-unified-service-desk-client"></a><span data-ttu-id="f36ae-106">Keyboard  access in the Unified Service Desk client</span><span class="sxs-lookup"><span data-stu-id="f36ae-106">Keyboard  access in the Unified Service Desk client</span></span>  
 [!INCLUDE[pn_unified_service_desk_for_crm](../../includes/pn-unified-service-desk-for-crm.md)] <span data-ttu-id="f36ae-107">offers keyboard navigation to help address issues faced by people with disabilities.</span><span class="sxs-lookup"><span data-stu-id="f36ae-107">offers keyboard navigation to help address issues faced by people with disabilities.</span></span> <span data-ttu-id="f36ae-108">Also, people who don’t use a mouse can use their keyboard to navigate in some areas of the [!INCLUDE[pn_unified_service_desk_for_crm](../../includes/pn-unified-service-desk-for-crm.md)] client.</span><span class="sxs-lookup"><span data-stu-id="f36ae-108">Also, people who don’t use a mouse can use their keyboard to navigate in some areas of the [!INCLUDE[pn_unified_service_desk_for_crm](../../includes/pn-unified-service-desk-for-crm.md)] client.</span></span>  
  
|<span data-ttu-id="f36ae-109">Tới</span><span class="sxs-lookup"><span data-stu-id="f36ae-109">To</span></span>|<span data-ttu-id="f36ae-110">Select</span><span class="sxs-lookup"><span data-stu-id="f36ae-110">Select</span></span>|  
|--------|-----------|  
|<span data-ttu-id="f36ae-111">Move from left to right and top to bottom towards the next control, option, option group, or field.</span><span class="sxs-lookup"><span data-stu-id="f36ae-111">Move from left to right and top to bottom towards the next control, option, option group, or field.</span></span>|<span data-ttu-id="f36ae-112">Thẻ</span><span class="sxs-lookup"><span data-stu-id="f36ae-112">Tab</span></span>|  
|<span data-ttu-id="f36ae-113">Move from right to left and bottom to top towards the next control, option, option group, or field.</span><span class="sxs-lookup"><span data-stu-id="f36ae-113">Move from right to left and bottom to top towards the next control, option, option group, or field.</span></span>|<span data-ttu-id="f36ae-114">Shift + Tab</span><span class="sxs-lookup"><span data-stu-id="f36ae-114">Shift + Tab</span></span>|  
|<span data-ttu-id="f36ae-115">Complete the command for the active, control, option, or button</span><span class="sxs-lookup"><span data-stu-id="f36ae-115">Complete the command for the active, control, option, or button</span></span>|<span data-ttu-id="f36ae-116">Phím Enter</span><span class="sxs-lookup"><span data-stu-id="f36ae-116">Enter</span></span>|  
|<span data-ttu-id="f36ae-117">Cyclically navigates through all the active panels.</span><span class="sxs-lookup"><span data-stu-id="f36ae-117">Cyclically navigates through all the active panels.</span></span>|<span data-ttu-id="f36ae-118">Ctrl + 0</span><span class="sxs-lookup"><span data-stu-id="f36ae-118">Ctrl + 0</span></span>|  
|<span data-ttu-id="f36ae-119">Changes the focus from an IE Process hosted control to the main window.</span><span class="sxs-lookup"><span data-stu-id="f36ae-119">Changes the focus from an IE Process hosted control to the main window.</span></span>|<span data-ttu-id="f36ae-120">Alt + 0</span><span class="sxs-lookup"><span data-stu-id="f36ae-120">Alt + 0</span></span>|  
|<span data-ttu-id="f36ae-121">Navigates through all active notifications in a cyclical manner.</span><span class="sxs-lookup"><span data-stu-id="f36ae-121">Navigates through all active notifications in a cyclical manner.</span></span>|<span data-ttu-id="f36ae-122">Alt + 1</span><span class="sxs-lookup"><span data-stu-id="f36ae-122">Alt + 1</span></span>|  
  
 <span data-ttu-id="f36ae-123">If the Alt + 0  key combination  is assigned as a shortcut in any other application, you can use the IEProcessKeyboardShortcut option in Unified Service Desk to assign a different key combination for moving out of an IE Process hosted control.</span><span class="sxs-lookup"><span data-stu-id="f36ae-123">If the Alt + 0  key combination  is assigned as a shortcut in any other application, you can use the IEProcessKeyboardShortcut option in Unified Service Desk to assign a different key combination for moving out of an IE Process hosted control.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="f36ae-124">[Manage Options for Unified Service Desk](../../unified-service-desk/admin/manage-options-unified-service-desk.md).</span><span class="sxs-lookup"><span data-stu-id="f36ae-124">[Manage Options for Unified Service Desk](../../unified-service-desk/admin/manage-options-unified-service-desk.md).</span></span>  
  
 <span data-ttu-id="f36ae-125">If the Alt + 1  key combination  is assigned as a shortcut in any other application, you can use the PopupCycleShortcut option in Unified Service Desk to assign a different key combination for moving out of an IE Process hosted control.</span><span class="sxs-lookup"><span data-stu-id="f36ae-125">If the Alt + 1  key combination  is assigned as a shortcut in any other application, you can use the PopupCycleShortcut option in Unified Service Desk to assign a different key combination for moving out of an IE Process hosted control.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="f36ae-126">[Manage Options for Unified Service Desk](../../unified-service-desk/admin/manage-options-unified-service-desk.md).</span><span class="sxs-lookup"><span data-stu-id="f36ae-126">[Manage Options for Unified Service Desk](../../unified-service-desk/admin/manage-options-unified-service-desk.md).</span></span>  
  
<a name="SplashScreen"></a>   
## <a name="keyboard-access-to-the-splash-screen"></a><span data-ttu-id="f36ae-127">Quyền truy cập bàn phím cho màn hình bật lên</span><span class="sxs-lookup"><span data-stu-id="f36ae-127">Keyboard access to the splash screen</span></span>  
 <span data-ttu-id="f36ae-128">Use the Tab key to navigate to the Change Credentials link in the [!INCLUDE[pn_unified_service_desk_for_crm](../../includes/pn-unified-service-desk-for-crm.md)] splash screen so you can view the login page.</span><span class="sxs-lookup"><span data-stu-id="f36ae-128">Use the Tab key to navigate to the Change Credentials link in the [!INCLUDE[pn_unified_service_desk_for_crm](../../includes/pn-unified-service-desk-for-crm.md)] splash screen so you can view the login page.</span></span>  
  
<a name="HighContrast"></a>   
## <a name="high-contrast-mode-in-the--unified-service-desk-client"></a><span data-ttu-id="f36ae-129">High contrast mode in the  Unified Service Desk client</span><span class="sxs-lookup"><span data-stu-id="f36ae-129">High contrast mode in the  Unified Service Desk client</span></span>  
 <span data-ttu-id="f36ae-130">Thiết đặt độ tương phản cao trong [!INCLUDE[pn_ms_Windows_long](../../includes/pn-ms-windows-long.md)] sẽ tăng cường độ tương phản màu sắc của một số văn bản và hình ảnh trên màn hình của bạn, làm cho những hình ảnh hoặc văn bản này dễ phân biệt và xác định hơn.</span><span class="sxs-lookup"><span data-stu-id="f36ae-130">The high contrast setting in [!INCLUDE[pn_ms_Windows_long](../../includes/pn-ms-windows-long.md)] increases the color contrast of some text and images on your screen, making them more distinct and easier to identify.</span></span> <span data-ttu-id="f36ae-131">Bạn sẽ tìm thấy thiết đặt này trên **trang Trợ năng** ở Bảng Điều khiển trong [!INCLUDE[pn_windows_10](../../includes/pn-windows-10.md)], [!INCLUDE[pn_windows8](../../includes/pn-windows8.md)] và [!INCLUDE[pn_Windows_7](../../includes/pn-windows-7.md)].</span><span class="sxs-lookup"><span data-stu-id="f36ae-131">You’ll find this setting on the **Ease of Access page** in the Control Panel in [!INCLUDE[pn_windows_10](../../includes/pn-windows-10.md)], [!INCLUDE[pn_windows8](../../includes/pn-windows8.md)], and [!INCLUDE[pn_Windows_7](../../includes/pn-windows-7.md)].</span></span>  <span data-ttu-id="f36ae-132">If you’re using the high contrast setting in  Windows, high contrast in the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client also becomes enabled.</span><span class="sxs-lookup"><span data-stu-id="f36ae-132">If you’re using the high contrast setting in  Windows, high contrast in the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client also becomes enabled.</span></span> <span data-ttu-id="f36ae-133">Và nếu bạn thay đổi chế độ tương phản cao trong Windows trong khi máy khách [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] đang chạy, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] cũng sẽ chuyển sang chế độ tương phản cao.</span><span class="sxs-lookup"><span data-stu-id="f36ae-133">And if you change the Windows high contrast mode while the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client is running, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] will  also switch to high contrast mode.</span></span>  
  
 <span data-ttu-id="f36ae-134">Note that there are two  themes available in earlier versions of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], Blue and Style, are no longer available because they  do not support high contrast mode.</span><span class="sxs-lookup"><span data-stu-id="f36ae-134">Note that there are two  themes available in earlier versions of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], Blue and Style, are no longer available because they  do not support high contrast mode.</span></span>  
  
<a name="ScreenReader"></a>   
## <a name="screen--reader-support"></a><span data-ttu-id="f36ae-135">Screen  reader support</span><span class="sxs-lookup"><span data-stu-id="f36ae-135">Screen  reader support</span></span>  
 <span data-ttu-id="f36ae-136">All out-of-box [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] hosted controls and custom controls that are included in the Dynamics 365 for Customer Engagement apps Web Client sample application package work with JAWS version 18 to provide speech output.</span><span class="sxs-lookup"><span data-stu-id="f36ae-136">All out-of-box [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] hosted controls and custom controls that are included in the Dynamics 365 for Customer Engagement apps Web Client sample application package work with JAWS version 18 to provide speech output.</span></span>  
  
 <span data-ttu-id="f36ae-137">For information about how developers can extend custom hosted controls or hosted controls in the other [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] sample application packages to support the JAWS screen reader, see [Configure JAWS Screen Reader in Unified Service Desk](../configure-jaws-screen-reader-support.md).</span><span class="sxs-lookup"><span data-stu-id="f36ae-137">For information about how developers can extend custom hosted controls or hosted controls in the other [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] sample application packages to support the JAWS screen reader, see [Configure JAWS Screen Reader in Unified Service Desk](../configure-jaws-screen-reader-support.md).</span></span>  
