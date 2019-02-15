---
title: Display hosted controls in the custom panel layout | MicrosoftDocs
description: Learn about specifying the custom panel layout as the display group for your hosted controls by using a syntax.
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
ms.assetid: f70fff3f-4007-4b74-8ea5-81e9cb7934cb
caps.latest.revision: 5
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 7371df85f1bd5319788d2ae9fbc2ec94e2f9b997
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388717"
---
# <a name="display-hosted-controls-in-the-custom-panel-layout"></a><span data-ttu-id="8dccf-103">Display hosted controls in the custom panel layout</span><span class="sxs-lookup"><span data-stu-id="8dccf-103">Display hosted controls in the custom panel layout</span></span>
<span data-ttu-id="8dccf-104">After you have created and loaded a custom panel layout in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], you will need to specify the custom panel layout as the display group for your hosted controls.</span><span class="sxs-lookup"><span data-stu-id="8dccf-104">After you have created and loaded a custom panel layout in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], you will need to specify the custom panel layout as the display group for your hosted controls.</span></span> <span data-ttu-id="8dccf-105">This is done using a special syntax:</span><span class="sxs-lookup"><span data-stu-id="8dccf-105">This is done using a special syntax:</span></span>  
  
```  
PanelLayoutControlName/NameOfPanelInsideControl  
```  
  
 <span data-ttu-id="8dccf-106">In the above syntax:</span><span class="sxs-lookup"><span data-stu-id="8dccf-106">In the above syntax:</span></span>  
  
- <span data-ttu-id="8dccf-107">**PanelLayoutControlName**: This is the name of your custom panel layout hosted control.</span><span class="sxs-lookup"><span data-stu-id="8dccf-107">**PanelLayoutControlName**: This is the name of your custom panel layout hosted control.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="8dccf-108">Do not specify the **Display Name** of your custom panel layout control.</span><span class="sxs-lookup"><span data-stu-id="8dccf-108">Do not specify the **Display Name** of your custom panel layout control.</span></span> <span data-ttu-id="8dccf-109">If this parameter is not specified, it is assumed to be your main panel layout.</span><span class="sxs-lookup"><span data-stu-id="8dccf-109">If this parameter is not specified, it is assumed to be your main panel layout.</span></span> <span data-ttu-id="8dccf-110">A main panel layout is the only panel layout hosted control located on the **MainWorkArea** display group.</span><span class="sxs-lookup"><span data-stu-id="8dccf-110">A main panel layout is the only panel layout hosted control located on the **MainWorkArea** display group.</span></span> <span data-ttu-id="8dccf-111">The **MainWorkArea** display group is defined as USDDeckTabPanel, but loading more than one control on this panel is generally not desirable.</span><span class="sxs-lookup"><span data-stu-id="8dccf-111">The **MainWorkArea** display group is defined as USDDeckTabPanel, but loading more than one control on this panel is generally not desirable.</span></span>  
  
- <span data-ttu-id="8dccf-112">**NameOfPanelInsideControl**: This is the name of the panel inside your custom panel layout.</span><span class="sxs-lookup"><span data-stu-id="8dccf-112">**NameOfPanelInsideControl**: This is the name of the panel inside your custom panel layout.</span></span> <span data-ttu-id="8dccf-113">See [Panel types](../unified-service-desk/panels-panel-types-panel-layouts.md#PanelTypes) for the various panels that might be referenced here.</span><span class="sxs-lookup"><span data-stu-id="8dccf-113">See [Panel types](../unified-service-desk/panels-panel-types-panel-layouts.md#PanelTypes) for the various panels that might be referenced here.</span></span>  
  
  <span data-ttu-id="8dccf-114">For example, if you want to configure a hosted control and display it on the MainPanel of your custom panel layout (MyUSDCustomPanelLayout), you will specify the following for as the Display Group value for the new hosted control: **MyUSDCustomPanelLayout/MainPanel**</span><span class="sxs-lookup"><span data-stu-id="8dccf-114">For example, if you want to configure a hosted control and display it on the MainPanel of your custom panel layout (MyUSDCustomPanelLayout), you will specify the following for as the Display Group value for the new hosted control: **MyUSDCustomPanelLayout/MainPanel**</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="8dccf-115">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="8dccf-115">See also</span></span>  
 [<span data-ttu-id="8dccf-116">Create custom panel layout in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="8dccf-116">Create custom panel layout in Unified Service Desk</span></span>](../unified-service-desk/create-custom-panel-layout.md)
