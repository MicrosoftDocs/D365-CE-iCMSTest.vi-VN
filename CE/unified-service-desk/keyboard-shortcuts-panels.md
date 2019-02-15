---
title: Keyboard shortcuts for panels in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn about the keyboard shortcuts for panels in Unified Service Desk
ms.custom:
- dyn365-a11y
- dyn365-USD
ms.date: 08/23/2017
ms.reviewer: ''
ms.service: dynamics-365-customerservice
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 539aa1c3-faa3-4e54-ad14-f7da96529e91
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: c351d39785ba466c83e2c470f9103d4a5e7d6dcf
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385876"
---
# <a name="keyboard-shortcuts-for-panels-in-unified-service-desk"></a><span data-ttu-id="572f4-103">Keyboard shortcuts for panels in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="572f4-103">Keyboard shortcuts for panels in Unified Service Desk</span></span>
[!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] <span data-ttu-id="572f4-104">now lets you cycle through all the active panels using a predefined keyboard shortcut and also define keyboard shortcuts to directly access individual panels in the panel layout.</span><span class="sxs-lookup"><span data-stu-id="572f4-104">now lets you cycle through all the active panels using a predefined keyboard shortcut and also define keyboard shortcuts to directly access individual panels in the panel layout.</span></span>  
  
  
  
<a name="traverse"></a>   

## <a name="keyboard-shortcut-to-traverse-through-panels"></a><span data-ttu-id="572f4-105">Keyboard shortcut to traverse through panels</span><span class="sxs-lookup"><span data-stu-id="572f4-105">Keyboard shortcut to traverse through panels</span></span>  

 <span data-ttu-id="572f4-106">Use the Ctrl+0 (default) keyboard shortcut to cyclically traverse through all the active panels in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client.</span><span class="sxs-lookup"><span data-stu-id="572f4-106">Use the Ctrl+0 (default) keyboard shortcut to cyclically traverse through all the active panels in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client.</span></span> <span data-ttu-id="572f4-107">To change the default shortcut key, use the **PanelNavigationShortcut** UII option to specify shortcut keys of your choice.</span><span class="sxs-lookup"><span data-stu-id="572f4-107">To change the default shortcut key, use the **PanelNavigationShortcut** UII option to specify shortcut keys of your choice.</span></span> <span data-ttu-id="572f4-108">More information: [Manage Options for Unified Service Desk](admin/manage-options-unified-service-desk.md)</span><span class="sxs-lookup"><span data-stu-id="572f4-108">More information: [Manage Options for Unified Service Desk](admin/manage-options-unified-service-desk.md)</span></span>  
  
 <span data-ttu-id="572f4-109">Some key points to consider while using the shortcut key to traverse through panels are:</span><span class="sxs-lookup"><span data-stu-id="572f4-109">Some key points to consider while using the shortcut key to traverse through panels are:</span></span>  
  
-   <span data-ttu-id="572f4-110">The standard order of traversal is left to right and top to bottom.</span><span class="sxs-lookup"><span data-stu-id="572f4-110">The standard order of traversal is left to right and top to bottom.</span></span>  
  
-   <span data-ttu-id="572f4-111">You cannot traverse to any visible panel that has no actionable control inside it.</span><span class="sxs-lookup"><span data-stu-id="572f4-111">You cannot traverse to any visible panel that has no actionable control inside it.</span></span>  
  
-   <span data-ttu-id="572f4-112">You cannot traverse to any hidden panels on the layout, like the ones inside a collapsed expander panel.</span><span class="sxs-lookup"><span data-stu-id="572f4-112">You cannot traverse to any hidden panels on the layout, like the ones inside a collapsed expander panel.</span></span>  
  
-   <span data-ttu-id="572f4-113">You cannot traverse to a panel that has the `Focusable` attribute set to `False`.</span><span class="sxs-lookup"><span data-stu-id="572f4-113">You cannot traverse to a panel that has the `Focusable` attribute set to `False`.</span></span>  
  
<a name="assign"></a>   

## <a name="assign-keyboard-shortcut-to-panel"></a><span data-ttu-id="572f4-114">Assign keyboard shortcut to panel</span><span class="sxs-lookup"><span data-stu-id="572f4-114">Assign keyboard shortcut to panel</span></span>  

 <span data-ttu-id="572f4-115">Assigning keyboard shortcuts to panels in a [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] panel layout helps customer service agents *directly* navigate to a panel in the client application by using keyboard.</span><span class="sxs-lookup"><span data-stu-id="572f4-115">Assigning keyboard shortcuts to panels in a [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] panel layout helps customer service agents *directly* navigate to a panel in the client application by using keyboard.</span></span> <span data-ttu-id="572f4-116">You can assign keyboard shortcut to a panel in a custom panel layout by using the `USD:PanelNavigation.KeyboardShortcut` attribute in the panel element definition of the panel layout XAML.</span><span class="sxs-lookup"><span data-stu-id="572f4-116">You can assign keyboard shortcut to a panel in a custom panel layout by using the `USD:PanelNavigation.KeyboardShortcut` attribute in the panel element definition of the panel layout XAML.</span></span>  
  
 <span data-ttu-id="572f4-117">You must also set the `Focusable` attribute to `True` in the panel element definition for which you are defining the shortcut.</span><span class="sxs-lookup"><span data-stu-id="572f4-117">You must also set the `Focusable` attribute to `True` in the panel element definition for which you are defining the shortcut.</span></span> <span data-ttu-id="572f4-118">Otherwise, you won't be able to access the panel using the assigned keyboard shortcut even after defining it in the panel layout XAML.</span><span class="sxs-lookup"><span data-stu-id="572f4-118">Otherwise, you won't be able to access the panel using the assigned keyboard shortcut even after defining it in the panel layout XAML.</span></span>  
  
 <span data-ttu-id="572f4-119">The following example demonstrates how to assign the Ctrl+8 keyboard shortcut to the right panel in your [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] custom panel layout XAML definition:</span><span class="sxs-lookup"><span data-stu-id="572f4-119">The following example demonstrates how to assign the Ctrl+8 keyboard shortcut to the right panel in your [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] custom panel layout XAML definition:</span></span>  
  
```xaml  
<USD:USDTabPanel x:Name="RightPanel"  
                 AutomationProperties.Name="Right Panel"  
                 Grid.Row="0"  
                 USD:PanelNavigation.KeyboardShortcut="Ctrl+8"  
                 Focusable="True"/>  
```  
  
> [!NOTE]
>  <span data-ttu-id="572f4-120">The standard panel layout in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] provides pre-configured keyboard shortcuts for the panels, and the  keyboard shortcuts range from Ctrl+1 to Ctrl+9.</span><span class="sxs-lookup"><span data-stu-id="572f4-120">The standard panel layout in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] provides pre-configured keyboard shortcuts for the panels, and the  keyboard shortcuts range from Ctrl+1 to Ctrl+9.</span></span> <span data-ttu-id="572f4-121">For information about the standard panel layout and its XAML definition with keyboard shortcuts assigned to different panels, see [Panel layouts in Unified Service Desk](../unified-service-desk/panels-panel-types-panel-layouts.md#PanelLayouts)</span><span class="sxs-lookup"><span data-stu-id="572f4-121">For information about the standard panel layout and its XAML definition with keyboard shortcuts assigned to different panels, see [Panel layouts in Unified Service Desk](../unified-service-desk/panels-panel-types-panel-layouts.md#PanelLayouts)</span></span>  
  
<a name="considerations"></a>   
## <a name="things-to-consider-while-using-keyboard-shortcut-for-panel"></a><span data-ttu-id="572f4-122">Things to consider while using keyboard shortcut for panel</span><span class="sxs-lookup"><span data-stu-id="572f4-122">Things to consider while using keyboard shortcut for panel</span></span>  
 <span data-ttu-id="572f4-123">Any key combination that is used by [!INCLUDE[pn_Internet_Explorer](../includes/pn-internet-explorer.md)] (for example Ctrl+S) or general Windows operations (such as Ctrl+C, Ctrl+V) can cause conflicts with keyboard shortcuts that you assign to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] panels.</span><span class="sxs-lookup"><span data-stu-id="572f4-123">Any key combination that is used by [!INCLUDE[pn_Internet_Explorer](../includes/pn-internet-explorer.md)] (for example Ctrl+S) or general Windows operations (such as Ctrl+C, Ctrl+V) can cause conflicts with keyboard shortcuts that you assign to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] panels.</span></span>  
  
 <span data-ttu-id="572f4-124">Therefore, as a developer or customizer, the foremost thing is to identify and assign  keyboard shortcuts to panels that do not conflict with [!INCLUDE[pn_Internet_Explorer](../includes/pn-internet-explorer.md)] or Windows.</span><span class="sxs-lookup"><span data-stu-id="572f4-124">Therefore, as a developer or customizer, the foremost thing is to identify and assign  keyboard shortcuts to panels that do not conflict with [!INCLUDE[pn_Internet_Explorer](../includes/pn-internet-explorer.md)] or Windows.</span></span> <span data-ttu-id="572f4-125">Also, ensure that you do not assign duplicate keyboard shortcut to panels that conflict within [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="572f4-125">Also, ensure that you do not assign duplicate keyboard shortcut to panels that conflict within [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> <span data-ttu-id="572f4-126">In case of a duplicate keyboard shortcut, [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] will set the keyboard shortcut  for the panel as the active shortcut key that was registered earlier during the execution sequence.</span><span class="sxs-lookup"><span data-stu-id="572f4-126">In case of a duplicate keyboard shortcut, [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] will set the keyboard shortcut  for the panel as the active shortcut key that was registered earlier during the execution sequence.</span></span> <span data-ttu-id="572f4-127">Further, information about duplicate shortcut key is logged in the `UnifiedSeviceDesk.log` file (typically available at c:\Users\\*\<UserName>* \AppData\Roaming\Microsoft\Microsoft Dynamics 365 for Customer Engagement Unified Service Desk\\*\<Version>*), which can be used by developers and customizers to resolve the duplicate keyboard shortcut issue in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration.</span><span class="sxs-lookup"><span data-stu-id="572f4-127">Further, information about duplicate shortcut key is logged in the `UnifiedSeviceDesk.log` file (typically available at c:\Users\\*\<UserName>* \AppData\Roaming\Microsoft\Microsoft Dynamics 365 for Customer Engagement Unified Service Desk\\*\<Version>*), which can be used by developers and customizers to resolve the duplicate keyboard shortcut issue in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration.</span></span>  
  
 <span data-ttu-id="572f4-128">Even after assigning non-conflicting keyboard shortcuts to your panels, the shortcut will not work if the current focus is on a control in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client that is hosted as a [IE Process](../unified-service-desk/ie-process.md) control because the focus is in a different process.</span><span class="sxs-lookup"><span data-stu-id="572f4-128">Even after assigning non-conflicting keyboard shortcuts to your panels, the shortcut will not work if the current focus is on a control in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client that is hosted as a [IE Process](../unified-service-desk/ie-process.md) control because the focus is in a different process.</span></span> <span data-ttu-id="572f4-129">However, this issue is not applicable to controls hosted using the [Internal WPF](../unified-service-desk/internal-wpf.md) control.</span><span class="sxs-lookup"><span data-stu-id="572f4-129">However, this issue is not applicable to controls hosted using the [Internal WPF](../unified-service-desk/internal-wpf.md) control.</span></span>  
  
 <span data-ttu-id="572f4-130">The workaround is to inform your [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client users, if you use the `IE Process` hosting for your controls, to use the CTRL+UP ARROW keyboard shortcut to move the focus from a `IE Process` hosted control to the main window *before* using the desired panel keyboard shortcut key to ensure that [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] honors the shortcut.</span><span class="sxs-lookup"><span data-stu-id="572f4-130">The workaround is to inform your [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client users, if you use the `IE Process` hosting for your controls, to use the CTRL+UP ARROW keyboard shortcut to move the focus from a `IE Process` hosted control to the main window *before* using the desired panel keyboard shortcut key to ensure that [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] honors the shortcut.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="572f4-131">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="572f4-131">See also</span></span>  
 <span data-ttu-id="572f4-132">[Bảng điều khiển, loại bảng điều khiển và bố cục bảng điều khiển trong Unified Service Desk](../unified-service-desk/panels-panel-types-panel-layouts.md) </span><span class="sxs-lookup"><span data-stu-id="572f4-132">[Panels, panel types, and panel layouts in Unified Service Desk](../unified-service-desk/panels-panel-types-panel-layouts.md) </span></span>  
 [<span data-ttu-id="572f4-133">Tạo bố chục bảng điều khiển tùy chỉnh</span><span class="sxs-lookup"><span data-stu-id="572f4-133">Create a custom panel layout</span></span>](../unified-service-desk/create-custom-panel-layout.md)
