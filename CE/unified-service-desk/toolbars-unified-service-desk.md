---
title: Toolbars in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn about configuring toolbars in Unified Service Desk.
ms.custom:
- dyn365-USD
ms.date: 04/24/2018
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
ms.assetid: f3738bca-89b7-48e6-bc97-2fb477d727b3
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: ff2d1f70e68e8134b12f293ac4e1ad3f4a5c4c96
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388171"
---
# <a name="toolbars-in-unified-service-desk"></a>Toolbars in Unified Service Desk
Thanh công cụ trong [!INCLUDE[pn_unified_service_desk_for_crm](../includes/pn-unified-service-desk-for-crm.md)] giữ và hiển thị danh sách các nút có hình ảnh và văn bản. Nhấp chuột hoặc chạm vào các nút có thể thực hiện một hoặc nhiều hành động.  
  
 Dưới đây là thanh công cụ **Chính** của ứng dụng mẫu [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].  
  
  ![Main toolbar in Unified Service Desk](../unified-service-desk/media/usd-toolbar-example.png "Main toolbar in Unified Service Desk")  
  
 You configure toolbars in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps in the **Settings** > **Unified Service Desk** > **Toolbars** area. Hơn nữa, mỗi thanh công cụ được gắn vào một loại kiểm soát tổ chức **Bộ chứa thanh công cụ** gắn liền với một khu vực Hiển thị (bảng điều khiển) trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. Điều này được thực hiện để xác định bảng điều khiển nơi thanh công cụ sẽ hiển thị trong ứng dụng khách.  
  
 Hình ảnh sau đây minh hoạ thanh công cụ sẵn có trong một [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] ứng dụng mẫu.  
  
  ![Toolbars in Unified Service Desk](../unified-service-desk/media/usd-toolbars.png "Toolbars in Unified Service Desk")  
  
## <a name="understanding-components-in-a-toolbar"></a>Biết các thành phần trong thanh công cụ  
 Nhấp vào bất kỳ tên thanh công cụ nào dưới cột **tên** để xem các nút bên trong thanh công cụ, cuộc gọi hành động cho mỗi nút và bộ chứa thanh công cụ trên thanh công cụ được gắn vào.  
  
 Để có ví dụ về cách thực hiện việc này, bấm vào **chính** trên trang thanh công cụ.  
  
- **Nút thanh công cụ**: trang thanh công cụ sẽ hiển thị các nút trong thanh công cụ **Chính**. Thứ tự của các nút sẽ xác định vị trí của nút từ trái sang phải theo một thứ tự tăng dần. Bạn có thể thêm, xóa hoặc chỉnh sửa một nút hiện có. 
  
  ![Buttons in the main toolbar](../unified-service-desk/media/usd-main-toolbar-buttons.png "Buttons in the main toolbar")  
  
- **Properties of a toolbar button**: To view the properties of a button, such as name, image, button label, tooltip, shortcut key, and action calls associated with a button, click any of the button names. For example, clicking **Dashboard** displays the following information for the button.  
  
  ![Toolbar button properties](../unified-service-desk/media/usd-toolbar-button-properties.png "Toolbar button properties")  
  
- **Bộ chứa thanh công cụ**: để xem kiểm soát tổ chức bộ chứa thanh công cụ được liên kết với thanh công cụ **Chính**, nhấp vào mũi tên xuống bên cạnh thanh công cụ **chính** trên thanh điều hướng và chọn **Kiểm soát tổ chức**.  
  
  ![View the toolbar container](../unified-service-desk/media/usd-main-toolbar.png "View the toolbar container")  
  
     Tên của bộ chứa thanh công cụ gắn liền với thanh công cụ **chính** sẽ được hiển thị.  
  
   ![Toolbar Container for the Main toolbar](../unified-service-desk/media/usd-main-toolbar-hosted-control.png "Toolbar Container for the Main toolbar")

- **Custom styles in toolbar**: You can now customize the toolbar in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] using the custom styles field in the Toolbar configuration window.  The Custom Styles field supports Extensible Application Markup Language (XAML) that defines <xref:System.Windows.ResourceDictionary> of <xref:System.Windows.Style> and <xref:System.Windows.Media.Brush> resources.<br><br>The resources in the dictionary refers to other resources that are available on [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application. Loading and parsing the XAML string is performed at runtime to create <xref:System.Windows.ResourceDictionary> and merge the resources of the toolbar control with the <xref:System.Windows.ResourceDictionary>. In addition, the <xref:System.Windows.ResourceDictionary> can have styles for button types inside a toolbar. Using the styles, you can customize the toolbars and buttons. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Styles in toolbar](configure-toolbars-application.md#styles-in-toolbar)


  ![Custom styles in toolbar](media/custom-styles-toolbar.PNG "Custom styles in toolbar")


### <a name="see-also"></a>Xem thêm  
 [Configure toolbars in your application](../unified-service-desk/configure-toolbars-application.md)

 [Walkthrough 2: Display an external webpage in your agent application](../unified-service-desk/walkthrough-2-display-an-external-webpage-in-your-agent-application.md)   

 [Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md)
