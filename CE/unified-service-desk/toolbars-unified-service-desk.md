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
# <a name="toolbars-in-unified-service-desk"></a><span data-ttu-id="a2b27-103">Toolbars in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="a2b27-103">Toolbars in Unified Service Desk</span></span>
<span data-ttu-id="a2b27-104">Thanh công cụ trong [!INCLUDE[pn_unified_service_desk_for_crm](../includes/pn-unified-service-desk-for-crm.md)] giữ và hiển thị danh sách các nút có hình ảnh và văn bản.</span><span class="sxs-lookup"><span data-stu-id="a2b27-104">Toolbars in [!INCLUDE[pn_unified_service_desk_for_crm](../includes/pn-unified-service-desk-for-crm.md)] hold and display a list of buttons with images and text.</span></span> <span data-ttu-id="a2b27-105">Nhấp chuột hoặc chạm vào các nút có thể thực hiện một hoặc nhiều hành động.</span><span class="sxs-lookup"><span data-stu-id="a2b27-105">Clicking or tapping the buttons can execute one or more actions.</span></span>  
  
 <span data-ttu-id="a2b27-106">Dưới đây là thanh công cụ **Chính** của ứng dụng mẫu [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="a2b27-106">Here is the **Main** toolbar in one of the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] sample applications.</span></span>  
  
  <span data-ttu-id="a2b27-107">![Main toolbar in Unified Service Desk](../unified-service-desk/media/usd-toolbar-example.png "Main toolbar in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="a2b27-107">![Main toolbar in Unified Service Desk](../unified-service-desk/media/usd-toolbar-example.png "Main toolbar in Unified Service Desk")</span></span>  
  
 <span data-ttu-id="a2b27-108">You configure toolbars in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps in the **Settings** > **Unified Service Desk** > **Toolbars** area.</span><span class="sxs-lookup"><span data-stu-id="a2b27-108">You configure toolbars in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps in the **Settings** > **Unified Service Desk** > **Toolbars** area.</span></span> <span data-ttu-id="a2b27-109">Hơn nữa, mỗi thanh công cụ được gắn vào một loại kiểm soát tổ chức **Bộ chứa thanh công cụ** gắn liền với một khu vực Hiển thị (bảng điều khiển) trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="a2b27-109">Furthermore, each toolbar is attached to a **Toolbar Container** type of hosted control, which in turn is attached to a display area (panel) in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> <span data-ttu-id="a2b27-110">Điều này được thực hiện để xác định bảng điều khiển nơi thanh công cụ sẽ hiển thị trong ứng dụng khách.</span><span class="sxs-lookup"><span data-stu-id="a2b27-110">This is done to specify the panel where the toolbar will display in the client application.</span></span>  
  
 <span data-ttu-id="a2b27-111">Hình ảnh sau đây minh hoạ thanh công cụ sẵn có trong một [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] ứng dụng mẫu.</span><span class="sxs-lookup"><span data-stu-id="a2b27-111">The following image shows the existing toolbars in a [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] sample application.</span></span>  
  
  <span data-ttu-id="a2b27-112">![Toolbars in Unified Service Desk](../unified-service-desk/media/usd-toolbars.png "Toolbars in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="a2b27-112">![Toolbars in Unified Service Desk](../unified-service-desk/media/usd-toolbars.png "Toolbars in Unified Service Desk")</span></span>  
  
## <a name="understanding-components-in-a-toolbar"></a><span data-ttu-id="a2b27-113">Biết các thành phần trong thanh công cụ</span><span class="sxs-lookup"><span data-stu-id="a2b27-113">Understanding components in a toolbar</span></span>  
 <span data-ttu-id="a2b27-114">Nhấp vào bất kỳ tên thanh công cụ nào dưới cột **tên** để xem các nút bên trong thanh công cụ, cuộc gọi hành động cho mỗi nút và bộ chứa thanh công cụ trên thanh công cụ được gắn vào.</span><span class="sxs-lookup"><span data-stu-id="a2b27-114">Click any toolbar name under the **Name** column to view the buttons inside the toolbar, action calls for each button, and the toolbar container that the toolbar is attached to.</span></span>  
  
 <span data-ttu-id="a2b27-115">Để có ví dụ về cách thực hiện việc này, bấm vào **chính** trên trang thanh công cụ.</span><span class="sxs-lookup"><span data-stu-id="a2b27-115">For an example of how to do this, click **Main** on the toolbars page.</span></span>  
  
- <span data-ttu-id="a2b27-116">**Nút thanh công cụ**: trang thanh công cụ sẽ hiển thị các nút trong thanh công cụ **Chính**.</span><span class="sxs-lookup"><span data-stu-id="a2b27-116">**Toolbar buttons**: The toolbar page displays the buttons in the **Main** toolbar.</span></span> <span data-ttu-id="a2b27-117">Thứ tự của các nút sẽ xác định vị trí của nút từ trái sang phải theo một thứ tự tăng dần.</span><span class="sxs-lookup"><span data-stu-id="a2b27-117">The order of the buttons determines the placement of buttons from left to right in an ascending order.</span></span> <span data-ttu-id="a2b27-118">Bạn có thể thêm, xóa hoặc chỉnh sửa một nút hiện có.</span><span class="sxs-lookup"><span data-stu-id="a2b27-118">You can add, remove, or edit an existing button.</span></span> 
  
  <span data-ttu-id="a2b27-119">![Buttons in the main toolbar](../unified-service-desk/media/usd-main-toolbar-buttons.png "Buttons in the main toolbar")</span><span class="sxs-lookup"><span data-stu-id="a2b27-119">![Buttons in the main toolbar](../unified-service-desk/media/usd-main-toolbar-buttons.png "Buttons in the main toolbar")</span></span>  
  
- <span data-ttu-id="a2b27-120">**Properties of a toolbar button**: To view the properties of a button, such as name, image, button label, tooltip, shortcut key, and action calls associated with a button, click any of the button names.</span><span class="sxs-lookup"><span data-stu-id="a2b27-120">**Properties of a toolbar button**: To view the properties of a button, such as name, image, button label, tooltip, shortcut key, and action calls associated with a button, click any of the button names.</span></span> <span data-ttu-id="a2b27-121">For example, clicking **Dashboard** displays the following information for the button.</span><span class="sxs-lookup"><span data-stu-id="a2b27-121">For example, clicking **Dashboard** displays the following information for the button.</span></span>  
  
  <span data-ttu-id="a2b27-122">![Toolbar button properties](../unified-service-desk/media/usd-toolbar-button-properties.png "Toolbar button properties")</span><span class="sxs-lookup"><span data-stu-id="a2b27-122">![Toolbar button properties](../unified-service-desk/media/usd-toolbar-button-properties.png "Toolbar button properties")</span></span>  
  
- <span data-ttu-id="a2b27-123">**Bộ chứa thanh công cụ**: để xem kiểm soát tổ chức bộ chứa thanh công cụ được liên kết với thanh công cụ **Chính**, nhấp vào mũi tên xuống bên cạnh thanh công cụ **chính** trên thanh điều hướng và chọn **Kiểm soát tổ chức**.</span><span class="sxs-lookup"><span data-stu-id="a2b27-123">**Toolbar Container**: To view the toolbar container hosted control associated with the **Main** toolbar, click the down arrow next to the **Main** toolbar on the nav bar, and select **Hosted Controls**.</span></span>  
  
  <span data-ttu-id="a2b27-124">![View the toolbar container](../unified-service-desk/media/usd-main-toolbar.png "View the toolbar container")</span><span class="sxs-lookup"><span data-stu-id="a2b27-124">![View the toolbar container](../unified-service-desk/media/usd-main-toolbar.png "View the toolbar container")</span></span>  
  
     <span data-ttu-id="a2b27-125">Tên của bộ chứa thanh công cụ gắn liền với thanh công cụ **chính** sẽ được hiển thị.</span><span class="sxs-lookup"><span data-stu-id="a2b27-125">The name of the toolbar container attached to the **Main** toolbar is displayed.</span></span>  
  
   <span data-ttu-id="a2b27-126">![Toolbar Container for the Main toolbar](../unified-service-desk/media/usd-main-toolbar-hosted-control.png "Toolbar Container for the Main toolbar")</span><span class="sxs-lookup"><span data-stu-id="a2b27-126">![Toolbar Container for the Main toolbar](../unified-service-desk/media/usd-main-toolbar-hosted-control.png "Toolbar Container for the Main toolbar")</span></span>

- <span data-ttu-id="a2b27-127">**Custom styles in toolbar**: You can now customize the toolbar in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] using the custom styles field in the Toolbar configuration window.</span><span class="sxs-lookup"><span data-stu-id="a2b27-127">**Custom styles in toolbar**: You can now customize the toolbar in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] using the custom styles field in the Toolbar configuration window.</span></span>  <span data-ttu-id="a2b27-128">The Custom Styles field supports Extensible Application Markup Language (XAML) that defines <xref:System.Windows.ResourceDictionary> of <xref:System.Windows.Style> and <xref:System.Windows.Media.Brush> resources.</span><span class="sxs-lookup"><span data-stu-id="a2b27-128">The Custom Styles field supports Extensible Application Markup Language (XAML) that defines <xref:System.Windows.ResourceDictionary> of <xref:System.Windows.Style> and <xref:System.Windows.Media.Brush> resources.</span></span><br><br><span data-ttu-id="a2b27-129">The resources in the dictionary refers to other resources that are available on [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application.</span><span class="sxs-lookup"><span data-stu-id="a2b27-129">The resources in the dictionary refers to other resources that are available on [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application.</span></span> <span data-ttu-id="a2b27-130">Loading and parsing the XAML string is performed at runtime to create <xref:System.Windows.ResourceDictionary> and merge the resources of the toolbar control with the <xref:System.Windows.ResourceDictionary>.</span><span class="sxs-lookup"><span data-stu-id="a2b27-130">Loading and parsing the XAML string is performed at runtime to create <xref:System.Windows.ResourceDictionary> and merge the resources of the toolbar control with the <xref:System.Windows.ResourceDictionary>.</span></span> <span data-ttu-id="a2b27-131">In addition, the <xref:System.Windows.ResourceDictionary> can have styles for button types inside a toolbar.</span><span class="sxs-lookup"><span data-stu-id="a2b27-131">In addition, the <xref:System.Windows.ResourceDictionary> can have styles for button types inside a toolbar.</span></span> <span data-ttu-id="a2b27-132">Using the styles, you can customize the toolbars and buttons.</span><span class="sxs-lookup"><span data-stu-id="a2b27-132">Using the styles, you can customize the toolbars and buttons.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="a2b27-133">[Styles in toolbar](configure-toolbars-application.md#styles-in-toolbar)</span><span class="sxs-lookup"><span data-stu-id="a2b27-133">[Styles in toolbar](configure-toolbars-application.md#styles-in-toolbar)</span></span>


  <span data-ttu-id="a2b27-134">![Custom styles in toolbar](media/custom-styles-toolbar.PNG "Custom styles in toolbar")</span><span class="sxs-lookup"><span data-stu-id="a2b27-134">![Custom styles in toolbar](media/custom-styles-toolbar.PNG "Custom styles in toolbar")</span></span>


### <a name="see-also"></a><span data-ttu-id="a2b27-135">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="a2b27-135">See also</span></span>  
 [<span data-ttu-id="a2b27-136">Configure toolbars in your application</span><span class="sxs-lookup"><span data-stu-id="a2b27-136">Configure toolbars in your application</span></span>](../unified-service-desk/configure-toolbars-application.md)

 [<span data-ttu-id="a2b27-137">Walkthrough 2: Display an external webpage in your agent application</span><span class="sxs-lookup"><span data-stu-id="a2b27-137">Walkthrough 2: Display an external webpage in your agent application</span></span>](../unified-service-desk/walkthrough-2-display-an-external-webpage-in-your-agent-application.md)   

 [<span data-ttu-id="a2b27-138">Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application</span><span class="sxs-lookup"><span data-stu-id="a2b27-138">Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application</span></span>](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md)
