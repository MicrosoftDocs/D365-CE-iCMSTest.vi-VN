---
title: Incident (case) hierarchies (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Learn about incident (case) hierarchies that allow you to create parent and child case settings and rules for deactivating cases.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: ab5d6aed-52a9-4f4f-95a3-facaf313c088
caps.latest.revision: 17
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: f8db95c53f8129ed353d943b560e9cd123e4f9ff
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387505"
---
# <a name="incident-case-hierarchies"></a><span data-ttu-id="bcc6a-103">Incident (case) hierarchies</span><span class="sxs-lookup"><span data-stu-id="bcc6a-103">Incident (case) hierarchies</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="bcc6a-104">Incident entities can be related hierarchically.</span><span class="sxs-lookup"><span data-stu-id="bcc6a-104">Incident entities can be related hierarchically.</span></span> <span data-ttu-id="bcc6a-105">An administrator can use the **Parent and Child case settings** to configure specific behaviors for these relationships.</span><span class="sxs-lookup"><span data-stu-id="bcc6a-105">An administrator can use the **Parent and Child case settings** to configure specific behaviors for these relationships.</span></span>  
  
 <span data-ttu-id="bcc6a-106">Within the application, people can create a new child incident or associate an existing incident to a parent incident.</span><span class="sxs-lookup"><span data-stu-id="bcc6a-106">Within the application, people can create a new child incident or associate an existing incident to a parent incident.</span></span> <span data-ttu-id="bcc6a-107">This association uses the `incident_parent_incident` relationship.</span><span class="sxs-lookup"><span data-stu-id="bcc6a-107">This association uses the `incident_parent_incident` relationship.</span></span> <span data-ttu-id="bcc6a-108">When you create a new incident to be associated using this relationship, use the <xref:Microsoft.Crm.Sdk.Messages.InitializeFromRequest> message to initialize the new incident with the default values defined in the attribute mapping for this relationship.</span><span class="sxs-lookup"><span data-stu-id="bcc6a-108">When you create a new incident to be associated using this relationship, use the <xref:Microsoft.Crm.Sdk.Messages.InitializeFromRequest> message to initialize the new incident with the default values defined in the attribute mapping for this relationship.</span></span>  
  
 <span data-ttu-id="bcc6a-109">The **Parent and Child case settings** allow easy access to specify the attribute mappings to this relationship, but they may also be set by editing the relationship in the application or programmatically.</span><span class="sxs-lookup"><span data-stu-id="bcc6a-109">The **Parent and Child case settings** allow easy access to specify the attribute mappings to this relationship, but they may also be set by editing the relationship in the application or programmatically.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="bcc6a-110">[Create and edit entity relationships](https://technet.microsoft.com/library/dn531171.aspx) and [Customize Entity and Attribute Mappings](customize-entity-attribute-mappings.md).</span><span class="sxs-lookup"><span data-stu-id="bcc6a-110">[Create and edit entity relationships](https://technet.microsoft.com/library/dn531171.aspx) and [Customize Entity and Attribute Mappings](customize-entity-attribute-mappings.md).</span></span>  
  
 <span data-ttu-id="bcc6a-111">The following behaviors are enforced for incident hierarchies:</span><span class="sxs-lookup"><span data-stu-id="bcc6a-111">The following behaviors are enforced for incident hierarchies:</span></span>  
  
-   <span data-ttu-id="bcc6a-112">Only one level of hierarchy is supported.</span><span class="sxs-lookup"><span data-stu-id="bcc6a-112">Only one level of hierarchy is supported.</span></span> <span data-ttu-id="bcc6a-113">You can’t set an incident as a parent while it is a child of another incident.</span><span class="sxs-lookup"><span data-stu-id="bcc6a-113">You can’t set an incident as a parent while it is a child of another incident.</span></span>  
  
    -   <span data-ttu-id="bcc6a-114">If you try to associate a child incident for an incident that is already the child of another incident you will get error -2147224493 with the message: “You can't create child cases for child cases.”</span><span class="sxs-lookup"><span data-stu-id="bcc6a-114">If you try to associate a child incident for an incident that is already the child of another incident you will get error -2147224493 with the message: “You can't create child cases for child cases.”</span></span>  
  
    -   <span data-ttu-id="bcc6a-115">If you try to associate an incident that is a parent incident as a child of another incident you will get error -2147224491 with the message: “You can't add a parent case as a child case.”</span><span class="sxs-lookup"><span data-stu-id="bcc6a-115">If you try to associate an incident that is a parent incident as a child of another incident you will get error -2147224491 with the message: “You can't add a parent case as a child case.”</span></span>  
  
-   <span data-ttu-id="bcc6a-116">Each incident can have up to 100 child incidents.</span><span class="sxs-lookup"><span data-stu-id="bcc6a-116">Each incident can have up to 100 child incidents.</span></span> <span data-ttu-id="bcc6a-117">If you try to create too many child incidents you will get error -2147224492 with the message: “A Parent Case cannot have more than 100 child cases.</span><span class="sxs-lookup"><span data-stu-id="bcc6a-117">If you try to create too many child incidents you will get error -2147224492 with the message: “A Parent Case cannot have more than 100 child cases.</span></span> <span data-ttu-id="bcc6a-118">Contact your administrator for more details.”</span><span class="sxs-lookup"><span data-stu-id="bcc6a-118">Contact your administrator for more details.”</span></span>  
  
-   <span data-ttu-id="bcc6a-119">Incidents associated with different parent incidents cannot be merged.</span><span class="sxs-lookup"><span data-stu-id="bcc6a-119">Incidents associated with different parent incidents cannot be merged.</span></span> <span data-ttu-id="bcc6a-120">The error message is “You can’t merge cases that have different parent cases.”</span><span class="sxs-lookup"><span data-stu-id="bcc6a-120">The error message is “You can’t merge cases that have different parent cases.”</span></span> <span data-ttu-id="bcc6a-121">You can use the <xref:Microsoft.Crm.Sdk.Messages.MergeRequest> message to merge incidents.</span><span class="sxs-lookup"><span data-stu-id="bcc6a-121">You can use the <xref:Microsoft.Crm.Sdk.Messages.MergeRequest> message to merge incidents.</span></span>  
  
### <a name="rules-for-deactivating-cases"></a><span data-ttu-id="bcc6a-122">Rules for deactivating cases</span><span class="sxs-lookup"><span data-stu-id="bcc6a-122">Rules for deactivating cases</span></span>  
 <span data-ttu-id="bcc6a-123">The **Parent and Child case settings** in the application also allow you to configure additional cascade closure preferences.</span><span class="sxs-lookup"><span data-stu-id="bcc6a-123">The **Parent and Child case settings** in the application also allow you to configure additional cascade closure preferences.</span></span> <span data-ttu-id="bcc6a-124">Depending on how the hierarchies are configured for the organization, specific rules around deactivating incidents should be followed to align with the preferences of the organization.</span><span class="sxs-lookup"><span data-stu-id="bcc6a-124">Depending on how the hierarchies are configured for the organization, specific rules around deactivating incidents should be followed to align with the preferences of the organization.</span></span> <span data-ttu-id="bcc6a-125">When an incident is deactivated, its state is set to either resolved or canceled.</span><span class="sxs-lookup"><span data-stu-id="bcc6a-125">When an incident is deactivated, its state is set to either resolved or canceled.</span></span>  
  
 <span data-ttu-id="bcc6a-126">When **Parent and Child case settings** are configured in the application, data is stored in the following Boolean attributes of the organization entity.</span><span class="sxs-lookup"><span data-stu-id="bcc6a-126">When **Parent and Child case settings** are configured in the application, data is stored in the following Boolean attributes of the organization entity.</span></span>  
  
|<span data-ttu-id="bcc6a-127">Thuộc tính</span><span class="sxs-lookup"><span data-stu-id="bcc6a-127">Attribute</span></span>|<span data-ttu-id="bcc6a-128">UI Label</span><span class="sxs-lookup"><span data-stu-id="bcc6a-128">UI Label</span></span>|  
|---------------|--------------|  
|`CascadeStatusUpdate`|<span data-ttu-id="bcc6a-129">**Close all child cases when parent case is closed**</span><span class="sxs-lookup"><span data-stu-id="bcc6a-129">**Close all child cases when parent case is closed**</span></span>|  
|`RestrictStatusUpdate`|<span data-ttu-id="bcc6a-130">**Don’t allow parent case closure until all child cases are closed**</span><span class="sxs-lookup"><span data-stu-id="bcc6a-130">**Don’t allow parent case closure until all child cases are closed**</span></span>|  
  
 <span data-ttu-id="bcc6a-131">Based on the values of these attributes the following rules are applied by the platform.</span><span class="sxs-lookup"><span data-stu-id="bcc6a-131">Based on the values of these attributes the following rules are applied by the platform.</span></span>  
  
|<span data-ttu-id="bcc6a-132">`CascadeStatusUpdate` value</span><span class="sxs-lookup"><span data-stu-id="bcc6a-132">`CascadeStatusUpdate` value</span></span>|<span data-ttu-id="bcc6a-133">`RestrictStatusUpdate` value</span><span class="sxs-lookup"><span data-stu-id="bcc6a-133">`RestrictStatusUpdate` value</span></span>|<span data-ttu-id="bcc6a-134">Tính chất</span><span class="sxs-lookup"><span data-stu-id="bcc6a-134">Behavior</span></span>|  
|---------------------------------|----------------------------------|--------------|  
|<span data-ttu-id="bcc6a-135">Sai</span><span class="sxs-lookup"><span data-stu-id="bcc6a-135">False</span></span>|<span data-ttu-id="bcc6a-136">false</span><span class="sxs-lookup"><span data-stu-id="bcc6a-136">false</span></span>|<span data-ttu-id="bcc6a-137">When the **Specify closure preference** option in the **Parent and Child case settings** is not selected, incidents can be deactivated regardless of the status of parent or child incidents.</span><span class="sxs-lookup"><span data-stu-id="bcc6a-137">When the **Specify closure preference** option in the **Parent and Child case settings** is not selected, incidents can be deactivated regardless of the status of parent or child incidents.</span></span>|  
|<span data-ttu-id="bcc6a-138">Sai</span><span class="sxs-lookup"><span data-stu-id="bcc6a-138">False</span></span>|<span data-ttu-id="bcc6a-139">true</span><span class="sxs-lookup"><span data-stu-id="bcc6a-139">true</span></span>|<span data-ttu-id="bcc6a-140">Parent incidents can’t be deactivated if any active child incidents exist.</span><span class="sxs-lookup"><span data-stu-id="bcc6a-140">Parent incidents can’t be deactivated if any active child incidents exist.</span></span> <span data-ttu-id="bcc6a-141">If you attempt to do this, you get error -2147224495 with the message: “You can't resolve the parent case because it has {0} active child cases.”</span><span class="sxs-lookup"><span data-stu-id="bcc6a-141">If you attempt to do this, you get error -2147224495 with the message: “You can't resolve the parent case because it has {0} active child cases.”</span></span>|  
|<span data-ttu-id="bcc6a-142">Đúng</span><span class="sxs-lookup"><span data-stu-id="bcc6a-142">True</span></span>|<span data-ttu-id="bcc6a-143">false</span><span class="sxs-lookup"><span data-stu-id="bcc6a-143">false</span></span>|<span data-ttu-id="bcc6a-144">When parent incidents are deactivated, any active child incidents are also deactivated.</span><span class="sxs-lookup"><span data-stu-id="bcc6a-144">When parent incidents are deactivated, any active child incidents are also deactivated.</span></span>|  
|<span data-ttu-id="bcc6a-145">Đúng</span><span class="sxs-lookup"><span data-stu-id="bcc6a-145">True</span></span>|<span data-ttu-id="bcc6a-146">true</span><span class="sxs-lookup"><span data-stu-id="bcc6a-146">true</span></span>|<span data-ttu-id="bcc6a-147">The application won’t allow both of these values to be set.</span><span class="sxs-lookup"><span data-stu-id="bcc6a-147">The application won’t allow both of these values to be set.</span></span> <span data-ttu-id="bcc6a-148">You shouldn’t set both of these organization attribute values to true.</span><span class="sxs-lookup"><span data-stu-id="bcc6a-148">You shouldn’t set both of these organization attribute values to true.</span></span>|  
  
### <a name="see-also"></a><span data-ttu-id="bcc6a-149">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="bcc6a-149">See also</span></span>  
 <span data-ttu-id="bcc6a-150">[Service Entities (Contract, Incident, Knowledge Base)](service-entities.md) </span><span class="sxs-lookup"><span data-stu-id="bcc6a-150">[Service Entities (Contract, Incident, Knowledge Base)](service-entities.md) </span></span>  
 <span data-ttu-id="bcc6a-151">[Incident (Case) Entities](incident-case-entities.md) </span><span class="sxs-lookup"><span data-stu-id="bcc6a-151">[Incident (Case) Entities](incident-case-entities.md) </span></span>  
 <span data-ttu-id="bcc6a-152">[Incident Entity](entities/incident.md) </span><span class="sxs-lookup"><span data-stu-id="bcc6a-152">[Incident Entity](entities/incident.md) </span></span>  
 <span data-ttu-id="bcc6a-153">[IncidentResolution Entity](entities/incidentresolution.md) </span><span class="sxs-lookup"><span data-stu-id="bcc6a-153">[IncidentResolution Entity](entities/incidentresolution.md) </span></span>  
 [<span data-ttu-id="bcc6a-154">Sample: Close an Incident</span><span class="sxs-lookup"><span data-stu-id="bcc6a-154">Sample: Close an Incident</span></span>](sample-close-incident.md)
