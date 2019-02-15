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
# <a name="apply-slas-to-entities"></a><span data-ttu-id="b622e-104">Apply SLAs to entities</span><span class="sxs-lookup"><span data-stu-id="b622e-104">Apply SLAs to entities</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="b622e-105">Service level agreements (SLAs) in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps help you define the level of service or support that your organization agrees to offer a customer by including items to define metrics or key performance indicators (KPIs) to attain the service level.</span><span class="sxs-lookup"><span data-stu-id="b622e-105">Service level agreements (SLAs) in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps help you define the level of service or support that your organization agrees to offer a customer by including items to define metrics or key performance indicators (KPIs) to attain the service level.</span></span> <span data-ttu-id="b622e-106">You can apply SLAs to custom entities and the following system entities:</span><span class="sxs-lookup"><span data-stu-id="b622e-106">You can apply SLAs to custom entities and the following system entities:</span></span>  
  
-   <span data-ttu-id="b622e-107">Tất cả thực thể hoạt động (chẳng hạn như Email, Tác vụ và Cuộc hẹn) ngoại trừ các cuộc hẹn định kỳ (RecurringAppointmentMaster)</span><span class="sxs-lookup"><span data-stu-id="b622e-107">All activity entities (such as Email, Task, and Appointment) except recurring appointments (RecurringAppointmentMaster)</span></span>  
  
-   <span data-ttu-id="b622e-108">Khách hàng</span><span class="sxs-lookup"><span data-stu-id="b622e-108">Account</span></span>  
  
-   <span data-ttu-id="b622e-109">người liên hệ</span><span class="sxs-lookup"><span data-stu-id="b622e-109">Contact</span></span>  
  
-   <span data-ttu-id="b622e-110">Hóa đơn</span><span class="sxs-lookup"><span data-stu-id="b622e-110">Invoice</span></span>  
  
-   <span data-ttu-id="b622e-111">Incident (Case)</span><span class="sxs-lookup"><span data-stu-id="b622e-111">Incident (Case)</span></span>  
  
-   <span data-ttu-id="b622e-112">Cơ hội</span><span class="sxs-lookup"><span data-stu-id="b622e-112">Opportunity</span></span>  
  
-   <span data-ttu-id="b622e-113">Báo giá</span><span class="sxs-lookup"><span data-stu-id="b622e-113">Quote</span></span>  
  
-   <span data-ttu-id="b622e-114">Khách hàng tiềm năng</span><span class="sxs-lookup"><span data-stu-id="b622e-114">Lead</span></span>  
  
-   <span data-ttu-id="b622e-115">SalesOrder (Order)</span><span class="sxs-lookup"><span data-stu-id="b622e-115">SalesOrder (Order)</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b622e-116">SLA support for entities, in addition to the Incident entity, was introduced in [!INCLUDE[pn_crm_8_1_0_online_subsequent](../includes/pn-crm-8-1-0-online-subsequent.md)] and Dynamics 365 for Customer Engagement apps Service Pack 1 (on-premises).</span><span class="sxs-lookup"><span data-stu-id="b622e-116">SLA support for entities, in addition to the Incident entity, was introduced in [!INCLUDE[pn_crm_8_1_0_online_subsequent](../includes/pn-crm-8-1-0-online-subsequent.md)] and Dynamics 365 for Customer Engagement apps Service Pack 1 (on-premises).</span></span>  
  
<a name="EnableSLAs"></a>   
## <a name="enable-entities-for-applying-slas"></a><span data-ttu-id="b622e-117">Enable entities for applying SLAs</span><span class="sxs-lookup"><span data-stu-id="b622e-117">Enable entities for applying SLAs</span></span>  
 <span data-ttu-id="b622e-118">To apply SLAs to an entity, you must set the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsSLAEnabled> attribute to true for the entity.</span><span class="sxs-lookup"><span data-stu-id="b622e-118">To apply SLAs to an entity, you must set the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsSLAEnabled> attribute to true for the entity.</span></span> <span data-ttu-id="b622e-119">You can’t change this setting after it’s been enabled.</span><span class="sxs-lookup"><span data-stu-id="b622e-119">You can’t change this setting after it’s been enabled.</span></span> <span data-ttu-id="b622e-120">By default, the `Incident` entity is enabled for SLAs.</span><span class="sxs-lookup"><span data-stu-id="b622e-120">By default, the `Incident` entity is enabled for SLAs.</span></span>  
  
 <span data-ttu-id="b622e-121">You can also use the customization tool to enable entities for SLAs.</span><span class="sxs-lookup"><span data-stu-id="b622e-121">You can also use the customization tool to enable entities for SLAs.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="b622e-122">[Enable entities for service level agreements](../customer-service/enable-entities-service-level-agreements.md)</span><span class="sxs-lookup"><span data-stu-id="b622e-122">[Enable entities for service level agreements](../customer-service/enable-entities-service-level-agreements.md)</span></span>  
  
 <span data-ttu-id="b622e-123">After you have enabled an entity forSLAs, new SLA-related attributes, such as `SLAId` and `SLAInvokedId`, will be automatically added to the entity.</span><span class="sxs-lookup"><span data-stu-id="b622e-123">After you have enabled an entity forSLAs, new SLA-related attributes, such as `SLAId` and `SLAInvokedId`, will be automatically added to the entity.</span></span>  
  
<a name="CreateSLAKPI"></a>   
## <a name="create-sla-kpis"></a><span data-ttu-id="b622e-124">Create SLA KPIs</span><span class="sxs-lookup"><span data-stu-id="b622e-124">Create SLA KPIs</span></span>  
 <span data-ttu-id="b622e-125">To programmatically create SLA KPIs for an entity, create a lookup attribute on any SLA-enabled entity, and then set a relationship for that attribute to the `SLAKPIInstance` entity.</span><span class="sxs-lookup"><span data-stu-id="b622e-125">To programmatically create SLA KPIs for an entity, create a lookup attribute on any SLA-enabled entity, and then set a relationship for that attribute to the `SLAKPIInstance` entity.</span></span>  
  
<a name="ApplySLA"></a>   
## <a name="apply-slas-to-entity-records"></a><span data-ttu-id="b622e-126">Apply SLAs to entity records</span><span class="sxs-lookup"><span data-stu-id="b622e-126">Apply SLAs to entity records</span></span>  
 <span data-ttu-id="b622e-127">Using the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] web client, you can create SLAs for an SLA-enabled entity, and set an SLA as default for the entity so that it is applied automatically to any new entity records.</span><span class="sxs-lookup"><span data-stu-id="b622e-127">Using the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] web client, you can create SLAs for an SLA-enabled entity, and set an SLA as default for the entity so that it is applied automatically to any new entity records.</span></span>  
  
 <span data-ttu-id="b622e-128">However, if you want to manually apply SLAs to entity records based on any custom business requirement, you can programmatically update the entity record to set the `SLAId` attribute value to the desired active SLA record.</span><span class="sxs-lookup"><span data-stu-id="b622e-128">However, if you want to manually apply SLAs to entity records based on any custom business requirement, you can programmatically update the entity record to set the `SLAId` attribute value to the desired active SLA record.</span></span>  
  
<a name="Limitations"></a>   
## <a name="limitations-to-applying-slas-in-dynamics-365-for-customer-engagement-apps"></a><span data-ttu-id="b622e-129">Limitations to applying SLAs in Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="b622e-129">Limitations to applying SLAs in Dynamics 365 for Customer Engagement apps</span></span>
 <span data-ttu-id="b622e-130">In [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] apps, the following limitations are applicable for SLAs per [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance (organization):</span><span class="sxs-lookup"><span data-stu-id="b622e-130">In [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] apps, the following limitations are applicable for SLAs per [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance (organization):</span></span>  
  
- <span data-ttu-id="b622e-131">You can have a maximum of 7 entities that can have active SLAs.</span><span class="sxs-lookup"><span data-stu-id="b622e-131">You can have a maximum of 7 entities that can have active SLAs.</span></span> <span data-ttu-id="b622e-132">You will encounter an error on activating an SLA if this limit is exceeded.</span><span class="sxs-lookup"><span data-stu-id="b622e-132">You will encounter an error on activating an SLA if this limit is exceeded.</span></span>  
  
- <span data-ttu-id="b622e-133">You can have a maximum of 5 SLA KPIs per entity for active SLAs.</span><span class="sxs-lookup"><span data-stu-id="b622e-133">You can have a maximum of 5 SLA KPIs per entity for active SLAs.</span></span> <span data-ttu-id="b622e-134">You will encounter an error on activating an SLA if this limit is exceeded.</span><span class="sxs-lookup"><span data-stu-id="b622e-134">You will encounter an error on activating an SLA if this limit is exceeded.</span></span> <span data-ttu-id="b622e-135">This limit is not applicable for the `Incident` entity.</span><span class="sxs-lookup"><span data-stu-id="b622e-135">This limit is not applicable for the `Incident` entity.</span></span>  
  
  <span data-ttu-id="b622e-136">These limits aren't applicable for [!INCLUDE[pn-crm-op-edition](../includes/pn-crm-op-edition.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="b622e-136">These limits aren't applicable for [!INCLUDE[pn-crm-op-edition](../includes/pn-crm-op-edition.md)] apps.</span></span>  
  
[!INCLUDE[cc_sdk_onpremises_note](../includes/cc-sdk-onpremises-note.md)]

### <a name="see-also"></a><span data-ttu-id="b622e-137">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="b622e-137">See also</span></span>  
 <span data-ttu-id="b622e-138">[Service entities in Customer Engagement](service-entities.md) </span><span class="sxs-lookup"><span data-stu-id="b622e-138">[Service entities in Customer Engagement](service-entities.md) </span></span>  
 [<span data-ttu-id="b622e-139">Enhanced service level agreements (SLAs)</span><span class="sxs-lookup"><span data-stu-id="b622e-139">Enhanced service level agreements (SLAs)</span></span>](../admin/enhanced-service-level-agreements.md)
