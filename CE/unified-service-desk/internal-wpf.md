---
title: Internal WPF process hosting method for your controls in Unified Service Desk for Dynamics 365 Customer Engagement| MicrosoftDocs
description: Learn about the Internal WPF hosting methods for your controls in Unified Service Desk.
ms.custom:
- dyn365-USD
ms.date: 12/01/2018
ms.service: dynamics-365-customerservice
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 (online)
- Dynamics 365 (on-premises)
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: 0847C77B-A922-4CB5-9155-2429816AEDDA
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
monikerRange: '>= dynamics-usd-3'
ms.openlocfilehash: 2f4f2a3eee22b529e8f6c4323ed4ac9d3fe1619d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388551"
---
# <a name="internal-wpf"></a><span data-ttu-id="0a46d-103">WPF nội bộ</span><span class="sxs-lookup"><span data-stu-id="0a46d-103">Internal WPF</span></span>

 <span data-ttu-id="0a46d-104">The `Internal WPF` browser control uses the [WpfBrowser](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.controls.wpfbrowser) component, which is based on the [!INCLUDE[pn_ms_Windows_Presentation_Foundation](../includes/pn-ms-windows-presentation-foundation.md)][WebBrowser](https://msdn.microsoft.com/library/system.windows.forms.webbrowser.aspx) control, to host the webpages in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="0a46d-104">The `Internal WPF` browser control uses the [WpfBrowser](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.controls.wpfbrowser) component, which is based on the [!INCLUDE[pn_ms_Windows_Presentation_Foundation](../includes/pn-ms-windows-presentation-foundation.md)][WebBrowser](https://msdn.microsoft.com/library/system.windows.forms.webbrowser.aspx) control, to host the webpages in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> <span data-ttu-id="0a46d-105">This browser control is the traditional method of hosting controls in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="0a46d-105">This browser control is the traditional method of hosting controls in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> <span data-ttu-id="0a46d-106">It uses the security subsystem in [!INCLUDE[pn_Internet_Explorer](../includes/pn-internet-explorer.md)] and [!INCLUDE[pn_ms_Windows_short](../includes/pn-ms-windows-short.md)] to allow the hosted application to operate the browser functionality in the same mode as the application without changing the [!INCLUDE[pn_Internet_Explorer](../includes/pn-internet-explorer.md)] settings, and therefore reduces the security of Internet Explorer for applications outside of Unified Service Desk.</span><span class="sxs-lookup"><span data-stu-id="0a46d-106">It uses the security subsystem in [!INCLUDE[pn_Internet_Explorer](../includes/pn-internet-explorer.md)] and [!INCLUDE[pn_ms_Windows_short](../includes/pn-ms-windows-short.md)] to allow the hosted application to operate the browser functionality in the same mode as the application without changing the [!INCLUDE[pn_Internet_Explorer](../includes/pn-internet-explorer.md)] settings, and therefore reduces the security of Internet Explorer for applications outside of Unified Service Desk.</span></span> <span data-ttu-id="0a46d-107">While there are advantages, occasionally you may find that you need the features of an [!INCLUDE[pn_Internet_Explorer](../includes/pn-internet-explorer.md)] add-in or a feature in the native browser that may not be supported in this browser control, and you should use the **IE Process** browser control instead.</span><span class="sxs-lookup"><span data-stu-id="0a46d-107">While there are advantages, occasionally you may find that you need the features of an [!INCLUDE[pn_Internet_Explorer](../includes/pn-internet-explorer.md)] add-in or a feature in the native browser that may not be supported in this browser control, and you should use the **IE Process** browser control instead.</span></span>

 ## <a name="see-also"></a><span data-ttu-id="0a46d-108">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="0a46d-108">See also</span></span>  
 [<span data-ttu-id="0a46d-109">Create or edit a hosted control</span><span class="sxs-lookup"><span data-stu-id="0a46d-109">Create or edit a hosted control</span></span>](../unified-service-desk/create-edit-hosted-control.md)   

 [<span data-ttu-id="0a46d-110">Hosted control types and action/event reference</span><span class="sxs-lookup"><span data-stu-id="0a46d-110">Hosted control types and action/event reference</span></span>](../unified-service-desk/hosted-control-types-action-event-reference.md)   

 [<span data-ttu-id="0a46d-111">Manage hosted controls, actions, and events</span><span class="sxs-lookup"><span data-stu-id="0a46d-111">Manage hosted controls, actions, and events</span></span>](../unified-service-desk/manage-hosted-controls-actions-events.md)
