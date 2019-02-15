---
title: Customize commands and the ribbon (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: 'Dynamics 365 for Customer Engagement displays commands in different ways depending on the entity and the client. In most places in the web application you will see a command bar instead of a ribbon. Dynamics 365 for Customer Engagement for tablets also uses data defined as ribbons to control what commands are available using a command bar that is optimized for touch. '
ms.custom: ''
ms.date: 09/25/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- ribbon
- customize, ribbon
ms.assetid: c688a24a-ef2d-4c0b-951b-e6db22382686
caps.latest.revision: 38
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 012304ef347a9ee9894845b6d60a7937bf5ec9e7
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388517"
---
# <a name="customize-commands-and-the-ribbon"></a><span data-ttu-id="58304-105">Customize commands and the ribbon</span><span class="sxs-lookup"><span data-stu-id="58304-105">Customize commands and the ribbon</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] <span data-ttu-id="58304-106">Customer Engagement displays commands in different ways depending on the entity and the client.</span><span class="sxs-lookup"><span data-stu-id="58304-106">Customer Engagement displays commands in different ways depending on the entity and the client.</span></span> <span data-ttu-id="58304-107">In most places in the web application you will see a *command bar* instead of a ribbon.</span><span class="sxs-lookup"><span data-stu-id="58304-107">In most places in the web application you will see a *command bar* instead of a ribbon.</span></span> [!INCLUDE[pn_moca_short](../../includes/pn-moca-short.md)] <span data-ttu-id="58304-108">also uses data defined as ribbons to control what commands are available using a command bar that is optimized for touch.</span><span class="sxs-lookup"><span data-stu-id="58304-108">also uses data defined as ribbons to control what commands are available using a command bar that is optimized for touch.</span></span>  
  
 <span data-ttu-id="58304-109">The command bar provides better performance.</span><span class="sxs-lookup"><span data-stu-id="58304-109">The command bar provides better performance.</span></span> <span data-ttu-id="58304-110">The ribbon is still displayed in the web application for certain entity forms and it is still used for list views in [!INCLUDE[pn_crm_2016_outlook](../../includes/pn-crm-2016-outlook.md)].</span><span class="sxs-lookup"><span data-stu-id="58304-110">The ribbon is still displayed in the web application for certain entity forms and it is still used for list views in [!INCLUDE[pn_crm_2016_outlook](../../includes/pn-crm-2016-outlook.md)].</span></span>  
  
 <span data-ttu-id="58304-111">Both the command bar and the ribbon use the same underlying XML data to define what commands to display, when the commands are enabled, and what the commands do.</span><span class="sxs-lookup"><span data-stu-id="58304-111">Both the command bar and the ribbon use the same underlying XML data to define what commands to display, when the commands are enabled, and what the commands do.</span></span>  
  
 <span data-ttu-id="58304-112">The topics in this section introduce you to key concepts that you must understand, and common tasks you perform when you customize the command bar or the ribbon.</span><span class="sxs-lookup"><span data-stu-id="58304-112">The topics in this section introduce you to key concepts that you must understand, and common tasks you perform when you customize the command bar or the ribbon.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="58304-113">Because the underlying XML schema was designed to display commands as ribbons, the term *ribbon* will continue to be used in the documentation.</span><span class="sxs-lookup"><span data-stu-id="58304-113">Because the underlying XML schema was designed to display commands as ribbons, the term *ribbon* will continue to be used in the documentation.</span></span>  
  
 <span data-ttu-id="58304-114">The SDK describes the process of editing the ribbon by editing the customization.xml file directly.</span><span class="sxs-lookup"><span data-stu-id="58304-114">The SDK describes the process of editing the ribbon by editing the customization.xml file directly.</span></span> <span data-ttu-id="58304-115">The most frequently used tool created by the community is the [Ribbon Workbench](http://www.develop1.net/public/rwb/ribbonworkbench.aspx)</span><span class="sxs-lookup"><span data-stu-id="58304-115">The most frequently used tool created by the community is the [Ribbon Workbench](http://www.develop1.net/public/rwb/ribbonworkbench.aspx)</span></span> 
 
<span data-ttu-id="58304-116">To obtain support or help to use this program, contact the program publisher.</span><span class="sxs-lookup"><span data-stu-id="58304-116">To obtain support or help to use this program, contact the program publisher.</span></span>  
  
  
## <a name="see-also"></a><span data-ttu-id="58304-117">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="58304-117">See also</span></span>  
 [<span data-ttu-id="58304-118">Ribbon Core Schema</span><span class="sxs-lookup"><span data-stu-id="58304-118">Ribbon Core Schema</span></span>](ribbon-core-schema.md)  
  
 [<span data-ttu-id="58304-119">Ribbon Types Schema</span><span class="sxs-lookup"><span data-stu-id="58304-119">Ribbon Types Schema</span></span>](ribbon-types-schema.md)  
  
 [<span data-ttu-id="58304-120">Ribbon WSS Schema</span><span class="sxs-lookup"><span data-stu-id="58304-120">Ribbon WSS Schema</span></span>](ribbon-wss-schema.md) 

 [<span data-ttu-id="58304-121">Sample: Export Ribbon Definitions</span><span class="sxs-lookup"><span data-stu-id="58304-121">Sample: Export Ribbon Definitions</span></span>](sample-export-ribbon-definitions.md) 
  
 [<span data-ttu-id="58304-122">Client scripting using JavaScript</span><span class="sxs-lookup"><span data-stu-id="58304-122">Client scripting using JavaScript</span></span>](../clientapi/client-scripting.md)
