---
title: Known issues of performance enhancement for CRM entity page loads | MicrosoftDocs
description: Learn about the known issues of the Internet Explorer pooling feature.
ms.custom:
- dyn365-USD, dyn365-admin
ms.date: 02/15/2018
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
ms.assetid: D552D7B4-61F0-43D3-AB7E-E2E2D0E8321F
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
ms.openlocfilehash: e662300dc839b6431e0424c7f0beb82abc6104ca
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382594"
---
# <a name="known-issues-of-performance-enhancement-for-crm-entity-page-loads"></a>Known issues of performance enhancement for CRM entity page loads

## <a name="closing-crm-entity-page-starts-loading-but-never-completes-loading"></a>Closing CRM entity page starts loading but never completes loading

When **InternetExplorerPooling** is enabled, and if you close a CRM entity page hosted in Unified Service Desk using the close (**x**) button (_see Image 1_), the CRM entity page to starts loading but never completes loading (_see Image 2_).

  ![Closing CRM entity page hosted in Unified Service Desk using close button](../../unified-service-desk/media/usd-crm-page-hosted-close-button.PNG "Closing CRM entity page hosted in Unified Service Desk using close button")
    
  _Image 1: Closing CRM entity page hosted in Unified Service Desk using close (x) button_
  
  ![CRM entity page start loading but never completes loading](../../unified-service-desk/media/usd-crm-page-hosted-never-completes-loading.PNG "CRM entity page start loading but never completes loading")
  
  _Image 2: CRM entity page start loading but never completes loading_

#### <a name="workaround"></a>**Giải pháp thay thế**

If you close the CRM entity page, the page starts loading but never completes the loading. In this case, to restore the CRM entity page, right-click on CRM entity page and select **Forward** from the context menu (_see Image 1_).

![Right-click on the CRM entity page and select Forward from the context menu](../../unified-service-desk/media/usd-crm-page-right-click-CRM-entity-page-select-forward.PNG "Right-click on the CRM entity page and select Forward from the context menu")

_Image 1: Right-click on the CRM entity page and select Forward from the context menu_

> [!Note]
> The session that you are working is fine and there is no data lost.

<!--If you  close the CRM entity page, the page starts loading but never completes loading. In this case, you need to close the CRM entity page and reopen the page to continue working.

It is possible that there is not close button on the CRM page tab, in this case, you can close the session tab and reopen the session and CRM entity page to continue working.

If the session tab does not have the close button, you must close the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application and relaunch the client application, session, and CRM entity page to continue working.-->

## <a name="see-also"></a>Xem thêm

[Manage Options for Unified Service Desk](../../unified-service-desk/admin/manage-options-unified-service-desk.md)
 
[Performance enhancement for CRM entity page loads](../admin/performance-enhancement-CRM-entity-page-loads.md)
