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
# <a name="panels-panel-types-and-panel-layouts-in-unified-service-desk"></a>Panels, panel types, and panel layouts in Unified Service Desk
[!INCLUDE[pn_unified_service_desk_for_crm](../includes/pn-unified-service-desk-for-crm.md)]sử dụng bảng điều khiển để hiển thị nhiều loại kiểm soát tổ chức. Có sẵn nhiều loại bảng điều khiển được xác định trước trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] để hỗ trợ nhiều tùy chọn bố cục như bố cục theo tab, bố cục sàn và bố cục xếp chồng. Bạn xác định cách sắp xếp các bảng điều khiển này trên màn hình chính của [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] bằng cách sử dụng kiểm soát tổ chức **Bố cục bảng điều khiển**. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Panel Layout (Hosted Control)](../unified-service-desk/panel-layout-hosted-control.md)  

<a name="Panels"></a>   
## <a name="panels-in-unified-service-desk"></a>Bảng điều khiển trong Unified Service Desk  
 Bất cứ khi nào bạn tạo kiểm soát tổ chức, bạn cần phải chỉ định bảng điều khiển sẽ giữ nó trong trường **Hiển thị nhóm** của trang **Kiểm soát tổ chức mới**. Đối với hầu hết các loại kiểm soát tổ chức, [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] tự động xác định giá trị bảng điều khiển trong trường **Hiển thị nhóm**. For example, **MainPanel** is used for a **CRM Page** type of hosted control and **ToolbarPanel** is used for the **Toolbar Container** type of hosted control.  

 Bảng điều khiển được xác định trước sau đây có sẵn trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].  


|          Bảng điều khiển          |                                                                                      Mô tả                                                                                      |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        Bảng điều khiển chính        |                                                                        Vùng làm việc chính ở dưới cùng bên phải.                                                                        |
|        Bảng điều khiển trò chuyện        |                                                   Vị trí thông thường của cửa sổ trò chuyện. Cửa sổ ở dưới kiểm soát ghi mã lệnh tổng đài viên.                                                   |
|       Bảng điều khiển bị ẩn       |                                                    Bảng điều khiển bị ẩn sẽ được sử dụng cho các thành phần không có giao diện người dùng (UI).                                                     |
|       Bảng điều khiển bên trái 1        |                                                                 Bảng điều khiển chỉ dưới **Bảng điều khiển quy trình làm việc** ở bên trái.                                                                 |
|       Bảng điều khiển bên trái 2        |                                                                  Bảng điều khiển chỉ ở dưới **Bảng điều khiển bên trái 1** ở bên trái.                                                                   |
|      Điền đầy bảng điều khiển bên trái      |                        Bảng điều khiển chỉ ở dưới **Bảng điều khiển bên trái 2**. Bảng điều khiển này mở rộng để điền vào phần còn lại của vùng sẵn có ở cạnh dưới cùng của bảng điều khiển bên trái.                         |
|       RightPanel        |                                                                          Một bảng điều khiển nằm ở phía bên phải.                                                                           |
|       CtiPanel \*       | Bảng điều khiển nằm ở phía trên cùng bên phải, đó là vị trí mặc định cho kiểm soát điện thoại mềm. Đây là bảng điều khiển kiểu xếp chồng vì vậy có thể thêm nhiều kiểm soát và hiển thị bên cạnh các kiểm soát khác. |
| SessionExplorerPanel \* |                                              Bảng điều khiển nằm ngay dưới các tab phiên nơi bạn thường hiển thị dòng phiên.                                               |
|    WorkflowPanel \*     |                                       Bảng điều khiển nằm ngay dưới **Bảng điều khiển trình khám phá phiên** và thường chứa kiểm soát lập mã lệnh tổng đài viên.                                       |
|     ToolbarPanel \*     |          Bảng điều khiển ở trên đầu về bên phải của biểu trưng [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] và thường có thanh công cụ.          |
|       Bảng điều khiển ruy băng       |                                                                                For internal use only.                                                                                 |
|     StatusPanel \*      |                                                      Bảng điều khiển đặc biệt nằm trên thanh trạng thái ở dưới cùng của ứng dụng.                                                      |

 \* These panels are generally reserved for special purposes so use of these should be avoided unless required.  

 You can also assign keyboard shortcuts to panels so that customer service agents can directly access the panel in the client application by just using the keyboard. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Keyboard shortcuts for panels](../unified-service-desk/keyboard-shortcuts-panels.md)  

<a name="PanelTypes"></a>   
## <a name="panel-types-in-unified-service-desk"></a>Loại bảng điều khiển trong Unified Service Desk  
 [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]cung cấp các loại bảng điều khiển được xác định trước để hỗ trợ một loạt các tùy chọn bố cục:  


|      Loại bảng điều khiển      |                                                                                                                                                                                                                                                                               Mô tả                                                                                                                                                                                                                                                                                |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     Bảng điều khiển Tab USD      |                                                                                   Loại bảng điều khiển chứa kiểm soát tab. Mỗi kiểm soát tổ chức được tải trên một trong số các tab. Tên tab sẽ hiển thị giá trị được chỉ định trong trường **Hiển thị tên** của kiểm soát tổ chức. Nếu không có tên hiển thị được chỉ định cho kiểm soát tổ chức, tên kiểm soát tổ chức được hiển thị làm tên tab. Tab điều khiển/tiêu đề được hiển thị cho các loại bảng điều khiển nếu một hoặc nhiều kiểm soát tổ chức có trên đó.                                                                                   |
|    Bảng điều khiển xếp chồng USD     | This panel type stacks hosted controls in a horizontal or vertical fashion similar to a stack panel in [!INCLUDE[pn_ms_Windows_Presentation_Foundation](../includes/pn-ms-windows-presentation-foundation.md)]. These can be useful for toolbars or status bars, etc. This panel type is derived from StackPanel, which supports an [Orientation](http://msdn.microsoft.com/library/system.windows.controls.stackpanel.orientation\(v=vs.100\).aspx) property. Định hướng này nên được xác định trong XAML để xác định cách xếp chồng các kiểm soát tổ chức. |
|   Bảng điều khiển tab sàn USD    |                                                                                                                    Nếu có một kiểm soát tổ chức trên bảng điều khiển này, các tab sẽ không được hiển thị. Các tab cho kiểm soát tab được hiển thị nếu hai hoặc nhiều kiểm soát nằm trên bảng này.<br /><br /> Kiểm soát này là giống như **Bảng điều khiển Tab USD** nhưng kiểu tồn tại trong các chủ đề mặc định sẽ ẩn các tab ở phía trên, khi chỉ có kiểm soát được tải.                                                                                                                     |
|   Bảng điều khiển thu nhỏ USD   |                                                                                                                                                                       Bảng điều khiển này giống như **Bảng điều khiển Tab USD** nhưng kiểu trong chủ đề mặc định được xác định sẽ tự động thu nhỏ loại bảng điều khiển này để nó không còn chiếm diện tích trong giao diện người dùng, nếu không có kiểm soát tổ chức nào được tải trong bảng điều khiển.                                                                                                                                                                        |
|   Bảng điều khiển Nổi USD   |                                                                                                                                          Máy tính để bàn mặc định cung cấp phiên bản của loại bảng điều khiển này. When “FloatingPanel” is specified for a hosted control, this panel type is being used. Thông thường bạn sẽ không chỉ định loại bảng trong bố cục tùy chỉnh của mình, tuy nhiên trong trường hợp cần sử dụng loại bảng điều khiển này thì nó sẽ được sử dụng.                                                                                                                                          |
| Bảng điều khiển công cụ Nổi USD |                                                                                                 Loại bảng điều khiển này tạo ra một cửa sổ công cụ cho mỗi kiểm soát tổ chức được tải vào bảng điều khiển đó. The default desktop provides an instance of this panel type. When “FloatingToolPanel” is specified for a hosted control, this panel type is being used. Thông thường bạn sẽ không chỉ định loại bảng trong bố cục tùy chỉnh của mình, tuy nhiên trong trường hợp cần sử dụng loại bảng điều khiển này thì nó sẽ được sử dụng.                                                                                                 |
|    USDPopUpPanel     |                                                                                                                                                                                                                                          Loại bảng điều khiển này cho phép nội dung trong bộ điều khiển lưu trữ di chuột qua giao diện chính.                                                                                                                                                                                                                                          |

 Bạn cũng có thể sử dụng các loại bảng điều khiển được xác định trước để tạo ra một loại bảng điều khiển tùy chỉnh trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Create a custom panel type](../unified-service-desk/create-custom-panel-type.md)  

<a name="PanelLayouts"></a>   
## <a name="panel-layouts-in-unified-service-desk"></a>Bố cục bảng điều khiển trong Unified Service Desk  
 Use  a panel layout to define the arrangement of panels on the screen in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client. A panel layout is defined using a **Panel Layout** hosted control. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Panel Layout (Hosted Control)](../unified-service-desk/panel-layout-hosted-control.md)  

 The following layout depicts the **Standard Main Panel** type of panel layout (also called standard panel layout) in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].  

 ![Air theme in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-themeair.png "Air theme in Unified Service Desk")  

> [!NOTE]
>  If you do not create any panel layout in your [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration, the standard panel layout is used automatically to display panels and controls in the client application.  
> 
>  The full application area on the main window is defined as a panel itself, and is called `MainWorkArea`.While defining `XAML` or `User-Defined` type of panel layout, `MainWorkArea` is used as the panel value for the **Display Group** field.  

 Because  panel layouts are hosted controls, you may use a panel layout anywhere you would have configured a hosted control. Một cách sử dụng phổ biến cho loại này đó là xác định chế độ xem phân chia trong vùng bảng điều khiển chính. Bạn có thể hiển thị chế độ xem danh sách hiển thị danh sách các tài khoản ở đầu và chế độ xem chi tiết ở dưới cùng. Bạn có thể hiển thị toàn bộ bộ cục bảng điều khiển trong bảng điều khiển nổi và hiển thị nó trên một màn hình thứ hai. For more information about the usage of floating panes, see [Configure Pop In and Pop Out feature for knowledge base articles](../unified-service-desk/configure-unified-service-desk-use-dynamics-365-knowledge.md#PopInOut).  

 [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] provides the following types of panel layouts:  

 **Bảng điều khiển chính tiêu chuẩn**  
 The standard panel layout provides the traditional layout including a series of panels on the left, collapsible area and a main work area on the right. The following is the XAML used to define the panel layout. You can also find this XAML in the [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] SDK. [Download](http://go.microsoft.com/fwlink/p/?LinkId=395257) the package, and extract it to view the `SamplePanelLayout.xaml`  file under the "UII\USD Developer Assets\USD Layout and Style Sheet" directory.  

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

 **Bảng điều khiển chính Ruy băng**  
 For internal use only.  

 **Phân chia theo hướng ngang**  
 This is a special layout typically used within the MainPanel as a hosted control. Nó chứa một bộ chia với bảng điều khiển trên đầu và bảng điều khiển ở dưới. Nó thường được sử dụng để hiển thị chế độ xem danh sách ở đầu và chế độ xem chi tiết ở cuối tương tự như Outlook. Hai bảng điều khiển được xác định trong bố cục này.  

|Tên bảng điều khiển|Mô tả|  
|----------------|-----------------|  
|TopPanel|Đây là bảng điều khiển hiển thị trên đầu. Nó được định nghĩa là:<br /><br /> Bảng điều khiển tab sàn USD|  
|BottomPanel|Đây là bảng điều khiển hiển thị phía dưới. It is defined as:<br /><br /> Bảng điều khiển tab sàn USD|  

 Bản điều khiển này hỗ trợ các thao tác sau:  


|        Hành động        |                                                                                                                                                                                                                                                                                              Mô tả                                                                                                                                                                                                                                                                                              |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  SetTopPanelHeight   | Hành động này có thể được sử dụng để đặt chiều cao của bảng điều khiển ở trên đầu. Nó hỗ trợ hai tham số, chiều cao và loại.<br /><br /> Loại có thể là bất kỳ giá trị nào sau đây:<br /><br /> - **Tự động**: được đặt kích thước để phù hợp với thành phần bên trong<br />- **Điểm ảnh**: số điểm ảnh<br />- **Sao**: chiếm không gian còn lại<br /><br /> Việc giải thích của các tham số chiều cao phụ thuộc vào giá trị loại này. For more information, see the [!INCLUDE[pn_ms_Windows_Presentation_Foundation](../includes/pn-ms-windows-presentation-foundation.md)][documentation](http://msdn.microsoft.com/library/ms754130\(v=vs.100\).aspx). |
| SetBottomPanelHeight |                                              Hành động này có thể được sử dụng để đặt chiều cao của bảng điều khiển ở phía dưới. It supports two parameters, height and type.<br /><br /> Loại có thể là bất kỳ giá trị nào sau đây:<br /><br /> - **Tự động**: được đặt kích thước để phù hợp với thành phần bên trong<br />- **Điểm ảnh**: số điểm ảnh<br />- **Sao**: chiếm không gian còn lại<br /><br /> Việc giải thích của các tham số chiều cao phụ thuộc vào giá trị loại này. Để biết thêm thông tin, xem tài liệu [WPF](http://msdn.microsoft.com/en-us/library/ms754130\(v=vs.100\).aspx).                                              |

 **Phân chia theo chiều dọc**  
 Đây là một bố cục đặc biệt có chứa bộ phân chia theo hướng dọc với một bảng điều khiển bên trái và một bảng điều khiển bên phải.  

|Tên bảng điều khiển|Mô tả|  
|----------------|-----------------|  
|LeftPanel|Đây là bảng điều khiển hiển thị bên trái. It is defined as:<br /><br /> Bảng điều khiển tab sàn USD|  
|RightPanel|Đây là bảng điều khiển hiển thị bên phải. It is defined as:<br /><br /> Bảng điều khiển tab sàn USD|  

 This panel supports the following actions:  

|Hành động|Mô tả|  
|------------|-----------------|  
|SetLeftPanelWidth|Hành động này có thể được sử dụng để đặt chiều rộng của bảng điều khiển bên trái. Nó hỗ trợ hai tham số, chiều rộng và loại.<br /><br /> Loại có thể là bất kỳ giá trị nào sau đây:<br /><br /> - **Tự động**: được đặt kích thước để phù hợp với thành phần bên trong<br />- **Điểm ảnh**: số điểm ảnh<br />- **Sao**: chiếm không gian còn lại<br /><br /> Việc giải thích của các tham số chiều rộng phụ thuộc vào giá trị loại này. Để biết thêm thông tin, xem tài liệu [WPF](http://msdn.microsoft.com/library/ms754130\(v=vs.100\).aspx).|  
|SetRightPanelWidth|Hành động này có thể được sử dụng để đặt chiều rộng của bảng điều khiển bên phải. It supports two parameters, width and type.<br /><br /> Loại có thể là bất kỳ giá trị nào sau đây:<br /><br /> - **Tự động**: được đặt kích thước để phù hợp với thành phần bên trong<br />- **Điểm ảnh**: số điểm ảnh<br />- **Sao**: chiếm không gian còn lại<br /><br /> Việc giải thích của các tham số chiều rộng phụ thuộc vào giá trị loại này. Xem tài liệu WPF để biết thêm chi tiết.|  

 **XAML**  
 Một trong những cách nhanh nhất để tạo bố cục tùy chỉnh. Tuy nhiên, tùy chọn này không hỗ trợ mã-đằng sau. Kết quả là, nếu bạn không thể mô tả bố cục của mình mà không có mã, bạn không thể sử dụng tùy chọn này và thay vào đó nên sử dụng tùy chọn **Do người dùng xác định**. For more information, see [Code-Behind and XAML in WPF](http://msdn.microsoft.com/library/aa970568\(v=vs.100\).aspx).  

 Here is an example of a XAML layout.  

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

 **Do người dùng xác định**  
 Thiết đặt này cho phép bạn xây dựng kiểm soát tổ chức với [mã đằng sau](http://msdn.microsoft.com/library/aa970568\(v=vs.100\).aspx) để nhận đầy đủ tính năng của of .NET trong khi xử lý bố cục của bạn.  

 For details about what panel types can be defined and used in a user defined panel, see [Panel types](../unified-service-desk/panels-panel-types-panel-layouts.md#PanelTypes).  

 For information about creating a custom panel layout, see [Create a custom panel layout](../unified-service-desk/create-custom-panel-layout.md).  

### <a name="see-also"></a>Xem thêm  
 [Sử dụng loại bảng điều khiển tùy chỉnh và bố cục bảng điều khiển](../unified-service-desk/use-custom-panel-types-panel-layouts-unified-service-desk.md)   
 [Keyboard shortcuts for panels](../unified-service-desk/keyboard-shortcuts-panels.md)
