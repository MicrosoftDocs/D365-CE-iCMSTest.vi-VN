---
title: Use localized labels with ribbons (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Learn about using localized labels with ribbons.
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
- ribbon, labels
ms.assetid: 8f5c65a8-3134-46a9-aee5-8d876e045f1e
caps.latest.revision: 14
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ccd26be6cdf2fee3b9a2fc55a2f25875e02f1a92
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388035"
---
# <a name="use-localized-labels-with-ribbons"></a><span data-ttu-id="74d0b-103">Use localized labels with ribbons</span><span class="sxs-lookup"><span data-stu-id="74d0b-103">Use localized labels with ribbons</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="74d0b-104">Although Ribbon elements that display text allow for direct entry of text, it is a best practice to use localized labels to define text displayed in the ribbon.</span><span class="sxs-lookup"><span data-stu-id="74d0b-104">Although Ribbon elements that display text allow for direct entry of text, it is a best practice to use localized labels to define text displayed in the ribbon.</span></span> <span data-ttu-id="74d0b-105">This enables multi-language capabilities and better management of shared text.</span><span class="sxs-lookup"><span data-stu-id="74d0b-105">This enables multi-language capabilities and better management of shared text.</span></span>  
  
## <a name="using-localized-labels"></a><span data-ttu-id="74d0b-106">Using localized labels</span><span class="sxs-lookup"><span data-stu-id="74d0b-106">Using localized labels</span></span>  
 <span data-ttu-id="74d0b-107">The `<RibbonDiffXml>` element includes the `<LocLabels>` element.</span><span class="sxs-lookup"><span data-stu-id="74d0b-107">The `<RibbonDiffXml>` element includes the `<LocLabels>` element.</span></span> <span data-ttu-id="74d0b-108">As shown in the following example, this is where you can specify which text to display in the ribbon labels and tooltips using the `<Titles>` element.</span><span class="sxs-lookup"><span data-stu-id="74d0b-108">As shown in the following example, this is where you can specify which text to display in the ribbon labels and tooltips using the `<Titles>` element.</span></span>  
  
```xml  
<LocLabels>  
 <LocLabel Id="MyISV.account.SendToOtherSystem.LabelText">  
  <Titles>  
   <Title languagecode="1033"  
          description="Send to Other System" />  
  </Titles>  
 </LocLabel>  
 <LocLabel Id="MyISV.account.SendToOtherSystem.ToolTip">  
  <Titles>  
   <Title languagecode="1033"  
          description="Sends this Record to another system" />  
  </Titles>  
 </LocLabel>  
</LocLabels>  
```  
  
 <span data-ttu-id="74d0b-109">Within the definition of a ribbon element that displays text, the following example show how the localized label can be referenced using the `$LocLabels:` directive.</span><span class="sxs-lookup"><span data-stu-id="74d0b-109">Within the definition of a ribbon element that displays text, the following example show how the localized label can be referenced using the `$LocLabels:` directive.</span></span>  
  
```xml  
ToolTipTitle="$LocLabels:MyISV.account.SendToOtherSystem.LabelText"  
ToolTipDescription="$LocLabels:MyISV.account.SendToOtherSystem.ToolTip"  
```  
  
## <a name="force-a-line-break-in-a-ribbon-control-label"></a><span data-ttu-id="74d0b-110">Force a line break in a ribbon control label</span><span class="sxs-lookup"><span data-stu-id="74d0b-110">Force a line break in a ribbon control label</span></span>  
 <span data-ttu-id="74d0b-111">If you have a ribbon control label that is very long, the text will wrap to fit the available space.</span><span class="sxs-lookup"><span data-stu-id="74d0b-111">If you have a ribbon control label that is very long, the text will wrap to fit the available space.</span></span> <span data-ttu-id="74d0b-112">You can specify where you want to include a line break by using the following characters: `&#x200b;&#x200b;`.</span><span class="sxs-lookup"><span data-stu-id="74d0b-112">You can specify where you want to include a line break by using the following characters: `&#x200b;&#x200b;`.</span></span>  
  
 <span data-ttu-id="74d0b-113">If the label text is very long without a space for the text to wrap, the width of the control expands to allow for the entire label to be displayed.</span><span class="sxs-lookup"><span data-stu-id="74d0b-113">If the label text is very long without a space for the text to wrap, the width of the control expands to allow for the entire label to be displayed.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="74d0b-114">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="74d0b-114">See also</span></span>  
 <span data-ttu-id="74d0b-115">[Customize commands and the ribbon](customize-commands-ribbon.md) </span><span class="sxs-lookup"><span data-stu-id="74d0b-115">[Customize commands and the ribbon](customize-commands-ribbon.md) </span></span>  
 <span data-ttu-id="74d0b-116">[Export, Prepare to Edit, and Import the Ribbon](export-prepare-edit-import-ribbon.md) </span><span class="sxs-lookup"><span data-stu-id="74d0b-116">[Export, Prepare to Edit, and Import the Ribbon](export-prepare-edit-import-ribbon.md) </span></span>  
 <span data-ttu-id="74d0b-117">[Use Localized Labels with Ribbons](use-localized-labels-ribbons.md) </span><span class="sxs-lookup"><span data-stu-id="74d0b-117">[Use Localized Labels with Ribbons](use-localized-labels-ribbons.md) </span></span>  
 [<span data-ttu-id="74d0b-118">Define Ribbon Commands</span><span class="sxs-lookup"><span data-stu-id="74d0b-118">Define Ribbon Commands</span></span>](define-ribbon-commands.md)
