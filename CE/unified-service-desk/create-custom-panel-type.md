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
# <a name="create-a-custom-panel-type"></a>Create a custom panel type
Creating a new panel type is considered an advanced topic, and only those intimately familiar with [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] should attempt to create a new panel type.  
  
 Một loại bảng điều khiển phải thực hiện hai giao diện:  
  
- [IPanel](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.ui.controls.ipanel): This interface enables [!INCLUDE[pn_customer_care_accelerator](../includes/pn-customer-care-accelerator.md)] (CCA) support. Tuy nhiên, vì bản thân CCA không hỗ trợ bảng điều khiển tùy chỉnh, nếu bạn chỉ thực hiện giao diện này, bạn vẫn có thể không sử dụng nó với CCA.  
  
- [IUSDPanel](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.panellayouts.iusdpanel): This interface provides the additional functions that are needed to support custom panel types in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].  
  
  Nếu hai giao diện này được thực hiện một cách chính xác, chúng có thể được sử dụng với bố cục bảng điều khiển tùy chỉnh [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] để thực hiện bố cục nâng cao.  
  
### <a name="see-also"></a>Xem thêm  
 [Panels, panel types, and panel layouts in Unified Service Desk](../unified-service-desk/panels-panel-types-panel-layouts.md)   
 [Di chuyển kiểm soát tổ chức giữa các bảng điều khiển tại thời gian chạy](../unified-service-desk/move-hosted-controls-between-panels-runtime.md)   
 [Create custom panel layout in Unified Service Desk](../unified-service-desk/create-custom-panel-layout.md)
