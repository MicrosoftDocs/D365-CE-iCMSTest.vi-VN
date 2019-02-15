---
title: Develop customized IoT solutions in Connected Field Service | MicrosoftDocs
description: Connected Field Service integrates Internet of Things (IoT) devices with Dynamics 365 for Customer Engagement (online) to enable their registration, monitoring and management into established business processes.
ms.custom:
- dyn365-developer
- dyn365-fieldservice
ms.date: 01/05/2018
ms.reviewer: ''
ms.service: dynamics-365-customerservice
ms.suite: ''
ms.technology:
- field-service
ms.tgt_pltfrm: ''
ms.topic: get-started-article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: b210b88e-3447-43a7-845e-23d6e7a94331
caps.latest.revision: 8
author: JimDaly
ms.author: jdaly
manager: jdaly
search.audienceType:
- developer
search.app:
- D365CE
- D365FS
ms.openlocfilehash: 31b59f250117ad6d0f2206e0d0577d825b37c1f1
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387176"
---
# <a name="develop-customized-iot-solutions-in-connected-field-service"></a>Develop customized IoT solutions in Connected Field Service

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[pn_connected_field_service_msdyn365](../../includes/pn-connected-field-service-msdyn365.md)] integrates Internet of Things (IoT) devices with [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] to enable their registration, monitoring and management into established business processes. This guide explains the component architecture, supplied interfaces and customization points, and explains the approach to develop customized IoT solutions.  
  
## <a name="supported-developer-scenarios"></a>Supported Developer Scenarios  
 The initial release of Connected Field Service supports the following two primary development scenarios:  
  
- Extend [!INCLUDE[pn_connected_field_service_msdyn365](../../includes/pn-connected-field-service-msdyn365.md)] so that manufacturers and hardware service organizations can register, monitor, and manage—including controlling and correcting—IoT devices. Future releases will provide additional support for predicative and prescriptive maintenance capabilities.  
  
- Provide an IoT Platform that ISVs and partners can build on to IOT-enable their [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] custom entities and managed solutions.  
  
  To enable the first scenario, the following capabilities are supported:  
  
- Abstract device registration in an action, so that devices can be easily registered using the CRM web client or the mobile client  
  
- Enable any CRM entity to be IOT-enabled, enabling straightforward IoT integration within existing business processes by using [Connection entities](../../developer/connection-entities.md)  
  
- Receive service alerts and automating their response with a customized workflow  
  
- Send remote commands to IoT devices, for example after diagnosing a problem to correct a malfunctioning device  
  
- Analyze incoming device data, and displaying aggregate, trend and other metrics in custom dashboards  
  
### <a name="see-also"></a>Xem thêm  
 [Connected Field Service architecture](connected-field-service-architecture.md)   
 [Mở rộng các giải pháp Connected Field Service](extend-connected-field-service-solutions.md)<br>
 [Hướng dẫn về Dynamics 365 for Customer Engagement dành cho nhà phát triển](../../developer/developer-guide.md)   
