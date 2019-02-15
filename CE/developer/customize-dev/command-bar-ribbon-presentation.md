---
title: Command bar or ribbon presentation (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Data defining commands in Dynamics 365 for Customer Engagement (online) Customer Engagement can be presented in several different ways depending on the client and differences in how some entities are treated. You need to take these factors into consideration as you change ribbon commands or define new ones.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 0eda8edd-3fc1-4b88-9413-b3cd89a30028
caps.latest.revision: 21
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4a22b7be3eaa889aeeb788e71892e68704cbd165
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388538"
---
# <a name="command-bar-or-ribbon-presentation"></a><span data-ttu-id="3fb30-104">Command bar or ribbon presentation</span><span class="sxs-lookup"><span data-stu-id="3fb30-104">Command bar or ribbon presentation</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="3fb30-105">Data defining commands in [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement can be presented in several different ways depending on the client and differences in how some entities are treated.</span><span class="sxs-lookup"><span data-stu-id="3fb30-105">Data defining commands in [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement can be presented in several different ways depending on the client and differences in how some entities are treated.</span></span> <span data-ttu-id="3fb30-106">You need to take these factors into consideration as you change ribbon commands or define new ones.</span><span class="sxs-lookup"><span data-stu-id="3fb30-106">You need to take these factors into consideration as you change ribbon commands or define new ones.</span></span>  
  
<a name="BKMK_DifferentPresentations"></a>   
## <a name="different-presentations-of-commands"></a><span data-ttu-id="3fb30-107">Different presentations of commands</span><span class="sxs-lookup"><span data-stu-id="3fb30-107">Different presentations of commands</span></span>  
 <span data-ttu-id="3fb30-108">There are three different ways that command data can be displayed.</span><span class="sxs-lookup"><span data-stu-id="3fb30-108">There are three different ways that command data can be displayed.</span></span>  
  
### <a name="updated-user-experience"></a><span data-ttu-id="3fb30-109">Updated user experience</span><span class="sxs-lookup"><span data-stu-id="3fb30-109">Updated user experience</span></span>  
 <span data-ttu-id="3fb30-110">This is the presentation of the command bar throughout the application and for forms for entities that have the updated user experience.</span><span class="sxs-lookup"><span data-stu-id="3fb30-110">This is the presentation of the command bar throughout the application and for forms for entities that have the updated user experience.</span></span>  
  
 <span data-ttu-id="3fb30-111">![Account command bar in Dynamics 365 for Customer Engagement](../media/customization-account-grid-command-bar.PNG "Account command bar in Dynamics 365 for Customer Engagement")</span><span class="sxs-lookup"><span data-stu-id="3fb30-111">![Account command bar in Dynamics 365 for Customer Engagement](../media/customization-account-grid-command-bar.PNG "Account command bar in Dynamics 365 for Customer Engagement")</span></span>  
  
 <span data-ttu-id="3fb30-112">In this experience, only the first seven commands are displayed and any remaining commands are available in a flyout menu.</span><span class="sxs-lookup"><span data-stu-id="3fb30-112">In this experience, only the first seven commands are displayed and any remaining commands are available in a flyout menu.</span></span>  
  
 <span data-ttu-id="3fb30-113">Enable rules will hide commands that should not be used.</span><span class="sxs-lookup"><span data-stu-id="3fb30-113">Enable rules will hide commands that should not be used.</span></span>  
  
 <span data-ttu-id="3fb30-114">Subgrids have a limited number of controls.</span><span class="sxs-lookup"><span data-stu-id="3fb30-114">Subgrids have a limited number of controls.</span></span> <span data-ttu-id="3fb30-115">Only controls to allow adding records, deleting records, or opening a view of the grid are available.</span><span class="sxs-lookup"><span data-stu-id="3fb30-115">Only controls to allow adding records, deleting records, or opening a view of the grid are available.</span></span> <span data-ttu-id="3fb30-116">But these commands are still defined by ribbon data and can be customized.</span><span class="sxs-lookup"><span data-stu-id="3fb30-116">But these commands are still defined by ribbon data and can be customized.</span></span>  
  
 <span data-ttu-id="3fb30-117">![Contact sub-grid in Dynamics 365 for Customer Engagement](../media/customization-contract-subgrid.PNG "Contact sub-grid in Dynamics 365 for Customer Engagement")</span><span class="sxs-lookup"><span data-stu-id="3fb30-117">![Contact sub-grid in Dynamics 365 for Customer Engagement](../media/customization-contract-subgrid.PNG "Contact sub-grid in Dynamics 365 for Customer Engagement")</span></span>  
  
 <span data-ttu-id="3fb30-118">To perform more actions on the list of records displayed in a subgrid, select the option to open a view of the grid.</span><span class="sxs-lookup"><span data-stu-id="3fb30-118">To perform more actions on the list of records displayed in a subgrid, select the option to open a view of the grid.</span></span>  
  
 <span data-ttu-id="3fb30-119">For more information about the behavior of subgrid controls and how they can be customized, see [Sub Grid Ribbons](ribbons-available-microsoft-dynamics-365.md#BKMK_SubGridRibbons).</span><span class="sxs-lookup"><span data-stu-id="3fb30-119">For more information about the behavior of subgrid controls and how they can be customized, see [Sub Grid Ribbons](ribbons-available-microsoft-dynamics-365.md#BKMK_SubGridRibbons).</span></span>  
  
### <a name="classic-user-experience"></a><span data-ttu-id="3fb30-120">Classic user experience</span><span class="sxs-lookup"><span data-stu-id="3fb30-120">Classic user experience</span></span>  
 <span data-ttu-id="3fb30-121">This is the presentation using the ribbon.</span><span class="sxs-lookup"><span data-stu-id="3fb30-121">This is the presentation using the ribbon.</span></span> <span data-ttu-id="3fb30-122">It is used for lists within the Outlook client and for the forms of entities that do not use the updated user experience.</span><span class="sxs-lookup"><span data-stu-id="3fb30-122">It is used for lists within the Outlook client and for the forms of entities that do not use the updated user experience.</span></span>  
  
 <span data-ttu-id="3fb30-123">![Article ribbon in Dynamics 365 for Customer Engagement](../media/customization-article-ribbon.PNG "Article ribbon in Dynamics 365 for Customer Engagement")</span><span class="sxs-lookup"><span data-stu-id="3fb30-123">![Article ribbon in Dynamics 365 for Customer Engagement](../media/customization-article-ribbon.PNG "Article ribbon in Dynamics 365 for Customer Engagement")</span></span>  
  
 <span data-ttu-id="3fb30-124">In this experience tabs are available and groups can define scaling so that all available commands in a tab are shown as the width of the screen changes.</span><span class="sxs-lookup"><span data-stu-id="3fb30-124">In this experience tabs are available and groups can define scaling so that all available commands in a tab are shown as the width of the screen changes.</span></span>  
  
 <span data-ttu-id="3fb30-125">Enable rules can disable commands that should not be used so that they are still visible.</span><span class="sxs-lookup"><span data-stu-id="3fb30-125">Enable rules can disable commands that should not be used so that they are still visible.</span></span>  
  
 <span data-ttu-id="3fb30-126">Subgrid commands are shown in a List Tools contextual tab at the top of the page when the subgrid is selected.</span><span class="sxs-lookup"><span data-stu-id="3fb30-126">Subgrid commands are shown in a List Tools contextual tab at the top of the page when the subgrid is selected.</span></span>  
  
 <span data-ttu-id="3fb30-127">![Article Comments sub-grid ribbon in Dynamics 365 for Customer Engagement](../media/customization-article-comments-subgrid-ribbon.PNG "Article Comments sub-grid ribbon in Dynamics 365 for Customer Engagement")</span><span class="sxs-lookup"><span data-stu-id="3fb30-127">![Article Comments sub-grid ribbon in Dynamics 365 for Customer Engagement](../media/customization-article-comments-subgrid-ribbon.PNG "Article Comments sub-grid ribbon in Dynamics 365 for Customer Engagement")</span></span>  
  
<a name="BKMK_CRMForTablets"></a>   
### <a name="includepndynamicscrmincludespn-dynamics-crmmd-for-tablets"></a>[!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] <span data-ttu-id="3fb30-128">dành cho máy tính bảng</span><span class="sxs-lookup"><span data-stu-id="3fb30-128">for tablets</span></span>  
 [!INCLUDE[pn_moca_full](../../includes/pn-moca-full.md)] <span data-ttu-id="3fb30-129">presents commands in a manner optimized for touch experiences.</span><span class="sxs-lookup"><span data-stu-id="3fb30-129">presents commands in a manner optimized for touch experiences.</span></span> <span data-ttu-id="3fb30-130">Commands appear in the command bar at the bottom right of the screen in order from right to left.</span><span class="sxs-lookup"><span data-stu-id="3fb30-130">Commands appear in the command bar at the bottom right of the screen in order from right to left.</span></span>  
  
 <span data-ttu-id="3fb30-131">![Lệnh biểu mẫu khách hàng đối với Dynamics 365 for Customer Engagement for tablets](../media/customization-nobile-app-account-form-command.PNG "Lệnh biểu mẫu khách hàng đối với Dynamics 365 for Customer Engagement for tablets")</span><span class="sxs-lookup"><span data-stu-id="3fb30-131">![Account form commands for Dynamics 365 for Customer Engagement for tablets](../media/customization-nobile-app-account-form-command.PNG "Account form commands for Dynamics 365 for Customer Engagement for tablets")</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="3fb30-132">Icons configured for commands will not display and labels that are too long will be truncated.</span><span class="sxs-lookup"><span data-stu-id="3fb30-132">Icons configured for commands will not display and labels that are too long will be truncated.</span></span>  
> 
> [!INCLUDE[pn_moca_full](../../includes/pn-moca-full.md)] <span data-ttu-id="3fb30-133">does not support adding dynamic elements to `<FlyoutAnchor>` or `<SplitButton>` elements at runtime.</span><span class="sxs-lookup"><span data-stu-id="3fb30-133">does not support adding dynamic elements to `<FlyoutAnchor>` or `<SplitButton>` elements at runtime.</span></span>  
  
 <span data-ttu-id="3fb30-134">Subgrid commands are displayed when people tap and press the subgrid control.</span><span class="sxs-lookup"><span data-stu-id="3fb30-134">Subgrid commands are displayed when people tap and press the subgrid control.</span></span> <span data-ttu-id="3fb30-135">These commands are shown on the bottom left of the screen in order from left to right.</span><span class="sxs-lookup"><span data-stu-id="3fb30-135">These commands are shown on the bottom left of the screen in order from left to right.</span></span>  
  
 <span data-ttu-id="3fb30-136">![Activity sub-grid commands in Dynamics 365 for Customer Engagement for tablets](../media/customization-mobile-app-activity-subgrid.PNG "Activity sub-grid commands in Dynamics 365 for Customer Engagement for tablets")</span><span class="sxs-lookup"><span data-stu-id="3fb30-136">![Activity sub-grid commands in Dynamics 365 for Customer Engagement for tablets](../media/customization-mobile-app-activity-subgrid.PNG "Activity sub-grid commands in Dynamics 365 for Customer Engagement for tablets")</span></span>  
  
<a name="BKMK_CommandData"></a>   
## <a name="command-data"></a><span data-ttu-id="3fb30-137">Command data</span><span class="sxs-lookup"><span data-stu-id="3fb30-137">Command data</span></span>  
 <span data-ttu-id="3fb30-138">Despite these very different presentations, the data that defines the commands for entities is consistent regardless of how the commands are presented.</span><span class="sxs-lookup"><span data-stu-id="3fb30-138">Despite these very different presentations, the data that defines the commands for entities is consistent regardless of how the commands are presented.</span></span> <span data-ttu-id="3fb30-139">It contains definitions for tabs and groups with scaling, but the visible parts of these containers for controls are only displayed in the classic user interface.</span><span class="sxs-lookup"><span data-stu-id="3fb30-139">It contains definitions for tabs and groups with scaling, but the visible parts of these containers for controls are only displayed in the classic user interface.</span></span>  
  
 <span data-ttu-id="3fb30-140">In both the updated user experience and Dynamics 365 for Customer Engagement for tablets, tabs and groups still act as containers for controls, but there is no visual indication of these containers and scaling is not applied.</span><span class="sxs-lookup"><span data-stu-id="3fb30-140">In both the updated user experience and Dynamics 365 for Customer Engagement for tablets, tabs and groups still act as containers for controls, but there is no visual indication of these containers and scaling is not applied.</span></span>  
  
<a name="BKMK_FilteringCommands"></a>   
## <a name="filtering-commands-based-on-presentation-and-client"></a><span data-ttu-id="3fb30-141">Filtering commands based on presentation and client</span><span class="sxs-lookup"><span data-stu-id="3fb30-141">Filtering commands based on presentation and client</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="3fb30-142">Including some kind of rule to filter the display of your commands is necessary unless you want the command to be available for all clients and presentations.</span><span class="sxs-lookup"><span data-stu-id="3fb30-142">Including some kind of rule to filter the display of your commands is necessary unless you want the command to be available for all clients and presentations.</span></span>  
  
 <span data-ttu-id="3fb30-143">With this release there is a new element that can be used in display and enable rules to adapt the commands you display with the presentation.</span><span class="sxs-lookup"><span data-stu-id="3fb30-143">With this release there is a new element that can be used in display and enable rules to adapt the commands you display with the presentation.</span></span>  
  
 <span data-ttu-id="3fb30-144">`<CommandClientTypeRule>` contains a `Type` attribute that will be evaluated based on the presentation.</span><span class="sxs-lookup"><span data-stu-id="3fb30-144">`<CommandClientTypeRule>` contains a `Type` attribute that will be evaluated based on the presentation.</span></span> <span data-ttu-id="3fb30-145">The following valid options correspond to the presentation:</span><span class="sxs-lookup"><span data-stu-id="3fb30-145">The following valid options correspond to the presentation:</span></span>  
  
- <span data-ttu-id="3fb30-146">`Refresh`: Updated user experience</span><span class="sxs-lookup"><span data-stu-id="3fb30-146">`Refresh`: Updated user experience</span></span>  
  
- <span data-ttu-id="3fb30-147">`Legacy`: Classic user experience</span><span class="sxs-lookup"><span data-stu-id="3fb30-147">`Legacy`: Classic user experience</span></span>  
  
- <span data-ttu-id="3fb30-148">`Modern`: Dynamics 365 for Customer Engagement for tablets</span><span class="sxs-lookup"><span data-stu-id="3fb30-148">`Modern`: Dynamics 365 for Customer Engagement for tablets</span></span>  
  
  <span data-ttu-id="3fb30-149">Use this element as you define commands to control whether they display in the different presentations.</span><span class="sxs-lookup"><span data-stu-id="3fb30-149">Use this element as you define commands to control whether they display in the different presentations.</span></span>  
  
  <span data-ttu-id="3fb30-150">There is also a pre-existing `<CrmClientTypeRule>` element, but the `Type` attribute for element can only differentiate between `Web` and `Outlook` clients.</span><span class="sxs-lookup"><span data-stu-id="3fb30-150">There is also a pre-existing `<CrmClientTypeRule>` element, but the `Type` attribute for element can only differentiate between `Web` and `Outlook` clients.</span></span> <span data-ttu-id="3fb30-151">This rule will evaluate the Dynamics 365 for Customer Engagement for tablets client as the web client.</span><span class="sxs-lookup"><span data-stu-id="3fb30-151">This rule will evaluate the Dynamics 365 for Customer Engagement for tablets client as the web client.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="3fb30-152">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="3fb30-152">See also</span></span>  
 <span data-ttu-id="3fb30-153">[Customize commands and the ribbon](customize-commands-ribbon.md) </span><span class="sxs-lookup"><span data-stu-id="3fb30-153">[Customize commands and the ribbon](customize-commands-ribbon.md) </span></span>  
 <span data-ttu-id="3fb30-154">[Ribbons Available in Microsoft Dynamics 365 for Customer Engagement](ribbons-available-microsoft-dynamics-365.md) </span><span class="sxs-lookup"><span data-stu-id="3fb30-154">[Ribbons Available in Microsoft Dynamics 365 for Customer Engagement](ribbons-available-microsoft-dynamics-365.md) </span></span>  
 <span data-ttu-id="3fb30-155">[Export Ribbon Definitions](export-ribbon-definitions.md) </span><span class="sxs-lookup"><span data-stu-id="3fb30-155">[Export Ribbon Definitions](export-ribbon-definitions.md) </span></span>  
 [<span data-ttu-id="3fb30-156">Developers guide to customization for Microsoft Dynamics 365 for Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="3fb30-156">Developers guide to customization for Microsoft Dynamics 365 for Customer Engagement</span></span>](customize-applications.md)
