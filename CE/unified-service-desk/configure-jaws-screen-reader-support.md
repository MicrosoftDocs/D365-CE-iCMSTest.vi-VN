---
title: Configure JAWS screen reader for Unified Service Desk | MicrosoftDocs
description: Learn about JAWS screen reader for Windows screen reader for speech output in the Unified Service Desk client. All the Unified Service Desk controls and custom controls that are part of the Microsoft Dynamics 365 for Customer Engagement apps Web Client package  are JAWS compliant.
ms.custom:
- dyn365-a11y
- dyn365-USD
keywords: Dynamics 365 for Customer Engagement apps Unified Service Desk; Unified Service Desk; JAWS Screen Reader; Windows Screen Reader
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
ms.assetid: D9FE67A6-2E02-48DF-B9C2-4250433D72BE
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: d414866e93339d5e20f95763e620cc46a2c43643
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388058"
---
# <a name="configure-jaws-screen-reader-for-unified-service-desk"></a><span data-ttu-id="7d47d-105">Configure JAWS Screen Reader for Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="7d47d-105">Configure JAWS Screen Reader for Unified Service Desk</span></span>

[!INCLUDE[pn-jaws](../includes/pn-jaws.md)] <span data-ttu-id="7d47d-106">(Job Access With Speech) is a computer screen reader program for Microsoft Windows that allows blind and visually impaired users to read the screen either with a text-to-speech output or by a refreshable Braille display.</span><span class="sxs-lookup"><span data-stu-id="7d47d-106">(Job Access With Speech) is a computer screen reader program for Microsoft Windows that allows blind and visually impaired users to read the screen either with a text-to-speech output or by a refreshable Braille display.</span></span>

[!INCLUDE[pn-unified-service-desk](../includes/pn-unified-service-desk.md)] <span data-ttu-id="7d47d-107">supports [!INCLUDE[pn-jaws](../includes/pn-jaws.md)] version 18 for Windows screen reader for speech output in the [!INCLUDE[pn-unified-service-desk](../includes/pn-unified-service-desk.md)] client.</span><span class="sxs-lookup"><span data-stu-id="7d47d-107">supports [!INCLUDE[pn-jaws](../includes/pn-jaws.md)] version 18 for Windows screen reader for speech output in the [!INCLUDE[pn-unified-service-desk](../includes/pn-unified-service-desk.md)] client.</span></span> <span data-ttu-id="7d47d-108">All the [!INCLUDE[pn-unified-service-desk](../includes/pn-unified-service-desk.md)] controls and custom controls that are part of the Microsoft Dynamics 365 for Customer Engagement apps Web Client package  are JAWS compliant.</span><span class="sxs-lookup"><span data-stu-id="7d47d-108">All the [!INCLUDE[pn-unified-service-desk](../includes/pn-unified-service-desk.md)] controls and custom controls that are part of the Microsoft Dynamics 365 for Customer Engagement apps Web Client package  are JAWS compliant.</span></span> <span data-ttu-id="7d47d-109">For the custom controls that you develop as part of the solution package, you need to define the necessary properties to make the controls JAWS compliant.</span><span class="sxs-lookup"><span data-stu-id="7d47d-109">For the custom controls that you develop as part of the solution package, you need to define the necessary properties to make the controls JAWS compliant.</span></span>

## <a name="jaws-support-for-focusable-controls-interactive-controls"></a><span data-ttu-id="7d47d-110">JAWS support for focusable controls (Interactive controls)</span><span class="sxs-lookup"><span data-stu-id="7d47d-110">JAWS support for focusable controls (Interactive controls)</span></span>
<span data-ttu-id="7d47d-111">You can configure [!INCLUDE[pn-jaws](../includes/pn-jaws.md)] screen reader support for controls that are focusable (Interactive controls), such as buttons, list box, menu, radio button, and check box.</span><span class="sxs-lookup"><span data-stu-id="7d47d-111">You can configure [!INCLUDE[pn-jaws](../includes/pn-jaws.md)] screen reader support for controls that are focusable (Interactive controls), such as buttons, list box, menu, radio button, and check box.</span></span>

<span data-ttu-id="7d47d-112">For [!INCLUDE[pn-jaws](../includes/pn-jaws.md)] screen reader to read a focusable control, you must specify a value for the [AutomationProperties.Name Attached Property](https://msdn.microsoft.com/en-us/library/system.windows.automation.automationproperties.name(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="7d47d-112">For [!INCLUDE[pn-jaws](../includes/pn-jaws.md)] screen reader to read a focusable control, you must specify a value for the [AutomationProperties.Name Attached Property](https://msdn.microsoft.com/en-us/library/system.windows.automation.automationproperties.name(v=vs.110).aspx).</span></span> 

<span data-ttu-id="7d47d-113">Ví dụ:</span><span class="sxs-lookup"><span data-stu-id="7d47d-113">For example:</span></span>

```<Button Width="30" Height="30" Name="Save" ToolTip="Click to save the doc." AutomationProperties.Name="Save" Focusable="True" IsTabStop="True">```

## <a name="jaws-support-for-tooltip"></a><span data-ttu-id="7d47d-114">JAWS support for tooltip</span><span class="sxs-lookup"><span data-stu-id="7d47d-114">JAWS support for tooltip</span></span>

<span data-ttu-id="7d47d-115">By default, [!INCLUDE[pn-jaws](../includes/pn-jaws.md)] screen reader does not support reading toolbar button tooltip text.</span><span class="sxs-lookup"><span data-stu-id="7d47d-115">By default, [!INCLUDE[pn-jaws](../includes/pn-jaws.md)] screen reader does not support reading toolbar button tooltip text.</span></span> <span data-ttu-id="7d47d-116">However, you can create [!INCLUDE[pn-jaws](../includes/pn-jaws.md)] custom scripts to enable [!INCLUDE[pn-jaws](../includes/pn-jaws.md)] screen reader to read tooltip text.</span><span class="sxs-lookup"><span data-stu-id="7d47d-116">However, you can create [!INCLUDE[pn-jaws](../includes/pn-jaws.md)] custom scripts to enable [!INCLUDE[pn-jaws](../includes/pn-jaws.md)] screen reader to read tooltip text.</span></span>

<span data-ttu-id="7d47d-117">Here is a sample script for checking button name and tooltip text (help text).</span><span class="sxs-lookup"><span data-stu-id="7d47d-117">Here is a sample script for checking button name and tooltip text (help text).</span></span> <span data-ttu-id="7d47d-118">In [!INCLUDE[pn-unified-service-desk](../includes/pn-unified-service-desk.md)], if you do not configure the tooltip text explicitly, the system applies the button name to the tooltip text.</span><span class="sxs-lookup"><span data-stu-id="7d47d-118">In [!INCLUDE[pn-unified-service-desk](../includes/pn-unified-service-desk.md)], if you do not configure the tooltip text explicitly, the system applies the button name to the tooltip text.</span></span> <span data-ttu-id="7d47d-119">In such case, [!INCLUDE[pn-jaws](../includes/pn-jaws.md)] read both the button name and the tooltip text.</span><span class="sxs-lookup"><span data-stu-id="7d47d-119">In such case, [!INCLUDE[pn-jaws](../includes/pn-jaws.md)] read both the button name and the tooltip text.</span></span> <span data-ttu-id="7d47d-120">To avoid reading the button name and tooltip text, you can create a custom script to check whether the button name and tooltip text is same.</span><span class="sxs-lookup"><span data-stu-id="7d47d-120">To avoid reading the button name and tooltip text, you can create a custom script to check whether the button name and tooltip text is same.</span></span>

<span data-ttu-id="7d47d-121">In the sample script, if the help text is not the same as button name, [!INCLUDE[pn-jaws](../includes/pn-jaws.md)] screen reader reads the tooltip (help text).</span><span class="sxs-lookup"><span data-stu-id="7d47d-121">In the sample script, if the help text is not the same as button name, [!INCLUDE[pn-jaws](../includes/pn-jaws.md)] screen reader reads the tooltip (help text).</span></span>

```
include "hjConst.jsh"
void function SayObjectTypeAndText(int nLevel)
SayObjectTypeAndText(nLevel)
if nLevel == 0
   var string sHelp = GetObjectHelp()
   var string objName = GetObjectName()
   if sHelp && sHelp != objName // If help text is not equal to the object name, the JAWS screen reads the help text
      Say(sHelp,ot_help)
   endIf
endIf
EndFunction
```
<span data-ttu-id="7d47d-122">In the example image, the button name and the tooltip text is same: **REMINDER**.</span><span class="sxs-lookup"><span data-stu-id="7d47d-122">In the example image, the button name and the tooltip text is same: **REMINDER**.</span></span> <span data-ttu-id="7d47d-123">In this scenario, the script checks for the button name and tooltip text, which is different and hence, [!INCLUDE[pn-jaws](../includes/pn-jaws.md)] does not read the tooltip text.</span><span class="sxs-lookup"><span data-stu-id="7d47d-123">In this scenario, the script checks for the button name and tooltip text, which is different and hence, [!INCLUDE[pn-jaws](../includes/pn-jaws.md)] does not read the tooltip text.</span></span>

<span data-ttu-id="7d47d-124">![Unified Service Desk button with same tootip](media/usd-reminder-button-reminder-tootip.png "Unified Service Desk button with same tootip")</span><span class="sxs-lookup"><span data-stu-id="7d47d-124">![Unified Service Desk button with same tootip](media/usd-reminder-button-reminder-tootip.png "Unified Service Desk button with same tootip")</span></span>

<span data-ttu-id="7d47d-125">In the example image, the **REMINDER** button name is different than the tooltip text: **SET REMINDER**.</span><span class="sxs-lookup"><span data-stu-id="7d47d-125">In the example image, the **REMINDER** button name is different than the tooltip text: **SET REMINDER**.</span></span> <span data-ttu-id="7d47d-126">In this scenario, the [!INCLUDE[pn-jaws](../includes/pn-jaws.md)] screen reads the tooltip text.</span><span class="sxs-lookup"><span data-stu-id="7d47d-126">In this scenario, the [!INCLUDE[pn-jaws](../includes/pn-jaws.md)] screen reads the tooltip text.</span></span>

<span data-ttu-id="7d47d-127">![Unified Service Desk button with differnt tootip](media/usd-reminder-button-setreminder-tootip.png "Unified Service Desk button with differnt tootip")</span><span class="sxs-lookup"><span data-stu-id="7d47d-127">![Unified Service Desk button with differnt tootip](media/usd-reminder-button-setreminder-tootip.png "Unified Service Desk button with differnt tootip")</span></span>

<span data-ttu-id="7d47d-128">You can write script for your application in [!INCLUDE[pn-jaws](../includes/pn-jaws.md)].</span><span class="sxs-lookup"><span data-stu-id="7d47d-128">You can write script for your application in [!INCLUDE[pn-jaws](../includes/pn-jaws.md)].</span></span> <span data-ttu-id="7d47d-129">For more information about writing scripts, see [Basics of Scripting Manual](http://www.freedomscientific.com/Content/Documents/Other/ScriptManual/01-0_Introduction.htm).</span><span class="sxs-lookup"><span data-stu-id="7d47d-129">For more information about writing scripts, see [Basics of Scripting Manual](http://www.freedomscientific.com/Content/Documents/Other/ScriptManual/01-0_Introduction.htm).</span></span>

<span data-ttu-id="7d47d-130">After you write the script, name the file as per the product name (example: UnifiedServiceDesk.jss).</span><span class="sxs-lookup"><span data-stu-id="7d47d-130">After you write the script, name the file as per the product name (example: UnifiedServiceDesk.jss).</span></span> <span data-ttu-id="7d47d-131">These are called application script file, and must be saved in either the [!INCLUDE[pn-jaws](../includes/pn-jaws.md)] shared or user settings folder in order to be loaded with the application at run-time.</span><span class="sxs-lookup"><span data-stu-id="7d47d-131">These are called application script file, and must be saved in either the [!INCLUDE[pn-jaws](../includes/pn-jaws.md)] shared or user settings folder in order to be loaded with the application at run-time.</span></span> <span data-ttu-id="7d47d-132">More information: [JAWS Scripts and Script Files](http://www.freedomscientific.com/Content/Documents/Other/ScriptManual/03-1_JAWSScriptsAndScriptFiles.htm).</span><span class="sxs-lookup"><span data-stu-id="7d47d-132">More information: [JAWS Scripts and Script Files](http://www.freedomscientific.com/Content/Documents/Other/ScriptManual/03-1_JAWSScriptsAndScriptFiles.htm).</span></span>

## <a name="jaws-support-for-non-focusable-controls-non-interactive-controls"></a><span data-ttu-id="7d47d-133">JAWS support for non-focusable controls (Non-Interactive controls)</span><span class="sxs-lookup"><span data-stu-id="7d47d-133">JAWS support for non-focusable controls (Non-Interactive controls)</span></span>

<span data-ttu-id="7d47d-134">By design of the product, the tab position does not focus the non-focusable controls (Non-interactive controls).</span><span class="sxs-lookup"><span data-stu-id="7d47d-134">By design of the product, the tab position does not focus the non-focusable controls (Non-interactive controls).</span></span> <span data-ttu-id="7d47d-135">Hence, [!INCLUDE[pn-jaws](../includes/pn-jaws.md)] screen reader does not read controls that are non-focusable, such as text block, image, and labels.</span><span class="sxs-lookup"><span data-stu-id="7d47d-135">Hence, [!INCLUDE[pn-jaws](../includes/pn-jaws.md)] screen reader does not read controls that are non-focusable, such as text block, image, and labels.</span></span>

### <a name="workaround"></a><span data-ttu-id="7d47d-136">Giải pháp thay thế</span><span class="sxs-lookup"><span data-stu-id="7d47d-136">Workaround</span></span>

<span data-ttu-id="7d47d-137">One of the ways to enable [!INCLUDE[pn-jaws](../includes/pn-jaws.md)] screen reader to read the non-focusable controls is to wrap the non-focusable control using the **UserControl** element, which enables the JAWS to read the non-focusable controls.</span><span class="sxs-lookup"><span data-stu-id="7d47d-137">One of the ways to enable [!INCLUDE[pn-jaws](../includes/pn-jaws.md)] screen reader to read the non-focusable controls is to wrap the non-focusable control using the **UserControl** element, which enables the JAWS to read the non-focusable controls.</span></span> 

> [!NOTE]
> <span data-ttu-id="7d47d-138">This method of enabling [!INCLUDE[pn-jaws](../includes/pn-jaws.md)] screen reader support for non-focusable controls is just a workaround, and not the officially recommended way.</span><span class="sxs-lookup"><span data-stu-id="7d47d-138">This method of enabling [!INCLUDE[pn-jaws](../includes/pn-jaws.md)] screen reader support for non-focusable controls is just a workaround, and not the officially recommended way.</span></span>

<span data-ttu-id="7d47d-139">When [!INCLUDE[pn-jaws](../includes/pn-jaws.md)] reader lands on the first focusable control, reads the non-focusable controls and then reads the focusable controls.</span><span class="sxs-lookup"><span data-stu-id="7d47d-139">When [!INCLUDE[pn-jaws](../includes/pn-jaws.md)] reader lands on the first focusable control, reads the non-focusable controls and then reads the focusable controls.</span></span>

<span data-ttu-id="7d47d-140">The XAML example for Session Overview control displays you the **UserControl** wrapping of the grid.</span><span class="sxs-lookup"><span data-stu-id="7d47d-140">The XAML example for Session Overview control displays you the **UserControl** wrapping of the grid.</span></span>
```
<TabControl xmlns:controlStyles="clr-namespace:Microsoft.Crm.UnifiedServiceDesk.Dynamics.Controls.Styles;assembly=Microsoft.Crm.UnifiedServiceDesk.Dynamics">
    <controlStyles:USDTab Header="General">
<UserControl>
        <Grid Margin="0"
          xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
          xmlns:CCA="clr-namespace:Microsoft.Crm.UnifiedServiceDesk.Dynamics;assembly=Microsoft.Crm.UnifiedServiceDesk.Dynamics">
<Grid.Resources>
<CCA:CRMImageConverter x:Key="CRMImageLoader" />
<Style x:Key="ImageLogo" TargetType="{x:Type Image}">
<Setter Property="Width" Value="16" /> 
<Setter Property="Height" Value="16" /> 
<!--<Setter Property="Margin" Value="5" /> -->
</Style>
    </Grid.Resources>            
<Grid.RowDefinitions>
                <RowDefinition Height="auto" />
                <RowDefinition Height="auto" />
                <RowDefinition Height="auto" />
                <RowDefinition Height="auto" />
                <RowDefinition Height="auto" />
                <RowDefinition Height="auto" />
            </Grid.RowDefinitions>
         <TextBlock Margin="5,6,0,0" Grid.Row="0" TextWrapping="Wrap" Padding="5,0,0,5"  FontFamily="Tohoma" FontSize="12" Text="Account Name: [[account.name]x]"   Foreground="#262626"/>
<TextBlock Margin="5,0,0,0" Grid.Row="4" TextWrapping="Wrap" Padding="3,0,0,3" FontFamily="Tohoma" FontSize="12" Style="{DynamicResource AutoCollapse}" Text="[[$Context.RevenuePotential]+]" />
<!--<TextBlock Margin="5,0,0,0" Grid.Row="1" TextWrapping="Wrap" Padding="3,0,0,3" Grid.ColumnSpan="3" FontFamily="Tohoma" FontSize="12" Style="{DynamicResource AutoCollapse}" Text="Phone: [[account.telephone1]x]"/>-->
<StackPanel  Orientation="Horizontal"  Grid.Row="2" Margin="5,0,0,0">
<Image Style="{DynamicResource ImageLogo}" Source="{Binding Source=msdyusd_Phone16, Converter={StaticResource CRMImageLoader}}" />
     <TextBlock  TextWrapping="Wrap" Padding="5,0,0,5" Text="Phone: " VerticalAlignment="Center"   Foreground="#262626" />
     <TextBlock  Padding="5,0,0,5" VerticalAlignment="Center">
     <Hyperlink Command="CCA:ActionCommands.DoActionCommand" CommandParameter="http://uii/CRM Global Manager/LaunchURL?callto:tel:[[account.telephone1]u+]" FontFamily="Tohoma" FontSize="12">[[account.telephone1]+]</Hyperlink>
       </TextBlock>
   </StackPanel >
<StackPanel  Orientation="Horizontal"  Grid.Row="1" Margin="5,0,0,0">
<Image Style="{DynamicResource ImageLogo}" Source="{Binding Source=msdyusd_Email16, Converter={StaticResource CRMImageLoader}}" />
<Label >
<TextBlock  TextWrapping="Wrap" Padding="3,0,0,3" Text="Email: [[Current Account.emailaddress1]+x]"   Foreground="#262626" />
</Label>
</StackPanel>
<TextBlock Margin="5,0,0,0" Grid.Row="3" TextWrapping="Wrap" Padding="5,0,0,5" Grid.ColumnSpan="3" FontFamily="Tohoma" FontSize="12" Style="{DynamicResource AutoCollapse}" Text="Primary Contact: [[account.primarycontactid.name]x]"   Foreground="#262626" />
</Grid>
</UserControl>
</controlStyles:USDTab>
<controlStyles:USDTab Header="Social Info">
    <Grid Margin="1"
       xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
       xmlns:CCA="clr-namespace:Microsoft.Crm.UnifiedServiceDesk.Dynamics;assembly=Microsoft.Crm.UnifiedServiceDesk.Dynamics">
     <Grid.RowDefinitions>
        <RowDefinition Height="auto" />
        <RowDefinition Height="auto" />
        <RowDefinition Height="auto" />
     </Grid.RowDefinitions>
      <TextBlock Margin="5,6,0,0" FontSize="12" Height="20" Grid.Row="0" Text="Twitter:     "   Foreground="#262626" >
       <Hyperlink Command="CCA:ActionCommands.DoActionCommand" CommandParameter="http://uii/Twitter/Navigate?about:blank">
               [[Account.msdyusd_twitter]x+]
       </Hyperlink>
     </TextBlock>
     <TextBlock Margin="5,0,0,0" FontSize="12" Height="50" Grid.Row="2"  Text="Facebook: "   Foreground="#262626">
        <Hyperlink Command="CCA:ActionCommands.DoActionCommand" CommandParameter="http://uii/Facebook/Navigate?about:blank">
                    [[Account.msdyusd_facebook]x+]
        </Hyperlink>
       </TextBlock>
        </Grid>
    </controlStyles:USDTab>
</TabControl>
```
