---
title: Schedule collections (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Schedule is a logical collection of appointments that contains the availability and assignments of a given resource.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- schedule and appointment entities, querying a schedule
- schedule and appointment entities, scheduling engine publishes changes
- schedules, definition
- schedules
- querying a schedule, schedule and appointment entities
- scheduling engine
- schedules, introduction
ms.assetid: 4d908509-0508-4cbc-bbe6-322326597970
caps.latest.revision: 23
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: e67f547f1b360577f591a7780b7f69eda51a24a3
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386955"
---
# <a name="schedule-collections"></a><span data-ttu-id="f9657-103">Schedule collections</span><span class="sxs-lookup"><span data-stu-id="f9657-103">Schedule collections</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="f9657-104">A *schedule* is a logical collection of appointments that contains the availability and assignments of a given resource.</span><span class="sxs-lookup"><span data-stu-id="f9657-104">A *schedule* is a logical collection of appointments that contains the availability and assignments of a given resource.</span></span> <span data-ttu-id="f9657-105">It is a logical collection of appointments with a scheduling interface.</span><span class="sxs-lookup"><span data-stu-id="f9657-105">It is a logical collection of appointments with a scheduling interface.</span></span> <span data-ttu-id="f9657-106">There is no schedule entity in the [!INCLUDE[cc-dyn365-ce-web-services](../includes/cc-dyn365-ce-web-services.md)].</span><span class="sxs-lookup"><span data-stu-id="f9657-106">There is no schedule entity in the [!INCLUDE[cc-dyn365-ce-web-services](../includes/cc-dyn365-ce-web-services.md)].</span></span> <span data-ttu-id="f9657-107">Instead, the service, resource specification, user, and equipment entities support the scheduling engine when booking appointments and service appointments.</span><span class="sxs-lookup"><span data-stu-id="f9657-107">Instead, the service, resource specification, user, and equipment entities support the scheduling engine when booking appointments and service appointments.</span></span> <span data-ttu-id="f9657-108">By using schedule messages, you can look for free or busy information, search for appointments, and book a specific appointment for a service and a set of resources.</span><span class="sxs-lookup"><span data-stu-id="f9657-108">By using schedule messages, you can look for free or busy information, search for appointments, and book a specific appointment for a service and a set of resources.</span></span>  
  
 <span data-ttu-id="f9657-109">Appointments stored in schedules are related to the owner of the schedule.</span><span class="sxs-lookup"><span data-stu-id="f9657-109">Appointments stored in schedules are related to the owner of the schedule.</span></span> <span data-ttu-id="f9657-110">It is only possible to ask the schedule for free or busy times within a given time period.</span><span class="sxs-lookup"><span data-stu-id="f9657-110">It is only possible to ask the schedule for free or busy times within a given time period.</span></span> <span data-ttu-id="f9657-111">The result of the operation is a collection of time blocks (appointments) that correspond to available or reserved time.</span><span class="sxs-lookup"><span data-stu-id="f9657-111">The result of the operation is a collection of time blocks (appointments) that correspond to available or reserved time.</span></span> <span data-ttu-id="f9657-112">You can create a schedule that represents the availability of a set of resources or even a set of activities or some arbitrary subset of service availability.</span><span class="sxs-lookup"><span data-stu-id="f9657-112">You can create a schedule that represents the availability of a set of resources or even a set of activities or some arbitrary subset of service availability.</span></span> <span data-ttu-id="f9657-113">To retrieve a schedule collection, use the retrieve messages listed in the following table.</span><span class="sxs-lookup"><span data-stu-id="f9657-113">To retrieve a schedule collection, use the retrieve messages listed in the following table.</span></span>  
  
 <span data-ttu-id="f9657-114">The scheduling engine must know when changes are made to several different entities in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].</span><span class="sxs-lookup"><span data-stu-id="f9657-114">The scheduling engine must know when changes are made to several different entities in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].</span></span> <span data-ttu-id="f9657-115">When changes are made, [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] automatically schedules an asynchronous system job to publish the changes.</span><span class="sxs-lookup"><span data-stu-id="f9657-115">When changes are made, [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] automatically schedules an asynchronous system job to publish the changes.</span></span> <span data-ttu-id="f9657-116">This occurs five minutes after the change, whether the change occurs through the user interface or through Web service methods.</span><span class="sxs-lookup"><span data-stu-id="f9657-116">This occurs five minutes after the change, whether the change occurs through the user interface or through Web service methods.</span></span>  
  
## <a name="supported-messages"></a><span data-ttu-id="f9657-117">Supported messages</span><span class="sxs-lookup"><span data-stu-id="f9657-117">Supported messages</span></span>  
 <span data-ttu-id="f9657-118">The following messages can be used with the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Execute*></span><span class="sxs-lookup"><span data-stu-id="f9657-118">The following messages can be used with the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Execute*></span></span> <span data-ttu-id="f9657-119">method to query a schedule.</span><span class="sxs-lookup"><span data-stu-id="f9657-119">method to query a schedule.</span></span>  
  
|<span data-ttu-id="f9657-120">Thông báo</span><span class="sxs-lookup"><span data-stu-id="f9657-120">Message</span></span>|<span data-ttu-id="f9657-121">Mô tả</span><span class="sxs-lookup"><span data-stu-id="f9657-121">Description</span></span>|  
|-------------|-----------------|  
|<xref:Microsoft.Crm.Sdk.Messages.QueryScheduleRequest>|<span data-ttu-id="f9657-122">Retrieves the content (existing commitments) of the schedule for a given entity.</span><span class="sxs-lookup"><span data-stu-id="f9657-122">Retrieves the content (existing commitments) of the schedule for a given entity.</span></span> <span data-ttu-id="f9657-123">Use this message to search the specified resources for an available time slot that matches the specified parameters.</span><span class="sxs-lookup"><span data-stu-id="f9657-123">Use this message to search the specified resources for an available time slot that matches the specified parameters.</span></span> <span data-ttu-id="f9657-124">The message is available on all schedulable entities.</span><span class="sxs-lookup"><span data-stu-id="f9657-124">The message is available on all schedulable entities.</span></span>|  
|<xref:Microsoft.Crm.Sdk.Messages.QueryMultipleSchedulesRequest>|<span data-ttu-id="f9657-125">Searches multiple resources for an available time slot that matches the specified parameters.</span><span class="sxs-lookup"><span data-stu-id="f9657-125">Searches multiple resources for an available time slot that matches the specified parameters.</span></span>|  
|<xref:Microsoft.Crm.Sdk.Messages.SearchRequest>|<span data-ttu-id="f9657-126">Searches for available time slots and returns a set of available `Appointment` instances (as time blocks).</span><span class="sxs-lookup"><span data-stu-id="f9657-126">Searches for available time slots and returns a set of available `Appointment` instances (as time blocks).</span></span> <span data-ttu-id="f9657-127">The message is available on the `Resource` entity or the `Service` entity.</span><span class="sxs-lookup"><span data-stu-id="f9657-127">The message is available on the `Resource` entity or the `Service` entity.</span></span>|  
  
### <a name="see-also"></a><span data-ttu-id="f9657-128">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="f9657-128">See also</span></span>  
 <span data-ttu-id="f9657-129">[Schedule and Appointment Entities](schedule-appointment-entities.md) </span><span class="sxs-lookup"><span data-stu-id="f9657-129">[Schedule and Appointment Entities](schedule-appointment-entities.md) </span></span>  
 <span data-ttu-id="f9657-130">[Sample: Schedule a Resource](sample-search-openings-schedule-resource.md) </span><span class="sxs-lookup"><span data-stu-id="f9657-130">[Sample: Schedule a Resource](sample-search-openings-schedule-resource.md) </span></span>  
 <span data-ttu-id="f9657-131">[Appointment Entities](appointment-entities.md) </span><span class="sxs-lookup"><span data-stu-id="f9657-131">[Appointment Entities](appointment-entities.md) </span></span>  
 <span data-ttu-id="f9657-132">[Appointment Entity](entities/appointment.md) </span><span class="sxs-lookup"><span data-stu-id="f9657-132">[Appointment Entity](entities/appointment.md) </span></span>  
 <span data-ttu-id="f9657-133">[Sample: Query the Schedule of a User](sample-query-working-hours-user.md) </span><span class="sxs-lookup"><span data-stu-id="f9657-133">[Sample: Query the Schedule of a User](sample-query-working-hours-user.md) </span></span>  
 [<span data-ttu-id="f9657-134">Sample: Query the Schedules of Multiple Users</span><span class="sxs-lookup"><span data-stu-id="f9657-134">Sample: Query the Schedules of Multiple Users</span></span>](sample-query-working-hours-multiple-users.md)
