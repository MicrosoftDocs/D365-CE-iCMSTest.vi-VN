---
title: Define ribbon tab display rules (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Learn about defining ribbon tab displays rules.
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
- ribbon, display tabs
ms.assetid: 08c73aba-26ed-4cf9-aacc-c225140025bc
caps.latest.revision: 17
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7d192503bc4a4d10a9b18473fa1ffa9af3f8e2d8
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386788"
---
# <a name="define-ribbon-tab-display-rules"></a><span data-ttu-id="c065b-103">Define ribbon tab display rules</span><span class="sxs-lookup"><span data-stu-id="c065b-103">Define ribbon tab display rules</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="c065b-104">Tab display rules control whether a specific tab is displayed for a ribbon or not.</span><span class="sxs-lookup"><span data-stu-id="c065b-104">Tab display rules control whether a specific tab is displayed for a ribbon or not.</span></span>  
  
 <span data-ttu-id="c065b-105">Unlike other ribbon elements like groups or specific controls, you must explicitly provide a tab display rule for a tab to be displayed in the ribbon.</span><span class="sxs-lookup"><span data-stu-id="c065b-105">Unlike other ribbon elements like groups or specific controls, you must explicitly provide a tab display rule for a tab to be displayed in the ribbon.</span></span> <span data-ttu-id="c065b-106">By default, other ribbon elements will always display unless a display rule removes them.</span><span class="sxs-lookup"><span data-stu-id="c065b-106">By default, other ribbon elements will always display unless a display rule removes them.</span></span>  
  
 <span data-ttu-id="c065b-107">`<TabDisplayRule>` elements require that the `TabCommand` attribute matches a `<Tab>` `Command` attribute value.</span><span class="sxs-lookup"><span data-stu-id="c065b-107">`<TabDisplayRule>` elements require that the `TabCommand` attribute matches a `<Tab>` `Command` attribute value.</span></span>  
  
 <span data-ttu-id="c065b-108">In the `RibbonDiffXml`, tabs can be defined for specific entities or defined globally.</span><span class="sxs-lookup"><span data-stu-id="c065b-108">In the `RibbonDiffXml`, tabs can be defined for specific entities or defined globally.</span></span> <span data-ttu-id="c065b-109">If the tab is defined for an entity, the only valid type of rule is `<EntityRule>`.</span><span class="sxs-lookup"><span data-stu-id="c065b-109">If the tab is defined for an entity, the only valid type of rule is `<EntityRule>`.</span></span> <span data-ttu-id="c065b-110">Because defining a tab in the scope of a particular entity already limits the tab to only that entity, the only valid attributes are `AppliesTo` (`PrimaryEntity` or `SelectedEntity`) and `Context` (`Form`, `HomePageGrid`, `SubGridStandard`, or `SubGridAssociated`).</span><span class="sxs-lookup"><span data-stu-id="c065b-110">Because defining a tab in the scope of a particular entity already limits the tab to only that entity, the only valid attributes are `AppliesTo` (`PrimaryEntity` or `SelectedEntity`) and `Context` (`Form`, `HomePageGrid`, `SubGridStandard`, or `SubGridAssociated`).</span></span>  
  
 <span data-ttu-id="c065b-111">When you define a tab display rule globally in the `RibbonDiffXml` for the application ribbons, you can apply both `EntityRule` elements and `<PageRule>` elements.</span><span class="sxs-lookup"><span data-stu-id="c065b-111">When you define a tab display rule globally in the `RibbonDiffXml` for the application ribbons, you can apply both `EntityRule` elements and `<PageRule>` elements.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="c065b-112">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="c065b-112">See also</span></span>  
 <span data-ttu-id="c065b-113">[Customize commands and the ribbon](customize-commands-ribbon.md) </span><span class="sxs-lookup"><span data-stu-id="c065b-113">[Customize commands and the ribbon](customize-commands-ribbon.md) </span></span>  
 <span data-ttu-id="c065b-114">[Define Scaling for Ribbon Elements](define-scaling-ribbon-elements.md) </span><span class="sxs-lookup"><span data-stu-id="c065b-114">[Define Scaling for Ribbon Elements](define-scaling-ribbon-elements.md) </span></span>  
 [<span data-ttu-id="c065b-115">Pass Parameters to a URL By Using the Ribbon</span><span class="sxs-lookup"><span data-stu-id="c065b-115">Pass Parameters to a URL By Using the Ribbon</span></span>](pass-parameters-url-by-using-ribbon.md)
