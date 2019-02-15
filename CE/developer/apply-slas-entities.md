---
title: Apply SLAs to entities (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn about applying SLAs to custom entities by enabling entities for applying SLAs. Also, you can create SLA KPIs.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 1b94bd7c-d683-4595-b402-47959137c3fd
caps.latest.revision: 21
author: KumarVivek
ms.author: kvivek
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 0696c117ff0bfdf7b0645e24bb8f8688ffcdd5b7
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385570"
---
# <a name="apply-slas-to-entities"></a>Apply SLAs to entities

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

Service level agreements (SLAs) in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps help you define the level of service or support that your organization agrees to offer a customer by including items to define metrics or key performance indicators (KPIs) to attain the service level. You can apply SLAs to custom entities and the following system entities:  
  
-   Tất cả thực thể hoạt động (chẳng hạn như Email, Tác vụ và Cuộc hẹn) ngoại trừ các cuộc hẹn định kỳ (RecurringAppointmentMaster)  
  
-   Khách hàng  
  
-   người liên hệ  
  
-   Hóa đơn  
  
-   Incident (Case)  
  
-   Cơ hội  
  
-   Báo giá  
  
-   Khách hàng tiềm năng  
  
-   SalesOrder (Order)  
  
> [!NOTE]
>  SLA support for entities, in addition to the Incident entity, was introduced in [!INCLUDE[pn_crm_8_1_0_online_subsequent](../includes/pn-crm-8-1-0-online-subsequent.md)] and Dynamics 365 for Customer Engagement apps Service Pack 1 (on-premises).  
  
<a name="EnableSLAs"></a>   
## <a name="enable-entities-for-applying-slas"></a>Enable entities for applying SLAs  
 To apply SLAs to an entity, you must set the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsSLAEnabled> attribute to true for the entity. You can’t change this setting after it’s been enabled. By default, the `Incident` entity is enabled for SLAs.  
  
 You can also use the customization tool to enable entities for SLAs. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Enable entities for service level agreements](../customer-service/enable-entities-service-level-agreements.md)  
  
 After you have enabled an entity forSLAs, new SLA-related attributes, such as `SLAId` and `SLAInvokedId`, will be automatically added to the entity.  
  
<a name="CreateSLAKPI"></a>   
## <a name="create-sla-kpis"></a>Create SLA KPIs  
 To programmatically create SLA KPIs for an entity, create a lookup attribute on any SLA-enabled entity, and then set a relationship for that attribute to the `SLAKPIInstance` entity.  
  
<a name="ApplySLA"></a>   
## <a name="apply-slas-to-entity-records"></a>Apply SLAs to entity records  
 Using the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] web client, you can create SLAs for an SLA-enabled entity, and set an SLA as default for the entity so that it is applied automatically to any new entity records.  
  
 However, if you want to manually apply SLAs to entity records based on any custom business requirement, you can programmatically update the entity record to set the `SLAId` attribute value to the desired active SLA record.  
  
<a name="Limitations"></a>   
## <a name="limitations-to-applying-slas-in-dynamics-365-for-customer-engagement-apps"></a>Limitations to applying SLAs in Dynamics 365 for Customer Engagement apps
 In [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] apps, the following limitations are applicable for SLAs per [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance (organization):  
  
- You can have a maximum of 7 entities that can have active SLAs. You will encounter an error on activating an SLA if this limit is exceeded.  
  
- You can have a maximum of 5 SLA KPIs per entity for active SLAs. You will encounter an error on activating an SLA if this limit is exceeded. This limit is not applicable for the `Incident` entity.  
  
  These limits aren't applicable for [!INCLUDE[pn-crm-op-edition](../includes/pn-crm-op-edition.md)] apps.  
  
[!INCLUDE[cc_sdk_onpremises_note](../includes/cc-sdk-onpremises-note.md)]

### <a name="see-also"></a>Xem thêm  
 [Service entities in Customer Engagement](service-entities.md)   
 [Enhanced service level agreements (SLAs)](../admin/enhanced-service-level-agreements.md)
