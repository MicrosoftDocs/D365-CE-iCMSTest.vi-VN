---
title: Configure notifications in Unified Service Desk | MicrosoftDocs
description: Learn about configuring notifications in Unified Service Desk.
keywords: ''
ms.date: 08/17/2018
ms.service:
- dynamics-365-customerservice
ms.custom:
- dyn365-USD
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: ca7905ed-47a0-47c9-bbfe-5cb1738b0125
author: kabala123
ms.author: kabala
manager: shujoshi
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 58c38f62b4d5632369d9cf5e796247404dc66689
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386333"
---
# <a name="how-to-configure-notifications-in-unified-service-desk"></a><span data-ttu-id="10546-103">How to configure notifications in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="10546-103">How to configure notifications in Unified Service Desk</span></span>
<span data-ttu-id="10546-104">Configure notifications in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] to display popup notification messages to your customer service agents that contains general information or some customer or process-related information that the agent can act on.</span><span class="sxs-lookup"><span data-stu-id="10546-104">Configure notifications in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] to display popup notification messages to your customer service agents that contains general information or some customer or process-related information that the agent can act on.</span></span> <span data-ttu-id="10546-105">The layout and behavior of the notification message is defined in XAML format by using forms in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], and displayed as a floating popup message using the new hosted control type, `Popup Notification`.</span><span class="sxs-lookup"><span data-stu-id="10546-105">The layout and behavior of the notification message is defined in XAML format by using forms in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], and displayed as a floating popup message using the new hosted control type, `Popup Notification`.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="10546-106">[Popup Notification (Hosted Control)](../unified-service-desk/popup-notification-hosted-control.md)</span><span class="sxs-lookup"><span data-stu-id="10546-106">[Popup Notification (Hosted Control)](../unified-service-desk/popup-notification-hosted-control.md)</span></span>  
  
 <span data-ttu-id="10546-107">Notifications support [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] actions, events, and replacement parameters for you to define popup messages that appear when particular events occur, interact with other hosted controls, and display contextual information from a session.</span><span class="sxs-lookup"><span data-stu-id="10546-107">Notifications support [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] actions, events, and replacement parameters for you to define popup messages that appear when particular events occur, interact with other hosted controls, and display contextual information from a session.</span></span> <span data-ttu-id="10546-108">You can define multiple notifications to appear at the same time.</span><span class="sxs-lookup"><span data-stu-id="10546-108">You can define multiple notifications to appear at the same time.</span></span> <span data-ttu-id="10546-109">You can define the position where the notification can be displayed in the agent application, and the timeout information after which the notification automatically disappears.</span><span class="sxs-lookup"><span data-stu-id="10546-109">You can define the position where the notification can be displayed in the agent application, and the timeout information after which the notification automatically disappears.</span></span>  
  
 <span data-ttu-id="10546-110">Notifications can be global or session-based.</span><span class="sxs-lookup"><span data-stu-id="10546-110">Notifications can be global or session-based.</span></span> <span data-ttu-id="10546-111">Global notifications are displayed outside of a session and will hide only if it times out or is explicitly closed by the user.</span><span class="sxs-lookup"><span data-stu-id="10546-111">Global notifications are displayed outside of a session and will hide only if it times out or is explicitly closed by the user.</span></span> <span data-ttu-id="10546-112">Session-based notifications appear only within a session, and switching to another session will hide the notification.</span><span class="sxs-lookup"><span data-stu-id="10546-112">Session-based notifications appear only within a session, and switching to another session will hide the notification.</span></span> <span data-ttu-id="10546-113">Switching back to the session with notification displays the notification again until it times out or is explicitly closed by the user.</span><span class="sxs-lookup"><span data-stu-id="10546-113">Switching back to the session with notification displays the notification again until it times out or is explicitly closed by the user.</span></span>

<span data-ttu-id="10546-114">You can use the Alt+1 keys (default) to set your focus on a notification.</span><span class="sxs-lookup"><span data-stu-id="10546-114">You can use the Alt+1 keys (default) to set your focus on a notification.</span></span> <span data-ttu-id="10546-115">Nếu có nhiều thông báo hiển thị, bạn có thể ấn Alt+1 lặp lại để di chuyển tuần hoàn qua tất cả các thông báo hiện hoạt trên màn hình.</span><span class="sxs-lookup"><span data-stu-id="10546-115">If there are multiple notifications displayed, you can press Alt+1 repeatedly to cycle through all the active notifications on your screen.</span></span> <span data-ttu-id="10546-116">To change the default keyboard shortcut keys for notifications, use the new **PopupNavigationShortcut** UII option to specify the shortcut keys of your choice.</span><span class="sxs-lookup"><span data-stu-id="10546-116">To change the default keyboard shortcut keys for notifications, use the new **PopupNavigationShortcut** UII option to specify the shortcut keys of your choice.</span></span> <span data-ttu-id="10546-117">More information: [Manage Options for Unified Service Desk](admin/manage-options-unified-service-desk.md)</span><span class="sxs-lookup"><span data-stu-id="10546-117">More information: [Manage Options for Unified Service Desk](admin/manage-options-unified-service-desk.md)</span></span>  
  
<a name="Define"></a>   
## <a name="define-layout-and-behavior-of-notification-using-forms"></a><span data-ttu-id="10546-118">Define layout and behavior of notification using forms</span><span class="sxs-lookup"><span data-stu-id="10546-118">Define layout and behavior of notification using forms</span></span>  
 <span data-ttu-id="10546-119">Use [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] forms to define the layout and behavior of your forms.</span><span class="sxs-lookup"><span data-stu-id="10546-119">Use [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] forms to define the layout and behavior of your forms.</span></span> <span data-ttu-id="10546-120">When you define a new form record (**Settings** > `Unified Service Desk` > **Forms** > **New**), you specify your XAML in the **Markup** field of the form record to define the layout.</span><span class="sxs-lookup"><span data-stu-id="10546-120">When you define a new form record (**Settings** > `Unified Service Desk` > **Forms** > **New**), you specify your XAML in the **Markup** field of the form record to define the layout.</span></span>  
  
 <span data-ttu-id="10546-121">![Create a form using XAML](../unified-service-desk/media/usd-new-form.png "Create a form using XAML")</span><span class="sxs-lookup"><span data-stu-id="10546-121">![Create a form using XAML](../unified-service-desk/media/usd-new-form.png "Create a form using XAML")</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="10546-122">You should have prior knowledge of [!INCLUDE[pn_ms_Windows_Presentation_Foundation](../includes/pn-ms-windows-presentation-foundation.md)] and XAML scripting for defining the layout and behavior of the form.</span><span class="sxs-lookup"><span data-stu-id="10546-122">You should have prior knowledge of [!INCLUDE[pn_ms_Windows_Presentation_Foundation](../includes/pn-ms-windows-presentation-foundation.md)] and XAML scripting for defining the layout and behavior of the form.</span></span>  
  
<a name="CommandBinding"></a>   
### <a name="command-binding-to-execute-uii-actions-action-calls-and-events-from-notification"></a><span data-ttu-id="10546-123">Command binding to execute UII actions, action calls, and events from notification</span><span class="sxs-lookup"><span data-stu-id="10546-123">Command binding to execute UII actions, action calls, and events from notification</span></span>  
 <span data-ttu-id="10546-124">There are custom WPF commands available in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] (Microsoft.Crm.UnifiedServiceDesk.Dynamics assembly) that can be associated to WPF controls such as buttons and hyperlinks in the form XAML to be hosted inside the notification control.</span><span class="sxs-lookup"><span data-stu-id="10546-124">There are custom WPF commands available in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] (Microsoft.Crm.UnifiedServiceDesk.Dynamics assembly) that can be associated to WPF controls such as buttons and hyperlinks in the form XAML to be hosted inside the notification control.</span></span> <span data-ttu-id="10546-125">The commands can be associated to the controls that implement the [ICommandSource](https://msdn.microsoft.com/en-us/library/system.windows.input.icommandsource\(v=vs.110\).aspx) interface.</span><span class="sxs-lookup"><span data-stu-id="10546-125">The commands can be associated to the controls that implement the [ICommandSource](https://msdn.microsoft.com/en-us/library/system.windows.input.icommandsource\(v=vs.110\).aspx) interface.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="10546-126">[Commanding Overview](https://msdn.microsoft.com/en-us/library/ms752308\(v=vs.110\).aspx).</span><span class="sxs-lookup"><span data-stu-id="10546-126">[Commanding Overview](https://msdn.microsoft.com/en-us/library/ms752308\(v=vs.110\).aspx).</span></span>  
  
 <span data-ttu-id="10546-127">The commands can be used to execute actions on any hosted control or fire events from the notification control that hosts the form XAML.</span><span class="sxs-lookup"><span data-stu-id="10546-127">The commands can be used to execute actions on any hosted control or fire events from the notification control that hosts the form XAML.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="10546-128">The command values mentioned below to be specified in the form XAML have the namespace alias as CCA which is to be defined in the root element of the XAML as follows:</span><span class="sxs-lookup"><span data-stu-id="10546-128">The command values mentioned below to be specified in the form XAML have the namespace alias as CCA which is to be defined in the root element of the XAML as follows:</span></span>  
>   
>  `xmlns:CCA="clr-namespace:Microsoft.Crm.UnifiedServiceDesk.Dynamics;assembly=Microsoft.Crm.UnifiedServiceDesk.Dynamics"`  
  
- <span data-ttu-id="10546-129">**UII action**: To execute a UII action from the form XAML, specify the following values for `Command` and `CommandParameter`.</span><span class="sxs-lookup"><span data-stu-id="10546-129">**UII action**: To execute a UII action from the form XAML, specify the following values for `Command` and `CommandParameter`.</span></span>  
  
     `Command`  
     <span data-ttu-id="10546-130">CCA:ActionCommands.DoActionCommand</span><span class="sxs-lookup"><span data-stu-id="10546-130">CCA:ActionCommands.DoActionCommand</span></span>  
  
  <span data-ttu-id="10546-131">**CommandParameter**</span><span class="sxs-lookup"><span data-stu-id="10546-131">**CommandParameter**</span></span>  
     <span data-ttu-id="10546-132">The command parameter must contain the name of the hosted control on which the action is to be executed, the name of the UII action, and the optional action data.</span><span class="sxs-lookup"><span data-stu-id="10546-132">The command parameter must contain the name of the hosted control on which the action is to be executed, the name of the UII action, and the optional action data.</span></span> <span data-ttu-id="10546-133">All these values have to be specified in the following URL format: `http://uii/[HostedControlName]/[UIIActionName]?[ActionData]`.</span><span class="sxs-lookup"><span data-stu-id="10546-133">All these values have to be specified in the following URL format: `http://uii/[HostedControlName]/[UIIActionName]?[ActionData]`.</span></span>  
  
     <span data-ttu-id="10546-134">Note that the different parts of the URL must be encoded if required as per standard guidelines.</span><span class="sxs-lookup"><span data-stu-id="10546-134">Note that the different parts of the URL must be encoded if required as per standard guidelines.</span></span> <span data-ttu-id="10546-135">For example, the space character has to be encoded as “%20” or ‘+’.</span><span class="sxs-lookup"><span data-stu-id="10546-135">For example, the space character has to be encoded as “%20” or ‘+’.</span></span>  
  
  <span data-ttu-id="10546-136">**Ví dụ**</span><span class="sxs-lookup"><span data-stu-id="10546-136">**Example**</span></span>  
     <span data-ttu-id="10546-137">Suppose there is a hosted control named `Contact` of type **CRM Page**, and you want to execute the `Open_CRM_Page` action on this control with the following action data:</span><span class="sxs-lookup"><span data-stu-id="10546-137">Suppose there is a hosted control named `Contact` of type **CRM Page**, and you want to execute the `Open_CRM_Page` action on this control with the following action data:</span></span>  
  
    ```  
    LogicalName=contact  
    id=[[contact.Id]]  
    ```  
  
     <span data-ttu-id="10546-138">Then, you need to pass the following URL as the `CommandParameter` value in your form XAML:</span><span class="sxs-lookup"><span data-stu-id="10546-138">Then, you need to pass the following URL as the `CommandParameter` value in your form XAML:</span></span>  
  
    ```xaml  
    http://uii/Contact/Open_CRM_Page?LogicalName%3Dcontact%0D%0Aid%3D%5B%5Bcontact.Id%5D%5D  
    ```  
  
     <span data-ttu-id="10546-139">Further you can associate the command with a button click in the form XAML as follows:</span><span class="sxs-lookup"><span data-stu-id="10546-139">Further you can associate the command with a button click in the form XAML as follows:</span></span>  
  
    ```xaml  
    <Button Command="CCA:ActionCommands.DoActionCommand"  
    CommandParameter="http://uii/Contact/Open_CRM_Page?LogicalName%3Dcontact%0D%0Aid%3D%5B%5Bcontact.Id%5D%5D"  
    ```  
  
- <span data-ttu-id="10546-140">**Action call**: This serves as an alternative to executing a UII action on a hosted control where you don't want to encode the action data and put it in the XAML.</span><span class="sxs-lookup"><span data-stu-id="10546-140">**Action call**: This serves as an alternative to executing a UII action on a hosted control where you don't want to encode the action data and put it in the XAML.</span></span> <span data-ttu-id="10546-141">To execute an action call from the form XAML, specify the following values for `Command` and `CommandParameter`.</span><span class="sxs-lookup"><span data-stu-id="10546-141">To execute an action call from the form XAML, specify the following values for `Command` and `CommandParameter`.</span></span>  
  
     `Command`  
     <span data-ttu-id="10546-142">CCA:ActionCommands.DoActionCommand</span><span class="sxs-lookup"><span data-stu-id="10546-142">CCA:ActionCommands.DoActionCommand</span></span>  
  
  <span data-ttu-id="10546-143">**CommandParameter**</span><span class="sxs-lookup"><span data-stu-id="10546-143">**CommandParameter**</span></span>  
     <span data-ttu-id="10546-144">The command parameter must contain the name of the action call to be executed, and must be specified in the following URL format: `http://actioncall/[ActionCallName]`.</span><span class="sxs-lookup"><span data-stu-id="10546-144">The command parameter must contain the name of the action call to be executed, and must be specified in the following URL format: `http://actioncall/[ActionCallName]`.</span></span>  
  
     <span data-ttu-id="10546-145">Note that the action call name must be URL encoded if it contains spaces or special characters.</span><span class="sxs-lookup"><span data-stu-id="10546-145">Note that the action call name must be URL encoded if it contains spaces or special characters.</span></span> <span data-ttu-id="10546-146">For example, the space character has to be encoded as “%20” or ‘+’.</span><span class="sxs-lookup"><span data-stu-id="10546-146">For example, the space character has to be encoded as “%20” or ‘+’.</span></span>  
  
  <span data-ttu-id="10546-147">**Ví dụ**</span><span class="sxs-lookup"><span data-stu-id="10546-147">**Example**</span></span>  
     <span data-ttu-id="10546-148">Suppose you want to execute an action call named `Open Contact Page`.</span><span class="sxs-lookup"><span data-stu-id="10546-148">Suppose you want to execute an action call named `Open Contact Page`.</span></span>  
  
     <span data-ttu-id="10546-149">Then, you need to pass the following URL as the `CommandParameter` value in your form XAML:</span><span class="sxs-lookup"><span data-stu-id="10546-149">Then, you need to pass the following URL as the `CommandParameter` value in your form XAML:</span></span>  
  
    ```xaml  
    http://actioncall/Open+Contact+Page  
    ```  
  
- <span data-ttu-id="10546-150">**Event**: To execute an event from the form XAML, specify the following values for `Command` and `CommandParameter`.</span><span class="sxs-lookup"><span data-stu-id="10546-150">**Event**: To execute an event from the form XAML, specify the following values for `Command` and `CommandParameter`.</span></span>  
  
     `Command`  
     <span data-ttu-id="10546-151">CCA:ActionCommands.UIIEvent</span><span class="sxs-lookup"><span data-stu-id="10546-151">CCA:ActionCommands.UIIEvent</span></span>  
  
  <span data-ttu-id="10546-152">**CommandParameter**</span><span class="sxs-lookup"><span data-stu-id="10546-152">**CommandParameter**</span></span>  
     <span data-ttu-id="10546-153">The command parameter must contain the event name optionally followed by a question mark (?) and event parameters in the form of a query string.</span><span class="sxs-lookup"><span data-stu-id="10546-153">The command parameter must contain the event name optionally followed by a question mark (?) and event parameters in the form of a query string.</span></span> <span data-ttu-id="10546-154">Each parameter is specified as a “name = value” pair where both name and value need to be URL encoded if required.</span><span class="sxs-lookup"><span data-stu-id="10546-154">Each parameter is specified as a “name = value” pair where both name and value need to be URL encoded if required.</span></span> <span data-ttu-id="10546-155">Further, parameters must be separated using "&amp;".</span><span class="sxs-lookup"><span data-stu-id="10546-155">Further, parameters must be separated using "&amp;".</span></span>  
  
     <span data-ttu-id="10546-156">Specify the command parameter in the following format: `[EventName]?[Name]=[Value]&amp;[Name]=[Value]`</span><span class="sxs-lookup"><span data-stu-id="10546-156">Specify the command parameter in the following format: `[EventName]?[Name]=[Value]&amp;[Name]=[Value]`</span></span>  
  
  <span data-ttu-id="10546-157">**Ví dụ**</span><span class="sxs-lookup"><span data-stu-id="10546-157">**Example**</span></span>  
     <span data-ttu-id="10546-158">Suppose you want to fire an event named `OK` with following parameters.</span><span class="sxs-lookup"><span data-stu-id="10546-158">Suppose you want to fire an event named `OK` with following parameters.</span></span>  
  
    ```  
    Name1=Value1  
    Name2=My Value  
    ```  
  
     <span data-ttu-id="10546-159">Then, you need to pass the following as the `CommandParameter` value in your form XAML:</span><span class="sxs-lookup"><span data-stu-id="10546-159">Then, you need to pass the following as the `CommandParameter` value in your form XAML:</span></span>  
  
    ```xaml  
    OK?Name1=Value1&amp;Name2=My+Value  
    ```  
  
<a name="Countdown"></a>   
### <a name="display-countdown-timer-in-notifications"></a><span data-ttu-id="10546-160">Display countdown timer in notifications</span><span class="sxs-lookup"><span data-stu-id="10546-160">Display countdown timer in notifications</span></span>  
 <span data-ttu-id="10546-161">You can use the `TimeoutProperty` parameter to display a countdown timer for your notification message until which the message will be displayed.</span><span class="sxs-lookup"><span data-stu-id="10546-161">You can use the `TimeoutProperty` parameter to display a countdown timer for your notification message until which the message will be displayed.</span></span> <span data-ttu-id="10546-162">The timeout value for a notification control is defined when you configure the action to show the control.</span><span class="sxs-lookup"><span data-stu-id="10546-162">The timeout value for a notification control is defined when you configure the action to show the control.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="10546-163">[How to configure a notification?](#HowTo)</span><span class="sxs-lookup"><span data-stu-id="10546-163">[How to configure a notification?](#HowTo)</span></span>  
  
 <span data-ttu-id="10546-164">For example, you can add a label element in form  XAML that is bound to the `TimeoutProperty` parameter to display countdown in seconds after which the notification message will be closed.</span><span class="sxs-lookup"><span data-stu-id="10546-164">For example, you can add a label element in form  XAML that is bound to the `TimeoutProperty` parameter to display countdown in seconds after which the notification message will be closed.</span></span> <span data-ttu-id="10546-165">Ví dụ:</span><span class="sxs-lookup"><span data-stu-id="10546-165">For example:</span></span>  
  
```xaml  
<TextBlock Foreground="White" x:Name="lblElapsedTime" Margin="0,0,9,0"   
           HorizontalAlignment="Right" VerticalAlignment="Center" FontSize="20"   
           Grid.Column="1" Text="{Binding TimeoutProperty}" FontFamily="Calibri" />  
```  

  
### <a name="sample-xaml-for-notification"></a><span data-ttu-id="10546-166">Sample XAML for notification</span><span class="sxs-lookup"><span data-stu-id="10546-166">Sample XAML for notification</span></span>  
 <span data-ttu-id="10546-167">The following sample XAML displays a notification based on the max number of sessions value configured in the replacement parameter for your instance, and displays a notification when you reach the session limit.</span><span class="sxs-lookup"><span data-stu-id="10546-167">The following sample XAML displays a notification based on the max number of sessions value configured in the replacement parameter for your instance, and displays a notification when you reach the session limit.</span></span>  
  
```xaml  
<Border xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"  
        xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"   
xmlns:CCA="clr-namespace:Microsoft.Crm.UnifiedServiceDesk.Dynamics;assembly=Microsoft.Crm.UnifiedServiceDesk.Dynamics"  
BorderBrush="Blue" BorderThickness="1">  
        <Grid Background="AliceBlue" Height="100" Width="400">  
<Grid.Resources>  
 <CCA:CRMImageConverter x:Key="CRMImageLoader" />  
<Style x:Key="ImageLogo" TargetType="{x:Type Image}">  
<Setter Property="Width" Value="16" />   
<Setter Property="Height" Value="16" />   
<!--<Setter Property="Margin" Value="5" /> -->  
</Style>  
    </Grid.Resources>   
            <Grid.RowDefinitions>  
                <RowDefinition Height="75"/>  
                <RowDefinition Height="*"/>  
            </Grid.RowDefinitions>  
            <Grid.ColumnDefinitions>  
            </Grid.ColumnDefinitions>  
            <Grid Grid.Row="0">  
                <Grid.ColumnDefinitions>  
                    <ColumnDefinition Width="50"/>  
                    <ColumnDefinition Width="350"/>  
                </Grid.ColumnDefinitions>  
<Image Style="{DynamicResource ImageLogo}" Source="{Binding Source=msdyusd_Email16, Converter={StaticResource CRMImageLoader}}" Grid.Column="0" />  
                <TextBlock TextWrapping="Wrap" Grid.Column="1" Text="You can have a maximum of [[$Global.maxNumberOfSessions]+] concurrent sessions open. To open a new session, close at least one of the existing ones."/>  
            </Grid>  
            <Grid Background="SkyBlue" Grid.Row="1">  
                <Grid.ColumnDefinitions>  
                    <ColumnDefinition Width="300"/>  
                    <ColumnDefinition Width="100"/>  
                </Grid.ColumnDefinitions>  
                <TextBlock Grid.Column="0">  
                    <Run Text="The notification closes in " />  
                    <Run Text="{Binding TimeoutProperty}" />  
                    <Run Text=" seconds"/>  
                </TextBlock>  
                <Button Height="20" Width="90" Grid.Column="1" Foreground="Black" Command="CCA:ActionCommands.UIIEvent" CommandParameter="Cancel">Close</Button>  
            </Grid>  
        </Grid>  
    </Border>  
```  
  
<a name="Show"></a>   
## <a name="show-notifications-using-popup-notification-control"></a><span data-ttu-id="10546-168">Show notifications using Popup Notification control</span><span class="sxs-lookup"><span data-stu-id="10546-168">Show notifications using Popup Notification control</span></span>  
 <span data-ttu-id="10546-169">Use predefined actions for the `Popup Notification` control to show, hide and close a notification message.</span><span class="sxs-lookup"><span data-stu-id="10546-169">Use predefined actions for the `Popup Notification` control to show, hide and close a notification message.</span></span>  
  
 <span data-ttu-id="10546-170">Using the `Show` action, you can specify the form name to display, the position on the screen where you want the notification message to be displayed, and the time duration for the notification to be displayed.</span><span class="sxs-lookup"><span data-stu-id="10546-170">Using the `Show` action, you can specify the form name to display, the position on the screen where you want the notification message to be displayed, and the time duration for the notification to be displayed.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="10546-171">[Predefined UII Actions](../unified-service-desk/popup-notification-hosted-control.md#Actions).</span><span class="sxs-lookup"><span data-stu-id="10546-171">[Predefined UII Actions](../unified-service-desk/popup-notification-hosted-control.md#Actions).</span></span>

 <span data-ttu-id="10546-172">Use predefined events for the `Popup Notification` control to respond to user actions performed in the notification message as explained earlier.</span><span class="sxs-lookup"><span data-stu-id="10546-172">Use predefined events for the `Popup Notification` control to respond to user actions performed in the notification message as explained earlier.</span></span> <span data-ttu-id="10546-173">You can also add additional actions for an event that gets executed when the event occurs.</span><span class="sxs-lookup"><span data-stu-id="10546-173">You can also add additional actions for an event that gets executed when the event occurs.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="10546-174">[Predefined Events](../unified-service-desk/popup-notification-hosted-control.md#events).</span><span class="sxs-lookup"><span data-stu-id="10546-174">[Predefined Events](../unified-service-desk/popup-notification-hosted-control.md#events).</span></span> 

<a name="Consume"></a>
## <a name="consume-event-parameters-in-the-form-used-for-notifications"></a><span data-ttu-id="10546-175">Consume event parameters in the form used for notifications</span><span class="sxs-lookup"><span data-stu-id="10546-175">Consume event parameters in the form used for notifications</span></span>
<span data-ttu-id="10546-176">The form used in the `Show` action of the Popup Notification control can also consume parameters of the event that triggered the `Show` action call.</span><span class="sxs-lookup"><span data-stu-id="10546-176">The form used in the `Show` action of the Popup Notification control can also consume parameters of the event that triggered the `Show` action call.</span></span>

<span data-ttu-id="10546-177">Action calls in Unified Service Desk can use event parameters as replacement parameters in the action data .</span><span class="sxs-lookup"><span data-stu-id="10546-177">Action calls in Unified Service Desk can use event parameters as replacement parameters in the action data .</span></span> <span data-ttu-id="10546-178">To make some or all of these event parameters available in the form XAML, you can add additional parameters in the `Show` action other than the pre-defined ones.</span><span class="sxs-lookup"><span data-stu-id="10546-178">To make some or all of these event parameters available in the form XAML, you can add additional parameters in the `Show` action other than the pre-defined ones.</span></span> <span data-ttu-id="10546-179">For example, one extra `Show` action parameter can be added as:</span><span class="sxs-lookup"><span data-stu-id="10546-179">For example, one extra `Show` action parameter can be added as:</span></span>
 
<span data-ttu-id="10546-180">`Param1 = [[EventParam1]+]` where `EventParam1` is one of the parameters of the event that triggered the `Show` action call.</span><span class="sxs-lookup"><span data-stu-id="10546-180">`Param1 = [[EventParam1]+]` where `EventParam1` is one of the parameters of the event that triggered the `Show` action call.</span></span>

<span data-ttu-id="10546-181">The added custom parameter can be used in the form XAML as replacement parameter like any other replacement parameter.</span><span class="sxs-lookup"><span data-stu-id="10546-181">The added custom parameter can be used in the form XAML as replacement parameter like any other replacement parameter.</span></span> <span data-ttu-id="10546-182">In the above example, `[[Param1]]` can be used in the form XAML to show some data.</span><span class="sxs-lookup"><span data-stu-id="10546-182">In the above example, `[[Param1]]` can be used in the form XAML to show some data.</span></span> 
  
<a name="Multiple"></a>   
## <a name="multiple-notification-controls"></a><span data-ttu-id="10546-183">Multiple notification controls</span><span class="sxs-lookup"><span data-stu-id="10546-183">Multiple notification controls</span></span>
 
::: moniker range="dynamics-usd-3" 
 <span data-ttu-id="10546-184">You can  configure multiple notification controls and invoke actions independently of each other.</span><span class="sxs-lookup"><span data-stu-id="10546-184">You can  configure multiple notification controls and invoke actions independently of each other.</span></span> <span data-ttu-id="10546-185">When multiple notifications are shown at the same time, all the notifications are visible in the order in which they were invoked.</span><span class="sxs-lookup"><span data-stu-id="10546-185">When multiple notifications are shown at the same time, all the notifications are visible in the order in which they were invoked.</span></span> <span data-ttu-id="10546-186">If two global notifications are configured to be displayed at the same  position, the latest one will overlay on top of the earlier notification.</span><span class="sxs-lookup"><span data-stu-id="10546-186">If two global notifications are configured to be displayed at the same  position, the latest one will overlay on top of the earlier notification.</span></span> <span data-ttu-id="10546-187">Similarly, if a global and session-based notifications or multiple session-based notifications are  configured to be displayed at the same  position in a session, the latest one will overlay on top of the earlier notification in the session.</span><span class="sxs-lookup"><span data-stu-id="10546-187">Similarly, if a global and session-based notifications or multiple session-based notifications are  configured to be displayed at the same  position in a session, the latest one will overlay on top of the earlier notification in the session.</span></span>
::: moniker-end

::: moniker range=">=dynamics-usd-4" 
 <span data-ttu-id="10546-188">You can  configure multiple notification controls and invoke actions independently of each other.</span><span class="sxs-lookup"><span data-stu-id="10546-188">You can  configure multiple notification controls and invoke actions independently of each other.</span></span> <span data-ttu-id="10546-189"><!--When multiple notifications are shown at the same time, all the notifications are visible in the order in which they were invoked.--> If two global notifications are configured to be displayed at the same  position, the latest one will overlay on top of the earlier notification.</span><span class="sxs-lookup"><span data-stu-id="10546-189"><!--When multiple notifications are shown at the same time, all the notifications are visible in the order in which they were invoked.--> If two global notifications are configured to be displayed at the same  position, the latest one will overlay on top of the earlier notification.</span></span> <span data-ttu-id="10546-190">Similarly, if a global and session-based notifications or multiple session-based notifications are  configured to be displayed at the same  position in a session, the latest one will overlay on top of the earlier notification in the session.</span><span class="sxs-lookup"><span data-stu-id="10546-190">Similarly, if a global and session-based notifications or multiple session-based notifications are  configured to be displayed at the same  position in a session, the latest one will overlay on top of the earlier notification in the session.</span></span>
::: moniker-end

::: moniker range=">=dynamics-usd-4"
 ### <a name="stack-notifications"></a><span data-ttu-id="10546-191">Stack notifications</span><span class="sxs-lookup"><span data-stu-id="10546-191">Stack notifications</span></span>

 <span data-ttu-id="10546-192">You can also configure the stack notification by adding the **stack** parameter in the **Data** field of **Show** action.</span><span class="sxs-lookup"><span data-stu-id="10546-192">You can also configure the stack notification by adding the **stack** parameter in the **Data** field of **Show** action.</span></span> <span data-ttu-id="10546-193">The parameter takes a Boolean value.</span><span class="sxs-lookup"><span data-stu-id="10546-193">The parameter takes a Boolean value.</span></span> <span data-ttu-id="10546-194">Unified Service Desk shows the notifications in stack when the parameter is set to **true**.</span><span class="sxs-lookup"><span data-stu-id="10546-194">Unified Service Desk shows the notifications in stack when the parameter is set to **true**.</span></span> <span data-ttu-id="10546-195">The default value is **false**.</span><span class="sxs-lookup"><span data-stu-id="10546-195">The default value is **false**.</span></span> <span data-ttu-id="10546-196">If you do not specify any value, the default value (false) is passed.</span><span class="sxs-lookup"><span data-stu-id="10546-196">If you do not specify any value, the default value (false) is passed.</span></span> <span data-ttu-id="10546-197">For example, **stack = true**, shows the notifications in stack.</span><span class="sxs-lookup"><span data-stu-id="10546-197">For example, **stack = true**, shows the notifications in stack.</span></span>

 <span data-ttu-id="10546-198">Also, you can define the height of the stack by defining the **stackHeight** parameter.</span><span class="sxs-lookup"><span data-stu-id="10546-198">Also, you can define the height of the stack by defining the **stackHeight** parameter.</span></span> <span data-ttu-id="10546-199">The value range is 1 - 100.</span><span class="sxs-lookup"><span data-stu-id="10546-199">The value range is 1 - 100.</span></span> <span data-ttu-id="10546-200">Giá trị mặc định là 50.</span><span class="sxs-lookup"><span data-stu-id="10546-200">The default value is 50.</span></span> <span data-ttu-id="10546-201">If you do not specify any value, the default value (50) is passed.</span><span class="sxs-lookup"><span data-stu-id="10546-201">If you do not specify any value, the default value (50) is passed.</span></span> <span data-ttu-id="10546-202">Also, if you specify 0 or specify more than 100, default value (50) is passed.</span><span class="sxs-lookup"><span data-stu-id="10546-202">Also, if you specify 0 or specify more than 100, default value (50) is passed.</span></span> <span data-ttu-id="10546-203">For example, **stackHeight = 60**.</span><span class="sxs-lookup"><span data-stu-id="10546-203">For example, **stackHeight = 60**.</span></span>

 <span data-ttu-id="10546-204">For more information about the parameters, see  [Popup Notification (Hosted Control)](../unified-service-desk/popup-notification-hosted-control.md).</span><span class="sxs-lookup"><span data-stu-id="10546-204">For more information about the parameters, see  [Popup Notification (Hosted Control)](../unified-service-desk/popup-notification-hosted-control.md).</span></span>

 <span data-ttu-id="10546-205">The order of the notification in the stack is top to bottom, where the newest notification appears at the bottom.</span><span class="sxs-lookup"><span data-stu-id="10546-205">The order of the notification in the stack is top to bottom, where the newest notification appears at the bottom.</span></span> <span data-ttu-id="10546-206">A maximum of five stack notification can be displayed at any given point.</span><span class="sxs-lookup"><span data-stu-id="10546-206">A maximum of five stack notification can be displayed at any given point.</span></span>

 > [!Note]
 > <span data-ttu-id="10546-207">When there are more than 5 notifications, the new notification overlays the recently shown notification.</span><span class="sxs-lookup"><span data-stu-id="10546-207">When there are more than 5 notifications, the new notification overlays the recently shown notification.</span></span></br> <span data-ttu-id="10546-208">For example, you see 5 notifications in stack.</span><span class="sxs-lookup"><span data-stu-id="10546-208">For example, you see 5 notifications in stack.</span></span> <span data-ttu-id="10546-209">Now, 6th notification is incoming, then the 6th notification overlays the 5th notification.</span><span class="sxs-lookup"><span data-stu-id="10546-209">Now, 6th notification is incoming, then the 6th notification overlays the 5th notification.</span></span> <span data-ttu-id="10546-210">Similarly, when the 7th notification is incoming, it overlays the 6th notification.</span><span class="sxs-lookup"><span data-stu-id="10546-210">Similarly, when the 7th notification is incoming, it overlays the 6th notification.</span></span><br/>
 <span data-ttu-id="10546-211">![New notification replacing the recent notification in the stack](../unified-service-desk/media/stack-notification.PNG "New notification replacing the recent notification in the stack")</span><span class="sxs-lookup"><span data-stu-id="10546-211">![New notification replacing the recent notification in the stack](../unified-service-desk/media/stack-notification.PNG "New notification replacing the recent notification in the stack")</span></span>
::: moniker-end

::: moniker range="dynamics-usd-3"  
<a name="HowTo"></a>   
## <a name="how-to-configure-a-notification"></a><span data-ttu-id="10546-212">How to configure a notification?</span><span class="sxs-lookup"><span data-stu-id="10546-212">How to configure a notification?</span></span>  
 <span data-ttu-id="10546-213">These are the broad steps for displaying a notification:</span><span class="sxs-lookup"><span data-stu-id="10546-213">These are the broad steps for displaying a notification:</span></span>  
  
1. <span data-ttu-id="10546-214">Create a **Form** record with your notification definition (XAML).</span><span class="sxs-lookup"><span data-stu-id="10546-214">Create a **Form** record with your notification definition (XAML).</span></span> <span data-ttu-id="10546-215">For example, create a form with the example XAML illustrated earlier and with the following name: `MaxSessionNotificationForm`.</span><span class="sxs-lookup"><span data-stu-id="10546-215">For example, create a form with the example XAML illustrated earlier and with the following name: `MaxSessionNotificationForm`.</span></span>  
  
2. <span data-ttu-id="10546-216">Create a `Popup Notification` control, and keep it global.</span><span class="sxs-lookup"><span data-stu-id="10546-216">Create a `Popup Notification` control, and keep it global.</span></span> <span data-ttu-id="10546-217">For example, create a control with the following name: `MaxSessionNotificationControl`.</span><span class="sxs-lookup"><span data-stu-id="10546-217">For example, create a control with the following name: `MaxSessionNotificationControl`.</span></span>  
  
3. <span data-ttu-id="10546-218">Create an action call to display the notification by specifying the form name to display along with other parameters in the **Data** field of the `Show` action.</span><span class="sxs-lookup"><span data-stu-id="10546-218">Create an action call to display the notification by specifying the form name to display along with other parameters in the **Data** field of the `Show` action.</span></span> <span data-ttu-id="10546-219">For example,  create an action call with the following name: `Action Call for Max Sessions Notification`:</span><span class="sxs-lookup"><span data-stu-id="10546-219">For example,  create an action call with the following name: `Action Call for Max Sessions Notification`:</span></span>  
  
   <span data-ttu-id="10546-220">![Action Call for displaying notification](../unified-service-desk/media/usd-action-call-notification.png "Action Call for displaying notification")</span><span class="sxs-lookup"><span data-stu-id="10546-220">![Action Call for displaying notification](../unified-service-desk/media/usd-action-call-notification.png "Action Call for displaying notification")</span></span>  
  
4. <span data-ttu-id="10546-221">Finally, add the action call to an event to execute the action.</span><span class="sxs-lookup"><span data-stu-id="10546-221">Finally, add the action call to an event to execute the action.</span></span> <span data-ttu-id="10546-222">As we are checking for maximum number of sessions on the creation of a new session to show the notification, add the action call to the `SessionNew` event of the [Global Manager (Hosted Control)](../unified-service-desk/global-manager-hosted-control.md).</span><span class="sxs-lookup"><span data-stu-id="10546-222">As we are checking for maximum number of sessions on the creation of a new session to show the notification, add the action call to the `SessionNew` event of the [Global Manager (Hosted Control)](../unified-service-desk/global-manager-hosted-control.md).</span></span> 
::: moniker-end

::: moniker range=">=dynamics-usd-4"  
<a name="HowTo"></a>   
## <a name="how-to-configure-a-notification"></a><span data-ttu-id="10546-223">How to configure a notification?</span><span class="sxs-lookup"><span data-stu-id="10546-223">How to configure a notification?</span></span>  
 <span data-ttu-id="10546-224">These are the broad steps for displaying a notification:</span><span class="sxs-lookup"><span data-stu-id="10546-224">These are the broad steps for displaying a notification:</span></span>  
  
1. <span data-ttu-id="10546-225">Create a **Form** record with your notification definition (XAML).</span><span class="sxs-lookup"><span data-stu-id="10546-225">Create a **Form** record with your notification definition (XAML).</span></span> <span data-ttu-id="10546-226">For example, create a form with the example XAML illustrated earlier and with the following name: `Sample Notification Form`.</span><span class="sxs-lookup"><span data-stu-id="10546-226">For example, create a form with the example XAML illustrated earlier and with the following name: `Sample Notification Form`.</span></span>  
  
2. <span data-ttu-id="10546-227">Create a `Popup Notification` control, and keep it global.</span><span class="sxs-lookup"><span data-stu-id="10546-227">Create a `Popup Notification` control, and keep it global.</span></span> <span data-ttu-id="10546-228">For example, create a control with the following name: `MaxSessionNotificationControl`.</span><span class="sxs-lookup"><span data-stu-id="10546-228">For example, create a control with the following name: `MaxSessionNotificationControl`.</span></span>

    <span data-ttu-id="10546-229">![Hosted control with USD Component type as Popup Notification](../unified-service-desk/media/usd-popupnotification-hosted-control.PNG "Hosted control with USD Component type as Popup Notification")</span><span class="sxs-lookup"><span data-stu-id="10546-229">![Hosted control with USD Component type as Popup Notification](../unified-service-desk/media/usd-popupnotification-hosted-control.PNG "Hosted control with USD Component type as Popup Notification")</span></span>
  
3. <span data-ttu-id="10546-230">Create an action call to display the notification.</span><span class="sxs-lookup"><span data-stu-id="10546-230">Create an action call to display the notification.</span></span></br> <span data-ttu-id="10546-231">For example, create an action call and specify the following:</span><span class="sxs-lookup"><span data-stu-id="10546-231">For example, create an action call and specify the following:</span></span> 

    |<span data-ttu-id="10546-232">Trường</span><span class="sxs-lookup"><span data-stu-id="10546-232">Field</span></span>|<span data-ttu-id="10546-233">Value</span><span class="sxs-lookup"><span data-stu-id="10546-233">Value</span></span>|
    |--------|--------|
    |<span data-ttu-id="10546-234">Tên</span><span class="sxs-lookup"><span data-stu-id="10546-234">Name</span></span>|<span data-ttu-id="10546-235">Action Call for Max Sessions Notifications</span><span class="sxs-lookup"><span data-stu-id="10546-235">Action Call for Max Sessions Notifications</span></span>|
    |<span data-ttu-id="10546-236">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="10546-236">Hosted Control</span></span>|<span data-ttu-id="10546-237">MaxSessionNotificationControl</span><span class="sxs-lookup"><span data-stu-id="10546-237">MaxSessionNotificationControl</span></span>|
    |<span data-ttu-id="10546-238">Hành động</span><span class="sxs-lookup"><span data-stu-id="10546-238">Action</span></span>|<span data-ttu-id="10546-239">Show</span><span class="sxs-lookup"><span data-stu-id="10546-239">Show</span></span>|
    |<span data-ttu-id="10546-240">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="10546-240">Data</span></span>|<span data-ttu-id="10546-241">formName = Sample Notification Form</span><span class="sxs-lookup"><span data-stu-id="10546-241">formName = Sample Notification Form</span></span></br><span data-ttu-id="10546-242">top = 10</span><span class="sxs-lookup"><span data-stu-id="10546-242">top = 10</span></span></br><span data-ttu-id="10546-243">left = 80</span><span class="sxs-lookup"><span data-stu-id="10546-243">left = 80</span></span></br><span data-ttu-id="10546-244">timeout = 20</span><span class="sxs-lookup"><span data-stu-id="10546-244">timeout = 20</span></span></br><span data-ttu-id="10546-245">stack = true</span><span class="sxs-lookup"><span data-stu-id="10546-245">stack = true</span></span></br><span data-ttu-id="10546-246">stackHeight = 60</span><span class="sxs-lookup"><span data-stu-id="10546-246">stackHeight = 60</span></span>
  
   <span data-ttu-id="10546-247">![Action Call for displaying notification](../unified-service-desk/media/usd-action-call-notification.png "Action Call for displaying notification")</span><span class="sxs-lookup"><span data-stu-id="10546-247">![Action Call for displaying notification](../unified-service-desk/media/usd-action-call-notification.png "Action Call for displaying notification")</span></span>  
  
4. <span data-ttu-id="10546-248">Finally, add the action call to an event to execute the action.</span><span class="sxs-lookup"><span data-stu-id="10546-248">Finally, add the action call to an event to execute the action.</span></span> </br>
<span data-ttu-id="10546-249">As we are checking for maximum number of sessions on the creation of a new session to show the notification, add the action call to the `SessionNew` event of the [Global Manager (Hosted Control)](../unified-service-desk/global-manager-hosted-control.md).</span><span class="sxs-lookup"><span data-stu-id="10546-249">As we are checking for maximum number of sessions on the creation of a new session to show the notification, add the action call to the `SessionNew` event of the [Global Manager (Hosted Control)](../unified-service-desk/global-manager-hosted-control.md).</span></span> </br>

    <span data-ttu-id="10546-250">a.</span><span class="sxs-lookup"><span data-stu-id="10546-250">a.</span></span> <span data-ttu-id="10546-251">Go to **Unified Service Desk** > **Events**.</span><span class="sxs-lookup"><span data-stu-id="10546-251">Go to **Unified Service Desk** > **Events**.</span></span></br>
    <span data-ttu-id="10546-252">b.</span><span class="sxs-lookup"><span data-stu-id="10546-252">b.</span></span> <span data-ttu-id="10546-253">Select **SessionNew** from the list.</span><span class="sxs-lookup"><span data-stu-id="10546-253">Select **SessionNew** from the list.</span></span></br>
    <span data-ttu-id="10546-254">c.</span><span class="sxs-lookup"><span data-stu-id="10546-254">c.</span></span> <span data-ttu-id="10546-255">On the **SessionNew** event page, under the **Active Actions** area, click **+** to add action calls.</span><span class="sxs-lookup"><span data-stu-id="10546-255">On the **SessionNew** event page, under the **Active Actions** area, click **+** to add action calls.</span></span></br>
    <span data-ttu-id="10546-256">d.</span><span class="sxs-lookup"><span data-stu-id="10546-256">d.</span></span> <span data-ttu-id="10546-257">In the search box, type **Action Call for Max Sessions Notifications** and select search icon.</span><span class="sxs-lookup"><span data-stu-id="10546-257">In the search box, type **Action Call for Max Sessions Notifications** and select search icon.</span></span> <span data-ttu-id="10546-258">The result appears.</span><span class="sxs-lookup"><span data-stu-id="10546-258">The result appears.</span></span>
   <span data-ttu-id="10546-259">e.</span><span class="sxs-lookup"><span data-stu-id="10546-259">e.</span></span> <span data-ttu-id="10546-260">Select the **Action Call for Max Sessions Notifications**, and select **Save**.</span><span class="sxs-lookup"><span data-stu-id="10546-260">Select the **Action Call for Max Sessions Notifications**, and select **Save**.</span></span></br>
    <span data-ttu-id="10546-261">![Add the action Call to the SessionNew event for displaying notification](../unified-service-desk/media/usd-add-action-call-sessionnew-event.PNG "Add the action Call to the SessionNew event for displaying notification")</span><span class="sxs-lookup"><span data-stu-id="10546-261">![Add the action Call to the SessionNew event for displaying notification](../unified-service-desk/media/usd-add-action-call-sessionnew-event.PNG "Add the action Call to the SessionNew event for displaying notification")</span></span>  
::: moniker-end

### <a name="see-also"></a><span data-ttu-id="10546-262">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="10546-262">See also</span></span>  
 <span data-ttu-id="10546-263">[Popup Notification (Hosted Control)](../unified-service-desk/popup-notification-hosted-control.md) </span><span class="sxs-lookup"><span data-stu-id="10546-263">[Popup Notification (Hosted Control)](../unified-service-desk/popup-notification-hosted-control.md) </span></span>  
 <span data-ttu-id="10546-264">[Thêm cuộc gọi hành động vào một sự kiện](../unified-service-desk/add-action-calls-event.md) </span><span class="sxs-lookup"><span data-stu-id="10546-264">[Add action calls to an event](../unified-service-desk/add-action-calls-event.md) </span></span>  
 [<span data-ttu-id="10546-265">Bắt đầu với cấu hình ứng dụng tổng đài viên của bạn</span><span class="sxs-lookup"><span data-stu-id="10546-265">Get started with configuring your agent application</span></span>](../unified-service-desk/get-started-configuring-agent-application.md)
