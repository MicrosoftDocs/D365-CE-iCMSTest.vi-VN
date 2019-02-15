---
title: Types of calendars (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 6f88c4ff-876e-4108-885f-98700436d461
caps.latest.revision: 11
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 17edbf15b81bca451f70ef9f115d1d0825b6aae1
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386658"
---
# <a name="types-of-calendars"></a><span data-ttu-id="a29e3-102">Types of calendars</span><span class="sxs-lookup"><span data-stu-id="a29e3-102">Types of calendars</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="a29e3-103">The calendar entity was modified to support additional types of calendars in [!INCLUDE[pn_v6_online_ur1_shortest](../includes/pn-v6-online-ur1-shortest.md)] and [!INCLUDE[pn_crm_2015_service_pack_1_op_short](../includes/pn-crm-2015-service-pack-1-op-short.md)].</span><span class="sxs-lookup"><span data-stu-id="a29e3-103">The calendar entity was modified to support additional types of calendars in [!INCLUDE[pn_v6_online_ur1_shortest](../includes/pn-v6-online-ur1-shortest.md)] and [!INCLUDE[pn_crm_2015_service_pack_1_op_short](../includes/pn-crm-2015-service-pack-1-op-short.md)].</span></span>  
  
## <a name="calendar-type"></a><span data-ttu-id="a29e3-104">Calendar type</span><span class="sxs-lookup"><span data-stu-id="a29e3-104">Calendar type</span></span>  
 <span data-ttu-id="a29e3-105">The `Type` Picklist attribute contains the following options:</span><span class="sxs-lookup"><span data-stu-id="a29e3-105">The `Type` Picklist attribute contains the following options:</span></span>  
  
|<span data-ttu-id="a29e3-106">Value</span><span class="sxs-lookup"><span data-stu-id="a29e3-106">Value</span></span>|<span data-ttu-id="a29e3-107">Nhãn</span><span class="sxs-lookup"><span data-stu-id="a29e3-107">Label</span></span>|<span data-ttu-id="a29e3-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="a29e3-108">Description</span></span>|  
|-----------|-----------|-----------------|  
|<span data-ttu-id="a29e3-109">0</span><span class="sxs-lookup"><span data-stu-id="a29e3-109">0</span></span>|<span data-ttu-id="a29e3-110">Mặc định</span><span class="sxs-lookup"><span data-stu-id="a29e3-110">Default</span></span>|<span data-ttu-id="a29e3-111">All calendars that are not customer service, holiday schedule, or inner calendars.</span><span class="sxs-lookup"><span data-stu-id="a29e3-111">All calendars that are not customer service, holiday schedule, or inner calendars.</span></span>|  
|<span data-ttu-id="a29e3-112">1</span><span class="sxs-lookup"><span data-stu-id="a29e3-112">1</span></span>|<span data-ttu-id="a29e3-113">Customer Service</span><span class="sxs-lookup"><span data-stu-id="a29e3-113">Customer Service</span></span>|<span data-ttu-id="a29e3-114">Service calendars for customer service.</span><span class="sxs-lookup"><span data-stu-id="a29e3-114">Service calendars for customer service.</span></span>|  
|<span data-ttu-id="a29e3-115">2</span><span class="sxs-lookup"><span data-stu-id="a29e3-115">2</span></span>|<span data-ttu-id="a29e3-116">Holiday Schedule</span><span class="sxs-lookup"><span data-stu-id="a29e3-116">Holiday Schedule</span></span>|<span data-ttu-id="a29e3-117">Holiday schedule calendars for customer service.</span><span class="sxs-lookup"><span data-stu-id="a29e3-117">Holiday schedule calendars for customer service.</span></span>|  
|<span data-ttu-id="a29e3-118">-1</span><span class="sxs-lookup"><span data-stu-id="a29e3-118">-1</span></span>|<span data-ttu-id="a29e3-119">Inner Calendar type</span><span class="sxs-lookup"><span data-stu-id="a29e3-119">Inner Calendar type</span></span>|<span data-ttu-id="a29e3-120">Inner Calendars are used by other calendars to build a graph of time slots available for customer service or service scheduling to be performed.</span><span class="sxs-lookup"><span data-stu-id="a29e3-120">Inner Calendars are used by other calendars to build a graph of time slots available for customer service or service scheduling to be performed.</span></span>|  
  
### <a name="customer-service-calendars"></a><span data-ttu-id="a29e3-121">Customer service calendars</span><span class="sxs-lookup"><span data-stu-id="a29e3-121">Customer service calendars</span></span>  
 <span data-ttu-id="a29e3-122">Customer service calendars exist to calculate performance against service level agreements (SLAs).</span><span class="sxs-lookup"><span data-stu-id="a29e3-122">Customer service calendars exist to calculate performance against service level agreements (SLAs).</span></span> <span data-ttu-id="a29e3-123">SLAs are frequently based on key performance indicators (KPIs) based on time, such as duration for first response or a time limit before escalation.</span><span class="sxs-lookup"><span data-stu-id="a29e3-123">SLAs are frequently based on key performance indicators (KPIs) based on time, such as duration for first response or a time limit before escalation.</span></span> <span data-ttu-id="a29e3-124">When these time limits are restricted to periods when customer service operations are open, calculations to enforce these agreements must include data from the customer service calendar.</span><span class="sxs-lookup"><span data-stu-id="a29e3-124">When these time limits are restricted to periods when customer service operations are open, calculations to enforce these agreements must include data from the customer service calendar.</span></span>  
  
 <span data-ttu-id="a29e3-125">Customer service calendars define regular weekly schedules.</span><span class="sxs-lookup"><span data-stu-id="a29e3-125">Customer service calendars define regular weekly schedules.</span></span> <span data-ttu-id="a29e3-126">Events that don’t fall into those regular schedules are usually holidays.</span><span class="sxs-lookup"><span data-stu-id="a29e3-126">Events that don’t fall into those regular schedules are usually holidays.</span></span> <span data-ttu-id="a29e3-127">A customer service calendar can be associated with a holiday schedule to provide a complete description of the times when customer services are available.</span><span class="sxs-lookup"><span data-stu-id="a29e3-127">A customer service calendar can be associated with a holiday schedule to provide a complete description of the times when customer services are available.</span></span>  
  
### <a name="service-scheduling-calendars"></a><span data-ttu-id="a29e3-128">Service scheduling calendars</span><span class="sxs-lookup"><span data-stu-id="a29e3-128">Service scheduling calendars</span></span>  
 <span data-ttu-id="a29e3-129">Service scheduling uses the default calendar type.</span><span class="sxs-lookup"><span data-stu-id="a29e3-129">Service scheduling uses the default calendar type.</span></span> <span data-ttu-id="a29e3-130">Business closure calendars can be defined and shared on service and resource entities.</span><span class="sxs-lookup"><span data-stu-id="a29e3-130">Business closure calendars can be defined and shared on service and resource entities.</span></span> <span data-ttu-id="a29e3-131">The scheduling engine makes sure that all appropriate calendar rules are considered for an appointment request.</span><span class="sxs-lookup"><span data-stu-id="a29e3-131">The scheduling engine makes sure that all appropriate calendar rules are considered for an appointment request.</span></span>  
  
 <span data-ttu-id="a29e3-132">In addition to free/busy times, you can define effort (required/available) constraints on the `CalendarRule` entity.</span><span class="sxs-lookup"><span data-stu-id="a29e3-132">In addition to free/busy times, you can define effort (required/available) constraints on the `CalendarRule` entity.</span></span> <span data-ttu-id="a29e3-133">These constraints are defined as the effort that is available from a resource to perform, deliver, or repeat a particular service at a given time.</span><span class="sxs-lookup"><span data-stu-id="a29e3-133">These constraints are defined as the effort that is available from a resource to perform, deliver, or repeat a particular service at a given time.</span></span> <span data-ttu-id="a29e3-134">Similarly, each service defines the effort that is required from the required pool of resources to complete one unit of service for its specified duration.</span><span class="sxs-lookup"><span data-stu-id="a29e3-134">Similarly, each service defines the effort that is required from the required pool of resources to complete one unit of service for its specified duration.</span></span> <span data-ttu-id="a29e3-135">The scheduling engine automatically computes the appropriate time blocks for an appointment when the total effort that is required for a given service is less than or equal to the total available effort for all the required resources.</span><span class="sxs-lookup"><span data-stu-id="a29e3-135">The scheduling engine automatically computes the appropriate time blocks for an appointment when the total effort that is required for a given service is less than or equal to the total available effort for all the required resources.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="a29e3-136">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="a29e3-136">See also</span></span>  
 <span data-ttu-id="a29e3-137">[Calendar Entities](calendar-entities.md) </span><span class="sxs-lookup"><span data-stu-id="a29e3-137">[Calendar Entities](calendar-entities.md) </span></span>  
 <span data-ttu-id="a29e3-138">[Calendar Entity](entities/calendar.md) </span><span class="sxs-lookup"><span data-stu-id="a29e3-138">[Calendar Entity](entities/calendar.md) </span></span>  
 <xref:Microsoft.Dynamics.CRM.calendarrule>
