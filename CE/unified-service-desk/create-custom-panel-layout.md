---
title: Create a custom panel layout | MicrosoftDocs
description: Panel layouts in Unified Service Desk are hosted controls, which provide the ability to load all sorts of different layouts in the system. Unified Service Desk provides some predefined panel layouts for you to use in your agent application.
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
ms.assetid: 6b57c966-00ab-4ebe-9d91-07ae9fa100ba
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
ms.openlocfilehash: da05900b7e5ff7ec170cfd110b7dad16dfd6a444
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388676"
---
# <a name="create-a-custom-panel-layout"></a><span data-ttu-id="e2c60-104">Create a custom panel layout</span><span class="sxs-lookup"><span data-stu-id="e2c60-104">Create a custom panel layout</span></span>
<span data-ttu-id="e2c60-105">Panel layouts in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] are hosted controls, which provide the ability to load all sorts of different layouts in the system.</span><span class="sxs-lookup"><span data-stu-id="e2c60-105">Panel layouts in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] are hosted controls, which provide the ability to load all sorts of different layouts in the system.</span></span> [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] <span data-ttu-id="e2c60-106">provides some predefined panel layouts for you to use in your agent application.</span><span class="sxs-lookup"><span data-stu-id="e2c60-106">provides some predefined panel layouts for you to use in your agent application.</span></span> <span data-ttu-id="e2c60-107">For more information, see [Panel layouts](../unified-service-desk/panels-panel-types-panel-layouts.md#PanelLayouts).</span><span class="sxs-lookup"><span data-stu-id="e2c60-107">For more information, see [Panel layouts](../unified-service-desk/panels-panel-types-panel-layouts.md#PanelLayouts).</span></span>  
  
 [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] <span data-ttu-id="e2c60-108">also lets you create user defined or custom panel layouts where you lay out the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] panel types as per your requirement, and enhance the experience with [code-behind XAML](https://msdn.microsoft.com/library/vstudio/aa970568\(v=vs.110\).aspx).</span><span class="sxs-lookup"><span data-stu-id="e2c60-108">also lets you create user defined or custom panel layouts where you lay out the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] panel types as per your requirement, and enhance the experience with [code-behind XAML](https://msdn.microsoft.com/library/vstudio/aa970568\(v=vs.110\).aspx).</span></span> [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] <span data-ttu-id="e2c60-109">apps provides a Visual Studio project template for creating user-defined panel layouts with code-behind support.</span><span class="sxs-lookup"><span data-stu-id="e2c60-109">apps provides a Visual Studio project template for creating user-defined panel layouts with code-behind support.</span></span>  
  
 <span data-ttu-id="e2c60-110">This topic shows you how to create a panel layout where you’ll rearrange the panels to display the session information, agent scripting, notes manager, and associated cases to appear on the right side of the desktop instead of the left side.</span><span class="sxs-lookup"><span data-stu-id="e2c60-110">This topic shows you how to create a panel layout where you’ll rearrange the panels to display the session information, agent scripting, notes manager, and associated cases to appear on the right side of the desktop instead of the left side.</span></span> <span data-ttu-id="e2c60-111">Also, the pane that displays all this information will be displayed automatically when a session is started in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], and will disappear automatically when the session is closed instead of you having to manually expand and collapse the pane.</span><span class="sxs-lookup"><span data-stu-id="e2c60-111">Also, the pane that displays all this information will be displayed automatically when a session is started in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], and will disappear automatically when the session is closed instead of you having to manually expand and collapse the pane.</span></span>  
  
<a name="Prereq"></a>   
## <a name="prerequisites"></a><span data-ttu-id="e2c60-112">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="e2c60-112">Prerequisites</span></span>  
  
- [!INCLUDE[pn_Microsoft_.Net_Framework](../includes/pn-microsoft-net-framework.md)] <span data-ttu-id="e2c60-113">4.5.2</span><span class="sxs-lookup"><span data-stu-id="e2c60-113">4.5.2</span></span>  
  
- [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] <span data-ttu-id="e2c60-114">client application; the client application is required for testing the custom panel layout hosted control by signing in using the agent application.</span><span class="sxs-lookup"><span data-stu-id="e2c60-114">client application; the client application is required for testing the custom panel layout hosted control by signing in using the agent application.</span></span>  
  
- [!INCLUDE[pn_microsoft_visual_studio_2012](../includes/pn-microsoft-visual-studio-2012.md)]<span data-ttu-id="e2c60-115">, [!INCLUDE[pn_visual_studio_2013](../includes/pn-visual-studio-2013.md)], or [!INCLUDE[pn_visual_studio_2015](../includes/pn-visual-studio-2015.md)]</span><span class="sxs-lookup"><span data-stu-id="e2c60-115">, [!INCLUDE[pn_visual_studio_2013](../includes/pn-visual-studio-2013.md)], or [!INCLUDE[pn_visual_studio_2015](../includes/pn-visual-studio-2015.md)]</span></span>  
  
- [!INCLUDE[tn_nuget](../includes/tn-nuget.md)] <span data-ttu-id="e2c60-116">Package Manager for [Visual Studio 2012](http://visualstudiogallery.msdn.microsoft.com/27077b70-9dad-4c64-adcf-c7cf6bc9970c), [Visual Studio 2013](http://visualstudiogallery.msdn.microsoft.com/4ec1526c-4a8c-4a84-b702-b21a8f5293ca), or [Visual Studio 2015](https://visualstudiogallery.msdn.microsoft.com/5d345edc-2e2d-4a9c-b73b-d53956dc458d)</span><span class="sxs-lookup"><span data-stu-id="e2c60-116">Package Manager for [Visual Studio 2012](http://visualstudiogallery.msdn.microsoft.com/27077b70-9dad-4c64-adcf-c7cf6bc9970c), [Visual Studio 2013](http://visualstudiogallery.msdn.microsoft.com/4ec1526c-4a8c-4a84-b702-b21a8f5293ca), or [Visual Studio 2015](https://visualstudiogallery.msdn.microsoft.com/5d345edc-2e2d-4a9c-b73b-d53956dc458d)</span></span>  
  
- <span data-ttu-id="e2c60-117">**CRM SDK Templates** for [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] that contains the custom panel layout project template.</span><span class="sxs-lookup"><span data-stu-id="e2c60-117">**CRM SDK Templates** for [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] that contains the custom panel layout project template.</span></span> <span data-ttu-id="e2c60-118">[Download](http://go.microsoft.com/fwlink/p/?LinkId=400925) the **CRM SDK Templates** from the Visual Studio gallery, and double-click the CRMSDKTemplates.vsix file to install the template in [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)].</span><span class="sxs-lookup"><span data-stu-id="e2c60-118">[Download](http://go.microsoft.com/fwlink/p/?LinkId=400925) the **CRM SDK Templates** from the Visual Studio gallery, and double-click the CRMSDKTemplates.vsix file to install the template in [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)].</span></span>  
  
<a name="HowTo"></a>   
## <a name="create-a-custom-panel-layout"></a><span data-ttu-id="e2c60-119">Create a custom panel layout</span><span class="sxs-lookup"><span data-stu-id="e2c60-119">Create a custom panel layout</span></span>  
  
<a name="Step1"></a>   
1. <span data-ttu-id="e2c60-120">Start [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)], and create a new project.</span><span class="sxs-lookup"><span data-stu-id="e2c60-120">Start [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)], and create a new project.</span></span>  
  
2. <span data-ttu-id="e2c60-121">In the **New Project** dialog box:</span><span class="sxs-lookup"><span data-stu-id="e2c60-121">In the **New Project** dialog box:</span></span>  
  
   1. <span data-ttu-id="e2c60-122">From the list of installed templates, expand **Visual C#**, and select **CRM SDK Templates** > **Unified Service Desk** > **USD Custom Panel Layout**.</span><span class="sxs-lookup"><span data-stu-id="e2c60-122">From the list of installed templates, expand **Visual C#**, and select **CRM SDK Templates** > **Unified Service Desk** > **USD Custom Panel Layout**.</span></span>  
  
   2. <span data-ttu-id="e2c60-123">Ensure that **[!INCLUDE[pn_NET_Framework](../includes/pn-net-framework.md)] 4.5.2** is selected.</span><span class="sxs-lookup"><span data-stu-id="e2c60-123">Ensure that **[!INCLUDE[pn_NET_Framework](../includes/pn-net-framework.md)] 4.5.2** is selected.</span></span>  
  
   3. <span data-ttu-id="e2c60-124">Specify the name and location of the project, and click **OK**.</span><span class="sxs-lookup"><span data-stu-id="e2c60-124">Specify the name and location of the project, and click **OK**.</span></span>  
  
   <span data-ttu-id="e2c60-125">![Create a custom panel layout](../unified-service-desk/media/usd-custom-panel-type-1.png "Create a custom panel layout")</span><span class="sxs-lookup"><span data-stu-id="e2c60-125">![Create a custom panel layout](../unified-service-desk/media/usd-custom-panel-type-1.png "Create a custom panel layout")</span></span>  
  
3. <span data-ttu-id="e2c60-126">In **Solution Explorer**, double-click the `CustomLayout.xaml` file to bring up the XAML designer.</span><span class="sxs-lookup"><span data-stu-id="e2c60-126">In **Solution Explorer**, double-click the `CustomLayout.xaml` file to bring up the XAML designer.</span></span> <span data-ttu-id="e2c60-127">The XAML designer displays the default panel layout in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="e2c60-127">The XAML designer displays the default panel layout in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span>  
  
4. <span data-ttu-id="e2c60-128">Replace the XAML code in the `CustomLayout.xaml` file with the code provided in the following sample.</span><span class="sxs-lookup"><span data-stu-id="e2c60-128">Replace the XAML code in the `CustomLayout.xaml` file with the code provided in the following sample.</span></span> <span data-ttu-id="e2c60-129">To do this, select all the code (CTRL+A) in the XAML area (as shown in the illustration), delete it, and then paste the XAML code provided at the same place.</span><span class="sxs-lookup"><span data-stu-id="e2c60-129">To do this, select all the code (CTRL+A) in the XAML area (as shown in the illustration), delete it, and then paste the XAML code provided at the same place.</span></span> <span data-ttu-id="e2c60-130">This is done to change the location of the expander pane from left to right.</span><span class="sxs-lookup"><span data-stu-id="e2c60-130">This is done to change the location of the expander pane from left to right.</span></span>  
  
   <span data-ttu-id="e2c60-131">![Update the XAML code for the custom panel layout](../unified-service-desk/media/usd-create-custom-panel-layout-2.png "Update the XAML code for the custom panel layout")</span><span class="sxs-lookup"><span data-stu-id="e2c60-131">![Update the XAML code for the custom panel layout](../unified-service-desk/media/usd-create-custom-panel-layout-2.png "Update the XAML code for the custom panel layout")</span></span>  
  
   ```  
   <USD:PanelLayoutBase             
           x:Class="MyUSDCustomPanelLayout.CustomLayout"  
           xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"  
           xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"  
           xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"  
           xmlns:d="http://schemas.microsoft.com/expression/blend/2008"  
           mc:Ignorable="d"   
           xmlns:local="clr-namespace:Microsoft.Crm.UnifiedServiceDesk.Dynamics;assembly=Microsoft.Crm.UnifiedServiceDesk.Dynamics"  
           xmlns:USD="clr-namespace:Microsoft.Crm.UnifiedServiceDesk.Dynamics.PanelLayouts;assembly=Microsoft.Crm.UnifiedServiceDesk.Dynamics"  
           d:DesignHeight="500" d:DesignWidth="500">  
       <Grid x:Name="LayoutRoot">  
           <Grid.Resources>  
               <local:CRMImageConverter x:Key="CRMImageLoader" />  
               <Style x:Key="ImageLogo" TargetType="{x:Type Image}">  
                   <Setter Property="FlowDirection" Value="LeftToRight"/>  
                   <Setter Property="Width" Value="161" />  
                   <Setter Property="Height" Value="25" />  
                   <Setter Property="Margin" Value="0" />  
                   <Setter Property="HorizontalAlignment" Value="Left" />  
                   <Setter Property="VerticalAlignment" Value="Center" />  
               </Style>  
           </Grid.Resources>  
           <Grid.RowDefinitions>  
               <RowDefinition Height="auto"/>  
               <RowDefinition Height="*"/>  
               <RowDefinition Height="auto"/>  
           </Grid.RowDefinitions>  
           <Border Grid.Row="0" BorderBrush="#d8d8d8" BorderThickness="0,1,0,1">  
               <Grid Background="{DynamicResource WindowHeaderStyle}" Grid.Row="0"  Margin="0">  
                   <Grid.ColumnDefinitions>  
                       <ColumnDefinition Width="auto" />  
                       <ColumnDefinition Width="auto" />  
                       <ColumnDefinition Width="*" />  
                       <ColumnDefinition Width="Auto" />  
                   </Grid.ColumnDefinitions>  
                   <Image Grid.Column="0" Source="{Binding Source=msdyusd_Logo, Converter={StaticResource CRMImageLoader}}"  Style="{DynamicResource ImageLogo}"   />  
                   <Rectangle Width="10" Grid.Column="1" />  
                   <USD:USDDeckTabPanel x:Name="ToolbarPanel" Grid.Column="2" AutomationProperties.Name="Toolbar Panel" VerticalAlignment="Stretch" Focusable="False" Margin="1" />  
                   <Grid Grid.Column="3">  
                       <Grid.ColumnDefinitions>  
                           <ColumnDefinition Width="*" />  
                           <ColumnDefinition Width="412"/>  
                       </Grid.ColumnDefinitions>  
                       <Grid.Background>  
                           <ImageBrush ImageSource="{Binding Source=msdyusd_Office15, Converter={StaticResource CRMImageLoader}}" Stretch="Fill" ></ImageBrush>  
                       </Grid.Background>  
                       <USD:USDStackPanel Grid.Column="0" x:Name="CtiPanel"  Orientation="Horizontal" Focusable="False" VerticalAlignment="Center" AutomationProperties.Name="Cti Panel" SelectedAppChanged="SelectedAppChangedHander"/>  
                       <USD:USDStackPanel Grid.Column="1" HorizontalAlignment="Right" x:Name="AboutPanel"  Orientation="Horizontal" Focusable="False" VerticalAlignment="Center" AutomationProperties.Name="AboutPanel"/>  
                   </Grid>  
               </Grid>  
           </Border>  
           <Grid Grid.Row="1" VerticalAlignment="Stretch" Margin="0" Background="{DynamicResource WindowBackgroundStyle}">  
               <Grid.RowDefinitions>  
                   <RowDefinition Height="auto" />  
                   <RowDefinition Height="*" />  
                   <RowDefinition Height="auto" />  
               </Grid.RowDefinitions>  
               <USD:USDDeckTabPanel x:Name="SessionTabsPanel" Grid.Row="0" Margin="5,5,0,5" AutomationProperties.Name="Session Tabs Panel" Focusable="False" ClipToBounds="True" />  
               <Grid x:Name="MainGrid" Grid.Row="1" AutomationProperties.Name="Main Panels">  
                   <Grid.ColumnDefinitions>  
                       <ColumnDefinition Width="*" />  
                       <ColumnDefinition Width="auto"/>  
                   </Grid.ColumnDefinitions>  
                   <Expander Grid.Column="1" Style="{DynamicResource StretchExpanderStyle}"  ExpandDirection="Right" x:Name="RightExpander" IsExpanded="false" BorderBrush="White" Expanded="Expander_Expanded" Collapsed="Expander_Collapsed" >  
                       <Grid Style="{DynamicResource LeftPanelGrid}">  
                           <Grid.RowDefinitions>  
                               <RowDefinition Height="auto" />  
                               <RowDefinition Height="auto" />  
                               <RowDefinition Height="auto" Name="ChatPanelRow" />  
                               <RowDefinition Height="auto" />  
                               <RowDefinition Height="auto" />  
                               <RowDefinition Height="*" />  
                           </Grid.RowDefinitions>  
                           <USD:USDCollapsePanel x:Name="SessionExplorerPanel" AutomationProperties.Name="Session Explorer Panel" Grid.Row="0" Margin="1" SelectedAppChanged="SelectedAppChangedHander" />  
                           <USD:USDCollapsePanel x:Name="WorkflowPanel" AutomationProperties.Name="Workflow Panel" Grid.Row="1" Margin="1" SelectedAppChanged="SelectedAppChangedHander" />  
                           <USD:USDCollapsePanel x:Name="ChatPanel" AutomationProperties.Name="Workflow Panel" Grid.Row="2" Margin="1" SelectedAppChanged="SelectedAppChangedHander"/>  
                           <USD:USDCollapsePanel x:Name="LeftPanel1" AutomationProperties.Name="Left Panel 1" Grid.Row="3" Margin="1" SelectedAppChanged="SelectedAppChangedHander"/>  
                           <USD:USDCollapsePanel x:Name="LeftPanel2" AutomationProperties.Name="Left Panel 2" Grid.Row="4" Margin="1" SelectedAppChanged="SelectedAppChangedHander"/>  
                           <USD:USDDeckTabPanel x:Name="LeftPanelFill" AutomationProperties.Name="Left Panel Fill" Grid.Row="5" Margin="1" SelectedAppChanged="SelectedAppChangedHander"/>  
                       </Grid>  
                   </Expander>  
                   <Grid Grid.Column="0" Background="Transparent">  
                       <Grid.RowDefinitions>  
                           <RowDefinition Height="0" />  
                           <RowDefinition Height="*" />  
                       </Grid.RowDefinitions>  
                       <USD:USDCollapsePanel x:Name="RibbonPanel" Grid.Row="0" Visibility="Collapsed"  AutomationProperties.Name="Ribbon Panel" Focusable="False" Margin="1" ClipToBounds="False" SnapsToDevicePixels="True" />  
                       <USD:USDTabPanel x:Name="MainPanel" Grid.Row="1" AutomationProperties.Name="Main Panel" SelectedAppChanged="SelectedAppChangedHander"/>  
                   </Grid>  
               </Grid>  
           </Grid>  
           <StatusBar Margin="0" Background="{DynamicResource WindowHeaderStyle}"  Grid.Row="2" Height="auto" VerticalAlignment="Bottom">  
               <StatusBarItem Background="{DynamicResource WindowHeaderStyle}" >  
                   <USD:USDStackPanel x:Name="StatusPanel" Orientation="Horizontal" AutomationProperties.Name="Status Panel" Margin="1" SelectedAppChanged="SelectedAppChangedHander" />  
               </StatusBarItem>  
           </StatusBar>  
       </Grid>  
   </USD:PanelLayoutBase>  
   ```  
  
5. <span data-ttu-id="e2c60-132">You can also define a keyboard shortcut to access a panel in your custom panel layout.</span><span class="sxs-lookup"><span data-stu-id="e2c60-132">You can also define a keyboard shortcut to access a panel in your custom panel layout.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="e2c60-133">[Define keyboard shortcuts for panels in custom panel layout](../unified-service-desk/keyboard-shortcuts-panels.md)</span><span class="sxs-lookup"><span data-stu-id="e2c60-133">[Define keyboard shortcuts for panels in custom panel layout](../unified-service-desk/keyboard-shortcuts-panels.md)</span></span>  
  
6. <span data-ttu-id="e2c60-134">In **Solution Explorer**, right-click the `CustomLayout.xaml` file, and click **View Code** to add the code behind the XAML.</span><span class="sxs-lookup"><span data-stu-id="e2c60-134">In **Solution Explorer**, right-click the `CustomLayout.xaml` file, and click **View Code** to add the code behind the XAML.</span></span> <span data-ttu-id="e2c60-135">This opens up the `CustomLayout.xaml.cs` file.</span><span class="sxs-lookup"><span data-stu-id="e2c60-135">This opens up the `CustomLayout.xaml.cs` file.</span></span>  
  
7. <span data-ttu-id="e2c60-136">Update the `NotifyContextChange` method definition by adding the following code.</span><span class="sxs-lookup"><span data-stu-id="e2c60-136">Update the `NotifyContextChange` method definition by adding the following code.</span></span>  
  
   ```  
   if (context.Count != 0)  
   {  
      RightExpander.IsExpanded = true;  
   }  
   else  
   {   
      RightExpander.IsExpanded = false;  
   }  
   ```  
  
    <span data-ttu-id="e2c60-137">The code checks if there are any sessions active in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], and automatically displays (expands) or hides (collapses) the expander pane.</span><span class="sxs-lookup"><span data-stu-id="e2c60-137">The code checks if there are any sessions active in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], and automatically displays (expands) or hides (collapses) the expander pane.</span></span>  
  
    <span data-ttu-id="e2c60-138">This is the updated `NotifyContextChange` method definition.</span><span class="sxs-lookup"><span data-stu-id="e2c60-138">This is the updated `NotifyContextChange` method definition.</span></span>  
  
   <span data-ttu-id="e2c60-139">![Updated NotifyContextChange method](../unified-service-desk/media/usd-create-custom-panel-layout-3.png "Updated NotifyContextChange method")</span><span class="sxs-lookup"><span data-stu-id="e2c60-139">![Updated NotifyContextChange method](../unified-service-desk/media/usd-create-custom-panel-layout-3.png "Updated NotifyContextChange method")</span></span>  
  
8. <span data-ttu-id="e2c60-140">Save your project, and build it (**Build** > **Build Solution**) to check if it builds successfully.</span><span class="sxs-lookup"><span data-stu-id="e2c60-140">Save your project, and build it (**Build** > **Build Solution**) to check if it builds successfully.</span></span>  
  
   > [!NOTE]
   >  <span data-ttu-id="e2c60-141">Note the name of the class that is used to build your custom panel layout in the `CustomLayout.xaml.cs` file.</span><span class="sxs-lookup"><span data-stu-id="e2c60-141">Note the name of the class that is used to build your custom panel layout in the `CustomLayout.xaml.cs` file.</span></span> <span data-ttu-id="e2c60-142">Trong trường hợp này, đó là `CustomLayout`.</span><span class="sxs-lookup"><span data-stu-id="e2c60-142">In this case, it’s `CustomLayout`.</span></span> <span data-ttu-id="e2c60-143">You’ll need this information in the next step.</span><span class="sxs-lookup"><span data-stu-id="e2c60-143">You’ll need this information in the next step.</span></span>  
  
<a name="Test"></a>   
## <a name="test-your-custom-panel-layout"></a><span data-ttu-id="e2c60-144">Test your custom panel layout</span><span class="sxs-lookup"><span data-stu-id="e2c60-144">Test your custom panel layout</span></span>  
 <span data-ttu-id="e2c60-145">Sau khi dự án của bạn xây dựng thành công, kiểm tra bố cục bảng điều khiển tùy chỉnh.</span><span class="sxs-lookup"><span data-stu-id="e2c60-145">After your project builds successfully, test the custom panel layout.</span></span> <span data-ttu-id="e2c60-146">The testing consists of two parts: defining the custom panel layout hosted control on the server and then signing in to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] on the server using your client application with the custom code assembly in the client directory.</span><span class="sxs-lookup"><span data-stu-id="e2c60-146">The testing consists of two parts: defining the custom panel layout hosted control on the server and then signing in to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] on the server using your client application with the custom code assembly in the client directory.</span></span>  
  
### <a name="define-the-custom-panel-layout-hosted-control-on-server"></a><span data-ttu-id="e2c60-147">Xác định kiểm soát tổ chức bố cục bảng điều khiển tùy chỉnh trên máy chủ</span><span class="sxs-lookup"><span data-stu-id="e2c60-147">Define the custom panel layout hosted control on server</span></span>  
  
1. <span data-ttu-id="e2c60-148">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="e2c60-148">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. <span data-ttu-id="e2c60-149">On the nav bar, choose **Microsoft Dynamics 365 for Customer Engagement**, and select **Settings**.</span><span class="sxs-lookup"><span data-stu-id="e2c60-149">On the nav bar, choose **Microsoft Dynamics 365 for Customer Engagement**, and select **Settings**.</span></span>  
  
3. <span data-ttu-id="e2c60-150">Choose **Settings** > **Unified Service Desk** > **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="e2c60-150">Choose **Settings** > **Unified Service Desk** > **Hosted Controls**.</span></span>  
  
4. <span data-ttu-id="e2c60-151">Choose **NEW**, and then specify values in the **New Hosted Control** screen as shown here.</span><span class="sxs-lookup"><span data-stu-id="e2c60-151">Choose **NEW**, and then specify values in the **New Hosted Control** screen as shown here.</span></span>  
  
   <span data-ttu-id="e2c60-152">![Custom panel hosted control definition](../unified-service-desk/media/usd-custom-panel-type-2.png "Custom panel hosted control definition")</span><span class="sxs-lookup"><span data-stu-id="e2c60-152">![Custom panel hosted control definition](../unified-service-desk/media/usd-custom-panel-type-2.png "Custom panel hosted control definition")</span></span>  
  
   > [!NOTE]
   > <span data-ttu-id="e2c60-153">**Assembly URI** is the name of your assembly and the **Assembly Type** is the name of your assembly file (dll) followed by a dot (.) and then the class name in your [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] project.</span><span class="sxs-lookup"><span data-stu-id="e2c60-153">**Assembly URI** is the name of your assembly and the **Assembly Type** is the name of your assembly file (dll) followed by a dot (.) and then the class name in your [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] project.</span></span> <span data-ttu-id="e2c60-154">Trong ví dụ này, tên của cụm là **Bố cục bảng điều khiển tùy chỉnh USD của tôi** và tên của các lớp là **Bố cục tùy chỉnh**, chính là tên lớp mặc định khi bạn tạo bố cục bảng điều khiển tùy chỉnh.</span><span class="sxs-lookup"><span data-stu-id="e2c60-154">In this example, the name of the assembly is **MyUSDCustomPanelLayout** and name of the class is **CustomLayout**, which is the default class name when you create a custom panel layout.</span></span>  
  
5. <span data-ttu-id="e2c60-155">Save the hosted control.</span><span class="sxs-lookup"><span data-stu-id="e2c60-155">Save the hosted control.</span></span>  
  
### <a name="run-the-unified-service-desk-client-to-work-with-the-custom-panel-layout"></a><span data-ttu-id="e2c60-156">Run the Unified Service Desk client to work with the custom panel layout</span><span class="sxs-lookup"><span data-stu-id="e2c60-156">Run the Unified Service Desk client to work with the custom panel layout</span></span>  
  
1. <span data-ttu-id="e2c60-157">Copy the assembly file (dll) that contains your custom hosted control definition from your [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] project debug folder to the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] application directory, which is, by default, c:\Program Files\Microsoft Dynamics CRM USD\USD.</span><span class="sxs-lookup"><span data-stu-id="e2c60-157">Copy the assembly file (dll) that contains your custom hosted control definition from your [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] project debug folder to the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] application directory, which is, by default, c:\Program Files\Microsoft Dynamics CRM USD\USD.</span></span>  
  
2. <span data-ttu-id="e2c60-158">Run the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client to connect to your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps server.</span><span class="sxs-lookup"><span data-stu-id="e2c60-158">Run the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client to connect to your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps server.</span></span>  
  
3. <span data-ttu-id="e2c60-159">On successful sign in, you’ll see the custom panel layout without the expander pane in the left side.</span><span class="sxs-lookup"><span data-stu-id="e2c60-159">On successful sign in, you’ll see the custom panel layout without the expander pane in the left side.</span></span> <span data-ttu-id="e2c60-160">The expander pane is now on the right side.</span><span class="sxs-lookup"><span data-stu-id="e2c60-160">The expander pane is now on the right side.</span></span>  
  
   <span data-ttu-id="e2c60-161">![Screenshot of custom panel layout](../unified-service-desk/media/usd-create-custom-panel-layout-4.png "Screenshot of custom panel layout")</span><span class="sxs-lookup"><span data-stu-id="e2c60-161">![Screenshot of custom panel layout](../unified-service-desk/media/usd-create-custom-panel-layout-4.png "Screenshot of custom panel layout")</span></span>  
  
4. <span data-ttu-id="e2c60-162">Choose **Search** on the toolbar, and then select a record to be displayed in a session.</span><span class="sxs-lookup"><span data-stu-id="e2c60-162">Choose **Search** on the toolbar, and then select a record to be displayed in a session.</span></span> <span data-ttu-id="e2c60-163">In this case, choose **Contacts** in the **Search** window, and then choose **Maria Campbell (Sample)**.</span><span class="sxs-lookup"><span data-stu-id="e2c60-163">In this case, choose **Contacts** in the **Search** window, and then choose **Maria Campbell (Sample)**.</span></span> <span data-ttu-id="e2c60-164">The right pane automatically appears to display the associated session data, agent scripting, and other information about the current contact record.</span><span class="sxs-lookup"><span data-stu-id="e2c60-164">The right pane automatically appears to display the associated session data, agent scripting, and other information about the current contact record.</span></span>  
  
   <span data-ttu-id="e2c60-165">![The right expander pane displays automatically](../unified-service-desk/media/usd-create-custom-panel-layout-5.png "The right expander pane displays automatically")</span><span class="sxs-lookup"><span data-stu-id="e2c60-165">![The right expander pane displays automatically](../unified-service-desk/media/usd-create-custom-panel-layout-5.png "The right expander pane displays automatically")</span></span>  
  
5. <span data-ttu-id="e2c60-166">Close the session by clicking cross in the session tab at the top, and the right pane will automatically close/collapse.</span><span class="sxs-lookup"><span data-stu-id="e2c60-166">Close the session by clicking cross in the session tab at the top, and the right pane will automatically close/collapse.</span></span>  
  
   > [!NOTE]
   >  <span data-ttu-id="e2c60-167">In case of multiple sessions, the right pane will continue to display until you have closed all the session tabs.</span><span class="sxs-lookup"><span data-stu-id="e2c60-167">In case of multiple sessions, the right pane will continue to display until you have closed all the session tabs.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="e2c60-168">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="e2c60-168">See also</span></span>  
 <span data-ttu-id="e2c60-169">[Display hosted controls in the custom panel layout](../unified-service-desk/display-hosted-controls-custom-panel-layout.md) </span><span class="sxs-lookup"><span data-stu-id="e2c60-169">[Display hosted controls in the custom panel layout](../unified-service-desk/display-hosted-controls-custom-panel-layout.md) </span></span>  
 [<span data-ttu-id="e2c60-170">Panels, panel types, and panel layouts in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="e2c60-170">Panels, panel types, and panel layouts in Unified Service Desk</span></span>](../unified-service-desk/panels-panel-types-panel-layouts.md)
