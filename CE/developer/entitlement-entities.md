---
title: Entitlement entities (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Learn about entitlement entities that allow you to set a default entitlement for a customer and control entitlement terms for incidents.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 30023495-fc7e-4b42-aa61-29d43647606a
caps.latest.revision: 20
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4d63e1a9acec4e3df9c7f8ebab7926db7b85a686
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387729"
---
# <a name="entitlement-entities"></a>Entitlement entities

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

Entitlements specify the support term based on number of hours or number of cases. Mức hỗ trợ của khách hàng có thể khác nhau dựa trên sản phẩm hay dịch vụ mà khách hàng đã mua. Khách hàng đã mua những sản phẩm khác nhau có thể có quyền hưởng nhiều mức hỗ trợ khác nhau. Thông tin này giúp tổng đài viên hỗ trợ khách hàng xác minh khách hàng đủ điều kiện cho quyền nào và dựa vào đó tạo trường hợp cho họ.  
  
 Entitlement channel records contain the total terms and remaining terms for each channel in an entitlement. Default channels include Phone, Email, Web, [!INCLUDE[tn_facebook](../includes/tn-facebook.md)], and [!INCLUDE[tn_twitter](../includes/tn-twitter.md)]. You can add custom channels by editing the `incident_caseorigincode` global option set.  
  
 Use entitlement templates and entitlement template channels to create entitlements prefilled with the basic information like the start and end date, service level agreement (SLA), allocation type, and total term. You can also relate entitlement channels and products to entitlement templates. Ví dụ, tạo mẫu cho một quyền lợi tiêu chuẩn, và sau đó áp dụng mẫu này cho mọi khách hàng tiêu chuẩn trong tổ chức của bạn.  
  
 If you’re using [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] or [!INCLUDE[pn_crm_2016_onprem](../includes/pn-crm-2016-onprem.md)] or later, you can also:  
  
- **Set a default entitlement for a customer**: When you create or update an incident (case) for the customer, the default entitlement is automatically applied to the incident. For incident updates, the default entitlement is automatically applied only if you are updating the customer, contact, or product information for an incident record. This is especially useful when you have a single entitlement per customer in your organization, and want the default entitlement to be automatically applied to the incidents that are created or updated for each customer instead of the customer service representatives having to manually select the entitlement, and apply it to the incident.  
  
     Use the `Entitlement.IsDefault` attribute to specify the default entitlement for a customer. Only an active entitlement for a customer can be set as the default entitlement. If an entitlement is already set as default for a customer, setting another entitlement as default for the customer will override the existing one, and set the new entitlement as default. For the default entitlement for a customer to be applied automatically to all the new or modified incidents for the customer, the `Organization.AutoApplyDefaultonCaseCreate` and `Organization.AutoApplyDefaultonCaseUpdate` attributes must be set to 1 (true).  
  
- **Control entitlement terms for incidents (cases)**: When an incident is created and an entitlement is applied to it, the entitlement terms from the associated entitlement are decremented. However, at times you don’t want the entitlement terms to be decremented for an incident (for example, faulty part is installed). To prevent the entitlement terms to be decremented for an incident, set the `Incident.DecrementEntitlementTerm` attribute to 0 (false).  
  
     If you accidentally prevented the entitlement terms to be decremented for a case, you can revert it as follows:  
  
  - If the associated entitlement is configured to have its remaining term decremented on case creation, setting the `Incident.DecrementEntitlementTerm` attribute back to 1 (true) won’t decrement the entitlement term automatically. You have to explicitly decrement from the remaining terms of the associated entitlement using workflow or programmatically.  
  
  - If the associated entitlement is configured to have its remaining term decremented on case resolution, set the `Incident.DecrementEntitlementTerm` back to 1 (true). This ensures that the entitlement terms get decremented when the case is resolved.  
  
    To set the `Incident.DecrementEntitlementTerm` attribute for an incident record, you must have the privileges on the incident record, and have the new `prvControlDecrementTerm` privilege. By default, the `prvControlDecrementTerm` privilege is available to only System Administrator and CSR Manager roles.  
  
## <a name="in-this-section"></a>In This Section  
 [Entitlement Entity](entities/entitlement.md)  
  
 [EntitlementChannel Entity](entities/entitlementchannel.md)  
  
 [EntitlementTemplate Entity](entities/entitlementtemplate.md)  
  
 [EntitlementTemplateChannel Entity](entities/entitlementtemplatechannel.md)  
  
## <a name="related-sections"></a>Các phần liên quan  
 [Incident (Case) Entities](incident-case-entities.md)