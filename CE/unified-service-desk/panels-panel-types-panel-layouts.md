---
title: Panels, panel types, and panel layouts in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn about using panels to display hosted controls of various types. Various predefined panel types are available in Unified Service Desk to support a variety of layout options such as tabbed layout, deck layout, and stacked layout.
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
ms.assetid: cc93dff6-3d0e-4a73-918d-16dd883d7fec
caps.latest.revision: 9
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: d462f16ec419b98d337623ed65099eb483017ed3
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386080"
---
# <a name="panels-panel-types-and-panel-layouts-in-unified-service-desk"></a><span data-ttu-id="060fa-104">Panels, panel types, and panel layouts in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="060fa-104">Panels, panel types, and panel layouts in Unified Service Desk</span></span>
[!INCLUDE[pn_unified_service_desk_for_crm](../includes/pn-unified-service-desk-for-crm.md)]<span data-ttu-id="060fa-105">sử dụng bảng điều khiển để hiển thị nhiều loại kiểm soát tổ chức.</span><span class="sxs-lookup"><span data-stu-id="060fa-105">uses panels to display hosted controls of various types.</span></span> <span data-ttu-id="060fa-106">Có sẵn nhiều loại bảng điều khiển được xác định trước trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] để hỗ trợ nhiều tùy chọn bố cục như bố cục theo tab, bố cục sàn và bố cục xếp chồng.</span><span class="sxs-lookup"><span data-stu-id="060fa-106">Various predefined panel types are available in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] to support a variety of layout options such as tabbed layout, deck layout, and stacked layout.</span></span> <span data-ttu-id="060fa-107">Bạn xác định cách sắp xếp các bảng điều khiển này trên màn hình chính của [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] bằng cách sử dụng kiểm soát tổ chức **Bố cục bảng điều khiển**.</span><span class="sxs-lookup"><span data-stu-id="060fa-107">You define the arrangement of these panels on the main screen of [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] using a **Panel Layout** hosted control.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="060fa-108">[Panel Layout (Hosted Control)](../unified-service-desk/panel-layout-hosted-control.md)</span><span class="sxs-lookup"><span data-stu-id="060fa-108">[Panel Layout (Hosted Control)](../unified-service-desk/panel-layout-hosted-control.md)</span></span>  

<a name="Panels"></a>   
## <a name="panels-in-unified-service-desk"></a><span data-ttu-id="060fa-109">Bảng điều khiển trong Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="060fa-109">Panels in Unified Service Desk</span></span>  
 <span data-ttu-id="060fa-110">Bất cứ khi nào bạn tạo kiểm soát tổ chức, bạn cần phải chỉ định bảng điều khiển sẽ giữ nó trong trường **Hiển thị nhóm** của trang **Kiểm soát tổ chức mới**.</span><span class="sxs-lookup"><span data-stu-id="060fa-110">Whenever you create a hosted control, you have to specify the panel that will hold it in the **Display Group** field of the **New Hosted Control** page.</span></span> <span data-ttu-id="060fa-111">Đối với hầu hết các loại kiểm soát tổ chức, [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] tự động xác định giá trị bảng điều khiển trong trường **Hiển thị nhóm**.</span><span class="sxs-lookup"><span data-stu-id="060fa-111">For most of the hosted control types, [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] automatically populates a panel value in the **Display Group** field.</span></span> <span data-ttu-id="060fa-112">For example, **MainPanel** is used for a **CRM Page** type of hosted control and **ToolbarPanel** is used for the **Toolbar Container** type of hosted control.</span><span class="sxs-lookup"><span data-stu-id="060fa-112">For example, **MainPanel** is used for a **CRM Page** type of hosted control and **ToolbarPanel** is used for the **Toolbar Container** type of hosted control.</span></span>  

 <span data-ttu-id="060fa-113">Bảng điều khiển được xác định trước sau đây có sẵn trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="060fa-113">The following predefined panels are available in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span>  


|          <span data-ttu-id="060fa-114">Bảng điều khiển</span><span class="sxs-lookup"><span data-stu-id="060fa-114">Panel</span></span>          |                                                                                      <span data-ttu-id="060fa-115">Mô tả</span><span class="sxs-lookup"><span data-stu-id="060fa-115">Description</span></span>                                                                                      |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        <span data-ttu-id="060fa-116">Bảng điều khiển chính</span><span class="sxs-lookup"><span data-stu-id="060fa-116">MainPanel</span></span>        |                                                                        <span data-ttu-id="060fa-117">Vùng làm việc chính ở dưới cùng bên phải.</span><span class="sxs-lookup"><span data-stu-id="060fa-117">The main work area in the bottom right.</span></span>                                                                        |
|        <span data-ttu-id="060fa-118">Bảng điều khiển trò chuyện</span><span class="sxs-lookup"><span data-stu-id="060fa-118">ChatPanel</span></span>        |                                                   <span data-ttu-id="060fa-119">Vị trí thông thường của cửa sổ trò chuyện.</span><span class="sxs-lookup"><span data-stu-id="060fa-119">The typical location of the chat window.</span></span> <span data-ttu-id="060fa-120">Cửa sổ ở dưới kiểm soát ghi mã lệnh tổng đài viên.</span><span class="sxs-lookup"><span data-stu-id="060fa-120">It is under the agent scripting control.</span></span>                                                   |
|       <span data-ttu-id="060fa-121">Bảng điều khiển bị ẩn</span><span class="sxs-lookup"><span data-stu-id="060fa-121">HiddenPanel</span></span>       |                                                    <span data-ttu-id="060fa-122">Bảng điều khiển bị ẩn sẽ được sử dụng cho các thành phần không có giao diện người dùng (UI).</span><span class="sxs-lookup"><span data-stu-id="060fa-122">A nonvisible panel generally used for component without a user interface (UI).</span></span>                                                     |
|       <span data-ttu-id="060fa-123">Bảng điều khiển bên trái 1</span><span class="sxs-lookup"><span data-stu-id="060fa-123">LeftPanel1</span></span>        |                                                                 <span data-ttu-id="060fa-124">Bảng điều khiển chỉ dưới **Bảng điều khiển quy trình làm việc** ở bên trái.</span><span class="sxs-lookup"><span data-stu-id="060fa-124">A panel just under the **WorkflowPanel** on the left.</span></span>                                                                 |
|       <span data-ttu-id="060fa-125">Bảng điều khiển bên trái 2</span><span class="sxs-lookup"><span data-stu-id="060fa-125">LeftPanel2</span></span>        |                                                                  <span data-ttu-id="060fa-126">Bảng điều khiển chỉ ở dưới **Bảng điều khiển bên trái 1** ở bên trái.</span><span class="sxs-lookup"><span data-stu-id="060fa-126">A panel just under the **LeftPanel1** on the left.</span></span>                                                                   |
|      <span data-ttu-id="060fa-127">Điền đầy bảng điều khiển bên trái</span><span class="sxs-lookup"><span data-stu-id="060fa-127">LeftPanelFill</span></span>      |                        <span data-ttu-id="060fa-128">Bảng điều khiển chỉ ở dưới **Bảng điều khiển bên trái 2**.</span><span class="sxs-lookup"><span data-stu-id="060fa-128">A panel just under the **LeftPanel2**.</span></span> <span data-ttu-id="060fa-129">Bảng điều khiển này mở rộng để điền vào phần còn lại của vùng sẵn có ở cạnh dưới cùng của bảng điều khiển bên trái.</span><span class="sxs-lookup"><span data-stu-id="060fa-129">This panel expands to fill the rest of the area available to the bottom edge of the left panel.</span></span>                         |
|       <span data-ttu-id="060fa-130">RightPanel</span><span class="sxs-lookup"><span data-stu-id="060fa-130">RightPanel</span></span>        |                                                                          <span data-ttu-id="060fa-131">Một bảng điều khiển nằm ở phía bên phải.</span><span class="sxs-lookup"><span data-stu-id="060fa-131">A panel located on the right side.</span></span>                                                                           |
|       <span data-ttu-id="060fa-132">CtiPanel \*</span><span class="sxs-lookup"><span data-stu-id="060fa-132">CtiPanel \*</span></span>       | <span data-ttu-id="060fa-133">Bảng điều khiển nằm ở phía trên cùng bên phải, đó là vị trí mặc định cho kiểm soát điện thoại mềm.</span><span class="sxs-lookup"><span data-stu-id="060fa-133">A panel located in the top right, it is the default location for softphone controls.</span></span> <span data-ttu-id="060fa-134">Đây là bảng điều khiển kiểu xếp chồng vì vậy có thể thêm nhiều kiểm soát và hiển thị bên cạnh các kiểm soát khác.</span><span class="sxs-lookup"><span data-stu-id="060fa-134">This is a stack panel so more than one control can be added and will show up next to each other.</span></span> |
| <span data-ttu-id="060fa-135">SessionExplorerPanel \*</span><span class="sxs-lookup"><span data-stu-id="060fa-135">SessionExplorerPanel \*</span></span> |                                              <span data-ttu-id="060fa-136">Bảng điều khiển nằm ngay dưới các tab phiên nơi bạn thường hiển thị dòng phiên.</span><span class="sxs-lookup"><span data-stu-id="060fa-136">A panel located just under the session tabs where you typically display the session lines.</span></span>                                               |
|    <span data-ttu-id="060fa-137">WorkflowPanel \*</span><span class="sxs-lookup"><span data-stu-id="060fa-137">WorkflowPanel \*</span></span>     |                                       <span data-ttu-id="060fa-138">Bảng điều khiển nằm ngay dưới **Bảng điều khiển trình khám phá phiên** và thường chứa kiểm soát lập mã lệnh tổng đài viên.</span><span class="sxs-lookup"><span data-stu-id="060fa-138">A panel located just under the **SessionExplorerPanel** and usually contains the agent scripting control.</span></span>                                       |
|     <span data-ttu-id="060fa-139">ToolbarPanel \*</span><span class="sxs-lookup"><span data-stu-id="060fa-139">ToolbarPanel \*</span></span>     |          <span data-ttu-id="060fa-140">Bảng điều khiển ở trên đầu về bên phải của biểu trưng [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] và thường có thanh công cụ.</span><span class="sxs-lookup"><span data-stu-id="060fa-140">A panel at the very top just to the right of the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] logo, and typically holds the Toolbar.</span></span>          |
|       <span data-ttu-id="060fa-141">Bảng điều khiển ruy băng</span><span class="sxs-lookup"><span data-stu-id="060fa-141">RibbonPanel</span></span>       |                                                                                <span data-ttu-id="060fa-142">For internal use only.</span><span class="sxs-lookup"><span data-stu-id="060fa-142">For internal use only.</span></span>                                                                                 |
|     <span data-ttu-id="060fa-143">StatusPanel \*</span><span class="sxs-lookup"><span data-stu-id="060fa-143">StatusPanel \*</span></span>      |                                                      <span data-ttu-id="060fa-144">Bảng điều khiển đặc biệt nằm trên thanh trạng thái ở dưới cùng của ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="060fa-144">A special panel located on the status bar at the bottom of the application.</span></span>                                                      |

 <span data-ttu-id="060fa-145">\* These panels are generally reserved for special purposes so use of these should be avoided unless required.</span><span class="sxs-lookup"><span data-stu-id="060fa-145">\* These panels are generally reserved for special purposes so use of these should be avoided unless required.</span></span>  

 <span data-ttu-id="060fa-146">You can also assign keyboard shortcuts to panels so that customer service agents can directly access the panel in the client application by just using the keyboard.</span><span class="sxs-lookup"><span data-stu-id="060fa-146">You can also assign keyboard shortcuts to panels so that customer service agents can directly access the panel in the client application by just using the keyboard.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="060fa-147">[Keyboard shortcuts for panels](../unified-service-desk/keyboard-shortcuts-panels.md)</span><span class="sxs-lookup"><span data-stu-id="060fa-147">[Keyboard shortcuts for panels](../unified-service-desk/keyboard-shortcuts-panels.md)</span></span>  

<a name="PanelTypes"></a>   
## <a name="panel-types-in-unified-service-desk"></a><span data-ttu-id="060fa-148">Loại bảng điều khiển trong Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="060fa-148">Panel types in Unified Service Desk</span></span>  
 [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]<span data-ttu-id="060fa-149">cung cấp các loại bảng điều khiển được xác định trước để hỗ trợ một loạt các tùy chọn bố cục:</span><span class="sxs-lookup"><span data-stu-id="060fa-149">provides the following predefined panel types to support a variety of layout options:</span></span>  


|      <span data-ttu-id="060fa-150">Loại bảng điều khiển</span><span class="sxs-lookup"><span data-stu-id="060fa-150">Panel Type</span></span>      |                                                                                                                                                                                                                                                                               <span data-ttu-id="060fa-151">Mô tả</span><span class="sxs-lookup"><span data-stu-id="060fa-151">Description</span></span>                                                                                                                                                                                                                                                                                |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     <span data-ttu-id="060fa-152">Bảng điều khiển Tab USD</span><span class="sxs-lookup"><span data-stu-id="060fa-152">USDTabPanel</span></span>      |                                                                                   <span data-ttu-id="060fa-153">Loại bảng điều khiển chứa kiểm soát tab.</span><span class="sxs-lookup"><span data-stu-id="060fa-153">This panel type contains a tab control.</span></span> <span data-ttu-id="060fa-154">Mỗi kiểm soát tổ chức được tải trên một trong số các tab.</span><span class="sxs-lookup"><span data-stu-id="060fa-154">Each hosted control is loaded on one of the tabs.</span></span> <span data-ttu-id="060fa-155">Tên tab sẽ hiển thị giá trị được chỉ định trong trường **Hiển thị tên** của kiểm soát tổ chức.</span><span class="sxs-lookup"><span data-stu-id="060fa-155">The tab name displays the value specified in the **Display Name** filed of a hosted control.</span></span> <span data-ttu-id="060fa-156">Nếu không có tên hiển thị được chỉ định cho kiểm soát tổ chức, tên kiểm soát tổ chức được hiển thị làm tên tab.</span><span class="sxs-lookup"><span data-stu-id="060fa-156">If no display name is specified for a hosted control, the hosted control name is displayed as the tab name.</span></span> <span data-ttu-id="060fa-157">Tab điều khiển/tiêu đề được hiển thị cho các loại bảng điều khiển nếu một hoặc nhiều kiểm soát tổ chức có trên đó.</span><span class="sxs-lookup"><span data-stu-id="060fa-157">The tab control/header is displayed for this panel type if one or more hosted controls are on it.</span></span>                                                                                   |
|    <span data-ttu-id="060fa-158">Bảng điều khiển xếp chồng USD</span><span class="sxs-lookup"><span data-stu-id="060fa-158">USDStackPanel</span></span>     | <span data-ttu-id="060fa-159">This panel type stacks hosted controls in a horizontal or vertical fashion similar to a stack panel in [!INCLUDE[pn_ms_Windows_Presentation_Foundation](../includes/pn-ms-windows-presentation-foundation.md)].</span><span class="sxs-lookup"><span data-stu-id="060fa-159">This panel type stacks hosted controls in a horizontal or vertical fashion similar to a stack panel in [!INCLUDE[pn_ms_Windows_Presentation_Foundation](../includes/pn-ms-windows-presentation-foundation.md)].</span></span> <span data-ttu-id="060fa-160">These can be useful for toolbars or status bars, etc. This panel type is derived from StackPanel, which supports an [Orientation](http://msdn.microsoft.com/library/system.windows.controls.stackpanel.orientation\(v=vs.100\).aspx) property.</span><span class="sxs-lookup"><span data-stu-id="060fa-160">These can be useful for toolbars or status bars, etc. This panel type is derived from StackPanel, which supports an [Orientation](http://msdn.microsoft.com/library/system.windows.controls.stackpanel.orientation\(v=vs.100\).aspx) property.</span></span> <span data-ttu-id="060fa-161">Định hướng này nên được xác định trong XAML để xác định cách xếp chồng các kiểm soát tổ chức.</span><span class="sxs-lookup"><span data-stu-id="060fa-161">This orientation should be defined in the XAML to define which way the hosted controls should be stacked.</span></span> |
|   <span data-ttu-id="060fa-162">Bảng điều khiển tab sàn USD</span><span class="sxs-lookup"><span data-stu-id="060fa-162">USDDeckTabPanel</span></span>    |                                                                                                                    <span data-ttu-id="060fa-163">Nếu có một kiểm soát tổ chức trên bảng điều khiển này, các tab sẽ không được hiển thị.</span><span class="sxs-lookup"><span data-stu-id="060fa-163">If a single hosted control is on this panel, the tabs are not shown.</span></span> <span data-ttu-id="060fa-164">Các tab cho kiểm soát tab được hiển thị nếu hai hoặc nhiều kiểm soát nằm trên bảng này.</span><span class="sxs-lookup"><span data-stu-id="060fa-164">The tabs for a tab control are shown if two or more controls reside on this panel.</span></span><br /><br /> <span data-ttu-id="060fa-165">Kiểm soát này là giống như **Bảng điều khiển Tab USD** nhưng kiểu tồn tại trong các chủ đề mặc định sẽ ẩn các tab ở phía trên, khi chỉ có kiểm soát được tải.</span><span class="sxs-lookup"><span data-stu-id="060fa-165">This control is the same as the **USDTabPanel** but a style exists in the default themes that will hide the tabs at the top, when only one control is loaded.</span></span>                                                                                                                     |
|   <span data-ttu-id="060fa-166">Bảng điều khiển thu nhỏ USD</span><span class="sxs-lookup"><span data-stu-id="060fa-166">USDCollapsePanel</span></span>   |                                                                                                                                                                       <span data-ttu-id="060fa-167">Bảng điều khiển này giống như **Bảng điều khiển Tab USD** nhưng kiểu trong chủ đề mặc định được xác định sẽ tự động thu nhỏ loại bảng điều khiển này để nó không còn chiếm diện tích trong giao diện người dùng, nếu không có kiểm soát tổ chức nào được tải trong bảng điều khiển.</span><span class="sxs-lookup"><span data-stu-id="060fa-167">This is the same as the **USDTabPanel** but a style in the default themes is defined that will automatically collapse this panel type so it no longer takes up space in the UI, if no hosted controls are loaded within it.</span></span>                                                                                                                                                                        |
|   <span data-ttu-id="060fa-168">Bảng điều khiển Nổi USD</span><span class="sxs-lookup"><span data-stu-id="060fa-168">USDFloatingPanel</span></span>   |                                                                                                                                          <span data-ttu-id="060fa-169">Máy tính để bàn mặc định cung cấp phiên bản của loại bảng điều khiển này.</span><span class="sxs-lookup"><span data-stu-id="060fa-169">The default desktop provides an instance of this panel type.</span></span> <span data-ttu-id="060fa-170">When “FloatingPanel” is specified for a hosted control, this panel type is being used.</span><span class="sxs-lookup"><span data-stu-id="060fa-170">When “FloatingPanel” is specified for a hosted control, this panel type is being used.</span></span> <span data-ttu-id="060fa-171">Thông thường bạn sẽ không chỉ định loại bảng trong bố cục tùy chỉnh của mình, tuy nhiên trong trường hợp cần sử dụng loại bảng điều khiển này thì nó sẽ được sử dụng.</span><span class="sxs-lookup"><span data-stu-id="060fa-171">Typically you would not specify this panel type in your custom layout, however, it is exposed in case there is a reason to use it.</span></span>                                                                                                                                          |
| <span data-ttu-id="060fa-172">Bảng điều khiển công cụ Nổi USD</span><span class="sxs-lookup"><span data-stu-id="060fa-172">USDFloatingToolPanel</span></span> |                                                                                                 <span data-ttu-id="060fa-173">Loại bảng điều khiển này tạo ra một cửa sổ công cụ cho mỗi kiểm soát tổ chức được tải vào bảng điều khiển đó.</span><span class="sxs-lookup"><span data-stu-id="060fa-173">This panel type creates a tool window for each hosted control loaded into it.</span></span> <span data-ttu-id="060fa-174">The default desktop provides an instance of this panel type.</span><span class="sxs-lookup"><span data-stu-id="060fa-174">The default desktop provides an instance of this panel type.</span></span> <span data-ttu-id="060fa-175">When “FloatingToolPanel” is specified for a hosted control, this panel type is being used.</span><span class="sxs-lookup"><span data-stu-id="060fa-175">When “FloatingToolPanel” is specified for a hosted control, this panel type is being used.</span></span> <span data-ttu-id="060fa-176">Thông thường bạn sẽ không chỉ định loại bảng trong bố cục tùy chỉnh của mình, tuy nhiên trong trường hợp cần sử dụng loại bảng điều khiển này thì nó sẽ được sử dụng.</span><span class="sxs-lookup"><span data-stu-id="060fa-176">Typically you would not specify this panel type in your custom layout, however, it is exposed in case there is a reason to use it.</span></span>                                                                                                 |
|    <span data-ttu-id="060fa-177">USDPopUpPanel</span><span class="sxs-lookup"><span data-stu-id="060fa-177">USDPopUpPanel</span></span>     |                                                                                                                                                                                                                                          <span data-ttu-id="060fa-178">Loại bảng điều khiển này cho phép nội dung trong bộ điều khiển lưu trữ di chuột qua giao diện chính.</span><span class="sxs-lookup"><span data-stu-id="060fa-178">This panel type enables the content in the hosted control to hover over the main view.</span></span>                                                                                                                                                                                                                                          |

 <span data-ttu-id="060fa-179">Bạn cũng có thể sử dụng các loại bảng điều khiển được xác định trước để tạo ra một loại bảng điều khiển tùy chỉnh trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="060fa-179">You can also use these predefined panel types to create a custom panel type in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="060fa-180">[Create a custom panel type](../unified-service-desk/create-custom-panel-type.md)</span><span class="sxs-lookup"><span data-stu-id="060fa-180">[Create a custom panel type](../unified-service-desk/create-custom-panel-type.md)</span></span>  

<a name="PanelLayouts"></a>   
## <a name="panel-layouts-in-unified-service-desk"></a><span data-ttu-id="060fa-181">Bố cục bảng điều khiển trong Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="060fa-181">Panel layouts in Unified Service Desk</span></span>  
 <span data-ttu-id="060fa-182">Use  a panel layout to define the arrangement of panels on the screen in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client.</span><span class="sxs-lookup"><span data-stu-id="060fa-182">Use  a panel layout to define the arrangement of panels on the screen in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client.</span></span> <span data-ttu-id="060fa-183">A panel layout is defined using a **Panel Layout** hosted control.</span><span class="sxs-lookup"><span data-stu-id="060fa-183">A panel layout is defined using a **Panel Layout** hosted control.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="060fa-184">[Panel Layout (Hosted Control)](../unified-service-desk/panel-layout-hosted-control.md)</span><span class="sxs-lookup"><span data-stu-id="060fa-184">[Panel Layout (Hosted Control)](../unified-service-desk/panel-layout-hosted-control.md)</span></span>  

 <span data-ttu-id="060fa-185">The following layout depicts the **Standard Main Panel** type of panel layout (also called standard panel layout) in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="060fa-185">The following layout depicts the **Standard Main Panel** type of panel layout (also called standard panel layout) in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span>  

 <span data-ttu-id="060fa-186">![Air theme in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-themeair.png "Air theme in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="060fa-186">![Air theme in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-themeair.png "Air theme in Unified Service Desk")</span></span>  

> [!NOTE]
>  <span data-ttu-id="060fa-187">If you do not create any panel layout in your [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration, the standard panel layout is used automatically to display panels and controls in the client application.</span><span class="sxs-lookup"><span data-stu-id="060fa-187">If you do not create any panel layout in your [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration, the standard panel layout is used automatically to display panels and controls in the client application.</span></span>  
> 
>  <span data-ttu-id="060fa-188">The full application area on the main window is defined as a panel itself, and is called `MainWorkArea`.While defining `XAML` or `User-Defined` type of panel layout, `MainWorkArea` is used as the panel value for the **Display Group** field.</span><span class="sxs-lookup"><span data-stu-id="060fa-188">The full application area on the main window is defined as a panel itself, and is called `MainWorkArea`.While defining `XAML` or `User-Defined` type of panel layout, `MainWorkArea` is used as the panel value for the **Display Group** field.</span></span>  

 <span data-ttu-id="060fa-189">Because  panel layouts are hosted controls, you may use a panel layout anywhere you would have configured a hosted control.</span><span class="sxs-lookup"><span data-stu-id="060fa-189">Because  panel layouts are hosted controls, you may use a panel layout anywhere you would have configured a hosted control.</span></span> <span data-ttu-id="060fa-190">Một cách sử dụng phổ biến cho loại này đó là xác định chế độ xem phân chia trong vùng bảng điều khiển chính.</span><span class="sxs-lookup"><span data-stu-id="060fa-190">One common use for this is to define a split view in the main panel area.</span></span> <span data-ttu-id="060fa-191">Bạn có thể hiển thị chế độ xem danh sách hiển thị danh sách các tài khoản ở đầu và chế độ xem chi tiết ở dưới cùng.</span><span class="sxs-lookup"><span data-stu-id="060fa-191">You might display a list view showing a list of accounts at the top and a detail view at the bottom.</span></span> <span data-ttu-id="060fa-192">Bạn có thể hiển thị toàn bộ bộ cục bảng điều khiển trong bảng điều khiển nổi và hiển thị nó trên một màn hình thứ hai.</span><span class="sxs-lookup"><span data-stu-id="060fa-192">You might display a whole panel layout in the floating panel and show it on a second monitor.</span></span> <span data-ttu-id="060fa-193">For more information about the usage of floating panes, see [Configure Pop In and Pop Out feature for knowledge base articles](../unified-service-desk/configure-unified-service-desk-use-dynamics-365-knowledge.md#PopInOut).</span><span class="sxs-lookup"><span data-stu-id="060fa-193">For more information about the usage of floating panes, see [Configure Pop In and Pop Out feature for knowledge base articles](../unified-service-desk/configure-unified-service-desk-use-dynamics-365-knowledge.md#PopInOut).</span></span>  

 [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] <span data-ttu-id="060fa-194">provides the following types of panel layouts:</span><span class="sxs-lookup"><span data-stu-id="060fa-194">provides the following types of panel layouts:</span></span>  

 <span data-ttu-id="060fa-195">**Bảng điều khiển chính tiêu chuẩn**</span><span class="sxs-lookup"><span data-stu-id="060fa-195">**Standard Main Panel**</span></span>  
 <span data-ttu-id="060fa-196">The standard panel layout provides the traditional layout including a series of panels on the left, collapsible area and a main work area on the right.</span><span class="sxs-lookup"><span data-stu-id="060fa-196">The standard panel layout provides the traditional layout including a series of panels on the left, collapsible area and a main work area on the right.</span></span> <span data-ttu-id="060fa-197">The following is the XAML used to define the panel layout.</span><span class="sxs-lookup"><span data-stu-id="060fa-197">The following is the XAML used to define the panel layout.</span></span> <span data-ttu-id="060fa-198">You can also find this XAML in the [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] SDK.</span><span class="sxs-lookup"><span data-stu-id="060fa-198">You can also find this XAML in the [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] SDK.</span></span> <span data-ttu-id="060fa-199">[Download](http://go.microsoft.com/fwlink/p/?LinkId=395257) the package, and extract it to view the `SamplePanelLayout.xaml`  file under the "UII\USD Developer Assets\USD Layout and Style Sheet" directory.</span><span class="sxs-lookup"><span data-stu-id="060fa-199">[Download](http://go.microsoft.com/fwlink/p/?LinkId=395257) the package, and extract it to view the `SamplePanelLayout.xaml`  file under the "UII\USD Developer Assets\USD Layout and Style Sheet" directory.</span></span>  

```xaml  
<USD:PanelLayoutBase xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"  
  xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"  
  xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"  
  xmlns:d="http://schemas.microsoft.com/expression/blend/2008"  
  mc:Ignorable="d"  
  xmlns:local="clr-namespace:Microsoft.Crm.UnifiedServiceDesk.Dynamics;assembly=Microsoft.Crm.UnifiedServiceDesk.Dynamics"  
  xmlns:USD="clr-namespace:Microsoft.Crm.UnifiedServiceDesk.Dynamics.PanelLayouts;assembly=Microsoft.Crm.UnifiedServiceDesk.Dynamics"  
  d:DesignHeight="300"  
  d:DesignWidth="300">  
  <Grid x:Name="LayoutRoot">  
    <Grid.Resources>  
      <local:CRMImageConverter x:Key="CRMImageLoader" />  
    </Grid.Resources>  
    <Grid.RowDefinitions>  
      <RowDefinition Height="40"/>  
      <RowDefinition Height="*"/>  
      <RowDefinition Height="30"/>  
    </Grid.RowDefinitions>  
    <Border Grid.Row="0"  
            BorderBrush="#d8d8d8"  
            BorderThickness="0,1,0,1">  
      <Grid Background="{DynamicResource WindowHeaderStyle}"  
            Grid.Row="0"  
            Margin="0">  
        <Grid.ColumnDefinitions>  
          <ColumnDefinition Width="auto" />  
          <ColumnDefinition Width="auto" />  
          <ColumnDefinition Width="*" />  
          <ColumnDefinition Width="Auto" />  
        </Grid.ColumnDefinitions>  
        <Image Style="{DynamicResource USDLogo}"  
               Grid.Column="0"  
               ToolTip="Unified Service Desk"  
               AutomationProperties.Name="Unified Service Desk" />  
        <Rectangle Width="10"  
                   Grid.Column="1" />  
        <USD:USDDeckTabPanel x:Name="ToolbarPanel"  
                             Grid.Column="2"  
                             AutomationProperties.Name="Toolbar Panel"  
                             VerticalAlignment="Center"  
                             Focusable="True"  
                             Margin="0"  
                             USD:PanelNavigation.KeyboardShortcut="CTRL+1"/>  
        <Grid Grid.Column="3"  
              Background="{DynamicResource AboutPanelStandardBackground}">  
          <Grid.ColumnDefinitions>  
            <ColumnDefinition Width="*" />  
            <ColumnDefinition Width="412"/>  
          </Grid.ColumnDefinitions>  
          <USD:USDStackPanel Grid.Column="0"  
                             x:Name="CtiPanel"  
                             Orientation="Horizontal"  
                             Focusable="True"  
                             VerticalAlignment="Center"  
                             AutomationProperties.Name="Cti Panel"/>  
          <USD:USDStackPanel Grid.Column="1"  
                             HorizontalAlignment="Right"  
                             x:Name="AboutPanel"  
                             Orientation="Horizontal"  
                             Focusable="True"  
                             VerticalAlignment="Center"  
                             AutomationProperties.Name="AboutPanel"  
                             USD:PanelNavigation.KeyboardShortcut="CTRL+2"/>  
        </Grid>  
      </Grid>  
    </Border>  
    <Grid Grid.Row="1"  
          VerticalAlignment="Stretch"  
          Margin="0"  
          Background="{DynamicResource WindowBackgroundStyle}">  
      <Grid.RowDefinitions>  
        <RowDefinition Height="auto" />  
        <RowDefinition Height="*" />  
        <RowDefinition Height="auto" />  
      </Grid.RowDefinitions>  
      <USD:USDDeckTabPanel x:Name="SessionTabsPanel"  
                           Grid.Row="0"  
                           Margin="5,5,0,5"  
                           AutomationProperties.Name="Session Tabs Panel"  
                           Focusable="True"  
                           ClipToBounds="True"  
                           USD:PanelNavigation.KeyboardShortcut="CTRL+3"/>  
      <Grid x:Name="MainGrid"  
            Grid.Row="1"  
            AutomationProperties.Name="Main Panels">  
        <Grid.ColumnDefinitions>  
          <ColumnDefinition Width="auto" />  
          <ColumnDefinition Width="*"/>  
          <ColumnDefinition Width="auto"/>  
        </Grid.ColumnDefinitions>  
        <Expander Grid.Column="0"  
                  Style="{DynamicResource StretchExpanderStyle}"  
                  ExpandDirection="Left"  
                  x:Name="ExpanderSessionDetails"  
                  IsExpanded="false"  
                  BorderBrush="White" >  
          <ScrollViewer VerticalScrollBarVisibility="Auto" >  
            <Grid Style="{DynamicResource LeftPanelGrid}"  
                  Margin="5">  
              <Grid.RowDefinitions>  
                <RowDefinition Height="auto" />  
                <RowDefinition Height="auto" />  
                <RowDefinition Height="auto"  
                               Name="ChatPanelRow" />  
                <RowDefinition Height="auto" />  
                <RowDefinition Height="auto" />  
                <RowDefinition Height="auto" />  
              </Grid.RowDefinitions >  
              <USD:USDCollapsePanel x:Name="SessionExplorerPanel"  
                                    AutomationProperties.Name="Session Explorer Panel"  
                                    Grid.Row="0"  
                                    Margin="1"  
                                    USD:PanelNavigation.KeyboardShortcut="CTRL+4"/>  
              <USD:USDCollapsePanel x:Name="WorkflowPanel"  
                                    AutomationProperties.Name="Workflow Panel"  
                                    Grid.Row="1"  
                                    Margin="1"  
                                    USD:PanelNavigation.KeyboardShortcut="CTRL+5"/>  
              <USD:USDCollapsePanel x:Name="ChatPanel"  
                                    AutomationProperties.Name="Workflow Panel"  
                                    Grid.Row="2"  
                                    Margin="1"/>  
              <USD:USDCollapsePanel x:Name="LeftPanel1"  
                                    AutomationProperties.Name="Left Panel 1"  
                                    Grid.Row="3"  
                                    Margin="1"/>  
              <USD:USDCollapsePanel x:Name="LeftPanel2"  
                                    AutomationProperties.Name="Left Panel 2"  
                                    Grid.Row="4"  
                                    Margin="1"/>  
              <USD:USDTabPanel x:Name="LeftPanelFill"  
                               AutomationProperties.Name="Left Panel Fill"  
                               Grid.Row="5"  
                               Margin="1"  
                               MinHeight="300"  
                               USD:PanelNavigation.KeyboardShortcut="CTRL+6"/>  
            </Grid>  
          </ScrollViewer>  

        </Expander>  
        <Grid Grid.Column="1"  
              Background="Transparent">  
          <Grid.RowDefinitions>  
            <RowDefinition Height="0" />  
            <RowDefinition Height="79*" />  
            <RowDefinition Height="125*"/>  
          </Grid.RowDefinitions>  
          <USD:USDCollapsePanel x:Name="RibbonPanel"  
                                Grid.Row="0"  
                                Visibility="Collapsed"  
                                AutomationProperties.Name="Ribbon Panel"  
                                Focusable="True"  
                                Margin="1"  
                                ClipToBounds="False"  
                                SnapsToDevicePixels="True"/>  
          <USD:USDTabPanel x:Name="MainPanel"  
                           Grid.Row="1"  
                           AutomationProperties.Name="Main Panel"  
                           Grid.RowSpan="2"  
                           USD:PanelNavigation.KeyboardShortcut="CTRL+7"/>  
        </Grid>  
        <Expander Grid.Column="2"  
                  Style="{DynamicResource StretchExpanderStyle}"  
                  ExpandDirection="Right"  
                  x:Name="RightPanelExpander"  
                  IsExpanded="false"  
                  BorderBrush="White" >  
          <ScrollViewer VerticalScrollBarVisibility="Auto" >  
            <Grid Style="{DynamicResource LeftPanelGrid}" >  
              <Grid.RowDefinitions>  
                <RowDefinition Height="*" />  
              </Grid.RowDefinitions >  
              <USD:USDTabPanel x:Name="RightPanel"  
                               AutomationProperties.Name="Right Panel"  
                               Grid.Row="0"  
                               USD:PanelNavigation.KeyboardShortcut="CTRL+8"/>  
              <USD:USDPopupPanel x:Name="RightPopupPanel"  
                                 Height="{Binding ActualHeight, ElementName=RightPanel, Mode=OneWay}"  
                                 Width="{Binding ActualWidth, ElementName=RightPanel, Mode=OneWay}"  
                                 Placement="Left"  
                                 PlacementTarget="{Binding ElementName=RightPanel}"  
                                 PopupAnimation="Scroll"  
                                 USD:PanelNavigation.KeyboardShortcut="CTRL+9">  
                <Grid>  
                  <Grid.RowDefinitions>  
                    <RowDefinition Height="20" />  
                    <RowDefinition Height="*" />  
                  </Grid.RowDefinitions>  
                  <Border Background="#cccccc"  
                          Grid.Row="0" >  
                    <TextBlock Text="Article Preview"  
                               HorizontalAlignment="Center"  
                               Margin="10,0,0,0" />  
                  </Border>  
                  <Border BorderThickness="1"  
                          Grid.Row="1"  
                          BorderBrush="#cccccc"  
                          Background="White">  
                    <ContentControl  Margin="0,0,0,0"  
                                     Name="PopupContainer"  
                                     Style="{DynamicResource USDContentControlStyle}"/>  
                  </Border>  
                </Grid>  
              </USD:USDPopupPanel>  
            </Grid>  
          </ScrollViewer>  
        </Expander>  
      </Grid>  
    </Grid>  
    <StatusBar Grid.Row="2"  
               Style="{DynamicResource StatusBarStyle}">  
      <StatusBarItem>  
        <TextBlock x:Name="lblStatusBarClock"  
                   Text="00:00 AM/PM"  
                   Style="{DynamicResource StatusBarClockLabelStyle}"/>  
      </StatusBarItem>  
      <Separator Style="{DynamicResource StatusBarSeparatorStyle}"/>  
      <StatusBarItem >  
        <USD:USDStackPanel x:Name="StatusPanel"  
                           Orientation="Horizontal"  
                           AutomationProperties.Name="Status Panel"  
                           Margin="1"/>  
      </StatusBarItem>  
    </StatusBar>  
  </Grid>  
</USD:PanelLayoutBase>  
```  

 <span data-ttu-id="060fa-200">**Bảng điều khiển chính Ruy băng**</span><span class="sxs-lookup"><span data-stu-id="060fa-200">**Ribbon Main Panel**</span></span>  
 <span data-ttu-id="060fa-201">For internal use only.</span><span class="sxs-lookup"><span data-stu-id="060fa-201">For internal use only.</span></span>  

 <span data-ttu-id="060fa-202">**Phân chia theo hướng ngang**</span><span class="sxs-lookup"><span data-stu-id="060fa-202">**Horizontal Split**</span></span>  
 <span data-ttu-id="060fa-203">This is a special layout typically used within the MainPanel as a hosted control.</span><span class="sxs-lookup"><span data-stu-id="060fa-203">This is a special layout typically used within the MainPanel as a hosted control.</span></span> <span data-ttu-id="060fa-204">Nó chứa một bộ chia với bảng điều khiển trên đầu và bảng điều khiển ở dưới.</span><span class="sxs-lookup"><span data-stu-id="060fa-204">It contains a splitter with a top panel and a bottom panel.</span></span> <span data-ttu-id="060fa-205">Nó thường được sử dụng để hiển thị chế độ xem danh sách ở đầu và chế độ xem chi tiết ở cuối tương tự như Outlook.</span><span class="sxs-lookup"><span data-stu-id="060fa-205">It is typically used to display a list view at top and a detail view at the bottom similar to Outlook.</span></span> <span data-ttu-id="060fa-206">Hai bảng điều khiển được xác định trong bố cục này.</span><span class="sxs-lookup"><span data-stu-id="060fa-206">Two panels are defined in this layout.</span></span>  

|<span data-ttu-id="060fa-207">Tên bảng điều khiển</span><span class="sxs-lookup"><span data-stu-id="060fa-207">Panel Name</span></span>|<span data-ttu-id="060fa-208">Mô tả</span><span class="sxs-lookup"><span data-stu-id="060fa-208">Description</span></span>|  
|----------------|-----------------|  
|<span data-ttu-id="060fa-209">TopPanel</span><span class="sxs-lookup"><span data-stu-id="060fa-209">TopPanel</span></span>|<span data-ttu-id="060fa-210">Đây là bảng điều khiển hiển thị trên đầu.</span><span class="sxs-lookup"><span data-stu-id="060fa-210">This is the panel that displays on top.</span></span> <span data-ttu-id="060fa-211">Nó được định nghĩa là:</span><span class="sxs-lookup"><span data-stu-id="060fa-211">It is defined as:</span></span><br /><br /> <span data-ttu-id="060fa-212">Bảng điều khiển tab sàn USD</span><span class="sxs-lookup"><span data-stu-id="060fa-212">USDDeckTabPanel</span></span>|  
|<span data-ttu-id="060fa-213">BottomPanel</span><span class="sxs-lookup"><span data-stu-id="060fa-213">BottomPanel</span></span>|<span data-ttu-id="060fa-214">Đây là bảng điều khiển hiển thị phía dưới.</span><span class="sxs-lookup"><span data-stu-id="060fa-214">This is the panel that displays on bottom.</span></span> <span data-ttu-id="060fa-215">It is defined as:</span><span class="sxs-lookup"><span data-stu-id="060fa-215">It is defined as:</span></span><br /><br /> <span data-ttu-id="060fa-216">Bảng điều khiển tab sàn USD</span><span class="sxs-lookup"><span data-stu-id="060fa-216">USDDeckTabPanel</span></span>|  

 <span data-ttu-id="060fa-217">Bản điều khiển này hỗ trợ các thao tác sau:</span><span class="sxs-lookup"><span data-stu-id="060fa-217">This panel supports the following actions:</span></span>  


|        <span data-ttu-id="060fa-218">Hành động</span><span class="sxs-lookup"><span data-stu-id="060fa-218">Action</span></span>        |                                                                                                                                                                                                                                                                                              <span data-ttu-id="060fa-219">Mô tả</span><span class="sxs-lookup"><span data-stu-id="060fa-219">Description</span></span>                                                                                                                                                                                                                                                                                              |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <span data-ttu-id="060fa-220">SetTopPanelHeight</span><span class="sxs-lookup"><span data-stu-id="060fa-220">SetTopPanelHeight</span></span>   | <span data-ttu-id="060fa-221">Hành động này có thể được sử dụng để đặt chiều cao của bảng điều khiển ở trên đầu.</span><span class="sxs-lookup"><span data-stu-id="060fa-221">This action can be used to set the top panel height.</span></span> <span data-ttu-id="060fa-222">Nó hỗ trợ hai tham số, chiều cao và loại.</span><span class="sxs-lookup"><span data-stu-id="060fa-222">It supports two parameters, height and type.</span></span><br /><br /> <span data-ttu-id="060fa-223">Loại có thể là bất kỳ giá trị nào sau đây:</span><span class="sxs-lookup"><span data-stu-id="060fa-223">Type can be any of the following values:</span></span><br /><br /> <span data-ttu-id="060fa-224">- **Tự động**: được đặt kích thước để phù hợp với thành phần bên trong</span><span class="sxs-lookup"><span data-stu-id="060fa-224">- **Auto**: sized to fix components inside</span></span><br /><span data-ttu-id="060fa-225">- **Điểm ảnh**: số điểm ảnh</span><span class="sxs-lookup"><span data-stu-id="060fa-225">- **Pixel**: the number of pixels</span></span><br /><span data-ttu-id="060fa-226">- **Sao**: chiếm không gian còn lại</span><span class="sxs-lookup"><span data-stu-id="060fa-226">- **Star**: takes the remaining space</span></span><br /><br /> <span data-ttu-id="060fa-227">Việc giải thích của các tham số chiều cao phụ thuộc vào giá trị loại này.</span><span class="sxs-lookup"><span data-stu-id="060fa-227">The interpretation of the height parameter depends on this type value.</span></span> <span data-ttu-id="060fa-228">For more information, see the [!INCLUDE[pn_ms_Windows_Presentation_Foundation](../includes/pn-ms-windows-presentation-foundation.md)][documentation](http://msdn.microsoft.com/library/ms754130\(v=vs.100\).aspx).</span><span class="sxs-lookup"><span data-stu-id="060fa-228">For more information, see the [!INCLUDE[pn_ms_Windows_Presentation_Foundation](../includes/pn-ms-windows-presentation-foundation.md)][documentation](http://msdn.microsoft.com/library/ms754130\(v=vs.100\).aspx).</span></span> |
| <span data-ttu-id="060fa-229">SetBottomPanelHeight</span><span class="sxs-lookup"><span data-stu-id="060fa-229">SetBottomPanelHeight</span></span> |                                              <span data-ttu-id="060fa-230">Hành động này có thể được sử dụng để đặt chiều cao của bảng điều khiển ở phía dưới.</span><span class="sxs-lookup"><span data-stu-id="060fa-230">This action can be used to set the bottom panel height.</span></span> <span data-ttu-id="060fa-231">It supports two parameters, height and type.</span><span class="sxs-lookup"><span data-stu-id="060fa-231">It supports two parameters, height and type.</span></span><br /><br /> <span data-ttu-id="060fa-232">Loại có thể là bất kỳ giá trị nào sau đây:</span><span class="sxs-lookup"><span data-stu-id="060fa-232">Type can be any of the following values:</span></span><br /><br /> <span data-ttu-id="060fa-233">- **Tự động**: được đặt kích thước để phù hợp với thành phần bên trong</span><span class="sxs-lookup"><span data-stu-id="060fa-233">- **Auto**: sized to fix components inside</span></span><br /><span data-ttu-id="060fa-234">- **Điểm ảnh**: số điểm ảnh</span><span class="sxs-lookup"><span data-stu-id="060fa-234">- **Pixel**: the number of pixels</span></span><br /><span data-ttu-id="060fa-235">- **Sao**: chiếm không gian còn lại</span><span class="sxs-lookup"><span data-stu-id="060fa-235">- **Star**: takes the remaining space</span></span><br /><br /> <span data-ttu-id="060fa-236">Việc giải thích của các tham số chiều cao phụ thuộc vào giá trị loại này.</span><span class="sxs-lookup"><span data-stu-id="060fa-236">The interpretation of the height parameter depends on this type value.</span></span> <span data-ttu-id="060fa-237">Để biết thêm thông tin, xem tài liệu [WPF](http://msdn.microsoft.com/en-us/library/ms754130\(v=vs.100\).aspx).</span><span class="sxs-lookup"><span data-stu-id="060fa-237">For more information, see the WPF [documentation](http://msdn.microsoft.com/en-us/library/ms754130\(v=vs.100\).aspx).</span></span>                                              |

 <span data-ttu-id="060fa-238">**Phân chia theo chiều dọc**</span><span class="sxs-lookup"><span data-stu-id="060fa-238">**Vertical Split**</span></span>  
 <span data-ttu-id="060fa-239">Đây là một bố cục đặc biệt có chứa bộ phân chia theo hướng dọc với một bảng điều khiển bên trái và một bảng điều khiển bên phải.</span><span class="sxs-lookup"><span data-stu-id="060fa-239">This is a special layout that contains a vertical splitter with a left panel and a right panel.</span></span>  

|<span data-ttu-id="060fa-240">Tên bảng điều khiển</span><span class="sxs-lookup"><span data-stu-id="060fa-240">Panel Name</span></span>|<span data-ttu-id="060fa-241">Mô tả</span><span class="sxs-lookup"><span data-stu-id="060fa-241">Description</span></span>|  
|----------------|-----------------|  
|<span data-ttu-id="060fa-242">LeftPanel</span><span class="sxs-lookup"><span data-stu-id="060fa-242">LeftPanel</span></span>|<span data-ttu-id="060fa-243">Đây là bảng điều khiển hiển thị bên trái.</span><span class="sxs-lookup"><span data-stu-id="060fa-243">This is the panel that displays on left.</span></span> <span data-ttu-id="060fa-244">It is defined as:</span><span class="sxs-lookup"><span data-stu-id="060fa-244">It is defined as:</span></span><br /><br /> <span data-ttu-id="060fa-245">Bảng điều khiển tab sàn USD</span><span class="sxs-lookup"><span data-stu-id="060fa-245">USDDeckTabPanel</span></span>|  
|<span data-ttu-id="060fa-246">RightPanel</span><span class="sxs-lookup"><span data-stu-id="060fa-246">RightPanel</span></span>|<span data-ttu-id="060fa-247">Đây là bảng điều khiển hiển thị bên phải.</span><span class="sxs-lookup"><span data-stu-id="060fa-247">This is the panel that displays on right.</span></span> <span data-ttu-id="060fa-248">It is defined as:</span><span class="sxs-lookup"><span data-stu-id="060fa-248">It is defined as:</span></span><br /><br /> <span data-ttu-id="060fa-249">Bảng điều khiển tab sàn USD</span><span class="sxs-lookup"><span data-stu-id="060fa-249">USDDeckTabPanel</span></span>|  

 <span data-ttu-id="060fa-250">This panel supports the following actions:</span><span class="sxs-lookup"><span data-stu-id="060fa-250">This panel supports the following actions:</span></span>  

|<span data-ttu-id="060fa-251">Hành động</span><span class="sxs-lookup"><span data-stu-id="060fa-251">Action</span></span>|<span data-ttu-id="060fa-252">Mô tả</span><span class="sxs-lookup"><span data-stu-id="060fa-252">Description</span></span>|  
|------------|-----------------|  
|<span data-ttu-id="060fa-253">SetLeftPanelWidth</span><span class="sxs-lookup"><span data-stu-id="060fa-253">SetLeftPanelWidth</span></span>|<span data-ttu-id="060fa-254">Hành động này có thể được sử dụng để đặt chiều rộng của bảng điều khiển bên trái.</span><span class="sxs-lookup"><span data-stu-id="060fa-254">This action can be used to set the left panel width.</span></span> <span data-ttu-id="060fa-255">Nó hỗ trợ hai tham số, chiều rộng và loại.</span><span class="sxs-lookup"><span data-stu-id="060fa-255">It supports two parameters, width and type.</span></span><br /><br /> <span data-ttu-id="060fa-256">Loại có thể là bất kỳ giá trị nào sau đây:</span><span class="sxs-lookup"><span data-stu-id="060fa-256">Type can be any of the following values:</span></span><br /><br /> <span data-ttu-id="060fa-257">- **Tự động**: được đặt kích thước để phù hợp với thành phần bên trong</span><span class="sxs-lookup"><span data-stu-id="060fa-257">- **Auto**: sized to fix components inside</span></span><br /><span data-ttu-id="060fa-258">- **Điểm ảnh**: số điểm ảnh</span><span class="sxs-lookup"><span data-stu-id="060fa-258">- **Pixel**: the number of pixels</span></span><br /><span data-ttu-id="060fa-259">- **Sao**: chiếm không gian còn lại</span><span class="sxs-lookup"><span data-stu-id="060fa-259">- **Star**: takes the remaining space</span></span><br /><br /> <span data-ttu-id="060fa-260">Việc giải thích của các tham số chiều rộng phụ thuộc vào giá trị loại này.</span><span class="sxs-lookup"><span data-stu-id="060fa-260">The interpretation of the width parameter depends on this type value.</span></span> <span data-ttu-id="060fa-261">Để biết thêm thông tin, xem tài liệu [WPF](http://msdn.microsoft.com/library/ms754130\(v=vs.100\).aspx).</span><span class="sxs-lookup"><span data-stu-id="060fa-261">For more information, see the WPF [documentation](http://msdn.microsoft.com/library/ms754130\(v=vs.100\).aspx).</span></span>|  
|<span data-ttu-id="060fa-262">SetRightPanelWidth</span><span class="sxs-lookup"><span data-stu-id="060fa-262">SetRightPanelWidth</span></span>|<span data-ttu-id="060fa-263">Hành động này có thể được sử dụng để đặt chiều rộng của bảng điều khiển bên phải.</span><span class="sxs-lookup"><span data-stu-id="060fa-263">This action can be used to set the right panel width.</span></span> <span data-ttu-id="060fa-264">It supports two parameters, width and type.</span><span class="sxs-lookup"><span data-stu-id="060fa-264">It supports two parameters, width and type.</span></span><br /><br /> <span data-ttu-id="060fa-265">Loại có thể là bất kỳ giá trị nào sau đây:</span><span class="sxs-lookup"><span data-stu-id="060fa-265">Type can be any of the following values:</span></span><br /><br /> <span data-ttu-id="060fa-266">- **Tự động**: được đặt kích thước để phù hợp với thành phần bên trong</span><span class="sxs-lookup"><span data-stu-id="060fa-266">- **Auto**: sized to fix components inside</span></span><br /><span data-ttu-id="060fa-267">- **Điểm ảnh**: số điểm ảnh</span><span class="sxs-lookup"><span data-stu-id="060fa-267">- **Pixel**: the number of pixels</span></span><br /><span data-ttu-id="060fa-268">- **Sao**: chiếm không gian còn lại</span><span class="sxs-lookup"><span data-stu-id="060fa-268">- **Star**: takes the remaining space</span></span><br /><br /> <span data-ttu-id="060fa-269">Việc giải thích của các tham số chiều rộng phụ thuộc vào giá trị loại này.</span><span class="sxs-lookup"><span data-stu-id="060fa-269">The interpretation of the width parameter depends on this type value.</span></span> <span data-ttu-id="060fa-270">Xem tài liệu WPF để biết thêm chi tiết.</span><span class="sxs-lookup"><span data-stu-id="060fa-270">See the WPF documentation for more details.</span></span>|  

 <span data-ttu-id="060fa-271">**XAML**</span><span class="sxs-lookup"><span data-stu-id="060fa-271">**XAML**</span></span>  
 <span data-ttu-id="060fa-272">Một trong những cách nhanh nhất để tạo bố cục tùy chỉnh.</span><span class="sxs-lookup"><span data-stu-id="060fa-272">One of the quickest ways to create a custom layout.</span></span> <span data-ttu-id="060fa-273">Tuy nhiên, tùy chọn này không hỗ trợ mã-đằng sau.</span><span class="sxs-lookup"><span data-stu-id="060fa-273">However, this option does not support code-behind.</span></span> <span data-ttu-id="060fa-274">Kết quả là, nếu bạn không thể mô tả bố cục của mình mà không có mã, bạn không thể sử dụng tùy chọn này và thay vào đó nên sử dụng tùy chọn **Do người dùng xác định**.</span><span class="sxs-lookup"><span data-stu-id="060fa-274">As a result, if you can’t describe your layout without code, you can’t use this option and should instead use the **User Defined** option.</span></span> <span data-ttu-id="060fa-275">For more information, see [Code-Behind and XAML in WPF](http://msdn.microsoft.com/library/aa970568\(v=vs.100\).aspx).</span><span class="sxs-lookup"><span data-stu-id="060fa-275">For more information, see [Code-Behind and XAML in WPF](http://msdn.microsoft.com/library/aa970568\(v=vs.100\).aspx).</span></span>  

 <span data-ttu-id="060fa-276">Here is an example of a XAML layout.</span><span class="sxs-lookup"><span data-stu-id="060fa-276">Here is an example of a XAML layout.</span></span>  

```xaml  
<Grid xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"  
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"  
    xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"   
    xmlns:d="http://schemas.microsoft.com/expression/blend/2008"   
    mc:Ignorable="d" xmlns: USD="clr-namespace:Dynamics.PanelLayouts;assembly=Dynamics">  
 <Grid.RowDefinitions>  
 <RowDefinition Height="*" x:Name="TopPanelRow" />  
 <RowDefinition Height="auto" />  
 <RowDefinition Height="*" x:Name="BottomPanelRow" />  
 </Grid.RowDefinitions>  
 < USD: USDDeckTabPanel Grid.Row="1" x:Name="TopPanel" Focusable="False" ClipToBounds="True" />  
 <GridSplitter Height="5" Grid.Row="2" VerticalAlignment="Top" HorizontalAlignment="Stretch" ResizeDirection="Rows" ResizeBehavior="PreviousAndNext" />  
 <USD: USDDeckTabPanel Grid.Row="3" x:Name="BottomPanel" />  
</Grid>  
```  

 <span data-ttu-id="060fa-277">**Do người dùng xác định**</span><span class="sxs-lookup"><span data-stu-id="060fa-277">**User Defined**</span></span>  
 <span data-ttu-id="060fa-278">Thiết đặt này cho phép bạn xây dựng kiểm soát tổ chức với [mã đằng sau](http://msdn.microsoft.com/library/aa970568\(v=vs.100\).aspx) để nhận đầy đủ tính năng của of .NET trong khi xử lý bố cục của bạn.</span><span class="sxs-lookup"><span data-stu-id="060fa-278">This setting allows you to build a hosted control with [code behind](http://msdn.microsoft.com/library/aa970568\(v=vs.100\).aspx) to gain the full features of .NET in handling your layout.</span></span>  

 <span data-ttu-id="060fa-279">For details about what panel types can be defined and used in a user defined panel, see [Panel types](../unified-service-desk/panels-panel-types-panel-layouts.md#PanelTypes).</span><span class="sxs-lookup"><span data-stu-id="060fa-279">For details about what panel types can be defined and used in a user defined panel, see [Panel types](../unified-service-desk/panels-panel-types-panel-layouts.md#PanelTypes).</span></span>  

 <span data-ttu-id="060fa-280">For information about creating a custom panel layout, see [Create a custom panel layout](../unified-service-desk/create-custom-panel-layout.md).</span><span class="sxs-lookup"><span data-stu-id="060fa-280">For information about creating a custom panel layout, see [Create a custom panel layout](../unified-service-desk/create-custom-panel-layout.md).</span></span>  

### <a name="see-also"></a><span data-ttu-id="060fa-281">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="060fa-281">See also</span></span>  
 <span data-ttu-id="060fa-282">[Sử dụng loại bảng điều khiển tùy chỉnh và bố cục bảng điều khiển](../unified-service-desk/use-custom-panel-types-panel-layouts-unified-service-desk.md) </span><span class="sxs-lookup"><span data-stu-id="060fa-282">[Use custom panel types and panel layouts](../unified-service-desk/use-custom-panel-types-panel-layouts-unified-service-desk.md) </span></span>  
 [<span data-ttu-id="060fa-283">Keyboard shortcuts for panels</span><span class="sxs-lookup"><span data-stu-id="060fa-283">Keyboard shortcuts for panels</span></span>](../unified-service-desk/keyboard-shortcuts-panels.md)
