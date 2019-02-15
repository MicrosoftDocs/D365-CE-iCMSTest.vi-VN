---
title: Define custom actions to modify the ribbon (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Learn about defining custom actions to modify the ribbon.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- ribbon, hide ribbon elements
- ribbon, change ribbon elements
- ribbon, add ribbon elements
ms.assetid: f074df11-da5c-4efe-bbf2-a965f50bf3a9
caps.latest.revision: 18
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ca23da45dd43a70e72450141bba273e707655942
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385680"
---
# <a name="define-custom-actions-to-modify-the-ribbon"></a><span data-ttu-id="2a835-103">Define custom actions to modify the ribbon</span><span class="sxs-lookup"><span data-stu-id="2a835-103">Define custom actions to modify the ribbon</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="2a835-104">The default, an application command bar or ribbon is defined by [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement metadata.</span><span class="sxs-lookup"><span data-stu-id="2a835-104">The default, an application command bar or ribbon is defined by [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement metadata.</span></span> <span data-ttu-id="2a835-105">This default data can’t be changed, but you can include definitions of specific actions that will override the default ribbon.</span><span class="sxs-lookup"><span data-stu-id="2a835-105">This default data can’t be changed, but you can include definitions of specific actions that will override the default ribbon.</span></span>  
  
## <a name="types-of-custom-actions"></a><span data-ttu-id="2a835-106">Types of custom actions</span><span class="sxs-lookup"><span data-stu-id="2a835-106">Types of custom actions</span></span>  
 <span data-ttu-id="2a835-107">There are two types of custom actions for ribbons:</span><span class="sxs-lookup"><span data-stu-id="2a835-107">There are two types of custom actions for ribbons:</span></span>  
  
- <span data-ttu-id="2a835-108">`<CustomAction>`: [!INCLUDE[ribbon_element_CustomAction](../../includes/ribbon-element-customaction.md)]</span><span class="sxs-lookup"><span data-stu-id="2a835-108">`<CustomAction>`: [!INCLUDE[ribbon_element_CustomAction](../../includes/ribbon-element-customaction.md)]</span></span>  
  
- <span data-ttu-id="2a835-109">`<HideCustomAction>` : [!INCLUDE[ribbon_element_HideCustomAction](../../includes/ribbon-element-hidecustomaction.md)]</span><span class="sxs-lookup"><span data-stu-id="2a835-109">`<HideCustomAction>` : [!INCLUDE[ribbon_element_HideCustomAction](../../includes/ribbon-element-hidecustomaction.md)]</span></span>  
  
### <a name="custom-actions"></a><span data-ttu-id="2a835-110">Custom actions</span><span class="sxs-lookup"><span data-stu-id="2a835-110">Custom actions</span></span>  
 <span data-ttu-id="2a835-111">A custom action is a statement of how you want to change the default ribbon definition.</span><span class="sxs-lookup"><span data-stu-id="2a835-111">A custom action is a statement of how you want to change the default ribbon definition.</span></span> <span data-ttu-id="2a835-112">It is evaluated and applied to the ribbon at runtime.</span><span class="sxs-lookup"><span data-stu-id="2a835-112">It is evaluated and applied to the ribbon at runtime.</span></span> <span data-ttu-id="2a835-113">To set the context for a custom action, you must include information about the location of the items that you want to change.</span><span class="sxs-lookup"><span data-stu-id="2a835-113">To set the context for a custom action, you must include information about the location of the items that you want to change.</span></span> <span data-ttu-id="2a835-114">Use the `Location` attribute to specify where your change applies.</span><span class="sxs-lookup"><span data-stu-id="2a835-114">Use the `Location` attribute to specify where your change applies.</span></span>  
  
 <span data-ttu-id="2a835-115">When you add a new ribbon element, you refer to the containing element, for example, an existing tab or group.</span><span class="sxs-lookup"><span data-stu-id="2a835-115">When you add a new ribbon element, you refer to the containing element, for example, an existing tab or group.</span></span> <span data-ttu-id="2a835-116">You then include the suffix `._children` to indicate that this custom action will add something to an existing item.</span><span class="sxs-lookup"><span data-stu-id="2a835-116">You then include the suffix `._children` to indicate that this custom action will add something to an existing item.</span></span>  
  
 <span data-ttu-id="2a835-117">When you change the definition of an existing item, the `Location` value will match the ID of that item.</span><span class="sxs-lookup"><span data-stu-id="2a835-117">When you change the definition of an existing item, the `Location` value will match the ID of that item.</span></span>  
  
 <span data-ttu-id="2a835-118">You must also specify a unique identifier for the custom action.</span><span class="sxs-lookup"><span data-stu-id="2a835-118">You must also specify a unique identifier for the custom action.</span></span> <span data-ttu-id="2a835-119">Use the **Id** attribute to set this value.</span><span class="sxs-lookup"><span data-stu-id="2a835-119">Use the **Id** attribute to set this value.</span></span> <span data-ttu-id="2a835-120">We strongly recommend that you use a naming convention that will guarantee a unique value.</span><span class="sxs-lookup"><span data-stu-id="2a835-120">We strongly recommend that you use a naming convention that will guarantee a unique value.</span></span> <span data-ttu-id="2a835-121">For consistency and readability, we recommend that you use a period to separate consistent components.</span><span class="sxs-lookup"><span data-stu-id="2a835-121">For consistency and readability, we recommend that you use a period to separate consistent components.</span></span> <span data-ttu-id="2a835-122">The first item in your naming convention should be something related to your solutions publisher or solution, for example, `Contoso.contact.form.CustomButton.CustomAction`.</span><span class="sxs-lookup"><span data-stu-id="2a835-122">The first item in your naming convention should be something related to your solutions publisher or solution, for example, `Contoso.contact.form.CustomButton.CustomAction`.</span></span>  
  
> [!TIP]
>  <span data-ttu-id="2a835-123">Consistently applying your `Id` attribute naming conventions will greatly enhance your productivity while editing RibbonDiffXml.</span><span class="sxs-lookup"><span data-stu-id="2a835-123">Consistently applying your `Id` attribute naming conventions will greatly enhance your productivity while editing RibbonDiffXml.</span></span>  
  
 <span data-ttu-id="2a835-124">Based on the location information that you provide, the `Sequence` attribute value determines the order in which to render items.</span><span class="sxs-lookup"><span data-stu-id="2a835-124">Based on the location information that you provide, the `Sequence` attribute value determines the order in which to render items.</span></span> <span data-ttu-id="2a835-125">If you want a custom control to appear between two existing controls, you must select a sequence value that is in between the sequence values of the existing items.</span><span class="sxs-lookup"><span data-stu-id="2a835-125">If you want a custom control to appear between two existing controls, you must select a sequence value that is in between the sequence values of the existing items.</span></span>  
  
### <a name="hide-custom-actions"></a><span data-ttu-id="2a835-126">Hide custom actions</span><span class="sxs-lookup"><span data-stu-id="2a835-126">Hide custom actions</span></span>  
 <span data-ttu-id="2a835-127">A `<HideCustomAction>` is a statement that you use when you want to remove an existing ribbon element so that it is not rendered.</span><span class="sxs-lookup"><span data-stu-id="2a835-127">A `<HideCustomAction>` is a statement that you use when you want to remove an existing ribbon element so that it is not rendered.</span></span> <span data-ttu-id="2a835-128">This does not hide the ribbon element, it actually removes the ribbon element at runtime so that it doesn’t exist in the ribbon.</span><span class="sxs-lookup"><span data-stu-id="2a835-128">This does not hide the ribbon element, it actually removes the ribbon element at runtime so that it doesn’t exist in the ribbon.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="2a835-129">Because the `HideCustomAction` element removes a specified node from the ribbon, removing ribbon elements in this manner may not be the best option for every situation.</span><span class="sxs-lookup"><span data-stu-id="2a835-129">Because the `HideCustomAction` element removes a specified node from the ribbon, removing ribbon elements in this manner may not be the best option for every situation.</span></span>  
> 
> - <span data-ttu-id="2a835-130">If you want to remove a button that is associated with a specific privilege, you should adjust the privileges for the entity in the security roles in your implementation.</span><span class="sxs-lookup"><span data-stu-id="2a835-130">If you want to remove a button that is associated with a specific privilege, you should adjust the privileges for the entity in the security roles in your implementation.</span></span> <span data-ttu-id="2a835-131">This will allow the default ribbon display and enables rules to hide or disable ribbon elements from users who do not have the necessary privileges to perform those actions.</span><span class="sxs-lookup"><span data-stu-id="2a835-131">This will allow the default ribbon display and enables rules to hide or disable ribbon elements from users who do not have the necessary privileges to perform those actions.</span></span>  
>   -   <span data-ttu-id="2a835-132">If you want to replace an existing ribbon element with a custom ribbon element, you can overwrite that element by specifying a `CustomAction.Location` value identical to the existing element.</span><span class="sxs-lookup"><span data-stu-id="2a835-132">If you want to replace an existing ribbon element with a custom ribbon element, you can overwrite that element by specifying a `CustomAction.Location` value identical to the existing element.</span></span>  
  
 <span data-ttu-id="2a835-133">The **HideActionId** element provides a unique ID for the action.</span><span class="sxs-lookup"><span data-stu-id="2a835-133">The **HideActionId** element provides a unique ID for the action.</span></span> <span data-ttu-id="2a835-134">For consistency and readability, you should follow the same naming convention described for `<CustomAction>` elements.</span><span class="sxs-lookup"><span data-stu-id="2a835-134">For consistency and readability, you should follow the same naming convention described for `<CustomAction>` elements.</span></span> <span data-ttu-id="2a835-135">The **Location** attribute must match the Id of the ribbon element you want to remove.</span><span class="sxs-lookup"><span data-stu-id="2a835-135">The **Location** attribute must match the Id of the ribbon element you want to remove.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="2a835-136">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="2a835-136">See also</span></span>  
 <span data-ttu-id="2a835-137">[Customize commands and the ribbon](customize-commands-ribbon.md) </span><span class="sxs-lookup"><span data-stu-id="2a835-137">[Customize commands and the ribbon](customize-commands-ribbon.md) </span></span>  
 <span data-ttu-id="2a835-138">[Pass Microsoft Dynamics 365 for Customer Engagement data from a page as a parameter to Ribbon Actions](pass-dynamics-365-data-page-parameter-ribbon-actions.md) </span><span class="sxs-lookup"><span data-stu-id="2a835-138">[Pass Microsoft Dynamics 365 for Customer Engagement data from a page as a parameter to Ribbon Actions](pass-dynamics-365-data-page-parameter-ribbon-actions.md) </span></span>  
 [<span data-ttu-id="2a835-139">Define Scaling for Ribbon Elements</span><span class="sxs-lookup"><span data-stu-id="2a835-139">Define Scaling for Ribbon Elements</span></span>](define-scaling-ribbon-elements.md)
