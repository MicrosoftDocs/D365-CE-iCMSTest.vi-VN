---
title: Activity entities (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: In Dynamics 365 for Customer Engagement (online), activities are tasks that you or your teams perform when they contact customers, for example, sending letters or making telephone calls.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: c433ebc0-f3c1-47a4-a7df-8ffe821b51c0
caps.latest.revision: 32
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: f1742fa89357a16d45ca97608f1241ead5419f04
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388821"
---
# <a name="activity-entities"></a><span data-ttu-id="0545c-103">Thực thể hoạt động</span><span class="sxs-lookup"><span data-stu-id="0545c-103">Activity entities</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)] 

<span data-ttu-id="0545c-104">In [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps, activities are tasks that you or your teams perform when they contact customers, for example, sending letters or making telephone calls.</span><span class="sxs-lookup"><span data-stu-id="0545c-104">In [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps, activities are tasks that you or your teams perform when they contact customers, for example, sending letters or making telephone calls.</span></span> <span data-ttu-id="0545c-105">You  can create activities for yourselves, can assign them to someone else, or can share them with other users or teams.</span><span class="sxs-lookup"><span data-stu-id="0545c-105">You  can create activities for yourselves, can assign them to someone else, or can share them with other users or teams.</span></span> <span data-ttu-id="0545c-106">An activity is any action which can be entered  on a calendar  and has time dimensions (start time, stop time, due date, and duration) that help determine when the action occurred or is to occur.</span><span class="sxs-lookup"><span data-stu-id="0545c-106">An activity is any action which can be entered  on a calendar  and has time dimensions (start time, stop time, due date, and duration) that help determine when the action occurred or is to occur.</span></span> <span data-ttu-id="0545c-107">Activities has some basic properties that help determine what action the activity represents, for example, subject and description.</span><span class="sxs-lookup"><span data-stu-id="0545c-107">Activities has some basic properties that help determine what action the activity represents, for example, subject and description.</span></span> <span data-ttu-id="0545c-108">An activity state can be opened, canceled, or completed.</span><span class="sxs-lookup"><span data-stu-id="0545c-108">An activity state can be opened, canceled, or completed.</span></span> <span data-ttu-id="0545c-109">The completed status of an activity will have several substatus values associated with it to clarify the way that the activity was completed.</span><span class="sxs-lookup"><span data-stu-id="0545c-109">The completed status of an activity will have several substatus values associated with it to clarify the way that the activity was completed.</span></span>
  
 <span data-ttu-id="0545c-110">Activities involve one or more participants, called activity parties in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="0545c-110">Activities involve one or more participants, called activity parties in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps.</span></span> <span data-ttu-id="0545c-111">For a meeting activity, the participants are those contacts or users attending the meeting.</span><span class="sxs-lookup"><span data-stu-id="0545c-111">For a meeting activity, the participants are those contacts or users attending the meeting.</span></span> <span data-ttu-id="0545c-112">For a telephone call or fax activity, the parties are the caller and the person who is called.</span><span class="sxs-lookup"><span data-stu-id="0545c-112">For a telephone call or fax activity, the parties are the caller and the person who is called.</span></span> <span data-ttu-id="0545c-113">The following diagram shows the entity relationships for activities.</span><span class="sxs-lookup"><span data-stu-id="0545c-113">The following diagram shows the entity relationships for activities.</span></span>  
  
 <span data-ttu-id="0545c-114">![Activity diagram](media/entity-model-activity.gif "Activity diagram")</span><span class="sxs-lookup"><span data-stu-id="0545c-114">![Activity diagram](media/entity-model-activity.gif "Activity diagram")</span></span>  
  
 <span data-ttu-id="0545c-115">To support the communication needs of the modern-day business, such as instant messaging (IM) and SMS, you can create custom activities in [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="0545c-115">To support the communication needs of the modern-day business, such as instant messaging (IM) and SMS, you can create custom activities in [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps.</span></span>  
  
 <span data-ttu-id="0545c-116">**Other activity entities**</span><span class="sxs-lookup"><span data-stu-id="0545c-116">**Other activity entities**</span></span>  
  
-   <span data-ttu-id="0545c-117">The scheduling activities enables you to schedule your services and resources, and thus define work schedules.</span><span class="sxs-lookup"><span data-stu-id="0545c-117">The scheduling activities enables you to schedule your services and resources, and thus define work schedules.</span></span> <span data-ttu-id="0545c-118">The scheduling activity entities are `Appointment`, `ServiceAppointment`, and `RecurringAppointmentMaster`.</span><span class="sxs-lookup"><span data-stu-id="0545c-118">The scheduling activity entities are `Appointment`, `ServiceAppointment`, and `RecurringAppointmentMaster`.</span></span> <span data-ttu-id="0545c-119">For more information, see [Schedule and Appointment Entities](schedule-appointment-entities.md).</span><span class="sxs-lookup"><span data-stu-id="0545c-119">For more information, see [Schedule and Appointment Entities](schedule-appointment-entities.md).</span></span>  
  
-   <span data-ttu-id="0545c-120">The marketing activity, `CampaignResponse`, enables you to capture responses from the customers for a marketing campaign, while the `CampaignActivity` entity represents a step in a campaign.</span><span class="sxs-lookup"><span data-stu-id="0545c-120">The marketing activity, `CampaignResponse`, enables you to capture responses from the customers for a marketing campaign, while the `CampaignActivity` entity represents a step in a campaign.</span></span> <span data-ttu-id="0545c-121">For more information, see [Campaign Entities](campaign-entities.md).</span><span class="sxs-lookup"><span data-stu-id="0545c-121">For more information, see [Campaign Entities](campaign-entities.md).</span></span>  
  
-   <span data-ttu-id="0545c-122">The sales force automation entities `OpportunityClose`, `OrderClose`, and `QuoteClose` activities capture information about each of these events.</span><span class="sxs-lookup"><span data-stu-id="0545c-122">The sales force automation entities `OpportunityClose`, `OrderClose`, and `QuoteClose` activities capture information about each of these events.</span></span> <span data-ttu-id="0545c-123">For more information, see [Sales Entities (Lead, Opportunity, Competitor, Quote, Order, Invoice)](sales-entities-lead-opportunity-competitor-quote-order-invoice.md).</span><span class="sxs-lookup"><span data-stu-id="0545c-123">For more information, see [Sales Entities (Lead, Opportunity, Competitor, Quote, Order, Invoice)](sales-entities-lead-opportunity-competitor-quote-order-invoice.md).</span></span>  
  
-   <span data-ttu-id="0545c-124">The customer service entity `IncidentResolution` activity captures information about the resolution of a case.</span><span class="sxs-lookup"><span data-stu-id="0545c-124">The customer service entity `IncidentResolution` activity captures information about the resolution of a case.</span></span> <span data-ttu-id="0545c-125">For more information, see [Incident (Case) Entities](incident-case-entities.md).</span><span class="sxs-lookup"><span data-stu-id="0545c-125">For more information, see [Incident (Case) Entities](incident-case-entities.md).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="0545c-126">In This Section</span><span class="sxs-lookup"><span data-stu-id="0545c-126">In This Section</span></span>  
 [<span data-ttu-id="0545c-127">Custom Activities in Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="0545c-127">Custom Activities in Dynamics 365 for Customer Engagement apps</span></span>](custom-activities.md)  
  
 [<span data-ttu-id="0545c-128">Activity Pointer (Activity) Entity</span><span class="sxs-lookup"><span data-stu-id="0545c-128">Activity Pointer (Activity) Entity</span></span>](activitypointer-activity-entity.md)  
  
 [<span data-ttu-id="0545c-129">Activity Party Entity</span><span class="sxs-lookup"><span data-stu-id="0545c-129">Activity Party Entity</span></span>](activityparty-entity.md)  
  
 [<span data-ttu-id="0545c-130">Task, Fax, Phone Call, and Letter Activity Entities</span><span class="sxs-lookup"><span data-stu-id="0545c-130">Task, Fax, Phone Call, and Letter Activity Entities</span></span>](task-fax-phone-call-letter-activity-entities.md)  
  
 [<span data-ttu-id="0545c-131">E-mail Activity Entities</span><span class="sxs-lookup"><span data-stu-id="0545c-131">E-mail Activity Entities</span></span>](email-activity-entities.md)  
  
 [<span data-ttu-id="0545c-132">Sample Code for Activity Entities</span><span class="sxs-lookup"><span data-stu-id="0545c-132">Sample Code for Activity Entities</span></span>](sample-code-activity-entities.md)  
  
## <a name="related-sections"></a><span data-ttu-id="0545c-133">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="0545c-133">Related Sections</span></span>  
 [<span data-ttu-id="0545c-134">Model Your Business Data with Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="0545c-134">Model Your Business Data with Dynamics 365 for Customer Engagement apps</span></span>](model-business-data.md)  
  
 [<span data-ttu-id="0545c-135">Server-side Synchronization Entities</span><span class="sxs-lookup"><span data-stu-id="0545c-135">Server-side Synchronization Entities</span></span>](server-side-synchronization-entities.md)  
  
 [<span data-ttu-id="0545c-136">Customize Entity Metadata</span><span class="sxs-lookup"><span data-stu-id="0545c-136">Customize Entity Metadata</span></span>](customize-entity-metadata.md)
