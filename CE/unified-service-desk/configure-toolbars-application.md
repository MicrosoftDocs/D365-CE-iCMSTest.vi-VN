---
title: Configure toolbars in your application | MicrosoftDocs
description: Learn about configuring toolbars in your application.
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
ms.assetid: 61cf4cb9-71ed-40c8-bbfa-c846c45cfb74
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 03b9de6430a641e74e8b935d07d5332772a801c9
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387059"
---
# <a name="configure-toolbars-in-your-application"></a><span data-ttu-id="44aa7-103">Configure toolbars in your application</span><span class="sxs-lookup"><span data-stu-id="44aa7-103">Configure toolbars in your application</span></span>
<span data-ttu-id="44aa7-104">Bạn có thể cấu hình thanh công cụ trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] để tạo ra hoặc quản lý nút trong thanh công cụ hiện có, hoặc tạo ra các thanh công cụ mới hoàn toàn.</span><span class="sxs-lookup"><span data-stu-id="44aa7-104">You can configure toolbars in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] to create or manage buttons in an existing toolbar, or create new toolbars altogether.</span></span> <span data-ttu-id="44aa7-105">For an overview of toolbars, see [Toolbars in Unified Service Desk](../unified-service-desk/toolbars-unified-service-desk.md).</span><span class="sxs-lookup"><span data-stu-id="44aa7-105">For an overview of toolbars, see [Toolbars in Unified Service Desk](../unified-service-desk/toolbars-unified-service-desk.md).</span></span>  
  
<a name="Create"></a>  

## <a name="create-a-toolbar"></a><span data-ttu-id="44aa7-106">Tạo thanh công cụ</span><span class="sxs-lookup"><span data-stu-id="44aa7-106">Create a toolbar</span></span>  
 <span data-ttu-id="44aa7-107">Trước khi tạo một thanh công cụ, đảm bảo là đã có kiểm soát tổ chức vùng chứa thanh công cụ được cấu hình.</span><span class="sxs-lookup"><span data-stu-id="44aa7-107">Before creating a toolbar, ensure that there is a toolbar container hosted control already configured.</span></span> <span data-ttu-id="44aa7-108">For more information, see [Toolbar Container (Hosted Control)](../unified-service-desk/toolbar-container-hosted-control.md).</span><span class="sxs-lookup"><span data-stu-id="44aa7-108">For more information, see [Toolbar Container (Hosted Control)](../unified-service-desk/toolbar-container-hosted-control.md).</span></span>  
  
1. <span data-ttu-id="44aa7-109">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="44aa7-109">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  
  
3. <span data-ttu-id="44aa7-110">Bấm vào **Thanh công cụ**.</span><span class="sxs-lookup"><span data-stu-id="44aa7-110">Click **Toolbars**.</span></span>  
  
4. <span data-ttu-id="44aa7-111">Trên trang thanh công cụ, bấm vào **Mới** trên thanh lệnh.</span><span class="sxs-lookup"><span data-stu-id="44aa7-111">On the toolbars page, click **New** on the command bar.</span></span>  
  
5. <span data-ttu-id="44aa7-112">Trên trang **Thanh công cụ mới** và.</span><span class="sxs-lookup"><span data-stu-id="44aa7-112">On the **New Toolbar** page, and.</span></span>  
  
   1.  <span data-ttu-id="44aa7-113">Nhập tên cho thanh công cụ mới.</span><span class="sxs-lookup"><span data-stu-id="44aa7-113">Type a name for the new toolbar.</span></span>  
  
   2.  <span data-ttu-id="44aa7-114">Nhập một tiêu đề cho thanh công cụ, mà sẽ được hiển thị trên bờ trái của dải thanh công cụ.</span><span class="sxs-lookup"><span data-stu-id="44aa7-114">Type a title for the toolbar, which is displayed on the left edge of the toolbar strip.</span></span>  
  
   3.  <span data-ttu-id="44aa7-115">Bấm vào **Lưu** để bật vùng **nút**.</span><span class="sxs-lookup"><span data-stu-id="44aa7-115">Click **Save** to enable the **Buttons** area.</span></span>  
  
6. <span data-ttu-id="44aa7-116">Under the **Buttons** area, click **+** to create a button to be placed on the toolbar.</span><span class="sxs-lookup"><span data-stu-id="44aa7-116">Under the **Buttons** area, click **+** to create a button to be placed on the toolbar.</span></span>  
  
7. <span data-ttu-id="44aa7-117">Trên trang **Nút Thanh công cụ mới**:</span><span class="sxs-lookup"><span data-stu-id="44aa7-117">On the **New Toolbar Button** page:</span></span>  
  
   1.  <span data-ttu-id="44aa7-118">Chỉ định tên của nút.</span><span class="sxs-lookup"><span data-stu-id="44aa7-118">Specify the name of the button.</span></span>  
  
   2.  <span data-ttu-id="44aa7-119">Chỉ định tên của tập tin hình ảnh cho nút thanh công cụ.</span><span class="sxs-lookup"><span data-stu-id="44aa7-119">Specify the name of the image file for the toolbar button.</span></span>  
  
   3.  <span data-ttu-id="44aa7-120">Trong trường **ButtonText**, nhập nhãn của nút.</span><span class="sxs-lookup"><span data-stu-id="44aa7-120">In the **ButtonText** field, type the label of the button.</span></span>  
  
   4.  <span data-ttu-id="44aa7-121">Để kiểm soát thứ tự hiển thị các nút trên thanh công cụ từ bên trái sang phải, chỉ định một giá trị số nguyên trong trường **Thứ tự**.</span><span class="sxs-lookup"><span data-stu-id="44aa7-121">To control the left to right order in which the buttons are displayed on the toolbar, specify an integer value in the **Order** field.</span></span> <span data-ttu-id="44aa7-122">Nút được sắp xếp từ trái sang phải theo một thứ tự tăng dần.</span><span class="sxs-lookup"><span data-stu-id="44aa7-122">The buttons are arranged from left to right in the ascending order.</span></span>  
  
   5.  <span data-ttu-id="44aa7-123">Bấm vào **Lưu** để bật vùng **Hoạt động**.</span><span class="sxs-lookup"><span data-stu-id="44aa7-123">Click **Save** to enable the **Actions** area.</span></span>  
  
8. <span data-ttu-id="44aa7-124">Under the **Actions** area, click **+** to add an action call to the button.</span><span class="sxs-lookup"><span data-stu-id="44aa7-124">Under the **Actions** area, click **+** to add an action call to the button.</span></span>  
  
9. <span data-ttu-id="44aa7-125">Trong hộp tìm kiếm trong vùng **hành động** lá, gõ tên cuộc gọi hành động mà bạn muốn gắn vào nút.</span><span class="sxs-lookup"><span data-stu-id="44aa7-125">In the search box in Under the **Actions** area, type the name of the action call that you want to attach to the button.</span></span> <span data-ttu-id="44aa7-126">Nếu bạn muốn gắn nút vào cuộc gọi hành động mới, bấm vào **Mới**, và sau đó thêm tạo cuộc gọi hành động và sau đó thêm nó vào hành động UII.</span><span class="sxs-lookup"><span data-stu-id="44aa7-126">If you want to attach the button to a new action call, click **New**, and then add create an action call and then add it to the UII action.</span></span> <span data-ttu-id="44aa7-127">For more information, see [Create an action call for a UII action](../unified-service-desk/create-action-call-uii-action.md).</span><span class="sxs-lookup"><span data-stu-id="44aa7-127">For more information, see [Create an action call for a UII action](../unified-service-desk/create-action-call-uii-action.md).</span></span>  
  
10. <span data-ttu-id="44aa7-128">Để có thêm nút trên thanh công cụ, hãy làm theo bước 6-9.</span><span class="sxs-lookup"><span data-stu-id="44aa7-128">For additional button on the toolbar, follow steps 6-9.</span></span>  
  
11. <span data-ttu-id="44aa7-129">Sau khi thêm các nút và cuộc gọi hành động vào thanh công cụ, gắn thanh công cụ vào bộ chứa thanh công cụ.</span><span class="sxs-lookup"><span data-stu-id="44aa7-129">After adding buttons and action calls to a toolbar, attach the toolbar to a toolbar container.</span></span> <span data-ttu-id="44aa7-130">Điều này được thực hiện để xác định vị trí của thanh công cụ mới trên màn hình của trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="44aa7-130">This is done to specify the location of the new toolbar on the desktop of in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> <span data-ttu-id="44aa7-131">Với đinh nghĩa thanh công cụ đang mở, nhấp vào mũi tên xuống bên cạnh tên thanh công cụ, và sau đó chọn **Kiểm soát tổ chức**.</span><span class="sxs-lookup"><span data-stu-id="44aa7-131">With the toolbar definition open, click the down arrow next to the toolbar name, and then select **Hosted Controls**.</span></span>  
  
12. <span data-ttu-id="44aa7-132">Trên trang tiếp theo, bấm vào **Thêm ứng dụng kiểm soát tổ chức hiện tại**.</span><span class="sxs-lookup"><span data-stu-id="44aa7-132">On the next page, click **Add Existing Hosted Application**.</span></span>  
  
13. <span data-ttu-id="44aa7-133">Trong hộp tìm kiếm, gõ tên của kiểm soát tổ chức bộ chứa thanh công cụ, nhấp vào tìm kiếm, và sau đó chọn kiểm soát tổ chức.</span><span class="sxs-lookup"><span data-stu-id="44aa7-133">In the search box, type the name of the toolbar container hosted control, click search, and then select the hosted control.</span></span>  
  
14. <span data-ttu-id="44aa7-134">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="44aa7-134">Click **Save**.</span></span> 

15. <span data-ttu-id="44aa7-135">Under the **Styles** area, in the **Custom Styles** text box, write the XAML string to customize the toolbar and buttons.</span><span class="sxs-lookup"><span data-stu-id="44aa7-135">Under the **Styles** area, in the **Custom Styles** text box, write the XAML string to customize the toolbar and buttons.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="44aa7-136">[Styles in toolbar](#styles-in-toolbar)</span><span class="sxs-lookup"><span data-stu-id="44aa7-136">[Styles in toolbar](#styles-in-toolbar)</span></span>

16. <span data-ttu-id="44aa7-137">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="44aa7-137">Click **Save**.</span></span> 
  
<a name="EditToolbar"></a> 

## <a name="addremove-button-from-existing-toolbar"></a><span data-ttu-id="44aa7-138">Thêm/xóa nút khỏi thanh công cụ hiện tại</span><span class="sxs-lookup"><span data-stu-id="44aa7-138">Add/remove button from existing toolbar</span></span>  
  
1. <span data-ttu-id="44aa7-139">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="44aa7-139">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  
  
3. <span data-ttu-id="44aa7-140">Bấm vào **Thanh công cụ**.</span><span class="sxs-lookup"><span data-stu-id="44aa7-140">Click **Toolbars**.</span></span>  
  
4. <span data-ttu-id="44aa7-141">Trên trang thanh công cụ, bấm vào tên của thanh công cụ mà bạn muốn sửa đổi.</span><span class="sxs-lookup"><span data-stu-id="44aa7-141">On the toolbars page, click the name of the toolbar that you want to modify.</span></span>  
  
5. <span data-ttu-id="44aa7-142">Trang tiếp theo hiển thị định nghĩa thanh công cụ.</span><span class="sxs-lookup"><span data-stu-id="44aa7-142">The next page displays the toolbar definition.</span></span>  
  
   1.  <span data-ttu-id="44aa7-143">Thêm nhiều nút sử dụng vùng **nút**.</span><span class="sxs-lookup"><span data-stu-id="44aa7-143">Add more buttons using the **Buttons** area.</span></span> <span data-ttu-id="44aa7-144">Để biết thêm chi tiết, xem các bước 6-10 như trong phần trước.</span><span class="sxs-lookup"><span data-stu-id="44aa7-144">For more information, see steps 6-10 as in the previous section.</span></span>  
  
   2.  <span data-ttu-id="44aa7-145">Modify an existing button by clicking the button name under the **Buttons**, This opens the button definition page where you can change information about the button, such as bname, button text (label), order, and action call.</span><span class="sxs-lookup"><span data-stu-id="44aa7-145">Modify an existing button by clicking the button name under the **Buttons**, This opens the button definition page where you can change information about the button, such as bname, button text (label), order, and action call.</span></span>  
  
   3.  <span data-ttu-id="44aa7-146">Bấm vào **Lưu** để lưu thay đổi của bạn.</span><span class="sxs-lookup"><span data-stu-id="44aa7-146">Click **Save** to save the changes.</span></span>

<a name="StylesToolbar"></a>  
 
## <a name="styles-in-toolbar"></a><span data-ttu-id="44aa7-147">Styles in toolbar</span><span class="sxs-lookup"><span data-stu-id="44aa7-147">Styles in toolbar</span></span>

<span data-ttu-id="44aa7-148">You can now customize the toolbar in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] using the custom styles field in the Toolbar configuration window.</span><span class="sxs-lookup"><span data-stu-id="44aa7-148">You can now customize the toolbar in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] using the custom styles field in the Toolbar configuration window.</span></span>  <span data-ttu-id="44aa7-149">The Custom Styles field supports Extensible Application Markup Language (XAML) that defines <xref:System.Windows.ResourceDictionary> of <xref:System.Windows.Style> and <xref:System.Windows.Media.Brush> resources.</span><span class="sxs-lookup"><span data-stu-id="44aa7-149">The Custom Styles field supports Extensible Application Markup Language (XAML) that defines <xref:System.Windows.ResourceDictionary> of <xref:System.Windows.Style> and <xref:System.Windows.Media.Brush> resources.</span></span>
 
<span data-ttu-id="44aa7-150">The resources in the dictionary refers to other resources that are available on [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application.</span><span class="sxs-lookup"><span data-stu-id="44aa7-150">The resources in the dictionary refers to other resources that are available on [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application.</span></span> <span data-ttu-id="44aa7-151">Loading and parsing the XAML string is performed at runtime to create <xref:System.Windows.ResourceDictionary> and merge the resources of the toolbar control with the <xref:System.Windows.ResourceDictionary>.</span><span class="sxs-lookup"><span data-stu-id="44aa7-151">Loading and parsing the XAML string is performed at runtime to create <xref:System.Windows.ResourceDictionary> and merge the resources of the toolbar control with the <xref:System.Windows.ResourceDictionary>.</span></span> <span data-ttu-id="44aa7-152">In addition, the <xref:System.Windows.ResourceDictionary> can have styles for button types inside a toolbar.</span><span class="sxs-lookup"><span data-stu-id="44aa7-152">In addition, the <xref:System.Windows.ResourceDictionary> can have styles for button types inside a toolbar.</span></span> <span data-ttu-id="44aa7-153">Using the styles, you can customize the toolbars and buttons.</span><span class="sxs-lookup"><span data-stu-id="44aa7-153">Using the styles, you can customize the toolbars and buttons.</span></span>

<span data-ttu-id="44aa7-154">**Sample 1:** The sample XAML that defines <xref:System.Windows.ResourceDictionary> of <xref:System.Windows.Style> and <xref:System.Windows.Media.Brush> resources demonstrates customizing the **About Tool bar**.</span><span class="sxs-lookup"><span data-stu-id="44aa7-154">**Sample 1:** The sample XAML that defines <xref:System.Windows.ResourceDictionary> of <xref:System.Windows.Style> and <xref:System.Windows.Media.Brush> resources demonstrates customizing the **About Tool bar**.</span></span>

> [!NOTE]
> <span data-ttu-id="44aa7-155">You can find this sample XAML styles in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] - Unified Interface sample package.</span><span class="sxs-lookup"><span data-stu-id="44aa7-155">You can find this sample XAML styles in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] - Unified Interface sample package.</span></span>

  ```XAML
  <ResourceDictionary xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation" 
  xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml" 
  xmlns:usd="clr-namespace:Microsoft.Crm.UnifiedServiceDesk.Dynamics;assembly=Microsoft.Crm.UnifiedServiceDesk.Dynamics" 
  xmlns:controlStyles="clr-namespace:Microsoft.Crm.UnifiedServiceDesk.Dynamics.Controls.Styles;assembly=Microsoft.Crm.UnifiedServiceDesk.Dynamics" 
  xmlns:usdPanelLayouts="clr-namespace:Microsoft.Crm.UnifiedServiceDesk.Dynamics.PanelLayouts;assembly=Microsoft.Crm.UnifiedServiceDesk.Dynamics" 
  xmlns:themes="clr-namespace:Microsoft.Windows.Themes;assembly=PresentationFramework.Luna" 
  xmlns:control="clr-namespace:Microsoft.Crm.UnifiedServiceDesk.Dynamics.Controls;assembly=Microsoft.Crm.UnifiedServiceDesk.Dynamics"> 
  
    <Style x:Key="ToolBarMainPanelBorderStyle" TargetType="{x:Type Border}"> 
          <Setter Property="Margin" Value="0,0,0,0"/> 
          <Setter Property="CornerRadius" Value="3,3,3,3"/> 
          <Setter Property="KeyboardNavigation.TabNavigation" Value="Continue"/> 
          <Style.Triggers> 
              <DataTrigger Binding="{Binding Source={x:Static SystemParameters.HighContrast}}" Value="true"> 
                  <Setter Property="CornerRadius" Value="0,0,0,0"/> 
              </DataTrigger> 
          </Style.Triggers> 
      </Style> 
  
  <Style x:Key="ToolBarThumbStyle" TargetType="{x:Type Thumb}"> 
          <Setter Property="Template"> 
              <Setter.Value> 
                  <ControlTemplate TargetType="{x:Type Thumb}"> 
                      <Border Background="Transparent" Padding="{TemplateBinding Padding}" SnapsToDevicePixels="True"> 
                          <Rectangle> 
                              <Rectangle.Fill> 
                                  <DrawingBrush TileMode="Tile" Viewbox="0,0,4,4" Viewport="0,0,4,4" ViewportUnits="Absolute" ViewboxUnits="Absolute"> 
                                      <DrawingBrush.Drawing> 
                                          <DrawingGroup> 
                                              <GeometryDrawing Brush="White" Geometry="M 1 1 L 1 3 L 3 3 L 3 1 z"/> 
                                              <GeometryDrawing Brush="{DynamicResource ToolBarGripper}" Geometry="M 0 0 L 0 2 L 2 2 L 2 0 z"/> 
                                          </DrawingGroup> 
                                      </DrawingBrush.Drawing> 
                                  </DrawingBrush> 
                              </Rectangle.Fill> 
                          </Rectangle> 
                      </Border> 
                      <ControlTemplate.Triggers> 
                          <Trigger Property="IsMouseOver" Value="true"> 
                              <Setter Property="Cursor" Value="SizeAll"/> 
                          </Trigger> 
                      </ControlTemplate.Triggers> 
                  </ControlTemplate> 
              </Setter.Value> 
          </Setter> 
      </Style> 
  
  <Style x:Key="ToolBarHorizontalOverflowButtonStyle" TargetType="{x:Type ToggleButton}"> 
  <Setter Property="Background" Value="Transparent"/> 
  <Setter Property="MinHeight" Value="0"/> 
  <Setter Property="MinWidth" Value="0"/> 
  <Setter Property="KeyboardNavigation.TabNavigation" Value="Continue"/> 
  <Setter Property="Template"> 
  <Setter.Value> 
  <ControlTemplate TargetType="{x:Type ToggleButton}"> 
  <Border x:Name="Bd" Background="Transparent" CornerRadius="0" SnapsToDevicePixels="true"> 
  <Image Source="{DynamicResource ImageMoreToolBarButtons}" Margin="7,5,7,5" Width="16" Height="16" VerticalAlignment="Bottom" HorizontalAlignment="Right" 
    AutomationProperties.Name="More Menu"></Image> 
  </Border> 
  <ControlTemplate.Triggers> 
  <Trigger Property="IsMouseOver" Value="true"> 
  <Setter Property="Background" TargetName="Bd" Value="{DynamicResource USDTabBackgroundBrush}"/> 
  </Trigger> 
  <Trigger Property="IsKeyboardFocused" Value="true"> 
  <Setter Property="Background" TargetName="Bd" Value="{DynamicResource USDTabBackgroundBrush}"/> 
  <Setter Property="KeyboardNavigation.TabNavigation" Value="Continue"/> 
  </Trigger> 
  <Trigger Property="IsEnabled" Value="false"> 
  <Setter Property="Foreground" Value="{DynamicResource ToolBarGripper}"/> 
  </Trigger> 
  </ControlTemplate.Triggers> 
  </ControlTemplate> 
  </Setter.Value> 
  </Setter> 
  <Style.Triggers> 
  <DataTrigger Binding="{Binding Source={x:Static SystemParameters.HighContrast}}" Value="true"> 
  <Setter Property="Background" Value="Transparent"/> 
  </DataTrigger> 
  </Style.Triggers> 
  </Style> 
  
  <Style x:Key="MainToolBarFocusVisual"> 
      <Setter Property="Control.Template"> 
        <Setter.Value> 
          <ControlTemplate> 
            <Rectangle SnapsToDevicePixels="true" Stroke="White" 
                    StrokeDashArray="1 2" StrokeThickness="1"/> 
          </ControlTemplate> 
        </Setter.Value> 
      </Setter> 
    </Style> 
  
  
  <Style x:Key="ToolBarVerticalOverflowButtonStyle" TargetType="{x:Type ToggleButton}"> 
  <Setter Property="Background" Value="{DynamicResource NormalBrush}"/> 
  <Setter Property="MinHeight" Value="0"/> 
  <Setter Property="MinWidth" Value="0"/> 
  <Setter Property="KeyboardNavigation.TabNavigation" Value="Continue"/> 
  <Setter Property="KeyboardNavigation.DirectionalNavigation" Value="Continue"/> 
  <Setter Property="Template"> 
  <Setter.Value> 
  <ControlTemplate TargetType="{x:Type ToggleButton}"> 
  <Border x:Name="Bd" Background="Transparent" CornerRadius="0" SnapsToDevicePixels="true"> 
  <Image Source="{DynamicResource ImageMoreToolBarButtons}" Margin="7,5,7,5" Width="16" Height="16" VerticalAlignment="Bottom" HorizontalAlignment="Right" 
    AutomationProperties.Name="More Menu"></Image> 
  </Border> 
  <ControlTemplate.Triggers> 
  <Trigger Property="IsMouseOver" Value="true"> 
  <Setter Property="Background" TargetName="Bd" Value="{DynamicResource USDTabBackgroundBrush}"/> 
  </Trigger> 
  <Trigger Property="IsKeyboardFocused" Value="true"> 
  <Setter Property="Background" TargetName="Bd" Value="{DynamicResource USDTabBackgroundBrush}"/> 
  <Setter Property="KeyboardNavigation.TabNavigation" Value="Continue"/> 
  </Trigger> 
  <Trigger Property="IsEnabled" Value="false"> 
  <Setter Property="Foreground" Value="{DynamicResource ToolBarGripper}"/> 
  </Trigger> 
  </ControlTemplate.Triggers> 
  </ControlTemplate> 
  </Setter.Value> 
  </Setter> 
  <Style.Triggers> 
  <DataTrigger Binding="{Binding Source={x:Static SystemParameters.HighContrast}}" Value="true"> 
  <Setter Property="Background" Value="Transparent"/> 
  </DataTrigger> 
  </Style.Triggers> 
  </Style> 
  
  <Style TargetType="{x:Type ToolBar}"> 
  <Setter Property="Background" Value="Transparent"/> 
  <Setter Property="KeyboardNavigation.TabNavigation" Value="Local"/> 
  <Setter Property="KeyboardNavigation.DirectionalNavigation" Value="Continue"/> 
  <Setter Property="Template"> 
  <Setter.Value> 
  <ControlTemplate TargetType="{x:Type ToolBar}"> 
  <Grid x:Name="Grid" Margin="0,0,0,0" SnapsToDevicePixels="true" Height="42"> 
  <Grid x:Name="OverflowGrid" HorizontalAlignment="Right" Margin="0,0,-11,0"> 
  <ToggleButton x:Name="OverflowButton" ClickMode="Press" FocusVisualStyle="{x:Null}" IsChecked="{Binding IsOverflowOpen, Mode=TwoWay, RelativeSource={RelativeSource TemplatedParent}}"  
    IsEnabled="{TemplateBinding HasOverflowItems}" Style="{StaticResource ToolBarHorizontalOverflowButtonStyle}" Visibility="Collapsed" 
    Margin="0,0,0,5"> 
  </ToggleButton> 
  <Popup x:Name="OverflowPopup" AllowsTransparency="true" Focusable="True" IsOpen="{Binding IsOverflowOpen, RelativeSource={RelativeSource TemplatedParent}}" PopupAnimation="{DynamicResource {x:Static SystemParameters.ComboBoxPopupAnimationKey}}" Placement="Bottom" StaysOpen="false"> 
  <themes:SystemDropShadowChrome x:Name="Shdw" Color="Transparent"> 
  <Border x:Name="ToolBarSubMenuBorder" BorderBrush="{DynamicResource ToolBarMenuBorder}" BorderThickness="1" Background="{DynamicResource ToolBarSubMenuBackground}" RenderOptions.ClearTypeHint="Enabled"> 
  <ToolBarOverflowPanel x:Name="PART_ToolBarOverflowPanel" KeyboardNavigation.DirectionalNavigation="Continue" FocusVisualStyle="{x:Null}" Focusable="true" SnapsToDevicePixels="{TemplateBinding SnapsToDevicePixels}" KeyboardNavigation.TabNavigation="Cycle" WrapWidth="200"/> 
  </Border> 
  </themes:SystemDropShadowChrome> 
  </Popup> 
  </Grid> 
  <Border x:Name="MainPanelBorder" BorderBrush="{TemplateBinding BorderBrush}" BorderThickness="{TemplateBinding BorderThickness}" Background="{TemplateBinding Background}" Padding="{TemplateBinding Padding}" Style="{StaticResource ToolBarMainPanelBorderStyle}"> 
  <DockPanel KeyboardNavigation.TabIndex="1" KeyboardNavigation.TabNavigation="Local"> 
  <Thumb x:Name="ToolBarThumb" Margin="-3,-1,0,0" Padding="6,5,1,6" Style="{StaticResource ToolBarThumbStyle}"/> 
  <ContentPresenter x:Name="ToolBarHeader" ContentSource="Header" HorizontalAlignment="Center" Margin="4,0,4,0" SnapsToDevicePixels="{TemplateBinding SnapsToDevicePixels}" VerticalAlignment="Center"/> 
  <ToolBarPanel x:Name="PART_ToolBarPanel" IsItemsHost="true" Margin="0" SnapsToDevicePixels="{TemplateBinding SnapsToDevicePixels}"/> 
  </DockPanel> 
  </Border> 
  </Grid> 
  <ControlTemplate.Triggers> 
  <Trigger Property="HasOverflowItems" Value="true"> 
  <Setter Property="Visibility" TargetName="OverflowButton" Value="Visible"/> 
  </Trigger> 
  <Trigger Property="IsOverflowOpen" Value="true"> 
  <Setter Property="IsEnabled" TargetName="ToolBarThumb" Value="false"/> 
  </Trigger> 
  <Trigger Property="Header" Value="{x:Null}"> 
  <Setter Property="Visibility" TargetName="ToolBarHeader" Value="Collapsed"/> 
  </Trigger> 
  <Trigger Property="ToolBarTray.IsLocked" Value="true"> 
  <Setter Property="Visibility" TargetName="ToolBarThumb" Value="Collapsed"/> 
  </Trigger> 
  <Trigger Property="HasDropShadow" SourceName="OverflowPopup" Value="true"> 
  <Setter Property="Margin" TargetName="Shdw" Value="0,0,5,5"/> 
  <Setter Property="SnapsToDevicePixels" TargetName="Shdw" Value="true"/> 
  <Setter Property="Color" TargetName="Shdw" Value="#71000000"/> 
  </Trigger> 
  <Trigger Property="Orientation" Value="Vertical"> 
  <Setter Property="Margin" TargetName="Grid" Value="1,3,1,1"/> 
  <Setter Property="Style" TargetName="OverflowButton" Value="{StaticResource ToolBarVerticalOverflowButtonStyle}"/> 
  <Setter Property="Height" TargetName="ToolBarThumb" Value="10"/> 
  <Setter Property="Width" TargetName="ToolBarThumb" Value="Auto"/> 
  <Setter Property="Margin" TargetName="ToolBarThumb" Value="-1,-3,0,0"/> 
  <Setter Property="Padding" TargetName="ToolBarThumb" Value="5,6,6,1"/> 
  <Setter Property="Margin" TargetName="ToolBarHeader" Value="0,0,0,4"/> 
  <Setter Property="Margin" TargetName="PART_ToolBarPanel" Value="1,0,2,2"/> 
  <Setter Property="DockPanel.Dock" TargetName="ToolBarThumb" Value="Top"/> 
  <Setter Property="DockPanel.Dock" TargetName="ToolBarHeader" Value="Top"/> 
  <Setter Property="HorizontalAlignment" TargetName="OverflowGrid" Value="Stretch"/> 
  <Setter Property="VerticalAlignment" TargetName="OverflowGrid" Value="Bottom"/> 
  <Setter Property="Placement" TargetName="OverflowPopup" Value="Right"/> 
  <Setter Property="Margin" TargetName="MainPanelBorder" Value="0,0,0,11"/> 
  <Setter Property="Background" Value="Transparent"/> 
  <Setter Property="KeyboardNavigation.TabNavigation" Value="Local"/> 
  <Setter Property="KeyboardNavigation.DirectionalNavigation" Value="Continue"/> 
  </Trigger> 
  <Trigger Property="IsEnabled" Value="false"> 
  <Setter Property="Foreground" Value="{DynamicResource {x:Static SystemColors.GrayTextBrushKey}}"/> 
  </Trigger> 
  </ControlTemplate.Triggers> 
  </ControlTemplate> 
  </Setter.Value> 
  </Setter> 
  <Style.Triggers> 
  <DataTrigger Binding="{Binding Source={x:Static SystemParameters.HighContrast}}" Value="true"> 
  <Setter Property="Background" Value="Transparent"/> 
  </DataTrigger> 
  </Style.Triggers> 
  </Style> 
  
  <Style x:Key="ToolBarButtonBaseStyle"> 
  <Setter Property="Control.BorderThickness" Value="0"/> 
  <Setter Property="Control.Padding" Value="0"/> 
  <Setter Property="Control.Background" Value="Transparent"/> 
  <Setter Property="Control.BorderBrush" Value="Transparent"/> 
  <Setter Property="Control.Foreground" Value="{DynamicResource ToolBarFontColor}"/> 
  <Setter Property="Control.FontFamily" Value="Segoe UI"/> 
  <Setter Property="Control.FontSize" Value="12"/> 
  </Style> 
  <Style x:Key="ToolbarButtonTemplate" TargetType="{x:Type control:ToolbarButton}" BasedOn="{StaticResource ToolBarButtonBaseStyle}"> 
          <Setter Property="HorizontalContentAlignment" Value="Center"/> 
          <Setter Property="VerticalContentAlignment" Value="Center"/> 
          <Setter Property="VerticalAlignment" Value="Center"/> 
          <Setter Property="FontFamily" Value="Segoe UI"/> 
          <Setter Property="FontSize" Value="14"/> 
          <Setter Property="FocusVisualStyle" Value="{DynamicResource MainToolBarFocusVisual}" /> 
          <Setter Property="Template"> 
              <Setter.Value> 
                  <ControlTemplate TargetType="{x:Type control:ToolbarButton}"> 
                      <Border x:Name="Bd" Height="42"  BorderBrush="{TemplateBinding BorderBrush}" BorderThickness="{TemplateBinding BorderThickness}" Background="{TemplateBinding Background}" Padding="{TemplateBinding Padding}" SnapsToDevicePixels="true"> 
                          <StackPanel x:Name="AboutToolBarButtonStackPanel"  Orientation="Horizontal" Margin="7,0,7,0"> 
                              <Image Margin="0,0,7,0" x:Name="Icon" VerticalAlignment="Center" MaxWidth="16" MaxHeight="16" Source="{TemplateBinding Image}"/> 
                              <ContentPresenter Margin="0,7,0,7"  HorizontalAlignment="{TemplateBinding HorizontalContentAlignment}" SnapsToDevicePixels="{TemplateBinding SnapsToDevicePixels}" VerticalAlignment="{TemplateBinding VerticalContentAlignment}"/> 
                          </StackPanel> 
                      </Border> 
                      <ControlTemplate.Triggers> 
                          <Trigger Property="Text" Value="{x:Null}"> 
                              <Setter TargetName="Icon" Property="Margin" Value="0,0,0,0"/> 
                              <Setter TargetName="AboutToolBarButtonStackPanel" Property="Margin" Value="13,0,13,0"/> 
                          </Trigger> 
                          <Trigger Property="Image" Value="{x:Null}"> 
                              <Setter TargetName="Icon" Property="Visibility" Value="Collapsed"/> 
                          </Trigger> 
                          <Trigger Property="IsMouseOver" Value="true"> 
                              <Setter Property="Background" TargetName="Bd" Value="{DynamicResource ToolBarButtonHover}"/> 
                              <Setter Property="Foreground" Value="{DynamicResource ToolBarTextFontHighlightColor}"/> 
                          </Trigger> 
                          <Trigger Property="IsKeyboardFocused" Value="true"> 
                              <Setter Property="Background" TargetName="Bd" Value="{DynamicResource ToolBarButtonHover}"/> 
                              <Setter Property="Foreground" Value="{DynamicResource ToolBarTextFontHighlightColor}"/> 
                          </Trigger> 
                          <Trigger Property="IsEnabled" Value="false"> 
                              <Setter Property="Foreground" Value="{DynamicResource {x:Static SystemColors.GrayTextBrushKey}}"/> 
                          </Trigger> 
                      </ControlTemplate.Triggers> 
                  </ControlTemplate> 
              </Setter.Value> 
          </Setter> 
      </Style> 
        <Style x:Key="ToolBarSplitButtonStyle" TargetType="{x:Type control:SplitButton}" BasedOn="{StaticResource ToolBarButtonBaseStyle}" > 
      <Setter Property="HorizontalAlignment" Value="Stretch"/> 
      <Setter Property="VerticalAlignment" Value="Stretch"/> 
      <Setter Property="HorizontalContentAlignment" Value="Stretch"/> 
      <Setter Property="VerticalContentAlignment" Value="Center"/> 
      <Setter Property="Height" Value="42"/> 
        <Setter Property="FocusVisualStyle" Value="{DynamicResource MainToolBarFocusVisual}"/> 
      <Setter Property="Template"> 
        <Setter.Value> 
          <ControlTemplate TargetType="{x:Type control:SplitButton}"> 
            <Border SnapsToDevicePixels="True" Background="{TemplateBinding Background}" BorderBrush="{TemplateBinding BorderBrush}" BorderThickness="{TemplateBinding BorderThickness}"> 
              <StackPanel Orientation="Horizontal" Margin="0,0,0,0"> 
                <Button x:Name="PART_Button"  Margin="0,0,0,0" Style="{DynamicResource ButtonStyle}" AutomationProperties.Name="{Binding Path=(AutomationProperties.Name), RelativeSource={RelativeSource Mode=FindAncestor, AncestorType={x:Type control:SplitButton}}}" FocusVisualStyle="{DynamicResource MainToolBarFocusVisual}" > 
                  <StackPanel Orientation="Horizontal"> 
                    <Image x:Name="Icon"  Margin="7,0,7,0" VerticalAlignment="Center" MaxWidth="16" MaxHeight="16" Source="{TemplateBinding Image}"/> 
                    <ContentPresenter x:Name="ToolBarSplitButtonContent" Margin="0,7,7,7" HorizontalAlignment="{TemplateBinding HorizontalContentAlignment}" SnapsToDevicePixels="{TemplateBinding SnapsToDevicePixels}" VerticalAlignment="{TemplateBinding VerticalContentAlignment}"/> 
                  </StackPanel> 
                </Button> 
                <Separator Style="{DynamicResource VerticalSeparatorStyle}" Height="1" Width="16" Background="{DynamicResource SeparatorBrush}" Margin="0,0,0,0"/> 
                <Border x:Name="SplitDropDown"> 
                  <Path x:Name="DownArrow" Style="{DynamicResource DownArrowGeometryStyle}" Margin="4,4,4,0"/> 
                </Border> 
              </StackPanel> 
            </Border> 
            <ControlTemplate.Triggers> 
              <Trigger Property="Image" Value="{x:Null}"> 
                <Setter TargetName="Icon" Property="Visibility" Value="Collapsed"/> 
                <Setter TargetName="ToolBarSplitButtonContent" Property="Margin" Value="7,7,7,7"/> 
              </Trigger> 
              <Trigger Property="Text" Value="{x:Null}"> 
                <Setter TargetName="ToolBarSplitButtonContent" Property="Margin" Value="0,0,0,0"/> 
              </Trigger> 
              <Trigger SourceName="PART_Button" Property="IsMouseOver" Value="True"> 
                <Setter Property="Background" Value="Transparent" TargetName="SplitDropDown"/> 
                <Setter Property="Background" Value="{DynamicResource ToolBarButtonHover}" TargetName="PART_Button"/> 
              </Trigger> 
              <Trigger SourceName="PART_Button" Property="IsKeyboardFocused" Value="True"> 
                <Setter Property="Background" Value="{DynamicResource ToolBarButtonHover}" TargetName="PART_Button"/> 
              </Trigger> 
              <Trigger SourceName="SplitDropDown" Property="IsMouseOver" Value="True"> 
                <Setter Property="Background" Value="{DynamicResource ToolBarButtonHover}" TargetName="SplitDropDown"/> 
                <Setter Property="Background" Value="Transparent" TargetName="PART_Button"/> 
              </Trigger> 
              <Trigger Property="IsChecked" Value="True"> 
                <Setter Property="Background" Value="{DynamicResource ToolBarButtonHover}"/> 
              </Trigger> 
              <Trigger Property="IsKeyboardFocused" Value="True"> 
                <Setter Property="Background" Value="{DynamicResource ToolBarButtonHover}"/> 
              </Trigger> 
              <MultiTrigger> 
                <MultiTrigger.Conditions> 
                  <Condition Property="IsMouseOver" Value="True"/> 
                  <Condition Property="IsChecked" Value="True"/> 
                </MultiTrigger.Conditions> 
                <Setter Property="Background" Value="{DynamicResource ToolBarButtonHover}"/> 
              </MultiTrigger> 
              <MultiTrigger> 
                <MultiTrigger.Conditions> 
                  <Condition Property="IsKeyboardFocused" Value="True"/> 
                  <Condition Property="IsChecked" Value="True"/> 
                </MultiTrigger.Conditions> 
                <Setter Property="Background" Value="{DynamicResource ToolBarButtonHover}"/> 
              </MultiTrigger> 
              <Trigger Property="IsPressed" Value="True"> 
                <Setter Property="Background" Value="{DynamicResource ToolBarButtonHover}"/> 
              </Trigger> 
              <Trigger Property="IsEnabled" Value="False"> 
                <Setter Property="Foreground" Value="{DynamicResource {x:Static SystemColors.GrayTextBrushKey}}"/> 
              </Trigger> 
            </ControlTemplate.Triggers> 
          </ControlTemplate> 
        </Setter.Value> 
      </Setter> 
    </Style> 
  </ResourceDictionary> 
  ```
  
<span data-ttu-id="44aa7-156">**Sample 2:** The sample XAML that defines defines <xref:System.Windows.ResourceDictionary> of <xref:System.Windows.Style> and <xref:System.Windows.Media.Brush> resources demonstrates customizing the **Main** toolbar.</span><span class="sxs-lookup"><span data-stu-id="44aa7-156">**Sample 2:** The sample XAML that defines defines <xref:System.Windows.ResourceDictionary> of <xref:System.Windows.Style> and <xref:System.Windows.Media.Brush> resources demonstrates customizing the **Main** toolbar.</span></span>

> [!NOTE]
> <span data-ttu-id="44aa7-157">You can find this sample XAML styles in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] - Unified Interface sample package.</span><span class="sxs-lookup"><span data-stu-id="44aa7-157">You can find this sample XAML styles in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] - Unified Interface sample package.</span></span>

  ```XAML
  <ResourceDictionary xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
  xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
  xmlns:usd="clr-namespace:Microsoft.Crm.UnifiedServiceDesk.Dynamics;assembly=Microsoft.Crm.UnifiedServiceDesk.Dynamics"
  xmlns:controlStyles="clr-namespace:Microsoft.Crm.UnifiedServiceDesk.Dynamics.Controls.Styles;assembly=Microsoft.Crm.UnifiedServiceDesk.Dynamics"
  xmlns:usdPanelLayouts="clr-namespace:Microsoft.Crm.UnifiedServiceDesk.Dynamics.PanelLayouts;assembly=Microsoft.Crm.UnifiedServiceDesk.Dynamics"
  xmlns:themes="clr-namespace:Microsoft.Windows.Themes;assembly=PresentationFramework.Luna"
  xmlns:control="clr-namespace:Microsoft.Crm.UnifiedServiceDesk.Dynamics.Controls;assembly=Microsoft.Crm.UnifiedServiceDesk.Dynamics">

    <Style x:Key="ToolBarMainPanelBorderStyle" TargetType="{x:Type Border}">
          <Setter Property="Margin" Value="0,0,0,0"/>
          <Setter Property="CornerRadius" Value="3,3,3,3"/>
          <Setter Property="KeyboardNavigation.TabNavigation" Value="Continue"/>
          <Style.Triggers>
              <DataTrigger Binding="{Binding Source={x:Static SystemParameters.HighContrast}}" Value="true">
                  <Setter Property="CornerRadius" Value="0,0,0,0"/>
              </DataTrigger>
          </Style.Triggers>
      </Style>

  <Style x:Key="ToolBarThumbStyle" TargetType="{x:Type Thumb}">
          <Setter Property="Template">
              <Setter.Value>
                  <ControlTemplate TargetType="{x:Type Thumb}">
                      <Border Background="Transparent" Padding="{TemplateBinding Padding}" SnapsToDevicePixels="True">
                          <Rectangle>
                              <Rectangle.Fill>
                                  <DrawingBrush TileMode="Tile" Viewbox="0,0,4,4" Viewport="0,0,4,4" ViewportUnits="Absolute" ViewboxUnits="Absolute">
                                      <DrawingBrush.Drawing>
                                          <DrawingGroup>
                                              <GeometryDrawing Brush="White" Geometry="M 1 1 L 1 3 L 3 3 L 3 1 z"/>
                                              <GeometryDrawing Brush="{DynamicResource ToolBarGripper}" Geometry="M 0 0 L 0 2 L 2 2 L 2 0 z"/>
                                          </DrawingGroup>
                                      </DrawingBrush.Drawing>
                                  </DrawingBrush>
                              </Rectangle.Fill>
                          </Rectangle>
                      </Border>
                      <ControlTemplate.Triggers>
                          <Trigger Property="IsMouseOver" Value="true">
                              <Setter Property="Cursor" Value="SizeAll"/>
                          </Trigger>
                      </ControlTemplate.Triggers>
                  </ControlTemplate>
              </Setter.Value>
          </Setter>
      </Style>

  <Style x:Key="ToolBarHorizontalOverflowButtonStyle" TargetType="{x:Type ToggleButton}">
          <Setter Property="Background" Value="Transparent"/>
          <Setter Property="MinHeight" Value="0"/>
          <Setter Property="MinWidth" Value="0"/>
          <Setter Property="KeyboardNavigation.TabNavigation" Value="Continue"/>
          <Setter Property="Template">
              <Setter.Value>
                  <ControlTemplate TargetType="{x:Type ToggleButton}">
                      <Border x:Name="Bd" Background="Transparent" CornerRadius="0" SnapsToDevicePixels="true">
                          <Image Source="{DynamicResource ImageMoreToolBarButtons}" Margin="7,5,7,5" Width="16" Height="16" VerticalAlignment="Bottom" HorizontalAlignment="Right"
                                    AutomationProperties.Name="More Menu"></Image>
                      </Border>
                      <ControlTemplate.Triggers>
                          <Trigger Property="IsMouseOver" Value="true">
                              <Setter Property="Background" TargetName="Bd" Value="{DynamicResource USDTabBackgroundBrush}"/>
                          </Trigger>
                          <Trigger Property="IsKeyboardFocused" Value="true">
                              <Setter Property="Background" TargetName="Bd" Value="{DynamicResource USDTabBackgroundBrush}"/>
                              <Setter Property="KeyboardNavigation.TabNavigation" Value="Continue"/>
                          </Trigger>
                          <Trigger Property="IsEnabled" Value="false">
                              <Setter Property="Foreground" Value="{DynamicResource ToolBarGripper}"/>
                          </Trigger>
                      </ControlTemplate.Triggers>
                  </ControlTemplate>
              </Setter.Value>
          </Setter>
          <Style.Triggers>
              <DataTrigger Binding="{Binding Source={x:Static SystemParameters.HighContrast}}" Value="true">
                  <Setter Property="Background" Value="Transparent"/>
              </DataTrigger>
          </Style.Triggers>
      </Style>


      <Style x:Key="ToolBarVerticalOverflowButtonStyle" TargetType="{x:Type ToggleButton}">
          <Setter Property="Background" Value="{DynamicResource NormalBrush}"/>
          <Setter Property="MinHeight" Value="0"/>
          <Setter Property="MinWidth" Value="0"/>
          <Setter Property="KeyboardNavigation.TabNavigation" Value="Continue"/>
          <Setter Property="KeyboardNavigation.DirectionalNavigation" Value="Continue"/>
          <Setter Property="Template">
              <Setter.Value>
                  <ControlTemplate TargetType="{x:Type ToggleButton}">
                      <Border x:Name="Bd" Background="Transparent" CornerRadius="0" SnapsToDevicePixels="true">
                          <Image Source="{DynamicResource ImageMoreToolBarButtons}" Margin="7,5,7,5" Width="16" Height="16" VerticalAlignment="Bottom" HorizontalAlignment="Right"
                                    AutomationProperties.Name="More Menu"></Image>
                      </Border>
                      <ControlTemplate.Triggers>
                          <Trigger Property="IsMouseOver" Value="true">
                              <Setter Property="Background" TargetName="Bd" Value="{DynamicResource USDTabBackgroundBrush}"/>
                          </Trigger>
                          <Trigger Property="IsKeyboardFocused" Value="true">
                              <Setter Property="Background" TargetName="Bd" Value="{DynamicResource USDTabBackgroundBrush}"/>
                              <Setter Property="KeyboardNavigation.TabNavigation" Value="Continue"/>
                          </Trigger>
                          <Trigger Property="IsEnabled" Value="false">
                              <Setter Property="Foreground" Value="{DynamicResource ToolBarGripper}"/>
                          </Trigger>
                      </ControlTemplate.Triggers>
                  </ControlTemplate>
              </Setter.Value>
          </Setter>
          <Style.Triggers>
              <DataTrigger Binding="{Binding Source={x:Static SystemParameters.HighContrast}}" Value="true">
                  <Setter Property="Background" Value="Transparent"/>
              </DataTrigger>
          </Style.Triggers>
      </Style>

  <Style TargetType="{x:Type ToolBar}">
          <Setter Property="Background" Value="Transparent"/>
          <Setter Property="KeyboardNavigation.TabNavigation" Value="Local"/>
          <Setter Property="KeyboardNavigation.DirectionalNavigation" Value="Continue"/>
          <Setter Property="Template">
              <Setter.Value>
                  <ControlTemplate TargetType="{x:Type ToolBar}">
                      <Grid x:Name="Grid" Margin="0,0,0,0" SnapsToDevicePixels="true" Height="42">
                          <Grid x:Name="OverflowGrid" HorizontalAlignment="Right" Margin="0,0,-11,0">
                              <ToggleButton x:Name="OverflowButton" ClickMode="Press" FocusVisualStyle="{x:Null}" IsChecked="{Binding IsOverflowOpen, Mode=TwoWay, RelativeSource={RelativeSource TemplatedParent}}" 
                                            IsEnabled="{TemplateBinding HasOverflowItems}" Style="{StaticResource ToolBarHorizontalOverflowButtonStyle}" Visibility="Collapsed"
                                            Margin="0,0,0,5">
                              </ToggleButton>
                              <Popup x:Name="OverflowPopup" AllowsTransparency="true" Focusable="True" IsOpen="{Binding IsOverflowOpen, RelativeSource={RelativeSource TemplatedParent}}" PopupAnimation="{DynamicResource {x:Static SystemParameters.ComboBoxPopupAnimationKey}}" Placement="Bottom" StaysOpen="false">
                                  <themes:SystemDropShadowChrome x:Name="Shdw" Color="Transparent">
                                      <Border x:Name="ToolBarSubMenuBorder" BorderBrush="{DynamicResource ToolBarMenuBorder}" BorderThickness="1" Background="{DynamicResource ToolBarSubMenuBackground}" RenderOptions.ClearTypeHint="Enabled">
                                          <ToolBarOverflowPanel x:Name="PART_ToolBarOverflowPanel" KeyboardNavigation.DirectionalNavigation="Continue" FocusVisualStyle="{x:Null}" Focusable="true" SnapsToDevicePixels="{TemplateBinding SnapsToDevicePixels}" KeyboardNavigation.TabNavigation="Cycle" WrapWidth="200"/>
                                      </Border>
                                  </themes:SystemDropShadowChrome>
                              </Popup>
                          </Grid>
                          <Border x:Name="MainPanelBorder" BorderBrush="{TemplateBinding BorderBrush}" BorderThickness="{TemplateBinding BorderThickness}" Background="{TemplateBinding Background}" Padding="{TemplateBinding Padding}" Style="{StaticResource ToolBarMainPanelBorderStyle}">
                              <DockPanel KeyboardNavigation.TabIndex="1" KeyboardNavigation.TabNavigation="Local">
                                  <Thumb x:Name="ToolBarThumb" Margin="-3,-1,0,0" Padding="6,5,1,6" Style="{StaticResource ToolBarThumbStyle}"/>
                                  <ContentPresenter x:Name="ToolBarHeader" ContentSource="Header" HorizontalAlignment="Center" Margin="4,0,4,0" SnapsToDevicePixels="{TemplateBinding SnapsToDevicePixels}" VerticalAlignment="Center"/>
                                  <ToolBarPanel x:Name="PART_ToolBarPanel" IsItemsHost="true" Margin="0" SnapsToDevicePixels="{TemplateBinding SnapsToDevicePixels}"/>
                              </DockPanel>
                          </Border>
                      </Grid>
                      <ControlTemplate.Triggers>
                          <Trigger Property="HasOverflowItems" Value="true">
                              <Setter Property="Visibility" TargetName="OverflowButton" Value="Visible"/>
                          </Trigger>
                          <Trigger Property="IsOverflowOpen" Value="true">
                              <Setter Property="IsEnabled" TargetName="ToolBarThumb" Value="false"/>
                          </Trigger>
                          <Trigger Property="Header" Value="{x:Null}">
                              <Setter Property="Visibility" TargetName="ToolBarHeader" Value="Collapsed"/>
                          </Trigger>
                          <Trigger Property="ToolBarTray.IsLocked" Value="true">
                              <Setter Property="Visibility" TargetName="ToolBarThumb" Value="Collapsed"/>
                          </Trigger>
                          <Trigger Property="HasDropShadow" SourceName="OverflowPopup" Value="true">
                              <Setter Property="Margin" TargetName="Shdw" Value="0,0,5,5"/>
                              <Setter Property="SnapsToDevicePixels" TargetName="Shdw" Value="true"/>
                              <Setter Property="Color" TargetName="Shdw" Value="#71000000"/>
                          </Trigger>
                          <Trigger Property="Orientation" Value="Vertical">
                              <Setter Property="Margin" TargetName="Grid" Value="1,3,1,1"/>
                              <Setter Property="Style" TargetName="OverflowButton" Value="{StaticResource ToolBarVerticalOverflowButtonStyle}"/>
                              <Setter Property="Height" TargetName="ToolBarThumb" Value="10"/>
                              <Setter Property="Width" TargetName="ToolBarThumb" Value="Auto"/>
                              <Setter Property="Margin" TargetName="ToolBarThumb" Value="-1,-3,0,0"/>
                              <Setter Property="Padding" TargetName="ToolBarThumb" Value="5,6,6,1"/>
                              <Setter Property="Margin" TargetName="ToolBarHeader" Value="0,0,0,4"/>
                              <Setter Property="Margin" TargetName="PART_ToolBarPanel" Value="1,0,2,2"/>
                              <Setter Property="DockPanel.Dock" TargetName="ToolBarThumb" Value="Top"/>
                              <Setter Property="DockPanel.Dock" TargetName="ToolBarHeader" Value="Top"/>
                              <Setter Property="HorizontalAlignment" TargetName="OverflowGrid" Value="Stretch"/>
                              <Setter Property="VerticalAlignment" TargetName="OverflowGrid" Value="Bottom"/>
                              <Setter Property="Placement" TargetName="OverflowPopup" Value="Right"/>
                              <Setter Property="Margin" TargetName="MainPanelBorder" Value="0,0,0,11"/>
                              <Setter Property="Background" Value="Transparent"/>
                              <Setter Property="KeyboardNavigation.TabNavigation" Value="Local"/>
                              <Setter Property="KeyboardNavigation.DirectionalNavigation" Value="Continue"/>
                          </Trigger>
                          <Trigger Property="IsEnabled" Value="false">
                              <Setter Property="Foreground" Value="{DynamicResource {x:Static SystemColors.GrayTextBrushKey}}"/>
                          </Trigger>
                      </ControlTemplate.Triggers>
                  </ControlTemplate>
              </Setter.Value>
          </Setter>
          <Style.Triggers>
              <DataTrigger Binding="{Binding Source={x:Static SystemParameters.HighContrast}}" Value="true">
                  <Setter Property="Background" Value="Transparent"/>
              </DataTrigger>
          </Style.Triggers>
      </Style>

  <Style x:Key="ToolBarButtonBaseStyle">
          <Setter Property="Control.BorderThickness" Value="0"/>
          <Setter Property="Control.Padding" Value="0"/>
          <Setter Property="Control.Background" Value="Transparent"/>
          <Setter Property="Control.BorderBrush" Value="Transparent"/>
          <Setter Property="Control.Foreground" Value="{DynamicResource ToolBarFontColor}"/>
          <Setter Property="Control.FontFamily" Value="Segoe UI"/>
          <Setter Property="Control.FontSize" Value="12"/>
      </Style>

  <Style x:Key="MainToolBarFocusVisual">
      <Setter Property="Control.Template">
        <Setter.Value>
          <ControlTemplate>
            <Rectangle SnapsToDevicePixels="true" Stroke="White"
                    StrokeDashArray="1 2" StrokeThickness="1"/>
          </ControlTemplate>
        </Setter.Value>
      </Setter>
    </Style>

  <Style x:Key="ToolbarButtonTemplate" TargetType="{x:Type control:ToolbarButton}" BasedOn="{StaticResource ToolBarButtonBaseStyle}">
          <Setter Property="HorizontalContentAlignment" Value="Center"/>
          <Setter Property="VerticalContentAlignment" Value="Center"/>
          <Setter Property="VerticalAlignment" Value="Center"/>
          <Setter Property="FontFamily" Value="Segoe UI"/>
          <Setter Property="FontSize" Value="14"/>
          <Setter Property="FocusVisualStyle" Value="{DynamicResource MainToolBarFocusVisual}"/>
          <Setter Property="Template">
              <Setter.Value>
                  <ControlTemplate TargetType="{x:Type control:ToolbarButton}">
                      <Border x:Name="Bd" Height="42"  BorderBrush="{TemplateBinding BorderBrush}" BorderThickness="{TemplateBinding BorderThickness}" Background="{TemplateBinding Background}" Padding="{TemplateBinding Padding}" SnapsToDevicePixels="true">
                          <StackPanel x:Name="ToolBarButtonStackPanel"  Orientation="Horizontal" Margin="14,0,14,0">
                              <Image Margin="0,0,7,0" x:Name="Icon" VerticalAlignment="Center" MaxWidth="16" MaxHeight="16" Source="{TemplateBinding Image}"/>
                              <ContentPresenter x:Name="ToolBarButtonContentPresenter" Margin="0,7,0,7" HorizontalAlignment="{TemplateBinding HorizontalContentAlignment}" SnapsToDevicePixels="{TemplateBinding SnapsToDevicePixels}" VerticalAlignment="{TemplateBinding VerticalContentAlignment}"/>
                          </StackPanel>
                      </Border>
                      <ControlTemplate.Triggers>
                          <Trigger Property="Text" Value="{x:Null}">
                              <Setter TargetName="Icon" Property="Margin" Value="0,0,0,0"/>
                          </Trigger>
                          <Trigger Property="Image" Value="{x:Null}">
                              <Setter TargetName="Icon" Property="Visibility" Value="Collapsed"/>
                          </Trigger>
                          <Trigger Property="IsMouseOver" Value="true">
                              <Setter Property="Background" TargetName="Bd" Value="{DynamicResource ToolBarButtonHover}"/>
                              <Setter Property="Foreground" Value="{DynamicResource ToolBarTextFontHighlightColor}"/>
                          </Trigger>
                          <Trigger Property="IsKeyboardFocused" Value="true">
                              <Setter Property="Background" TargetName="Bd" Value="{DynamicResource ToolBarButtonHover}"/>
                              <Setter Property="Foreground" Value="{DynamicResource ToolBarTextFontHighlightColor}"/>
                          </Trigger>
                          <Trigger Property="IsPressed" Value="true">
                              <Setter Property="Background" TargetName="Bd" Value="{DynamicResource ToolBarButtonPressed}"/>
                              <Setter Property="Foreground" Value="{DynamicResource ToolBarButtonHover}"/>
                          </Trigger>
                          <Trigger Property="IsEnabled" Value="false">
                              <Setter Property="Foreground" Value="{DynamicResource {x:Static SystemColors.GrayTextBrushKey}}"/>
                          </Trigger>
                      </ControlTemplate.Triggers>
                  </ControlTemplate>
              </Setter.Value>
          </Setter>
      </Style>
  <Style x:Key="ToolBarDropDownButtonStyle" TargetType="{x:Type control:DropDownButton}" BasedOn="{StaticResource ToolBarButtonBaseStyle}">
          <Setter Property="HorizontalAlignment" Value="Stretch"/>
          <Setter Property="VerticalAlignment" Value="Stretch"/>
          <Setter Property="HorizontalContentAlignment" Value="Stretch"/>
          <Setter Property="VerticalContentAlignment" Value="Center"/>
          <Setter Property="FontFamily" Value="Segoe UI"/>
          <Setter Property="FontSize" Value="14"/>
          <Setter Property="FocusVisualStyle" Value="{DynamicResource MainToolBarFocusVisual}"/>
          <Setter Property="Template">
              <Setter.Value>
                  <ControlTemplate TargetType="{x:Type control:DropDownButton}">
                      <Border SnapsToDevicePixels="True" Background="{TemplateBinding Background}" BorderBrush="{TemplateBinding BorderBrush}" BorderThickness="{TemplateBinding BorderThickness}">
                          <!--<Label>-->
                          <StackPanel Orientation="Horizontal" Margin="14,0,14,0">
                              <Image Margin="0,0,7,0" x:Name="Icon" VerticalAlignment="Center" Width="16" Height="16" Source="{TemplateBinding Image}"/>
                              <ContentPresenter Margin="{TemplateBinding Margin}" HorizontalAlignment="{TemplateBinding HorizontalContentAlignment}" SnapsToDevicePixels="{TemplateBinding SnapsToDevicePixels}" VerticalAlignment="{TemplateBinding VerticalContentAlignment}"/>
                              <Path x:Name="DownArrow" Style="{DynamicResource DownArrowGeometryStyle}" Margin="7,4,0,0"/>
                          </StackPanel>
                          <!--</Label>-->
                      </Border>
                      <ControlTemplate.Triggers>
                          <Trigger Property="Text" Value="{x:Null}">
                              <Setter TargetName="Icon" Property="Margin" Value="0,0,0,0"/>
                          </Trigger>
                          <Trigger Property="Image" Value="{x:Null}">
                              <Setter TargetName="Icon" Property="Visibility" Value="Collapsed"/>
                          </Trigger>
                          <Trigger Property="IsChecked" Value="True">
                              <Setter Property="Background" Value="White"/>
                              <Setter Property="Foreground" Value="{DynamicResource ToolBarButtonHover}"/>
                              <Setter TargetName="DownArrow" Property="Stroke" Value="{DynamicResource ToolBarButtonHover}" />
                          </Trigger>
                          <Trigger Property="IsMouseOver" Value="True">
                              <Setter Property="Background" Value="{DynamicResource ToolBarButtonHover}"/>
                              <Setter Property="Foreground" Value="{DynamicResource ToolBarTextFontHighlightColor}"/>
                              <Setter TargetName="DownArrow" Property="Stroke" Value="{DynamicResource ToolBarTextFontHighlightColor}" />
                          </Trigger>
                          <Trigger Property="IsKeyboardFocused" Value="True">
                              <Setter Property="Background" Value="{DynamicResource ToolBarButtonHover}"/>
                              <Setter Property="Foreground" Value="{DynamicResource ToolBarTextFontHighlightColor}"/>
                              <Setter TargetName="DownArrow" Property="Stroke" Value="{DynamicResource ToolBarTextFontHighlightColor}" />
                          </Trigger>

                          <MultiTrigger>
                              <MultiTrigger.Conditions>
                                  <Condition Property="IsMouseOver" Value="True"/>
                                  <Condition Property="IsChecked" Value="True"/>
                              </MultiTrigger.Conditions>
                              <Setter Property="Background" Value="{DynamicResource ToolBarSplitButtonSelectedBrush}"/>
                              <Setter Property="Foreground" Value="{DynamicResource ToolBarTextFontHighlightColor}"/>
                              <Setter TargetName="DownArrow" Property="Stroke" Value="{DynamicResource ToolBarTextFontHighlightColor}" />
                          </MultiTrigger>
                          <MultiTrigger>
                              <MultiTrigger.Conditions>
                                  <Condition Property="IsKeyboardFocused" Value="True"/>
                                  <Condition Property="IsChecked" Value="True"/>
                              </MultiTrigger.Conditions>
                              <Setter Property="Background" Value="White"/>
                              <Setter Property="Foreground" Value="{DynamicResource ToolBarButtonHover}"/>
                              <Setter TargetName="DownArrow" Property="Stroke" Value="{DynamicResource ToolBarButtonHover}" />
                          </MultiTrigger>
                          <Trigger Property="IsPressed" Value="True">
                              <Setter Property="Background" Value="White"/>
                              <Setter Property="Foreground" Value="{DynamicResource ToolBarButtonHover}"/>
                              <Setter TargetName="DownArrow" Property="Stroke" Value="{DynamicResource ToolBarButtonHover}"/>

                          </Trigger>
                          <Trigger Property="IsEnabled" Value="False">
                              <Setter Property="Foreground" Value="{DynamicResource {x:Static SystemColors.GrayTextBrushKey}}"/>
                          </Trigger>
                      </ControlTemplate.Triggers>
                  </ControlTemplate>
              </Setter.Value>
          </Setter>
      </Style>
  </ResourceDictionary>
  ```
  
## <a name="see-also"></a><span data-ttu-id="44aa7-158">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="44aa7-158">See also</span></span>  
 [<span data-ttu-id="44aa7-159">Thanh công cụ trong Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="44aa7-159">Toolbars in Unified Service Desk</span></span>](../unified-service-desk/toolbars-unified-service-desk.md)

 [<span data-ttu-id="44aa7-160">Configure your agent application using Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="44aa7-160">Configure your agent application using Unified Service Desk</span></span>](../unified-service-desk/configure-agent-application-unified-service-desk.md)
