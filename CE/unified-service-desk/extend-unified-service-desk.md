---
title: Extend Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: 'The section provides information on how you can use the User Interface Integration (UII) components to extend Unified Service Desk to integrate with external applications, web applications, and computer telephony integration (CTI) systems. '
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
ms.assetid: 88d2daf3-5a2d-4da2-ab13-aa650247b0e5
caps.latest.revision: 13
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: ee0fb10d6c7a77030fc7e65d0dda7b33371c1bfa
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387290"
---
# <a name="extend-unified-service-desk"></a><span data-ttu-id="5e021-103">Extend Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="5e021-103">Extend Unified Service Desk</span></span>
<span data-ttu-id="5e021-104">Phần này cung cấp thông tin về cách bạn có thể sử dụng các thành phần [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] để mở rộng [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] để tích hợp với ứng dụng bên ngoài, với các ứng dụng, web và hệ thống [!INCLUDE[pn_computer_telephony_integration_cti](../includes/pn-computer-telephony-integration-cti.md)].</span><span class="sxs-lookup"><span data-stu-id="5e021-104">This section provides information on how you can use the [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] components to extend [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] to integrate with external applications, web applications, and [!INCLUDE[pn_computer_telephony_integration_cti](../includes/pn-computer-telephony-integration-cti.md)] systems.</span></span> <span data-ttu-id="5e021-105">Phần này cũng cung cấp thông tin về cách tùy chỉnh [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] bằng cách phát triển kiểm soát tổ chức và bố cục ngăn tùy chỉnh.</span><span class="sxs-lookup"><span data-stu-id="5e021-105">It also provides information on how to customize [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] by developing custom hosted controls and panel layouts.</span></span>  
  
 [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] <span data-ttu-id="5e021-106">provides you with a host of [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)] project templates that you can use to create a [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] application adapter, a [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] web adapter, a [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] customer search control (Windows Forms and [!INCLUDE[pn_ms_Windows_Presentation_Foundation](../includes/pn-ms-windows-presentation-foundation.md)]), a [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] hosted control (Windows Forms and [!INCLUDE[pn_wpf_acronym](../includes/pn-wpf-acronym.md)]), a [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)][!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] adapter, a custom [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] hosted control, and a custom panel layout.</span><span class="sxs-lookup"><span data-stu-id="5e021-106">provides you with a host of [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)] project templates that you can use to create a [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] application adapter, a [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] web adapter, a [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] customer search control (Windows Forms and [!INCLUDE[pn_ms_Windows_Presentation_Foundation](../includes/pn-ms-windows-presentation-foundation.md)]), a [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] hosted control (Windows Forms and [!INCLUDE[pn_wpf_acronym](../includes/pn-wpf-acronym.md)]), a [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)][!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] adapter, a custom [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] hosted control, and a custom panel layout.</span></span> 
 
 <span data-ttu-id="5e021-107">You can get the project templates by [downloading](http://go.microsoft.com/fwlink/p/?LinkId=400925) the **CRM SDK Templates** from the Visual Studio gallery, and double-clicking the CRMSDKTemplates.vsix file to install the templates in [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)].</span><span class="sxs-lookup"><span data-stu-id="5e021-107">You can get the project templates by [downloading](http://go.microsoft.com/fwlink/p/?LinkId=400925) the **CRM SDK Templates** from the Visual Studio gallery, and double-clicking the CRMSDKTemplates.vsix file to install the templates in [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)].</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="5e021-108">The templates work with [!INCLUDE[pn_microsoft_visual_studio_2012](../includes/pn-microsoft-visual-studio-2012.md)], [!INCLUDE[pn_visual_studio_2013](../includes/pn-visual-studio-2013.md)], or [!INCLUDE[pn_visual_studio_2015](../includes/pn-visual-studio-2015.md)].</span><span class="sxs-lookup"><span data-stu-id="5e021-108">The templates work with [!INCLUDE[pn_microsoft_visual_studio_2012](../includes/pn-microsoft-visual-studio-2012.md)], [!INCLUDE[pn_visual_studio_2013](../includes/pn-visual-studio-2013.md)], or [!INCLUDE[pn_visual_studio_2015](../includes/pn-visual-studio-2015.md)].</span></span> <span data-ttu-id="5e021-109">Additionally, you must have [!INCLUDE[tn_nuget_package_manager](../includes/tn-nuget-package-manager.md)] for [Visual Studio 2012](http://visualstudiogallery.msdn.microsoft.com/27077b70-9dad-4c64-adcf-c7cf6bc9970c), [Visual Studio 2013](http://visualstudiogallery.msdn.microsoft.com/4ec1526c-4a8c-4a84-b702-b21a8f5293ca), or [Visual Studio 2015](https://visualstudiogallery.msdn.microsoft.com/5d345edc-2e2d-4a9c-b73b-d53956dc458d).</span><span class="sxs-lookup"><span data-stu-id="5e021-109">Additionally, you must have [!INCLUDE[tn_nuget_package_manager](../includes/tn-nuget-package-manager.md)] for [Visual Studio 2012](http://visualstudiogallery.msdn.microsoft.com/27077b70-9dad-4c64-adcf-c7cf6bc9970c), [Visual Studio 2013](http://visualstudiogallery.msdn.microsoft.com/4ec1526c-4a8c-4a84-b702-b21a8f5293ca), or [Visual Studio 2015](https://visualstudiogallery.msdn.microsoft.com/5d345edc-2e2d-4a9c-b73b-d53956dc458d).</span></span>  
  
 <span data-ttu-id="5e021-110">For information about the [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] concepts that you must know to extend [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Unified Service Desk and the UII framework](../unified-service-desk/unified-service-desk-uii-framework.md).</span><span class="sxs-lookup"><span data-stu-id="5e021-110">For information about the [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] concepts that you must know to extend [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Unified Service Desk and the UII framework](../unified-service-desk/unified-service-desk-uii-framework.md).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="5e021-111">In This Section</span><span class="sxs-lookup"><span data-stu-id="5e021-111">In This Section</span></span>  
 [<span data-ttu-id="5e021-112">Integrate with external application and web application</span><span class="sxs-lookup"><span data-stu-id="5e021-112">Integrate with external application and web application</span></span>](../unified-service-desk/integrate-external-applications-web-applications.md)  
  
 [<span data-ttu-id="5e021-113">Integrate with CTI applications</span><span class="sxs-lookup"><span data-stu-id="5e021-113">Integrate with CTI applications</span></span>](../unified-service-desk/integrate-cti-systems-cti-adapters.md)  
  
 [<span data-ttu-id="5e021-114">Integrate with Citrix applications</span><span class="sxs-lookup"><span data-stu-id="5e021-114">Integrate with Citrix applications</span></span>](../unified-service-desk/integrate-citrix-applications.md)  
  
 [<span data-ttu-id="5e021-115">Use custom hosted control in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="5e021-115">Use custom hosted control in Unified Service Desk</span></span>](../unified-service-desk/use-custom-hosted-control-unified-service-desk.md)  
  
 [<span data-ttu-id="5e021-116">Sử dụng loại bảng điều khiển tùy chỉnh và bố cục bảng điều khiển</span><span class="sxs-lookup"><span data-stu-id="5e021-116">Use custom panel types and panel layouts</span></span>](../unified-service-desk/use-custom-panel-types-panel-layouts-unified-service-desk.md)  
  
 [<span data-ttu-id="5e021-117">Use custom listeners for auditing, diagnostics and traces</span><span class="sxs-lookup"><span data-stu-id="5e021-117">Use custom listeners for auditing, diagnostics and traces</span></span>](../unified-service-desk/create-custom-listeners-auditing-diagnostics-traces.md)  
  
 [<span data-ttu-id="5e021-118">Reuse Entity Search definition in your custom code</span><span class="sxs-lookup"><span data-stu-id="5e021-118">Reuse Entity Search definition in your custom code</span></span>](../unified-service-desk/reuse-entity-search-definition-custom-code.md)  
  
 [<span data-ttu-id="5e021-119">Debug your custom code for Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="5e021-119">Debug your custom code for Unified Service Desk</span></span>](../unified-service-desk/debug-custom-code-unified-service-desk.md)  
  
## <a name="reference"></a><span data-ttu-id="5e021-120">Tham chiếu</span><span class="sxs-lookup"><span data-stu-id="5e021-120">Reference</span></span>  
 [<span data-ttu-id="5e021-121">Tham chiếu chương trình</span><span class="sxs-lookup"><span data-stu-id="5e021-121">Programming reference</span></span>](../unified-service-desk/programming-reference.md)  
  
 [<span data-ttu-id="5e021-122">Unified Service Desk Team Blog</span><span class="sxs-lookup"><span data-stu-id="5e021-122">Unified Service Desk Team Blog</span></span>](http://blogs.msdn.com/b/usd/)  
  
## <a name="related-sections"></a><span data-ttu-id="5e021-123">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="5e021-123">Related Sections</span></span>  
 [<span data-ttu-id="5e021-124">Core concepts for extending Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="5e021-124">Core concepts for extending Unified Service Desk</span></span>](../unified-service-desk/unified-service-desk-uii-framework.md)  
  
 [<span data-ttu-id="5e021-125">Core concepts for configuring Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="5e021-125">Core concepts for configuring Unified Service Desk</span></span>](../unified-service-desk/core-concepts-for-configuring-unified-service-desk.md)
