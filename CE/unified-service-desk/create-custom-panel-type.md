---
title: Create a custom panel type | MicrosoftDocs
description: Learn about creating a custom panel type.
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
ms.assetid: 6d49565d-f5d0-4e61-bca7-9fb990dbfdb4
caps.latest.revision: 6
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 09049f51039df18c87d44f07ac341c83d464cfa4
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387455"
---
# <a name="create-a-custom-panel-type"></a><span data-ttu-id="adcd5-103">Create a custom panel type</span><span class="sxs-lookup"><span data-stu-id="adcd5-103">Create a custom panel type</span></span>
<span data-ttu-id="adcd5-104">Creating a new panel type is considered an advanced topic, and only those intimately familiar with [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] should attempt to create a new panel type.</span><span class="sxs-lookup"><span data-stu-id="adcd5-104">Creating a new panel type is considered an advanced topic, and only those intimately familiar with [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] should attempt to create a new panel type.</span></span>  
  
 <span data-ttu-id="adcd5-105">Một loại bảng điều khiển phải thực hiện hai giao diện:</span><span class="sxs-lookup"><span data-stu-id="adcd5-105">A panel type must implement two interfaces:</span></span>  
  
- <span data-ttu-id="adcd5-106">[IPanel](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.ui.controls.ipanel): This interface enables [!INCLUDE[pn_customer_care_accelerator](../includes/pn-customer-care-accelerator.md)] (CCA) support.</span><span class="sxs-lookup"><span data-stu-id="adcd5-106">[IPanel](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.ui.controls.ipanel): This interface enables [!INCLUDE[pn_customer_care_accelerator](../includes/pn-customer-care-accelerator.md)] (CCA) support.</span></span> <span data-ttu-id="adcd5-107">Tuy nhiên, vì bản thân CCA không hỗ trợ bảng điều khiển tùy chỉnh, nếu bạn chỉ thực hiện giao diện này, bạn vẫn có thể không sử dụng nó với CCA.</span><span class="sxs-lookup"><span data-stu-id="adcd5-107">However, as CCA by itself does not support custom panels, if you only implement this interface, you still may not use it with CCA.</span></span>  
  
- <span data-ttu-id="adcd5-108">[IUSDPanel](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.panellayouts.iusdpanel): This interface provides the additional functions that are needed to support custom panel types in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="adcd5-108">[IUSDPanel](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.panellayouts.iusdpanel): This interface provides the additional functions that are needed to support custom panel types in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span>  
  
  <span data-ttu-id="adcd5-109">Nếu hai giao diện này được thực hiện một cách chính xác, chúng có thể được sử dụng với bố cục bảng điều khiển tùy chỉnh [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] để thực hiện bố cục nâng cao.</span><span class="sxs-lookup"><span data-stu-id="adcd5-109">If these two interfaces are implemented correctly, they may be used with [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] panel layouts to perform advanced layouts.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="adcd5-110">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="adcd5-110">See also</span></span>  
 <span data-ttu-id="adcd5-111">[Panels, panel types, and panel layouts in Unified Service Desk](../unified-service-desk/panels-panel-types-panel-layouts.md) </span><span class="sxs-lookup"><span data-stu-id="adcd5-111">[Panels, panel types, and panel layouts in Unified Service Desk](../unified-service-desk/panels-panel-types-panel-layouts.md) </span></span>  
 <span data-ttu-id="adcd5-112">[Di chuyển kiểm soát tổ chức giữa các bảng điều khiển tại thời gian chạy](../unified-service-desk/move-hosted-controls-between-panels-runtime.md) </span><span class="sxs-lookup"><span data-stu-id="adcd5-112">[Move hosted controls between panels at runtime](../unified-service-desk/move-hosted-controls-between-panels-runtime.md) </span></span>  
 [<span data-ttu-id="adcd5-113">Create custom panel layout in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="adcd5-113">Create custom panel layout in Unified Service Desk</span></span>](../unified-service-desk/create-custom-panel-layout.md)
